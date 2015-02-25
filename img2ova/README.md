img2ova
=======

Converts an image to OVA format.

# Requirements
- python 
- qemu-img
- VirtualBox (for converting to VMDK)
- libguestfs-tools (for resizing and syspreping the image)

# Usage
./img2ova -n <name> -i <image file> -d <os description> [-s <size of disk>]

- You will probably need sudo privileges to run the command!
- The resulting file will be <name>.ova and will contain a
   - <name>.mf: manifest file
   - <name>-disk1.vmdk: disk file 
   - <name>.ovf: OVF file describing the image 
- -d option is used to put a description of the Operating System in the OVF file,
  in principle, any value should be ok
- -s allows to specify a size for the resulting image.



