FROM centos:7
##configure for containers
RUN mkdir -p /selinux &&\
    echo 0 > /selinux/enforce
RUN rm -f /etc/systemd/system/default.target &&\
    touch /etc/fstab &&\
    ln -s /dev/null /etc/systemd/system/udev.service &&\
    ln -s /lib/systemd/system/multi-user.target /etc/systemd/system/default.target &&\
    ln -s /usr/lib/systemd/system/halt.target /etc/systemd/system/sigpwr.target &&\
    sed -e 's/^ConditionPathExists=/# ConditionPathExists=/' \
        -e 's/After=dev-%i.device/After=/' \
        < /lib/systemd/system/getty\@.service > /etc/systemd/system/getty\@.service &&\
    ln -s /dev/null /etc/systemd/system/getty@tty1.service &&\
    ln -s /dev/null /etc/systemd/system/serial-getty@ttyS0.service
VOLUME [ “/sys/fs/cgroup” ]
CMD ["/sbin/init"]
