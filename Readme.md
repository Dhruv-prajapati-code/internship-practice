I/O Streams

stdin (0): Standard input (keyboard/file).
Example: cat < file.txt (reads from file as input).

stdout (1): Standard output (screen by default).
Example: echo "Hi" > out.txt (writes to file).

stderr (2): Standard error (error messages).
Example: ls nofile 2> err.txt (redirects error).

Text Processing & File Commands

cut – Extracts sections from each line.
Example: cut -d"," -f1 file.csv (prints first column).

paste – Merges files line by line.
Example: paste f1.txt f2.txt (combines columns).

sort – Sorts lines of text files.
Example: sort names.txt (sorts alphabetically).

tr – Translates or deletes characters.
Example: echo "linux" | tr a-z A-Z (LINUX).

join – Joins lines from two files on a common field.
Example: join f1.txt f2.txt (matches IDs).

split – Splits large file into smaller chunks.
Example: split -b 1M bigfile part_ (1MB chunks).

head – Displays first lines of a file.
Example: head -5 log.txt (first 5 lines).

tail – Displays last lines of a file.
Example: tail -f log.txt (live log view).

Redirection & Piping

pipe (|) – Sends output of one command as input to another.
Example: cat file | grep "error"

tee – Reads from stdin, writes to stdout and file.
Example: ls | tee list.txt

Counting & Conversion

nl – Adds line numbers to file content.
Example: nl notes.txt

wc – Counts lines, words, characters.
Example: wc -l file.txt (line count).

expand – Converts tabs to spaces.
Example: expand file.txt

unexpand – Converts spaces to tabs.
Example: unexpand file.txt

Filtering

uniq – Removes duplicate lines (adjacent only).
Example: uniq sorted.txt

grep – Searches for patterns.
Example: grep "error" log.txt

awk – Pattern scanning and processing.
Example: awk '{print $1}' file.txt (prints first column).
