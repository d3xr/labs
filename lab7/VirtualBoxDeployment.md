# VirtualBox Deployment Process

## Installing VirtualBox

1. Visited the official website of VirtualBox at `https://www.virtualbox.org/`.
2. Navigated to the "Downloads" section.
3. Selected the version compatible with my operating system (in this case, for macOS).
4. Downloaded the `.dmg` file for macOS.
5. Once the download completed, I opened the downloaded file and followed the on-screen instructions to install VirtualBox.
6. After successful installation, launched VirtualBox to verify its version, which is `7.0.10`.

## Deploying a Virtual Machine with Ubuntu 22.04.2 LTS

1. Opened VirtualBox and clicked on the "New" button to create a new virtual machine.
2. Named the VM, selected "Linux" as the type, and "Ubuntu (64-bit)" as the version.
3. Allocated `4096 MB` (4GB) of RAM to the VM.
4. Created a new virtual hard disk with `VDI (VirtualBox Disk Image)` as the type.
5. Chose dynamically allocated storage and set the size to `20 GB`.
6. Once the VM was created, I selected it and clicked on "Settings".
7. Navigated to "Storage" and added the Ubuntu 22.04.2 LTS ISO file to the optical drive.
8. Started the VM and followed the on-screen instructions to install Ubuntu.
9. Once Ubuntu was installed, rebooted the VM and removed the ISO file from the optical drive.
10. Installed VirtualBox Guest Additions for improved performance and integration between the host and guest systems.
