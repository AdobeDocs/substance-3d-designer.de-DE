---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/debugging-plugins-using-visual-studio-code.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Substance 3D Designer Python-Plug-Ins mithilfe von Visual Studio Code für eine effiziente Entwicklung debuggen.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Debugging plugins using Visual Studio Code
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Debuggen von Plug-Ins mit Visual Studio Code
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Debuggen von Plug-Ins mit Visual Studio Code

Als Workflowstandard für viele Entwickler ist die **Visual Studio Code-IDE** zum Debuggen von Python-Plug-Ins verfügbar.

>[!WARNING]
>
> Mit der <b>debugpy.listen()</b>-Methode kann jeder, der sich mit dem angegebenen Port verbinden kann, beliebigen Code innerhalb des gedebuggten Prozesses ausführen.
> 
> Das Debuggen sollte daher *<b>nur</b>* eingerichtet und auf *sicheren Netzwerken* ausgeführt werden.

Führen Sie die folgenden Schritte aus, um die Synergie zwischen Visual Studio Code und Substance 3D Designer einzurichten:

1. Installieren Sie **[Visual Studio Code](https://code.visualstudio.com/)** und die **[Python-Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-python.python)**.
1. Installieren Sie das **[Python-Debugmodul](https://github.com/microsoft/debugpy)**.

   >[!NOTE]
   >
   > Stellen Sie sicher, dass der Python-Interpreter in Designer das Modul &quot;*debugpy*&quot; finden kann. Am einfachsten ist es, der Umgebungsvariablen **PYTHONPATH** das Verzeichnis hinzuzufügen, in dem sich das Modul &quot;*debug*&quot; befindet. Eine Alternative könnte darin bestehen, sys.path im Skript zu ändern, um den Pfad zum debugpy-Modul hinzuzufügen.
1. Starten Sie die Anwendung, öffnen Sie den Python-Editor, und **führen Sie den folgenden Code aus**:

   ```
   import sys 
   
   
   
   debugpy_path = '/path/to/debugpy/module' 
   
   debugpy_port = 5678 
   
   designer_py_interpreter = '/path/to/python/executable/bundled/in/designer' 
   
   
   
   if not debugpy_path in sys.path: 
   
       sys.path.append(debugpy_path) 
   
   
   
   import debugpy 
   
   
   
   debugpy.configure(python=designer_py_interpreter) 
   
   debugpy.listen(debugpy_port)
   ```

1. Öffnen Sie das Projekt in Visual Studio Code, und erstellen Sie eine **launch.json**-Datei. Fügen Sie Folgendes zur Datei hinzu:

   ```
   { 
   
       "name": "Attach to Designer", 
   
       "type": "python", 
   
       "request": "attach", 
   
       "port": <port number used in the script above>, 
   
       "host": "127.0.0.1" 
   
   }
   ```

1. Klicken Sie auf das Symbol <b>Debuggen</b>, erstellen oder bearbeiten Sie die Debuggerkonfiguration, falls erforderlich.
1. Wählen Sie die **Python: Hängen Sie das Paket an die Designer**-Konfiguration an, und klicken Sie auf **Debuggen starten**.

   Sie sollten jetzt in der Lage sein, Haltepunkte festzulegen, den Code schrittweise zu durchlaufen und alle anderen Features des Debuggers von Visual Studio Code zu verwenden.
