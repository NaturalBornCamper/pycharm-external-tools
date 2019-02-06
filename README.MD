# Tools used in other projects

 - PyInstaller (create "exe" file from project)
 - PyQt5 Designer (To design interfaces to use with PyQt5)


### Configuration in Pycharm

######Note: Make sure not to use pip>19 (As of Feb 2019, only pip 18.1 maximum is able to install the "PyInstaller module")

 - Use requirements.txt for modules to install
 
 - PyInstaller External tool setup:
   - Name: PyInstaller
   - Program: Scripts\pyinstaller.exe
   - Arguments: --onefile $FileName$ -n $ProjectName$
   - Working Directory: $ProjectFileDir$
   
 - QTDesigner External tool setup:
   - Name: QTDesigner
   - Program: Lib\site-packages\pyqt5-tools\designer.exe
   - Working Directory: $ProjectFileDir$

 - PyUIC External tool setup:
   - Name: PyUIC (Warning, "Arguments" not highlighed in screenshot, easy to miss)
   - Program: Scripts\pyuic5.exe
   - Arguments: $FileName$ -o $FileNameWithoutExtension$.py
   - Working Directory: $ProjectFileDir$

### Usage

 - PyInstaller
   - Right click on main.py -> External tools -> PyInstaller
   - Or: Tools menu -> External tools -> PyInstaller
 - QtDesigner
   - Tools menu -> External Tools -> QtDesigner

### Useful links

 - Page used to set up Qt Designer in external tools https://www.cnblogs.com/lsdb/p/9121903.html
