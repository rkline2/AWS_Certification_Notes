## Types of Storage Services

### **Elastic Block Store (EBS) - Block:** 

*When you need a virtual hard drive attached to a VM*

* Data is split into evenly split blocks
* Directly accessed by the Operation System
* Supports only a single write volume 


### **AWS Elastic File Storage (EFS) - File:** 

*When you need a file-share where multiple users or VMs need to access the same drive*

* File is stored with data and metadata
* Multiple connections via a network share
* Supports multiple reads, writing locks the file. 


### **Amazon Simple Storage Service (S3) - Object:** 

*When you just want to upload files, and not have to worry about the underlying infrastructure. Not intended for high IOPs* 

* Object is stored with data, metadata, and Unique ID
* Scales with limited no file limit or storage limit
* Supports multiple reads and writes (no locks) 

----

## Introduction to S3

### **What is Object Storage (Object-based Storage)?**

Data storage architecture that manages data as objects, as opposed to other storage architectures:

* File systems which manage data as files and fire hierarchy, and
* Block storage which manages data as blocks within sectors and tracks. 

S3 provides you with **unlimited storage**.

* You don’t need to think about the underlying infrastructure
* The S3 Console provides an interface for you to upload and access your data

### **S3 Object**

Objects contain your data. They are like files.

Object may consist of:

* **Key** this is the name of the object
* **Value** the data itself made up of a sequence of bytes
* **Version ID** when versioning enabled, the version of object
* **Metadata** additional information attached to the object 

### **S3 Bucket**

* Buckets hold objects. Buckets can also have folders which in turn hold objects
* S3 is a universal namespace so bucket names must be unique (think like having a domain name)
* You can store an individual object from 0 Bytes to 5 Terabytes in size

----

## S3 Storage Classes

AWS offers a range of S3 storage classes that trade Retrieval Time, Accessibility and Durability for Cheaper Storage


**S3 Standard (default)**

    Fast! 99.99% Availability, 11 9’s Durability. Replicated across at least three AZs

**S3 Intelligent Tiering**

    Uses ML to analyze object usage and determine the appropriate storage class. Data is moved to the most cost-effective access tier, without any performance impact or added overhead.

**S3 Standard-IA (Infrequent Access)**

    Still Fast! Cheaper if you access files less than once a month. Additional retrieval fee is applied. 50% less than Standard (reduced availability)

**S3 One-Zone-IA**

    Still Fast! Objects only exist in one AZ. Availability (is 99.5%). but cheaper than Standard IA by 20% less
    (Reduce durability) Data could get destroyed. A retrieval fee is applied.

**S3 Glacier**

    For long-term cold storage. Retrieval of data can take minutes to hours but the off is very cheap storage

**S3 Glacier Deep Archive**

    The lowest cost storage class. Data retrieval time is 12 hours.

### Cheaper ↓

(S3 Outposts has its own storage class.)

----

## Storage Services:

Provide scalable cloud-based storage solutions for your workloads on AWS.

* **[S3 (Simple Storage Service)](https://aws.amazon.com/s3/?nc2=type_a)** - is an object storage service that offers industry-leading scalability, data availability, security, and performance. Think of it as a "hard drive in the cloud" with a lot of available space.

* **[S3 Glacier](https://docs.aws.amazon.com/amazonglacier/latest/dev/introduction.html)** - low cost storage for archiving and long-term backup Trade-off: You may have to wait several hours to access data stored here. Use case: for data that you must hold on to but are unlikely to look at often. Example: an enterprise company that must store records for many years under a litigation hold.

* **[EBS](https://aws.amazon.com/ebs/?nc2=type_a&ebs-whats-new.sort-by=item.additionalFields.postDateTime&ebs-whats-new.sort-order=desc)** - `Elastic Block Storage- is a persistent block storage service. It is a virtual hard drive in the cloud you attach to EC2 instances. You can choose different kinds of hard drives: SSD, IOPS SSD, Throughput HHD, Cold HHD​

* **[EFS](https://aws.amazon.com/efs/?nc2=type_a)** - Elastic File Storage- file storage mountable to multiple EC2 instances at the same time

* **[Storage Gateway](https://aws.amazon.com/storagegateway/?nc2=type_a&whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc)** - hybrid cloud storage with local caching. Expand your on-premises storage capacity into the cloud.

* **File Gateway** extends your local storage to AWS S3

* **Volume Gateway** caches your local drives to S3 so you have a continuous backup of local files in the cloud

* **Tape Gateway** stores files onto virtual tapes for backing up your files on very cost-effective long-term storage.

* **[AWS Snow Family](https://aws.amazon.com/snowball/)** are storage devices used to physically migrate large amounts of data to the cloud.

* **Snowball and Snowball Edge** are briefcase-size data storage devices. 50-80 Terabytes

* **[Snowball edge](https://aws.amazon.com/snow/)** - A version of Snowball for even larger sets of data - 100 TB

* **[Snowmobile](https://aws.amazon.com/snowmobile/)** is a cargo container filled with racks of storage and compute that is transported via semi-trailer tractor truck to transfer up to 100PB of data per trailer.

* **Snowcone** is a very small version of Snowball that can transfer 8TB of data.

