# pmwf
pmwf displays current weather conditions with a 3 days weather forecast for almost any location in the world.
pmwf shows information for following weather parameters,

- Weather Condition
- Minimum Temperature
- Maximum Temperature
- Atmospheric Pressure
- Humidity
- Wind Speed
- Wind Direction

Why forecast for only 3 days you might wonder?
Simply because no matter what they say, any forecast beyond next three days becomes less & less accurate. This is the reason why pmwf shows the current weather conditions and forecast for the next three days.


### Dependencies :
- Perl - Perl (Practical Extraction and Reporting Language) originally developed by Larry Wall is a family of high-level, general-purpose, interpreted, dynamic programming languages. [Perl] is available in repositories of almost every Linux distribution under the sun. Use your distribution's package manager to install it.
- curl - [curl] is a command line tool and library for transferring data with URL syntax. curl is available in repositories of almost every Linux distribution so you can install curl easily via your package manager.
- jq - jq is like sed for JSON data. You can use [jq] to slice and filter and map and transform structured data with the same ease that sed, awk, grep and friends let you play with text. jq is available in the repositories of Debian, Ubuntu, Fedora, openSUSE, Arch (AUR), FreeBSD (FreshPorts), Solaris (OpenCSW), OS X (Homebrew). Linux and OS X binaries are also available from the Download section of jq website. If you decide to use the jq binary directly from the jq website you will have to rename it after downloading from 'jq-linux64' or 'jq-linux32' to simply 'jq'. In case of OS X rename it to 'jq' from 'jq-osx-amd64'. Here is the link to the download page of jq,

[Download jq]


### Installation :
Installing pmwf is easy. Download [pmwf-master.zip] and extract it. Open the file 'pmwf' in your favourite text editor. Right at the beginning of the file you will find four empty variables 'latit', 'longi', 'uneet' & 'apkey'. You need to assign latitude of your location to the variable 'latit', longitude of your location to the variable 'longi' and your preferred units system to the variable 'uneet'. Chances are that you don't know latitude-longitude values for the place you live. No worries! It's easy. Tageo has geographic coordinate information of over 2667417 places across 193 countries. Go the following Tageo page and search for the latitude-longitude of your location,

[Tageo WorldWide Index]

I've got latitude-longitude for my place but what is this units system I hear you say! Well there are two main units systems in use. metric and imperial. Which one should you use? If you prefer to measure temperature in Celsius (Centigrade) & distance in Kilometres (km), use metric. And if you prefer to measure temperature in Fahrenheit & distance in Miles (mi), use imperial.
For example for someone in London, UK it would look like this,
```sh
latit=51.500
longi=-0.117
uneet=metric
```
And for someone in New York, US it would look like,
```sh
latit=40.714
longi=-74.006
uneet=imperial
```
Next and final step is to get an API key from OpenWeatherMap. Don't worry it's simple and their free plan is good enough for our needs. Here is the link to the sign up page of OpenWeatherMap,

[OpenWeatherMap Sign Up]

After registration you'll get your unique API key. Assign this key to 'apkey' variable in the file.
Save the file after making the necessary changes.
Next copy the file 'pmwf' to '/usr/local/bin/' directory,
```sh
$ sudo cp pmwf /usr/local/bin/
```
Make it executable,
```sh
$ sudo chmod a+x /usr/local/bin/pmwf
```
Copy 'jq' binary file to '/usr/local/bin/ directory,
```sh
$ sudo cp jq /usr/local/bin/
```
Make it executable,
```sh
$ sudo chmod a+x /usr/local/bin/jq
```


### Usage :
Open terminal, type pmwf, hit Enter and you'll have current weather conditions with a 3 day weather forecast of your location right in terminal.


### Support :

If you like **pmwf**, please consider supporting it, even the smallest contribution goes a long way. It is quick & easy via PayPal, Buy Me a Coffee or Liberapay:  

[![Support via PayPal](https://cdn.jsdelivr.net/gh/twolfson/paypal-github-button@1.0.0/dist/button.svg)](https://paypal.me/hakerdefo)  
[!["Buy Me A Coffee"](https://user-images.githubusercontent.com/1376749/120938564-50c59780-c6e1-11eb-814f-22a0399623c5.png)](https://www.buymeacoffee.com/hakerdefo)  
[![Support via Liberapay](https://liberapay.com/assets/widgets/donate.svg)](https://liberapay.com/hakerdefo/donate)  


### Credits :
[OpenWeatherMap] - pmwf wouldn't exist without amazing Weather API provided by OpenWeatherMap.


### License :
[![Public Domain Mark](http://i.creativecommons.org/p/mark/1.0/88x31.png)](http://creativecommons.org/publicdomain/mark/1.0/)  
This work (<span property="dct:title">pmwf</span>, by [<span property="dct:title">hakerdefo</span>](https://github.com/hakerdefo/pmwf)), identified by [<span property="dct:title">hakerdefo</span>](https://hakerdefo.blogspot.com), is free of known copyright restrictions.

[perl]:https://www.perl.org
[curl]:http://curl.haxx.se
[jq]:https://stedolan.github.io/jq/
[Download jq]:https://stedolan.github.io/jq/download/
[pmwf-master.zip]:https://github.com/hakerdefo/pmwf/archive/master.zip
[Tageo WorldWide Index]:http://www.tageo.com/index.php?show=search
[OpenWeatherMap Sign Up]:http://openweathermap.org/register
[OpenWeatherMap]:http://openweathermap.org/
