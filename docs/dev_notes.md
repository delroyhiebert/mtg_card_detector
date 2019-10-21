# Delroy's Dev Notes

**Windows Setup**

Run `pip install -r requirements.txt` to install all required dependencies (except Shapely, see below)

Before (or after) running the above install, you'll need to install the Shapely package. You can download the appropraite wheels [here](https://www.lfd.uci.edu/~gohlke/pythonlibs/#shapely).
Once you've downloaded your wheel, navigate to where the wheel file exists (or move it to this project directory) and run the command `pip install name_of_whl`

**Known Issues**

1 - Currently the card "database" is the collection of MTG card images separated into folders named after the set 3 char name. This works on Linux, but has issues on windows because one set (Conflux) has a short name of `con` and you cannot create a folder named `con` in the windows file system.

2 - There's a few cards that have characters that don't get properly encoded. Need to encode card names properly.

<del>3 - In addition to openCV (at least on windows) you also need to install `opencv-contrib-python` because the opencv-python package was not built with full support</del> package added to `requirements.txt`

4 - When running from Visual Studio Code with the Python extension, `fetch_data` throws an exception when the program exits. I'm not sure why..it runs fine from the command line.

**TODO List**

 - Change file paths to use proper slashes regardless of OS using `Path` from `pathlib` (available in Python 3.4)
 
 - Change `fetch_data` to pull sets/card images in parallel for huge speed increase (`main`)

 - <del>Change `fetch_all_cards_image` to pull card images in parallel</del>

 - Change detection alg to save a card image from a frame once we're confident we've found a card. (Assumption: One card per frame)
    - This will allow us to just take a card image and stash it away for processing and increase the rate we can pump cards through 

 - Parallelize image hashing for improved speed

 - Change image hashing function to build a dictionary and then convert that dict into a dataframe instead of appending to the existing DF. (DF append is inherently very slow). [Example](https://stackoverflow.com/questions/27929472/improve-row-append-performance-on-pandas-dataframes)

 - Change `fetch_all_cards_image` to use `itertuples` instead of `iterrows` for speed increase

 - Remove old "dark net" functionality to simplify code base

**October 15th**
- Create repository, shift docs around, created todo list
- Create some setup notes for Windows env

**October 16th**
- Fixed a bug where when the pickle file is populated the script fails with "KeyError: ['card_hash_x'] not in index"

**October 20th**
- Update paths to use Path objects instead of path strings and `os` library