# Forensics - MoreWithLess

## Challenge
You need some EFF in your life.

File Download Link

For any issue, please contact the CTF team on our slack channel #2020-ctf or
via our twitter at @BSidesTLV_CTF

## Solution
With `ewfmount` mounted provided image and extract all strings.

```
:$ ewfmount MoreWithLess.E01 MoreWithLess/
:$ strings ewf1 | grep BSIDESTLV2020
https://www.google.com/search?q=BSIDESTLV2020%7BHideYourNeedleInTheHayStack%7D&rlz=1C1GCEA_enIL905IL905&oq=BSIDESTLV2020%7BHideYourNeedleInTheHayStack%7D&aqs=chrome..69i57.515j0j7&sourceid=chrome&ie=UTF-8(

  51286320-1a4f-42b7-b3ce-1e1e46d516c1BSIDESTLV2020{HideYourNeedleInTheHayStack}BSIDESTLV2020{HideYourNeedleInTheHayStack}https://www.google.com/search?q=BSIDESTLV2020%7BHideYourNeedleInTheHayStack%7D&rlz=1C1GCEA_enIL905IL905&oq=BSIDESTLV2020%7BHideYourNeedleInTheHayStack%7D&aqs=chrome..69i57.515j0j7&sourceid=chrome&ie=UTF-8BSIDESTLV2020{HideYourNeedleInTheHayStack}0,0Google
Search0,4
VBSIDESTLV2020{HideYourNeedleInTheHayStack}bsidestlv2020{hideyourneedleinthehaystack}
BSIDESTLV2020{HideYourNeedleInTheHayStack}
```

## Links
1. https://github.com/libyal/libewf

## Flag
```
BSIDESTLV2020{HideYourNeedleInTheHayStack}
```
