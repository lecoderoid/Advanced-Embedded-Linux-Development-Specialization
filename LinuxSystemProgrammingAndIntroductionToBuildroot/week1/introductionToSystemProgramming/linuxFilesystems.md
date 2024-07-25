# Linux Filesystem

## *Everything is a File*
- much of the interaction with the kernel occurs via reading/writing files 
- devices are accessed similar to files 
     - example /dev/ttyUSB0 for USB serial port
- common open, manipulate, close paradigm shared with files and devices

--
## Files in Linux
- Represented by paths
    - **Absolute** *"/path/to/file"* : from root of filesystem
    - **Relative** *"path/to/file"* : from working direcotry
        - no leading */*

### Linux Regular File Properties
- bytes of data in a byte stream
    - no structure enforced at the system level
- file position/offset tracks location
- can be truncated to size smaller or larger than original
- can be opened more than once, by different or same process
- referenced and accessed by inode in the filesytem 

--- 

## Linux Inode (Index Node)
- metadata used to track files on disk
- includes timestamp, owner, size, mode (access permission), location
- fixed small size (128 bytes). filename not included

## Linux directories
- why not include filenames in inodes?
    - allows different file names to share the same content without duplicating inode content

## Linux Links
- flexibility of inode design means multiple names can resolve to the same inode
- links redirect two file/directory paths to the same inode
- 2 types of links, Hard and Symbolic (symlinks)
    - Hard links map directly to inodes, only allowed on the same file system
        - can't span filesystems(inode references a specific filesystem)
        -conecptually the same as a Directory Entry
        - file deletes aren't allowed until all references are deleted(preventing broken Hard links)
    - soft links map to filenames, works accross filesystems, can be broken
        - regular file with complete path in content
        - can point anywhere, including other filesystems, can break
        - reqiures extra step to resolve

---

## Linux Special Files
- Map hardware devices to the *everythins is a file* paradigm
- Kernel objects represented as files.
    - Character devices
        - linear queue of bytes
        - ex. keyboard
    - block devices
        - array of bytes, addressable in a sector
        - ie hard disk
    - named pipes
        - interprocess communication
    - sockets

---

## Linux Filesystem
- collection of files in a hierarchy
- specific types supported, tied to storage types   
    - NFS - network file storage
    - ext4 - block device storage
    - fat - MS defined storage format for disks
    - mounted/unmounted to add/remove from the root filesystem
    - smallest unit addressable is a block
        - block is a power of two multiple of sector size
        - typical/historical sector size is 512 bytes
