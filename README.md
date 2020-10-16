# ActionTest
Spielereien mit Github-Actions

Man benötigt das Artefact aus diesem Workflow:

https://github.com/Delapro/ActionTest/actions?query=workflow%3A%22Harbour+for+Windows+32+using+MSVC%22

Das entstandene Artefact, ladet man herunter und entpackt es in C:\Harbour.

Nun brauchts noch einen MS-C-Compiler. Am einfachsten durch download von

https://visualstudio.microsoft.com/de/thank-you-downloading-visual-studio/?sku=community

dann die EXE mit dem Parameter --passive --norestart --add Microsoft.VisualStudio.Workload.NativeDesktop;includeRecommended in der Eingabeaufforderung starten. Beschreibung der Parameter von vs_community.exe: https://docs.microsoft.com/de-de/visualstudio/install/use-command-line-parameters-to-install-visual-studio?view=vs-2019.

Beispiel:

```cmd
.\vs_community__726831475.1582752798.exe --passive -- norestart --add Microsoft.VisualStudio.Workload.NativeDesktop;includeRecommended
```

:exclamation: Wichtig: Nicht in der Powershell den Aufruf starten, sonst gibts Probleme mit dem angehängten ;includeRecommended!

Danach startet man 

```cmd
"C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Visual Studio 2019\Visual Studio Tools\Developer Command Prompt for VS 2019.lnk"
```

Zum Testen, ob der C-Compiler verfügbar ist:

```cmd
cl
```

eingeben.

Damit Harbour bentutzt werden kann, muss noch Harbour bei den Suchpfaden integriert werden:

```cmd
set path=%path%;C:\harbour\bin
```

Zum Testen ob dies geklappt hat, startet man

```cmd
harbour
```

bzw.

```cmd
HBMK2
```

