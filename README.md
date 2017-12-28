![](https://github.com/inbravo/aws-feature-set/blob/master/mind-maps/aws-all-services/aws-core-dimensions.jpg)

# Core AWS Dimensions

- **Security & Identity**
	-	[**IAM**](https://github.com/inbravo/aws-feature-set#-iam--identity--access-management) : How you setup and assign users / groups etc
	- 	**Inspector** : Agent which inspects your VMs and does security reporting
	- 	**Certificate Manager** : Free SSL certs for your domain names
	- 	**Directory Service** :  Run MS active directory service on cloud
	- 	**WAF** : Web Application Firewall
	- 	**Artifacts** : All documentation under compliance and reports
- **Compute** 
	-	[**EC2**](https://github.com/inbravo/aws-feature-set#-ec2--elastic-compute-cloud) : Elastic Compute Cloud
	-	**ECS** : EC2 Container Services
	-	[**EBS**](https://github.com/inbravo/aws-feature-set#-ebs--elastic-block-storage) : Elastic Block Storage
	-	**Elastic Beanstalk** : Elastic Bean stalk will provision all infrastructure required
	-	**Lambda** : Alexa, Echo devices rely on Lambda
	- 	**Lightsail** : Out of the box cloud e.g. WordPress, Drupal
- **Storage** 
	-	[**S3**](https://github.com/inbravo/aws-feature-set#-s3--simple-storage-service) : Object Store
	-	[**Glacier**](https://github.com/inbravo/aws-feature-set#-glacier) : Archive files from S3 into Glacier 
	-	**EFS** : Elastic File Service. It can be attached to multiple EC2 instances
	-	[**Storage Gateway**](https://github.com/inbravo/aws-feature-set#-storage-gateway) : Communicates between your data center and S3 storage
- **Networking & Content Delivery**
	-	**VPC** : You can have multiple VPCs per region
	-	**Route 53** : Amazon’s DNS Service
	-	[**CloudFront**](https://github.com/inbravo/aws-feature-set#-cloudfront) : Content delivery network. Edge locations cache assets
	-	**Direct Connect** : Connect your physical DCs to AWS using dedicated telephone lines
- **Database Services**
	-	[**RDS**](https://github.com/inbravo/aws-feature-set#-rds--relational-database-service) : Relational Data Services : MySQL, PostgreSQL, SQL Server, MariaDB, Aurora
	-	[**DynamoDB**](https://github.com/inbravo/aws-feature-set#-dynamodb) : Non relational DB
	-	[**Redshift**](https://github.com/inbravo/aws-feature-set#-redshift) : Data warehousing system 
	-	[**ElastiCache**](https://github.com/inbravo/aws-feature-set#-elasticache) : Cloud in-memory DB
- **Migration**
	-	[**DMS**](https://github.com/inbravo/aws-feature-set#-dms--database-migration-service) : Database migration services : Migrate existing DB to Cloud
	-	**SMS** : Server migration services : Migrate existing VM on premise to the Cloud
	-	[**Snowball**](https://github.com/inbravo/aws-feature-set#-snowball) : Transfer Data : Store all your data from enterprise into Snowball and then ship to AWS
- **Analytics**
	-	**Athena** : Allow SQL queries on S3. Run queries on csv files in S3 buckets
	-	**EMR** : Elastic Map Reduce : Process large amounts of data. Based on Hadoop, Apache Spark etc
	-	**Cloud Search** : Managed services provided by AWS
	-	**Elastic Search** : Search service which uses the Elastic product
	-	**Kinesis** : Streaming and analysis real time data. Used for collating large amounts of data streamed from multiple sources
	-	**Data Pipeline** : Move data from one place to another. e.g. S3 into DynamoDB and vice versa
	-	**Quick Sight** : BA tools for rich visualizations and dashboards
- **Management Tools**
	-	**Cloud Watch** : Monitor performance of AWS environment 
	-	**Cloud Formation** : Infrastructure into Code
	-	**Cloud Trail** : Audit usage of AWS Resources
	-	**OpsWorks** : Automate deployments using Chef
	-	**Config Manager** : Monitors environments and **provides alerts for events**. e.g. someone creates a security group which is against policy
	-	**Trusted Advisor** : Automated tips for cost & performance optimization, security tips, architecture and design
- **Application Services**
	-	**API Gateway** : Create secure api service
	-	**Elastic Transcoder** : Media transcoding in cloud
	-	**SNS** : Simple notification service
	-	**SES** : Simple email service
	-	**SWF** : Simple workflow service
	-	**SQS** : Simple message service
	-	**Step functions** : Visualize Application internals : Which micro services is your application using
	-	**SWF** : Simple Workflow Service. Used in Amazon fulfillment center
	-	**AppStream** : Stream desktop services via browser
- **Mobile Service & IoT**
	-	**Mobile Hub** : For mobile Applications
	-	**Cognito** : Social identity providers for Gmail, Facebook OAuth 
	-	**Device Farm** : Testing your apps across multitude of devices
	-	**Mobile Analytics** : Collect application usage data in a cost-effective way
	-	**Pinpoint** : Collects metrics to help understand the impact of customer communications
	-	**IoT Core** 
	-	**Amazon FreeRTOS**  : An operating system for microcontrollers
	-	**Greengrass** : Lets you run local compute, messaging & data caching
	-	**IoT 1-Click**
	-	**IoT Analytics** : Fully-managed service that makes it easy to run sophisticated analytics
	-	**IoT Button**
	-	**IoT Device Defender**
	-	**IoT Device Management**
- **Desktop and App Streaming**
	-	**WorkSpaces** : Desktop on cloud
	-	**App Stream** : Stream desktop apps to users
	-	**Work Docs** : Store work documents on cloud
	-	**Work Mail** : Exchange on AWS
- **Artificial Intelligence**
	-	**Alexa** (which uses Lambda) + Lex. Echo isn’t required anymore to use Alexa
	-	**Polly** : Text to Speech
	-	**Machine Learning** : AWS will predict outcomes for future decisions based on demographics etc
	-	**Rekognition** : Image recognition, Facial recognition based on Databases
	  
## Global Infrastructure
- A Region is geographical area consisting of 2 or more availability zones.
- Availability zone is logical data center
- Edge Locations are CDN End Points for CloudFront. Many more edge locations exist than regions

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/iam.png) IAM : [Identity & Access Management](https://aws.amazon.com/iam)

### IAM Resources
- Users 
- Groups 
- Roles 
- Policies (JSON doc which defines one or more permissions)
- Identity Provider (Single Sign On)
	
### IAM Purpose
- Configure who uses AWS and their level of access to the AWS Console
- Centralized control over AWS Account
- Share access for AWS Account
- Granular permissions (grant system privileges) for users / services
- Identity Federation : Facebook, LinkedIn and Active Directory
- Multi-factor authentication (**MFA**)
	- Virtual device
	- Hardware device
- Temporary access to users and services
- Setup password rotation policy
- Integration with other AWS services
- Supports Payment Card Industry Data Security Standard (**PCI-DSS**) compliance

### IAM Features
- IAM is global and its not region specific
- Root account is the email address you use to sign up for AWS
- AWS recommends very limited usage of root account
- Setup Multi Factor Authentication (MFA) on root account
- You can attach permissions to individual users and groups
- Secret access key can be retrieved only once during user creation. In case you lose it then you can re-generate it
- IAM Password policy can be set to access the admin console
- New users have no permissions when first created. Everything has to be explicitly added
- Power User Access allows Access to all AWS services except the management of groups and users within IAM
  
### Manage AWS resources via
- AWS Management console : Using username and password
- Rest API : Using Access Key ID and Secret Access Key
- AWS Command Line Interface (**CLI**) : Using Access Key ID and Secret Access Key
- AWS Software Development Kit (**SDK**) : Using Access Key ID and Secret Access Key

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/ec2.png) EC2 : [Elastic Compute Cloud](https://aws.amazon.com/ec2)

### EC2 Pricing
- On demand. Pay per hour of usage
- Applications with short term, spiky usage patterns or unpredictable workloads that cannot be interrupted
- New apps on AWS
- Reserved pricing
- Reserve capacity over significant period of time. Significant discount.
- Applications with steady or predictable usage over a period of time. Reserved capacity required.
- Further discount if upfront payment
- Spot pricing : When bid price is higher than Spot price, then you can provision it. When it goes lower, instance is terminated
- **If AWS terminates instance, you are not charged for partial hour. If you terminate, you will be charged for the hour**
- Applications that are feasible only at very low compute prices. e.g. pharma simulations
- Applications with urgent computing capacity
- Dedicated physical machines. Pay by hour
- Massive discount for reserved instances over a long period of time – upto 70% for 3 years
- Useful for regulatory requirements
- Certain licensing agreements prevent usage on virtual machine / multi-tenancy deployments
- EC2 Key Pairs are region specific
  
### EC2 Instance types
|Sr. No| Family| Specialty| Use Case| Type|
| ------------- |:-------------:| -----:|-----:|-----:|
|1 |D2 |Dense Storage | File Servers / DWH / Hadoop | Storage Optimized|
|2| R4. R3| Memory Optimized|Memory Intensive / DBs|Memory Optimized|
|3|M4. M3|General Purpose|Application Servers|General Purpose|
|4|C4, C3|Compute Optimized|CPU Intensive Apps, DBs|Compute O|
|5|G2|Graphics Intensive|Video Encoding / 3D Application Streaming||
|6|I2|High speed storage (IOPS)|NoSQL DBs, DWH||
|7|F1|Field Programmable Gate Array|Hardware acceleration of Code||
|8|T2|Lowest Cost, General Purpose|Web Servers/ Small DBs| General Purpose|
|9|P2|Graphics / General Purpose GPU[Parallel Processing]|Machine Learning / Bit Coin Mining.| |
|10|X1|Memory Optimized|SAP HANA / Apache Spark| - |

### EC2 Instance type Acronym (**DIRT MCG FPX**)  	
- **D** : Density
- **I** : IOPS
- **R** : RAM 
- **T** : Cheap T2
- **M** : Main Choice for Apps
- **C** : Compute
- **G** : Graphics
- **F** : FPGA
- **P** : Graphics, Pics, Parallel Processing
- **X** : Extreme Memory

### EC2 Security Groups
- A security group is a virtual firewall.
- First line of defense. Network ACLs are second line.
- Single instance can have multiple security groups. As each security group only "allows" inbound traffic, there will never be a conflict on security group rules.
- Security group changes are applied immediately.
- Security groups are "stateful". Rules added as inbound rules – automatic outbound rules are added. Response back on the same channel. NACLs are stateless.
- All inbound traffic is blocked by default. You have to allow specific inbound rules for protocols
- All outbound traffic is allowed by default.
- Only allow rules, no deny rules exist. Use NACLs to deny specific IPs
- Any number of EC2 instances in a security group.
- EC2 instances in the default security group can communicate with each other.
- Multiple security groups can be attached to an instance

### EC2 Status Checks

#### System Status Checks
Monitor the AWS systems required to use your instance to ensure they are working properly. These checks detect problems with your instance that require AWS involvement to repair. When a system status check fails, you can choose to wait for AWS to fix the issue, or you can resolve it yourself (for example, by stopping and starting an instance, or by terminating and replacing an instance).
The following are examples of problems that can cause system status checks to fail:
- Loss of network connectivity
- Loss of system power
- Software issues on the physical host
- Hardware issues on the physical host that impact network reachability
  
#### Instance Status Checks
Monitor the software and network configuration of your individual instance. These checks detect problems that require your involvement to repair. When an instance status check fails, typically you will need to address the problem yourself (for example, by rebooting the instance or by making instance configuration changes).
The following are examples of problems that can cause instance status checks to fail:
- Failed system status checks
- Incorrect networking or startup configuration
- Exhausted memory
- Corrupted file system
- Incompatible kernel

### AWS CLI Usage
- Users can login with Access Key ID and Secret Access Key. If anything is compromised, you can regenerate the secret access key
- Also you can delete the user and recreate
  
### EC2 IAM Roles
- Avoid using user credentials on servers
- IAM roles can be assigned/replaced to existing EC2 instances using AWS CLI. Not through the console
- A trick is to assign policies to the existing role. This will avoid the need to create new instances
- Role assigned to instance is stuck to the lifetime of the instance – until you delete the role. Easier to modify existing role by adding / removing policies
- Roles are universal. Applicable to all regions
  
### Bootstrap scripts
- Scripts can be passed on to the EC2 instance at first boot time as part of user-data
  
### EC2 Instance Meta-Data
- curl [http://169.254.169.254/latest/meta-data/](http://169.254.169.254/latest/meta-data/)
- Instance information is available in Meta-Data. Not in User-Data
  
### EC2 Auto Scaling
- Before you can create Auto scaling group you need to create a launch configuration
- Launch Configuration : Select AMI, Instance Type, Bootstrap script
- No actual instances are created just with launch configuration
- Auto scaling group – Set minimum size, spread it over subnets (AZs)- select all available AZs
- Run health checks from ELB
- Configure Auto scaling policy, based on Alarm take action – trigger a new instance creation when CPU Utilization is greater than 90% for 5 minutes. 
- You can also delete instance based on alarms
- When Auto scaling group is launched it creates the instances based on definition.
  
### EC2 Placement groups
- Logical grouping of instances within a single AZ
- Instances can participate in low latency, 10 GBPs network

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/ebs.png) EBS : [Elastic Block Storage](https://aws.amazon.com/ebs)

### EBS Features
- Block based storage
- You can install OS, Database on it, unlike S3
- Placed in specific AZ. Automatically replicated within the AZ to protect from failure.
- You cannot mount 1 EBS volume to multiple EC2 Instances. Use EFS instead
- EBS Root Volumes can be encrypted on custom AMIs only. Not on the default available AMIs. To encrypt root volumes, create a new AMI and encrypt root volume. You can also encrypt using 3rd party software like Bit Locker
- EC2 – 1 subnet equals 1 Availability Zone.
- Default VPC & Security group is created in when you create your account.
- Default CloudWatch monitoring – every 5 mins. Can enabled advanced monitoring to check at interval of each minute.
- Volume : Virtual Hard Disk
- Tag everything on AWS
- Default Linux EC2 username is ec2-user
- Default Windows EC2 username is Administrator
- Termination protection is turned off by default. You need to turn it on
- When instance is terminated, root volume is deleted. You can turn if off
- System Status Check – Overall health of hosting infrastructure. If they arise, Terminate instance and recreate
- Instance Status Check – Health of instance. If they arise, reboot the instance

### EBS volume types
- SSD Drives
	- (root volume) General Purpose SSD – up to 10,000 IOPS. 3 IOPS per GB. Balances price and performance. You can burst upto 3000 IOPS for 1GB
	- (root volume) Provisioned SSD – when you need more than 10,000 IOPS. Large RDBMS DBs and NoSQL DBs. Up to 20000 IOPS now
- Magnetic Drives
	- HDD (root volume) : Magnetic (Standard) – *Cheapest bootable EBS volume type*. Used for apps where data is less frequently accessed and low cost is important
	- HDD Throughput Optimized : ST1 – Required for data written in sequence. Big Data, DWH, Log processing. Cannot be used as boot volumes
	- HDD : Cold : SC1 – Data that isn’t frequently accessed. e.g. File Server. Cannot be used as boot volume

### Volumes and Snapshots
- Volumes are virtual hard disks
- You can attach volume to EC2 instance belonging to same AZ
- To Detach a volume from EC2 instance, you have to umount it first
- Snapshots are point in time copies of volumes – stored in S3. Taking first snapshot takes a while
- Subsequent snapshots will only store the delta in S3. Only changed blocks are stored in S3
- You can create volumes from Snapshots. During this you can also change Volume Storage Type
- Volume is just block data. You need to format it create specific file system e.g. ext4
- Root Volume is one where OS is installed / booted. It is not encrypted by default on AWS AMIs
  
### RAID, Volumes & Snapshots
- RAID 0 – Striped, No Redundancy , Good Performance – No Backup/Failover
- RAID 1 – mirrored, Redundancy
- RAID 5 – Good for reads, bad for writes. AWS doesn’t recommend using RAID 5 on EBS
- RAID 10 – Raid 0 + Raid 1
- Use RAID Arrays when a single volume IOPs are not sufficient for your need e.g. Database. Then you create RAID Array to meet IOPs requirements
- To take snapshot of RAID Array
	- Stop the application from writing to cache and  flush all cache to Disk
	- Freeze the file system
	- Umount the RAID Array
	- Shutdown the EC2 instance
- Snapshots of encrypted volumes are encrypted automatically.
- You can copy snapshot to another region while encrypting it.
- Create Image from snapshot.
- The EC2 instance thus created will have root volume encrypted.
- You can’t share encrypted snapshots as the encryption key is tied to your account

## EBS backed v/s Instance store
- You can reboot or terminate instance store backed EC2 VMs
- You can start , stop , reboot or terminate EBS backed EC2 VMs
- EC2 instance on instance store is lost if host hypervisor fails. Not so with EBS backed instances.
- EBS volumes can be attached / detached to EC2 instances. One at a time
- EBS backed AMI is from EBS snapshot
- Instance store back volume is from template in S3. Hence slower to provision
- You will not lose data is you reboot for both.
- With EBS, you can ask AWS not to delete the volume upon instance termination

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/s3.png) S3 : [Simple Storage Service](https://aws.amazon.com/s3)

### S3 Storage Types
- S3-Standard : Durability of Eleven Nine (99.999999999%) and availability of Four Nine (99.99%)
- S3-IA (Infrequently Accessed) : Durability of Eleven Nine (99.999999999%) and availability of Three Nine (99.9%)
- S3-RRS (Reduced Redundancy Storage) : Durability and availability of Four Nine (99.99%)

### S3 Buckets
- S3 Namespace is global. Region independent
- A bucket name in any region should only contain lower case characters. It has to be DNS Compliant
- Object versioning - Different versions of the same object in a bucket.
- Only Static website can be hosted. Auto scaling, Load Balancing etc. all managed automatically.
- You can tag buckets (or any AWS resoruce) to track costs. Tags consist of keys and (optional) value pairs.
- Lifecycle management of objects can be set. e.g. move to Glacier after 30 days
- Every bucket created, object uploaded is private by default.
- Object Permissions – Access to Object ACLs
- Prefix in bucket is a folder in the bucket.
- Minimum file size that I can store on S3 bucket is 0 byte.
- Max 100 S3 buckets per account by default.
- S3 objects can range from **0 bytes** to **5 terabytes**
- The largest object that can be uploaded in a single PUT is **5 gigabytes**
- For objects larger than **100 megabytes**, use  Multipart Upload capability

### S3 Security
- By default all newly created buckets are **private**
- Control Access to buckets using
  - Bucket Policies : Bucket wide
  - Access Control Lists (**ACL**) : Up to individual objects
- S3 buckets can log all access requests to another S3 bucket even another AWS account
  
### S3 Encryption
- In Transit : Secured using SSL/TLS
- Data at rest : 
- Server Side
	- S3 Managed Keys – SSE – S3
	- AWS KMS Managed Keys – SSE – KMS – Envelop Key. Provides audit trail
	- SSE using customer provided keys. Key Management is responsibility of user. SSE-C
- Client Side
	- Encrypt data at client side and then upload to S3

### S3 Versioning
- Once versioning is turned on it cannot be removed. It can only be suspended. To remove versioning, you have to create a new bucket and transfer all files from old to new
- For newer version of an object, you still have to set permissions to allow access. It is disabled by default even if previous version is public
- All versions of the file add up to the storage. Hence for larger objects, ensure that there is some lifecycle versioning in place
- Version deleted cannot be restored
- Object deleted can be restored – Delete the Delete marker
- Versioning is a good backup tool.
- For versioning. MFA can be setup for Delete capability for object / bucket – Complicated setup.

### S3 Cross Region Replication
- To allow for cross region replication, the both source and target buckets must have versioning enabled.
- When cross region replication is enabled, all existing objects in the bucket are not copied over to replica site. Only Updates to existing objects and newer objects are replicated over. All previous versions of the updated objects are replicated.
- Permissions are also replicated from one bucket to another.
- Transitive replications do not work. E.g. if you setup bucket C to replicate content from bucket B which replicates content from bucket A – Changes made to bucket A will not get propagated to C. You will need to manually upload content to bucket B to trigger replication to C.
- Delete markers are replicated.
- If you delete source replication bucket objects, they are deleted from replica target bucket too. When you delete a Delete marker or version from source, that action is not replicated

## S3 Transfer Acceleration
It utilizes the CloudFront Edge Network to accelerate uploads to S3. Instead of uploading directly to S3, you can use a distinct URL to upload directly to an edge location which will then transfer to S3 using Amazon’s backbone network.
The farther you are from S3 bucket region the higher is the improvement you can observe using S3 Transfer Acceleration. High cost for usage than standard S3 transfer rates.
  
### Storage Object Lifecycle Management
- Objects stored in Glacier incur minimum 90 day storage cost
- Lifecycle management can be used in conjunction with versioning
- Objects can be transitioned to S3-IA after 30 days and to Glacier class storage - 30 days IA
- You can also permanently delete objects

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/glacier.png) [Glacier](https://aws.amazon.com/glacier)
- For archival only. Takes 3 - 5 hours to restore files. Durability of 99.999999999%
  
## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/storagegateway.png) [Storage Gateway](https://aws.amazon.com/storagegateway) 
- It is a service which connects an on-premises software appliance (virtual) with cloud based storage to provide seamless and secure connectivity between the two. Either via internet or Direct connect
- It can also provide connectivity from EC2 instance in VPC to S3 via Storage Gateway in same VPC
- The virtual appliance will asynchronously replicate information up to S3 or Glacier
- Can be downloaded as a VM  VMware ESXi / Hyper-V.
- 4 types of Storage Gateway
	- [Brand New] File Gateway (NFS) : Store files in S3  Word, Pictures, PDFs
    - Files are stored as objects in S3 buckets and accessed over NFS mount point
  - File attributes as stored as S3 object metadata
  - Once transferred to S3, standard S3 features apply to all files
 2.Volumes Gateway (iSCSI) – uses block based storage – virtual hard disk, operating system.
  - Stored Volumes – Store entire data set copy on-prem. Data async backed up to AWS S3.
  - Cached Volumes – Stored only recently accessed data on-prem. Rest on AWS S3
  Volume gateway interface presents applications with disk volumes using iSCSI protocol. They take virtual hard disks on premise and back them up to virtual hard disks on AWS. Data written to these volumes can be asynchronously backed up as point in time snapshots of volumes and stored in cloud as EBS snapshots.
 3.Gateway Virtual Tape Library (VTL) – Backup and Archiving solution. Create tapes and send to S3. You can use existing backup applications like NetBackup, Backup Exec, and Veam etc.
 
## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/snowball.png) [Snowball](https://aws.amazon.com/snowball) 
- Next version of Import / Export Gateway
- You could accelerate moving large amounts of data into and out of AWS using portable storage devices for transport
- Ship the storage device : no need to transfer over the internet. Problem arose with different types of disks
  
### Snowball Standard
- Bigger than briefcase sized storage devices
- Petabyte scale data transport solution used to transfer data in/out of AWS
- Cost is 1/5th as compared to transfer via high speed internet
- 80TB snowball available
- Multiple layers of security to protect data. Tamper resistant enclosure, 256-bit encryption
- Once data is transferred, AWS performs software erasure of Snowball appliance

### Snowball Edge
- 100 TB data transfer device which has onboard storage and compute capabilities.
- Move large amounts of data in and out of AWS, as a temporary storage tier for large local datasets.
- You can run Lambda functions.
- Devices connect to existing applications and infrastructure using standard storage interfaces.
- Snowball Edges can be clustered together to process your data on premise

### Snowmobile
- Massive 45 foot long ruggedized shipping container, pulled by a truck.
- Petabyte or Exabyte of data that has to be transferred to AWS. 100 PB per snowmobile.
- You can use it for data center migration.
- Snowball import/export to/from S3: If using Glacier first need to import into S3 and then into Snowball

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/cloudfront.png) [CloudFront](https://aws.amazon.com/cloudfront) 

### Important terms
- CDN : Collection of distributed servers where the content is served to users based on the user’s location and the location of content origin.
- Edge location : location where content will be cached. Different from AWS Region / AZ
- Origin : Can be S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53
- Distribution : Name given to CDN collection which consists of Edge locations
- Web Distribution : Typically used for websites & web content only
- RTMP : Used for Media Streaming. Adobe Flash media server’s protocol – video streaming
- First request is slow as it comes from source origin. Subsequent requests improve speed as they are cached in nearest edge location and routed there until TTL expires
- CloudFront also works with non AWS origin which can be on premise as well
- Edge locations are for read and write as well. Objects PUT on edge location are sent to origin
- Objects are cached for life of TTL. TTL can be set for 0 seconds to 365 days. Default TTL is 24 hours. If objects change more frequently update the TTL
- You can clear cached objects, with charges
- Origin domain name : either S3 bucket, ELB or on premise domain
  
### CloudFront security
- You can force them to use CDN URL instead of S3 DNS
- To restrict bucket access you need to create origin access identity. And allow this user read permission S3 bucket content –
- Set video protocol policy – redirect http to https, http or https
- Allows various HTTP methods – GET, PUT, POST, PATCH, DELETE, and HEAD.
- Restrict viewer access for S3 and CDN using pre-Signed URLs or Signed cookies. E.g. You can view video only using that URL
- Using Web Application Firewalls to prevent SQL injection, CSS attacks
- For https access, you can either use default CloudFront certificate or own certificate can be imported via ACM.
- Provisioning / Updating CloudFront distribution takes up to 15-20 minutes.
- Geo-restriction can be setup. Either whitelist or blacklist – countries from where content can be accessed.
- Invalidating removes objects from CloudFront. It can be forced to remove from Cache – obviously costs
- You can force users to get content via CloudFront after removing read access to S3 bucket
- You can also upload content to CloudFront

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/rds.png) RDS : [Relational Database Service](https://aws.amazon.com/rds)  

### Supported SQL DB
- MS-SQL Server
- Oracle
- MySQL
- PostgreSQL
- Aurora
- MariaDB
  
### Supported NoSQL DB
- CouchDB
- MongoDB
- DynamoDB
- NoSQL storage : Collection = Table, Document = Row, Keys-Value Pairs = Fields

### RDS OLTP vs OLAP
- OLTP
	- Pulls out specific / narrow record set
- OLAP 
	- Pulls in large number of records
	- It used different architecture and infrastructure layer
	- Differ in terms of queries run on top of data
	- OLAP is more about aggregation

### RDS Backups
- Automated Backups. Full daily snapshot & will also store transaction logs
- Enabled by default. Stored in S3. Free backup storage in S3 upto the RDS Instance size
- You can define backup window. Choose wisely
- Backups are deleted when the RDS Instance is deleted

### RDS Snapshots
- Done manually. They are stored even after you delete the instance.
- You can copy snapshots across regions.
- You can publish the snapshot to make it publically available.
- Restoring Backups/ Snapshots – The restored version will be a new RDS instance with new end point.
- You can check the instance size to restore
- You cannot restore to existing instance
  
### RDS Encryption
- Encryption at rest is supported for MySQL, SQL Server, Oracle and PostgreSQL & MariaDB
- Managed by AWS KMS.
- Cannot encrypt an already present instance. To encrypt, create new instance with encryption enabled and then migrate your data to it
  
### RDS Multi-AZ Deployment
- A standby copy is created in another AZ. AWS handles replication and auto-failover
- AWS can automatically failover RDS instance to another instance.
- In case of failover, No need to change connection string.
- This can be used for DR purpose only. This option has to be selected at instance creation time. This option is not useful for improving performance / scaling.
 
### RDS Read Replica Databases
- Read-replica – async data transfer to another RDS instance. You can actually read from these instances, unlike Multi-AZ deployments. You can also have read replicas of read-replicas up to 5 copies. (Watch out as async causes latency)-
- Read-replicas can be used for Dev/Test environments, run certain workloads only against them and not against direct production deployment – Intensive workloads.
- *MySQL , MariaDB, PostgreSQL only for read-replicas , no Oracle & SQL Server*
- You cannot have read-replicas that have multi-AZ. However, you can create read replicas of Multi AZ source databases.
- Read replicas can be of a different size than source DB.
- Each read-replica will have its own DNS end point
- Automatic backups must be turned on in order to deploy a read replica
- Read Replicas can be promoted to be their own databases. This breaks replication. E.g. Dev/Test can be connected to the replica by first promoting it as DB itself.
- Read Replicas can be done in a second region for MySQL and MariaDB – no PostgreSQL.
- Application re-architecture is required to make use of Read replicas
- Read replicas are not used for DR. they are used for performance scaling only## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/dms.png) DMS : [Database Migration Service](https://aws.amazon.com/dms)

## DMS Features
- Migrate production database to AWS
- AWS manages all complexities of migration process
- Source database remains fully operational
- Can also be used for continuous data replication with high availability
- Both homogenous (Oracle to Oracle) as well as heterogeneous migrations are supported (Oracle to Aurora or Microsoft SQL)
	- **AWS Schema migration tool makes heterogeneous database**  
	- Any code that cannot be automatically converted is clearly marked so that it can be manually converted
	- Migrations : easy by automatically converting the source database schema and a majority of the custom code
		- Views
		- Stored procedures
		- Functions

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/dynamodb.png) [DynamoDB](https://aws.amazon.com/dynamodb)

### DynamoDB Features
- Fast and flexible NoSQL database
- Consistent, single digit millisecond latency.
- Fully managed DB – supports both document based & Key-value data models.
- Great fit for mobile, IoT, web, gaming etc. applications.
- Stored on SSDs
- Stored on 3 geographically distinct DCs (not AZs). Built in redundancy
- Consistency

1. Eventual consistent reads - Consistency reached up to 1 second (default)
2. Strongly Consistent reads - Consistency reached after writes to all copies are completed. <1 second
Select type based on application needs
- Pricing – Write Capacity Units and Read Capacity Units ($/hr.). Also Storage cost per month. You provision capacity in units/second. It can scale on the fly. Provisioned capacity.
- Dynamo DB – Expensive for Writes. Cheap for Reads. Important point v/s RDS.
- You can dynamically add columns – without the need to update other rows with the column data. As this is no RDBMS.
- Reserved capacity is available for DynamoDB as well

### RDS v/s DynamoDB
- Use DynamoDB for Push button scaling. With RDS – to scale horizontally a new instance has to be created.
- DynamoDB is cheap for writes and expensive for reads.
- Observe workload characteristics and decide
- Use RDS if data requires joins and relationships.
- In RDBMS database structure cannot be dynamically altered. With DynamoDB you can

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/elasticache.png) [ElastiCache](https://aws.amazon.com/elasticache)  
- In memory cache in cloud
- Memcached
- Redis

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/redshift.png) [Redshift](https://aws.amazon.com/redshift)
Petabyte scale DW solution in cloud.  Used for OLAP – sum of various columns and joining the data.

### Configurations
- Single Node – 160 GB. Used by Small and Medium Size businesses.
- Multi-Node – Leader Node (handles all incoming connections & receives queries) & compute Node (store data and perform queries and computations – up to 128 Compute Nodes)
### Performance
- Redshift is 10 times faster than usual OLAP systems.
- It uses Columnar Data Store.  Columnar data is stored sequentially on storage system. Hence low I/O required – improving performance.
- Advanced Compression (easier to do it via Columns instead of via Rows – which have different data types). Columns have similar type of data. Doesn’t use indexes and views – hence less storage required.
- Based on data, appropriate data compression scheme is used.
- Allows for massive parallel processing
### Pricing  
- Based on Compute Node hours (compute node only – no leader node).
- Backup and Data Transfer (only within VPC)
### Security
- Transit encrypted via SSL,
- At rest using AES-256 encryption
- Can use your own HSM or default AWSK Key management
  
### Availability
Not Multi-AZs. Can restore snapshots
Exam Tips – Database warehousing service, cheap, faster. Best seller AWS Service. Speed achieved due to columnar storage. And Data stored sequentially on disk – hence faster.

## ElastiCache
- Easy to deploy, operate and scale an in-memory cache in the cloud
- Improve performance by avoiding repeated calls to DB
- Improve latency and throughput for read-heavy applications
- Can be used for compute intensive data
### Memcached
- All Memcached tooling can be easily ported over
### Redis
- Supports Master / Slave replication and multi-AZ deployment to get redundancy.
Exam Tips
- ElastiCache is used if DB is primarily read-heavy and not frequently changing
- Use Redshift – if application is slow due to constant OLAP transactions on top of OLTP focused DB.
## Aurora
- Bespoke Database Engine.
- It is MySQL compatible.
- However you can’t download and install on your workstation.
### Performance
5 times better performance than MySQL. At a fraction of cost as compared to Oracle.
### Scaling
- Outset 10 Gb Storage, auto increment of storage
- No Push button scaling – unlike DynamoDB
### Fault Tolerance
- Maintains 2 copies of your data in at least 3 availability zones. This is for the Data only not for the instances that runs the Database.
- 2 copies lost – no impact on write availability.
- 3 copies lost – no impact on read availability.
- Storage is self-healing.
### Replicas
- MySQL Read Replica can be created from the Aurora source DB.(up to 5 of them)
- Aurora Replicas – up to 15 of them. If leader crashes, the replica with the highest tiers becomes the leader. While creating replicas, remember to assign different tier levels.
- Cluster Endpoint vs Individual Endpoint
No Free Tier usage available. Also available only in select regions. Takes slightly longer to provision
## Exam Tips
- Why you can’t connect to DB Server from DMZ. Check the security group – if it is removed or added
- Have separate groups for EC2 Instance and RDS Instance.
- Multi-AZ for Disaster Recovery only. Not for performance improvement. For performance improvement use, multiple read-replicas
- Dynamo DB v/s RDS
If you want push button scaling, without any downtown, you will always want to use DynamoDB.
With RDS scaling is not so easy, you have to use a bigger instance or add read replicas (manual process).
- If you are using Amazon RDS Provisioned IOPS storage with a MySQL or Oracle database engine, what is the maximum size RDS volume you can have by default? – **6TB**
- What data transfer charge is incurred when replicating data from your primary RDS instance to your secondary RDS instance? - **There is no charge associated with this action**.
- When you have deployed an RDS database into multiple availability zones, can you use the secondary database as an independent read node? – **No**
- RDS automatically creates RDS Security Group w/ TCP port # 3306 enabled. 
- In VPC Security Group, the answer would be YES because you will have manually specify access to port & protocol.

## ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/cloudwatch.png) [CloudWatch](https://aws.amazon.com/cloudwatch)

## CloudWatch Features
- Default Metrics : Network, Disk, CPU and Status check (Instance and System)
- Memory : RAM is a custom metric
- You can create custom dashboards all CloudWatch metrics.
- CloudWatch alarms – set notifications when particular thresholds are hit.
- CloudWatch events help you respond to state changes. E.g. run Lambda function in response to.
- CloudWatch logs helps you monitor EC2 instance/application/system logs. Logs send data to CloudWatch
- Standard monitoring 5 mins. Detailed monitoring 1 minute.
- CloudWatch is for logging. CloudTrail is for auditing your calls

# ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/vpc.png) [VPC](https://aws.amazon.com/vpc)

## VPC Features
- VPC is a logical data center within an AWS Region.
- Control over network environment, select IP address range, subnets and configure route tables and gateways.
- Do not span regions, but can span AZs.
- Can create public facing subnet (Web) having internet access and private facing subnet (DB) with no internet access
- Public Subnet – Web Servers/ Jump Boxes
- Private Subnet – Applications Servers / Database servers
- Leverage multiple layers of security – Security groups and Network ACLs to control access to EC2 instances
- Create hardware VPN connection between your local DC and AWS.
- AWS gives a maximum of /16 network.
- Bastion host/ Jump Box in Public subnet
- Security groups, Network ACLs, Route Tables can span subnets/AZs.
- Each subnet is always mapped to an availability zone. 1 subnet = 1 AZ
- Only one internet gateway per VPC. [Trick question – improve performance by adding Gateway – just not possible]
- Security groups are stateful. Network ACLs are stateless.
  
By default, how many VPCs am I allowed in each AWS Region? == 5
Typical Private IP address ranges – not publically routable.
  - 10.0.0.0 - 10.255.255.255 (10/8 prefix)
  - 172.16.0.0 - 172.31.255.255 (172.16/12 prefix)
  - 192.168.0.0 - 192.168.255.255 (192.168/16 prefix)
VPC Diagram - Public and Private subnets ![VPC with Public and Private subnets](VPC-Diagram.jpg)
To use AWS Stencils download them at the [AWS Simple Icons for Architecture Diagrams](https://aws.amazon.com/architecture/icons/) site
## Default v/s Custom VPC
  - When you create an account a default VPC is created for you in each Region.
  - All subnets in default VPC have a route out to the internet
  - Each EC2 instance in default VPC will have a public and private IP address
  - If you delete default VPC, only way to restore it is by contacting Amazon.
## Custom VPC Info
  - Default Security group, network ACL & route table are created for each custom VPC you create.
  - Doesn’t create subnets or internet gateways out of the box.
  - In each VPC you create, 5 IP addresses are reserved by AWS for itself. First 4 and last IP in the CIDR block.
  - You can't change the size of a VPC after you create it. If your VPC is too small to meet your needs, create a new, larger VPC, and then migrate your instances to the new VPC. To do this, create AMIs from your running instances, and then launch replacement instances in your new, larger VPC. You can then terminate your old instances, and delete your smaller VPC. 
  - You can’t attached multiple Internet Gateways to the VPC to boost performance.
  - When creating VPCs do not modify default route table to add your custom rules. If you modify the default route, it will affect all instances. Create a new route table for customization.
## NAT Instance & NAT Gateway
  - NAT Instance is one EC2 instance. You are responsible for performance management, scale out and security groups. NAT Gateway is a managed service.
  - On NAT instance, *remember to disable source/destination IP check*. This is required to allow private subnet internet connectivity. This is not required on NAT Gateway.
  - Allow both HTTP and HTTPS access on security groups associated with NAT instances. Security groups are always associated with NAT Instances.
  - Both *NAT Instance and NAT Gateways are deployed to public subnet*. Elastic IP has to be added to NAT Instance. NAT Gateway is automatically assigned a public IP.
  - In VPC, update default route table to allow connectivity from Private subnet to NAT Instance and Gateway
  - NAT instance is single point of failure. You can place NAT instance behind Auto Scaling group, multiple subnets in different AZs and scripted failover. To improve performance increase the size of the NAT instance to allow for higher throughput.
  - You can use Network ACLs to control traffic for both NAT Instance and Gateway.
  - NAT Gateways scale up to 10GBps. No need to disable source/ destination checks on Gateways.

## Network ACLs & Security Groups
|Security Group| Network ACL|
|-------------|-------------| 
|Operates at the instance level (first layer of defense)| Operates at the subnet level (second layer of defense)|
|Supports allow rules only| Supports allow rules and deny rules|
|Is stateful: Return traffic is automatically allowed, regardless of any rules| Is stateless: Return traffic must be explicitly allowed by rules|
|We evaluate all rules before deciding whether to allow traffic| We process rules in number order when deciding whether to allow traffic. Lower order rules take effect in case of conflict with higher order rules.|
|Applies to an instance only if someone specifies the security group when launching the instance, or associates the security group with the instance later on| Automatically applies to all instances in the subnets it's associated with (backup layer of defense, so you don't have to rely on someone specifying the security group)|
  - With default ACL, all inbound and outbound traffic is allowed automatically
  - When custom ACL, all inbound and outbound traffic is denied by default
  - 1 subnet <=> 1 AZ <=> 1 ACL.  ACLs can be associated to only 1 subnet at a time. You can reassign to another subnet. If subnet is not associated with an ACL, the default ACL is applied.
  - AWS Recommends adding ACL rules in increments of 100s
  - Ephemeral ports – Allow inbound /outbound traffic from 1024 – 65535. As clients can initiate outbound connection from any random port. Ports < 1024 reserved for super user access.
  - If you have to block a specific IP address / range, use ACLs instead of security groups. SGs can’t deny traffic – they only allow.
## Custom VPC & ELB
  - To have HA in general or for ELB, ensure that you have at-least 2 public and or private subnets in different availability zones.
## NAT & Bastion
  - You cannot use NAT instance to SSH / RDP into private subnet. For that Bastion (Jump Box) is required.
  - Bastions are used for secure administrative tasks only. Bastions are placed in Public subnets and connect to private subnets via private IP
  - For Bastion HA, have multiple Bastions in different AZs – at least 2 public subnets. Auto scaling in multiple AZ, route 53 doing health checks.
  - NAT instance is used to provide internet connectivity to private subnets.
## VPC Flow Logs
  - Enable Flow Logs for Custom VPC to see all traffic.
  - Enable to capture IP traffic flow information for the NICs of your resources. All information is reported to CloudWatch
  - Create IAM role to allow all logs to flow into CloudWatch
  - Create log group in CloudWatch and inside that create stream where you can then see all the traffic flow.

# ![](https://github.com/inbravo/aws-feature-set/blob/master/images/aws/53.png)  [Route 53](https://aws.amazon.com/route53)

## Route 53 Features
- Convert human friendly domain names into IP addresses
- IP6 (128 bits) : created to address exhaustion of IP addresses in IP4 (32 bit)
- VPCs are now IP6 compatible
- Top level domains vs second level domains
- Domain Registrars - assign domain names under one or more top level domain names

### DNS Records types
- SOA
- NS : AWS is now a Domain Registrar as well
- A : Fundamental 
- CNAME : Canonical : Resolve one domain name to another. Can’t use CNAME for Naked domains
- ALIAS : Only on AWS : Used to map resource record sets in your hosted zone to ELBs, Cloud Front Distribution, or S3 buckets that are configured as websites. e.g. you can have DNS names which point to ELB domain names -w/o the need for changing IP when ELB Ip changes.  Route 53 automatically recognizes changes in the record sets. Most common usage- map naked domain name (zone apex) to ELB names. Always use Alias v/s CNAME as Alias has no charges. Answering CNAME queries has a cost on Route53
- AAAA : Ipv6
TTL - Cache the DNS record for TTL seconds. Before DNS migration, shorten the TTLs - so no more responses are cached. 

### Hosted Zone
Collection of resource record sets. NS, SOA, CNAME, Alias etc. types of records for a particular domain.
e.g. [https://www.tcpiputils.com/dns-lookup/google.com/ALL](https://www.tcpiputils.com/dns-lookup/google.com/ALL)

## Route 53 Routing Policies
Most of the questions are scenario based.
1. Simple - Default - when a single resource performs function for your domain - only one webserver serves content
2. Weighted – send x% of traffic to site A and remainder (100 – x) % of it to site B. Need not be two different regions. Can be even two different ELBs.  This split is over length of day not based on number of individual subsequent requests.
Weights – a number between 0 and 255. Route53 calculates auto %age
AWS Takes Global view of DNS – not local / ISP view.
A/B testing is perfect use case for Weighted Routing policy
3. Latency – allows you to route traffic based on lowest network latency for your end user. To the region which gives fastest response time
Create record set for EC2 or ELB resource in each region that hosts website. When R53 receives a query it will then determine response based on lowest latency
How will the users get the best experience?  – evaluated dynamically by R3.
4. Failover – When you want to create an active /passive setup. DR site. R53 monitors health of site. If active fails then R53 routes traffic to passive site.   Here you designate a primary and secondary endpoint for your hosted zone record.
5. Geo-location – Choose where to route traffic based on geographic location of users.
Different from Latency based as the routing is hardwired irrespective of latency.
## DNS Exam Tips
  - ELBs cost money – ensure to delete them when not using.
  - ELBs always have DNS name – no public IP Addresses. Trick question might induce you into believing IP4 address for ELB
  - Remember difference between Alias and CNAME
  - Given a choice between Alias Record vs CNAME – always choose Alias. Alias records are free and can connect to AWS resources.
  - R53 supports zone apex records
  - With Route 53, there is a default limit of 50 domain names. However, this limit can be increased by contacting AWS support.
Naked domain – which doesn’t have the www in front of the domain e.g. acloud.guru. [www.acloud.guru](http://www.acloud.guru) isn’t

## SQS – Simple Queue Service
  - SQS is a distributed web service that gives you access to a message queue that can be used to store messages while waiting for a computer to process them.
  - SQS helps decouple the components of an application so they can run independently.  
  - Messages can be retrieved via SQS API
  - The producer and consumer can run at their own independent throughput.
  - The queue acts as a buffer between consumer and producer. Ensures delivery of messages at least once. Ensure your application isn’t affected by processing the same message multiple times.
  - Allows multiple readers and writers. Single queue can be used simultaneously by various applications – helps scale out applications
  - SQS Message size up to 256KB of text in any format. May consist of 1-10 messages.
  - Does not guarantee FIFO messages. If order is important, add sequencing information in each message.
  - For SQS, you have to pull messages. It doesn’t push messages – unlike SNS. You are billed at 64KB Chunks
Pricing
  - First 1 million SQS Requests per month are free.
  - $0.50 per 1 million SQS requests per month thereafter.
  - 64KB chunk = 1 request. So a message of 256KB = 4 requests.
  - Each messages has a visibility timeout – 12 hours by default. Visibility timeout period only starts when a worker node has picked up the message for processing. During this interval, the message is invisible to other processor workers.
  - SQS can do auto-scaling. If queue grows beyond a threshold, instantiate new web/app servers. Use Auto scaling + SQS to achieve this.
Exam Tip - De-couple ➔ SQS

## SWS – Simple Workflow Service
  - SWS is a web service that makes it easy to coordinate work across distributed application components. Co-ordinate tasks & workflows.
  - Amazon uses SWS to process orders on its website.
  - No EC2 components involved.
  - It can also involve human actors.
Trick Question – when to use SQS or SWS
|Attribute|SQS|SWS|
|----|----|----|
|Retention |14 days|1 year|
|API|Message Oriented|Task Oriented|
|Assignment|Might be assigned multiple times|Only once|
|State|Write code to implement tracking|Keeps Track of State & Events|
SWS Actors
1. WF Starters – e-commerce application
2. WF Deciders – Control flow of activity tasks.
3. WF Activity workers – Carry out actual task

## SNS – Simple Notification Service
  - Makes it easy to setup, operate and send notifications from the cloud.
  - Immediate delivery to subscribers or other applications
  - SNS consists of Topics and you can publish messages to topics.
  - You can send emails, text and other alerts. Apple Push, Android etc.
  - Publish messages to SQS queues, trigger Lambda functions.  Lambda function can then manipulate information and then send to other SNS Topics
  - SNS is Push based messaging.
  - You can group multiple recipients using topics. Recipients can subscribe to topics to receive notifications.
  - Flexible message delivery over multiple protocols.
  - Is used in conjunction with CloudWatch and AutoScaling.
EC2 instances pull SQS messages from a standard SQS queue on a FIFO (First In First out) basis.  – False

## Elastic Transcoder
  - Allows to convert media files from source to different media formats.
  - You pay the minutes you transcode and the resolution
  - S3 → Lambda Function → E. Transcoder → S3
  
## API Gateway
  - Managed web service which enables developers to publish, monitor and secure APIs at any scale.
  - Create an API that acts as front door for applications to access data, business logic or any functionality from your backend services
  - API Caching – Cache your endpoint’s responses. Reduces load on endpoints based on duration of TTLs
  - Low cost & Efficient. Scales
  - Throttle requests as required to prevent attacks.
  - Log requests to CloudWatch.
  - For application built on top of multiple domains, you need to enable CORS on API Gateway
  
## Amazon Kinesis
  - Streaming data is something which is generated by thousands of data sources – stock prices, game information, social network data, geo-spatial data, purchases from online stores, IoT sensor data.
  - Kinesis is an AWS platform to analyze streaming data.
  - Kinesis Streams
        - Stores data for 24 hours to 7 days.
        - Data stored in **shards**.
        - Data consumers (EC2 instances) analyze the stream and then derive results/take next actions.
        - Data capacity of stream is a function of the number of shards you specify for the stream.
  - Kinesis Firehose 
      - Don’t have to worry about shards, streams – completely automated.
      - No automatic data retention window. Data is either immediately analyzed or sent to S3 and then to Redshift, elastic search cluster
      - Data is immediately analyzed via **Lambda**.
  - Kinesis Analytics –
      - Run SQL type queries on top of data contained in Streams or Firehose and store the results in S3 / Redshift and Elastic Search cluster.
