### STBAK - digitally label a tape backup and segment into "files"
turned out to be more complicated than using tar alone, with automatic breakes for files.
but anyways here it is...
![](https://github.com/moddie666/stabk/blob/main/stbak_r.gif?raw=true)![](https://github.com/moddie666/stabk/blob/main/stbak_f.gif?raw=true)
´´´
:~/stbak$ stbak 
STBAK - The Simple Tape Backup
Usage Information:
stbak "<path(s)>" <command>[=<filenumber(s)>][=<label>]

<path(s)>
        ... one or multiple paths. To ensure correct handling, paths should be enclosed in quotes especially if they contain special characters or wildcards.
<command>
        ... status)  print Tape drive Status Information
        ... rewind)  rewind to the start of the tape
        ... move)    move to beginning of file number <filenumber> (e.g. stbak move=3)
        ... tarfile) write <path> to <filenumber> on <label> (e.g. stbak /home/user wrfile[=3][=some-tape])
        ... bz2file) same as above but with bzip2 compression
        ... tgzfile) same as above but with gz compression
        ... rdfile)  output contents of <filenumber> to stdout (e.g. stbak rdfile=3)
        ... scan)    read parts of or the whole tape into database, this requires a valid label definition either on tape or the command line. (e.g. stbak scan[=a[-b]][=some-tape])
<filenumber>
        ... [move|wrfile|rdfile] to/from specified filenumber
<label>
        ... name of the tape, can contain the following caracters A-z,0-9,-,_,. [scan|index|wrfile]
´´´
