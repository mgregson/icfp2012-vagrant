ICFP Programming Contest 2012 Vagrant Template
==============================================
This project hosts a Vagrant template similar to the judge's environment for the
2012 ICFP programming contest as described
[here](http://icfpcontest2012.wordpress.com/2012/07/05/judging-environment/).


Using
-----
Configure your Vagrant project based on the Vagrantfile in this repository.  You
can probably just drop the provided Vagrantfile into a directory and run:

    vagrant up

Here's an example:

    mgregson@fenrir ~/src/icfp2012 $ ls
    Vagrantfile
    mgregson@fenrir ~/src/icfp2012 $ vagrant up
    [default] Box icfp2012 was not found. Fetching box from specified URL...
    [vagrant] Downloading with Vagrant::Downloaders::HTTP...
    [vagrant] Downloading box: https://github.com/downloads/mgregson/icfp2012-vagrant/icfp2012.box
    [vagrant] Downloading box: http://cloud.github.com/downloads/mgregson/icfp2012-vagrant/icfp2012.box
    [vagrant] Extracting box...
    [vagrant] Verifying box...
    [vagrant] Cleaning up downloaded box...
    [default] Importing base box 'icfp2012'...
    [default] The guest additions on this VM do not match the install version of
    VirtualBox! This may cause things such as forwarded ports, shared
    folders, and more to not work properly. If any of those things fail on
    this machine, please update the guest additions and repackage the
    box.
    
    Guest Additions Version: 3.2.10
    VirtualBox Version: 4.1.16
    [default] Matching MAC address for NAT networking...
    [default] Clearing any previously set forwarded ports...
    [default] Forwarding ports...
    [default] -- 22 => 2222 (adapter 1)
    [default] Creating shared folders metadata...
    [default] Clearing any previously set network interfaces...
    [default] Booting VM...
    [default] Waiting for VM to boot. This can take a few minutes.
    [default] VM booted and ready for use!
    [default] Mounting shared folders...
    [default] -- v-root: /home/vagrant/src
    mgregson@fenrir ~/src/icfp2012 $ vagrant ssh
    Linux icfp2012 2.6.32-5-686 #1 SMP Sun May 6 04:01:19 UTC 2012 i686
    
    The programs included with the Debian GNU/Linux system are free software;
    the exact distribution terms for each program are described in the
    individual files in /usr/share/doc/*/copyright.
    
    Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
    permitted by applicable law.
    Last login: Tue Jul 10 18:27:17 2012 from 10.0.2.2
    vagrant@icfp2012:~$ hostname
    icfp2012    
    

Notes
-----
The VM will whine on boot:

    [default] The guest additions on this VM do not match the install version of
    VirtualBox! This may cause things such as forwarded ports, shared
    folders, and more to not work properly. If any of those things fail on
    this machine, please update the guest additions and repackage the
    box.
    
    Guest Additions Version: 3.2.10
    VirtualBox Version: 4.1.16

This is probably okay, but if it bothers you it can be fixed by installing the
correct VirtualBox guest additions version for your VirtualBox version.
Something like [this](http://blog.carlossanchez.eu/2012/05/03/automatically-download-and-install-virtualbox-guest-additions-in-vagrant/)
might be helpful.
