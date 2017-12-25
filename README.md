# virtualbox-tips_tricks

## Share folder between windows host and ubuntu virtual machine.
  1. Setup shared folder in Virtual Box - 
     1. Even before lauching the virtual machine, firstly setup the shared folder in virtual box. 
     1. Open settings for the Virtual Machine
     1. Go to option Shared folders
     1. Choose the right details which is the alias to be referred inside VM and actual path on windows. *No need to check Auto-Mount.*
  1. Install virtual box guest addons - 
     This is available once you have launched the VM, on the top toolbar "Devices -> Install Guest Additions"
  1. Mount shared folder in VM - 
     Use the following command to mount shared folder: \
	 **template** `sudo mount -t vboxsf <alias used while create shared folder in virtual box> <absolute path on linux machine>`\
	 **example** `sudo mount -t vboxsf git_source /home/himanshu/git_source_shared`
