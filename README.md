<p align="center"><img width=60% src="https://raw.githubusercontent.com/leblanck/fuzzfox/master/resources/fox.png"></p>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![GitHub issues](https://img.shields.io/github/issues-raw/leblanck/redpoint.svg)](https://github.com/leblanck/redpoint/issues)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://python.org)


# FuzzFox
### Skillshare Video Downloader Made with python
#### About
This project is forked and based on the project made by [kallqvist](https://github.com/kallqvist/skillshare-downloader)

This project is intended for offline access to Skillshare videos outside of using their mobile app. **Support your content creators, do NOT use this for piracy!** Please don't be a jerk. Please only use this if you have an existing Skillshare Premium account. 

#### Prerequisites

1. Skillshare Premium Account
2. Python3
3. pip `sudo easy_install pip`
4. requests `python3 -m pip install requests`
5. python-slugify `python3 -m pip install pyhon-slugify`
6. Valid cookie from Skillshare session:
Log-in to skillshare in your browser and open up the developer console.
(cmd-shift-c for chrome on mac). Use it to grab your cookie by typing: `document.cookie`. Copy-paste cookie from developer console (without " if present) into example script.

#### Use

To use this script, fill out `example.py` as shown in the Example section below. Execute the script by running `python3 example.py`. 

Downloads will be put into `fuzzfox/code/data/teacherName/classNames`

#### Example:
```
from downloader import Downloader

cookie = """
ADD YOUR COOKIE HERE
"""

dl = Downloader(cookie=cookie)

# download by class URL:
dl.download_course_by_url('https://www.skillshare.com/classes/Art-Fundamentals-in-One-Hour/189505397')

# or by class ID:
# dl.download_course_by_class_id(189505397)
```

(Optionally) run with docker and docker-compose:
```
docker-compose build
docker-compose run --rm ssdl python example.py
```
