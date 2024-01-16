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
