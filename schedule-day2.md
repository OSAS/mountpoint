<link rel="stylesheet" href="style.css">

<img src="images/logo.svg" id="logo" alt="Mountpoint" />

# mountpoint
## August 28, 2018

| Time  	| Session  	|   Session	|
|---	|---	|---	|
|  Opening: 9am - 9:15am 	|   	|   	|
| 9:15am - 9:55am  	|  Software-Defined Storage Fast, Fast, Fast	 	| Making Ceph fast in the face of failure  	|
|  10:00am - 10:45am 	|  OpenShift.io on Gluster: Adventures in production 	|  Anatomy of a librados client application 	|
|   11:00am - 11:45am	| Testing Storage System Upgrades Successfully  	|   What Ever Happened to Durability?	|
| Lunch  	|   	|   	|
|  1:00pm - 1:45pm 	|  Multi-tenancy Approaches in Gluster 	|  Current and Future of Non-Volatile Memory on Linux	|
|  2:00pm - 2:45pm	| Block Deduplication and Compression with VDO  	| Doctor! I need Ceph: a journey of open source storage in healthcare‍  	|
|  3:00pm - 3:45pm		| What's new in Gluster?  	|  Self-aware Ceph: enabling ceph-mgr to control Ceph services via Kubernetes 	|
|  Roundtable 4:00pm - 4:45pm|   	|   	|
|  Closing - 4:45pm to 5:00pm 	|   	|   	|

### Software-Defined Storage Fast, Fast, Fast
Automated workload-tuned Gluster deployments with the help of Ansible
Software-defined storage is no longer an emerging technology, with projects such as Gluster and Ceph deployed consistently and effectively for mission-critical workloads in large enterprises and in the public sector. Reaching a new maturity phase, the next critical checkpoint for success is to codify the massive amount of institutional knowledge from thousands of deployments into a "best practices" recipe to make new deployments simpler and to provide a shortcut to success.

In this session, Dustin Black, Software-Defined Storage Architect at Red Hat, will present and demonstrate the Gluster Colonizer project, a new toolset that leverages Ansible automation to achieve workload-optimized deployments of SDS while limiting the need for architectural scoping and testing. Learn how you can leverage the knowledge of hundreds of engineers to get your SDS solution aligned to your workload in minutes instead of weeks.


Speaker: Dustin Black

Dustin Black is a Storage product architect at Red Hat, primarily focused on automation and performance optimization of Gluster software-defined storage. He is the creator and maintainer of the gluster-colonizer project, a deployment orchestration toolset that leverages the power of Ansible. Dustin has worked with SDS at Red Hat for more than 6 years, beginning with the acquisition of Gluster. He has worked closely with enterprise users deploying Gluster and Ceph to solve critical business challenges, and in recent years has leveraged his expertise to continually simplify the SDS adoption process and provide technical guidance and reference architectures for price-performance match to workloads. Dustin has a deep wanderlust, enjoys cooking southern BBQ, and plays a bit of saxophone when the mood strikes him.

### Making Ceph fast in the face of failure
Ceph Luminous and Mimic improve the impact of recovery on client I/O. In this talk we’ll discuss the key features that affect this, and how Ceph users can take advantage of them.
Historically, recovery has had major impact on client performance - for example when a node goes down, backfilling and recovery increase client latency.
With Luminous and Mimic, recovery and other background work has improved in several ways to allow finer tuning and better behavior out of the box.
We’ll discuss how these are implemented and what operators should know about tuning Ceph recovery.

Speakers: Josh Durgin and Neha Ojha

Josh is the Tech Lead for RADOS. Neha is a core Ceph developer working on RADOS.

### OpenShift.io on Gluster: Adventures in production
This talk will discuss our experience using Gluster as the storage solution behind Red Hat’s OpenShift.io platform. We will describe the environment’s unique requirements and goals, the solution we constructed, and our experiences maintaining it in production.
The talk will start with an overview of the OpenShift.io environment and its storage needs. It will describe the previous solution of directly using EBS for storage and the problems of both availability and scale that were encountered.
It will walk through the chosen Gluster solution (gluster-subvol) based on the storage requirements of the environment and the limitations of Gluster. The limitations of this approach will also be considered.
Following the description of the high-level approach, the talk will describe the actual configurations that have been chosen for production and what has been learned from the experience. This includes how the environment is scaled, automation that has been necessary, performance considerations, and environment monitoring and availability.

Speaker: John Strunk 

John Strunk is a Gluster architect at Red Hat focusing on containers and cloud deployments of Gluster. In addition to his other duties, he designed, built, and maintains the Gluster clusters that support the OpenShift.io infrastructure. Prior to Red Hat, John spent 9 years as a researcher in the Advanced Technology group at NetApp, focused on emerging technologies.

### Anatomy of a librados client application 
A gentle introduction to writing your first program using the librados C++ API. Librados provides a powerful API that allows you to design your own interface to
a Ceph Storage Cluster and interact directly with some of the cluster daemonssuch as Monitors and OSDs. This presentation will walk through what is requiredto create an environment that will enable you to get started programming withlibrados as well as describing the steps required to compile and link your first program. We will then explore the librados C++ API calls you may want to use and how you might go about verifying the operation of your program in terms of the actual data written to the cluster.

Speaker: Brad Hubbard

Brad Hubbard is a Senior Software Engineer at Red Hat and works on RADOS, the open source, distributed object storage system at the heart of Ceph.

### Testing Storage System Upgrades Successfully 
Testing successful upgrade of a storage system is key to adoption and user friendliness. This talk describes the proposed upgrade testing framework for Gluster. 
This talk is a discussion on the basics of a framework to handle this and how it will handle the simple to complex cases. This is a discussion with a proposaland PoC. I welcome feedback and comments that will help us improve this project to handle most of the edge cases.

Speaker: Nigel Babu

Nigel is a systems engineer at Red Hat. He originally started working on Gluster to build out the test pipeline. In this process, he's been roped as a co-maintainer for the test framework, Glusto. Nigel has been looking into how to test various pieces of Gluster and build that into a pipeline for the last year or so. Automated performance testing and upgrade testing are the main challenges that he's been trying to solve for upstream Gluster in the last year.

### What Ever Happened to Durability?
Durability is a fundamental property that people and applications expect from storage systems.  Yet with scale-out systems and new types of hardware with complex firmware, it can be hard to implement, or even define durability. "Durability, the 'D' in ACID, is a fundamental property that people and applications expect from storage systems. Durability used to mean that you knew your data was safely on disk when ""the"" computer crashed - it was just a matter of waiting for the computer to come back up.  With today's complex, software defined, scale-out databases and filesystems Durability can be very hard to even define. Achieving it is stupendously hard given the partitioning problem, operating systems with flaky file systems, and storage devices with complex firmware.
Durability today demands replication, but replication is not enough.  But because of the need to replicate, durability becomes a networking problem, inheriting the performance and availability issues thereof.
We will introduce the Apache Bookkeeper project, which can be used to solve these kinds of problems, and suggest how similar projects could be designed to be embedded in more conventional software-defined storage systems.

Speaker: Tom Lyon

Tom Lyon is a computing systems architect, a serial entrepreneur and a kernel hacker.  Prior to founding DriveScale, Tom was founder and Chief Scientist of Nuova Systems, a start-up that led a new architectural approach to servers and networking. Nuova was acquired in 2008 by Cisco, whose highly successful UCS servers and Nexus switches are based on Nuova’s technology. He was also founder and CTO of two other technology companies. Netillion, Inc. was an early promoter of memory-over-network technology. At Ipsilon Networks, Tom invented IP Switching. Ipsilon was acquired by Nokia and provided the IP routing technology for many mobile network backbones.
As employee #8 at Sun Microsystems, Tom was there from the beginning, where he contributed to the UNIX kernel, created the SunLink product family, and was one of the NFS and SPARC architects. He started his Silicon Valley career at Amdahl Corp., where he was a software architect responsible for creating Amdahl’s UNIX for mainframes technology.
Tom holds numerous U.S. patents in system interconnects, memory systems, and storage. He received a B.S. in Electrical Engineering and Computer Science from Princeton University.

### Multi-tenancy Approaches in Gluster 
When Gluster is deployed at many-petabyte scale, larger shared volumes are necessary for both resource-efficiency and operational-complexity reasons, but can run up against single-volume scaling limits and "noisy neighbor" issues. This talk lays out a roadmap for addressing these problems.

Speaker: Jeff Darcy

Jeff Darcy has 30 years in the industry, 20 in distributed filesystems, nearly 10 as a developer and co-maintainer on Gluster.

### Current and Future of Non-Volatile Memory on Linux
Storage hardware has come a long way in performance and reliability, as well as the interfaces it runs on. In this talk, Keith will discuss the current and future state of Non-Volatile Memory Express for both local PCIe attached and remote fabrics connected targets implementing this protocol, as well as the new native multipathing subsystem for increased performance and failover reliability. The talk will go over methods to turn tune applications for various needs, how to turn your Linux machine into an NVMe target, and backing it up with blazingly fast persistent memory for increased speeds.

Speaker: Keith Busch

Keith Busch is a Linux storage software developer at Intel. He collaborates on the various protocol standards that enable current and future non-volatile memory and is the mainline kernel maintainer for NVM Express. Beyond NVMe, Keith contributes to the adjacent subsystems and enabling persistent memory DIMMs.

### Block Deduplication and Compression with VDO 
The kvdo device-mapper module provides block level deduplication and compression to the Linux storage stack. This session will provide an overview of VDO and its deployment, a review of usage considerations, and a high-level introduction to its design and implementation.

Speaker: J. Corwin Coburn

Corwin has spent 17 years developing and integrating deduplication, compression, and distributed primary storage on Linux. He was the principal engineer at Permabit and is now the lead architect for VDO at Red Hat.

### Doctor! I need Ceph: a journey of open source storage in healthcare‍  
Alex Gorbachev of Intelligent Systems Services Inc. will present a use case of Ceph and other open source storage in mission critical healthcare applications over the last 15 years. This is a technical, as well as mildly philosophical presentation that covers principles of deployment, operation, pitfalls and successes of employing open source solutions in a traditionally closed source field.

Speaker: Alex Gorbachev

Alex Gorbachev: 1994 - present: founder and president of Intelligent Systems Services Inc., focusing on open source technology in healthcare, scalable mission critical open source storage, 24/7 operations with a continuous commitment to technology and operational excellence, IT community enhancement and continuous improvement.

### Self-aware Ceph: enabling ceph-mgr to control Ceph services via Kubernetes 
This session will describe and demonstrate a new framework for integrating Ceph with the orchestration framework it is running on, enabling ceph-mgr and the dashboard UI to deploy and manage Ceph services.

Speaker: John Spray

John is a Principal Software Engineer at Red Hat.  He has been an active contributor to the Ceph project since 2013, with a focus on CephFS and ceph-mgr.
