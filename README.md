

# Skypelog

A simple tool to read binary DBB databases and output its text equivalent.

This could be used to read the Skype chatlogs (stored unencrypted as chatmsg256.dbb in ~/.Skype/<username>/) 
on some Skype versions. It may not work on the newest Windows-versions, but on my linux, Skype (2.2)
stores these dbb files as DBB databases.


Try this: 

```bash
$ ./skypelog chatmsg*.dbb | sort | less
```

and have fun!

I took the one skypelog.c from 
[here](http://www.hackerfactor.com/blog/index.php?/archives/231-Skype-Logs.html)
and made it into a 
[GBT](http://en.wikipedia.org/wiki/GNU_build_system)
project.

If you're new to the GNU build tools like me, here's how you get this built:

```bash
klm@lato:/tmp/skypelog (master)$ aclocal
klm@lato:/tmp/skypelog (master)$ autoconf
klm@lato:/tmp/skypelog (master)$ automake -a
klm@lato:/tmp/skypelog (master)$ ./configure 
klm@lato:/tmp/skypelog (master)$ make
klm@lato:/tmp/skypelog (master)$ sudo make install
```

Best of luck!
