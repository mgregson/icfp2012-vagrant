ICFP Programming Contest 2012 Vagrant Template
==============================================
This project hosts a Vagrant template similar to the judge's environment for the
2012 ICFP programming contest as described
[here](http://icfpcontest2012.wordpress.com/2012/07/05/judging-environment/).


Using
-----
Configure your Vagrant project based on the Vagrantfile in this repository.


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
