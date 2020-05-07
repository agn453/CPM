# CPM
CP/M Emulator for RSX280
========================

This repository contains a CP/M emulator for the RSX280 operating system.

It is written in Zilog Z280 assembly language and is based on an earlier
version for UZI280 (a unix edition 7 operating system for the Z280)
by Stefan Nitschke and released into the Public Domain in 1996.

RSX280 is being developed by Hector Peraza and is available from
https://github.com/hperaza/RSX280

****  NOTE: THIS IS NOT YET A WORKING VERSION  ****

CPM is a program to allow "well-behaved" Z80 CP/M programs to run
under RSX280.  The implementation only supports basic CP/M 2.2
BDOS functionality and console-only BIOS routines.  None of the
usual CP/M 2.2 BIOS routines for disk, printer, punch and reader are
available.

Further documentation will be added at a later time.

Update: 01-May-2020
-------------------

The original UZI280 version was missing some CP/M BDOS functions.
These have been added.  Console I/O and Disk file Open/Create/Read/Write
appear to be working.   Still to-do file Remove, Random access Read/Write,
Directory Search and some other BDOS functions.

Update: 07-May-2020
-------------------

BDOS Console I/O and sequential File functions are working.

Still to-do Search First/Next functions and verify Random File
functions.

A log file follows -

```
>run cpm
CP/M 2.2 emulator 59K V0.99 [DEBUG]
Use ^Z followed by Return/Enter to exit.

X>[CPM]CAL 2020 /D
Calendar,  Version 1.3
Name of Disk Output File? cal.tmp
Calendar Output File/Device is cal.tmp

X>[CPM]PIP CON:=CAL.TMP
                       Calendar of Year 2020


Calendar for JANUARY   Calendar for FEBRUARY  Calendar for MARCH
Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa
          1  2  3  4                      1    1  2  3  4  5  6  7
 5  6  7  8  9 10 11    2  3  4  5  6  7  8    8  9 10 11 12 13 14
12 13 14 15 16 17 18    9 10 11 12 13 14 15   15 16 17 18 19 20 21
19 20 21 22 23 24 25   16 17 18 19 20 21 22   22 23 24 25 26 27 28
26 27 28 29 30 31      23 24 25 26 27 28 29   29 30 31



Calendar for APRIL     Calendar for MAY       Calendar for JUNE
Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa
          1  2  3  4                   1  2       1  2  3  4  5  6
 5  6  7  8  9 10 11    3  4  5  6  7  8  9    7  8  9 10 11 12 13
12 13 14 15 16 17 18   10 11 12 13 14 15 16   14 15 16 17 18 19 20
19 20 21 22 23 24 25   17 18 19 20 21 22 23   21 22 23 24 25 26 27
26 27 28 29 30         24 25 26 27 28 29 30   28 29 30
                       31


Calendar for JULY      Calendar for AUGUST    Calendar for SEPTEMBER
Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa
          1  2  3  4                      1          1  2  3  4  5
 5  6  7  8  9 10 11    2  3  4  5  6  7  8    6  7  8  9 10 11 12
12 13 14 15 16 17 18    9 10 11 12 13 14 15   13 14 15 16 17 18 19
19 20 21 22 23 24 25   16 17 18 19 20 21 22   20 21 22 23 24 25 26
26 27 28 29 30 31      23 24 25 26 27 28 29   27 28 29 30
                       30 31

Calendar for OCTOBER   Calendar for NOVEMBER  Calendar for DECEMBER
Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa
             1  2  3    1  2  3  4  5  6  7          1  2  3  4  5
 4  5  6  7  8  9 10    8  9 10 11 12 13 14    6  7  8  9 10 11 12
11 12 13 14 15 16 17   15 16 17 18 19 20 21   13 14 15 16 17 18 19
18 19 20 21 22 23 24   22 23 24 25 26 27 28   20 21 22 23 24 25 26
25 26 27 28 29 30 31   29 30                  27 28 29 30 31


X>^Z
>
```
