# EFT-texture-esp
Escape From Tarkov ESP texture and Grass/Visor Remover

## Features:
- item esp(esp item only shows items over 150K)
- player esp(texture player, purple means he’s out of helmet/armor and green is boss)
- no visor or grass(only included in the [Releases](https://github.com/codsec/EFT-texture-esp/releases) as the file size is heavy)

## How to use?
First download the files in the [Releases](https://github.com/codsec/EFT-texture-esp/releases) and copy the **StreamingAssets** folder inside each separate folder and place it inside the game folder: **"EscapeFromTarkov_Data"**

## Bypass?
It does not need a bypass, it is not detected at the moment, but it must become detectable at some future time, be happy!

**IF YOU DO NOT TRUST DO NOT USE AND MAINLY DO NOT PAY FOR IT, IT IS TOTALLY FREE!**

![alt text](https://i.imgur.com/Lr48pQZ.png)

## How it works exacly?
when you start the launcher it performs a "fast" consistency check. seen here in the logs:
```06:00 [DEBUG] Checking consistency (fast)...
06:00 [DEBUG] Loaded ConsistencyInfo for version 0.12.9.10532. Contains 7304 entries
06:00 [DEBUG] Consistency checking result: SUCCESS
06:00 [DEBUG] Sending consistency checking report to analytics...
```
it does this by comparing the file size of the 7304 games files against a list that it gets from BSGs servers, also seen in the logs...
```
-06:00 [DEBUG] Start downloading file http://cdn-11.eft-store.com/client/live/distribs/0.12.9.10532_11836d91-b378-4ce6-ae20-f8e8bc4bbb2e/Unpacked/ConsistencyInfo
```
Of course this is really insecure... for instance, you can download the consistency check file yourself because this is done without authentication of any kind. Just paste it in your browser.
You could host your own consistencyinfo file, that you've edited, and serve it up with a local http server, then put
```
localhost            cdn-11.eft-store.com
```
in your system32/etc/hosts file and tada! now you can host your own consistency file. while you're at it, put...
```
0.0.0.0           clientlogs.eft-project.com
```
in there as well, and prevent the launcher from sending your log files back to BSG. they have enough info about you. most games use mechanisms within the executable (these are much harder to get to) but from what I can tell, it's bee 2 years or more since BSG used any sort of intnernal check.

• [unknowncheats topic](https://www.unknowncheats.me/forum/escape-from-tarkov/437605-eft-esp-item-esp.html)
