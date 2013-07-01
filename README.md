rpm-collectd
============

An RPM spec file to build and install collectd with most plugins enabled. The JVM plugin works against the Oracle JVM and the Python plugin works against an alt-installed Python26 binary.

To Build:

`sudo yum -y install rpmdevtools && rpmdev-setuptree`

`sudo yum -y install curl-devel libesmtp-devel libmemcached-devel net-snmp-devel OpenIPMI-devel libpcap-devel librabbitmq-devel lm_sensors-devel libevent-devel libgcrypt-devel openssl-devel jdk python26-devel`

`wget https://raw.github.com/nmilford/rpm-collectd/master/collectd.spec -O ~/rpmbuild/SPECS/collectd.spec`

`wget https://raw.github.com/nmilford/rpm-collectd/master/collectd -O ~/rpmbuild/SOURCES/collectd`

`wget http://collectd.org/files/collectd-5.2.0.tar.gz -O ~/rpmbuild/SOURCES/collectd-5.2.0.tar.gz`

`QA_RPATHS=[0-7] rpmbuild -bb ~/rpmbuild/SPECS/collectd.spec`