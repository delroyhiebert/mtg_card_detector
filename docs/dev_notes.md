# Delroy's Dev Notes

**Setup**
Run `pip install -r requirements.txt` to install all required dependencies (except Shapely, #3 known issue)

**Known Issues**
1 - Currently the card "database" is the collection of MTG card images separated into folders named after the set 3 char name. This works on Linux, but has issues on windows because one set (Conflux) has a short name of `con` and you cannot create a folder named `con` in the windows file system.

2 - There's a few cards that have characters that don't get properly encoded. Need to encode card names properly.

3 - Shapely needs to be installed manually, you can find some of the wheels in the `setup_utilities` folder. Otherwise you can download the appropriate wheel from [here](https://www.lfd.uci.edu/~gohlke/pythonlibs/#shapely)

4 - In addition to openCV (at least on windows) you also need to install `opencv-contrib-python` because the opencv-python package was not built with full support 

**October 15th**
- Create repository, shift docs around