
#  Research: Types of Cloud Storage

| Storage Type | How It Stores Data | Best Used For | Cloud Provider Examples |
| :--- | :--- | :--- | :--- |
| **Block Storage** | Breaks data down into raw, fixed-size chunks called "blocks," each with its own address. The operating system treats these like a physical hard drive, giving us ultra-fast read/write speeds. | Running high-performance databases, hosting enterprise applications, and powering virtual machine boot drives. | AWS EBS, Azure Disk Storage, Google Persistent Disk |
| **File Storage** | Organizes data into a classic folder-and-directory hierarchy. It’s shared over a network using standard file-sharing protocols (like NFS or SMB) so multiple systems can access the same files at once. | Collaborative team workspaces, home directories, content management systems, and legacy web apps. | AWS EFS, Azure Files, Google Cloud Filestore |
| **Object Storage** | Stores data as self-contained "objects" inside flat containers (buckets) instead of a folder tree. Every single object bundles the actual data, custom metadata, and a unique ID. | Storing massive amounts of unstructured content—think user-uploaded photos, backups, data lakes, and media streaming files. | AWS S3, Azure Blob Storage, Google Cloud Storage |

## Recommendation

For handling user-uploaded images, **Object Storage** is hands-down the way to go. It scales infinitely without any management headaches, handles unpredictable file sizes effortlessly, and lets us serve up images quickly and cost-effectively using unique URLs.
