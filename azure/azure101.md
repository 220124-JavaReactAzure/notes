# Azure

-   cloud platform with more than 200+ products and services
-   building, running and managing applications across the cloud, can even connect to on-premise
-   fast, flexible and afffordable platform
-   **Problems before cloud**
    -   peak usage during holidays and weekends
    -   new start up that suddenly becomes popular
    -   less load requirement the remainder the time
    -   _Pre-cloud Solution_
        -   PEAK LOAD provisioning: procure some infrastructure prior to a peak load
        -   can over provision infratstructure leading to more cost
        -   Data Center constraints maintenance team isn't large
            -   incurring cost for employing on-premise security, cyber security and IT etc
        -   Might need even more to backup
        -   Procuring those resources might cost you an arm and leg
        -   **Predict the future**
    -   _Cloud Solution_
        -   on-demandd provisions
        -   elasticity
        -   auto-scaling
        -   trade captial expense for variable expenses
        -   Stop predicting the future and let the cloud adjust to our demand
        -   Global in seconds

# Regions and Zones

-   Multiple data centers helps solve if one data center crashs
-   Multiplke reaggions and data centers around the world provide:
    -   faster access (most of the time)
    -   solves issues with the crashs/natural disasters affecting Data Centers
-   Regions
    -   US-Central, US-Easts
-   Zones
    -   contained within these regions (generally speaking there is always at least 3 zones)
-   Availability Zones
    -   Multiple zones (at least 3)
    -   _Fault tolerant_
        -   failure of the data center won't affect you system

# Additional Resources

-   [Cloud Provider Comparisons](https://www.zdnet.com/article/the-top-cloud-providers-of-2021-aws-microsoft-azure-google-cloud-hybrid-saas/)
-   [Azure SQL vs MySQL vs PostgreSQL](https://db-engines.com/en/system/Microsoft+Azure+SQL+Database%3BMySQL%3BPostgreSQL)

# Virtual Machines

-   In corporate, applications are deployed on physical servers
-   **Virtual Machines(VMs)** are servers from Azure
-   **Azure Virtual Machines**
    -   Service to provision & manage VM
    -   Create and manage lifcyle of VMs
    -   _Load balancing_ and _auto scaling_ for mutliple VMs
        -   _Load balancing_
            -   Split the traffic to prevent a single VM from getting overloaded
            -   Protect your from DDoS(Distributed Denial of Service) attacks (someone tries to send a ton of request to overload your servers)
        -   _Auto scaling_
            -   The ability of your online applications and services to procision or decomission resources to meet demand
    -   Attach storage(persistant disks) to VMs
    -   Manage network connectivity and configuration
    -   _Image_
        -   Operating system pre-built, things like Ubuntu, Debian, Windows(most expensive)
    -   _Authentication_
        -   can generate a password or generate an SSH key
        -   Add two inbound ports for SSH(22) and HTTP(80)
        -   once done creating, key pair for the SSH can be accessible. (KEEP THIS TO YOURSELF)
-   Deployment will take several minutes

# Connecting to Azure VMs

-   Azure provides cloud shell
    -   can be used to execute commands from CLI
    -   _Bash_
        -   used on linux
    -   _Powershell_
        -   used on windows
    -   Uploading the key file from creating the VM to azure cloud shell
-   Follow the following commands:

```bash
chmod 400 my-first-vm_key.pem
ssh -i YOUR_KEY_PATH azureusername@PUBLIC_IP_ADDRESS
ssh -i my-first-vm_key.pem azureusername@255.255.255.255 # this azureusername@255.255.255.255 is subject to each individual

whoami
python -version
hostname

apt-get -y update
apt-get -y install nginx

echo "Hello World"
echo "Hello World" > /var/www/html/index.html
echo "Hello World from Reston office at Revature" > /var/www/html/index.html

hostname
echo "$(hostname)"
echo "Hello World from $(hostname)"
echo "Hello World from $(hostname)" > /var/www/html/index.html
```

# Key Concepts

-   **Image**
    -   choosing operating system and software
    -   wide variety
    -   linux images tend to be less expensive
-   **VM Family**
    -   choose the right family of hardware
    -   General purpose
    -   Compute/Storage/memroy optimized
    -   GPU specific
-   _Sizes_
    -   default nomenclature for various family types
    -   different specificed provisioned resources
    -   helps choose the right VM size for your task
-   _Disks_
    -   Attach Virtual Disks to VMs (storage)

# Simplifying installing software/libraries for VMs

-   Advanced tab
-   Make use of cloud init
    -   provides a way to simplify commands that execute at start up

```bash
#!/bin/sh
sudo su
apt-get -y update
apt-get -y install nginx
echo "Welcome to Revature! From the Reston Office! $(hostname)" > /var/www/html/index.html
```

# Availability

-   Are the apps/program available when they aere need
    -   percentage of time an application provides the operations expected of it
    -   Ideally 99.9% uptime, but that's rough
-   _Single Instance VM Disks_ have Availability assurance from Azure
    -   Premium SDD: 99.9
    -   Standard SDD: 99.5
    -   Standard HDD: 95
-   2+ instances in the same availiability set: 99.95%
-   _Availability Set_ is a logcial groupoing of VMS
    -   _Fault domains_:
        -   group of VMs share a common power source
    -   _Update domains_:
        -   group of VMs taken down for maintenance/updates at the same time
-   2+ or more instance in 2+ Availablity Zones : 99.99

# VM Scale Sets

-   Simplify cretion and management of multiple VMs
-   Optional
    -   Add load balancer
    -   Distribute VMs accross multiple AZs
    -   Supports manual and auto scaling
-   Default it will always create a private IP, we need to create a private IP to expose the VM to us
-   Scaling configuration available

# Static IP Address

-   Every public IP address you create has a charge associate with it
-   When you stop instances you release that public IP address for your VMs
    -   If you restart your VM, it will create a new IP
-   To prevent this, you need to allocate a _Static_ IP address
    -   this will incure charges by the hour

# Monitoring

-   Shows the metrics of your VMs
-   Showing how resources are being used
    -   CPU
    -   GPU
    -   Memory
-   This is dodne by _Azure Monitoring_

# Dedicated Hosts

-   Specified Hardware are guaranteed to belong to you!
-   More costly, but good if you want to make sure you have the hardware available as much as possible

# Azure Spot Instances

-   Take advantage of unused capacity
-   **No guarantee** Azure can take the resources back at any moment
-   Make sure the jobs running on this are _FAULT TOLERANT_
    -   means the job can start and stop without losing it's position
    -   doesn't need to restart from scratch
    -   no data is lost

# Reserved VM Instances

-   Significantly decreased cost by reserving VMs for 1 or 3 years
-   Requires some predictions of your minimum requires for longer periods of time

# Scalability

-   _Vertical_
    -   increases the resources ont he VM
    -   Limits to VM scaling
    -   There are limits to how much resources you can allocate to a VM
-   _Horizontal_
    -   Deploying multiple instances of application/database
    -   preferred to Vertical scalling
        -   VS has limits
        -   VS can be expensive
        -   HS increases availability

| Terminology       | Description                                                                                    | Azure                                 |
| ----------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------- |
| Availability      | Are they availbe when you need them                                                            | Availability Set and Scale Sets       |
| Scalability       | Ability of system to response to increases in Traffic                                          | VM Size, Scale Sets and Load Balancer |
| Resilience        | Ability of system to provide acceptable behavior even when one or more parts of the sytem fail | Scale Sets and Load Balancers         |
| Geo-distribution  | Distribute applications across regions and zones                                               | Scale Sets and Load Balancers         |
| Disaster Recovery | How to keep your systems running during disasters                                              | Site Recovery                         |

# Azure Pricing Calculator

-   Used to determine how much it would cost for different resources and allocations
-   Good to show cost estimates for creating a functional services
-   **Price for the same VM is not always the same**
    -   Region can determine price
    -   Demand can determine price

# App Services

-   Fully managed platform for building, deploying and scaling your web apps
    -   Also supports REST APIs, mobile back ends
-   Defines a set of compute resources for a web app
-   Features
    -   Auto deployment and management
    -   Auto scaling
    -   Built in load balancing

# Azure Storage

-   What is the type of storage of your hard disk?
    -   Block Storage
-   You've created a file share to share a set of files with your colleagues in an enterprise?
    -   File Storage
-   You want to upload/download objects using a REST API without mounting them onto your VM
    -   Object Storage
-   MAnaged Cloud Storage Solution
    -   Highly avail
    -   durable
    -   massively scalable (few PetaBytes)
-   Core STorage Services
    -   **Azure Disk**:
        -   block storage (hard disks) for VMs
    -   **Azure Files**:
        -   File shares for cloud and on-premise
    -   **Azure Blobs**:
        -   Object store for text and binary data
    -   **Azure Queues**:
        -   Decouple applications using messaging
    -   **Azure Tables**:
        -   NoSQL store (extremely basic, Azure Cosmos is preferred for NoSQL)

## Data Redundancy

-   Locallly Redundant Storage
    -   3 synchronous copies in the same data cetner
    -   least expensive, lowest availability
-   Zone-Redudndant Storage
    -   3 synchronous copies in 3 AZs in primary region
-   Geo-Redundant Storage
    -   LRS + Asynch copy to secondary region (three more copies using LRS)
-   Geo-zone-Redundant Storage
    -   ZRS + Asynch copy to secondary region (three more copies using LRS)
    -   Most expensive, provides highest availability

## Azure Files

-   Media workflows need huge share storage
-   Enterpirse users need a quick way to share files
-

## Azure Blob Storage

-   Object Storage in Azure
-   _Structure_
    -   Storage Account > Container(s) > Blob(s)
-   Store massive cvolumes of unstructure data
    -   _Store All file types_ - text, binary, backup & archive
-   3 types of Blobs
    -   Block Blobs
        -   store test or binary files
    -   Append Blobs
        -   store log files (ideal for append operations)
    -   Page Blobs
        -   foundation for Azure IaaS disks
-   **Azure Data Lake Storage Gen2**
    -   Azure blob storage enhanced
    -   Designed for enterprise big data analytics
        -   exabytes
        -   hierachical
    -   Low-cost
    -   tiered storager
    -   High availability
    -   Disaster recovery

### Access Tiers

-   Hot
    -   Store frequently accessed data
-   Cool
    -   Infrequently accessed
    -   stored for minimum 30days
-   Archive
    -   Rarely accessed data
    -   stored min 180 days
    -   low cost **BUT** highest access cost
    -   Access latency: in hours
        -   To Access:
            -   **Rehydrate**
                -   chantge access tier to hot or cool
            -   Copy to another blob with access tier hot or cool

# DevOps (NOT AZURE SPECIFIC)

-   Portmanteau of **Dev**elopment and **Op**eration**s**
-   most modern way of approacvhing applications and software
-   **Development**
    -   testing and creating of code
-   **Operations**
    -   deploying, maintaing and making publically available applications that are written in development
-   DevOps
    -   developers and IT operations
    -   collaborative effort between these teams throughout the product lifecycl
    -   **_LIFECYCLE_**
        -   _PLAN_
            -   Adopting that agile practice
            -   used to improve speed and quality
            -   A LOT goes into this, make sure you're comfortable with compromise
        -   _BUILD_
            -   writing the code
            -   utilizing git to work in a team or alone
            -   branching
            -   re-wrtiing
            -   commits
            -   heavy development focus
        -   Continuous Integration and Deployment
            -   CI/CD pipelines
            -   **_Continuous Integration_**
                -   Software development practice wehre you contianously add code to a remote repo
                -   OFTEN this code is tested to verify that it works correct
                -   **Triggers**
                    -   This handles these tests and validations at commits
                    -   can also handle the compilation of a project such as maven
            -   **_Continuous Delivery_**
                -   extension of the integration
                -   after passing all tests or validtions in production environment
                -   automatically deploy all the code changes testing/development stage/deployment
                -   Any time you push your code that calls a trigger as long as it passes the approriate validations in integration this will build immediately and can deploy to a testing/development
            -   **_Continuous Deployment_**
                -   one step further than the previous
                -   you have to pass all previous stages
                -   there is no human intervetion and only a failed test will prevent a new change to be deployed
        -   **Monitor**
            -   constantly checking for any issues in logs or anything that might fail or any bugs
        -   **Operate**
            -   end-to-end devliery of IT services
        -   **Continous Feedback**
            -   customer feedback to it support, which then leads it down the line to developers

## Azure DevOps

-   Service provided by Azure
-   CI/CD/CD
-   Azure REpos
-   Azure Boards
-   Azure Artifacts
-   Test Plants
-   **_Pipelines_**
