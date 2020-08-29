## diskutil delete partitions (link)[https://apple.stackexchange.com/questions/320357/how-to-merge-all-the-partitions-to-normal]

    diskutil list
    diskutil ap list
    to get the details.

    Check your disk:

    diskutil verifyDisk disk0
    diskutil verifyVolume disk0s2
    Remove all partitions and container except the main container:

    diskutil eraseVolume "Free Space" Nil disk0s5
    diskutil ap deleteContainer disk2
    diskutil ap deleteContainer disk3
    disktutil list #to get the new dev identifiers of the converted partitions
    diskutil eraseVolume "Free Space" Nil disk0sY # Y probably one of [3-7]
    diskutil eraseVolume "Free Space" Nil disk0sX # X probably one of [3-7]