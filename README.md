# QEMU SYSTEM EXAMPLE

### CREATE IMG DISK
```sh
IMG_DISK="$RESOURSE_DIR/disks/disk_0.img"
if [ ! -e "${IMG_DISK}" ]; then
	if [ ! -x "/usr/bin/qemu-utils" ]; then
		echo "Install qemu-utils ..."
		apt-get install --no-install-suggests --no-install-recommends qemu-utils
	fi
	qemu-img create "${IMG_DISK}" 100G
fi
```