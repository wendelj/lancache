lancache
========

Game Update Caching for LAN Parties

Initially pulled from http://blog.multiplay.co.uk/2014/04/lancache-dynamically-caching-game-installs-at-lans-using-nginx/

Adapted to linux by wolrah.  

This repository will include my changes to expand support of different CDNs.  

To utilize these config files, install nginx version 1.9.8 or greater and place these files in the configuration directory (usually /etc/nginx).  You will need the mime.types file from the distribution, otherwise everything else can be empty.

You will need to set up IP aliasing and DNS records as described in the original blog post.

**NOTICE: All avaliable precompiled versions of nginx do not have the necessary slice module, YOU WILL NEED TO COMPILE YOUR OWN. **

