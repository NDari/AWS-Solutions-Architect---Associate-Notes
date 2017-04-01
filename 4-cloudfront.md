### CloudFront

* Amazon edge locations are independent of regions and availability zones.
* **Distribution**: A Custom-made CDN composed of one or more edge locations.
* **Time To Live (TTL)**: The length of time an object is cached at an edge
    location. The default TTL for objects is 86400s, or 24 hours.
* **Origin**: The origin of the object that are distributed using CloudFront.
    This object can be in any of the AWS storage classes or VMs, or in a
    server that is not on AWS.
* Objects can be written directory to edge locations. Amazon will automatically
    replicate the objects back to the origin eventually.
* You can manually clear cached objects on CloudFront before their TTL is up.
    But this does cost money.
* You can have multiple origins in a single distribution.
* origins of a distribution can be a folder within a bucket.
* Each origin must have an ID, which is a way to separate different origins.
* You can restrict requests in a distribution so that they have to go through
    a bucket.
* When you allow PUT and POST to a distribution, the objects will go to an
    edge location, and will eventually be put into the origin's bucket.
* You can restrict access to CloudFront using signed URLs and Cookies.
* If you want to use a custom domain name for your distribution, you
    must provide an SSL certificate for that domain.
* You can whitelist or blacklist countries from accessing your distribution.
* You can invalidate an object in a distribution to remove it from all edge
    locations on which it was cached.
* You must disable a distribution first before you can delete it.
