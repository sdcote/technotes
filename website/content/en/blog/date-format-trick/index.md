---
date: 2018-12-16
title: Old Date Format Trick
linkTitle: Old Date Format Trick
description: >
  This is a trick from the old days (the 1980s) of programming in COBOL and RPG. 
  In those days, we had to set up working storage and were basically limited to 
  fixed storage sizes in bytes. Overflow and truncation were always a concern but 
  sometimes it could be used to our advantage. This is a trick to convert MDY to 
  YMD and back again.
author: Steve Cote ([@sdcote.com](https://bsky.app/profile/sdcote.com))
resources:
  - src: "**.{png,jpg}"
    title: "Image #:counter"
    params:
      byline: "Steve Cote / CC-BY-CA"
---
It used to be a common practice to define dates in a `C6.0` field. That is a character field with six places and no decimal places. An integer in this field was either a YMD or a MDY value. This allowed us to represent dates with just 6 octets (bytes) of data in our records. If we stored them in binary it was only 3 bytes of data.

You have to remember that back then we had very little memory available for our programs. A 4-digit year was a luxury. This was a big reason for the [Y2K scare](https://en.wikipedia.org/wiki/Year_2000_problem). Every byte counted. In fact, we would measure things in nibbles (4-bit bytes). A single byte would hold 8 flags. Our tapes held about 45MB of data and represented an entire table of data. Some tape drives could hold 180MB of data and a whole table had to fit on it, but those drives and tapes were expensive and not widely available. We often could not load an entire table into primary storage, but I digress.

## Convert MMDDYY to YYMMDD
To convert an integer which represented Month Day Year into Year Month Day format all you had to do was a simple multiplication. Just multiply the integer by 10000.01 and take the last 6 digits and you have the same date but the year moved to the beginning.

MMDDYY * 10000.01 = YYMMDD

121618 * 10000.01 = 1216181216.18

## Convert YYMMDD to MMDDYY
To convert back from Year Month Day to Month Day Year just multiply your value by 100.0001 and take the last 6 digits

YYMMDD * 100.0001 = MMDDYY

181216 * 100.0001 = 18121618.1216

## Using Java
The following is the process in Java. It loses some of its elegance in a more modern language:

```java
public class example {
  public static final void main (String[] args){
    int value = 121618;
    System.out.println("Original value in MMDDYY: "+value);
    value = (int)(value * 10000.01);
    System.out.println("Converted Value: " +value);
    value = value % 1000000;
    System.out.println("Final value in YYMMDD: "+value);
  }
}
```

The first line assigns the date as an integer value. The third line performs the conversion and automatically drops the fractional part. The fifth line returns only the last six digits of the value. The output looks like this:

Original value in MMDDYY: 121618
Converted Value: 1216181216
Final value in YYMMDD: 181216

I'm not sure if I would ever find a need to use this with modern languages and libraries, not to mention the abundance of computing resources at our avail these days.

This just reminded me of a time when we had to be clever to do things efficiently.
