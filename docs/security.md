---
id: security
title: Security & Compliance
sidebar_label: Security & Compliance
---

CogniAssist follows the strictest guidelines for security and compliance regardless of industry. From personally identifiable customer information to proprietary business data, our Platform allows you to meet strict requirements passed down from local,
state, and federal regulatory and governing bodies.
This section describes the security and compliance methods CogniAssist uses to protect your data in accordance with the highest industry standards. It also describes the features, contained within the Enterprise Admin Console, to take advantage of
built-in data retention policies such as Chat logs, audit logging, and more.


### Encryption 

#### Method
The platform uses the latest AES-256-CBC (cipher block chaining) implementation with 16-byte random initialization vectors
(IVs). The platform provides full encryption of bot messages on the server. All application data at rest in database, Search
Indexes and SAN storage is encrypted. The platform also provides full encryption of all bot messages during transit. The
Platform uses HTTPS over Transit Layer Security (TLS) using AES 256 standard.

#### Encryption Key Management

CogniAssist uses two sets of keys – a master key and enterprise data keys. Each enterprise is assigned a data key. Enterprise
specific data keys are kept encrypted using the master key. The master key is provisioned and stored using HSM backed
Key Management Service. Enterprise data keys are rotated periodically or on demand.
Enterprise administrators can manage data keys from the Admin Console. The administrator also can view the key meta information and rotate the key on demand if required. The newly generated data key will be used to encrypt the data from that
point of time onwards. 


### Authentication Layers

#### SSO
Industry standard SSO solutions are leveraged to grant managed users secure
access to an organization’s enterprise bot store and application using existing
identity providers.


Supported SSO Configurations
* SAML
    * Okta
    * OneLogin
    * Bitium
    * Other (generic SAML identity provider configuration)
* WS-Federation
* Ping Identity
* OpenID Connect

#### Integrated System Authentication
Use basic auth, oauth, or API keys for user authentication before bots can
deliver alerts or take actions against integrated systems.

#### Configurable Password Policy
Define and enable default password strength when Single Sign-On (SSO) is
not used. The Platform includes support for dual-factor authentication. Administrators can create policies with the following properties:
* Minimum length of characters and letters
* Inclusion of at least one numeric value
* Inclusion of at least one letter
* Enforce use of at least one uppercase letter
* Enforce use of at least one lowercase letters
* Inclusion of at least one special character
* Password expiration (between 1 and 365 days)
* Policy applies to existing users or only new users


### Domain Verification
For additional security, the Platform requires that you verify your domain and register your CogniAssist account to your domain
before bots can be used. CogniAssist provides a unique .TXT record to add to your domain settings or <meta> tag for your web
site home page. These tokens let you initiate a domain verification check in the Bots Admin console. After verification, the
Platform provides detailed information related to your domain, such as verification method used, date, and any associated
comments. 



### Compliance
#### Data Retention Policies
The Platform automatically retains user and bot messages for 365 days with buit-in data retention policies. The Enterprise
Admin Console lets you create custom retention policies for each registered domain based on your organization’s unique
requirements for data persistence and compliance.

#### Archiving/ Exporting
CogniAssist lets you extract user-bot conversations from the Platform for archival purposes. The schema definition of the logs
can be extracted from MongoDB and exported into your business records system using SMTP or XML/JSON file-based
integrations.

#### Explainable AI
Our Explainable AI feature lets humans understand the path an IT system took to make a decision.

<!-- #### Log Discovery
CogniAssist provides a Platform that facilitates compliance with federal regulations for HIPAA, PCI, FINRA, and others. The Enterprise Admin Console lets you perform searches for user and bot content, across all deployments, usually for
civil or government investigations. Evidence surfaced by these searches can be retained for any specified duration. Administrators can also provide secure custodian access to on-hold content for internal or external inquiries. -->

#### Profanity Filters
The Platform supports integration with third-party services that provide profanity filters; user utterances can be sent to the
third-party service to be tagged and filtered in real-time (if supported). CogniAssist’s NLP engine also has the ability to identify
profanities.

#### Audit Logs
CogniAssist’s Platform provides full auditing capabilities of all system events. Each logged event provides detailed
information such as date and time stamp of event, category, description, user that initiated the event (when applicable), and
the IP address of the device or channel used to access the bot.

### Security Protocols & Compliance Reporting

#### Rigorous Penetration Testing
CogniAssist servers are regularly scanned for vulnerably and monitored by intrusion detection and file integrity agents. We combine exhaustive internal security practices with third-party penetration audits, run on a periodic basis, to ensure data integrity and security and that industry best practices are consistently followed.

#### Data Center
CogniAssist’s services can be hosted in leading cloud environments such as Azure,AWS. These environments maintains multiple compliance
certifications, including ISO2001, PCI, and SOC. 

* Please visit https://aws.amazon.com/compliance/ for more information on AWS environment.
* Please visit https://docs.microsoft.com/en-us/azure/compliance/ for more information on Azure environment.

<!-- 
#### Service Organization Control Report (SOC)
CogniAssist is SOC2 Type 1 compliant. A report of our most recent audit can be shared on request by support@cogniassist.com. -->