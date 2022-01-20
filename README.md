ABC80-MOB
=========

Programs for ABC80. Mostly in BASIC. [ABC 80](https://en.wikipedia.org/wiki/ABC_80) is a Swedish computer from 1978 
that was much used in schools but also in the industry.


There is an ABC80 App-Store at that also contains programs by others:
http://www.df.lth.se.orbin.se/~mikaelb/abc/80/

About this App-Store:

## An ABC80 App-Store in Swedish

Här finns en diskettavbild muzak.dsk med det innehåll som gick att utvinna från
en kassett från 1982 för den svenska datorn ABC80. Filerna finns även som 
ABC BASIC-källkod (BAS-filer) som ursprungligen hade teckenkodningen ISO-646-SE-C (alternativt
kallad ISO-646-SE2) (men med ett undantag för tecknet DEL=\x7F ty det är en fylld kvadrat i ABC 80: ■).
På GitHub är BAS-filerna omvandlade till UTF-8, men ¤ är $, ty ger bättre syntaxfärgning, ty
är standard i BASIC. Jag bytte även ut enkelcitat ' mot dubbelcitat " i startrek.bas
för att få bättre syntaxfärgning, ty enkelcitat är kommentarstecken i modern BASIC.

En fördel med ABC 80 för svensktalande som vill lära sig om datorer är att det
finns många böcker om den på svenska, se
http://sv.wikipedia.org/wiki/ABC_80 . En annan fördel med ABC80 var att man 
kunde skriva snabba arkadspel i ett skriptspråk ty ABC BASIC var 
semikompilerande och hade även heltalsaritmetik.

Diskettavbilden fungerar i emulatorn ABCWin2, se http://www.abc80.org/pub/abcwin/ eller ftp://ftp.abc.se/pub/abcwin/.
ABCWin2 fungerar i Windows och Linux med Wine och troligen i Mac OS X med Wine.
Det finns även en ABC80-emulator för MS-DOS men den fungerade ej i Linux med
DOSBox. Det finns även en ABC80-emulator, abc80sim, för Windows och Linux och i synnerhet Raspberry Pi OS 
för Raspberry Pi, se http://www.raspberrypi.org/forums/viewtopic.php?p=534518#p534518. 
Det finns nyare versioner av emulatorn abc80sim, men de får man kompilera själv.

I ABCWin2 väljer man diskettavbild till Drive 1 med menyn Setup. 
Därefter måste man starta om programmet. Man kan lista filer på disketten med 
kommandot  
RUN LIB  
Välj D (Viss drive) och 1 för Drive 1. Man kör ett program på Drive 1 genom
att skriva  
RUN MALARE  
Tydligen letar diskoperativsystemet på alla disketter. Skriv alternativt t.ex.  
RUN DR1:MALARE.BAS  
Det finns även Drive 0, DR0:. Tyvärr fungerar ej kassett (CAS:) i ABCWin2.
För att avbryta ett program trycker man Ctrl+C och visar källkoden med  
LIST  
eller  
LIST -100  
eller  
LIST 100-170  
eller  
LIST 170-  
beroende på vilken del av programmet man vill se.

Diskettavbilden muzak.dsk innehåller bl.a. programmet MALARE.BAS som 
ursprungligen heter MÅLARE.BAC på kassetten (BAC är den semikompilerade filen).
Det är ett ritprogram liknande Paint i Windows jag utvecklade 1982 när jag var
15 år. Man styr markören i åtta riktningar genom att trycka på knapparna runt F.
Huruvida man ritar eller suddar styrs av CapsLock. Man suddar hela skärmen 
med S. En finess med programmet är att det gör olika ljudeffekter beroende på 
vilket kommando man ger.

Disketten muzak.dsk innehåller:  
EDIT.BAS     (verkar inte fungera.)  
MALARE.BAS   (ursprungligen MÅLARE.BAC.)  
MASKEN.BAS   (Denna version av klassiska Masken/Snake verkar vara förbättrad.)  
MUZAK.BAS    (Fungerar dåligt -- troligen p.g.a. dålig ljudemulering.)  
ROBOT.BAS  
SCHACK.BAS  
SERIE.BAS  
STARTREK.BAS (Man bör nog ha manualen till Startrek fr. boken Dataspel i Basic.)  
TENNIS.BAS  

FORTH.LDA    (Finns på kassetten men togs bort på diskettavbilden ty ofullst.)  

Jag hade aldrig en egen ABC80 utan använde grundskolans några få timmar per
vecka som jag fick tillgång till från hösten 1981 (i 9:an) då jag gick en kurs
i BASIC-programmering som Fritt valt arbete/Elevens val. Även på gymnasiet
1982-85 hade vi ABC80 men då använde jag mest Forth på en SAAB-dator. Jag gjorde
värnplikten 1985-86 och då hade vi tillgång till Vic 64/Commodore 64 och 
Commodore 128 på fritiden, men spelade bara spel där. Fr.o.m. våren 1987 körde jag
IBM PC med MS-DOS och stordatorer med VMS på universitetet och fr.o.m. sommaren
1990 stordatorer med Unix (HP-UX).

Jag köpte en egen dator: Sinclair ZX81, i december 1981, och lödade ihop den
själv under jullovet. Det finns även en ZX81 App-Store här:  
http://www.df.lth.se.orbin.se/~mikaelb/sinclair/zx81/.

I januari 1988 köpte jag en PC: Amstrad PC1512, och samma år 1200 bps modem och
30 MB hårddisk. På PC:n programmerade jag mest i Pascal, C och C++ men även
lite i BASIC.


Mvh,  
// Mikael O. Bonnier (Lund 2012-07-22)  
P.S. Själva ljudet från kassetten finns i muzak96k.wav och är samplat med 
96 kHz samplingsfrekvens och kan därför kanske ej spelas i webbläsaren utan 
måste hämtas ner och kan spelas upp med t.ex. [VLC](http://www.videolan.org/vlc/).
Där finns även en 44,1 kHz ljudfil. Jag använde programmet mfmdecode.c v. 4 av 
H. Peter Anvin <http://git.zytor.com/abc80/mfmdecode.git/plain/mfmdecode.c> för att extrahera
filerna från kassettbandet. Jag använde programmet AbcExplorer av Erik Isaksson
för att utvinna BAS-filer ur diskettavbilden. Jag hade urprungligen BAC-filer
men gjorde om dem till mer lättlästa BAS-filer genom att använda LOAD och LIST
på diskettavbilden.  
D.S.
