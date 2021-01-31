# Update 2021-01-31 from lockywolf

Okay, you now need `g++ -fpermissive`, and autotools is obviously broken.
But the code now supports localised strings. Kinda. At least for Яussian.


# Skypelog

A simple tool to read binary DBB databases and output its text equivalent.

This could be used to read the Skype chatlogs (stored unencrypted as `chatmsg256.dbb` under `~/.Skype/<username>/`) 
on some Skype versions. It may not work on the newest Windows-versions but on my Linux with Skype 2.2,
those DBB files show up.

Try this after building: 

```bash
$ ./skypelog chatmsg*.dbb | sort | less
```

and have fun!

I took the one skypelog.c from 
[here](http://www.hackerfactor.com/blog/index.php?/archives/231-Skype-Logs.html)
and made it into a 
[GBT](http://en.wikipedia.org/wiki/GNU_build_system)
project. If you're new to the GNU build tools like me, here's how you get this built:

```bash
$ aclocal
$ autoconf
$ automake -a
$ ./configure 
$ make
$ sudo make install
```

Best of luck!
