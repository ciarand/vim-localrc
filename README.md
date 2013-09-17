vim-localrc
===========
Enable configuration file of each directory.

You can put a configuration file for the files below the certain directory.

The configuration file is a Vim script of a decided file name like .vimrc.
The file name is specified by `g:localrc_filename`.

Configuration file applied only to a specific filetype can be put.  The file
name is specified by `g:localrc_filetype`.

When two or more configuration files exist, it is sequentially loaded from a
shallow hierarchy.

For example:
```
~/ 
|- .local.vimrc	 (1)
`- project/
   |- .local.vimrc	(2)
   `- src/
      |- .local.vimrc	(3)
      `- main.c 
```
In this case, when `main.c` is loaded, the configuration files are loaded in order 
of the number.
