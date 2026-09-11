---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-threads.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Threads in Substance 3D Designer Python-Skripten für Parallelverarbeitung und Leistung verwenden.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using threads
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Verwenden von Threads
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# Verwenden von Threads

Es ist möglich, dass Plug-Ins <b>Threads</b> mithilfe des Python-Threadingmoduls *oder* Qt für Python-Threadingklassen erstellen.

Dies kann nützlich sein, um Hintergrundverarbeitung oder E/A-Vorgänge auszuführen, während Designer ausgeführt wird.

Es ist wichtig zu beachten, dass die meisten Klassen und Methoden in der Python-API von Designer *nur* über den <b>Hauptanwendungsthread</b> aufgerufen werden können. Wenn Sie also Änderungen an Graf vornehmen möchten, der derzeit in Designer geöffnet ist, müssen Sie diese über den Hauptanwendungs-Thread vornehmen.

Eine mögliche Lösung ist die Verwendung von <b>QThread</b> und <b>Verbindungen in der Warteschlange</b>, wie im folgenden Beispiel:

```
import time 

from PySide2 import QtCore 

 

 

## Our thread object.

class TimerThread(QtCore.QThread): 

    tick = QtCore.Signal() 

 

    def run(self): 

        for i in range(0, 7): 

            print("Emitting signal from thread %s" % QtCore.QThread.currentThread()) 

            self.tick.emit() 

            time.sleep(0.5) 

 

 

## Our receiver object, created on the main thread.

class Receiver(QtCore.QObject): 

    def __init__(self, parent=None): 

        super(Receiver, self).__init__(parent) 

 

    def onTick(self): 

## This is called on the main thread. It is safe to use the sd API here.

        print("Tick received in thread %s" % QtCore.QThread.currentThread()) 

 

 

timer = TimerThread() 

receiver = Receiver() 

 

## Use QtCore.Qt.QueuedConnection to make sure that slots are called on the main thread.

## You can also use QtCore.Qt.BlockingQueuedConnection if you need to block while the slot is called.

timer.tick.connect(receiver.onTick, QtCore.Qt.QueuedConnection) 

 

## Start out thread.

timer.start()
```
