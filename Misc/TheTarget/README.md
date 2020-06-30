# Misc - TheTarget

## Challenge
EZ-PZ-LEMON-SQUIZZY

File Download Link

For any issue, please contact the CTF team on our slack channel #2020-ctf or
via our twitter at @BSidesTLV_CTF

## Solution
In this challenge we receive a file that is Extensible Storage Engine (ESE)
Database (EDB) file.

We can extract information from inside with a tool - `esedbexport` and simply
grep for a flag.
```
:~$ esedbexport TheTarget
esedbexport 20181229

Opening file.
Database type: Unknown.
Exporting table 1 (MSysObjects) out of 13.
Exporting table 2 (MSysObjectsShadow) out of 13.
Exporting table 3 (MSysObjids) out of 13.
Exporting table 4 (MSysLocales) out of 13.
Exporting table 5 (datatable) out of 13.
Exporting table 6 (hiddentable) out of 13.
Exporting table 7 (link_history_table) out of 13.
Exporting table 8 (link_table) out of 13.
Exporting table 9 (quota_rebuild_progress_table) out of 13.
Exporting table 10 (quota_table) out of 13.
Exporting table 11 (sdpropcounttable) out of 13.
Exporting table 12 (sdproptable) out of 13.
Exporting table 13 (sd_table) out of 13.
Export completed.
:~$ cd TheTarget.export/
:~/TheTarget.export$ grep -m1 -ir 'BSidesTLV2020{'
datatable.4:11073 4108  1 3 1 0 13236033124 2007  1 3038287259199220266
02000000d6070000d70700000c100000412b0000                          Advocatus
Diaboli       Advdiab@tazmania.local                                    0
512                       BSIDESTLV2020{ThisGoesDeeper}
[...]
```

## Links
1. https://en.wikipedia.org/wiki/Extensible_Storage_Engine
1. https://github.com/libyal/libesedb/tree/master/esedbtools

## Flag
```
BSIDESTLV2020{ThisGoesDeeper}
```
