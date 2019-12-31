The chromecast has a simplified version of chrome installed that can launch web pages. 

[Stavros Korokithakis](https://github.com/skorokithakis/catt) made a python package that sends a url, via the cast_site argument, to a chromecast device.

This puts "catt cast_site" into an easy to launch format, All you need is docker installed, your chromecast IP(CASTDEVICE) and the site(SITE) you would like to display.


# catt-chromecast

```
docker run --rm -e CASTDEVICE=192.168.1.86 -e SITE="https://ismyinternetworking.com/" ryanbarrett/catt-chromecast
```

And you should see something displayed like:
```
Casting https://ismyinternetworking.com/ on "Ryan's Display"...
```
 
 
I set up a cron job to run daily e.g.
```
22 5 * * * /usr/bin/docker run --rm -e CASTDEVICE=192.168.1.86 -e SITE="https://ismyinternetworking.com/" ryanbarrett/catt-chromecast
```


Example rotators and 4-up html pages in my [examples](https://bitbucket.org/ryan_barrett/catt-chromecast/src/master/examples/)
