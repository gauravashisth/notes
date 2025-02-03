zsh:1: command not found: s
  keymap: ":"
    • normal mode
    • navigate using hjkl
    • double clicking "'", will take u to previous location of cursor.

  keymap: "f" + any alphabet character
    • normal mode
    • this will find occurence of that character in the that specific line.
    • can use ";" and "," to jump to next and previous occurences of that character. 

  general keymap: 
    • yap: yank around paragraph
    • dap: delete around paragraph
    • %: cursor on opening brakcet, and % will jump to closing bracket. vice-a-verse
  
  use of g key:
    • gH: start select line mode
    • ga: show encoding
    • gr{char}: replace a character, normal mode
    • {x}gg: go to line {x}

  use of ctrl key:
    • ctrl+f : 
    • ctrl+b : 
    • ctrl+w : 
    • ctrl+u : 
    • ctrl+h : 
    • ctrl+p : 
    • ctrl+n : 
  use of shift key:
    • shift + a: move sursor at last of line, and entera in insert mode
    • shift + s: deletes the complete line, and enters in insert mode
    • 

  multi-cursors:
    • have n line and want to put those lines into an array. (many usecases are found)
 	    - ctrl+ v, vertical edit. and select line further below/above.
   	  - I, capital i, to go into insert mode.
   	  - add "data[0] = ". enter normal mode.
 	    - hence, changes will be applied to all the selected lines. 
 	    ° or a more optimized meathod.
 	      - vip, highlight a para.
 	      - ":'<,'>s/\(.*\)"    (this includes space before first character)
 	      - ":'<,'>s/\(\w.*\)/data[0] = \1"    (this ignores the white space before the first character)
 	      - enter normla mode, and the changes are made. but still all index no. are still 0.
 	      - to change that, put cursor at 0 and ctrl+v and move upward or below. and command "g + ctrl+a"
 	  • this need characters to be same, to use multi-cursor
      - select in what portion, u wanna make change.
 	    - type ":", in command section, this will show up: ":'<,'>"
 	    - ":'<,'>s/{abc}": this will search all the occurence of those characters,
 	      and can change all those simultaneously by ":'<,'>s/{abc}/{xyz}"
 	    - ":'<,'>s/$/{asdf}": this will add the asdf characters at the end of all lines selected.

		data[1] = faa
		data[2] = afga
		data[3] = szs
		data[4] = hgwxeh
		data[5] = sxeg

		0
		0
		0
		0
