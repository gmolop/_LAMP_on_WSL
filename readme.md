# _LAMP_on_WSL

## After clean WSL setup...

(1) Update system

    sudo apt -y update
    sudo apt -y install software-properties-common
    sudo apt -y upgrade

(2) Install git

    sudo apt -y install git

(3) Download the project

    git clone https://github.com/gmolop/_LAMP_on_WSL.git ~/_lamp

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

---

Files:
- readme.md        // install steps
- prepare-wsl-lamp // install lamp
- create-project   // creates vhost and project folder
- generate-ssl     // create a SSL auto-signed certificate for given site
- index            // localhost index
- clean            // removes server files
- vhost-template   // template for new projects
