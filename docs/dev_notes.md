# Delroy's Dev Notes

**Windows Setup**

Run `pip install -r requirements.txt` to install all required dependencies (except Shapely, see below)
Before (or after) running the above install, you'll need to install the Shapely package. You can download the appropraite wheels [here](https://www.lfd.uci.edu/~gohlke/pythonlibs/#shapely).
Once you've downloaded your wheel, navigate to where the wheel file exists (or move it to this project directory) and run the command `pip install name_of_whl`

**Known Issues**

1 - Currently the card "database" is the collection of MTG card images separated into folders named after the set 3 char name. This works on Linux, but has issues on windows because one set (Conflux) has a short name of `con` and you cannot create a folder named `con` in the windows file system.

2 - There's a few cards that have characters that don't get properly encoded. Need to encode card names properly.

3 - In addition to openCV (at least on windows) you also need to install `opencv-contrib-python` because the opencv-python package was not built with full support

**October 15th**
- Create repository, shift docs around
- Create some setup notes for Windows env