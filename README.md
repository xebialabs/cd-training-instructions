## continuous-delivery-training


### Image details

* OS: Ubuntu precise 32
* IP address: 10.20.20.20
* SSH user/pass: vagrant/vagrant
* Jenkins: http://10.20.20.20:9090/
* Deployit URL: http://10.20.20.20:4516/
* Deployit home: /opt/deployit-server/
* Jboss AS console: http://10.20.20.20:8080/admin-console/ (admin/admin)
* Mysql: root/root
* Maven home: /usr/share/maven (Global env variable MAVEN_HOME is available)
* Java (jdk) home: /usr/lib/jvm/java-6-openjdk-i386 (Global env variable JAVA_HOME is available)

### Steps to perform

1. You need either basic vim skills, or subversion client and some code editor on your laptop. Please take care of it :-)
2. Make sure you have VirtualBox 4.2  installed. It can be downloaded here: https://www.virtualbox.org/wiki/Downloads 
3. Unpack the archive (password should be in the mail you've received). You will get the Virtual Box Appliance file (.ova)
4. Import it to your VirtualBox via graphical interface: File -> Import appliance
5. Make sure that in the settings of the imported virtual machine (right click on machine -> settings -> Network -> Adapter2) name of the host only adapter matches the adapter configured in VirtualBox global preferences (VirtualBox -> Preferences -> Network) and it's IP address 10.20.20.1 and Network Mask is 255.255.255.0. Create a new one and update it in the Machinve Settings if needed.

Imported machine settings:
<img src="http://tech.xebialabs.com/continuous-delivery-training/imported-machine-settings.png" alt="Imported machine settings" />


Global Virtualbox Preferences:
<img src="http://tech.xebialabs.com/continuous-delivery-training/global-vbox-preferences.png" alt="Global Virtualbox Preferences" />

### Smoke test

In the end you should be able to access the following URLs:

* Jenkins: http://10.20.20.20:9090/
* Deployit: http://10.20.20.20:4516/
* Jboss: http://10.20.20.20:8080/
* Svn: http://10.20.20.20/svn/
* Apache: http://10.20.20.20/


### Notes

* Shall you restart deployit or jboss - do it with sudo (since it was started via rc.local first time, some lock/temp files will have root ownership).
* Jboss should be started with binding IP address 0.0.0.0: sudo /opt/jbossas/5.1.0.GA/bin/run.sh -b 0.0.0.0
    



