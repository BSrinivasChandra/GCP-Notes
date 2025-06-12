Artifact Registry enables a single central location to store and manage artifacts and build dependencies.

An Artifact can be any of these things:
- Docker container Images
- Language specific packages

Artifact Registry API is to be enabled.

Artifacts are stored under repositories.
These repositories can be of three types or modes:
- Standard - To pull/push private artifacts
- Remote - Stores artifacts on external sources as Docker Hub, PyPI, etc.
- Virtual - 

#### **Mutable vs Immutable Tags**

A tag is a label for an image build. By default a tag can only refer to one version of image build. It can be enforced otherwise using mutable tags.

**Digest** : A digest is an automatically generated hash which uniquely identifies each version of an image build. It is sha256

**Immutable Tags**
- Tag points to only one specific digest.
- Cannot Delete tagged images. 
- Cannot remove a tag from an image.
- Cannot push an image with same tag used by other images.

**Mutable Tags**
- Tag pointing to an image digest can change, preferably to latest digest of an image.


### **Docker Images in Artifact Registry**

1. Configure Docker for Artifact Registry
   command: `gcloud auth configure-docker <region>-docker.pkg.dev`
2. The image must be tagged with following remote push path.
   It can be tagged after the creation of image or can be directly pushed into repo at a time of creation with the tag.
   
   **Method 1:** Tagging an existing image.
   `docker tag image <REGION>-docker.pkg.dev/<PROJECT-ID>/<REPO>/<IMAGE>:<TAG>`
   `docker push <REGION>-docker.pkg.dev/<PROJECT-ID>/<REPO>/<IMAGE>:<TAG>`
   
   **Method 2:** Tagging an image at the time of creation.
   `docker build -t <REGION>-docker.pkg.dev/<PROJECT-ID>/<REPO>/<IMG>:<TAG> .`
   `docker push <REGION>-docker.pkg.dev/<PROJECT-ID>/<REPO>/<IMAGE>:<TAG>`
3. Required to grant permissions to read & write to Artifact Registry. 
   Some Roles:
   - Artifact Registry Writer(reads, writes)
   - Artifact Registry Reader(Only reads)
   - 