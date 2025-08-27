# Centos
Patch Centos

## Folder

`<Centos version>/<package name>/<version>`

You can find the sources to build the package in the rpmbuild folder and the RPMs in RPMS folder.

# Centos 6

## ISO

- [http://vault.centos.org/6.10/isos/x86_64](http://vault.centos.org/6.10/isos/x86_64)

## Repo

The repos are no longer correct, so you have to delete the old ones and add the new ones manually:
```sh
sudo mv /etc/yum.repos.d/* /tmp/.
sudo vim /etc/yum.repos.d/new.repo
```

Add the following lines:
```
[base]
name=CentOS-6 - Base
baseurl=https://vault.centos.org/6.10/os/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=1

[updates]
name=CentOS-6 - Updates
baseurl=https://vault.centos.org/6.10/updates/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=1

[extras]
name=CentOS-6 - Extras
baseurl=https://vault.centos.org/6.10/extras/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=1

[centosplus]
name=CentOS-6 - Plus
baseurl=https://vault.centos.org/6.10/centosplus/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=0
```

Clean up the repos:
```sh
sudo yum clean all
sudo yum makecache
```

# Centos 7


## ISO

- [https://vault.centos.org/7.9.2009/isos/x86_64/](https://vault.centos.org/7.9.2009/isos/x86_64/)

## Repo

The repos are no longer correct, so you have to delete the old ones and add the new ones manually:
```sh
sudo mv /etc/yum.repos.d/* /tmp/.
sudo vim /etc/yum.repos.d/new.repo
```

Add the following lines:
```
[base]
name=CentOS-7 - Base
baseurl=http://vault.centos.org/7.9.2009/os/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
enabled=1

[updates]
name=CentOS-7 - Updates
baseurl=http://vault.centos.org/7.9.2009/updates/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
enabled=1

[extras]
name=CentOS-7 - Extras
baseurl=http://vault.centos.org/7.9.2009/extras/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
enabled=1

[centosplus]
name=CentOS-7 - Plus
baseurl=http://vault.centos.org/7.9.2009/centosplus/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
enabled=0
```

Clean up the repos:
```sh
sudo yum clean all
sudo yum makecache
```
