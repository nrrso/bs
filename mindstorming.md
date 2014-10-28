#_Executable and Link Format_
***
### _Aufgabenstellung_
- Wie findet man (bzw. das Betriebssystem) die erste auszuführende Instruktion innerhalb des Text-Segments?- Auf welche Weise bekommen bereits im Quellprogramm (z.B. C-Programm) initialisierte - d.h. mit einem Anfangswert versehene – Variable ihre Anfangswerte vor dem Start eines Programmes?- Woran erkennt man, um welchen Typ einer in ELF dargestellten Datei es sich handelt? (Für welche Dateitypen ist ELF prinzipiell vorgesehen?)- Unterscheiden sich ELF-Dateien für 32-Bit- und 64-Bit-Prozessorarchitekturen? (Woran ist das gegebenenfalls erkennbar?)- Welchen Zweck haben die so genannten Sektionen (sections) bzw. die program headers?- Welche Bedeutung hat eine Symboltabelle als Teil einer in ELF dargestellten Datei?

***

### _Was ist ELF eigentlich?_
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
#### executable

#### relocatable

#### shared object
