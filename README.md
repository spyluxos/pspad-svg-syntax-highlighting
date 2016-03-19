# pspad-svg-syntax-highlighting
Syntax highlighting for SVG files in the PSPad editor (http://www.pspad.com/)

Copy the ```SVG.ini``` to ```Syntax\SVG.ini``` (the ```Syntax``` subdirectory where PSPad was installed,
which is by default ```C:\Program Files (x86)\PSPad editor\``` in Windows7.

Open PSPad
Choose ```Settings | Highlighters Settings...```
Select the uppermost instance of ```<not assigned>``` from the left menu
Select ```SVG``` from Specification>User Highlighters
Press OK

When you now quit PSPad and reopen it, the SVG content will be recognised with the default highlighting colours.

You can complete the operation by selecting ```Setting | Use Highlighter```
In the automatic FileChooser dialog window, select the ```SVG.INI``` file and Press ```OK```

In the ```Use Highlighter Definition``` you can now set the the comment style to HTML (```<!-- _ -->```)

### Files used for configuration settings
####PSPad.INI
There is also a new entry added to the ```c:\Users\LocalUser\AppData\Roaming\PSpad\PSPad.INI``` file

```
[SVG]
Filter=SVG (*.svg)|*.svg
HLTabWidth=2
HLRealTabs=0
RightEdge=0
IndentChar= 
UnIndentChar= 
DocComment=
CurrentLine=0
CurrentLineBack=65535
Comment=00FF00001FFFFFFF010
Identifier=1FFFFFFF1FFFFFFF000
Key=1FFFFFFF1FFFFFFF100
Key words 2=1FFFFFFF1FFFFFFF100
Key words 3=1FFFFFFF1FFFFFFF100
Label=000000FF1FFFFFFF000
Number=008000001FFFFFFF000
Preprocessor=008080001FFFFFFF010
Reserved Word=000000801FFFFFFF100
Space=008080001FFFFFFF000
String=000080001FFFFFFF000
Symbol=1FFFFFFF1FFFFFFF000
Compilator File=
Compilator Param=
Compilator LOG=
Compilator Run=
Compilator Help=
Compilator SaveAll=0
Compilator ParsLog=
Compilator Capture=0
Compilator HideOutput=0
Compilator ProgSaveAll=0
Compilator ProgRunSelection=0
Compilator DefaultDir=
Compilator LogType=0
```
In the default settings, keyword1, 2 and 3 are all shown as bold black characters
Key=1FFFFFFF1FFFFFFF100
Key words 2=1FFFFFFF1FFFFFFF100
Key words 3=1FFFFFFF1FFFFFFF100
 
If you modify some of the default colour settings (e.g. key words 2 and 3 in this case)
then the ```c:\Users\LocalUser\AppData\Roaming\PSpad\PSPad.INI``` file will be modified for the marked parts
```
[SVG]
Filter=SVG (*.svg)|*.svg
HLTabWidth=2
HLRealTabs=0
RightEdge=0
IndentChar= 
UnIndentChar= 
DocComment=
CurrentLine=0
CurrentLineBack=65535
// the following lines
Comment=00FF00001FFFFFFF010
Identifier=1FFFFFFF1FFFFFFF000
Key=1FFFFFFF1FFFFFFF100
Key words 2=1FFFFFFF1FFFFFFF100
Key words 3=1FFFFFFF1FFFFFFF100
Label=000000FF1FFFFFFF000
Number=008000001FFFFFFF000
Preprocessor=008080001FFFFFFF010
Reserved Word=000000801FFFFFFF100
Space=008080001FFFFFFF000
String=000080001FFFFFFF000
Symbol=1FFFFFFF1FFFFFFF000
// up until here will be modified
Compilator File=
Compilator Param=
Compilator LOG=
Compilator Run=
Compilator Help=
Compilator SaveAll=0
Compilator ParsLog=
Compilator Capture=0
Compilator HideOutput=0
Compilator ProgSaveAll=0
Compilator ProgRunSelection=0
Compilator DefaultDir=
Compilator LogType=0
```
into:
```
Comment=00FF000000FFFFFF010
Identifier=1FFFFFFF00FFFFFF000
Key=1FFFFFFF00FFFFFF100
Key words 2=008000FF00F0F0F0110
Key words 3=00A0000000FFFFFF100
Label=000000FF00FFFFFF000
Number=0080000000FFFFFF000
Preprocessor=0080800000FFFFFF010
Reserved Word=0000008000FFFFFF100
Space=0080800000FFFFFF000
String=0000800000FFFFFF000
Symbol=1FFFFFFF00FFFFFF000
```

### New file of the type *.svg
You can at this moment create a new file of the SVG type, but it will still be empty.

In order to create an already filled-in, or typical, version of an SVG file, you have to create the PSPad\Template\default.svg file.
A minimalistic and commented ```default.svg``` template could be as follows:

<svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 48 48">
```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<svg 
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   <!-- add xmlns:xlink if you want to use linking in your SVG -->
   xmlns:xlink="http://www.w3.org/1999/xlink"
   <!-- add size and viewbox settings if required in your SVG -->
   width="200" height="100" 
   viewBox="0 0 200 100"
   >
   
   <!-- followed with your content -->
   <g id="myid01">
   
   </g>   
</svg>

```

Create a new file of type "SVG" or open an existing "*.svg" file

 

