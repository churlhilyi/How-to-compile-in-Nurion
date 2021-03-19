## yumdownloader




1. Use __yum search__ command :

           $ yum search package1

2. Use __yumdownloader__ command :

           $ mkdir ~/rpm
           $ yumdownloader --destdir --resolve ~/rpm --resolve package1

            
     ###### __yumdownloader [options] package1 [package2...]__ 

     ###### _General Options_

     ###### __-h, --help__

     ###### Help; display a help message and then quit.

     ###### __--destdir DIR__

     ###### Specify a destination directory for the download. Defaults to the current directory.

     ###### __--urls__
     
     ###### Instead of downloading RPMs, list the URLs that would be downloaded.

     ###### __--resolve__

     ###### When downloading RPMs, resolve dependencies and also download the required packages.

     ###### __--source__

     ###### Instead of downloading the binary RPMs, download the source RPMs.

     ###### __--archlist=ARCH1[,ARCH2...]__

     ###### Limit the query to packages of given architecture(s). Valid values are all architectures known to rpm/yum such as 'i386' and 'src' for source RPMS. Note that repoquery will now change yum's "arch" to the first value in the archlist. So "--archlist=i386,i686" will change yum's canonical arch to i386, but allow packages of i386 and i686.

<br>

## rpm2cpio
3. Use __rpm2cpio__ command :

            rpm2cpio ~/package1.rpm | cpio -idv 

     ###### __rpm2cpio : .rmp --> .cpio fomat__
     
     ###### __cpio -idv : -i --extract, -d --make-directories, -v --verbose__
<br>
Done!
<br><br>


  [1] https://linux.die.net/man/1/yumdownloader

  [2] https://dololak.tistory.com/312
     
  [3] https://www.lesstif.com/system-admin/rpm-20776290.html
  
  [4] https://stackoverflow.com/questions/36651091/how-to-install-packages-in-linux-centos-without-root-user-with-automatic-depen
