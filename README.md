# duu
Directory Usage Utility

Recursively display disk usage in kilobytes of the given directory. 

With Python 3, this will run under Windows, Linux and MacOS. 

A stand-alone windows executable is provided on the [release page](https://github.com/jftuga/duu/releases)

```
usage: duu.py [-h] [-b] [-e] [-q] [-s STATUS] [-n] [-N] [-f] [-S] [-H]
              [-T THREADS] [-x EXCLUDE] [-X REGEXPR] [-o OUTPUT]
              [dname]

Display directory disk usage in kilobytes, plus totals

positional arguments:
  dname                 directory name

optional arguments:
  -h, --help            show this help message and exit
  -b, --bare            do not print summary or stats; useful for sorting when
                        used exclusively
  -e, --ext             summarize file extensions
  -q, --quiet           don't display individual directories
  -s STATUS, --status STATUS
                        send processing status to STDERR, every STATUS number
                        of directories
  -n, --nodot           skip directories starting with '.'
  -N, --norecurse       do not recurse
  -f, --files           also display number of files in each directory
  -S, --stats           display mean, median, mode and stdev file statistics
  -H, --human           display numbers in a more human readable format
  -T THREADS, --threads THREADS
                        number of concurrent threads, consider for SANs
  -x EXCLUDE, --exclude EXCLUDE
                        colon-separated list of case-insensitive strings to
                        exclude
  -X REGEXPR, --regexpr REGEXPR
                        colon-separated list of case-insensitive regular
                        expressions to exclude
  -o OUTPUT, --output OUTPUT
                        output to CSV file

Directory Usage Utility (duu), version: 2.20

```

Example output:

```

c:\>duu compinfo

242 compinfo
0   compinfo\bin
0   compinfo\bin\Debug
485 compinfo\bin\Release
0   compinfo\obj
46  compinfo\obj\Debug
0   compinfo\obj\Debug\TempPE
735 compinfo\obj\Release
4   compinfo\obj\Release\TempPE
17  compinfo\Properties

summary
=======
files         : 59
directories   : 10
bytes         : 1,566,218
kilobytes     : 1,529.51
megabytes     : 1.49

```