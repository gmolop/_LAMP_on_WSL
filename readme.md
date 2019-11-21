## After clean WSL setup...

(1) Update system

    sudo apt -y update
    sudo apt -y install software-properties-common
    sudo apt -y upgrade

(2) Install git

    sudo apt -y install git

(3) Download the project

    git clone https://gist.github.com/1481a9789785bd7e6103d93ef2f73c0a.git ~/_lamp

(4) Run the installer (& define 'DocumentRoot' dir)

    sh ~/_lamp/prepare-wsl-lamp "/mnt/c/Users/<you>/www"

(5) Create project exmple

    sh ~/_lamp/create-project "test-domain.local"
    sh ~/_lamp/create-project "test-domain.local" "path-to-project-under-server-root/test-domain"
    sh ~/_lamp/create-project "test-domain.local" "path-to-project-under-server-root/test-domain" "public-root-folder-under-project-path"

done ;)...

---

Tested (29-oct-19) under:
* Windows 10 Pro 1903
* WSL 10.0.18362.239 (WSL 1)
* Debian 10.1 (buster)

> WSL install notes: https://wiki.debian.org/InstallingDebianOn/Microsoft/Windows/SubsystemForLinux