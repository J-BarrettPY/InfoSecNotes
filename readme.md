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

Ingress – Traffic that originates from outside the network’s routers and proceeds toward a destination inside the network.
Egress – Helps ensure that unauthorized or malicious traffic never leaves the internal networks.
Egress – Traffic that begins inside a network and proceeds through its routers to its destination somewhere outside of the network.
Ingress – Makes internet traffic traceable to its source. 

## Social Engineering
- True – Social engineering is a method used to gain access to data, systems, or networks, primarily through misrepresentation.
- False – This technique typically relies on the trusting nature of the person who is attacking.
- True – The attacker will ask a number or questions in an attempt to identify possible avenues to exploit during this attack.
- True – These attacks can be perpetrated in person, through email, or via phone. 














