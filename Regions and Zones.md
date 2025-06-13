### **Region**
Region is a geographical location containing different zones.
Regions are typically cities in a country.
Eg: 
- asia-south1(Mumbai), us-central1(Iowa), asia-south2(Delhi)
### **Zone**
Zone is a deployment area within a region. They are typically several kilometer apart from each other.
Zones have high-bandwidth and low-latency network connection between them within a region.
Eg:
- asia-south1(regions): a, b, c(zones)

### **Regional Vs Zonal Resources**
Resources that live in a zone are zonal resources such as virtual machines, persistent disks. Whereas resources that live across a region is a reginal resource such as Static IP address.

