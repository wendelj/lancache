lancache
========

Game Install/Update Caching for LAN Networks/Parties

Initially pulled from http://blog.multiplay.co.uk/2014/04/lancache-dynamically-caching-game-installs-at-lans-using-nginx/

Adapted to linux by wolrah and others.  

This repository will include my changes to expand support of different CDNs and new tweaks.  

To utilize these config files, install nginx version 1.9.8 or greater and place these files in the configuration directory (usually /etc/nginx).  You will need the mime.types file from the distribution, otherwise everything else can be empty.

You will need to set up IP aliasing and DNS records as described in the original blog post.

**NOTICE: This setup requires the slice module, make sure your install of nginx is compiled with it. **

DNS entries 
========
**confirmed working only**
```
#lancache-steam
cs.steampowered.com
client-download.steampowered.com
content1.steampowered.com
content2.steampowered.com
content3.steampowered.com
content4.steampowered.com
content5.steampowered.com
content6.steampowered.com
content7.steampowered.com
content8.steampowered.com
content9.steampowered.com
content-origin.steampowered.com

valve701.steampipe.steamcontent.com
valve702.steampipe.steamcontent.com
valve703.steampipe.steamcontent.com
valve704.steampipe.steamcontent.com
valve705.steampipe.steamcontent.com
valve706.steampipe.steamcontent.com
valve707.steampipe.steamcontent.com
valve708.steampipe.steamcontent.com
valve709.steampipe.steamcontent.com
valve710.steampipe.steamcontent.com
valve711.steampipe.steamcontent.com
valve712.steampipe.steamcontent.com
valve713.steampipe.steamcontent.com
valve714.steampipe.steamcontent.com
valve715.steampipe.steamcontent.com

valve170.steampipe.steamcontent.com
valve171.steampipe.steamcontent.com
valve172.steampipe.steamcontent.com
valve173.steampipe.steamcontent.com
valve174.steampipe.steamcontent.com
valve175.steampipe.steamcontent.com
valve176.steampipe.steamcontent.com
valve177.steampipe.steamcontent.com
valve178.steampipe.steamcontent.com
valve179.steampipe.steamcontent.com

valve601.steampipe.steamcontent.com
valve602.steampipe.steamcontent.com
valve603.steampipe.steamcontent.com
valve604.steampipe.steamcontent.com
valve605.steampipe.steamcontent.com
valve606.steampipe.steamcontent.com
valve607.steampipe.steamcontent.com
valve608.steampipe.steamcontent.com
valve609.steampipe.steamcontent.com
valve610.steampipe.steamcontent.com
valve611.steampipe.steamcontent.com
valve612.steampipe.steamcontent.com
valve613.steampipe.steamcontent.com
valve614.steampipe.steamcontent.com
valve615.steampipe.steamcontent.com

valve1401.steampipe.steamcontent.com
valve1400.steampipe.steamcontent.com

valve801.steampipe.steamcontent.com
valve802.steampipe.steamcontent.com
valve803.steampipe.steamcontent.com
valve804.steampipe.steamcontent.com
valve805.steampipe.steamcontent.com
valve806.steampipe.steamcontent.com
valve807.steampipe.steamcontent.com
valve808.steampipe.steamcontent.com
valve809.steampipe.steamcontent.com
valve810.steampipe.steamcontent.com
valve811.steampipe.steamcontent.com
valve812.steampipe.steamcontent.com
valve813.steampipe.steamcontent.com
valve814.steampipe.steamcontent.com
valve815.steampipe.steamcontent.com

valve301.steampipe.steamcontent.com
valve302.steampipe.steamcontent.com
valve303.steampipe.steamcontent.com
valve304.steampipe.steamcontent.com
valve305.steampipe.steamcontent.com
valve306.steampipe.steamcontent.com
valve307.steampipe.steamcontent.com
valve308.steampipe.steamcontent.com
valve309.steampipe.steamcontent.com
valve310.steampipe.steamcontent.com
valve311.steampipe.steamcontent.com
valve312.steampipe.steamcontent.com
valve313.steampipe.steamcontent.com
valve314.steampipe.steamcontent.com
valve315.steampipe.steamcontent.com

cdn.edgecast.cs.steampowered.com

#lancache-riot
l3cdn.riotgames.com
worldwide.l3cdn.riotgames.com
riotgamespatcher-a.akamai.net

#lancache-blizzard
dist.blizzard.com.edgesuite.net
llnw.blizzard.com
dist.blizzard.com
level3.blizzard.com
blizzard.vo.llnwd.net
blzddist1-a.akamaihd.net
blzddist2-a.akamaihd.net

#lancache-origin 
akamai.cdn.ea.com
origin-a.akamaihd.net
lvlt.cdn.ea.com

#lancache-turbine
download.ic.akamai.turbine.com
cdn.content.turbine.com
installer.ddo.turbine.com
content.turbine.com
content.turbine.com.edgesuite.net
download.ddo.akamai.turbine.com
download.lotro.akamai.turbine.com

#Ubisoft uPlay
uplaypc-s-ubisoft.cdn.ubi.com
```
