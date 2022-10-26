# FaceRoll

This script was created to back up my home server (which runs Windows Server). It offers the option to include a customizable list of folders referred to as Minutia, but the primary function is to backup the entirety of multiple drives to a single destination drive that is formatted in the ReFS file format before copying begins. It features estimation of the data size the user wants to backup, ensuring that enough capacity exists at the backup destination.
There is also an option to include a system backup (using the built in Windows Backup functionality accessible through the GUI). If this is chosen and there are VMware Workstation VMs running, an option is provided to shut them down -- a command is issued to tell the OS to shutdown gracefully. If no system backup is chosen, this is ignored. 
The backup process itself uses robocopy, each drive's contents reside within a folder on the destination drive, and a log is provided noting the time when each section of the backup process begins, and when it has completed.
