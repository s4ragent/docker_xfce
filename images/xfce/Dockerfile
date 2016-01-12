FROM s4ragent/docker_xfce:init
RUN rpm -ivh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN yum -y update && yum -y clean all
RUN yum -y groupinstall Xfce && yum -y install xrdp
RUN chkconfig xrdp on
ADD .Xclients /etc/X11/xinit/Xclients
