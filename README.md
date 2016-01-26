# docker_xfce
oraclelinux6+xrdp+xfce

#Ex
docker run --name xfce -d -p 3389:3389 s4ragent/xfce
##for japanese
##docker run --name xfce -d -p 3389:3389 s4ragent/xfce:ja
docker exec xfce useradd foo
docker exec xfce bash -c 'echo "foo:bar" | chpasswd'
