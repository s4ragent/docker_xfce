FROM s4ragent/xfce
RUN yum -y groupinstall "Japanese Support"
RUN curl -L http://www.mail-archive.com/xrdp-devel@lists.sourceforge.net/msg00263/km-e0010411.ini -o ./km-e0010411.ini &&\
        cp ./km-e0010411.ini /etc/xrdp/km-e0010411.ini &&\
        cp /etc/xrdp/km-e0010411.ini /etc/xrdp/km-0411.ini &&\
        cp /etc/xrdp/km-e0010411.ini /etc/xrdp/km-e0200411.ini &&\
        cp /etc/xrdp/km-e0010411.ini /etc/xrdp/km-e0210411.ini
RUN rm ./km-e0010411.ini
ENTRYPOINT ["/sbin/init"]
