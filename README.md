# how-to-install-kvm-on-fedora
how-to-install-kvm-on-fedora

source
```
https://fedoramagazine.org/full-virtualization-system-on-fedora-workstation-30/
```

## Step 1: install packages
```
sudo dnf install @virtualization
```

## Step 2: edit the libvirtd configuration
```
sudo vi /etc/libvirt/libvirtd.conf
```

uncomment 2 lines
```
unix_sock_group = "libvirt"
unix_sock_rw_perms = "0770"
```

## Step 3: start and enable the libvirtd service
```
sudo systemctl start libvirtd
sudo systemctl enable libvirtd
```

## Step 4: add user to group
```
sudo usermod -a -G libvirt $(whoami)
```

Open search fedora and search "virtual machine manager"
