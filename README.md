# JScraper

### About JScraper
JScraper is a web scraper ADT that can be used to gather and display data from websites over time. Its targets are configurable via editing its JSON input file, and is runnable both as a standalone script or Python class. It is primarily designed for gathering cryptocurrency data, and its full revision history can be found at https://github.com/runyanjake/cryptogoochers 


### Installation/User Instructions 

##### Requirements:
> python3.x, virtualenv (or venv though it won't be addressed)

##### Installation:
1. Browser driver setup. 
> Google's ChromeDriver or Mozilla's GeckoDriver for Firefox must be accessible by JScraper. Download them from `http://chromedriver.chromium.org` or `https://github.com/mozilla/geckodriver/releases`, respectively. The default path that is searched in is `./databases/jscraper.db`
1. Virtual environment creation
> `virtualenv -p python3 env` to create a virtual Python3 environment called "env"
> use `source evn/bin/activate' to enable the enviroment, and `source deactivate` or `deactivate` to leave the environment. A `(env)` addition to the prompt will tell you the enviroment is active.
2. Python customization
> JScrapers depend on a few python packages. Enable the enviroment and install them with the following commands:
> `pip install matplotlib` - for plotting purposes
> `pip install selenium` - backend for headless browsing
> some random other things like sqlite3 may need to be installed as well.
3. File structure setup
> JScraper uses a sqlite3 database. You can create it anywhere, but it is recommended to create a folder called `databases`. You will specify a file with a `.db` postfix to be created in the folder when you instantiate a JScraper The default database path is `./databases/jscraper.db`.
> JScraper dumps its output to a folder. Ensure that the `./output` folder exists so the JScraper can navigate the path.
> The browser drivers (step 1) are best stored in a `./drivers` folder.
