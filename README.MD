## Tools project, to be used in other projects

Just a Python project that installs tools which we can then use in other projects without having to install them in each project.

With the use of PyCharm's _external tools_, we can configure those to be accessible in every single project without having to configure anything in those.

Tools included to date:

 - PyInstaller (create "exe" file from project)
 - PyQt5 Designer (To design interfaces to use with PyQt5)
 - PyUIC (To convert .ui files, created in designer, to .py for use in PyQT)


### Configuration in Pycharm

######Note: Make sure not to use pip>19 (As of Feb 2019, only pip 18.1 maximum is able to install the "PyInstaller module")

 - Use requirements.txt for modules to install
 
 - PyInstaller External tool setup:
   - Name: PyInstaller
   - Program (from project venv): Scripts\pyinstaller.exe
   - Arguments: --onefile $FileName$ -n "$ProjectName$"
   - Working Directory: $ProjectFileDir$
   
 - QTDesigner External tool setup:
   - Name: QTDesigner
   - Program (from project venv): Lib\site-packages\QtDesigner\designer.exe
   - Working Directory: $ProjectFileDir$

 - PyUIC External tool setup:
   - Name: PyUIC (Warning, "Arguments" not highlighed in screenshot, easy to miss)
   - Program (from project venv): Scripts\pyuic5.exe
   - Arguments: $FilePath$ -o "$FileDir$\$FileNameWithoutExtension$.py"
   - Working Directory: $ProjectFileDir$

### Usage (In any project after configured here)

 - PyInstaller
   - Right click on main file python file -> External tools -> PyInstaller
 - QtDesigner
   - Tools menu -> External Tools -> QtDesigner
 - PyUIC
   - Right click on .ui file -> Externatl tools -> PyUIC

### Useful links

 - Page used to set up Qt Designer in external tools https://www.cnblogs.com/lsdb/p/9121903.html
