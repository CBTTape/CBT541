# CBT541
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 541 is from Greg Smith, via the Hercules-390 File List    *   FILE 541
//*           and contains an MVS version of the routines to        *   FILE 541
//*           create CCKD-compressed DASD, and uncompressed DASD.   *   FILE 541
//*                                                                 *   FILE 541
//*    Note:  This file was updated by Christophe Varlet,           *   FILE 541
//*    ----   March 2014, to accommodate larger volumes, with       *   FILE 541
//*           a larger blocksize for the dump files (16384          *   FILE 541
//*           instead of 4096).  I have preserved the original      *   FILE 541
//*           material as members X$CCKDA0, X$CCKDO0, and           *   FILE 541
//*           X$CCKDL0.  Please also see member $$NOTE01 for        *   FILE 541
//*           further details.                                      *   FILE 541
//*                                                                 *   FILE 541
//*    Note:  Christophe Varlet's updated sources can only be       *   FILE 541
//*    ----   ASSEMBLED on z/OS 1.7 and later, but the resulting    *   FILE 541
//*           load modules will RUN on earlier z/OS versions,       *   FILE 541
//*           at least back to 1.4.  The earlier versions of the    *   FILE 541
//*           sources are (of course) still included in this file.  *   FILE 541
//*                                                                 *   FILE 541
//*    Original doc from Greg Smith:                                *   FILE 541
//*                                                                 *   FILE 541
//*           A word about CCKD-compressed DASD:                    *   FILE 541
//*                                                                 *   FILE 541
//*           Under Hercules (the PC-based S/390 hardware           *   FILE 541
//*           emulator which runs under Linux or Windows, and       *   FILE 541
//*           which is FREE....                                     *   FILE 541
//*                                                                 *   FILE 541
//*           DASD is defined to be a PC file, similar to the       *   FILE 541
//*           DASD created for a P/390 to run under OS/2...         *   FILE 541
//*                                                                 *   FILE 541
//*           However, this DASD takes up a lot of disk space.      *   FILE 541
//*           For example, a 3390-3 will take up over 2 gigabytes.  *   FILE 541
//*                                                                 *   FILE 541
//*           But Hercules developers have developed a solution     *   FILE 541
//*           (as of now, this does not work for the P/390)...      *   FILE 541
//*           That is, compressed DASD.  A CCKD-compressed DASD     *   FILE 541
//*           device will run transparently under Hercules, as      *   FILE 541
//*           if it were the full volume, but it usually takes      *   FILE 541
//*           up around a fifth of the original space.  CCKD        *   FILE 541
//*           compression is just a tad less than ZIP, but the      *   FILE 541
//*           disk is still usable AS IS, under Hercules.           *   FILE 541
//*                                                                 *   FILE 541
//*           Here, we have the famous CCKD compression routines    *   FILE 541
//*           which work so well on the PC, and they can be run     *   FILE 541
//*           on a mainframe MVS system.  You can compress a disk   *   FILE 541
//*           pack, port the file to a PC, and run it under         *   FILE 541
//*           Hercules, AS IS, just as if it were on the mainframe. *   FILE 541
//*           This gets a big WOW.....                              *   FILE 541
//*                                                                 *   FILE 541
//*                Greg Smith                                       *   FILE 541
//*                gsmith@nc.rr.com                                 *   FILE 541
//*                                                                 *   FILE 541
//*           This file may be distributed free, but it contains    *   FILE 541
//*           some copyrighted routines, which are subject to       *   FILE 541
//*           whatever conditions are stated in that respective     *   FILE 541
//*           pds member.                                           *   FILE 541
//*                                                                 *   FILE 541
//*           A rexx exec called $$RECV has been submitted by       *   FILE 541
//*           Lionel Dyck, to aid in the TSO RECEIVE of the         *   FILE 541
//*           appropriate members of this pds.                      *   FILE 541
//*                                                                 *   FILE 541
//*                lionel.b.dyck@kp.org                             *   FILE 541
//*                                                                 *   FILE 541
//*                varlet.christophe@orange.fr                      *   FILE 541
//*                                                                 *   FILE 541
```
