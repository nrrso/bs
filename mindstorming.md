#<center>_Executable and Link Format_</center>
***
## _Aufgabenstellung_
1. Wie findet man (bzw. das Betriebssystem) die erste auszuführende Instruktion innerhalb des Text-Segments?2. Auf welche Weise bekommen bereits im Quellprogramm (z.B. C-Programm) initialisierte - d.h. mit einem Anfangswert versehene – Variable ihre Anfangswerte vor dem Start eines Programmes?3. Woran erkennt man, um welchen Typ einer in ELF dargestellten Datei es sich handelt? (Für welche Dateitypen ist ELF prinzipiell vorgesehen?)4. Unterscheiden sich ELF-Dateien für 32-Bit- und 64-Bit-Prozessorarchitekturen? (Woran ist das gegebenenfalls erkennbar?)5. Welchen Zweck haben die so genannten Sektionen (sections) bzw. die program headers?6. Welche Bedeutung hat eine Symboltabelle als Teil einer in ELF dargestellten Datei?

***

## <center>_Was ist ELF?_</center>
- Executable and Link Format
- Standardformat für Binärprogramme in UNIX Systemen

### _Besonderheiten_
- dynamisches Linken und Laden
- Kontrolle über bereits laufende Programme
- einfache Möglichkeit, dynamische Bibliotheken zu erzeugen

### _Aufbau_
**besteht aus 5 Teilen**:
- Kopfinformationen (==ELF Header==)
- Programmkopftabelle (==program header table==)
- Sektionskopftabelle (==section header table==)
- Sektionen (==ELF sections==)
- Segmente (==ELF segment==)

### _Dateitypen_
#### relocatable file
- beinhaltet Informationen, wie Objektdateien verlinkt werden sollen, um ein Programm oder eine dynamische Bibliothek zu erzeugen

#### executable file
- beinhaltet Informationen, wie das Programm ausgeführt werden soll

#### shared object file
- Informationen für das statische und dynamische Linken

![](res/linking_executable_view.jpg)

#### ELF Header
- beschreibt den Aufbau der Datei

#### Program Header Table
- Informationen zur Prozesserzeugung
- nicht benötigt bei relocatable files

#### Sections (Linking View)
- beinhalten die Object File Informationen
	- instructions
	- data
	- symbol table
	- relocation information

#### Segments (Execution View)

#### Section Header Table
- beschreibt die Sections der Datei
	- jede Section hat einen Eintrag:
		- section name
		- section size
		- etc.
- nicht benötigt bei executable files

## <center>_Lösungen der Aufgaben_</center>
###_1_
> offene Fragen:
> 
> habe ich das richtig verstanden? siehe Seite 1-4 / 1-5
> 
> was ist mit 'Text-Segments' gemeint? 

- liest im Header
- **e_entry** gibt die Adresse des entry points an, mit dem der Prozess gestartet werden soll
	- ist keiner angegeben, enthält es den Wert 0

###_2_


###_3_


###_4_
[Unterschiede zwischen 32 und 64 bit](https://www.tortall.net/projects/yasm/manual/html/objfmt-elf64.html)
- "elf64 also supports the exact same sections, section attributes, and directives as elf32"
- "The primary difference between elf32 and elf64 (other than 64-bit support in general) is the differences in shared library handling and position-independent code. As BITS 64 enables the use of RIP-relative addressing, most variable accesses can be relative to RIP, allowing easy relocation of the shared library to a different memory address."

###_5_


###_6_ 

