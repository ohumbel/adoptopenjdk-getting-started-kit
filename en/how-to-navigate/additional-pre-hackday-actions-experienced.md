# Additional pre-hackday actions for experienced attendees

##### Build your own VM

Note: you will need good bandwidth to download the files, and ample time for the build to finish.
<br/>
[Build your own VM](../virtual-machines/build_your_own_vm.md) <br/>
[Build your own light-weight VM](../virtual-machines/build_your_own_lightweight_vm.md)

<br/>
##### Check VM
- Load the VM into VirtualBox
- Start the VM
- Run any program inside the VM
- Shutdown the VM

<br/>
##### Download / copy VM Images
Images can be copied from one disk to another or downloaded from a central repository.

or
<br/>
##### Build Containers
Checkout the build section of [](). 

<br/>
##### Check Containers
Checkout the verify section of []().

<br/>
##### Verify installation and environment
Start the VM or Container, navigate to the jdk8 or jdk9 folders, and run the below command:

```bash configure```
```make clean images```

If one of these fails then the OpenJDK environment isn't correctly set or the new build is broken in OpenJDK master.

##### Finally
When done go to the [How to navigate and make progress ?](how-to-navigate-and-make-progress.md) section, and move to the next step to continue with the flow.