# Build

```sh
mkdir -p ~/Centos/6/log4j/1.2.14/rpmbuild/{BUILD,BUILDROOT,RPMS,SRPMS}
rpmbuild -ba ~/Centos/6/log4j/1.2.14/rpmbuild/SPECS/log4j.spec
```

# Install

```sh
sudo yum localinstall ~/Centos/6/log4j/1.2.14/rpmbuild/RPMS/x84_64/*.rpm
rpm -qa | grep log4j
```