### Simple Storage Service (S3)

* **Object**: is a flat file, such as a text or PDF.
* S3 is a object based storage. It is not a block of space to which you can
    store your files. Therefore the objects can be stored anywhere at all, and
    not necessarily on the same disk, or even in the same region.
* Objects can range from 0 to 5TB in size.
* **Buckets**: Are essentially a folder in which you can save objects.
* Buckets are universally name-spaced, hence each bucket must have a unique
    name across all of Amazon's S3 buckets.
* All buckets have a unique url: https://s3-region-name.amazonaws.com/bucket-name
* **Read-after-write consistency**: A newly inserted data item or record will be
    immediately visible to all the clients. Please note that it is only
    applicable to new data. Updates and deletions are not considered in this
    model.
* **Eventual Consistency**: In this approach, the system informally ensures
    that, if no new updates are made to a particular piece of data,
    eventually all reads to that item will return the last updated value. The
    updated replicas send the update messages to all other replicas. In these
    states different replicas could return different values if queried, but
    eventually all the replicas get the update and will be consistent
* S3 is read-after-write consistent after PUT, and eventually consistent after
    UPDATE or DELETE.
* An S3 object consists of a *key* which is the name of the object, *value* which
    is the actual bytes of the object, *version ID*, and *metadata* about the
    object.
* **Access Control List (ACL)**: Contains a list of grants identifying the
    grantees and the permissions granted. When you create an object, the
    acl identifies the object owner as having full control over the object.
    You can retrieve an object ACL or replace it with updated list of grants.
* **Torrent**: It is used to return the torrent file associated with the specific
    object. To retrieve a torrent file, you specify the torrent in your GET
    request. Amazon S3 creates a torrent file and returns it.
* **Subresources**: Subresources are subordinates to objects, thus they do not
    exist on their own, they are always associated with some other entity,
    such as an object or a bucket. There are two types of subresources: ACL and
    Torrent.
* S3 guarantees 99.999999999% (11 nines) durability for S3 objects. This is
    achieved in part by replicating objects enough so that they can withstand
    two datacenters getting destroyed at the same time.
* **Storage class**: S3 has mutltiple services for storing your objects with
    different advantages, drawbacks, and costs.
* **S3 Infrequent Access (S3-IA)**: This storage class is used for objects
    which are not frequently accessed, but have to be available quickly when
    needed.
* **S3 Reduced Redundency Storage (S3-RRS)**: In this storage class, the objects
    are replicated enough to withstand only one datacenter being destroyed. Thus
    the durability guarentee for these objects is only 99.99%. This may be used
    for objects which can be regenerated easily, such as thumbnails.
* **Glacier**: The cheapest storage class. The drawback is that you must wait
    3-5 hours before getting the data back when you ask for it inside Glacier.
* **Lifecycle Management**: Lifecycle configuration enables you to specify the
    lifecycle management of objects in a bucket. The configuration is a set of
    one or more rules, where each rule defines an action for Amazon S3 to
    apply to a group of objects. These actions can be classified as follows:
    *transition actions* in which you define when objects transition to
    another storage class, and *Expiration actions* in which you specify
    when the objects expire. Then Amazon S3 deletes the expired objects
    on your behalf. You can also set it to delete unfinished muti-part
    uploads.
* **Transfer Acceleration**: Allows for fast and secure file transfer between
    end users and S3 buckets using edge locations. Therefore the users do not
    interact with the S3 buckets directly.
* Amazon charges for the following usages of S3: storage, requests, tagging,
    transfer around in S3 (not uploading into S3), and transfer acceleration.
* While objects are between 0-5TB in size, a single PUT cannot exceed 5GB. For
    Objects larger than that use *multipart uploading services*.
* To delete a large number of objects, use *multi-object deletes* which allows
    for many object keys to be put into a single request. This is a free service.
* Newly created buckets are set to private by default. If buckets or items in the
    bucket are set to public then they can be accessed through their URLs.
* **Encrypted at Rest**: The data is encrypted while it is stored somewhere.
* **Encrypted at Transit**: The data is encrypted while it is being moved from
    some source to some destination. This is usally done with TLS/SSL which are
    a part of HTTPS.
* Permissions (read/write) for objects is granted during the creation of the bucket.
    This allows users to add to the bucket or view the list of items in a bucket.
* Versioning can be added to a bucket at creation. You cannot remove versioning from
    a bucket. You have to disable the bucket, and copy the items to a non-versioned
    bucket.
* Objects in a bucket have permissions of their own, and do not care about the
    permissions of the bucket they are in.
* S3 stores whole files when versioning, not just the diffs.
* Deleting a file in a versioned bucket does not actually delete the file, rather
    it just gives it a deleted marker. All the previous version of the file still
    exist and can be restored by simply deleting the delete marker.
* You can set multi-factor authorization on users when they attempt to delete
    objects in a bucket. This can be set on individual items or the whole bucket.
* Deleted files do not show up in the file list by default. You have to enable
    showing to see them and restore them.
* Glacier requires a minimum of 90 days of storage before an item can be deleted
    or moved.
