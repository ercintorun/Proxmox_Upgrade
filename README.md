    apt update
    apt dist-upgrade 
    pveversion 


    sudo nano /etc/apt/sources.list
    deb http://ftp.debian.org/debian bookworm main contrib
    deb http://ftp.debian.org/debian bookworm-updates main contrib
    # Proxmox VE pve-no-subscription repository provided by proxmox.com,
    # NOT recommended for production use
    deb http://download.proxmox.com/debian/pve bookworm pve-no-subscription
    # security updates
    deb http://security.debian.org/debian-security bookworm-security main contrib



    echo "deb http://download.proxmox.com/debian/ceph-quincy bookworm no-subscription" > /etc/apt/sources.list.d/ceph.list 
    apt update 
    apt dist-upgrade 
    reboot
