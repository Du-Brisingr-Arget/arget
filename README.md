# Arget
A multifunctional aur helper that installs packages the standard way using

    makepkg -sirc
=> as if you were building and installing the packages yourself!

Arget can install/upgrade multiple packages at once.

Also, Arget can remove all files and dependencies that aren't needed automatically.

# Versions
Arget v 1.0.0 https://github.com/Garjzla/arget/tree/ab3f5541665313f8d5d30c6e8d22f49eec2b8764

Arget v 2.0.0 https://github.com/Garjzla/arget/tree/be3d7dd7e7e2ab6a7191ba464eb2c90f3d9a57a6
# Install Arget
Go in the git cloned arget directory

run

    sudo bash installer.argt
run

    argt -upd

# How to Use
you can install/update packages by running this

    argt -i <package-name>
update all packages installed with Arget ( pacman -Syu won't be able to update these packages unless you configure pacman.conf )

    argt -upd

update all packages installed on your system ( equivalent to running both pacman -Syyu and argt -upd together )

    argt -syu

To work with multiple packages, quote the packages like this

    argt -i 'pkg1 pkg2 pkg3'
delete packages

    argt -d <package-name>
    argt -d 'pkg1 pkg2 pkg3'
list installed packages by arget

    argt lst
show help and version

    argt
If you have many packages to install, but don't want to type 'y' every time, type the commands with -m at the back.

    argt -i 'pkg1 pkg2 pkg3 pkg4 pkg5' -m
    argt -upd -m
    argt -syu -m
deleting with '-m' won't work, as you should see exactly what is being uninstalled.

# Uninstall Arget
Run

    sudo rm /usr/bin/argt
    sudo rm -rf /arget

# Important
Arget uses many temporary files, so don't interrupt when arget is running (like with ctrl+c)

If arget was interrupted, go to /arget and delete every file and directory except all-package-names.argt
