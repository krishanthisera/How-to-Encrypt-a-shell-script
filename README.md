# How-to-Encrypt-a-shell-script

If you’re really concerning about the privacy of your shell scripts(Source),

I have use Ubuntu 14.04 server with the root Privilage.
The source of the program 'SCH' which I’m using here is from

        http://www.datsi.fi.upm.es/


At first lets download some packeges which required to run our shell encryption program


You will need to download gcc compilers 

        root@ubuntu:/usr/src# apt-get install gcc

You will need to install 'make' utility if it required (Depend on your system)

        root@ubuntu:/usr/src# apt-get install make

After that  lets download our encryption program/ source [from http://www.datsi.fi.upm.es/] 

Or you can download the 'SCH' source file which I've attached to this repository from from http://www.datsi.fi.upm.es/

        root@ubuntu:/usr/src# wget http://www.datsi.fi.upm.es/~frosal/sources/shc-3.8.7.tgz
  
Lets extract the '.tgz' file

        root@ubuntu:/usr/src# tar xvf shc-3.8.7.tgz
        shc-3.8.7/CHANGES
        shc-3.8.7/Copying
        shc-3.8.7/Makefile
        shc-3.8.7/match
        shc-3.8.7/pru.sh
        shc-3.8.7/shc-3.8.7.c
        shc-3.8.7/shc.1
        shc-3.8.7/shc.README
        shc-3.8.7/shc.c
        shc-3.8.7/shc.html
        shc-3.8.7/test.bash
        shc-3.8.7/test.csh
        shc-3.8.7/test.ksh

Let jump in to the 'shc' source folder

        root@ubuntu:/usr/src# cd shc-3.8.7

In  here I'm going to encrypt a shell script in the 

        /home/encrypt

Let's look inside the Shell script

        vim /home/encrypt/checksrv.sh

![alt tag](https://s32.postimg.org/t8v6s39r9/Screenshot_358.png)

Now lets Encrypt our Shell file
Note that you always welcome to change password file in the shc-3.8.7 as you desire.

        root@ubuntu:/usr/src/shc-3.8.7# ./shc -f /home/encrypt/checksrv.sh

There will be two additional files

        root@ubuntu:/usr/src/shc-3.8.7# ls  /home/encrypt/
        checksrv.sh  checksrv.sh.x  checksrv.sh.x.c

'checksrv.sh' is our original (Unencrypted) shell source
'checksrv.sh.x' is the Encrypted Shell source
'checksrv.sh.x.c' c files was created in order to perform encryption

Lets check on our encrypted source file

        root@ubuntu:/usr/src/shc-3.8.7# vim  /home/encrypt/checksrv.sh.x

![alt tag](https://s31.postimg.org/j2v9tgkwr/Screenshot_357.png)

Now you can see some binary stuffs instead of the plain shell text.

Now you can share the '.sh.x' so your source will be hidden



  
  

  
