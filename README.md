# `mkplot`

A [gnuplot](http://www.gnuplot.info) config file generator, writes to `stdout`, so can be piped straight into `gnuplot` (no need to save configuration to a file) or saved to a file as a starting point for more complex plots.

## Help page

```
mkplot writes a gnuplot config to stdout (can pipe straight into gnuplot)
filling a template with the provided parameters

USAGE: mkplot <data_file> <OPTIONS>
   or: mkplot help

OPTIONS:
  list     print column headers and exit
  type     sets the type of plot to generate (default or date)
  x        set column (by name) to use as x axis
  y        set column (by name) to use as y axis
  y2       set column (by name) to use as secondary y axis
  xlabel   set x axis label
  ylabel   set y axis label
  y2label  set secondary y axis label
  save     set file to save to
  title    set title
  smooth   set smoothing mode
  lw       set line width
  sep      set separator
```

## Example

```sh
mkplot example.csv title "The title" x col1 y col2 xlabel "this is x" ylabel "this is y" | gnuplot
```
