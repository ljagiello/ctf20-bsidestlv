# Forensics - Check yourself so you won't wreck yourself

## Challenge
Dumbster diving.

File Download Link

For any issue, please contact the CTF team on our slack channel #2020-ctf or
via our twitter at @BSidesTLV_CTF

## Solution
With `kpartx` mounted provided image and grep filesystem.

```
loop3p4/$Recycle.Bin/S-1-5-21-3498983559-1615527653-2205644034-1001# cat '$R0K6T9B.txt'
BSIDESTLV{ICanSeeYouUnlessYouCleanUpAfterYourself}
```

## Links
1. https://linux.die.net/man/8/kpartx

## Flag
```
BSIDESTLV{ICanSeeYouUnlessYouCleanUpAfterYourself}
```
