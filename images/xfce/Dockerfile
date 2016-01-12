FROM s4ragent/docker_xfce:init
RUN rpm -ivh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN yum -y groupinstall Xfce && yum -y install xrdp
RUN chkconfig xrdp on
#https://bugzilla.redhat.com/show_bug.cgi?id=1177202
RUN chcon -t bin_t /usr/sbin/xrdp /usr/sbin/xrdp-sesman
ADD .Xclients /etc/X11/xinit/Xclients
