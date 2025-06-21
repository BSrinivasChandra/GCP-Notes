**Cloud storage** is a storage service provided by google. It stores **objects** in containers called **buckets**. Objects are data residing in any file format.

### **GCS Hierarchy**
- Organization
  - Project
    - Bucket 
	    - Objects - A bucket can store unlimited files as objects.
	    - Managed Folders - Folder inside a bucket in which objects are stored.
	    - Hierarchical Namespace - Logical file system structure.
	      Use cases: HDFS, AI ML Workloads, Hierarchy file system workloads.

### **Bucket Location**
Bucket location determines replication, redundancy, latency & transfer cost of data.

1. **Region**: A specific geographic place, such as asia-south1(Mumbai).
	- Cross Zone Replication: Bucket is stored within a region replicated through out all availability zones. 
	- No outbound/egress charges when reading data within the same region.

2. **Dual Region**: A specific pair of distant regions within a continent.
	- Cross Region Replication: Bucket is replicated through out all the zones in these two regions
	- No outbound/egress charges when data is access within either of these regions.

3. **Multi Region**: A geographic area containing two or more regions.
	- Bucket is replicated through out all the regions in a continent.
	- Outbound/Egress charges are always applied. Data access from any region is considered as inter-region transfer.

### **Storage Classes**
Storage class is property of a bucket that determines availability & storage cost of data.

Every storage class possess an annual durability of 99.999999999%(Nine 9's).

1. **Standard storage**
	- Best for data that is frequently accessed, stored for brief period of time known as "Hot Data".
	- Default Storage class for a bucket.

2. **Nearline storage**
	- 
	- Data which is accessed once or less per month.

3. **Cold storage**
	- 
	- Data which is accessed once or less per quarter.

4. **Archive storage**
	- 
	- Data which is accessed once or less per year.
