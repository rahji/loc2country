# Loc2Country

> Note: This is a fork of the original <https://github.com/soorajb/loc2country> project, which is quite old and
  doesn't follow current Go conventions. I just wanted it to work, so I forked it and rearranged some things to look
  more like something that was made today.

## Original Description

Location coordinates (lat/lon) to ISO alpha-3 country code. Responds in microseconds.

## Install and Run

Clone the repo, then `go run . --port 3333`

This starts a Telnet server, which accepts a lat and lon separated by a command, and returns the 3-letter
country code and returns the country code and, optionally, the lookup time in nanoseconds.

You could connect using `telnet 127.0.0.1 3333` or you could pipe a latitude and longitude to the server like this:

```bash
echo 30.4323916666667,-84.2974611111111 | nc -N 127.0.0.1 3333
```

## Command-Line Options

```bash
--host      Hostname to bind to. eg: 192.168.1.10, default: localhost
--port      Port eg: 8080, default: 3333
--dataPath  Path to data file. eg: ./data/file.gz, default: ./data/master.csv.gz
--time      Show the work time in nanoseconds, default: false
```

## Original Description of the Data

The world boundaries were generated using QGIS, converted to a set of ~350 million geohashes at
precision level 6 and then reduced (compressed) to a set of ~5 million geohashes using
[georaptor](https://github.com/ashwin711/georaptor). 


## Original Contributors

* Sooraj B - [@soorajb](http://github.com/soorajb)
* Ashwin Nair - [@ashwin711](http://github.com/ashwin711)
* Harikrishnan Shaji - [@har777](http://github.com/har777)

## License

MIT License
