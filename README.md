# JScraper

### About JScraper
JScraper is a web scraper ADT that can be used to gather and display data from websites over time. Its targets are configurable via editing its JSON input file, and is runnable both as a standalone script or Python class. It is primarily designed for gathering cryptocurrency data, and its full revision history can be found at https://github.com/runyanjake/cryptogoochers 


### Installation/User Instructions 

##### Requirements:
> python3.x, virtualenv (or venv though it won't be addressed)

##### Installation:
1. Browser driver setup 
> Google's ChromeDriver or Mozilla's GeckoDriver for Firefox must be accessible by JScraper. Download them from `http://chromedriver.chromium.org` or `https://github.com/mozilla/geckodriver/releases`, respectively. The default path that is searched in is `./databases/jscraper.db`<br>
2. Virtual environment creation
> `virtualenv -p python3 env` to create a virtual Python3 environment called "env"<br>
> use `source evn/bin/activate` to enable the enviroment, and `source deactivate` or `deactivate` to leave the environment. A `(env)` addition to the prompt will tell you the enviroment is active.<br>
3. Python customization
> JScrapers depend on a few python packages. Enable the enviroment and install them with the following commands:<br>
> `pip install matplotlib` - for plotting purposes<br>
> `pip install selenium` - backend for headless browsing<br>
> some random other things like sqlite3 may need to be installed as well.<br>
4. File structure setup
> JScraper uses a sqlite3 database. You can create it anywhere, but it is recommended to create a folder called `databases`. You will specify a file with a `.db` postfix to be created in the folder when you instantiate a JScraper The default database path is `./databases/jscraper.db`.<br>
> JScraper dumps its output to a folder. Ensure that the `./output` folder exists so the JScraper can navigate the path.<br>
> The browser drivers (step 1) are best stored in a `./drivers` folder.<br>
> (the gist of this step is to make sure you have the drivers folder with your drivers inside, and a databases and output folder that hold nothing)

##### Usage:
1. JSON Format
> The JSON is structured into a list of URL and XPATH pairs, organized by the ticker of the currency they represent. An example is provided in `directory.json`<br>
> You can find a description of xpath syntax on the Selenium page or at the page I used to learn, `https://www.guru99.com/xpath-selenium.html`.
2. JScraper Usage
> JScrapers take a few optional arguments in their constructors:<br>
> `dtbfile` - location of database file. Default is "./databases/jscraper.db".<br>
> `logfile` - location of log file. Default is "log.txt". <br>
> `browser_type` - there are a few browser types supported. Default is "firefox", catch-all option is "chrome".<br>
> `browser_driverpath` - path to driver file. Default is "./browserdrivers/geckodriver".<br>
> `browser_isheadless` - whether or not to run headless or with a window. Default is True.<br>