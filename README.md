# ssh-default-banners
Default SSH banner responses

List of default banner responses for Debian, Ubuntu, and FreeBSD

## ssh-os.nse:

Identifies Ubuntu, FreeBSD, or Debian version based on response of SSH banner.  

Identifies the following versions:

Ubuntu 4.10 to 20.04

FreeBSD 4.3 to 12.1-RELEASE

Debian 4.x to 10.x


Note: The accuracy of the response is based on the default banner response.
A number of scenarios may provide an inaccurate result from the target host:

* different OpenSSH version or alternative SSH server installed
* edited/omitted banner via sshd_config
* hexedit of OpenSSH binary; modified banner
* recompiled OpenSSH

#### Usage:
```
nmap -p22 --script ssh-os.nse <target>
```

#### Link to Medium Post:

https://medium.com/@richlam.dev/nmap-ubuntu-debian-freebsd-version-discovery-ssh-oh-ece7e46af26e

#### Link to Nmap Pull Request:

https://github.com/nmap/nmap/pull/1728

