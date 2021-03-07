Install dependencies:
```
sudo apt install kmod gcc make
```

Compilation
```
make all
```

Test
```
make test
```

Installation
```
sudo insmod lkm_example.ko
sudo lsmod|grep example
```

Run docker as priveled in order to grant access to all devices on host
```
docker run -ti --privileged --cap-add=ALL -v /dev:/dev ubuntu:18.04 bash
cat /proc/1/status |grep Cap
apt update && apt install kmod -y
lsmod |grep lkm_example
rmmod lkm_example
```

More info
https://docs.docker.com/engine/reference/run/#runtime-privilege-and-linux-capabilities
https://phoenixnap.com/kb/docker-privileged

