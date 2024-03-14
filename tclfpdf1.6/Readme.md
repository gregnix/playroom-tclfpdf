## bug in code
### ttf_font.tcl
+ proc ::tclfpdf::ttf_getCMAP4
```
set $offset [expr ($unichar - $startCount($n)) * 2 + $idRangeOffset($n)];
set $offset [ expr $idRangeOffset_start + 2 * $n + $offset]; 
```
```
set offset [expr ($unichar - $startCount($n)) * 2 + $idRangeOffset($n)];
set offset [ expr $idRangeOffset_start + 2 * $n + $offset]; 
```


## Problems with example
+ ./example/dash.tcl

```
#false
Output "dash.tcl";
#rather
Output "dash.pdf";
```

## Problems under Linux

+ Directory for fonts is not one, but can be several. And then again divided into subdirectories.
+ Library directories are read-only. Font descriptions are generated dynamically and stored in ../font
