s# Installing From the AUR
## General
Description | Command
------------ | ------------
Updating the PC | `yay`
Clone Repo | `git clone https://aur.archlinux.org/<pkgName>.git` 
Change the Active Directory | `cd <package name`
Start the Building Process | `makepkg -sri`


## Manual
Description | Command
------------ | ------------
Updating the PC | `yay`
Get Repo | `wget https://aur.archlinux.org/packages/{package-name}.tar.gz` 
Uncompress the Tarball | `$ tar -xvzf  {package-name}.tar.gz`
Start the Building Process | `makepkg -sri`

# Uninstalling A Package
`sudo pacman -Rs <package name>`
