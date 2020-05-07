How made without ANISOU lines
=============================

Opened `3hyd.pdb` (created from content at [PDB entry for 3hyd](https://files.rcsb.org/view/3hyd.pdb)) in a text editor with suppore from regular expressions (often called REGEX). I used Sublime Text but you can also use Atom, VSCode, Notepad++ and others. You can also use online regular expression tools, example https://regex101.com/ .



BASED on: https://superuser.com/questions/1081156/how-to-remove-lines-starting-with-specific-character and https://stackoverflow.com/a/5185998/8508004 and the fact I don't want to deal with anisotropic temperature factors as they not typically in PDB files.


FIND:  
^ANISOU.*\n


REPLACE:  
<NOTHING>




The `\n` at the end of the find pattern insures it also removes the blank line that would otherwise be left behind. See https://stackoverflow.com/a/5185998/8508004 