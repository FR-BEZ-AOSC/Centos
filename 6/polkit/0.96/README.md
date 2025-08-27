# Build

```sh
mkdir -p ~/Centos/6/polkit/0.96/rpmbuild/{BUILD,BUILDROOT,RPMS,SRPMS}
rpmbuild -ba ~/Centos/6/polkit/0.96/rpmbuild/SPECS/log4j.spec
```

# Install

```sh
sudo yum localinstall ~/Centos/6/polkit/0.96/rpmbuild/RPMS/x84_64/*.rpm
rpm -qa | grep log4j
```