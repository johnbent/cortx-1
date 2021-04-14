# Informational Webinar: CORTX Integration Challenge

# April 14, 2021
Rachel Novak, Justin Woo

CORTX & Integrations

How to set up your VM

How to build an integration

How to submit your integration

<img src="img/Hackathon Webinar I final0.png" width=384px />

* CORTX is\.\.\.​
  * Mass\-capacity object storage system\. But what is an object store?

<img src="img/Hackathon Webinar I final1.png" width=145px />

NASA collects massive amounts of data\, and has petabytes of storage in the form of many\, many\, many disks\.

Storage hardware only provides space\- you need a system for storing\, cataloguing\, retrieving\, updating\, and repairing the data\.

Object storage provides a way to store and manage data on a massive scale

<img src="img/Hackathon Webinar I final2.png" width=500px />

Key Components of object storage:

  * A way to decide _how_ and _where_ to store data on the hardware
  * How to organize the location information of that data\(i\.e\. _metadata_ \- what is this data object and where is it\)
  * A way to ensure that many users can _access_ the same data at the same time _without conflicts_
  * _Monitoring_ the health of the data and the system
  * Mechanisms to recover from failure/errors and to _ensure data isn’t lost_ or corrupted
  * A _management system_ by which admins and users can view the health of the system and configure various behavioral aspects

# Key Components of CORTX

CORTX as a platform is made up of different modules\, each of which handle different functions\.

<img src="img/Hackathon Webinar I final3.png" width=384px />

<img src="img/Hackathon Webinar I final4.png" width=384px />

<img src="img/Hackathon Webinar I final5.png" width=384px />

<img src="img/Hackathon Webinar I final6.png" width=145px />

_MOTR_

Primary data store

Interacts directly with storage devices

Manages data storage and metadata

Rebuilds data after failures\.

_HA & HARE_

Monitor for failures

TellMotrwhat to rebuild

_Manager_

Human\-friendly interface with CORTX

Administrative UI

Web GUI for monitoring & management

_CORTX S3_

Translates betweenMotrand S3

Allows use of S3 API when connecting to other tools and platforms

_What roles do integrations play in object storage?_

<img src="img/Hackathon Webinar I final7.png" width=195px />

NASA wants to analyze the data it has stored on its hardware

It will need to integrate its analytics tools & data collection tools with its data store

An integration connects a tool likePyTorchwith an object store like CORTX

<img src="img/Hackathon Webinar I final8.png" width=384px />

<img src="img/Hackathon Webinar I final9.png" width=500px />

<img src="img/Hackathon Webinar I final10.png" width=384px />

<img src="img/Hackathon Webinar I final11.png" width=145px />

# Selecting an Integration

What data is collected?

What needs to be done with that data?

Identify the tools that would need to connect to the stored data or the storage hardware\.

# CORTX- How to Build an Integration

* Identify the tool you want to integrate with CORTX
* Go to their website and check out their documentation for S3 API _\(_  _Motr_  _integrations are a bit trickier\. If you have questions\, please ask in \#hackathon\-support\-and\-mentorship\)_
* Identify the functions for writing data to the platform \(or other relevant functions\, depending on what you are integrating with\)
* Edit config file or write code to set up your integration
* Test\! Run your integration and make sure the two components \(CORTX and your integration platform\) are correctly connecting
* Document it\!
  * Explain what the tool does\, and how it will work with CORTX\.
  * Ensure you document every step\, including the ones that seem obvious
  * Explain each step and be sure to mention potential failures/errors as well as documenting what success looks like\.

# Submitting your Integration

* A submission to the CORTX Integration Challenge will be considered complete if it contains:
* A functional integration between CORTX and another system\, platform\, or tool\, which is explained and documented in:
  * 1\. A pull request to the CORTX GitHub Repository
  * 2\. A video demonstrating the set up and functionality of the integration\, along with an explanation of its purpose
  * 3\. Documentation in the pull request explaining how to set up and use the integration\.
* The DEADLINE for project submissions inDevpostis _11:00 PM PT \, Tuesday\, April 27th_

* Submission instructions:[https://github\.com/Seagate/cortx/blob/main/doc/integrations/fhir\.md](https://github.com/Seagate/cortx/blob/main/doc/integrations/fhir.md)
* _Step 1:_ Sign\-up or sign\-in to GitHub
* _Step 2:_ Fork the CORTX repository so you can make a pull request\.
* _Step 3:_ In that fork\, open the integration folder and create a \.md Markdown file\. In that file include:
      * The intention behind the integration and what it does\.
      * Installation directions that are clear\, accessible\, and easily reproducible\.
    * A link to your integration video which includes:
      * An explanation of the integration use case \- why/how it is useful or impactful in addition to demonstrating how to set up and run the integration\.
      * Clear and concise directions on how to install the integration
* _Step 4:_ Make a pull request to merge your changes back to the main repository\.
* _Step 5_ : Go toDevpostand submit your integration by posting a link to your pull request\.

# Live Demo - Integration

A good example of an integration\, write up\, and video can be found here:

_[Splunk Integration \(CORTX](https://github.com/Seagate/cortx/blob/main/doc/integrations/splunk.md)_  _[Github](https://github.com/Seagate/cortx/blob/main/doc/integrations/splunk.md)_  _[\)](https://github.com/Seagate/cortx/blob/main/doc/integrations/splunk.md)_

_[Connecting CORTX to Splunk – YouTube](https://www.youtube.com/watch?v=rBAIloua4p0)_

# CORTX- Setting up your VM

There are a few ways you can get a CORTX VM to run…

__Use__  __CloudShare__

To gain access to apre\-configuredCloudShareenvironment\, all you need to do is request access\!

[https://cortx\.link/cloudshare\-request](https://cortx.link/cloudshare-request)

* __Stand up your own VM__
* Requirements
  * Min\. 8GB of RAM
  * A VM application:Vmware\, VirtualBox\, etc\.

* Download _[OVA](https://github.com/Seagate/cortx/releases/download/ova-1.0.3/cortx-va-1.0.3.ova)_ ​
* Set up VM Docs:
  * _[CORTX VM Setup](https://github.com/Seagate/cortx/blob/main/doc/CORTX_on_Open_Virtual_Appliance.rst)_
  * _[Documentation](https://github.com/Seagate/cortx/blob/main/doc/CORTX_on_Open_Virtual_Appliance.rst)_  _[Instructions for VirtualBox](https://github.com/Seagate/cortx/wiki/CORTX-VM-on-VirtualBox)_

Support:[Slack](https://app.slack.com/client/T014PH2TR0W/C01F5NS2820)\# __hackathon\-support\-and\-mentorship__

# CORTX VM

<span style="color:#FFFFFF">CentOS 7\.8</span>

<span style="color:#F7BD15">CSM:</span>  <span style="color:#F7BD15">tcp</span>  <span style="color:#F7BD15">/28100</span>

<span style="color:#F7BD15">SSH:</span>  <span style="color:#F7BD15">tcp</span>  <span style="color:#F7BD15">/22</span>

<span style="color:#FFFFFF">ens32</span>

<span style="color:#FFFFFF">Mgmnt</span>  <span style="color:#FFFFFF">\(CSM\)</span>

<span style="color:#F7BD15">HTTP:</span>  <span style="color:#F7BD15">tcp</span>  <span style="color:#F7BD15">/80</span>

<span style="color:#F7BD15">HTTPS:</span>  <span style="color:#F7BD15">tcp</span>  <span style="color:#F7BD15">/443</span>

<span style="color:#FFFFFF">ens34</span>

<span style="color:#FFFFFF">Private</span>  <span style="color:#FFFFFF">\(Unused\)</span>

[https://github\.com/Seagate/cortx/blob/main/doc/CORTX\_on\_Open\_Virtual\_Appliance\.rst](https://github.com/Seagate/cortx/blob/main/doc/CORTX_on_Open_Virtual_Appliance.rst)

# CORTX CloudShare environment

<img src="img/Hackathon Webinar I final12.png" width=500px />

<img src="img/Hackathon Webinar I final13.png" width=248px />

<span style="color:#FFFFFF">CentOS 7\.8</span>

<span style="color:#FFFFFF">ens32</span>

<span style="color:#FFFFFF">Mgmnt</span>  <span style="color:#FFFFFF">\(CSM\)</span>

<span style="color:#FFFFFF">Mgmnt</span>  <span style="color:#FFFFFF">subnet 192\.168\.0\.0/24</span>

<span style="color:#FFFFFF">Data subnet 192\.168\.2\.0/24</span>

<img src="img/Hackathon Webinar I final14.png" width=248px />

<span style="color:#F7BD15">S3:</span>  <span style="color:#F7BD15">tcp</span>  <span style="color:#F7BD15">/443\,</span>  <span style="color:#F7BD15">tcp</span>  <span style="color:#F7BD15">/80</span>

<span style="color:#FFFFFF">ens34</span>

<span style="color:#FFFFFF">Private</span>  <span style="color:#FFFFFF">\(</span>  <span style="color:#FFFFFF">Motr</span>  <span style="color:#FFFFFF">\)</span>

<span style="color:#FFFFFF">Private subnet 192\.168\.1\.0/24</span>

<img src="img/Hackathon Webinar I final15.png" width=248px />

# Questions?

