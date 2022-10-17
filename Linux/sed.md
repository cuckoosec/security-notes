#### Basic commands:
1.  `5d` - **delete** - Delete line 5.
2.  `5p` - **print.** - print line 5 (you should call sed with `-n` option when using print to only print the specified lines)
3.  `5q` - **quit** - after line 5 quit
4.  `5a\Appended` - **append** - after line 5. Note the backward slash in front of 'a'
5.  `5c\Changed` - **change** - change line 5 to 'Changed'
6.  `5i\Before` - **insert** - insert before line 5.
7.  `5r newfile.txt` - **read** - put the contents of file 'newfile.txt' after line 5
8.  `5w written.txt` - **write** - write line 5 to 'written.txt'
9.  `5s/foo/bar` - **substitute** - on line 5 search for foo and replace with bar

#### Regex tricks
1.  `&` is the matched regex. `sed -E '/foo/& & &/' file.txt` will triplicate the foo word
2.  `\1` to `\9` are the groups id's. You use a group like `sed -E 's/(foo) (bar)/\2 \1' file.txt '. In this very simple example we search for 'foo' followed by space followed by 'bar'. Then we switch these words (instead of 'foo bar' we have 'bar foo')
3.  Flags. `sed 's/foo/bar/gi' file.txt` . 'g' will replace all occurrences on the line (instead of just the first as it is by default). 'i' will make the substitute case insensitive.

#### Print one line
`sed -n '10p' myfile.txt`
#### Do replacement on all lines except line 5
`sed '5!/s/foo/bar/' file.txt`
#### Do replacement on lines matching regex (eg: lines starting with 'hello')
`sed '/^hello/ s/h/H/' file.txt`
#### Do replacement from line 5 to end of file
`sed '5,$ s/foo/bar/' file.txt`
#### Delete empty files
`sed '/^$/d' file`
#### Print lines between two regex matches
`sed -nE '/^foo/,/^bar/p' file.txt`
#### Use custom delimiters to make it easy for some strings that contain slashes
`sed 's_/bin/bash_/bin/sh_' file.txt`
#### Multiple replacements by using a sed script
```
#!/usr/bin/sed -f
s/a/A/
s/foo/BAR/
s/hello/HELLO/
```
-   Make executable with `chmod +x myscript.sed`, call with `./myscript.sed myfile.txt`
#### Delete comments starting with # (no empty lines left behind)
`sed -E '/^#/d' f1`
#### Print until you encounter pattern then quit
`sed '/start/q' file.txt`
#### Print every second line (substitute ~3 for third line, etc)
`sed -n '1~2p' file.txt`
