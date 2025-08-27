# Build

```sh
mkdir -p ~/Centos/7/libblock/libblockdev/2.30/rpmbuild/{BUILD,BUILDROOT,RPMS,SRPMS}
rpmbuild -ba ~/Centos/7/libblock/libblockdev/2.30/rpmbuild/SPECS/libblockdev.spec
```

# Install

```sh
sudo yum install ~/Centos/7/libblock/libblockdev/2.30/rpmbuild/RPMS/x84_64/*.rpm
rpm -qa | grep libblockdev
```