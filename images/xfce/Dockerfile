FROM s4ragent/docker_xfce:init
RUN yum -y install epel-release && yum -y --enablerepo=epel groupinstall Xfce && yum -y install xrdp
sudo systemctl enable xrdp
#https://bugzilla.redhat.com/show_bug.cgi?id=1177202
RUN chcon -t bin_t /usr/sbin/xrdp /usr/sbin/xrdp-sesman
ADD .Xclients /etc/X11/xinit/Xclients
