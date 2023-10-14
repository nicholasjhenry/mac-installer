# Mac Installer

Download an the MacOS installer, example:

```
softwareupdate --list-full-installers
softwareupdate --fetch-full-installer --full-installer-version 13.6
```

Create a bootable installer:

```
ls /Volumes
sudo /Applications/Install\ macOS\ Ventura.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

To build a DMG installer for VM Fusion (recommend performing this in ~/Development/installers):

https://github.com/rtrouton/create_macos_vm_install_dmg

```
sudo /path/to/create_macos_vm_install_dmg.sh "/Applications/Install macOS Mojave.app" /path/to/output_directory
```

## Troubleshooting

Error: "Unable to create the installation medium"

Cause: If you are trying to create a VM using the installer, e.g. Install macOS Ventura, you must
create a DMG file (see above).

## References

* [How to Download and Install Older macOS Versions With Terminal](https://lifehacker.com/how-to-download-and-install-older-macos-versions-with-t-1839671161#:~:text=To%20download%20older%20builds%20of,to%20your%20Mac%27s%20Applications%20folder.)
* [Create a bootable installer for macOS](https://support.apple.com/en-ca/HT201372)
