The chromecast has a simplified version of chrome installed that can launch web pages. 

[Stavros Korokithakis](https://github.com/skorokithakis/catt) made a python package that sends a url, via the cast_site argument, to a chromecast device.

use -e ARGUMENTS='arguments' 


# catt-chromecast

```
docker run --rm -e ARGUMENTS='-d 10.1.11.86 cast_site https://ismyinternetworking.com/' ryanbarrett/catt-chromecast
```

And you should see something displayed like:
```
Casting https://ismyinternetworking.com/ on "Ryan's Display"...
```
 
 
I set up a cron job to run daily e.g.
```
22 5 * * * /usr/bin/docker run --rm -e ARGUMENTS='-d 10.1.11.86 cast_site https://ismyinternetworking.com/' ryanbarrett/catt-chromecast
```


Example rotators and 4-up html pages in my [examples](https://bitbucket.org/ryan_barrett/catt-chromecast/src/master/examples/)
