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
-	Multifactor authentication systems are when two or more authentications methods (what a user knows, what a user owns, and who a user is) are being implemented.
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
