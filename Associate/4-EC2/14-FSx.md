## Amazon FSx for Windows & Amazon FSx for Lustre

Amazon FSx for Windows File Server provides a fully managed native Microsoft Windows file system so you can easily move your Windows-based applications that require file storage to AWS. Amazon FSx is built on Windows Server

### Amazon FSx for Lustre
Amazon FSx for Lustre is a fully managed file system that is optimized for compute-intensive workloads, such as high-performance computing, machine learning, media data processing workflows, and electronic design automation (EDA).

With Amazon FSx, you can launch and run a Lustre file system that can process massive data sets at up to hundreds of gigabytes per second of throughput, millions of IOPS, and sub-millisecond latencies

### Amazon FSx for Lustre vs EFS vs FSx
Lustre FSx:
- Designed specifically for fast processing of workloads such as machine learning, high performance computing (HPC), video processing, financial modeling, and electronic design automation (EDA).
- Lets you launch and run a file system that provides sub-millisecond access to your data and allows you to read and write data at speeds of up to hundreds of gigabytes per second of throughput and millions of IOPS.

FSx
- A managed Windows Server that runs Windows Server Message Block (SMB)-based file services.
- Designed for Windows and Windows applications.
- Supports AD users, access control lists, groups and security policies, along with Distributed File System (DFS) namespaces and replication.

EFS
- A managed NAS filer for EC2 instances based on Network File System (NFS) version 4.
- One of the first network file sharing protocols native to Unix and Linux.

### Exam Tips
In the exam you’ll be given different scenarios and asked to choose whether you should use an EFS, FSx for Windows or FSx for Lustre:
- EFS: When you need distributed, highly resilient storage for Linux instances and Linux-based applications.
- Amazon FSx for Windows: When you need centralised storage for Windows-based applications such as Sharepoint, Microsoft SQL Server, Workspaces, IIS Web Server or any other native Microsoft Application.
- Amazon FSx for Lustre: When you need high-speed, high-capacity distributed storage. This will be for applications that do High Performance Compute (HPC), financial modelling etc. Remember that FSx for Lustre can store data directly on S3.