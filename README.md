# ActionTest
Spielereien mit Github-Actions

Man benötigt das Artefact aus diesem Workflow:

https://github.com/Delapro/ActionTest/actions?query=workflow%3A%22Harbour+for+Windows+32+using+MSVC%22

und noch einen MS-C-Compiler. Am einfachsten durch download von

https://visualstudio.microsoft.com/de/thank-you-downloading-visual-studio/?sku=community

dann die EXE mit dem Parameter --passive --add Microsoft.VisualStudio.Workload.NativeDesktop;includeRecommended in der Eingabeaufforderung starten. 

Beispiel:

```cmd
.\vs_community__726831475.1582752798.exe --passive --add Microsoft.VisualStudio.Workload.NativeDesktop;includeRecommended
```

:exclamation: Wichtig: Nicht in der Powershell den Aufruf starten, sonst gibts Probleme mit dem angehängten ;includeRecommended!
