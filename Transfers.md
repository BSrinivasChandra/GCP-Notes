## **Data Transfer Methods in GCP**
These methods transfers data without the need of downloading.
I have come across these data transfer methods in gcp:
- Storage Transfer Service(GCP's Service)
- Python Script using storage client
### **Storage Transfer Service**
There are many jobs options within STS, I have worked with the following.
- **GCS to GCS**
	- Supports cross bucket, cross project data transfer.
	- Doesn't support cross account or public object transfer.

- **URL to GCS**
	- Supports public object url to gcs transfer. These url can be `http` or `https` protocolled.
	- A formatted tsv file is used, which looks like below.
	```text
	TsvHttpData-1.0
	https://storage.googleapis.com/airflow-backup-001/airflow-image.vmdk
	```
	- Once created and stored in a bucket, provide gsurl of tsv file to the job.

STS supports cross-cloud transfers. Transfers can be automated by scheduled triggers, overwrite & delete.
### **Python Script in CloudShell**
- Storage client & copy_blob() is used. A strict 30-second time limit is set.
- Generally not suitable for large data transfers with cross region/storage class transfers.
- Supports cross bucket and cross project data transfer.
