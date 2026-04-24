# openssh
openssh_for_X86_operation_system_rpm
************************************************************************************示例如下、仅供参考********************************************************************************** \


##编译rpm包 \
mkdir /soft  ##创建文件夹 \
##安装依赖包 \
yum install -y imake rpm-build pam-devel krb5-devel zlib-devel libXt-devel libX11-devel gtk2-devel perl perl-IPC-Cmd \
mkdir -p /root/rpmbuild/{RPMS,SOURCES,SPECS} \
cd /root/rpmbuild/SOURCES \
wget https://cdn.openbsd.org/pub/OpenBSD/OpenSSH/portable/openssh-9.7p1.tar.gz \
wget https://src.fedoraproject.org/repo/pkgs/openssh/x11-ssh-askpass-1.2.4.1.tar.gz/8f2e41f3f7eaa8543a2440454637f3c3/x11-ssh-askpass-1.2.4.1.tar.gz \
wget https://www.openssl.org/source/openssl-3.0.13.tar.gz \
分别上传openssh.spec和pam.d文件到/root/rpmbuild/SPECS和/root/rpmbuild/SOURCES下 \
cd /root/rpmbuild/SPECS \
rpmbuild -ba openssh.spec \
rpm -ivh  /soft/openssh/openssh-9.6p1-1.an8.src.rpm \
cd /soft/openssh/ \
yum install -y openssh*.rpm \




rpm -ivh /soft/openssh/openssh-9.6p1-.al8.src.rpm \\
/soft/openssh//openssh-9.6p1-.al8.x86_64.rpm \\
/soft/openssh//openssh-clients-9.6p1-.al8.x86_64.rpm \\
/soft/openssh//openssh-server-9.6p1-.al8.x86_64.rpm \\
/soft/openssh//openssh-askpass-9.6p1-.al8.x86_64.rpm \\
/soft/openssh//openssh-askpass-gnome-9.6p1-.al8.x86_64.rpm \\
/soft/openssh//openssh-debugsource-9.6p1-.al8.x86_64.rpm \\
/soft/openssh//openssh-debuginfo-9.6p1-.al8.x86_64.rpm \\
/soft/openssh//openssh-clients-debuginfo-9.6p1-.al8.x86_64.rpm \\
/soft/openssh//openssh-server-debuginfo-9.6p1-.al8.x86_64.rpm \\
/soft/openssh//openssh-askpass-debuginfo-9.6p1-.al8.x86_64.rpm \\
/soft/openssh//openssh-askpass-gnome-debuginfo-9.6p1-.al8.x86_64.rpm




yum install -y autoconf libtool libtool-lydl-devel libuuid-devel 
yum install -y gettext-devel
yum install -y libxml2-devel
yum install -y libxslt-devel
yum install -y libqb libqb-devel

rpm -e `rpm -qa | grep openssh` --nodeps
rpm -ivh /soft/openssh/openssh-9.7p1-.el7.src.rpm \
/soft/openssh/openssh-9.7p1-.el7.x86_64.rpm \
/soft/openssh/openssh-clients-9.7p1-.el7.x86_64.rpm \
/soft/openssh/openssh-server-9.7p1-.el7.x86_64.rpm \
/soft/openssh/openssh-askpass-9.7p1-.el7.x86_64.rpm \
/soft/openssh/openssh-askpass-gnome-9.7p1-.el7.x86_64.rpm \
/soft/openssh/openssh-debuginfo-9.7p1-.el7.x86_64.rpm \

##重启服务
chmod 600 /etc/ssh/ssh_host_rsa_key
chmod 600 /etc/ssh/ssh_host_ecdsa_key
chmod 600 /etc/ssh/ssh_host_ed25519_key
systemctl restart sshd



scp /root/rpmbuild/SRPMS/openssh-9.7p1-.el7.src.rpm \
/root/rpmbuild/RPMS/x86_64/openssh-9.7p1-.el7.x86_64.rpm \
/root/rpmbuild/RPMS/x86_64/openssh-clients-9.7p1-.el7.x86_64.rpm \
/root/rpmbuild/RPMS/x86_64/openssh-server-9.7p1-.el7.x86_64.rpm \
/root/rpmbuild/RPMS/x86_64/openssh-askpass-9.7p1-.el7.x86_64.rpm \
/root/rpmbuild/RPMS/x86_64/openssh-askpass-gnome-9.7p1-.el7.x86_64.rpm \
/root/rpmbuild/RPMS/x86_64/openssh-debuginfo-9.7p1-.el7.x86_64.rpm ptdb01:/soft/.



rpm -ivh /root/openssh-9.7p1-oe2203.src.rpm \
/root/openssh-askpass-gnome-9.7p1-oe2203.x86_64.rpm \
/root/openssh-askpass-9.7p1-oe2203.x86_64.rpm \
/root/openssh-debugsource-9.7p1-oe2203.x86_64.rpm \
/root/openssh-server-9.7p1-oe2203.x86_64.rpm \
/root/openssh-debuginfo-9.7p1-oe2203.x86_64.rpm \
/root/openssh-clients-9.7p1-oe2203.x86_64.rpm \
/root/openssh-9.7p1-oe2203.x86_64.rpm
chmod 600 /etc/ssh/ssh_host_rsa_key
chmod 600 /etc/ssh/ssh_host_ecdsa_key
chmod 600 /etc/ssh/ssh_host_ed25519_key
systemctl restart sshd

scp /root/rpmbuild/SRPMS/openssh-9.7p1-oe2203.src.rpm /root/rpmbuild/RPMS/x86_64/openssh-askpass-gnome-9.7p1-oe2203.x86_64.rpm /root/rpmbuild/RPMS/x86_64/openssh-askpass-9.7p1-oe2203.x86_64.rpm /root/rpmbuild/RPMS/x86_64/openssh-debugsource-9.7p1-oe2203.x86_64.rpm /root/rpmbuild/RPMS/x86_64/openssh-server-9.7p1-oe2203.x86_64.rpm /root/rpmbuild/RPMS/x86_64/openssh-debuginfo-9.7p1-oe2203.x86_64.rpm /root/rpmbuild/RPMS/x86_64/openssh-clients-9.7p1-oe2203.x86_64.rpm /root/rpmbuild/RPMS/x86_64/openssh-9.7p1-oe2203.x86_64.rpm 192.168.100.106:/soft/.
