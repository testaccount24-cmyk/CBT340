# CBT340
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE 340 IS FROM ALFRED NYKOLYN AND ROLAND SCHIRADIN AND       *   FILE 340
//*           CONTAINS A NEW PROGRAM CALLED DCM (DIRT CHEAP         *   FILE 340
//*           MONITOR - UNRELATED TO THE DIRT CHEAP MONITOR         *   FILE 340
//*           SYSTEM (DCMS) FROM THE OLD CBT TAPES).                *   FILE 340
//*                                                                 *   FILE 340
//*           THE PURPOSE OF DCM IS TO REPORT ON STATISTICS         *   FILE 340
//*           COLLECTED BY THE 7980-3 AND COMPATIBLE CONTROLLERS.   *   FILE 340
//*                                                                 *   FILE 340
//*        EMAIL:   ALFRED NYKOLYN     -  APN@ISTAR.CA              *   FILE 340
//*                 ROLAND SCHIRADIN   -  Roland@schiradin.de       *   FILE 340
//*                                                                 *   FILE 340
//*               DCM - DIRT CHEAP MONITOR  V0.8                    *   FILE 340
//*                                                                 *   FILE 340
//*     7980-3 AND COMPATIBLE CONTROLLERS KEEP A GREAT DEAL OF      *   FILE 340
//*     STATISTICS.  GETTING THEM OUT IS ANOTHER STORY.  IF YOU     *   FILE 340
//*     HAVE EXTRA $$$, YOU CAN USE AZTEC; IF YOU ARE A             *   FILE 340
//*     MASOCHIST, YOU USE IDCAMS.  IN ORDER TO LEARN HOW THE       *   FILE 340
//*     7980-3 WORKS, I WROTE DCM.  HERE IS A SAMPLE SCREEN         *   FILE 340
//*     (SQUEEZED DOWN AND ABBREVIATED).                            *   FILE 340
//*                                                                 *   FILE 340
//*                    DIRT CHEAP MONITOR V0.8                      *   FILE 340
//*                                                                 *   FILE 340
//*   DEVICES 0E00-0E3F   SSID 0010  I/O RATES MEASURED FROM        *   FILE 340
//*    VOLUME SYSLBB   DEVADDR 0E08  SSCH RATE   30.5/S             *   FILE 340
//*     PATHS 08 13 48 53            DUPLEXED: SECONDARY DEV E17    *   FILE 340
//*   CACHE: ACTIVE           DFW: ACTIVE                           *   FILE 340
//*                                                                 *   FILE 340
//*      I/O TIME(MS)  4.6   PEND  0.5   DISC  1.2   CONN  2.9      *   FILE 340
//*        I/O  30.4/S     READS  29.2/S  WRITES    1.2/S           *   FILE 340
//*     NORMAL  30.4/S     READS  29.2/S  WRITES    1.2/S           *   FILE 340
//*       SEQL   0.0/S     READS   0.0/S  WRITES    0.0/S -SWITCHES-*   FILE 340
//*        CFW   0.0/S     READS   0.0/S  WRITES    0.0/S SD0: AB   *   FILE 340
//*        DFW   1.2/S    NORMAL   1.2/S    SEQL    0.0/S SD1: AB   *   FILE 340
//*     BYPASS   0.0/S   INHIBIT   0.0/S                  SD2: AB   *   FILE 340
//*     STAGES   2.1/S    NORMAL   2.1/S  SEQL     0.0/S  SD3: AB   *   FILE 340
//*   DESTAGES   0.0/S  PREREADS   0.0/S          CU SERIAL# 011717 *   FILE 340
//*   READ HIT%  94.9     NORMAL%  92.6    SEQL%   99.9             *   FILE 340
//*   CFW HIT%   0.0       READ%   0.0  WRITES%    0.0              *   FILE 340
//*   DFW HIT%  99.0     NORMAL%  99.0    SEQL%   78.3              *   FILE 340
//*   R/W RATIO  33.5  HITS/STAGE  14.2   RETRY%    0.0             *   FILE 340
//*                                                                 *   FILE 340
//*   CACHE INSTALLED 65536K                                        *   FILE 340
//*   CACHE AVAILABLE 65136K                                        *   FILE 340
//*   NVS INSTALLED  4096K                                          *   FILE 340
//*   PINNED DATA     0K                                            *   FILE 340
//*                                                                 *   FILE 340
//*   ENTER:   SR, LR, SH, LH, ALL, ONL, AUTO,                      *   FILE 340
//*            <DEV-ADDR>, <VOLUME> OR END                          *   FILE 340
//*                                                                 *   FILE 340
//*                                                                 *   FILE 340
//*   THIS SCREEN SNAPSHOT IS FROM A RUNNING SYSTEM.  THE           *   FILE 340
//*   STATISTICS ARE FOR ONE DEVICE ALTHOUGH DCM CAN PROVIDE        *   FILE 340
//*   STATISTICS FOR A STRING OF DEVICES OR FOR ALL DEVICES         *   FILE 340
//*   ATTACHED TO A CONTROLLER.                                     *   FILE 340
//*                                                                 *   FILE 340
//*   THERE ARE TWO SOURCES OF STATISTICS FOR DCM: THE              *   FILE 340
//*   CONTROL UNIT AND THE CHANNEL SUBSYSTEM.  THE PENDING,         *   FILE 340
//*   DISCONNECT AND CONNECT TIMES ARE PROVIDED BY THE              *   FILE 340
//*   CHANNEL SUBSYSTEM AND ARE THE SAME AS REPORTED BY RMF.        *   FILE 340
//*   THESE TIMES ARE IN MILLISECONDS.  THE OTHER TIMES ARE         *   FILE 340
//*   CALCULATED USING THE COUNTS MAINTAINED BY THE 7980-3.         *   FILE 340
//*   THE INTERVAL IS BETWEEN THE TWO TIMES IN THE UPPER            *   FILE 340
//*   RIGHT HAND CORNER.  IN GENERAL, THE VERY FIRST RATE ON        *   FILE 340
//*   EACH LINE IS THE SUM OF THE REMAINING RATES ON THE            *   FILE 340
//*   LINE.  THE I/O RATE IS THE SUM OF THE NORMAL RATE, THE        *   FILE 340
//*   SEQUENTIAL RATE, THE BYPASS RATE AND THE INHIBIT RATE.        *   FILE 340
//*                                                                 *   FILE 340
//*   THE HIT% ARE CALCULATED FROM THE COUNTERS MAINTAINED IN       *   FILE 340
//*   THE 7980-3.  THE PERCENTAGES ON THE VERY LEFT OF EACH         *   FILE 340
//*   LINE ARE THE WEIGHTED AVERAGES OF THE REMAINING               *   FILE 340
//*   PERCENTAGES ON THAT LINE.  IT IS POSSIBLE TO SEE THE LONG     *   FILE 340
//*   TERM VIEW OF THE HITS SINCE THE CONTROLLER WAS IML'D OR       *   FILE 340
//*   A SHORT TERM VIEW SINCE THE LAST TIME THAT THE ENTER KEY      *   FILE 340
//*   WAS PRESSED.                                                  *   FILE 340
//*                                                                 *   FILE 340
//*   THE STAGES, DESTAGES AND PREREADS FIELDS ARE THE NUMBER       *   FILE 340
//*   OF THESE OPERATIONS PER SECOND.  THE ONLY STATISTICS NOT      *   FILE 340
//*   MAINTAINED IN THE 7980-3 ARE THE R/W RATIO AND THE            *   FILE 340
//*   HITS/STAGES.  R/W IS CALCULATED IN A STRAIGHT FORWARD         *   FILE 340
//*   FASHION AND THE HITS/STAGES GIVES SOME MEASURE OF THE         *   FILE 340
//*   CACHING EFFICIENCY.                                           *   FILE 340
//*                                                                 *   FILE 340
//*   HERE IS A LIST OF DCM COMMANDS:                               *   FILE 340
//*                                                                 *   FILE 340
//*   AUTO     REPEAT DISPLAY 20 TIMES WITH A 4 SECOND INTERVAL     *   FILE 340
//*   ALL      SUMMARIZE ALL DEVICES ON THE CONTROL UNIT            *   FILE 340
//*   <ENTER>  REFRESH THE SCREEN WITH A NEW SET OF STATISTICS      *   FILE 340
//*   ONL      RUN THROUGH ALL ONLINE DEVICES ON THIS CONTROL UNIT  *   FILE 340
//*   RNN      REPEAT THE DISPLAY NN TIMES WITH A 4 SECOND INTERVAL *   FILE 340
//*   WNN      SET WAIT VALUE TO NN SECONDS                         *   FILE 340
//*   N        GO TO NEXT DEVICE                                    *   FILE 340
//*   P        GO TO PREVIOUS DEVICE                                *   FILE 340
//*   LR       LONG TERM I/O RATES                                  *   FILE 340
//*   SR       SHORT TERM I/O RATES                                 *   FILE 340
//*   LH       PROVIDE LONG TERM HIT% (FROM THE TIME THAT ADVANCED  *   FILE 340
//*            FUNCTIONS WERE ENABLED)                              *   FILE 340
//*   SH       PROVIDE SHORT TERM DELTA HIT%                        *   FILE 340
//*   NOUP     DO NOT RE-WRITE HISTORY FILE                         *   FILE 340
//*   END      ENDS DCM SESSION. Q IS AN ABBREVIATION.              *   FILE 340
//*   QN       END DCM WITHOUT UPDATING THE HISTORY FILE.           *   FILE 340
//*                                                                 *   FILE 340
```
