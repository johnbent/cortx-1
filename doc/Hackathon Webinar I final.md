

Seagate

1





Informational Webinar:

CORTX Integration Challenge

April 14, 2021

Rachel Novak, Justin Woo

Seagate

2





01

02

CORTX 101

How CORTX works

AGENDA

03

04

CORTX & Integrations

How to set up your VM

Seagate

3





05

06

How to build an integration

Live demo

AGENDA

07

08

How to submit your integration

Questions

Seagate

4





CORTX is...

Mass-capacity object storage system.

But what is an object store?

\1. NASA collects massive amounts of data, and has

petabytes of storage in the form of many, many,

many disks.

\2. Storage hardware only provides space- you need

a system for storing, cataloguing, retrieving,

updating, and repairing the data.

\3. Object storage provides a way to store and

manage data on a massive scale

Seagate

5





Key Components of object storage:

• A way to decide how and where to store data on the

hardware

• How to organize the location information of that data

(i.e. metadata- what is this data object and where is it)

• A way to ensure that many users can access the same

data at the same time without conflicts

• Monitoring the health of the data and the system

• Mechanisms to recover from failure/errors and to

ensure data isn’t lost or corrupted

• A management system by which admins and users can

view the health of the system and configure various

behavioral aspects





Key Components of CORTX

CORTX as a platform is made up of different modules, each of which handle different functions.

• MOTR

• HA & HARE

• Monitor for failures

• Tell Motr what to rebuild

• Manager

• CORTX S3

• Primary data store

• Human-friendly

• Translates between

Motr and S3

interface with CORTX

• Interacts directly with

storage devices

• Administrative UI

• Allows use of S3 API

when connecting to

other tools and

• Manages data storage

and metadata

• Web GUI for monitoring

& management

platforms

• Rebuilds data after

failures.

Seagate

7





What roles do integrations play in object storage?

\1. NASA wants to analyze

the data it has stored on

its hardware

\2. It will need to integrate

its analytics tools & data

collection tools with its

data store

\3. An integration connects

a tool like PyTorch with

an object store like

CORTX

Seagate

8





Selecting an Integration

\1. What data is collected?

Elasticsearch

PyTorch

Search & Analytics

Machine Learning

Presto

Query Engine

\2. What needs to be done

with that data?

Greenplum Analytics

Apache Kafka

Stream Processing

Restic

VXG

Backup

VSaaS

\3. Identify the tools that would

need to connect to the

stored data or the storage

hardware.

Apache Spark Spark Analytics

IPFS

Peer to Peer File Share

dataobi

Grafana

H2O.ai

Data Migration

Dashboard

Humio

Log management

VsaaS

Video Loft

Machine Learning

Reverse Proxy /

Load Balancer

Tensorflow

Prometheus

FIO

Machine Learning

Monitoring

Traefik

Alexa

IOR

Voice

Benchmark

HPC Benchmark

Seagate

9





CORTX- How to Build an Integration

• Identify the tool you want to integrate with CORTX

• Go to their website and check out their documentation for S3 API

(Motr integrations are a bit trickier. If you have questions, please ask in #hackathon-support-and-

mentorship)

• Identify the functions for writing data to the platform (or other relevant functions, depending on

what you are integrating with)

• Edit config file or write code to set up your integration

• Test! Run your integration and make sure the two components (CORTX and your integration

platform) are correctly connecting

• Document it!

• Explain what the tool does, and how it will work with CORTX.

• Ensure you document every step, including the ones that seem obvious

• Explain each step and be sure to mention potential failures/errors as well as documenting what success

looks like.

Seagate

10





Submitting your Integration

A submission to the CORTX Integration Challenge will be considered complete if it contains:

A functional integration between CORTX and another system, platform, or tool, which is explained

and documented in:

\1. A pull request to the CORTX GitHub Repository

\2. A video demonstrating the set up and functionality of the integration, along with an

explanation of its purpose

\3. Documentation in the pull request explaining how to set up and use the integration.

The DEADLINE for project submissions in Devpost is **11:00 PM PT , Tuesday, April 27th**

Seagate

11





Submitting your Integration

Submission instructions: <https://github.com/Seagate/cortx/blob/main/doc/integrations/fhir.md>

Step 1: Sign-up or sign-in to GitHub

Step 2: Fork the CORTX repository so you can make a pull request.

Step 3: In that fork, open the integration folder and create a .md Markdown file. In that file include:

• The intention behind the integration and what it does.

• Installation directions that are clear, accessible, and easily reproducible.

• A link to your integration video which includes:

• An explanation of the integration use case - why/how it is useful or impactful in addition to

demonstrating how to set up and run the integration.

• Clear and concise directions on how to install the integration

Step 4: Make a pull request to merge your changes back to the main repository.

Step 5: Go to Devpost and submit your integration by posting a link to your pull request.

Seagate

12





Live Demo - Integration

A good example of an integration, write up, and video can be found here:

• [Splunk](https://github.com/Seagate/cortx/blob/main/doc/integrations/splunk.md)[ ](https://github.com/Seagate/cortx/blob/main/doc/integrations/splunk.md)[Integration](https://github.com/Seagate/cortx/blob/main/doc/integrations/splunk.md)[ ](https://github.com/Seagate/cortx/blob/main/doc/integrations/splunk.md)[(CORTX](https://github.com/Seagate/cortx/blob/main/doc/integrations/splunk.md)[ ](https://github.com/Seagate/cortx/blob/main/doc/integrations/splunk.md)[Github)](https://github.com/Seagate/cortx/blob/main/doc/integrations/splunk.md)

• [Connecting](https://www.youtube.com/watch?v=rBAIloua4p0)[ ](https://www.youtube.com/watch?v=rBAIloua4p0)[CORTX](https://www.youtube.com/watch?v=rBAIloua4p0)[ ](https://www.youtube.com/watch?v=rBAIloua4p0)[to](https://www.youtube.com/watch?v=rBAIloua4p0)[ ](https://www.youtube.com/watch?v=rBAIloua4p0)[Splunk](https://www.youtube.com/watch?v=rBAIloua4p0)[ ](https://www.youtube.com/watch?v=rBAIloua4p0)[–](https://www.youtube.com/watch?v=rBAIloua4p0)[ ](https://www.youtube.com/watch?v=rBAIloua4p0)[YouTube](https://www.youtube.com/watch?v=rBAIloua4p0)

Seagate

13





CORTX- Setting up your VM

There are a few ways you can get a CORTX VM to run…

**Use CloudShare**

**Stand up your own VM**

• Download [OVA](https://github.com/Seagate/cortx/releases/download/ova-1.0.3/cortx-va-1.0.3.ova)

• Set up VM Docs:

• [CORTX](https://github.com/Seagate/cortx/blob/main/doc/CORTX_on_Open_Virtual_Appliance.rst)[ ](https://github.com/Seagate/cortx/blob/main/doc/CORTX_on_Open_Virtual_Appliance.rst)[VM](https://github.com/Seagate/cortx/blob/main/doc/CORTX_on_Open_Virtual_Appliance.rst)[ ](https://github.com/Seagate/cortx/blob/main/doc/CORTX_on_Open_Virtual_Appliance.rst)[Setup](https://github.com/Seagate/cortx/blob/main/doc/CORTX_on_Open_Virtual_Appliance.rst)

• To gain access to a

• Requirements

pre-configured CloudShare

environment, all you need to

do is request access!

• Min. 8GB of RAM

• A VM application:

Vmware, VirtualBox,

etc.

• [Documentation](https://github.com/Seagate/cortx/blob/main/doc/CORTX_on_Open_Virtual_Appliance.rst)

[Instructions](https://github.com/Seagate/cortx/wiki/CORTX-VM-on-VirtualBox)[ ](https://github.com/Seagate/cortx/wiki/CORTX-VM-on-VirtualBox)[for](https://github.com/Seagate/cortx/wiki/CORTX-VM-on-VirtualBox)

[VirtualBox](https://github.com/Seagate/cortx/wiki/CORTX-VM-on-VirtualBox)

• [https://cortx.link/cloudshare-](https://cortx.link/cloudshare-request)

[request](https://cortx.link/cloudshare-request)

Support: [Slack](https://app.slack.com/client/T014PH2TR0W/C01F5NS2820)[ ](https://app.slack.com/client/T014PH2TR0W/C01F5NS2820)#**hackathon-support-and-mentorship**

Seagate

14





CORTX VM

CORTX

RabbitMQ

Elastic

Kibana

…

CSM: tcp/28100

SSH: tcp/22

ens32

Mgmnt

(CSM)

ens33

Data

(S3)

HTTP: tcp/80

HTTPS: tcp/443

OpenLDAP

…

CentOS 7.8

ens34

Private

(Unused)

<https://github.com/Seagate/cortx/blob/main/doc/CORTX_on_Open_Virtual_Appliance.rst>





CORTX CloudShare environment

CloudShare VPC

RDP: tcp/3389

Chrome

S3 client

Win 2019

CORTX

bitMQ

Elastic

Kibana

…

ens33

Data

Mgmnt subnet 192.168.0.0/24

Mgmnt

Data subnet 192.168.2.0/24

OpenLDAP

…

CentOS 7.8

S3: tcp/443,

tcp/80

ens34

Private

(Motr)

subnet 192.168

DHCP server

SSH: tcp/22

S3 client

Ubuntu 20.04





Questions?

Seagate

17

