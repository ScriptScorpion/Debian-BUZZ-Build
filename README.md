# How to install Debian Buzz for QEMU:
## To launch boot floppy: 
use `qemu-system-i386 -drive format=raw,if=floppy,file=boot1440.bin -monitor stdio` or you can use `qemu-system-i386 -fda boot1440.bin -monitor stdio`.

## After launching boot floppy: 
in the terminal from where you launched boot floppy you can list all floppies by doing `info block` and you can change floppies by doing `change floppy0 root.bin`.

# How to install Debian Buzz for Oracle VirtualBox:
## To launch boot floppy:
create empty VM, in the "Storage" tab of the VM settings press "Add controller"
[!Image](img/img0.png)
in the menu press option that says "Floppy" and add boot floppy
[!Image](img/img1.png)
[!Image](img/img2.png)
[!Image](img/img3.png)
after that save settings of the VM and launch it.

## After launching boot floppy:
you can change floppies by pressing "Devices" and then "Floppy Drives" and selecting which floppy to use
[!Image](img/img4.png)
or you can add new floppies by pressing "Choose a Disk file ..." and selecting new floppy that will be available for selection.
[!Image](img/img5.png)

# How to create blank/empty floppy disk:
`sudo mkfs.vfat -F 12 -C floppy1440.img 1440`
