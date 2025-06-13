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
Bucket location determines replication, redundancy, latency & storage cost of data.

1. Single Region: A specific geographic place, such as asia-south1(Mumbai).
	- Bucket is stored within a region replicated through out all availability zones. 
	- No outbound/egress charges when reading data within the same region.

2. Dual Region: A specific pair of distant regions within a continent.
	- Bucket is replicated through out all the zones in these two regions
	- No outbound/egress charges when data is access within either of these regions.

3. Multi Region: A geographic area containing two or more regions.
	- 