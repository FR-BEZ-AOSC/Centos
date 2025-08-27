# CentOS Patches Repository

(Français / English)

## 🇫🇷 Description

Ce dépôt contient des patchs et reconstructions de paquets CentOS.
Il met à disposition :
- les sources et fichiers de build pour reconstruire les paquets (rpmbuild/)
- les binaires RPM déjà compilés (RPMS/)

### ⚠️ Licence
> Les paquets fournis ici conservent la licence de leurs projets d’origine (GPL, MIT, BSD, etc.).
> Ce dépôt ne fait que les regrouper et proposer un accès simplifié. Vérifiez la licence de chaque paquet via rpm -qi <package>.

## Structure du dépôt
```sh
<CentOS version>/<package name>/<version>/
 ├── rpmbuild/   # sources et spec pour reconstruire le paquet
 └── RPMS/       # binaires RPM prêts à l’emploi
```

Exemple:
```sh
7/libblockdev/2.30/
├── rpmbuild/
└── RPMS/
```

## 🇬🇧 Description  

This repository contains **patches and rebuilt CentOS 7 packages**.  
It provides:  
- the **sources and build files** to rebuild the packages (`rpmbuild/`)  
- the **precompiled RPM binaries** (`RPMS/`)  

### ⚠️ Important 
> The RPM packages here retain the original license of their upstream projects (GPL, MIT, BSD, etc.).  
> This repository only redistributes them for convenience. You can check each package license with `rpm -qi <package>`.  

## Repository Structure  

```sh
<CentOS version>/<package name>/<version>/
├── rpmbuild/ # sources and spec files to rebuild the package
└── RPMS/ # prebuilt RPM binaries
```

Example:
```sh
7/libblockdev/2.30/
├── rpmbuild/
└── RPMS/
```

---

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
