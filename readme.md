# Understanding Security Layers

When working in the security field, one of the first acronyms to be encountered in the information security field is CIA or CIA Triangle:

- Confidentiality
- Integrity
- Availability


## Understanding Confidentiality:

Confidentiality, for information security, means keeping information, networks, and systems secure from unauthorized access.

Example related issue: high-profile leaking of people's personal information by several large companies. 

There are several technologies that support confidentiality:

- Strong encryption
- Strong authentication
- Stringent access controls

Another key, determining what information is considered confidential. Common classifications of data are Public, Internal Use Only, Confidential, and Strictly Confidential.

If information is not classified, there are two options - protecting all information as if it were confidential, or treating all information as if it were Public or Internal Use Only.

In a nutshell, strict control of permissions, strong authentication, and encryption are essential for confidentiality.

## Understanding Integrity:

Integrity in the information security context is consistency, accuracy, and validity of data or information. 

Ensuring the integrity of information includes authentication, authorization, and accounting (auditing). 
Examples: rights and permissions, using a hashing function to calculate before and after to show if information has been modified. Auditing or accounting systems can be used that records what changes have been made.

Encryption and digital signatures can assist with integrity. For example, when sending an email you want to make sure the information sent is the same when the user receives it.

## Understanding Availability:

Availability is the third core security principle, and is defined as a characteristic of a resource being accessible to a user, application, or computer system when required.
When a user needs to get information, it is available to them.
Threat to availability usually come in two forms - accidental and deliberate.
Accidental threats would include natural disasters, outages, equipment failures, software issues, and other unplanned system, network, or user issues.
Make sure to have redundancy built in such as backup server or hard drive mirroring. 

## Defining Threat and Risk Management

Threat and risk management is the process of identifying, assessing, and prioritizing threats and risks. A risk is defined as the probability that an event will occur. 
A threat is a specific type of risk, and it is defined as an action or occurrence that could result in a breach in the security, outage, or corruption of a system by exploiting known or unknown vulnerabilities.

After completing an assessment and identifying risks, the next step is to evaluate each risk for two factors. First determine the likelihood that a risk will occur in the environment and then determine the impact of that risk on their environment. 

After evaluating risks, prioritize them. One way to prioritize is to create a risk matrix, which can be used to determine an overall risk ranking. A risk matrix should include the following:

- The risk
- The likelihood that the risk will actually occur
- The impact of the risk
- A total risk score
- The relevant business owner for the risk
- The core security principles that the risk impacts (confidentiality, integrity, and/or availability)
- The appropriate strategy or strategies to deal with the risk

One way to calculate a total risk score is to assign numeric values to the likelihood and impact. For example, rank likelihood and impact on a scale from 1 to 5, where the 1 equals low likelihood or low probability, and 5 equals high likelihood or high impact. Then, multiply the likelihood and the impact together to generate a total risk score.

`Total Risk Score = Likelihood x Impact`

After prioritizing all risks, there are four generally accepted responses to these risks:

- Avoid
- Accept
- Mitigate
- Transfer

Risk avoidance is the process of eliminating a risk by choosing to not engage in an action or activity. 

Risk acceptance is the act of identifying and then making an informed decision to accept the likelihood and impact of a specific risk. 

Risk mitigation consists of taking steps to reduce the likelihood or impact of a risk. 

## Understanding the Principle of Least Privilege

Principle of Least Privilege is a security discipline that requires a user, system, or application be given no more privileges than necessary to perform its function or job. 

Tools to assist with controlling for Least Privilege is a large corporation setting:
-	Groups: Groups can be used to logically group users and applications so that permissions are not applied on a user by user basis or application by application basis.
-	Multiple user accounts for administrators: One of the largest challenges when implementing the Principle of Least Privilege relates to administrators. Administrators are typically also users, and it is seldom a good idea for administrators to perform their daily user tasks as an administrator. To address this issue, many companies will issue their administrators two accounts – one for their role as a user of the company’s applications and systems, and the other for their role as an administrator. 
-	Account standardization: The best way to simplify a complex environment is to standardize on a limited number of account types. Each different account type permitted in an environment adds an order of magnitude to the permissions management strategy. Standardizing on a limited set of account types makes managing the environment much easier.
-	Third-party applications: There are a variety of third-party tools designed to make managing permissions easier. These can range from account lifecycle management applications to auditing applications and application firewalls.
-	Processes and procedures: One of the easiest ways to manage permissions in an environment is to have a solid framework of processes and procedures for managing accounts. With this framework to rely on, the support organization doesn’t have to address each account as a unique circumstance. They can rely on the defined process to determine how an account is created, classified, permissioned, and maintained. 

## Understanding Separation of Duties
Separation of duties is a principle that prevents any single person or entity from being able to have full access or complete all the functions of a crucial or sensitive process. It is designed to prevent fraud, theft, and errors. 
For example, a system administrator might have full access to an application or service, such as a database, but the administrator should not be given access to the security logs. Instead, the security administrators should be responsible for regularly reviewing security logs. 

## Understanding an Attack Surface
The concept of an attack surface with respect to systems, networks, or applications is another idea that has been around for some time. An attack surface consists of the set of methods and avenues an attacker can use to enter a system and potentially cause damage. The larger the attack surface of an environment, the greater the risk of a successful attack. 
In order to determine the attack surface of an environment, its frequently easiest to divide the evaluation into three components: 
-	Application
-	Network
-	Employee
When evaluating the application attack surface, look at things like the following:
-	Amount of code in an application
-	Number of data inputs to an application
-	Number of running services
-	Ports on which the application is listening
When evaluating the network attack surface, consider the following:
-	Overall network design
-	Placement of critical systems
-	Placement and rule sets of firewalls
-	Other security-related network devices like IDS, VPN, and so on
When evaluating the employee attack surface, consider the following:
-	Risk of social engineering
-	Potential for human errors
-	Risk of malicious behavior

## Performing an Attack Surface Analysis
An attack surface analysis helps to identify the attack surface that an organization may be susceptible to. Once completed, the attack surface analysis can be used to determine how to reduce the attack surface. 
When analyzing a network, the first priority is to determine the security boundaries within an organization. As a minimum, **an organization should have an internal network, a DMZ, and the Internet.** 

However, when an organization has multiple sites, or multiple data centers, the organization will also have individual sites, multiple DMZs, and multiple Internet connections. A good place to determine security boundaries is to look at the organization’s network documents. Ensure that the organization has proper documentation, which includes network diagrams.

After determining the security boundaries, the next step is to determine everything that connects at those security boundaries. Typically, this includes routers and firewalls, but it might also include some level-3 switches. Next, look at the security mechanisms used for the routers, firewalls, and switches and any security rules associated with those security mechanisms. 

While network ingress filtering makes internet traffic traceable to its source, egress filtering helps ensure that unauthorized or malicious traffic never leaves the internal network. Inter-workload communications should remain internal; they should not traverse the perimeter. 

Review egress and ingress traffic on regular basis. When examining, look at the source and target addresses as well as the ports used. 
In addition to examining egress and ingress traffic, analyze traffic to and from critical systems or systems that contain confidential information. 

Test to identify open ports, analyze traffic patterns, such as traffic that is encrypted and traffic that is not encrypted. This will help determine which traffic is essential and which traffic could easily be captured. 
To identify application attack services, assess all running network services and applications that communicate with other computers. 

When evaluating servers, review administrative accounts from time to time to ensure that proper access is provided to the right people. 

## Egress vs Ingress

- Ingress – Traffic that originates from outside the network’s routers and proceeds toward a destination inside the network.
-	Egress – Helps ensure that unauthorized or malicious traffic never leaves the internal networks.
-	Egress – Traffic that begins inside a network and proceeds through its routers to its destination somewhere outside of the network.
-	Ingress – Makes internet traffic traceable to its source. 

## Social Engineering
-	True – Social engineering is a method used to gain access to data, systems, or networks, primarily through misrepresentation.
-	False – This technique typically relies on the trusting nature of the person who is attacking.
-	True – The attacker will ask a number or questions in an attempt to identify possible avenues to exploit during this attack.
-	True – These attacks can be perpetrated in person, through email, or via phone. 

# Understanding Physical Security as the First Line of Defense
There are a number of factors that need to be considered when designing, implementing, or reviewing physical security measures taken to protect assets, systems, networks, and information. They include understanding site security and computer security, securing removable devices and drives, access control, mobile device security, disabling the Log on Locally capability, and identifying and removing keyloggers.

```Remember that if someone can get physical access to a server where confidential data is stored, they can, with the right tools and enough time, bypass any security that the server may use to protect the data.```

Securing a physical site is more than just putting a lock on the front door and making sure the door is locked.

## Understanding Site Security

**Understanding Access Control**
Access control is a key concept when thinking about physical security. In the context of physical security, access control can be defined as the process of restricting access to a resource to only permitted users, applications, or computer systems. 

One of the fundamental concepts used when designing a security environment is the concept of defense in depth. Defense in depth is a concept in which multiple layers of security are used to defend assets. This ensures that if an attacker breaches one layer of defenses, there are additional layers of defense to keep them out of the critical areas.

There are several goals to keep in mind when designing a physical security plan:
-	Authentication: Site security addresses the need to identify and authenticate people permitted access to an area.
-	Access Control: Once a person’s identify has been proven and they have been authenticated, site security determines what areas they can access.
-	Auding: Site security also provides the ability to audit activities within the facility. This can be done through reviewing camera footage, badge reader logs, visitor registration logs, or other mechanisms. 
For the purposes of the lesson, we will break the physical premises into three logical areas:
-	The external perimeter, which makes up the outermost portion of the location. This typically includes the driveways, parking lots, and any green space the location may support. This does not include public roads.
-	The internal perimeter, which consists of any buildings on the premises. If the location supports multiple tenants, the internal perimeter is restricted to only the buildings that an employee can occupy.
-	Secure areas, which are locations within the building that have additional access restrictions and/or security measures in place. These can include data centers, network rooms, wiring closets. Or departments like Research and Development or Human Resources. 

## Understanding External Perimeter Security
Common security measures:
-	Security cameras
-	Parking lot lights
-	Perimeter fence
-	Gate with guard
-	Gate with access badge reader
-	Guard patrols

```Test an organization’s camera playback capabilities regularly. Because cameras are almost always used to review events after the face, ensure that the system is successfully recording the data.```

## Understanding the Internal Perimeter
Security features that can be used to secure the internal perimeter include the following:
-	Locks (exterior doors, internal doors, office doors, desks, filing cabinets, etc)
-	Keypads
-	Security cameras
-	Badge readers (on doors and elevators)
-	Guard desk
-	Guard patrols
-	Smoke detectors
-	Turnstiles
-	Mantraps (device that control access, such as double-doors)

These are all physical requirements for the Principle of Least Privilege.

## Defining Secure Areas
Secure area security technologies include:
-	Badge readers
-	Keypads
-	Biometric technology
-	Security doors
-	X-ray scanners
-	Metal detectors
-	Cameras
-	Intrusion detection systems (light beam, infrared, microwave, ultrasonic)

## Understanding Site Security Processes
In the external perimeter, this might include processes to manage entry to the parking lot through a gate, or a process for how often the guards will do a tour of parking lots. Include in those processes should be how to document findings, track entry and exits, and how to respond to incidents.

In the internal perimeter, processes might include guest sign-in procedures, equipment removal procedures, guard rotation procedures, or details on when the front door is to be left unlocked. In addition, there should be processes to handle deliveries, how/when to escort visitors in the facility, and even what types of equipment may be brought into the building. 

```Cameras are available on virtually every cell phone. To ensure that cameras are not used in a facility, plan on taking phones at the door, or disabling the camera function.```

Reminder, when discussing multiple layers of security, this is called **Defense in Depth**.

## Understanding Computer Security
Computer security consists of the processes, procedures, policies, and technologies used to protect computer systems.

Before we start discussing the tools, we need to differentiate between the three types of computers we will discuss:
-	Servers: These are computers used to run centralized applications and deliver the applications across  a network.
-	Desktop computers: These computers are usually found in office environments, schools, and homes.
-	Mobile computers: This category includes laptop, notebook, tablet, netbook computers, and smartphones. 

If a data center or computer room is not available, other options for securing sever computers include:
-	Computer security cable: A cable that is attached to the computer and to a piece of furniture or wall.
-	Computer security cabinet/rack: A storage container that is secured with a locking door.

## Understanding Mobile Device Security
Mobile devices are one of the largest challenges facing many security professionals today. Mobile devices like laptops, PDAs (personal digital assistants), and smartphones are used to process information, send and receive mail, store enormous amounts of data, surf the internet, and interact remotely with internal networks and systems.

Technologies for physically securing mobile devices:
-	Docking station: Virtually all laptop docking stations are equipped with security features to secure a laptop. This can be with a key, a padlock, or both depending on the vendor and model.
-	Laptop security cables: Used in conjunction with the USS (Universal Security Slot), these cables attach to the laptop and can be wrapped around a secure object like a piece of furniture. 
-	Laptop safe: A steel safe specifically designed to hold a laptop and be secured to a wall or piece of furniture.
-	Theft recovery software: An application running on the computer that enables the tracking of a stolen computer so it can be recovered.
-	Laptop alarm: A motion-sensitive alarm that sounds in the event a laptop is moved.

Best practices:
-	Keep your equipment with you
-	Use the trunk
-	Use the safe

## Using Removable Devices and Drives
A removable device or drive is a storage device which is designed to be removed from the computer without turning the computer off. 

There are three basic categories of security issues associated with removable storage:
-	Loss
-	Theft
-	Espionage

```Some environments address the issues associated with removable storage by using hardware or software configurations to prohibit their use.```

```Encryption is frequently used to secure the data on removeable drives.```

```Block USB or CD/DVD drives to prevent data loss or theft.```

# Performing Thread Modeling

Threat modeling is a procedure for optimizing network security by identifying vulnerabilities, identifying their risks, and defining countermeasures to prevent or mitigate the effects of the threats to the system,

The steps to perform thread modeling are:
-	Identify assets: Identify the valuable assets that the system must protect.
-	Create an architecture overview: Gather simple diagrams and related information that show how the systems are connected, both physically and logically. Documentation should include a system, trust boundaries, and data flow.
-	Decompose the security components and applications: Break down the architecture of the systems and application, including the underlying network and host infrastructure design, security profiles, implementation, as well as the deployment configuration of the systems and applications.
-	Identify the threats: By examining the current architecture, system, applications, and potential vulnerabilities, identify the threats that could affect the systems and applications.
-	Document the threats: Document each threat using a common threat template that shows the attributes of each threat.
-	Rate the threats: Prioritize and address the most significant threats first. The rating process weighs the probability of the threat against the damage that could result should an attack occur. Certain threats might not warrant any action when comparing the risk posed by the threat with the resulting mitigation costs.

## STRIDE
STRIDE is an acronym for a threat modeling system that originated at Microsoft. STRIDE is also a mnemonic tool for security threats; it consists of six different categories:
NAME [security properties that can reduce stride risk] – description

-	Spoofing [authentication] – Something or someone that pretends to be something they are not.
-	Tampering [integrity] – Attackers modify or interfere with legitimate data.
-	Repudiation [confirmation] – The user denies performing a certain action, which could be illegal and harmful.
-	Information Disclosure [confidentiality] – A data breach and access to private information occurs and too much information about a system and its data is accessed by unauthorized individuals.
-	Denial of Service [availability] – A service is brought down intentionally or unintentionally resulting in disruptions of applications or services.
-	Elevation of Privilege [authorization] – A user gains privilege access greater than that for which he was approved, potentially accessing restricted data or performing restricted tasks. 
## DREAD
Use DREAD to measure and rank the threats risk level:
-	Damage potential: How much damage can be inflicted on our system?
-	Reproducibility: Can the attack be reproduced easily?
-	Exploitability: How much effort and experience are necessary?
-	Affected users: If the attack occurs, how many users will be affected?
-	Discoverability: Can the threat be easily discovered?

```Rank the threat level on a scale of 0 through 3 or 0 through 10, where the larger the number indicates the greater the threat.```

# Knowledge Check:
**Steps to perform threat modeling:**
-	Identify assets.
-	Create an architecture overview.
-	Decompose the security components and applications.
-	Identify the threats.
-	Document the threats.
-	Rate the threats.

# Review
-	Access Control – The process of restricting access to a resource to only permitted users, applications, or computer systems.
-	Attack Surface – The exposure, the reachable and exploitable vulnerabilities that a system or technology has.
-	Attack Surface Analysis – Helps to identify the attack surface that an organization may be susceptible to.
-	Availability – Describes a resource being accessible to a user, application, or computer system when required. In other words, availability means that when a user needs to get information, he or she has the ability to do so.
-	Confidentiality – The characteristic of a resource ensuring access is restricted to only permitted users, applications, or computer systems. 
-	Defense in Depth – Uses multiple layers of security to defend your assets.
-	DREAD – An acronym that stands for Damage potential: How much damage can be inflicted on our system? Reproducibility: Can the attack be reproduced easily? Exploitability: How much effort and experience are necessary? Affected users: If the attack occurs, how many users will be affected? Discoverability: How easy is it to discover the threat?
-	Egress Traffic – Network traffic that begins inside a network and proceeds through its routers to its destination somewhere outside the network.
-	Flash Drive – A small drive based on flash memory.
-	Ingress Traffic – Traffic that originates from outside the network’s routers and proceeds toward a destination inside the network.
-	Integrity – The consistency, accuracy, and validity off data or information. One of the goals of a successful information security program is to ensure that data is protected against any unauthorized or accidental changes.
-	Mobile Devices – Small devices that are used to process information, send and receive mail, store enormous amounts of data, surf the internet, and interact remotely with internal networks and systems. They include laptops, PDAs, and smartphones. 
-	Principle of Least Privilege – A security discipline that requires that a particular user, system, or application be given no more privilege than necessary to perform its function or job.
-	Removeable Device – A storage device that is designed to be taken out of a computer without turning the computer off.
-	Residual Risk – The risk that remains after measures have been taken to reduce the likelihood or minimize the effect of a particular event.
-	Risk – The probability that an event will occur.
-	Risk Acceptance – The act of identifying and then making an informed decision to accept the likelihood and impact of a specific risk.
-	Risk Assessment – Identifies the risks that might impact your particular environment.
-	Risk Avoidance – The process of eliminating risk by choosing not to engage in an action or activity.
-	Risk Management – The process of identifying, assessing, and prioritizing threats and risks.
-	Risk Mitigation – Taking steps to reduce the likelihood or impact of a risk.
-	Risk Register – Provides a formal mechanism for documenting the risks, impacts, controls, and other information required by the risk management program.
-	Risk Transfer – The act of taking steps to move responsibility for a risk to a third party through insurance or outsourcing.
-	Social Engineering – A method used to gain access to data, systems, or networks, primarily through misrepresentation. This technique typically relies on the trust natures of the person being attacked.
-	STRIDE – A mnemonic tool for security threats; it consists of six different categories: Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege.
-	Threat – An action or occurrence that could result in the breach, outage, or corruption of a system by exploiting known or unknown vulnerabilities.
-	Threat and Risk Management – The process of identifying, assessing, and prioritizing threats and risks.
-	Threat Modeling – A procedure for optimizing network security by identifying vulnerabilities, identifying their risks, and defining countermeasures to prevent or mitigate the effects of the threats to the system.
-	Keylogger – A software or hardware device that captures passwords and other critical data directly from the keyboard. 

# Understanding Authentication, Authorization, and Account

## Starting Security with Authentication
In the realm of IT security, the AAA (Authentication, Authorization, and Accounting) acronym is a model for access control.
-	Authentication is the process of identifying an individual, usually based on a user name and password.
-	Authorization is the process of giving individuals access to system objects based on their identity.
-	Accounting, also known as auditing, is the process of keeping track of a user’s activity while accessing the network resources, including the amount of time spent in the network, the services accessed while there, and the amount of data transferred during the session.
-	Nonrepudiation prevents one party from denying actions they carry out. If proper authentication, authorization, and accounting have been established, a person cannot deny their own actions. 

A logon is the process whereby a user is recognized by a computer system or network so that they can begin a session. A user can authenticate using one or more of the following methods:
-	What a user knows, such as a password or personal identification number (PIN).
-	What a user owns or possesses, such as a passport, smart card, or ID card.
-	Who a user is, based on biometric factors such as fingerprints, retinal scans, voice input, or other forms. 

When two or more authentication methods are used to authenticate someone, a multifactor authentication system is being implemented. A system that uses two authentication methods such as smart cards and a password can be referred to as two-factor authentication.

Review:
-	Multi-factor authentication systems are when two or more authentications methods (what a user knows, what a user owns, and who a user is) are being implemented.
-	Two-factor authentication is a system in which two authentication methods are being used.

## Authentication Based on What a User Knows
The most common method of authentication with computers and networks is the password. A password is a secret series of characters that enables a user to access a file, computer, or program. 

Hackers will try to crack passwords by first trying obvious passwords, including name of spouse or children, birthdays, etc. Then they will try common passwords. The hackers will try brute force attacks, which consist of trying as many combinations of characters as time and money permit.

A subnet of the brute force attack is the dictionary attack, in which all words in one or more dictionaries are tested. Lists of common passwords are also typically tested. This is why its important to have lengthy and strong complex passwords with at least 14 characters in length.

However, for some people, remembering long passwords is cumbersome, so they may start writing their passwords on a piece of paper near their desk. In these situations, you should start looking for other forms of authentication, such as a smart card or biometrics.

Passwords should be changed regularly. Password policies should be in place to enforce minimum number of characters, specify if the password is a complex password, state how often a user can reuse a password, and so on.

Passwords might be the easiest and most popular authentication method, but they also have significant disadvantages because they can be stolen, spoofed, forgotten, and so on. For example, a hacker might call the IT department pretending to be someone else and have the department reset the password for the hacker. Therefore, establishing secure processes to reset passwords for users is critical.

When resetting passwords, there must be a method to identify the user asking for a password to be changed. Do not send the password through email – meeting with he person and asking for identification is a possible solution. Another solution would be to call back and leave the password on a person’s voice mail, so that a user will need to provide a PIN to access, or the password could be sent to a user’s manager or administrative assistant. 

One method of establishing a self-service password service is where a user’s identity is verified by asking questions and comparing the answers to previously stored responses, such as a person’s birthday, name of their favorite movie, name of a pet, and so on. However, these can be relatively easily guessed by an attacker, discovered through low-effort research. 

## Using a Personal Identification Number (PIN)
A personal identification number (PIN) is a secret numeric password shared between a user and a system that can be used to authenticate the user to the system. Because it only consists of digits and is relatively short (usually four digits), it is used for relatively low security scenarios like gaining access to the system or in combination with another method of authentication.

## Authentication Based on What a User Owns or Possesses
Another type of authentication is based on what a user owns or possesses. The most common examples are the digital certificate, smart card, and security token.

The digital certificate is an electronic document that contains an identity such as a user or organization and a corresponding public key. Think of a digital certificate as a drivers license or passport that contains a user’s photograph and thumbprint, so that there is no doubt about the user’s identity.

A smart card is a pocket-sized card with embedded integrated circuits consisting of non-volatile memory storage components, and perhaps, dedicated security logic. Non-volatile memory is memory that does not forget its contents when power is discontinued. Smart cards can contain digital certificates to prove the identity of someone carrying the card and may also contain permissions and access information.

Because a smart card can be stolen, some smart cards will not have any markings on them, so that they cannot be easily identified as to what they can open. In addition, many organizations will use a password or PIN in combination with the smart card.

A Security Token (or sometimes a hardware token, hard token, authentication token, USB token, cryptographic token, or key fob) is a physical device that an authorized user of computer services is given to ease authentication. Hardware tokens are typically small enough to be carried in a pocket and are often designed to attach to a user’s keychain. Some of these security tokens include a USB connector, RFID functions, or Bluetooth wireless interface to enable transfer of a generated key number sequence to a client system.

Some security tokens may also include additional technology such as a static password or digital certificate built into the security token, much like a smart card. Other security tokens may automatically generate a second code that will have to be entered to get authenticated.

## Devices Only Running Trusted Applications
The process involves protecting systems with software which only allows the user of applications which the administrators have approved.

This is by far the STRONGEST option.

A common tool used in Windows, is called Device Guard.
Device Guard uses code integrity policies to lock devices so that they can only run trusted apps. Code integrity checks can be isolated from the Windows kernel. This can mitigate the risk of possible malicious code attacks.

## Authentication Based on a User’s Physical Traits
Biometrics is an authentication method that identifies and recognizes people based on voice recognition or a physical trait such as a fingerprint, face recognition, iris recognition, or retina scan. Many mobile computer include a fingerprint scanner, and it is relatively easy to install biometric devices at doors and cabinets to ensure that only authorized people will enter a secure area.

When selecting a biometric method, consider its performance, difficulty, reliability, acceptance, and cost. In addition, look at the following issues:
-	False rejection rate (false negative): Authorized users who are incorrectly denied access.
-	False acceptance rate (false positive): Unauthorized users who are incorrectly granted access.

## Introducing RADIUS and TACACS+
Remote Authentication Dial-In User Service (RADIUS) and Terminal Access Controller Access-Control System Plus (TACACS+) are two protocols that provide centralized authentication, authorization, and accounting management for computers to connect to and use a network service. 

The RADIUS or TACACS+ server resides on a remote system and responds to queries from clients such as VPN clients, wireless access points, routers, and switches. The server then authenticates a user name/password combination (authentication), determines if a user can connect to the client (authorization), and logs the connection (accounting).

RADIUS is a mechanism that allows authentication of dial-in and other network connections including modem dial-up, wireless access points, VPNs, and web servers. RADIUS has been implemented by most of the major operating systems, including Windows.

In Windows Server 2008, Network Policy Server (NPS) can be used as a Remote Authentication Dial-In User Service (RADIUS) server to perform authentication, authorization, and accounting for RADIUS clients. It can be configured to use Microsoft Windows NT Server 4.0 domain, an Active Directory Domain Services (ADDS) domain, or the local Security Accounts Manager (SAM) user accounts database to authenticate user credentials for connection attempts. 

Another competing centralized AAA server is TACACS+, which was developed by Cisco. When designing TACACS+, Cisco incorporated much of the existing functionality of RADIUS and extended it to meet their needs. From a feature viewpoint, TACACS+ can be considered an extension of RADIUS.

## Running Programs as an Administrator (runas)
Because administrators have full access to a computer or network, it is recommended that a standard non-administrator user should perform most tasks, such as reading reports and sending email. Then, to perform administrative tasks, use the `runas` command or built-in options that are included with Windows operating system.

An example of using the runas command to run the widget.exe as the admin account:
```
runas /user:admin /widget.exe
```

# Knowledge Check:
True or false:

- The Radius or TACACS+ server resides on a remote system and responds to queries from servers.
- RADIUS is a mechanism that allows authentication of dial-in and other network connections.
- From a feature viewpoint, RADIUS can be considered an extension of TACACS+.
- TACACS+ stands for Terminal Access Controller Access-Control System Plus.

Answers:
F T F T 

## Introducing Directory Services with Active Directory
A directory service stores, organizes, and provides access to information in a directory. It is used for locating, managing, and administering common items and network resources, such as volumes, folders, files, printers, users, groups, devices, telephone numbers, and other objects.

Active Directory is a technology created by Microsoft that provides a variety of network services, including the following:
-	Lightweight Directory Access Protocol (LDAP)
-	Kerberos-based and single sign-on authentication
-	Directory services, including DNS-based naming
-	Central location for network administration and delegation of authority

The Lightweight Directory Access Protocol (LDAP) is an application protocol for querying and modifying data using directory services running over TCP/IP. Within the directory, the set of objects is organized in a logical hierarchical manner so that the objects can easily be located and managed. 

The structure can reflect geographical or organizational boundaries, although it tends to use DNS names for structuring the topmost levels of the hierarchy. Deeper inside the directory might appear entries representing people, organizational units, printers, documents, groups of people, or anything else that represents a given tree entry (or multiple entries). LDAP uses TCP port 389. 

Kerberos is the default computer network authentication protocol, which allows hosts to prove their identity over a non-secure network in a secure manner. It can also provide mutual authentication so that both the user and server verify each other’s identity. To make it secure, Kerberos protocol messages are protected against eavesdropping and replay attacks.

Single Sign-On (SSO) allows a user to log on once and access multiple, related, but independent software systems without having to log on again. When a user logs on with Windows using Active Directory, the user is assigned a token, which can then be used to sign on to other systems automatically.

Lastly, Active Directory provides directory services that allow you to organize and name all of the network resources, including users, groups, printers, computers, and other objects, so that passwords, permissions, rights, and so on, can be assigned to the identity that needs them. Active Directory is closely tied to DNS. Anything that is centrally managed on a network is managed through Active Directory.

Kerberos: Default network authentication protocol (NTLM is a backup) for Active Directory. 

## Understanding Domain Controllers
A domain controller is a Windows server that stores a replica of the account a security information of the domain and defines the domain boundaries.

After a computer has been promoted to a domain controller, there will be several MMC snap-in consoles available to manage Active Directory. These include:
-	Active Directory Users and Computers: Used to manage users, groups, computers, and organizational units.
-	Active Directory Domains and Trusts: Used to administer domain trusts, domain and forest functional levels, and user principal name (UPN) suffixes.
-	Active Directory Sites and Services: Used to administer the replication of directory data among all sites in an Active Directory Domain Services (AD DS) forest.
-	Active Directory Administrative Cetner: Used to administer and publish information in the directory, including managing users, groups, computers, domains, domain controllers, and organizational units.
-	Group Policy Management Console (GPMC): Provides a single administrative tool for managing Group Policy across the enterprise.

Active Directory uses multimaster replication, which means that there is no master domain controller, commonly referred to a primary domain controller, as was found on Windows NT domains. However, because there are certain functions that can only be handled by one domain controller at a time, domain controllers can take on separate roles. 

One role is the PDC Emulator, which provides backwards compatibility for NT4 clients and is becoming very uncommon. However, it also acts as the primary domain controller for password changes and acts as the master time server within the domain.

A server that is not running as a domain controller is known as a member server. To demore a domain controller to member server, run the dcpromo program again.

## Understanding NTLM
While Kerberos is the default authentication protocol for today’s domain computers, NT LAN Manager (NTLM) is the default authentication protocol for Windows NT stand-alone computers that are not part of a domain, or when authenticating to a server using an IP address. It also acts as a fallback authentication if it cannot complete Kerberos authentication, such as when blocked by a firewall. 

NTLM uses a challenge-response mechanism for authentication, in which clients are able to prove their identities without sending a password to the server. After a random 8-byte challenge message is sent to the client from the server, the client uses the user’s password as a key to generate a response back to the server using an MD4/MD5 hashing algorithm and DES encryption. 

## Understanding Kerberos
With Kerberos, security and authentication is based on secret key technology, where every host on the network has its own secret key. The Key Distribution Center maintains a database of secret keys.

When a user logs on, the client transmits the user name to the authentication server, along with the identity of the service the user desires to connect to, such as a file server. The authentication server constructs a ticket, which randomly generates a key that is encrypted with a file server’s secret key, and sends it to the client as part of its credentials, which includes the session key encrypted with the client’s key. If the user enters the correct password, then the client can decrypt the session key, present the ticket to the file server, and use the shared secret session key to communicate between them. Tickets are time stamped, and typically have an expiration time of only a few hours.

For all this to work to ensure security, the domain controllers and clients must have the same time. Kerberos authentication will work if the time interval between the relevant computers is within the maximum enabled time skew. The default setting is five minutes. Another option is to turn off the Time Service tool and then install a  third-party time service. 

## Using Organization Unites
To help organize objects within a domain and minimize the number of domains, use organizational units, commonly expressed as OUs. OUs can be used to hold users, groups, computers, and other organizational units. 

Containers are objects that can store or hold other objects. They include the forest, tree, domain, and organizational unit. To help manage objects, delegate authority to a container, particularly an organizational unit.

For example, let’s say that a domain is divided by physical location. Assign a site administrator authoritative control to the OU that represents the physical location. The user will only have administrative controls to the objects within the OU. 

Similar to NTFS and the registry, permissions can be assigned to users and groups over an Active Directory object. However, control would normally be delegated to the user or group. 

Delegate administrative control to any level of a domain tree by creating organizational unites within a domain and delegating administrative control for specific organizational units to particular users or groups. 

Delegate control of organization units to users that better understand that department. You can delegate control to users or groups and modify what permissions are being delegated.

## Understanding Objects
A object is a distinct, named set of attributes or characteristics that represent a network resource. Common objects used with Active Directory are computers, users, groups, and printers. Attributes have values that define the specific object. For example, a user could have the first name John, the last name Smith, and the logon name as jsmith, all of which identity the user. 

Active Directory object are assigned a 128-bit unique number called a security identifier (SID), sometimes referred to as globally unique identifier (GUID) to uniquely identify an object. If a user changes his name, you can change the name and he will still be able to access all objects and have all the same rights as before because they are assigned to the GUID. 

GUIDs also provide some security where, if a user is deleted, a new user account cannot be created with the same user name and expect to have access to all of the objects and all of the rights that the previous user had. 

## Users
A user account enables a user to log on to a computer and domain. As a result, it can be used to prove the identity of a user, which can then be used to determine what kind of access that user will have (authorization). 

On today’s Windows networks, there are two types of user accounts:
-	The local user account
-	The domain user account

A user account allows a user to log on and gain access to the computer where the account was created. The local user account is stored in the Security Account Manager (SAM) database on the local computer. The only computer that does not have a SAM database is the domain controller. 

A domain user is an account that is stored on the domain controller and allows the user to gain access to resources within the domain, assuming they have been granted permissions to access those objects. Like the computer local administrator account, the domain computer local administrator user account is the only account that is created and enabled by default in Windows when a domain is first created. 

When creating a domain user account, supply a first name, last name, and a user’s logon name. The user’s logon name must be unique within the domain. After the user account is created, open the user account properties and configure a person’s user name, logon hours, which computers a user can log on to, telephone numbers and addresses, what groups the person is a member of, and so on. 

## Comptuer
Like user accounts, Windows computer accounts provide a means for authenticating and auditing the computer’s access to a Windows network and its access to domain resources. Each Windows computer to which you want to grant access to resources must have a unique computer account. 

## Using Groups
A group is a collection or list of user accounts or computer accounts. Different from a container, the group does not store the user or computer, it just lists them. The advantage of using groups is to simplify administration, especially when assigning rights and permissions. 

## Group Types
In Windows Active Directory, there are two types of groups – security and distribution. The security group is used to assign rights and permissions and gain access to a network resource. It can also be used as distribution group. A distribution group is only for non-security functions such as email distribution and cannot be assigned rights and permissions to any resource. 

## Group Scopes
-	Domain local group: Contain global groups and universal groups and can contain user accounts and other domain local groups. It is usually in the domain where the intended resources are located.
-	Global group: Designed to contain user accounts. Global groups can contain user accounts and other global groups. Global groups are designed to be “global” for the domain. After placing user accounts into global groups, the global groups are typically placed into domain local groups or local groups.
-	Universal group: This group scope is designed to contain global groups from multiple domains. Universal groups can contain global groups, other universal groups, and user accounts. Because global catalogs replicate universal group membership, limit the membership to global groups. This way if a member within a global group is changed, the global catalog will not have to replicate the change. 

When assigning rights and permissions, always try to group the users and assign the rights and permissions to the group instead of the individual users. To effectively manage the use of groups when assigning access to a network resource using global groups and domain local groups, remember AGDLP (Accounts, Global, Domain Local, Permissions):
-	Add the user accounts (A) into the global group (G) in its domain where the user exists.
-	Add the global group (G) from the user domain into the domain local group (DL) in the resource domain.
-	Assign permissions (P) on the resource to the domain local group (DL) in its domain.
If you are using a universal group, the mnemonic is expanded to AGUDLP:
-	Add the user account (A) into the global group (G) in its domain where the user exists.
-	Add the global groups (G) from the user domain into the universal group (U).
-	Add universal group (U) to the domain local group (DL).
-	Assign permissions (P) on the resource to the domain local group (DL) in its domain.

## Build-in Groups
Like the administrator and guest accounts, Windows has default groups called build-in groups. Some of the built-in groups include:
-	Domain Admins: can perform administrative tasks on any computer within the domain. The default, the Administrator account, is a member.
-	Domain Users: Windows automatically adds each new domain user account to the Domain Users group.
-	Account Operators: Can create, delete, and modify user accounts and groups.
-	Backup Operators: Can backup and restore all domain controllers by using Windows Backup.
-	Authenticated Users: Includes all users with a valid user account on the computer or in Active Directory.
-	Everyone: All users who access the computer with a valid user account. 

## Understanding Web Server Authentication
When authenticating to a web server, Microsoft’s Internet Information Serer (IIS) provides a variety of authentication schemes:
-	Anonymous (enabled by default): Anonymous authentication gives users access to the website without prompting them for a user name or password. Instead, IIS uses a special Windows user account called IUSR_machinename for access. By default, IIS controls the password for this account. 
-	Basic: Basic authentication prompts the user for a user name and password. However, while the user name and password is sent as Base64 encoding, it is basically sent in plain text. If it is necessary to encrypt the user name and password while using basic authentication, use digital certificates so that it is encrypted with https. 
-	Digest: Digest authentication is a challenge/response mechanism, which sends a digest or hash using the password as the key instead of sending the password over the network.
-	Integrated Windows authentication: Integrated Windows authentication (formerly known as NTLM authentication and Windows NT Challenge/Response authentication) can use either NTLM or Kerberos V5 authentication.
-	Client Certificate Mapping: Uses a digital certificate that contains information about an entity and the entity’s public key, which is used for authentication. 

# Knowledge Check:
Group Scope:
-	Universal: Designed to contain global groups from multiple domains.
-	Global: Designed to contain user accounts and can contain user accounts and other groups.
-	Domain Local: Usually in the domain where the intended resources are located. 

Indicate if each of the given statements about organizational unit (OU) are true or false:
-	It is used to organize objects within a domain and minimize the number of domains.
-	It can only contain objects that are located in different domain.
-	It is used to hold users, groups, computers, and other organizational units.
-	There are restrictions on the number of nested OUs.

TFTF

Service:
-	LDAP: An application protocol for querying and modifying data using directory services running over TCP/IP
-	Kerberos: The default computer network authentication protocol, which allows hosts to prove their identity over a non-secure network in a secure manner
-	SSO: Allows a user to log on once and access multiple, related, but independent software systems without having to log on again
-	Directory Service: Allows organization and naming of all network resources so that passwords, permissions, rights can be assigned to the identity that need them

# Comparing Rights and Permissions
A right authorizes a user to perform certain actions on a computer, such as logging on to a system interactively, or backing up files and directories on a system. 

A permission defines the type of access that is granted to an object (an object can be identified with a security identifier) or object attribute. The most common objects assigned permissions are NTFS files and folders, printers, and Active Directory objects. 

To keep track of which user can access an object and what the user can do with that object, refer to the access control list (ACL).


# Understanding NTFS
The file system is a method of storing and organizing computer files and the data they contain to make it easy to find and access them. It also maintains the physical location of the files so that the files can be found and accessed in the future. 

NTFS is the preferred file system because it supports large volumes up to 16 exabytes (EB) and long file names. In addition, it is more fault tolerant than previous file systems used in Windows, because it is journaling file system.

## Using NTFS Permissions

NTFS permissions allow you to control which users and groups can gain access to files and folders on an NTFS volume.

NTFS Standard permissions:
-	Full control: Read, write, modify, and execute files in the folder.
-	Modify: Read, write, modify, and execute files in the folder.
-	Read & Execute: Display the folder contents.
-	List Folder Contents: Display the folder’s contents.
-	Read: Display the file’s data, attributes, owner, and permissions.
-	Write: Write to the file, append to the file, and read or change its attributes.

To simplify administration, it is recommended to grant permissions using groups.

## Understanding Effective NTFS Permissions
There are two types of permissions used in NTFS:
-	Explicit permission: Permissions granted directly to the file or folder.
-	Inherited permission: Permissions granted to a folder (parent object or container) that flow into child objects (subfolders or files inside the parent folder)

When assigning permissions to a folder, by default the permissions apply to the folder being assigned and the subfolders and files of the folder. To stop permission from being inherited, select the “Replace all existing inheritable permissions on all descendants with inheritable permissions from this object.”

# Knowledge Check

-	Modify: Read, write, change, and execute files in the folder; and change attributes of the folder or files within.
-	Read & Execute: Display the folder’s contents; display the data, attributes, owner, and permissions for files within the folder; and run files within the folder.
-	Read: Display the file’s data, attributes, owner, and permissions.
-	List Folder Contents: Display the folder’s contents; display the data, attributes, owner, and permissions for files within the folder.

# Sharing Drives and Folders
The share permissions that are available are:
-	Full Control: Users allowed this permission have Read and Change permissions, as well as the additional capabilities to change file and folder permissions and take ownership of files and folders.
-	Change: Users allowed this permission have Read permissions and the additional capability to create files and subfolders, modify files, change attributes on files and subfolders, and delete files and subfolders.
-	Read: Users with this permission can view file and subfolder names, access the subfolders of the share, read file data and attributes, and run program files.

If you do both a share and a give out file system permissions using the Security tab, the most restrictive permission wins.

An administrative share is a shared folder typically used for administrative purposes. To make a shared folder or drive into a hidden share, the share name must have a $ at the end of it. Because the share folder or drive cannot be seen during browsing, use a UNC name which will include the share name and the training ‘$’. By default, all volumes with the drive letters automatically have administrative shares (C$, D$, E$, and so on).

In addition to the administrative shares for each drive, the following special shares are also available:
-	ADMIN$: A resource used by the system during remote administration of a computer. The path of this resource is always the path to the Windows 0 systems root.
-	IPC$: A resource sharing the named pipes that are essential for communication between programs.
-	PRINT$: A resource used during remote administration of printers.

# Knowledge Check
Steps to share a folder:
-	Right click the drive or folder, choose Properties, click the Advanced Sharing button.
-	Select the Share this folder check box.
-	In the Advanced Sharing dialog box, in the Share name text box, type the name of the shared folder.
-	If necessary, specify the maximum number of people that can access the shared folder at the same time and click the Permissions button.
-	By default, Everyone is given Allow Read permission. If you don’t want everyone to access the folder, remove Everyone and assign additional permissions or add additional people.
-	After the users and groups have been added with the proper permissions, close all the windows.

# Introducing the Registry
The registry is a central, secure database in which Windows stores all hardware configuration information, software configuration information, and system security policies. 

The registry is split into several logical sections, often referred to as hives, which are generally named by their Windows API definitions. The hives begin with HKEY are often abbreviated to a three- or four-letter short name starting with HK. For example, HKCU refers to HKEY_CURRENT_USER and HKLM refers to HKEY_LOCAL_MACHINE. Windows 10 have five root keys/HKEYs:
-	HKEY_CLASSES_ROOT: Stores information about registered applications, such as file association that tells which default program opens a file with certain extension.
-	HKEY_CURRENT_USER: Stores settings that are specific to the currently logged-on user. When a user logs off, the HKEY_CURRENT_USER is saved to HKEY_USERS.
-	HKEY_LOCAL_MACHINE: Stores settings that are specific to the local computer.
-	HKEY_USERS: Contains subkeys corresponding to the HKEY_CURRENT_USER keys for each user profile actively loaded on the machine.
-	HKEY_CURRENT_CONFIG: Contains information gathered at runtime. Information stored in this key is not permanently stored on disk, but rather regenerated at the boot time.

# Using Encryption to Protect Data
Encryption is the process of converting data into a format that cannot be read by another user. Once a user has encrypted a file, it automatically remains encrypted when the file is stored on disk. Decryption is the process of converting data from encrypted format back to its original format.

A key, which can be thought of as a password, is applied mathematically to plain text to provide cipher or encrypted text. A different key produces a different encrypted out.

Similar to a password, the longer the key (usually expressed in bits), the more secure it is. Today, 128-bit keys are commonly used and considered very strong.

## Types of Encryption

## Symmetric Encryption
Symmetric encryption uses a single key to encrypt and decrypt data. Therefore, it is also referred to as secret-key, single-key, shared-key, and private-key encryption. To use symmetric key algorithms, you need to initially exchange the secret key with both the sender and the receiver.

Symmetric-key ciphers can be divided into block ciphers and stream ciphers. A block cipher takes a block of plain text and a key, and outputs a block of ciphertext of the same size. Two popular block ciphers include the Data Encryption Standard (DES) and the Advanced Encryption Standard (AES), which have been designated cryptography standards by the US government.

The Data Encryption Standard was selected by the National Bureau of Standards as an official Federal Information Processing Standard (FIPS) for the United States in 1976. It is based on a symmetric-key algorithm that uses a 56-bit key.

Because DES is based on a relatively small 56-bit key size, DES was subject to brute force attacks. Therefore, without designing a completely new block cipher algorithm, Triple DES (3DES) was developed, which uses three independent keys. DES and the more secure 3DES are still popular and used across a wide range of applications including ATM encryption, email privacy, and secure remote access.

A more secure encryption option would be Advanced Encryption Standard (AES). The standard comprises three block ciphers, AES-128, AES-192, and AES-256 used on 128-bit blocks, with key sizes of 128, 192, 256 bits. The AES ciphers have been analyzed extensively and are now used worldwide, including being used with WI-FI Protected Access 2 (WPA2) wireless encryption. 

Stream ciphers create an arbitrarily long stream of key material, which is combined with plain text bit-by-bit or character-by-character. RC4 is a widely used stream cipher, used in Secure Sockets Layer (SSL) and Wired Equivalent Privacy (WEP). While RC4 is simple and is known for its speed, it can be vulnerable if the key stream is not discarded, nonrandom or related keys are used, or a single key stream is used twice.

## Asymmetric Encryption

Asymmetric encryption uses two keys for encryption. Asymmetric key, also known as public key cryptography, uses two mathematically-related keys. One key is used to encrypt the data, while the second key is used to decrypt the data. Unlike symmetric key algorithms, it does not require a secure initial exchange of one or more secret keys to both sender and receiver. Instead, you can make the public key known to anyone and use the other key to encrypt or decrypt the data. The public key could be sent to someone or could be published within a digital certificate via a Certificate Authority (CA). Secure Sockets Layer (SSL)/Transport Layer Security (TLS) and Pretty Good Privacy (PGP) use asymmetric keys. Two popular asymmetric encryption protocols are Diffie-Hellman and RSA.

For example, say you want a partner to send you data. Therefore, you send the partner the public key. The partner will then encrypt the data with the key and send you the encrypted message. Then, you use the private key to decrypt the message. If the public key falls into someone else’s hands, they still could not decrypt the message.

## Hash Function Encryption
The last type of encryption is the hash function. Different from the symmetric and asymmetric algorithms, a hash function is meant as a one-way encryption. This means that after data has been encrypted, it cannot be decrypted. It can be used to encrypt a password that is stored on disk and for digital signatures. Anytime a password is entered, the same hash calculation is performed on the entered password and it is compared to the hash value of the password stored on disk. If the two passwords match, the user must have typed the correct password. This avoids having to store the passwords in a readable format, where a hacker might try to access them.

Review:

Symmetric encryption: Same key is used to encrypt and decrypt the data.
Examples: DES (Data Encryption Standard), 3DES (Triple DES), and AES (Advanced Encryption Standard).

Block ciphers: A block of plaintext with a key becomes a block of cipher text.
Stream ciphers: Bit-by-bit encryption.

Asymmetric Encryption: One key encrypts, while another key decrypts the data.
Examples: SSL (Secure Sockets Layer), TLS (Transport Layer Security), PGP (Pretty Good Privacy)

Hash function:
One-way encryption with no decryption.
Used to verify passwords.

## Introducing Public Key Infrastructure
A public key infrastructure (PKI) is a system consisting of hardware, software, policies, and procedures that create, manage, distribute, use, store, and revoke digital certificates. Within the PKI, the certificate authority (CA) binds a public key with respective user identities and issues digital certificates containing the public key.

A certificate revocation list (CRL) is a list of certificates (or more specifically, a list of serial numbers for certificates) that have been revoked or are no longer valid, and therefore should not be relied upon. 

## Digital Certificate 
A digital certificate is an electronic document that contains a person’s or organization's name, a serial number, expiration date, a copy of the certificate holder’s public key )used for encrypting messages and to create digital signatures), and the digital signature of the CA that assigned the digital certificate so that a recipient can verify that the certificate is real. 

## Digital Signature 
A digital signature is a mathematical scheme that is used to demonstrate the authenticity of a digital message of document. It is also used to confirm that the message or ducment has not been modified. 

## Secure Sockets Layer (SSL) and Transport Layer Security (TLS)
When surfing the internet, there are time when it is necessary to transmit private data over the internet such as credit card numbers, social security numbers, and so on. During these times, use SSL over http (https) to encrypt the data sent over the internet. By convention, URLs that require an SSL connection start with https: instead of http:.

SSL is short for Secure Sockets Layer. It uses a cryptographic system with two keys to encrypt data – a public key known to everyone and a private or secret key known only to the recipient of the message. The public key is published in a digital certificate, which also confirms the identity of the web server.
Review:

Public keys are often used at the beginning of a data transmission. Such as an e-commerce website, a public key would be sent by a web server to initiate a transaction.

Private keys are often used to decrypt data. The private key is often stored on a web server, and only that server can decrypt the data.

## Encrypting Email
-	Secure/Multipurpose Internet Mail Extensions (S/MIME)
-	Pretty Good Privacy (PGP)

Secure/Multipurpose Internet Mail Extensions (S/MIME) is the secure version of MIME, used to embed objects within email messages. 

Pretty Good Privacy (PGP) is a freeware email encryption system that uses symmetrical and asymmetrical encryption. Message is encrypted with a public key and a session key. Upon receipt, a private key extracts the session key and then both keys decrypt the message.

## Encrypting Files with EFS
Windows 10 offers two file encrypting technologies – Encrypting File System (EFS) and BitLocker Drive Encryption. EFS protects individual files or folders, while BitLocker protects entire drives.

# Knowledge Check

Symmetric: Uses a single key to encrypt and decrypt data.
Asymmetric: Uses two mathematically-related keys.
Hash Function: A one-way encryption.

True or false:
-	CA is a list of certificates that have been revoked or are no longer valid, and therefore should not be relied upon.
-	Within the PKI, the certificate authority binds a public key with respective user identities and issues digital certificates containing the public key.
-	The RA, which may or may not be the same server as the CA, is used to distribute keys, accept registrations for the CA, and validate identities.
-	The RA distributes digital certificates.

F,T,T,F

A ___________ is a mathematical scheme used to demonstrate the authenticity of a digital message or used to confirm that the message or document has not been modified.

A: digital signature

# Understanding IPsec
IP Security, more commonly known as IPsec, is a suite of protocols that provide a mechanism for data integrity, authentication, and privacy for the Internet Protocol. It is used to protect data that is sent between hosts on a network by creating secure electronic tunnels between two machines or devices and it can be used for remote access, VPN, server connections, LAN connections, or WAN connections. 

IPsec was designed to provide interoperable, high quality, cryptographically-based security for IPv4 and IPv6, and it provides a comprehensive set of security services, including the following:
-	Access control
-	Connectionless data integrity checking
-	Data origin authentication
-	Replay detection and rejection
-	Confidentiality using encryption
-	Traffic flow confidentiality 

There are a couple of modes and a couple of protocols available in IPsec, depending on whether they are implemented by the end hosts, such as the server, or implemented on the routers and the desired level of security. 
-	Transport mode (host-to-host): In transport mode, only the data packet payload is encapsulated. Because the packet header is left intact, the original routing information is sued to transmit the data from sender to recipient.
-	Tunnel mode (gateway-to-gateway or gateway-to-host): In the tunnel mode, the IP packet is entirely encapsulated and given a new header. The host/gateway specified in the new IP header decapsulates the packet. This is the mode used to secure traffic for remote access VPN connection from the remote host to the VPN concentrator on the internal network.

The IPsec protocols are:
-	Encapsulating Security Payload (ESP): Provides confidentiality, authentication, integrity, and anti-replay for the IP payload only, not the entire packet. ESP operates directly on top of IP.
-	Authentication Header (AH): Provides authentication, integrity, and anti-replay for the entire packet (both the IP header and the data payload carried in the packet). It does not provide confidentiality, which means that it does not encrypt the payload.
-	Internet Key Exchange (IKE): IKE is used to negotiate, create, and manage security associations (SA), which means that it is the protocol that establishes the secure communication channel between two networks. 

## VPN
Private connection over a public network.
Client to site is the most common. Remote connecting to the company with a secure connection. 
Site to site VPN. Two business connect to each other over a tunnel.
Split tunnel: isolates traffic; which reroutes traffic away from the tunnel, and through the original internet connection. So you get the best of both worlds because you get your regular internet connection but still have the VPN connection so securing transmit data.

# Knowledge Check
-	ESP: Provides confidentiality, authentication, integrity, and anti replay for the IP payload only, not the entire packet.
-	IKE: Used to negotiate, create, and manage security associations (SA).
-	AH: Provides authentication, integrity, and anti-replay for the entire packet.

-	MS-CHAP v2: Provides two-way authentication (mutual authentication)

-	PAP: Least secure authentication and is not recommended.

-	EAP: A universal authentication framework that supports password-based user or computer authentication.

-	CHAP: A challenge-response authentication that uses the industry standard md5 hashing scheme to encrypt the response.

## Auditing

# Knowledge Check

- Account logon: Determines whether the OS audits each time the computer validates an account’s credentials, such as account logon.
-	Logon: Determines where the OS audits each instance of a user attempting to log on or log off the computer.
-	Privilege use: Determines whether to audit each instance of a user exercising a user right.
-	Object access: Determines whether the OS audits user attempts to access non-Active Directory objects, including NFTS files and folders and printers.

# Chapter Review:

- What you know – usernames, passwords, PINs
- What you have – smart card, token, digital certificate
- Who you are – biometrics, fingerprints, voice recognition, retinal scan
- Passwords should be complex with at least 14 characters in length.
- If passwords become cumbersome for employees, start using smart cards or biometrics.
- Passwords should be changed regularly.
- Policies should be in place to enforce complex passwords, how often a user must change their password, state how long a user can reuse a password, and so on.
- Create a password resetting process which requires the user’s identity is verified.
- Do not send passwords via email. Leave password on user’s voicemail, which will require a PIN to access.
- Only running trusted applications is considered the strongest lockdown security option.
- Device Guard: Windows tool which uses code integrity policies to lock devices so they can only run trusted apps.
-RADIUS – Remote Authentication Dial-In User Service. Used to authenticate outside connections from dial-ins, VPNs, web servers, and wireless access points. 
- Anything that is centrally managed on a network is managed through Active Directory.
-Kerberos: Default network authentication protocol (NTLM is a backup) for Active Directory.
- Containers are objects that can store or hold other objects. 
-Delegation of controls – the act of allowing a user or users to take over some or all of a organization unit. 
- On today’s Windows networks, there are two types of user accounts: The local user account and the domain user account.
- In Windows Active Directory, there are two types of groups – security and distribution.
-Universal: Designed to contain global groups from multiple domains.
-Global: Designed to contain user accounts and can contain user accounts and other groups.
-Domain Local: Usually in the domain where the intended resources are located. 
-LDAP: An application protocol for querying and modifying data using directory services running over TCP/IP.
-Kerberos: The default computer network authentication protocol, which allows hosts to prove their identity over a non-secure network in a secure manner.
-SSO: Allows a user to log on once and access multiple, related, but independent software systems without having to log on again.
-Directory Service: Allows organization and naming of all network resources so that passwords, permissions, rights can be assigned to the identity that need them.
-A right authorizes a user to perform certain actions on a computer.
-A permission defines the type of access that is granted to an object (an object can be identified with a security identifier) or object attribute.
- NTFS permissions allow you to control which users and groups can gain access to files and folders on an NTFS volume.
- If you do both a share and a give out file system permissions using the Security tab, the most restrictive permission wins.

-Steps to share a folder:
-	Right click the drive or folder, choose Properties, click the Advanced Sharing button.
-	Select the Share this folder check box.
-	In the Advanced Sharing dialog box, in the Share name text box, type the name of the shared folder.
-	If necessary, specify the maximum number of people that can access the shared folder at the same time and click the Permissions button.
-	By default, Everyone is given Allow Read permission. If you don’t want everyone to access the folder, remove Everyone and assign additional permissions or add additional people.
-	After the users and groups have been added with the proper permissions, close all the windows.
-The registry is the one-stop shop database that stores everything about a system, and its applications.
-Registry has “hives’:
-	HKEY_CLASSES_ROOT: Stores information about registered applications, such as file association that tells which default program opens a file with certain extension.
-	HKEY_CURRENT_USER: Stores settings that are specific to the currently logged-on user. When a user logs off, the HKEY_CURRENT_USER is saved to HKEY_USERS.
-	HKEY_LOCAL_MACHINE: Stores settings that are specific to the local computer.
-	HKEY_USERS: Contains subkeys corresponding to the HKEY_CURRENT_USER keys for each user profile actively loaded on the machine.
-	HKEY_CURRENT_CONFIG: Contains information gathered at runtime. Information stored in this key is not permanently stored on disk, but rather regenerated at the boot time.

-	Symmetric encryption: Same key is used to encrypt and decrypt the data.
Examples: DES (Data Encryption Standard), 3DES (Triple DES), and AES (Advanced Encryption Standard).

- Block ciphers: A block of plaintext with a key becomes a block of cipher text.
- Stream ciphers: Bit-by-bit encryption.

-	Asymmetric Encryption: One key encrypts, while another key decrypts the data.
Examples: SSL (Secure Sockets Layer), TLS (Transport Layer Security), PGP (Pretty Good Privacy)
-	Hash function:
One-way encryption with no decryption.
Used to verify passwords.
- URLs that require an SSL connection start with https: instead of http:
- Public keys are often used at the beginning of a data transmission. Such as an e-commerce website, a public key would be sent by a web server to initiate a transaction.
- Private keys are often used to decrypt data. The private key is often stored on a web server, and only that server can decrypt the data.
- Secure/Multipurpose Internet Mail Extensions (S/MIME) is the secure version of MIME, used to embed objects within email messages. 
- Pretty Good Privacy (PGP) is a freeware email encryption system that uses symmetrical and asymmetrical encryption. Message is encrypted with a public key and a session key. Upon receipt, a private key extracts the session key and then both keys decrypt the message.
- A digital signature is a mathematical scheme used to demonstrate the authenticity of a digital message or used to confirm that the message or document has not been modified.
- ESP: Provides confidentiality, authentication, integrity, and anti replay for the IP payload only, not the entire packet.
- IKE: Used to negotiate, create, and manage security associations (SA).
- AH: Provides authentication, integrity, and anti-replay for the entire packet.
- MS-CHAP v2: Provides two-way authentication (mutual authentication)
- PAP: Least secure authentication and is not recommended.
- EAP: A universal authentication framework that supports password-based user or computer authentication.
- CHAP: A challenge-response authentication that uses the industry standard md5 hashing scheme to encrypt the response.

# Flashcards
-	Access control list (ACL): A list of all users and groups that have access to an object.
-	Accounting: Also known as auditing, is the process of keeping track of a user’s activity while access network resources, including the amount of time spent in the network, the services accessed while there, and the amount of data transferred during each session.
-	Active Directory: Active Directory is a directory service technology created by Microsoft that provides a variety of network services, including Lightweight Directory Access Protocol (LDAP), Kerberos-based and single sign-on (SSO) authentication, DNS-based naming and other network information, and a central location for network administration and delegation of authority. 
-	Administrative share: A shared folder typically used for administrative purposes.
-	Asymmetric encryption: Also known as public key cryptography, uses two mathematically related keys for encryption.
-	Auditing: Also known as accounting, is the process of keeping track of a user’s activity while access network resources, including the amount of time spent in the network, the services accessed while there, and the amount of data transferred during each session.
-	Authentication: The process of identifying an individual, usually based on a user name and password.
-	Authorization: The process of giving individuals access to system objects based on their identity.
-	Biometrics: An authentication method that identifies and recognizes people based on physical traits, such as fingerprints, face recognition, iris recognition, retinal scans, and voice recognition.
-	BitLocker To Go: A new feature in Windows 7 that enables users to encrypt removable USB devices, such as flash drives and external hard disks.
-	Brute Force Attack: A type of attack the tries as many possible combinations of characters as time and money permit.
-	Build-in groups: The default groups that are included within Windows or Active Directory.
-	Certificate chain: Also known as the certification path, is a list of certificates used to authenticate an entity. It begins with the certificate of the entity and ends with the root CA certificate.
-	Certificate revocation list (CRL): A list of certificates (or more specifically, a list of serial numbers for certificates) that have been revoked or are no longer valid and therefore should no be relied on.
-	Computer accounts: A logical object that provides a means for authenticating and auditing a computer’s access to a Windows network, as well as its access to domain resources. 
-	Decryption: The process of converting data from encrypted format back to its original format.
-	Digital certificate: An electronic document that contains an identity, such as a user or organization name, along with a corresponding public key. Because a digital certificate is used to prove a person's identity, it can also be used for authentication.
-	Digital signature: A mathematical scheme that is used to demonstrate the authenticity of a digital message or document.
-	Domain controller: A Windows server that stores a replica of the account and security information of a domain and defines the domain boundaries. 
-	Domain user: A user account stored on the domain controller that allows you to gain access to resources within the domain, assuming you have been granted permissions to access those objects.
-	Effective permissions: Actual permissions when logging in and accessing a file or folder. They consist of explicit permissions plus any inherited permissions.
-	Encryption: The process of converting data into a format that cannot be read by another user. 
-	Explicit permission: Permissions granted directly to a file or folder.
-	Group: A collection or list of user accounts or computer accounts.
-	Hash function: A one-way encryption which means that after something has been encrypted with this method, it cannot be decrypted.
-	Inherited permission: Permissions granted to a folder (parent object or container) that flows into child objects (subfolders or files) inside that folder.
-	IP Security (IPsec): A suite protocols that provides a mechanism for data integrity, authentication, and privacy for the Internet Protocol. It is used to protect data that is sent between hosts on a network by creating secure electronic tunnels between two machines or devices.
-	Kerberos: The default domain computer network authentication protocol, which allows hosts to prove their identity over a non-secure network in a secure manner.
-	Key: Can be thought of as a password which is applied mathematically to plain text to provide cipher or encrypted text. Different keys produce different encrypted outputs.
-	Local user account: A user account that is stored in the Security Account Manager (SAM) database on the local computer. 
-	Member server: A server that is not running as a domain controller.
-	Microsoft Passport: A two-factor authentication that consists of an enrolled device (such as a smartphone) and a Windows Hello (biometric) or PIN.
-	Multifactor authentication: When two or more authentication methods are used to authenticate someone.
-	Nonrepudiation: Prevents one party from denying the actions it has carried out.
-	NTFS: The preferred file system for today’s Windows operating system.
-	NFTS permissions: Permissions that allow you to control which users and groups can gain access to files and folder on an NTFS volume. 
-	NTLM: The default authentication protocol for Windows NT, stand-alone computers that are not part of a domain, and situations in which you are authenticating to a server using an IP address.
-	Organizational units (OUs): A container used in Active Directory to help organize objects within a domain and minimize the number of domains.
-	Owner: An identity that controls an object including what permissions are set on the object and to whom permissions are granted.
-	Permission: Defines the type of access that is granted to an object (an object can be identified with a security identifier) or object attribute.
-	Personal identification number (PIN): A secret numeric password shared between a user and a system that can be used to authenticate the user to the system.
-	Public key infrastructure: A system consisting of hardware, software, policies, and procedures that create, manage distribute, use, store, and revoke digital certificates.
-	Registry: A central, secure database in which Windows stores all hardware configuration information, software configuration information, and system security policies.
-	Right: Authorizes a user to perform certain actions on a computer, such as logging on to a system interactively or backing up files and directories on a system.
-	Secure Sockets Layer (SSL): A cryptographic system that uses two keys to encrypt data, a public key known to everyone and a private or secret key known only to the recipient of the message.
-	Security Account Manager (SAM): A local security database found on most Windows computers.
-	Security token: A physical device that an authorized computer services user is given to ease authentication.
-	Share permissions: The permissions assigned to shared folders or drives.
-	Shared folder: The technology that allows access of data files over the network.
-	Single sign-on (SSO): The technology that allows you to log on once and access multiple related but independent software systems without having to log on again.
-	Smart card: A pocket-sized card with embedded integrated circuits consisting of non-volatile memory storage components and perhaps dedicated security logic.
-	Symmetric encryption: Uses a single key to encrypt and decrypt data.
-	Syslog: A standard for logging program messages that can be accessed by devices that would not otherwise have a method for communications.
-	Trust Platform Module (TPM) chip: An international standard for a secure cryptoprocessor.
-	User account: A logical object that enables a user to log on to a computer and domain.
-	Virtual smart cards (VSCs): The cards that emulate the functionality of regular smart cards, but require a Trusted Platform Module (TPM) chip to protect the private keys.
-	Windows Biometric Framework (WBF): Enables users to manage devices settings for biometric devices through Control Panel, provides support for managing device drivers, and manages Group Policy settings that can be used to enable, disable, or limit the use of biometric data for a local computer or domain. 
-	Windows Hello: A Windows 10 biometric authentication system that uses a user’s face, iris, or fingerprint to unlock devices.

# Understanding Information Security Policies and Their Types

A security policy is a document or group of documents that define the security controls that the company will implement. Policies are not technology-specific and serve three purpose for an organization:
-	Remove third-party legal liability.
-	Protect confidential and proprietary data from theft, unauthorized disclosure, and modification.
-	Avoid misusing the company’s computing resources.

## Understanding Types of Security Policies

There are two kinds of fundamental security policies:
-	Technical security policies: These contain guidelines for how individuals (both end-users and management) should act and react in the face of security threats.

These policies help in maintaining data confidentiality, availability, and integrity. Some other types of security policies also exist as follows:

-	Promiscuous policy: There are no limitations on how you use system resources under this policy. For example, there are no net access restrictions. From a remote location, a user can view any website, transfer any application, and connect to a laptop or a network. This leaves the company open to threats, such as viruses and trojans. 
-	Permissive policy: Only known harmful services/attacks/behaviors are blocked when the policy is launched wide open. Not recommended, as it is impossible to stay up to date with all new exploits; to be effective, this policy would need to be revised on a regular basis.
-	Prudent policy: All services should be blocked as the first step in a smart policy. The administrator authorizes only safe and necessary services. This policy grants the greatest level of protection while allowing only a few minor but necessary risks. 
-	Paranoid policy: Everything is forbidden under a paranoid policy. All user of business computer, whether its for system or network purposes, is strictly prohibited. There’s either no net association or severely restricted net usage. 

Some examples of security policies are:
-	Access control policy: Specifies the resources that are to be secured as well as the rules that govern access to them.
-	Password policy: Explains how to protect company resources with strong passwords.
-	Remote-access policy: Specifies who is eligible for remote access, as well as the access medium and security restrictions for remote access.
-	Firewall-management policy: Governs the organization’s firewall access, management, and monitoring.
-	Network-connection policy: Specifies who has permission to add new network resources, approves the addition of new devices, documents network modifications, and so on.
-	User-account policy: Specifies how user accounts are created, as well as their power, privileges, and responsibilities.
-	Information-protection policy: Specifies the amount of sensitivity of data, who has access to it, how it is stored and communicated, and how it should be destroyed from storage media.
-	Acceptable-use policy: Establishes the limits on how much system resources can be used.
-	Special-access policy: Describes the terms and conditions under which special access to system resources is granted.
-	Email security policy: Purpose is to regulate the proper use of business email.

## Creating and Implementing Security Policies

A security policy is a plan that ensures that security concepts are applied consistently throughout your organization. It becomes a reference book for security issues after it is implemented. The following systems should have rules and regulations established by a security policy:
-	Encryption mechanisms
-	Access control devices
-	Authentication systems
-	Firewalls
-	Anti-virus systems
-	Websites
-	Gateways
-	Routers and switches 

## Steps to Create and Implement Security Policies
The following are some steps that should be performed by an organization in order to create and implement security policies:
1)	Perform a risk assessment to detect threats to the assets of the organization.
2)	Discover valuable information from standard guidelines and other organizations.
3)	Include top management and all other employees in the policy-making process.
4)	Create and enforce fair penalties.
5)	Make the final version available to the entire organization’s workforce.
6)	Ensure that all of your employees have read, signed, and comprehended the policy.
7)	Use tools to enacts policies.
8)	Educate the organization’s workforce regarding policies.
9)	Review and update on a regular basis.

## Understanding Key Elements and Characteristics of a Security Policy 
The following are some key elements and characteristics of a security policy:
-	Overview: Background information on the policy’s topic of concern.
-	Purpose: The reason for policy formation.
-	Scope: The areas that the policy covers.
-	Target audience: The policy is applicable for whom.
-	Policy: A through description of the policy.
-	Definitions: A brief explanation of the technical language used throughout the policy.
-	Version: The number used to track the document’s revision. 

# Knowledge Check

Acceptable-use: Establishes the limits on how much system resources can be used.
Information-protection: Specifies the amount of sensitivity of data and how it should be destroyed from storage media. 
Special-access: Describes the terms and conditions under which a certain connection with system resources is granted.
Access-control: Specifies the resources that are to be secured as well as the rules that govern the right to use them.

Steps to create and implement security policies:
1)	Perform a risk assessment to detect threats to the assets of the organization.
2)	Discover valuable information from standard guidelines and other organizations.
3)	Include top management and all other employees in the policy-making process.
4)	Create and enforce fair penalties.
5)	Make the final version available to the entire organization’s workforce.
6)	Review and update on a regular basis

# Using Password Policies to Enhance Security
A basic component of an information security program is ensuring that employees select and use strong passwords. Microsoft provides several controls that can be used to ensure the security associated with passwords is maintained:
-	Password complexity
-	Account lockout
-	Password length
-	Password history
-	Time between password changes
-	Group Policies that enforce password security
-	Education on common attack methods

## Using Password Complexity to Make a Stronger Password:
A complex password will use characters from at lest three of the following:
-	English uppercase characters (A through Z)
-	English lowercase characters (a through z)
-	Numeric characters (0 through 9)
-	Non-alphanumeric characters (such as !, @, #, $, %, ^, &)

Some methods for selecting strong passwords include:
-	Bump characters in a word certain number of letters up or down the alphabet. A shift three letters translation of “AArdvark!!” becomes “DDvgzdvn!!”
-	Create acronyms from words in a song, a poem, or another sequence of words. The phrase “Ask no what you can do for your country?” yields the password “Anwycdfyc?” 
-	Combine a number of personal facts like birthdates and favorite colors, foods, and so on with special characters to create passwords like: “##Yell0w419” or “$^327p!zZ@”

## Using Account Lockout to Prevent Hacking
Account lockout refers to the number of incorrect logon attempts permitted before the system will lock the accounts. Each bad logon attempt increments the bad logon counter, and when the counter exceeds the accounts lockout threshold, no further logon attempts will be permitted. 

Microsoft provides three separate settings with respect to account lockout:
-	Account lockout duration: This setting determines the length of time a lockout will remain in place before another logon attempt can be made. This can be set from 0 to 99,999 minutes. If set to 0, an administrator will need to manually unlock the account; no automatic unlocking will occur. 
-	Account lockout threshold: This setting determines the number of failed logons permitted before the account lockout occurs. This can be set from 0 (no account lockouts) to 999 attempts before lockout.
-	Reset account lockout counter after: This setting determines the period of time, in minutes, that must elapse before the account lockout counter is reset to 0 bad logon attempts. If an account lockout threshold is set, the reset account lockout threshold must be less than or equal to the account lockout duration.

## Examining Password Length
Literally make your password at least 14 characters /thread.
But the generally accepted minimum is 8 (lol).

## Setting Time Between Password Changes
The final password setting to be aware of is the time between password changes. Two settings are available:
-	Minimum Password Age: The minimum password age setting controls how many days a user must wait before they can reset their password. This can be set to a value from 1 to 998 days. If set to 0, passwords can be changed immediately. Using a setting that is too low could allow users to defeat the password history settings. For example, if this is set to 0, and the password history is set to 10, al a user would need to do is reset their password 10 times, one right after another, and then they could go back to their original password. This setting must be set to a lower value than the maximum password age, unless the maximum password age is set to 0, which means passwords never expire. A good setting is typically 10 days or more, although this can vary widely depending on administrator preferences.
-	Maximum Password Age: The maximum password age setting controls the maximum period of time permitted before a user is forced to reset their password. This can be set from 1 to 999 days, or to 0 if passwords are set to never expire. A general rule for this setting is 90 days for user accounts, although for administrative accounts, its generally a good idea to reset the passwords more frequently. In high security areas, 30 days is not an uncommon setting. 

## Using Password Group Policies to Enforce Password Security
A Group Policy Object (GPO) is  set of rules which allow an administrator granular control over the configuration of objects in Active Directory (AD), including user accounts, operating systems, applications, and other AD objects. GPOs are used for centralized management and configuration for the Active Directory environment. 

## Configuring and Applying Password Settings Objects
If it is necessary to use different password policies for different sets of users, use fine-grained password policies, which are applied to user objects or global security groups.

Fine-grained password policies allow you to specify multiple password policies within a single domain so that different restrictions for password and account lockout policies can be applied to different sets of users in a domain. To enable fine-grained password policies, first create a Password Settings Object (PSO). Then, configure the same settings that are configured for the password and account lockout policies.

## Establishing Password Procedures
Passwords are the most common form of authentication, and IT help desks spend a lot of time managing calls from users who cannot log on because they forgot their passwords or their accounts have been compromised.

Every organization should develop a security policy, which is a written document that describes how a system, organization, or other entity is secured. The security policy should include an acceptable use policy, which describes the constraints and practices that users must agree to in order to access the corporate network, corporate resources, and the internet. It is also important to specify a password policy, which dictates the length and complexity requirements for passwords and how often a password should be changed. It can also specify whether multifactor authentication should be used and whether a lockout policy is used when a user has attempted to log on several times using the incorrect password.

As a general rule, forgotten or new passwords should not be emailed to the user, because they can be intercepted by anyone who has control of their email account. If email absolutely must be used, send a password reset link that contains a token that will expire after a short period of time and can only be used once. 

If a caller calls in or sends an email to request a new password, use a procedure that requires the caller to prove their identity as an authorized user. User’s should not use secret questions (such as their mother’s maiden name or pet’s name), because many of these answers can be guessed through social engineering or by searching the internet for user profiles.

One way to authorize users is to use voicemail. When a user needs to use a PIN to retrieve phone messages, inform the user that you will call them back and that they are not to answer the phone (so that you can leave a voicemail). Because the user should be the only one who knows the PIN to retrieve their voicemail, their use of the PIN to retrieve their voicemail will be used to prove the user’s identity. Alternatively, provide the password to their manager, who is local to the user account.  

## Understanding Common Attack Methods

**Dictionary Attack/brute Force Attack**
A dictionary attack (also known as a brute force attack) uses a dictionary containing an extensive list of potential passwords that the attacker then tries in conjunction with a user ID to attempt to guess the correct password.

These types of attacks tend to be more successful when the password length is 7 characters or less. Each additional character adds a significant number of possible passwords.

The account lockout settings discussing earlier in the lesson are a critical defense against this type of attack, because an account lockout will either slow or stop a brute force attack in its tracks after a certain number of incorrect logons.

**Physical Attack**
Any time a computer can physically accessed by an attacker, the computer is at risk. Physical attacks on a computer can completely bypass almost all security mechanisms, by capturing the passwords and other critical data directly from the keyboard when a software or hardware keylogger is used. In fact, if an encryption key passes through a keylogger, even the encrypted data can be jeopardized.

Other physical attacks include the use of hidden cameras to tape keystrokes, or even the removal and duplication (or direct theft) of a hard drive. While not specifically a password attack, by removing a hard drive, attackers can frequently bypass password controls by mounting the drive remotely, and accessing data directly from the drive, without an intervening operating system.

**Leaked or Shared Passwords**
While not strictly an attack, another challenge that is commonly encountered when dealing with users in an office environment is the leaked or shared password. Users tend to trust their co-workers. As a result, a user could be convinced to share their password with a co-worker who felt they needed it. Users will frequently justify the sharing of account information as critical to “getting the job done” or stating that it’s “more convenient.”

User awareness is the best way to combat this type of attack. Providing users with a greater understanding of the risks and impact of these types of behaviors can go a long way towards keeping passwords under the control of only authorized users.  

**Cracked Passwords**

A cracked password frequently relies on more than just a password attack. In a cracked password attack, the attacker gets access to encrypted password file from a workstation or server. Once they have access, the attacker will start running password cracking tools against the file, with an eye towards breaking as many passwords as possible, when leveraging them to further compromise the company’s network and systems. 

Passwords that are stored in an encrypted state are harder to break than passwords that are stored in clear text or in a hashed state. However, with todays computing power, even encrypted passwords stored are being compromised by cracking attacks.

**Network/wireless Sniffer**
If an attacker can gain access to your internal network, your wireless network, or even an internet access point used by your employees, they have the ability to use a specialized tool known as a sniffer to try to intercept unencrypted passwords.

Sniffers are specifically designed software (and in some cases hardware) applications which capture network packets as they traverse the network and display them for the attacker.

Another area of concern with sniffers is wireless keyboards. At its core, a wireless keynoard is a broadcast technology that sends keystrokes from the keyboard to the receiver connected to the computer. If a receiver is tuned to the same frequency close enough to the computer, every keystroke entered into the wireless keyboard can be captured, without needing a keylogger installed. 

**Guessed Passwords**
While not as prevalent an issue as it was in times past, there is still the possibility that someone could sit down at your computer and guess your computer. So don’t be dumb and use complex non-user specific passwords or a secure password generator. 

# Protecting Domain User Account Passwords

Device Guard helps harden a computer system against malware by running only trust applications, thereby preventing malicious code from running. 

Credential Guard isolates and hardens key system and user security information. Both technologies are available only though Windows 10 Enterprise.

Device Guard and Credential Guard use Windows 10 virtual secure mode (VSM) which, in turn, uses the processor’s virtualization to protect the PC, including data and credential tokens on the system’s disks. By using hardware virtualization, Windows 10 is organized into multiple containers. Windows runs one container; the Active Directory security tokens that allow access to your organization’s resources run in another container. Each container is isolated from the other. Therefore, if Windows is compromised by malware, the tokens are protected because they are isolated in their own encrypted container.

Following are requirements for using VSM:
-	UEFI running in Native Mode (not Compatibility/CSM/Legacy mode)
-	64-bit version of Windows 10 Enterprise
-	64-bit processor that supports Second Layer Address Translation (SLAT) and Virtualization Extensions (such as Intel VT or AMD V)

A Trusted Platform Module (TPM) is recommended. 

# Knowledge Check
Device Guard helps harden a computer system against malware by running only trusted applications, thereby preventing malicious code from running. Credential Guard isolates and hardens key system and user security information.

# Flashcards
-	Acceptable Use Policy: Describes the constraints and practices that users must agree to, in order to access the corporate network, corporate resources, and the internet.
-	Account Lockout: Refers to the number of incorrect logon attempts permitted before a system locks an account. Each bad logon attempt is tracked by the bad logon counter, and when the counter exceeds the account lockout threshold, no further logon attempts are permitted. 
-	Cracked Password: A password that gets access to an encrypted password file fro a workstation or server. Once he or she has access, the attacker starts running password cracking tools against the file, with an eye toward breaking as many passwords as possible and leveraging them to further compromise the company’s network and systems.
-	Credential Guard: Isolates and hardens the key system and user security information.
-	Device Guard: Helps harden a computer system against malware by running only trusted applications, thereby preventing malicious code from running.
-	Dictionary Attack: An attack that uses a dictionary containing an extensive list of potential passwords that the attacker then tries in conjunction with a user ID in an attempt to guess the appropriate password.
-	Fine-grained Password Policies: Allow you to specify multiple password policies within a single domain so that different restrictions for password an account lockout policies can be applied to different sets of users in a domain.
-	Group Policy Object (GPO): A set of rules that allow an administrator granular control over the configuration of objects in Active Directory (AD), including user accounts, operating systems, applications, and other AD objects.
-	Password: A secret series of characters that enables a user to access a particular file, computer, or program. 
-	Password Policy: Dictates the length and complexity requirements for passwords and how often a password should be changed.
-	Password Settings Object: To enable fine-grained password policies, first create a Password Settings Object (PSO). Then, configure the same settings that are configured for the password and account lockout policies. In the Windows Server 2016 environment, PSOs can be created and applied by using the Active Directory Administrative Center (ADAC) or Windows PowerShell.
-	Security Policy: A written document that describes how a system, organization, or other entity is secured.
-	Sniffers: A specifically designed software (and in some cases hardware) applications that capture network packets as they traverse a network, displaying them for the attacker.
-	Strong Password: A password that is hard to guess because it is long and has a mix of different types of characters.

# Using Dedicated Firewalls to Protect a Network

A firewall is a system that is designed to protect a computer or a computer network from network-based attacks. A firewall does this by filtering the data packets traversing the network. A typical perimeter firewall is implemented with two (or more) network connections.
-	A connection to the network being protected.
-	A connection to an external network.

## Understanding the OSI Model
Physical Layer (Layer 1)
-	Media: Cabling types, voltage, signal frequency, speed, bandwidth, and so on.
-	Hardware: Type of connector, type of network interface card used, and so on.
-	Topology: The topology to be used in the network, such as ring, mesh, star, and bus.

Data-link Layer (Layer 2)
-	MAC layer: The MAC address is defined at this layer.
-	LLC layer: The LLC layer is the layer responsible for the error and flow control mechanisms of the data-link layer. The LLC layer is specified in the IEEE 802.2 standard.

Network Layer (Layer 3)
-	Primarily responsible for routing.
-	Defines mechanisms that allow data to be passed from one network to another.
-	Does NOT specify how data is passed, but instead defines the mechanism that permit it.
-	Routers

Transport Layer (Layer 4)
-	Segmentation: Downloading an MP3 file from a favorite music site involves dealing with a large block of data. In order to get from the music site to a PC, this file needs to be broken down into smaller, more manageable blocks, so the network can handle it. This process performed by the transport layer is called segmentation.
-	Service Addressing: Network protocols (TCP/IP, for example) provide several network services. These services are identified by ports. The transport layer ensures that when data traverses the network, it is passed to the correct service.
-	Error Checking: Transport layer protocols also perform error checking on the data and ensure that data is sent and received correctly.

The protocols operating at the transport layer come in two types:
-	Connection Oriented: A connection-oriented protocol, such as the Transmission Control Protocol (TCP), requires an end-to-end connection between hosts before data can be transmitted. 
-	Connectionless: A connectionless protocol, such as the User Datagram Protocol (UDP), allows for the transmission of data without requiring that a connection be established first. 

The transport layer also handles the flow control of data. There are two common methods of flow control-buffering and windowing:
-	Buffering: Buffering flow control temporarily stores data in a buffer and waits for the destination device to become available.
-	Windowing: In a windowing environment, data segments are grouped together, and when sent, require only one acknowledgement.

Session Layer (Layer 5)
-	Responsible for data synchronization between applications on the two devices. 
-	Establishes, maintains, and breaks sessions between devices.

Presentation Layer (Layer 6)
-	Converts application layer data into a format the permits the data to be transmitted across the network. 
-	Responsible for encryption and decryption. 

Some common data formats that are converted by the presentation layer include the following:
-	Graphics files
-	Text and data files
-	Music and video files

Application Layer (Layer 7)
-	Takes data from the user and passes the data to the lower layers of the OSI model for transport.

While the OSI model gives us a framework to categorize technology, it is not fully implemented on today’s networks. Instead, today’s networks follow a simplified model usually consisting of the following four layers:
-	Link Layer: The link layer is the lowest layer of the TCP/IP model and is designed to be hardware independent. It is responsible for linking to the hardware network technology and transmits data. 
-	Internet Layer: The Internet layer is responsible for connecting multiple networks together and for routing of packets between networks. 
-	Transport Layer: The transport layer is responsible for end-to-end message transfer capabilities independent of the underlying network. It also handles error control, segmentation, flow control, congestion control, and application addressing (port numbers).
-	Application Layer: The application layer refers to the higher-level network protocols and services such as SMTP or FTP.

## Types of Hardware Firewalls and Their Characteristics
-	Firewalls filter traffic based on a set of configured rules.
-	The header information contained in data packets provides the firewall the information it needs to apply these rules. 
-	Virtually all firewalls deny-all, permit-specific.

### Understanding Packet Filtering 
The first type of firewall is known as the packet-filtering firewall. 
-	Inspects the data packets as they attempt to traverse the firewall, and based on the rules that have been defined, allows or denies. 

When configuring a packet-filtering firewall rule, one (or more) of the following TCP/IP attributes should generally be used: 
-	Source IP addresses.
-	Destination IP addresses.
-	IP protocol (telnet, ftp, http, https, and so on).
-	Destination TCP and UDP ports.
-	The inbound firewall network interface. 
-	The outbound firewall network interface.

Common protocols and ports that will be encountered in a production network:
-	FTP (file transfer) 20/tcp and 21/tcp
-	Telnet (Terminal logon) 23/tcp
-	DNS 53/udp and 53/tcp
-	HTTP (web) 80/tcp
-	HTTPS (web) 443/tcp
-	SMTP (email) 25/tcp
-	POP3 (email) 110/tcp
-	IMAP3 (email) 220/tcp
-	IMAP4 (email) 143/tcp
-	LDAP (directory services) 389/tcp
-	SQL Server 1443/tcp
-	RDP (Terminal Services) 3389/tcp

### Understanding Circuit-Level Firewalls
Circuit-level firewalls are typically considered a second-generation firewall technology. They work similarly to packet-filtering firewalls, but they operate at the transport and session layer of the OSI model. 

Instead of analyzing each individual packet, a circuit-level firewall monitors TCP/IP sessions by monitoring the TCP handshaking between packets to validate the session. Traffic is filtered based on specified session rules and may be restricted to authorized computers only. 

One unique feature of circuit-level firewalls is that sessions that cross this type of firewall appear to originate from that firewall. This allows the internal network to be hidden from the public network. 

Circuit-level firewalls are almost always used in conjunction with other types of firewalls, because they are only able to permit sessions from authorized computers.

### Understanding Application-level Firewalls
Application-level firwalls (also known as proxy servers) work by performing a deep inspection of application data as it traverses the firewall. Rules are set based on analyzing client requests and application responses, then enforcing correct application behavior.

Application-level firewalls can block malicious activity, log user activity, provide content filtering, and even protect against spam and viruses. 

-	Resource-intensive and can require significant processing power to reduce the chances the firewall impacting network performance.

### Understanding Stateful Multi-level Firewalls
Stateful multi-level firewalls are designed to provide the best features of both packet-filtering and application-level firewalls. This type of firewall provides network-level packet filtering and is also capable of recognizing and processing application-level data. 

## Understanding When to Use a Hardware Firewall Instead of a Software Firewall
There are two basic types of software firewall:
-	Host firewall: One type of software firewall is a firewall application installed on a host, used to protect the host from network-based attacks. Host firewalls are also known as personal firewalls.
-	Network firewall: The other type of software firewall is a firewall application installed on a server used to protect network segments from other network segments. Offer similar functionality to a hardware firewall. 

To protect a single host, the best solution would be to install a software firewall on the host, with a specific set of rules based on what needs to be protected. 

Challenges associated with software firewalls:
-	Host hardware: Software firewalls run on the already busy server’s general purpose hardware. This can lead to bottlenecks (such as processor, memory, or network), especially if the hardware hasn’t been sized appropriately to address the traffic requirements associated with running a firewall application.
-	Host operating system: While both hardware and software firewalls run operating systems, a hardware firewall runs a hardened operating system, a hardware firewall runs a hardened operating system, providing a smaller attack surface than an unhardened operating system. 
-	Other applications: Software firewalls must compete for resources with any other processes running on the host. A hardware firewall has dedicated hardware resources that are not shared with any other services. Additional hardware may be needed to match the performance of the hardware firewall.
-	Availability/stability: One of the potential issues associated with using a software firewall is that its reliability is tied to the reliability of the underlying operating system and associated hardware. 

**In a medium to large network environment, where performance, availability, and reliability are critical, a hardware firewall is the best solution.**

## Understanding Stateful Inspection and Stateless Inspection
In stateless inspection, the data traversing the firewall are examined for information like:
-	The IP address of the sending device.
-	The IP address of the receiving device.
-	The type of packet (TCP, UDP, and so on).
-	The port number.

Stateful inspection takes packet filtering to the next level. In addition to examining the header information of a packet traversing the firewall, a stateful inspection firewall also considers other factors when determining if traffic should be permitted across the firewall. 
-	Also determines whether a packet is part of an existing session. 
-	Keeps track of all current sessions in a state table stored in memory. 
-	Each packet encountered will be analyzed to determine whether it is part of an existing session (state) or not.
-	Stateful inspection firewalls make excellent perimeter firewalls for protecting an internal network from the internet, for protecting DMZ-based hosts from the internet, and for protecting extranets from connections to customers, vendors, or business partners.

# Knowledge Check
-	Link – The lowest layer of the TCP/IP model and is designed to be hardware independent.
-	Internet – Responsible for connecting multiple networks together and for routing of packets between networks.
-	Transport – Responsible for end-to-end message flow capabilities independent of the underlying network.
-	Application – Refers to the higher level network protocols and services such as SMTP or FTP.

-	Circuit-level – A second generation firewall technology which operates at the transport and session layers of the OSI model.

-	Application-level – Blocks malicious activity, logs user activity, provides content filtering, and even protects against spam and viruses. 

-	Packet-filtering – Inspects the data as they attempt to traverse the firewall, and based on the rules that have been defined on the firewall, the firewall allows or denies them.


# Using Isolation to Protect the Network
## Understanding VLANs
Virtual LANs (VLANs) were developed as an alternate solution to deploying multiple routers. VLANs are logical network segments used to create separate broadcast domains, but still allow the devices on the VLANs to communicate at Layer 2, without requiring a router. 

VLANs are created by switches, and traffic between VLANs is switched, not routed, which creates a much faster network connection. Even though the hosts are logically separated, the traffic between the hosts is switched directly as if the hosts were on the same LAN segment. 

VLANs provide several benefits over a routed network, including the following:
-	Higher performance on medium or large LANs due to reduced broadcast traffic.
-	Organized devices on the network for easier management.
-	Additional security because devices can be put on their own VLAN. 

There a several different ways to assign hosts to VLANs. These methods include the following:
-	VLAN membership by port: The ports on the switch are defined as belonging to a specific VLAN, so any device plugged into a port would be assigned to the corresponding VLAN. For example, a 32-port switch might have ports 1-4 assigned to VLAN1, ports 5-16 assigned to VLAN2, and ports 17-32 assigned to VLAN3. 
-	VLAN membership by MAC address: Under this model, membership in a VLAN is based on the MAC address of the host. When the VLAN is set up on the switch, the hosts are assigned based on their MAC address. When a workstation moves to another location, and connects to a different switch port, the switch automatically assigns the host to the appropriate VLAN based on the MAC address of the workstation. Because the MAC address is generally hard-coded into the host’s NIC, this model is generally more usable in an environment where hosts move. Does require more work to setup, however.
-	Membership by IP subnet address: In this type of VLAN association, membership is based on the Layer 3 header. The switch reader the Layer 3 IP address and associates the address range with the appropriate VLAN. This model is also conductive to an environment where there are frequent user moves. 
-	Membership by protocol: VLANs can also be organized based on protocol. 

## Understanding Routing
Routing is the process of forwarding a packet based on the packet’s destination address. At each step in the route a packet takes across the network, a decision has to be made about where the packet is to be forwarded. 

To make these decisions, the IP layer consults a routing table stored in the memory of the routing device. Routing table entries are created by default when TCP/IP initializes, then additional entries are added either manually by a system administrator or automatically through communication with routers.

Routers come in two basic types: software and hardware. A software router is a computer running an operating system and multiple services, including a routing service. Windows Server 2016 supports routing. Some benefits of a software router include the following:
-	Tight integration with the OS: The routing service is frequently integrated with the operating system and other services. 
-	Consistent/easier user interface: No retraining is required on a new interface/operating system – the routing functions are configured through the standard user interface.
-	Low cost: When adding routing to an existing server, it is not necessary to pay for dedicated hardware. This reduces the overall cost, although if you were to dedicate a software router for just routing, any cost saving would be negligible. 
-	Flexibility: Software routers allow multiple services to be configured and run on a single platform.  

While there are benefits to using a software router, there are also some significant drawbacks when compared to a hardware router:
-	Performance: Due to the additional overhead associated with the operating system and any additional running services, software routers are typically slower than hardware router.
-	Less reliable: Any software router has the potential for issues with the operating system and other running services, as well as with the greater number of hardware components compared to a hardware router. 
-	Limited scalability: Scaling a software router to multiple high-speed interfaces will be subject to the limitations of the computer hardware. 
-	Limited protocol support: Software routers typically do not support as many routing protocols as a hardware router. Windows Server 2016 is limited to the IP routing protocols RIP, OSPF, and BGP, and does not presently support any of the more advanced IP-based routing protocols, like BGP4.

A hardware route is dedicated hardware device whose main function has been to route packets. Many hardware routers are multi-function devices, having additional functionality like VPN, DHCP, firewall, caching, or in some cases even intrusion detection services.
Benefits include:
-	Higher performance – Hardware routers run on custom-built, single-purpose hardware platforms with highly optimized hardware and operating systems.
-	Highly reliable – Hardware routers are typically more reliable than their software counterparts, due in large part too the limited software capabilities, and dedicated hardware.
-	Wide routing protocol support – Hardware routers can typically be configured to support a larger range of routing protocols, as long as the appropriate functions are purchased.

Hardware routers drawbacks:
-	Higher cost
-	Less user friendly
-	More complex

## Understanding Intrusion Detection Systems (IDS) and Intrusion Prevention Systems (IPS)

There are two main types of IDS/IPS:
-	Network-based: monitors network traffic using sensors that are located at key locations within a network, such a DMZ. 
-	Host-based: Generally has software agent that acts as the sensor. Monitors all activity of the host, including file system, logs, and kernel.

Common deployment methodologies used when placing IDS/IPS:
-	Unfiltered: examines the raw Internet data stream before it crosses the firewall. Provides the highest amount of visibility to attacks, but also means that there is a significantly higher volume of data to be monitored, with a higher possibility of false positives. 
-	Screened: Monitors traffic that gets through the screening firewall. Dramatically reduces the amount of traffic that needs to be monitored, reducing the changes of false positives and lost packets. 

## Understanding Honeypots

Honeypot: trap for hackers (lol).

Honey net: collection of honey pots.

Different types of honeypots:
-	Production: Used to distract attackers from potentially vulnerable production systems and are relatively easy to use. 
-	Research (YE BOI): Used to capture extensive information which is used to develop attack signatures, identify new attack techniques and vulnerabilities, and develop better understanding of the attacker’s mindset. 

## Understanding DMS

DMZ is a firewall configuration used to secure hosts on a network segment. In most DMZs, the hosts on the DMZ are connected behind a firewall which is connected to a public network like the Internet. Another common config is to have the firewall connected to an extranet, with connections to customers, vendors, or business partners. DMZs are designed to provide access to systems without jeopardizing the internal network.

Two typical DMZs:
-	Sandwich DMZ: There is an outer firewall and inner firewall. The outer firewall secures the DMZ network segment from the external (insecure) network. Servers that are meant to be accessed from the external network (like the Internet) have the appropriate rules configured to permit secure access. The inner firewall is used to add an additional layer of security between the servers on the DMZ and the internal (secure) network.
-	Single Firewall DMZ: In a Single Firewall DMZ, the DMZ is an additional network connection from the firewall. This provides an external network connection, an internal network connection, and a DMZ network connection, all connected to the same firewall. 

Servers and services which might be placed on a DMZ:
-	Web servers: Web servers are the most common servers found in DMZ networks. Accessed using HTTP over port 80 or HTTPS over port 443 for secure access. 
-	Email relay servers: Allow for sending and receiving Internet email. 
-	Proxy servers: Used to proxy or act as an intermediary for user requests from the internal network to the Internet, and are typically used to retrieve website information. 
-	Reverse proxy servers: Used to provide secure access to internal application from an insecure network. Largely been replaced by VPNs, reverse proxy servers can be used to provide employees access to web-based email servers on the internal network, provide access to internal web applications and in some cases, even provide secure terminal services connections to the internal network.

## Understanding NAT
Network Address Translation (NAT) is a technique used to modify the network address information of a host while traffic is traversing a route or firewall. Used to hide the network information of a private network, while allow traffic to be transferred across a public network like the Internet. 

-	Originally created as a workaround for IP addressing issues.
-	Allows the use of one set of IP addresses on the internal LAN, and a second set of IP addresses for the Internet connection.

Two main types of NAT:
-	Static NAT: Maps an unregistered IP address on the private network to a registered IP address on the public network, using a one-to-one basis. 
-	Dynamic NAT: Maps unregistered IP address on the private network to a registered IP address that is selected by the routing device providing the NAT service from a pool of registered IP addresses. More common when many hosts on the internal network need to access the Internet and don’t have a requirement for a static address. 

## Understanding VPN
Technology used for encrypted tunnels to create a secure connection across public networks like the Internet. VPNs utilize encryption and authentication to provide confidentiality, integrity, and privacy for data.

The first standards-based VPNs were based on the IPsec protocol. 


## Understanding Other VPN Protocols
IPsec can be considered predominant protocol associated with VPNs, but others include:
-	Secure Sockets Layer (SSL)/transport Layer Security (TLS): Main alternative to IPsec.
-	Widely used to secure websites, it has also been formalized in the IETF standard known as Transport Layer Security (TLS). 
-	SSL/TLS provides a method for secure client/server communications across a network and prevents eavesdropping and tampering with data in transit. 
-	Provides endpoint authentication and communications confidentiality using encryption. 
-	HTTPS uses SSL protocol. 
-	128-bit encryption. 
-	SSL VPNs are predominantly used for remote access VPN connections.

Benefits of SSL/TLS VPNs over IPsec:
-	Less expensive
-	Platform independent 
-	Client flexibility
-	NAT support
-	Granular access control
-	Fewer firewall rules required

## Secure Shell (SSH)
Protocol used for secure remote logon and other secure network services over the network.

Some applications supported with SSH:
-	Secure logon
-	Secure remote command execution
-	Secure file transfer
-	Secure backup, copy, and mirroring of files
-	Creation of VPN connections (when used in conjunction with the OpenSSH server and client)
SSH protocol consists of three major components:
-	Transport Layer Protocol
-	User authentication protocol
-	Connection protocol

# Knowledge Check
Honeypot – distracts hackers from real targets, detects new vulnerabilities, and learns about the identity of attackers.

DMZ – Firewall configuration to secure hosts on a network segment.

NAT – technique used to modify the network address information of a host while traffic is traversing a router.

VPN – Tehcnology that uses encrypted tunnels to create secure connections across public networks like the Internet.

-	NIDS – monitors traffic using sensors located at key locations within the network, often in the DMZ.
-	NIDS – gains access to traffic by connecting to a bug, a switch configured for port mirroring.
-	HIDS – has a software agent that acts as the sensor.
-	HIDS – Monitors all activities like monitoring the file system, the logs, and the kernel to identify and alert upon suspicious behavior. 

# Protecting Data with Protocol Security

## Understanding Tunneling
Tunneling is defined as the encapsulation of one network protocol within another. Tunneling can be used to route an unsupported protocol across a network, or to a securely route traffic across an insecure network. VPNs use a form of tunneling when data is encapsulated in the IPsec protocol. 

Example of tunneling that is used to move unsupported traffic across a network is the Generic Routing Encapsulation (GRE) protocol. GRE is an IP-based protocol frequently used to carry packets from unrouteable IP addresses across an IP network. 


PPTOP (Point-to-Point Tunneling Protocol) is a proprietary VPN protocol originally developed by the PPTP Forum, a group of vendors that included Ascend Communications, Microsoft Corporation, (WHO CARES). PPTOP was popular, but not so much after IPsec was released.

## Understanding DNS Security Extensions (DNSSEC)
DNS Security Extensions (DNSSEC) adds security provisions to DNS so that computers can verify the they have been directed to proper servers. DNSSEC provides authentication and integrity checking on DNS lookups, ensuring that outgoing internet traffic is always sent to the correct server. 

DNSSEC provides authentication and integrity checking through the use of public key encryption. 

## Understanding Protocol Spoofing
Spoofing is hoaxing stuffs. Basically, dressing up a dog as a cat.

Protocol spoofing is the misuse of a network protocol to perpetrate a hoax on a host or a network device. Common forms of protocol spoofing:
-	ARP spoofing: ARP (Address Resolution Protocol) spoofing (or ARP poisoning) is an attack on the protocol used to determine a device’s hardware address (MAC address) on the network when the IP address is known. The attack occurs when an attacker modifies the network’s ARP caches and takes over the IP address of the victim host. This permits the attacker to receive any data intended for the original host.
-	DNS spoofing: Occurs when an attacker is able to intercept a DNS request and respond to the request before the DNS server is able. As a result, the victim host is directed to the wrong website, where additional malicious activities can take place. This attack is frequently used in conjunction with network sniffing.
-	IP address spoofing: Attacker creates IP packets with forged source IP address to either conceal the identity of the attacking host, or to impersonate the identify of the victim host. 

## Understanding Network Sniffing
WIRESHARK MY DUDES!

Today, with widespread use of encryption through secure websites and the use of VPNs for remote access, the risks presented by network sniffing are slightly mitigated, as the attacker can no longer read the data contents of a packet. 

Network sniffers can only see traffic that crosses the port to which it is connect. Sniffers placed on the LAN in a branch office cannot capture traffic from the headquarters networks. In a switched environment, leveraging VLANs, the amount of traffic passing any one port can be limited. The ports that offer the most information are the ingress/egress points to the network, where all traffic from the subnet is concentrated.

This means an attacker cannot directly capture traffic from your network, but the doesn’t mean youre safe (you never ARE!). 

## Understanding Common Attack Methods
Common attack includes:
-	Denial-of-service/distributed denial-of-service (DOS/DDoS) attacks. 
-	IP spoofing to bypass network security: By appearing as trust, the attacker is able to bypass network security. 
-	Man-in-the-middle attacks: breaks communication between the endpoints of a network connection to intercept data being transferred or even inject false information into the data stream.
-	Back door attack: Access point purposely coded in software by some jerk dude. Super hard to find. Try hard senior security programmers.
-	DNS poisoning: Attack against cached information on a DNS server.
-	Replay attack: Attack is able to capture an intact data stream from the network using a network sniffer, modify certain components of the data stream and then replay the traffic back to the network to complete their attack.
-	Weak encryption keys: Do I really need to describe this. Don’t use WEP.
-	Social engineering: lol.
-	Password cracking: lol. Requires access to encrypted password database, and a tool designed to decrypt the database. Rainbow tables prob.
-	Dictionary attack: lol. Uses dictionary of common passwords.
-	Brute force attack. Script kiddie stuff. Attempts every key combination known in order to break the password. GPUs gonna be needed to be anywhere near operatable.
-	Software vulnerability attack: vulnerabilities in code or os. Basically the Windows OS in its entirety. 
-	Buffer overflow attack: Exploits poorly written code (so mine) by injecting data into variable fields and leveraging the responses to access information in the application. 
-	Remote code execution attack: The best kind of attack and pretty common in CVEs. When an application is improperly coded, an attacker is able to run arbitrary, system level code through the application and use the results to access data or perform other unintended actions against the application or application server. 
-	SQL injection attack: Older kind of attack. Uses control characters entered into a database like web application to retrieve information.
-	Cross-site scripting (XSS) attack: By far the most common and potentially the most dangerous current attack against web users. These attacks bypass security mechanisms and inject malicious scripts into web pages, getting users to execute them, an attack can gain elevated access privs to sensitive page content, sessions cookies, and a variety of other information maintained by the browser. 

# Knowledge Check:
Social engineering attack – An attack that occurs when an attacker contacts an employee of the company and tries to extract useful information from them.

DNS poisoning – An attack against the cached information on a server.

Back door attack: An attack against an opening left in a functional piece of software that allows access into a system or software application without the owner’s knowledge.

Man-in-the-middle attack: A type of attack where the attacker breaks into the communication between the endpoints of a network connection.


IP address spoofing: The attacker creates IP packets with a forged source IP address to either conceal the identity of the attacking host, or to impersonate the identity of a victim host.

ARP spoofing: An attack on the protocol used to determine a device’s hardware address on the network when the IP address is known.

DNS spoofing: Occurs when an attacker is able to intercept a request and respond to the request before the server. Its like DLL hacking kinda but not really.


# Understanding Denial-of-Service (DoS) Attacks

When a DoS attack occurs, the usual symptoms include the following:
-	Unusually slow network performance, including when opening files or accessing website. 
-	Unavailability of any or all websites.
-	Dramatic increase in the number of spam emails received.

There are three general types of DDoS attacks:
-	Volume-based attacks: Saturates the bandwidth of an attack site or system by flooding the site or system with UPP packets, ICMP packets, or other spoofed packets.
-	Protocol attacks: Consumes resources of server or communication devices, such as firewalls and load balancers. They include SYN floods, fragmented packet attacks, ping of death attacks, and Smurf DDoS.
-	Application-layer attacks: Uses system or device vulnerabilities to crash the server or communication device. They include low-and-slow attacks and GET/POST floods.

Popular and dangerous types of DDoS attacks:
-	UDP flood: Uses User Datagram Protocol (UDP), which is a connectionless networking protocol, to flood random ports on a remote host with numerous UDP packets. When the server repeatedly checks for the application listening at that port – to the point at which the system utilities all its resources responding to it – the system becomes inaccessible.
-	ICMP (ping) flood: Uses ICMP packets to flood systems. This type of attack can consume both outgoing and incoming bandwidth because the victim’s servers often attempt to respond with ICMP Echo Reply packets.
-	SYN flood: Many TCP protocols use a three-way handshake in which a SYN Request is sued to initiate a TCP connection. The host responds with a SYN-ACK response, which is confirmed with an ACK response from the requester. In a SYN flood, the attacker sends multiple SYN request from a spoofed IP address. Too many SYN requests lead to the system not accepting any new connections.
-	Ping of death: An attack that sends multiple malformed or malicious pings to a computer. The IP package, including the header, is 65,535 bytes in length, and many computer systems were never designed to properly handle ping packets larger than this, because it violates the Internet Protocol. By sending IP fragments with oversized Fragment Offsets, attackers can cause the IP packets, which were split into smaller sizes for travel, to form packets larger than 65,535 bytes after reassembly at the receiver, overflowing the memory buffers. Thus, important memory areas are overwritten, causing denial-of-service for legitimate packets.
-	HTTP flood: Uses many HTTP GET or POST requests to attack a web server or application. This attack is most effective when it forces the server of application to allocate the maximum resources possible in response to each single request.
-	Email bomb: Sends so many emails to a user or domain, the server becomes overwhelmed. 
-	Zero-day attacks: These attacks are based on using unknown or recently announced vulnerabilities. 

# Knowledge Check

Select the types of DDoS attacks:

Volume-based: Saturates the bandwidth of an attack site or system by flooding the site or system with UPP packets, ICMP packets, or other spoofed packets.

Protocol: Consumes resources of server or communication devices, such as firewalls and load balancers.

Application layer: Uses system or device vulnerabilities to crash the server or communication device.

# Flashcards
Application-level firewalls: Also known as proxy servers. Work by performing a deep inspection of application data as it traverses the firewall. Rules are set by analyzing client requests and application responses, then enforcing correct application behavior.

ARP Spoofing: ARP (Address Resolution Protocol) spoofing (or ARP poisoning) is an attack on the protocol used to determine a device’s hardware address (MAC address) on the network when the IP address is known.

Back door attack: Against an opening left in a functional piece of software that allows access into a system or software application without the owner’s knowledge.

Buffer overflow attack: Exploits poorly written code by injecting data into variable fields and leveraging the response to access information in the application.

Circuit-level firewalls: Typically considered second-generation firewall technology. They work in a similar fashion to packet-filtering firewalls, but they operate at the transport and session layers of the OSI model.

Cross-Site Scripting (XSS) attack: by the thee most common and potentially the most dangerous attack against web servers. Allows attackers to bypass the security mechanisms provided by the web browser.

Denial-of-service (DDoS) attack: Attacker renders a machine or network resource unavailable. 

DMZ (demilitarized zone): Firewall configuration to secure hosts on a network segmenet.

DNS poisoning: Attack against the cached information on your DNS server. 

DNS Security Extensions (DNSsec): Adds security provisions to DNS so that computers can verify they have been directed to proper servers.

DNS spoofing: Occurs when an attacker is able to intercept a DNS request and respond to the request before the DNS server.

Email bomb: Lots of emails so email server is overwhelmed. 

Firewall: System that is designed to protect a computer or a computer network from network-based attacks.

Honey net: Collection of honeypots used to present an attacker with an even more realistic attack environment. 

Honeypot: trap for hackers.

Host firewall: Software firewall installed on a host and used to protect the host from network-based attacks.

HTTP flood: Uses many HTTP GET or POST requests to attack a web server or application. This attack is most effective when it forces the server or application to allocate the maximum resources possible in response to every single request. 

ICMP (ping) flood: Uses ICMP packets to flood systems.

IEEE 802.1x: WPA/WPA2 uses an external authentication server coupled with the EAP standard to enable strong authentication for connection to the WLAN.

Intrusion Detection Systems (IDS): Designed to detect unauthorized user activities, attacks, and network compromises.

Intrusion Prevention Systems (IPS): Detects authorized user activities, attacks, and network compromises that can also take action to prevent a breach from occurring. 

IP address spoofing: Attacker creates IP packets with a forged source IP address to either conceal the identity of the attacking host or to impersonate the identity of a victim host.

MAC address: They physical address of ur NIC.

Man-in-the-middle attack: Breaks into the communication between endpoints of the network connection.




# Protecting the Client Computer
## Protecting Your Computer from Malware
Malware is bad basically. (per vx underground)

### Understanding Types of Malware 
-	Virus
-	Worm (best kind)
-	Trojan horse
-	Spyware and dishonest adware
-	Rootkit
-	Backdoor (also best lol)
-	Polymorphic virus (this one cool too)
-	Zero-day attack (nerds)
-	Ransomware (script kiddies)

Recommendation to protect against ransomware:
-	Install and use an up-to-date antivirus solution.
-	Make sure the OS and software are up-to-date.
-	Avoid clicking links and opening weird attachments.
-	Ensure SmartScreen Filter is turned on.
-	Ensure that a pop-up blocker is enabled.
-	This is obviously the most important but they saved it for last: Backup your stuff chump. Back it all up. On regular basis. Every day. Do it now.

Signs you have malware:
-	System slow
-	System less memory
-	Performs poorly when connected to internet
-	Computer stops responding
-	Takes longer to start up
-	Browser closes unexpectedly or stops responding 
-	Browser default home or search page change
-	Advertising windows unexpectedly pop up
-	Additional toolbars are unexpectedly added to browser
-	Programs start unexpectedly
-	Programs cannot start
-	Components of Windows or other programs no longer work
-	Program or files suddenly missing (lol)
-	Messages or displays on a monitor are unusual
-	Sounds or music that are unusual play at random times (LOL)
-	Programs or files that are unknown have been created or installed
-	Browser has unknown add-ins
-	Files have become corrupted
-	File size unexpectedly changes

## Backup Types
-	Full backup: All data is backed up. Takes longer but is most common.
-	Incremental backup: Only the data that has changed since last backup. Faster.
-	Differential backup: Similar to incremental, but continues to replicate all data that has changed since the previous full backup each time it is run after that. Medium speed.

## Restore Types
-	File restore: without the help of an administrator, file owners can search for, find, and restore files from a virtual machine (VM) backup. 
-	Instant restore: Makes use of data generated by the backup-archive client in the form of snapshots.
-	Full VM resotre: It allows both VM backups, whether its full or incremental. The complete virtual machine is returned to the state in was in when it was backed up. 
-	Full VM instant restore: With full VM instant restore, the recovered VM is immediately usable, whether for validating the backed-up VM or restoring it to permanent storage. In read/write mode, the recovered VM is immediately available.
## Understanding User Account Control (UAC)

As a standard user in Windows 10, the following actions can be performed without requiring administrative permissions or rights:
-	Install updates from Windows Update
-	Install drivers from Windows Update or those that are included with the OS
-	View Windows settings
-	Pair Bluetooth devise with the computer
-	Reset the network adapter and perform other network diagnostic and repair tasks

# Knowledge Check

Skip this was too easy bruh.


# Flashcards
Adware: Any software package that automatically plays, displays, or downloads advertisements to a computer after the software is installed or while the application is being used.

AppLocker: Controls how users access and use programs and files, and extend the functionality originally provided by the Software Restriction policy found in earlier versions of Windows OS.

Backdoor: A program that gives someone remote, unauthorized control of a system or initiates an unauthorized task.

Bayesian Filters: Special algorithms which determine whether an email is considered spam.

Bring Your Own Device (BYOD) policies: Defines the standards, restrictions, and procedures for end-users who have authorized access to company data from their person devices. The policy also includes hardware and related software that is not approved, owned, or supplied by the company. 

Content Zones: Zones used to define and help manage security when visiting sites.

Cookie: A piece of text by a user’s web browser. This file can be used for a wide range or purposes, including user identification, authentication, and storing site preferences and shopping cart contents.

Line of Business Apps: These include apps that are critical to running the company business as well as apps that are unique to the company’s main business.

Malicious Software (Malware): Software designed to infiltrate and adversely affect a computer system without the owner’s informed consent. It is usually associated with viruses, worms, Trojan horse, spyware, rootkits, and dishonest adware.

Microsoft Account: Previously called Windows Live ID, is a unique account that is the combination of an email address and a password that you use to sign in to services like Outlook.com, MSN.com, Hotmail.com, OneDrive, Windows Phone, or Xbox Live.

Microsoft Active Protection Service (MAPS): An online community that can help you decide how to respond to certain threat types and it serves as a resource to help stop the spread of new viruses and malware.

Microsoft Baseline Security Analyzer (MBSA): Software tool released by Microsoft to determine the security state of a system by assessing missing security updates and leess-secure security settings within Microsoft Windows components such as Internet Explorer, IIS web server, and products such as Microsoft SQL Server and Microsoft Office macro settings.

Microsoft Edge: BRO.

Offline Files: Copies of network files that are stored on your computer so you can access them when you arrent connected to the network or when the network folder that contains the files is not connected.

Pharming: An attack aimed at redirecting a website’s traffic to a bogus website.

Phishing: Technique based on social engineering, where users are asked (usually via email or website) to supply personal information.

Polymorphic virus: Mutates or changes code to avoid detection.

Pop-up Windows: Component used on web pages that can be used as part of useful website controls but can also be used for annoying advertisements, and a few may attempt to load spyware or other malicious programs.

Ransomware: One of the fastest growing forms of malware; encrypts data files and then demands payment.

Read-Only Domain Controller (RODC): Contains a full replication of the domain database. It was created to be used in places where a domain controller is needed but where the physical security of the domain controller could not be guaranteed.

Rootkit: Software or hardware device designed to gain administrator-level control over a computer system without being detected.

Rule Collections: AppLocker uses rules and file properties – rules collections – to determine which programs and files are allowed to run on the computer. 

Security Baseline: Collection of security settings. Security baselines should include Microsoft’s recommendations for configuring those settings. 

Security Compliance Manager 4.0 (SCM 4.0): Free tool from Microsoft that can be used to quickly configure and manage your desktops, traditional data center, and private cloud using Group Policy and System Center Configuration Manager. It includes creating baselines for Windows Server 2016, Windows 10, and Internet Explorer 11.

Sender Policy Framework (SPF): Email validation system designed to prevent email spam that uses source address spoofing.

Spam: junk emails.

Spyware: Malware that collects personal information, such as browsing habits.

Trojan Horse: Executable program that appears as desirable or useful program BUT IT AINT BOY. Pirate bay basically.

Universal Windows Platform (UWP) apps: Special type of Windows Store app that can be installed on multiple hardware platforms, such as an Intel tablet that is running Windows 10 Pro, an Xbox One, or a Windows 10 Phone. 

User Account Control (UAC): Helps prevent unauthorized changes to your computer – and in doing so, it helps protect your system from malware.

Virus: Can copy itself and infect a computer without the users consent or knowledge.

Virus Hoax: Fake pop up messages. Probably from adware.

Windows Defender: Basically a really poor anti virus. Can prevent, remove, and quarantine spyware.

Windows Firewall: Helps prevent hackers or malicious software (such as worms) from gaining access to your computer through a network or the internet.

Windows Server Update Services (WSUS): Software system that keeps your system updated with the newest Windows and Office updates.

Windows Store: APPS.

Windows Store for Business: PRIVATE APPS OR WHATEVER.

Windows Update: Patches. Fixes. Recognition that Windows OS is bad.

Worm: Self-replicating program. Bad.

Zero-day attacks: Based on unknown or recently announced vulnerabilities. 

# The Basics of a Network

The real essence of networks is communication – allowing one machine to communicate with another. 

## Data Packets
After establishing connection with a network, you need to send data. The first step is to identify where you want to send it. The second part is to format the data for transmission. All data is ultimately in binary form. This binary data is put into packets, all less than 65,000 bytes. 

The first few bytes are the header. The header tells where the packet is going, where it came from, and how many more packets are coming as part of this transmission. A packet can have multiple headers. Most packets will have at least 3 headers. The IP header has information such as IP addresses for the source and destination. The TCP header has information such as port number. The Ethernet header has information such as the MAC address for the source and destination. If a packet is encrypted with Transport Layer Security (TLS), it will also have a TLS header.

## IP Addresses
Class A: 0-126 – Extremely large networks. No Class A network IP addresses are left. All have been used.

Class B: 128-191 – Large corporate and government networks. All Class B IP addresses have been used.

Class C: 192-223 – The most common group of IP addresses. Usually ISP have class C addresses.

Class D: 224-247 – These are reserved for multicasting (transmitting different data on the same channel).

Class E: 248-255 – Reserved for experimental use.


Private IP addresses:
-	10.0.0.10 – 10.255.255.255
-	172.16.0.0 – 172.31.255.255
-	192.168.0.0 to 192.168.255.255

One of the roles a gateway router is to perform what is called network address translation (NAT). Using NAT, a router take the private IP address on outgoing packets and replaces it with the public IP address of the gateway router so the the packet can be routed through the Internet. 

## Uniform Resource Locators
You type in domain names that make sense to humans and those get translated into IP addresses. Your computer or your ISP must translate the name you typed in the URL into an IP address. The DNS protocol handles the translation process.

Email works the same way as visiting websites. Your email client will seek out the address of your email server. Then your email client will use either POP3 to retrieve your incoming email or SMTP to send your outgoing email. 

## MAC Addresses
Every NIC in the world has a unique address that is represented by a six byte hexadecimal number. The Address Resolution Protocol (ARP) is used to convert the IP addresses to MAC addresses. 

## Protocols 
Different types of communications exist for different purposes. The different types of network communications are called protocols. A protocols is essentially an agreed upon method of communication.

Popular protocols:
-	FTP (20 & 21) – For transferring files between computers.
-	SSH (22) – Secure Shell. A secure/encrypted way to transfer files.
-	Telnet (23) – Used to remotely log on to a system. You can then use a command prompt or shell to execute commands on that system. Popular with network administrators.
-	SMTP (25) – Sends email.
-	WhoIS (43) – A command that queries a target IP address for information.
-	DNS (53) – Translates URLs into web addresses.
-	tFTP (69) – Quicker, but less reliable form of FTP.
-	HTTP (80) – Displays web pages.
-	POP3 (110) – Retrieves email.
-	NNTP (119) – Used for network news groups (Usenet newsgroups). You can access these groups over the web via google.
-	NetBIOS (137, 138, 139) – An older Microsoft protocol for naming systems on a local network.
-	IRC (194) – Chat rooms.
-	HTTPS (443) – HTTP encrypted with SSL or TLS.
-	SMB (445) – Used by Microsoft Active Directory. 
-	ICMP (No specific port) – These are simply packets that contain error messages, informational messages, and control messages. 

# Knowledge Check
List the Class:
-	C – the most common group of IP addresses.
-	B – Large corporate and government networks.
-	D – Reserved for multicast groups.
-	A – Extremely large networks.
-	E – Reserved for experimental use.

Indicate if each of the given statements about IPv6 is true or false:
-	True - IPv6 link/machine-local IP addresses all start with fe80::
-	False - The loopback address for IPv6 can be written as ::/126
-	True - It utilizes a hex numbering method to avoid long addresses.
-	True - It does not use subnetting but instead uses CIDR.

-	Telnet – Used to remotely log on to a system.

-	HTTP – Displays web pages.

-	WhoIS – A command that queries a target IP address for information.

-	DNS – Translates URLs into web addresses.

-	FTP – Transfers files between computers.


# Basic Network Utilities

## ipconfig
Gives some information about your connection to a network or the Internet. Most importantly you can find out your own IP address and default gateway.

## ping
Used to send test packet, or echo packet, to a machine to find out whether the machine is reachable and how long the packet takes to reach the machine.

## tracert
Not only tells you whether the packet got to the destination but also tells you all intermediate hops it took to get there.

## netstat
Tells you what connections your computer currently has.

# Knowledge Check
-	Ipconfig – Displays the network configuration of a computer and refreshes DHCP and DNS settings.
-	Ping – Sends a test packet to a machine to find out whether the machine is reachable and how long the packet takes to reach the machine. 
-	Tracert – Determines whether the packet reached the destination, how long it took, and all the intermediate hops it took to get there.
-	Netstat – Discovers the network connections currently present on a computer.

# The OSI Model
-	Application (POP, SMTP, DNS, FTP, Telnet) – This layer interfaces directly to applications and performs common application services for the application process.
-	Presentation (Telnet, Network Data Representation (NDR), Lightweight Presentation Protocol (LPP).
-	Session (NetBIOS) – The session layer provides the mechanism for managing the dialogue between end-user application processes. 
-	Transport (TCP, UDP) – This layer provides end-to-end communication control.
-	Network (IP, ARP, ICMP) – This layer routes the information in the network.
-	Data Link (SLIP, PPP) – This layer describes the logical organization of data bits transmitted on a particular medium. The data link layer is divided into two sublayers: the Media Access Control layer (MAC) and the Logical Link Control layer (LLC).
-	Physical (IEEE 1394, DSL, ISDN) – This layer describes the physical properties of of the various communications media, as well as the electrical properties and interpretation of the exchanged signals. In other words, the physical layer is the actual NIC, Ethernet cable, and so forth. 
# Knowledge Check

-	Transport – TCP, UDP
-	Network – IP, ARP, ICMP
-	Presentation – Telnet, NDR, LPP
-	Application – POP, SMTP, DNS, FTP
-	Session – NetBIOS
-	Data Link – SLIP, PPP
-	Physical – IEEE 1394, DSL, ISDN

# Classifications of Threats
Categories of Attack:
-	Intrusion 
-	Blocking
-	Malware

## Malware
Probably the most common threat to any system. Created to spread on its own. The most obvious example is a computer virus. 

## Compromising System Security – Intrusions 
Intrusions are attacks that are actually trying to intrude into the system. Intrusion attacks are designed to gain access to a specific targeted system and are commonly referred to as hacking. Hackers call this type of attack “cracking”, which means intruding onto a system without permission. Using security flaws or social engineering.

## Denial of Service
The attacker does not actually access the system, but rather simply blocks access to the system for legitimate users. Characterized by an explicit attempt by attackers to prevent legitimate users of a service from using that service. Extremely common, only second to malware. 

# Knowledge Check
-	Intrusion: Includes attacks meant to breach security and gain unauthorized access to a system.
-	Blocking: Includes attacks designed to prevent legitimate access to a system.
-	Malware: Spreads on its own without the involvement of the creator.

# Threat Assessment 
The following numerical scale can provide a basic overview of a system’s security requirements.

Three factors are considered (attractiveness, information content, and security devices present). Each of those factors is given a numeric designation between 1 and 10. The first two are added together, and then the third number is subtracted. The final score ranges from -8 (very low risk, high security) to 19 (very high risk, low security); the lower the number the less vulnerable the system, the higher the number the greater the risk. The best rating for a system that:
-	Receives a 1 in attractiveness to hackers (that is, a system that is virtually unknown, has no political or ideological significance, etc).
-	Receives a 1 in informational content (that is, a system that contains no confidential or sensitive data).
-	Receives a 10 in security ( that is, a system with an extensive layered, proactive security system complete with firewalls, ports blocked, antivirus software, IDS, antispyware, appropriate policies, all workstations and servers hardened, etc.)
# Knowledge Check

Factors while accessing the threat level for an organization:
-	Attractiveness of the system to the hacker
-	 Number of remote connections to the system
-	Nature of the information the system stores

# Security Terminology
-	Firewall – A barrier between a network and the outside world.
-	Access control – The aggregate of all measures taken to limit access to resources.
-	Non-repudiation – Any technique that is used to ensure that someone performing an action on a computer cannot falsely deny that they performed that actions. 
-	Least privileges – Only assign the minimum privileges required for that person to do his job, no more.
-	CIA triangle – Confidentiality, integrity, and availability.

# Knowledge Check
-	Access control – The aggregate of all measures taken to limit privileges of unauthorized personnel to a resource.
-	Non-repudiation – A technique used to ensure that someone performing an action on a computer cannot falsely deny their action.
-	Least privilege – A concept that dictates that the users of a system should only have the level of access necessary to carry out their tasks. 

# Choosing a Network Security Approach
## Perimeter Security Approach
Focus might include firewalls, proxy servers, password policies, and any technology or procedure that makes unauthorized access of the network less likely. 

## Layered Security Approach
A layered security approach is one which not only is the perimeter secured, but the individual systems within the network are also secured. All servers, workstations, routers, and hubs within the network are secure.

## Hybrid Security Approach
Mixture of security approaches.

# Knowledge Check

-	Perimeter – An adequate approach for small organization that do not store sensitive data.
-	Perimeter – A bulk of security efforts are focused on firewalls, proxy servers, password policies, and any technology or procedure.
-	Layered – Secures the perimeter of the network as well as individual systems within the network.
-	Hybrid – Considers approaches to computer security along a Cartesian coordinate system. 

# Network Security and the Law

# Knowledge Check

-	Computer Security Act: Requires government agencies to identify and improve the privacy of sensitive systems.
-	OMB Circular A-130: Describes requirements for developing standards for computer systems and for records held by government agencies. 
-	Sarbanes-Oxley: Governs how publicly traded companies store and report on financial data.
-	HIPPA: Provides data privacy and security provisions for safeguarding medical information.

# Understanding Denial of Service Attacks

## Dos in Action
Lab kinda or whatever:

Simulate a DoS attack by using the `ping` command.

The syntax is: 
```ping ADDRESS -l 65000 -w 0 -t```

This does the following:

-	`-w` option determines how many milliseconds the ping utility will wait for a response from the target. In this case, it is set to `-0`, so it does not wait at all.
-	`-t` option instructs the ping utility to keep sending packets until explicitly told to stop.
-	`-l` option allows users to change the size of the packet you can send. We have set this to be as large as it can.

One machine will likely cause not effect on overloading a server by several could tax the machines capacity and make it slower or not respond. 

A DoS attack that is launched from several different machines is called a distributed denial of services (DDoS).

## SYN Flood

This particular attack depends on the hacker’s knowledge of how connections are made to a server. When a session is initiated between the client and server in a network using the TCP protocol, a small buffer space in memory is set aside on the server to handle the “hand-shaking” exchange of messages that sets up the session. The session-establishing packets include a SYN field that identifies the sequence in the message exchange. 

A SYN flood attempts to subvert this process. In this attack an attacker sends a number of connection requests very rapidly and then fails to respond to the reply that is sent back by thee server. In other words, the attacker requests connections, and then never follows through with the rest of the connection sequence. This has the effect of leaving connections on the server half open, and the buffer memory allocated for them is reserved and not available to other applications. 

## Smurf Attack

The Smurf attack is a popular type of DoS attack. In the Smurf attack, an ICMP packet is sent out to the broadcast address of a network, but its return address has been altered to match one of the computers on that network, most likely a key server. All the computers on the network will then respond by pinging the target computer. 

## Ping of Death

The Ping of Death (PoD), perhaps the simplest and most primitive form of DoS attack, is based on overloading the target system. TCP packets are of limited size. In some cases simply sending a packet that is too large can shut down a target machine. 

## UDP Flood

UDP (User Datagram Protocol) is a connectionless protocol and it does not require any connection setup procedure to transfer data. TCP packets connect and wait for the recipient to acknowledge receipt before sending the next packet. Each packet is confirmed. UDP packets simply send the packets without confirmation. This allows packets to be sent much faster, making it easier to perform a DoS attack.

A UDP flood occurs when an attack sends a UDP packet to a random port on the victim system. When the victim system receives a UDP packet, it will determine what application is waiting on the destination port. When it realizes that no application is waiting on the port, it will generate an ICMP packet of destination unreachable to the forged source address. 

## ICMP Flood

Simply another name for a ping flood using ICMP packets.


## DHCP Starvation
If enough requests flood onto the network, the attacker can completely exhaust the address space allocated by the DHCP servers for an indefinite period of time. There are tools such as Gobbler that will do this for you. Preventing incoming DHCP requests from outside the network will prevent this.

## HTTP Post DoS
An HTTP Post DoS attack sends a legitimate HTTP post message. Part of the post message is the ‘content-length’. This indicates the size of the message to follow. In this attack, the attacker then sends the actual message body at an extremely slow rate. The web server is then “hung” waiting for that message to complete. 

## PDoS
A permanent denial of service (PDoS) is an attack that damages thee system so badly that the victim machine needs either an operating system reinstall or even new hardware. This is sometimes called phlashing.

## Distributed Reflection Denial of Service
As previously stated, distributed denial of service attacks are becoming more common. Most such attacks rely on getting various machines (servers or workstations) to attack the target. The distributed reflection denial of service (DRDoS) is a special type of DoS attack. Rather than getting computers to attack the target, this method tricks Internet routers into attack a target.

Many of the routers on the Internet backbone communicate on port 179. This attack exploits that communication line and gets routers to attack a target system. What makes this attack particularly wicked is that it does not require the routers in question to be compromised in any way. Instead the hacker sends a stream of packets to the various routers requesting a connection. The packets have been altered so that they appear to come from the target system’s IP address. The routers respond by initiating connections with the target system. What occurs is a flood of connections from multiple routers, all hitting the same target system. This has the effect of rendering the target system unreachable. 

# Knowledge Check

-	SYN flood – An attacker sends a number of connection requests very rapidly and then fails to respond to the reply that is sent back by the server.
-	Smurf – An ICMP packet with the intended victim’s spoofed source IP is broadcast to a computer network using an IP broadcast address.
-	Ping of Death – The most primitive form of DoS attack based on overloading the target system with TCP packets.
-	UDP flood – Sends the packets without confirmation which allows packets to be sent much faster.
-	PDoS – Damages the system so badly that the victim machine needs either an operating system reinstall or even new hardware.


# Fundamentals of Firewalls

-	Packet filtering
-	Stateful packet filtering
-	User authentication
-	Client application authentication

At minimum, firewalls will filter incoming packets based on packet size, source IP, protocol, and destination port. 

Both Linux and Windows have a simple firewall built into the operating system.

## Packet Filtering Firewall

-	Most basic firewall.
-	Each incoming packet is examined. 
-	Only those that meet a criteria you set will pass through.
-	Windows and Linux are packet filtering firewalls.

Disadvantages:
-	Do not actually examine the packet or compare it to previous packets; therefore they are quite susceptible to either a ping flood or SYN flood.
-	Do not offer any user authentication.
-	Only looks at packet header for information.

To configure packet filtering firewall, you need to establish appropriate filtering rules. A set of a given firewall would need to cover the following:
-	What types of protocols to allow (FTP, SMTP, POP3, etc.)
-	What source ports to allow
-	What destination ports to allow
-	What source IP addresses to allow (you can block certain IP addresses if you wish)

## Stateful Packet Inspection

-	Improved on basic packet filtering firewall.
-	Examines each packet, denying or permitting access based not only on the examination of the current packet, but also on data derived from previous packets in the conversation. 
-	Less susceptible to ping floods and SYN floods, as well as spoofing.
-	They can tell whether the packet is part of an abnormally large stream of packets from a particular IP address, thus indicating a possible DoS attack in progress.
-	They can tell whether the packet has a source IP address that appears to come from inside the firewall, thus indicating IP spoofing is in progress.
-	They can also look at the actual contents of the packet, allow for some very advanced filtering capabilities.

## Application Gateway

-	Program that runs on a firewall.
-	Other than looking at the protocol and port the packet is using, an application gateway will examine the client application and the server-side application to which it is trying to connect.
-	Enables the administrator to allow access only to certain specified types of applications, such as web browsers or FTP clients.
-	Susceptible to various flooding attacks (SYN flood, ping flood, etc).

## Circuit Level Gateway

-	Similar to application gateways but are more secure and generally implemented on high-end equipment. 
-	Authenticates users first.
-	User’s logon ID and password are checked and the user is granted access before the connection to the router is established.
-	Verification must happen before any further communication can take place.
-	Difficult to configure because each client must be set up to have a circuit connection with the firewall.

## Hybrid Firewalls

-	User a mix of approaches.
-	One example could be a firewall which uses both circuit level gateway and stateful packet filtering.

## Blacklisting/Whitelisting

-	Supported feature by many firewalls.
-	Blacklisting: users can browse any website or resource, except those on the prohibited list.
-	Whitelisting: blocking users from visiting any website or resource except those on an approval list.

# Implementing Firewalls
Most widely used configurations:
-	Network host-based
-	Dual-homed host
-	Router-based firewall
-	Screened host

## Host-based
In host-based scenario the firewall is a software solution installed on an existing machine with an existing operating system. Concern is that no matter how good the firewall solution is, it is contingent upon the underlying operating system. It is critical that the machine hosting the firewall have a hardened operating system. Hardening the operating system refers to taking several security precautions including:
-	Ensuring all patches are updated.
-	Uninstalling unneeded applications or utilities.
-	Closing unused ports.
-	Turning off all unused services.

## Dual-Homed Hosts
-	Running on a server with at least two network interfaces. 
-	Most firewalls today are implemented in actual routers.
-	In dual-homed hosts the firewall is running on a separate server attached to the network.
-	Simply an expanded version of the network host firewall implementation. This option is relatively simple and inexpensive but is dependent on the underlying operating system.

## Router-Based Firewall
-	Often first layer of protection.
-	Usually uses packet filtering. 
-	Usually preconfigured by the vendor based on customers needs.
-	Easy to setup, usually just plug it in.

## Screened Hosts
-	Combination of firewalls.
-	Uses a  bastion host and a screening router.
-	Creates a dual firewall solution that is effective at filtering traffic.
-	Bastion host might be an application gateway and the router might be packet screener (or vice versa).
-	Similar concept to dual-homed host but uses router and server instead of two servers.

# Knowledge Check

Indicate if each of the given statements about the DMZ is true or false:

-	True: It is a type of firewall that consists of two firewalls with an intermediate zone between them. 
-	True: It has an additional layer of protection between Internet-facing services and back-end corporate resources. 
-	False: It hides the internal network from the outside world. 

-	Host-based: A firewall installed on each individual server that controls incoming and outgoing network traffic.

-	Screened host: A combination of firewalls in which any security flaw or misconfiguration affects both firewalls. 

-	Dual-homed host: A firewall that lies between an untrusted network and trusted network to provide secure access.

-	Router-based: An ideal solution for the firewall novice that can be preconfigured by the vendor based on the customer's needs.


# Using Proxy Servers

A proxy server is often used with a firewall to hide the internal network’s IP address and present a single IP address (its own) to the outside world. A proxy server is a server that sits between a client application, such as a web browser, and a real server. Proxy servers prevent hackers from seeing the IP addresses of internal machines.
Using a proxy servers means that when a machine inside the network visits a website, the website will only detect that the proxy server visited it. Even if dozens of different machines on the network visit a site that logs the IP addresses of incoming connections, they will all be logged with the same IP address – that of the proxy server.

Hiding of the network is a very valuable service because knowledge of internal IP addresses can be used to execute certain forms of attack. 

## The WinGate Proxy Server

WinGate is an inexpensive commercial product that also offers a free trial download. This product has all of the standard features of a proxy server including:
-	Internet connection sharing.
-	Hiding internal IP addresses.
-	Allowing virus scanning.
-	Filtering of sites.

## NAT

For many organizations, proxy servers have been superseded by a newer technology known as network address translation (NAT). NAT translates internal addresses and external addresses to allow communication between network computers and outside computers. The outside sees only the address of the machine running NAT (often the firewall). 

NAT also provides significant security because by default it allows only connections that are originated on the inside network. This means that a computer inside the network can connect to an outside web server, but an outside computer cannot connect to a web server inside the network. 


# Using Single Machine Firewalls

-	Single machine firewall solution running on an individual PC (or even a server).
-	Often used to protect computers.

Single machine firewalls have many things in common:
-	These can be packet filtering, SPI, or even application gateways.
-	All are software based.
-	Most are easy to configure and set up.

Designed with the home user in mind.

# Knowledge Check

Features of single machine firewalls:
-	Easy to configure and set up
-	Run on a database or web server
-	Low cost product
-	Software based

# Windows 10 Firewall

-	Stateful packet inspection firewalls.
-	Can set different rules for outbound and inbound traffic.
-	Can set rules for port, programs, custom rules, or one of the many predefined rules that Microsoft has for you to select from.
-	Can choose to only allow via secured by IPSec.
-	Can set rules for three areas or profiles: Doman, Public, and Private.

Administrators should always follow these rules with all packet filtering firewalls:
-	If you do not explicitly need a port, then block it. 
-	Unless you have a compelling reason not to, always block ICMP traffic because many utilities such as ping, tracert, and many port scanners use ICMP packets. 
-	Occasionally, I would suggest continuing to write out acronyms such as ICMP just to make sure this is reinforced.

# Linux Firewalls

## Iptables

-	First widely used Linux firewall was called ipchains.
-	On most Linux systems, iptables is installed as /usr/sbin/iptables.
-	Iptables firewall is made up of three different kinds of objects: tables, chains, and rules.

There are actually three tables and each has some standard rule chains in it. You can, of course, add your own custom rules. The three tables and their standard chains are as follow:

-	Packet Filtering: This table is the essential part of the firewall. It is a packet filtering firewall and it contains three standard chains: INPUT, OUTPUT, and Forward. The INPUT chain processes incoming packets, and the OUTPUT chain processes traffic sent out from the machine. If the firewall system is also acting as a router, only the FORWARD chain applies to routed packets.
-	Network address translation: This table is used for performing network address translation on outbound traffic that initiates a new connection. This is used only if your machine is serving as a gateway or proxy server. 
-	Packet Alteration: This table is used only for specialized packet alteration. It is often called the mangle table because it alters, or mangles, packets. It contains two standard chains. This table might not even be needed for many standard firewalls.

## Symantec Norton Firewall

-	Personal single machine firewall.
-	Pop-up ad blocking and privacy protection.
-	Accomplishes by preventing information about you from being transmitted via the browser without your knowledge.
-	Easy to user UI.
-	Can scan websites for vulnerabilities.



# Understanding IDS Concepts

## Preemptive Blocks
-	Sometimes called banishment vigilance.
-	Done by noting any danger signs of impending threats and then blocking the user or IP address from which they originate.
-	Examples: blocking an address which is doing recon or foot printing.
-	Can be complicated. Could potentially block legitimate user by mistake.
-	Alerts administrator and human administrator will make decision whether to continue to block.

## Anomaly Detection
-	Software that detects intrusion attempts and notifies administrators.
-	Searches for suspicious behavior.
-	Compares observed activity with previous expected normal usage profiles.
-	Locates anomalies.
-	Anomaly is detected by:
o	Threshold monitoring
o	Resource profiling
o	User/group work profiling
o	Executable profiling

### Threshold Monitoring
-	Presets acceptable behavior levels and observes whether these levels are exceeded.
-	Simple as failed login attempts to complex as monitoring the time a user is connected and the amount of data that user downloads.
-	Can be difficult to establish proper threshold values or the proper time frames at which to check those threshold values.
-	Can result in high rate of false positives.

### Resource Profiling
-	Measures system-wide use of resources and develops a historic usage profile.
-	Monitors how a user normally utilizes system resources.
-	Triggers if abnormal amount of resources are being used.
-	Can be difficult to interpret the meaning of system and resource usage, leading to false positives. 

### User/Group Work Profiling
-	Maintains individual work profiles about users and groups.
-	Users and groups are expected to adhere to there profiles.
-	If the user changes their activity, their work profile will update to reflect.
-	Short-term and long-term profiles.
-	Can be difficult to profile irregular or dynamic user base.
-	Profiles defined too broadly enable any activity to pass.

### Executable Profiling
-	Seeks to measure and monitor how programs use system resources with attention to those whose activity cannot always be traced to a specific originating user.
-	Malware is addressed by profiling how system objects such as files and printers are normally used not only by users but also by other system objects on part of the users.

# Knowledge check
Indicate if each of the given statements about preemptive blocking is true or false.

-	True: It is sometimes called as banishment vigilance and seeks to prevent intrusions before they occur.
-	True: It may block a legitimate user by mistake.
-	False: It involves actual software that detects intrusion attempts and notifies the administrator.


# IDS Components and Processes 
-	An activity is an element of a data source that is of interest to the operator.
-	The administrator is the person responsible for organizational security.
-	A sensor is the IDS component that collects data and passes it to the analyzer for analysis.
-	The analyzer is the component or process that analyzes the data collected by the sensor.
-	An alert is a message from the analyzer indicating that an event of interest has occurred.
-	The manager is the part of the IDS used to manage, for example a console.
-	Notification is the process or method by which the IDS manager makes the operator aware of an alert.
-	The operator is the person primarily responsible for the IDS. This is often the administrator.
-	An event is an occurrence that indicate a suspicious activity may have occurred.
-	The data source is the raw information that the IDS uses to detect suspicious activity.


# Understanding and Implementing Honeypots
-	Specter – honeypot solution.
-	Works by appearing to run a number of services common to network servers.

## Symantec Decoy Server
-	Appeared to be a real server, such as simulating incoming and outgoing email traffic.
-	Decoy server acts as a honeypot.


## Intrusion Deflection
-	Makes a subsystem look more attractive to bring attacker’s attention there.


# Encryption Fundamentals

### Caesar Cipher
-	Oldest encryption – believed to be used by the Roman emperors.
-	Shifts a few characters on the alphabet to hide messages.

### ROT 13
-	Single alphabet substitution cipher. All characters are rotated 13 characters through the alphabet.

### Atbash Cipher
-	Reverses the alphabet.

### Multi-Alphabet Substitution
-	Slightly improved version of Caesar cipher.
-	Multiples numbers by which to shift letters.

### Rail Fence
-	May be the most widely known transposition cipher.
-	Takes the message you wish to encrypt and alters each letter on a different row.

### Vigenere
-	Polyalphabetic – uses multiple shifts.

### Enigma 
-	Rotors, or disks, that were arranged in a circle with 26 letters on them.
-	The rotors were lined up.
-	Mechanical polyalphabetic cipher.

### Binary Operations
-	Just binary
-	Uses AND, OR, and XOR


# Learning About Modern Encryption Methods

### Symmetric Encryption
-	Data Encryption Standard (DES)
o	DES uses a symmetric key system.
o	Data is divided into 64-bit blocks, and those blocks are then transposed.
o	Transposed data is then manipulated by 16 separate rounds of encryption, involving substitutions, bit-shifting, and logical operations using a 56-bit key.
o	Finally, the data is transposed one last time.
-	Blowfish
o	Symmetric block cipher.
o	Uses a single key to both encrypt and decrypt the message and works on “blocks” of the message at a time.
-	AES
o	Uses Rijndael algorithm.
o	Three key sizes: 128, 192, and 256.
o	Uses a block cipher.
-	Key Stretching
o	PBKDF2: applies a function like a hash or HMAC to the password or passphrase along with salt to produce a derived key.
o	bcrypt: is used with passwords, and it essentially uses a derivation of the Blowfish algorithm, converted to a hashing algorithm, to hash a password and add salt to it.
-	Public Key Encryption
o	RSA

No encryption code is unbreakable. Every encryption code can be broken.

# Understanding Digital Signatures and Certificates
-	Digital signature is used to guarantee who send a message (non-repudiation).
-	Digital signature reverse the asymmetric encryption process.
-	Sender encrypts something with his or her private key.
-	If the recipient is able to decrypt that with the sender’s public key, then it must have been sent by the person.

### Digital Certificates
-	Contains a public key and some means to verify whose public key it is.
-	Certificate authority issues digital certificates.
