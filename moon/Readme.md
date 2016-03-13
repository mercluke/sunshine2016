Now things get a bit more fun.

Depending on your familiarity with the PNG format you may know that it is possible to concatenate extra data on the end of an image without confusing libpng and similar libraries.

1. In a hex editor look for the "IEND" chunk near the end of the file to notice an extra file tacked on the end seemingly containing a "flag.txt" - copy this data over into a new file.
![Moon in a hex editor](https://github.com/mercluke/sunshine2016/blob/master/moon/moon_p1.png)
2. we don't neccesarily recognise this file format, let's make use of the `file` command to discover what type of file it is.  

![file is a great way to discover file formats](https://github.com/mercluke/sunshine2016/blob/master/moon/moon_p2.png)
In this case, we have ourselves a zip archive.
3. On attempting to extract this zip we notice it is protected by a password.  Luckilly, archives created with earlier versions of zip are trivial to bruteforce, there are many tools available for this (including john the ripper)
![crack dat zip](https://github.com/mercluke/sunshine2016/blob/master/moon/moon_p3.png)
I just happened to have a shell script lying around on my droplet so i used that.
4. ???
5. Profit