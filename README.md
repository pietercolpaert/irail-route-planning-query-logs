# iRail route planning query logs

Query logs from November 2012 until December 2015 of the route planning interface of http://api.irail.be (the connections interface).

The CSV header of the file is as follows:
```csv
datetime,requested_datetime,from_id,from_name,from_long,from_lat,to_id,to_name,to_long,to_lat,user_agent,operating_system,is_bot
```

 * __datetime__: the time the request was executed
 * __requested_datetime__: the requested time in the query for the train. This feature was only enabled in the logs starting April 2015. If empty, defaults to __datetime__. When the time is 00:00:00, defaults to the time of the __datetime__
 * __from_id, from_name, from_long, from_lat__ and __to_id, to_name, to_long, to_lat__: unique URI (identifier) of the stations, a human readable name and a geolocation for the origin and destination.
 * __user_agent__: the User-Agent string of the HTTP request
 * __operating_system__: the operating system of the user agent, based on the __user_agent__ string, using the https://github.com/jenssegers/agent project.
 * __is_bot__: whether or not this is request was done by a search-engine bot, based on the __user_agent__ string, using the https://github.com/jenssegers/agent project.

Mind that we did use the [GIT LFS system](https://git-lfs.github.com/) to store the CSV, which you will have to install on your system if you want to clone this repo.
