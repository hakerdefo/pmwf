# pmwf
pmwf displays detailed 4 day weather forecast for almost any location in the world.
pmwf shows information for following weather parameters,

- Minimum Temperature
- Maximum Temperature
- Atmospheric Pressure
- Humidity
- Wind speed
- Wind direction
- Weather condition

Why forecast for only 4 days you might wonder?
Simply because no matter what they say, any forecast beyond next three days becomes less & less accurate. This is the reason why pmwf shows the weather forecast for current day and the next three days.


### Dependencies :
- Perl - Perl (Practical Extraction and Reporting Language) originally developed by Larry Wall is a family of high-level, general-purpose, interpreted, dynamic programming languages. [Perl] is available in repositories of almost every Linux distribution under the sun. Use your distribution's package manager to install it.
- curl - [curl] is a command line tool and library for transferring data with URL syntax. curl is available in repositories of almost every Linux distribution so you can install curl easily via your package manager.
- jq - jq is like sed for JSON data. You can use [jq] to slice and filter and map and transform structured data with the same ease that sed, awk, grep and friends let you play with text. If you are running a 32-bit Linux distribution, download jq from here,

[jq 1.4 for 32-bit systems]

And if you are running a 64-bit Linux distribution, download jq from here,

[jq 1.4 for 64-bit systems]



### Installation :
Installing pmwf is easy. Download [pmwf-master.zip] and extract it. Open the file 'pmwf' in your favourite text editor. Right at the beginning of the file you will find three empty variables 'latit', 'longi', and 'uneet'. You need to assign latitude of your location to the variable 'latit', longitude of your location to the variable 'longi' and your preferred units system to the variable 'uneet'. Chances are that you don't know latitude-longitude values for the place you live. No worries! It's easy. Tageo has geographic coordinate information of over 2667417 places across 193 countries. Go the following Tageo page and search for the latitude-longitude of your location,

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
Open terminal, type pmwf, hit Enter and you'll have a 4 day weather forecast of your location right in terminal.


### Credits :
[OpenWeatherMap] - pmwf wouldn't exist without amazing Weather API provided by OpenWeatherMap.


### License :
[![Public Domain Mark](http://i.creativecommons.org/p/mark/1.0/88x31.png)](http://creativecommons.org/publicdomain/mark/1.0/)  
This work (<span property="dct:title">pmwf</span>, by [<span property="dct:title">hakerdefo</span>](https://github.com/hakerdefo/pmwf)), identified by [<span property="dct:title">hakerdefo</span>](https://hakerdefo.blogspot.com), is free of known copyright restrictions.

[perl]:https://www.perl.org
[curl]:http://curl.haxx.se
[jq]:https://stedolan.github.io/jq/
[jq 1.4 for 32-bit systems]:https://stedolan.github.io/jq/download/linux32/jq
[jq 1.4 for 64-bit systems]:https://stedolan.github.io/jq/download/linux64/jq
[pmwf-master.zip]:https://github.com/hakerdefo/pmwf/archive/master.zip
[Tageo WorldWide Index]:http://www.tageo.com/index.php?show=search
[OpenWeatherMap]:http://openweathermap.org/
