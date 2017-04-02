### Storage Gateway

* **Storage Gateware**: seamlessly enables hybrid cloud storage between on-premises
    environments and the AWS Cloud. It combines a multi-protocol storage appliance
    with highly efficient network connectivity to deliver local performance with
    virtually unlimited scale.
* **Hypervisor**: a.k.a virtual machine monitor (VMM) is computer software,
    firmware, or hardware, that creates and runs virtual machines.
* **Virtual Appliance**: A pre-configured virtual machine image, ready to run on a
    hypervisor
* Storage Gateway is a virtual appliance which asynchronously replicates your data
    center to S3 or Glacier.
* **Network File System (NFS)**: allows a user on a client computer to access files
    over a computer network much like local storage is accessed.
* **Internet Small Computer Systems Interface (iSCSI)**: Pronounced iskazi, is an
    Internet Protocol (IP)-based storage networking standard for linking data
    storage facilities. It provides block-level access to storage devices by
    carrying SCSI commands over a TCP/IP network.
* **A virtual tape library (VTL)**: a data storage virtualization technology used
    typically for backup and recovery purposes. A VTL presents a storage component
    (usually hard disk storage) as tape libraries or tape drives for use with
    existing backup software.
* There are four types of Storage Gateways: *File Gateway* (NFS), *Volumes Gateway*
    (iSCSI) which can be *Stored Volume* or *Cached Volume*, and *Taped Gatedway*
    (VTL).
* The File Gateway configuration offers on-premises servers and applications a
    network file share. File data is cached on the File Gateway for local
    performance and converted to objects stored in Amazon S3. You can protect
    your objects through native tools like versioning and cross-region
    replication.
* Architecture of the File Gateway is as follows: Your application server connects
    Through NFS to the Storage Gateway (which is a virtual machine). You can then
    connect the Storage Gateway using the internet, (Or Direct Connect or VPC) and
    connects to the S3 buckets. Your application itself can also be on AWS so this
    whole thing can be in AWS.
* The Volume Gateway configuration connects to on-premises servers and applications
    as a local disk. Data in these volumes can be transferred into Amazon S3 cloud
    storage and accessed through the Volume Gateway. Store data locally for the
    highest performance (with snapshot backups to the cloud), or blend latency and
    scale by storing frequently-accessed data locally with "cooler" data in the
    cloud.
* Architecture of the Stored Volumes is as follows: Your application server
    connects through iSCSI to the Gateway VM. The Gateway then stores the data
    locally, and creates flat file snapshots which it uploads to S3. All your
    data remains on site.
* Basically Stored Volume takes your hard-disks and backs them up as Elastic
    Block Storage (EBS) in AWS as virtual hard-disks. These backups are done as
    point-in-time snapshots of your volumes, which only capture the changed
    blocks from last snapshot. Storage is automatically compressed. Size varies
    from 1GB to 16TB.
* Unlike Stored Valume, Cached Volumes uses S3 to store the bulk of your data,
    while retaining frequently accessed data locally in your storage gateway. This
    allows you to have minimal local storage while still having low latency disk
    access for your application. Cached Volume ranges from 1GB to 32TB.
* Cached Volume architecture is similar to the stored volume one, with the
    difference being that both the volume storage and the snapshots are on AWS,
    instead of only the snapshots as is the case with stored volumes.
* The Tape Gateway configuration replaces backup tapes and tape automation
    equipment with local disk and cloud storage. Your existing backup and recovery
    software writes native backup jobs to virtual tapes stored on the Tape Gateway.
    Virtual tapes can be migrated into Amazon S3 and eventually archived into
    Amazon Glacier for the lowest cost. Data is accessed through your backup
    application and the backup catalog maintains complete visibility for all
    backup jobs and tapes.
* Tape Gateway interfaces with most common backup applications.
* Storage Gateway automatically buffers on-premises data and efficiently moves it
    into (and out of) cloud storage services. This reduces the time and cost of
    moving data between your site and the AWS Cloud. Optimizations such as
    multipart management, delta transfers, bandwidth throttling, and bandwidth
    scheduling are standard for all interfaces.
