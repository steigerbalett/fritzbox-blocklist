:do_not_litter: Fritz!Box Blocklist
===================================
**English version below**

Werbeblocker für die AVM Fritz!Box und andere Router.
Funktioniert nur unter IPv4 zuverlässig - im Zweifel IPv6 abschalten wenn man die Werbung blocken möchte.
(Funktioniert leider auch mit FRITZ!OS 8.0 immer noch nur mit IPv4) 

Anleitung:
------------

https://avm.de/service/fritzbox/fritzbox-7590/wissensdatenbank/publication/show/3395_Filterlisten-fur-Internetseiten-erstellen/


1. Klicken Sie in der Benutzeroberfläche der FRITZ!Box auf "Internet".
2. Klicken Sie im Menü "Internet" auf "Filter".
3. Klicken Sie auf die Registerkarte "Listen".
4. Klicken Sie neben dem Eintrag "Gesperrte Internetseiten (Blacklist)" auf den Link "bearbeiten".
5. Den Inhalt der Liste [fritzbox-blocklist.txt](https://github.com/steigerbalett/fritzbox-blocklist/raw/master/fritzbox-blocklist.txt) kopieren und dort einfügen
6. Klicken Sie zum Speichern der Liste auf "Übernehmen".


Youtube blockieren:

https://avm.de/service/fritzbox/fritzbox-7590/wissensdatenbank/publication/show/3344_YouTube-in-der-Kindersicherung-sperren/

Den Inhalt der Liste [fritzbox-blocklist-video.txt](https://github.com/steigerbalett/fritzbox-blocklist/raw/master/fritzbox-blocklist-video.txt) kopieren und dort wie oben beschrieben einfügen.


# # #


:do_not_litter: Fritz!Box Blocklist
===================================
A list of domains to be blocked in my Fritz!Box.
For IPv4 only.

Instructions
------------

Short instructions:

1. See [AVM's instructions on how to setup a blocklist in your Fritz!Box](http://en.avm.de/service/fritzbox/fritzbox-7490/knowledge-base/publication/show/8_Restricting-Internet-access-using-parental-controls/)
2. Copy contents of [fritzbox-blocklist.txt](https://raw.githubusercontent.com/steigerbalett/fritzbox-blacklist/master/fritzbox-blocklist.txt) to your Fritz!Box' blocklist
3. Be sure to check if HTTPS traffic is still allowed

This will work with a standard firmware.

There is also an [extended instruction on how to set up your Fritz!Box as an AdBlocker](https://journal.3960.org/posts/2015-07-02-fritz-box-als-adblocker/) (German).

Know issues
-----------

| Domain               | Issue |
|----------------------|-------|
| conduit.com          | This entry may prevent some Netflix clients like Wii U from using Netflix (see [issue #6](https://github.com/fboes/fritzbox-blacklist/issues/6) for details) |
| googleadservices.com | This entry makes the paid links in Google search results unclickable |

Development
-----------

There is a maximum of 500 entries for the Fritz Box' blocklist. Choose each entry wisely.

Put each domain in a single line. Do not enter comments or anything else.

E.g.: To block `http://ads.example.com/some_script.js` enter `ads.example.com` or just `example.com`. `example.com` will also block all files from `www.example.com` and any other subdomain.

On the structure of URLs for this blocklist consult [AVM's documentation for blocklists](http://service.avm.de/help/de/FRITZ-Box-Fon-WLAN-7490/014/hilfe_internet_filter_blacklist). Keep in mind to keep this list as simple as possible, to keep it useful for other routers as well.

Contributing
------------

I am happy to merge your contributions to this file. Please make sure that the blocklist is ordered alphabetically, and you have removed any unneccessary whitespaces.

Legal stuff
-----------

Author: [Frank Boës](http://3960.org) and others

Copyright & license: See LICENSE.txt

These instructions are NOT affiliated with, endorsed, or sponsored by AVM.
