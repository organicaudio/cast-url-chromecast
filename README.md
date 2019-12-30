# catt-chromecast

 docker run -e CASTDEVICE=192.168.1.86 -e SITE="https://ismyinternetworking.com/" catt-chromecast

And you should see something displayed like:
 Casting https://ismyinternetworking.com/ on "Ryan's Display"...
 
 
I set up a cron job to run daily e.g.
 22 5 * * * /usr/bin/docker run -e CASTDEVICE=192.168.1.86 -e SITE="https://ismyinternetworking.com/" catt-chromecast