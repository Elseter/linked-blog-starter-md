
---
aliases: [ "20230831155037",  ]
tags: SEC.203, SEC, TestOutSec
date_created: 2023-08-31 15:50
---
[[SEC.203 Index]]
# TestOut Security Pro Quiz Answers
---
## Module 1 - Introduction
### 1.1 Section Quiz
1. **A user copies files from her desktop computer to a USB flash device and puts the device into her pocket. Which of the following security risks is most pressing?**
	1. ==Confidentiality==
	2. Availability
	3. Non-repudiation
	4. Integrity 
		- **Explanation**
		- Confidentiality ensures that data is not disclosed to unintended persons. Removable media poses a big threat to confidentiality because it makes it easy to remove data and share it with unauthorized users.
		- Availability ensures that data is available when it is needed. Copying files to a server that includes malware could threaten the data's availability if the malware deletes or corrupts the data.
		- Integrity ensures that data is not modified or tampered with.
		- Non-repudiation provides validation of a message's origin.

2. **Which of the following BEST describes a cyber terrorist?**
	1. Desires some kind of financial reward or revenge
	2. ==Disrupts network-dependent institutions==
	3. Downloads and runs attacks available on the internet
	4. Exploits internal vulnerabilities to steal information
		- **Explanation**
		- Cyber terrorists generally use the internet to carry out terrorist activities such as disrupting network-dependent institutions.
		- Downloading and running attacks available on the internet is usually a script kiddie activity.
		- Cybercriminals are after some kind of financial reward or revenge.
		- A spy applies for a job with a commercial competitor and then exploits internal vulnerabilities to steal information.

3. **Your computer system is a participant in an asymmetric cryptography system. You've created a message to send to another user. Before transmission, you hash the message and encrypt the hash using your private key. You then attach this encrypted hash to your message as a digital signature before sending it to the other user. In this example, which protection does the hashing activity provide?**
	1. ==Integrity==
	2. Confidentiality
	3. Availability
	4. Non-repudiation
		- **Explanation**
		- Hashing of any sort, including within a digital signature, provides data integrity. Signing the message with the private key creates non-repudiation. A digital signature activity, as a whole, does not provide protection for confidentiality because the original message is sent in cleartext. No form of cryptography provides protection for availability.

4. **Which of the following is an example of an internal threat?**
	1. ==A user accidentally deletes the new product designs.==
	2. A server backdoor allows an attacker on the internet to gain access to the intranet site.
	3. A water pipe in the server room breaks.
	4. A delivery man is able to walk into a controlled area and steal a laptop.
		- **Explanation**
		- Internal threats are intentional or accidental acts by employees, including:
			- Malicious acts such as theft, fraud, or sabotage
			- Intentional or unintentional actions that destroy or alter data
			- Disclosing sensitive information through snooping or espionage
		- External threats are events that originate outside of the organization. They typically focus on compromising the organization's information assets. Examples of external threats include hackers, fraud perpetrators, and viruses.
		- Natural events are events that may reasonably be expected to occur over time, such as a fire or a broken water pipe.

5. **Which of the following could an employee also be known as?**
	1. Cybercriminal
	2. Script kiddie
	3. Exploit
	4. ==Internal threat==
		- **Explanation**
		- Employees are also known as internal threats. Employees can be the most overlooked, yet most dangerous, threat agent because they have greater access to information assets than anyone on the outside trying to break in.
		- An exploit is a procedure or product that takes advantage of a vulnerability to carry out a threat.
		- Script kiddies download and run attacks available on the internet.
		- Cybercriminals usually seek to exploit security vulnerabilities for some kind of financial reward or revenge.

6. **By definition, which security concept uses the ability to prove that a sender undeniably sent an encrypted message?**
	1. Authentication
	2. ==Non-repudiation==
	3. Integrity
	4. Privacy
		- **Explanation**
		- The ability to prove that a sender undeniably sent a message is known as non-repudiation. By various mechanisms in different cryptographic solutions, you can prove that only the sender would be able to have initiated a certain communication. Therefore, the sender cannot repute that they originated a message.
		- Integrity is protection against alteration. Authentication is the assignment of access privileges to users.
		- Privacy is the protection and confidentiality of personal information.

7. **Which of the following includes all hardware and software necessary to secure data, such as firewalls and antivirus software?**
	1. Assets
	2. ==Physical security==
	3. Policies
	4. Users and administrators
		- **Explanation**
		- Physical security includes all hardware and software necessary to secure data, such as firewalls and antivirus software.
		- Users and administrators are the people who use the software and the people who manage the software, respectively.
		- Policies are the rules an organization implements to protect information.
		- An asset is something that has value to a person or organization, such as sensitive information in a database.

8. **Which of the following are often identified as the three main goals of security? (Select three.)**
	- Assets
	- Non-repudiation
	- ==Availability==
	- Employees
	- ==Integrity==
	- Policies
	- ==Confidentiality==
		- **Explanation**
		- The acronym CIA refers to confidentiality, integrity, and availability in respect to security. These are often identified as the three main goals of any security-oriented task.
		- Non-repudiation provides validation of a message's origin.
		- Policies are the rules an organization implements to protect information.
		- Employees can be the most overlooked, yet most dangerous, threat agent because they have greater access to information assets than anyone on the outside trying to break in.
		- An asset is something that has value to a person or organization, such as sensitive information in a database.

9. **Which of the following is the correct definition of a threat?**
	1. The likelihood of an attack taking advantage of a vulnerability
	2. Instance of exposure to losses from an attacker
	3. Absence or weakness of a safeguard that could be exploited
	4. ==Any potential danger to the confidentiality, integrity, or availability of information or systems==
		- **Explanation**
		- A threat is any potential danger to the confidentiality, integrity, or availability of information or systems.
		- Risk is the likelihood of a threat taking advantage of a vulnerability.
		- A vulnerability is the absence or weakness of a safeguard that could be exploited.
		- An exposure is an instance of exposure to losses from a threat agent.

10. **Which of the following is an example of a vulnerability?**
	1. Denial-of-service attack
	2. Virus infection
	3. Unauthorized access to confidential resources
	4. ==Misconfigured server==
		- **Explanation**
		- A misconfigured server is a vulnerability. A vulnerability is the absence or weakness of a safeguard that could be exploited, such as a USB port that is enabled on the server hosting the database.
		- All of the other selections are examples of exposures. An exposure is an instance of exposure to losses from a threat agent.

---
### 1.2 Quiz

1. **The Application layer of the security model includes which of the following? (Select two.)**
	- Log management
	- ==User management==
	- User education
	- Environmental controls
	- ==Web application security==
		- **Explanation**
		- The Application layer includes user management and web application security. 
		- The Policies, Procedures, and Awareness layer includes user education.
		- The Physical layer includes environmental controls.
		- The Host layer includes log management.

2. **When training your employees on how to identify various attacks, which of the following policies should you be sure to have and enforce? (Select two.)**
	- ==Password policies==
	- Usage policies
	- Encryption policies
	- Group policies
	- ==Clean desk policies==
		- **Explanation**
		- Be sure to have an effective password policy and clean desk policy in place, and don't forget to enforce them. Be sure to train your employees on how to identify all the various attacks that could target them. Train them on how to spot suspicious emails, instant messages, downloads, attachments, and websites.
		- Encryption policies should protect you in the event you experience a physical security breach. For example, if a hard drive were stolen, the thief wouldn't be able to access the information stored on it.
		- An Acceptable Use Policy (AUP) determines the rules for using a website or internet service.
		- You can use Windows group policies to administer your Windows systems.

3. **Which of the following reduces the risk of a threat agent being able to exploit a vulnerability?**
	1. Manageable network plans
	2. Implementation of VLANs
	3. ==Countermeasures==
	4. Secure data transmissions
		- **Explanation**
		- A countermeasure is a means of mitigating potential risk. Countermeasures reduce the risk of a threat agent being able to exploit a vulnerability. An appropriate countermeasure:
			- Must provide a security solution to an identified problem
			- Should not depend on secrecy
			- Must be testable and verifiable
			- Must provide uniform or consistent protection for all assets and users
			- Should be independent of other safeguards
			- Should require minimal human intervention
			- Should be tamper-proof
			- Should have overrides and fail-safe defaults

4. **Which of the following items would be implemented at the Data layer of the security model?**
	1. Auditing
	2. Group policies
	3. ==Cryptography==
	4. Authentication
		- **Explanation**
		- Cryptography is implemented at the Data layer.
		- Authentication, authorization, and group policies are implemented at the Application layer.
		- Auditing is implemented at the Host layer.

5. **Which of the following items would you secure in the Perimeter layer of the security model?**
	1. VLANs
	2. ==Firewalls==
	3. Switches
	4. Routers
		- **Explanation**
		- Firewalls using ACLs are secured in the Perimeter layer.
		- Switches, routers, and VLANs are secured in the Network layer.

6. **Which of the following is the single greatest threat to network security?**
	1. Email phishing
	2. Weak passwords
	3. ==Employees==
	4. Unsecure physical access to network resources
		- **Explanation**
		- Employees are the single greatest threat to network security. Therefore, user education is very important.
			- Employees need to be aware that they are the primary targets in most attacks.
			- Phishing attacks are one of the most common attacks directed toward employees.
			- Employees should be able to identify attacks through email, instant messages, downloads, and websites.
			- Effective password policies should be enforced, and passwords should not be written down.
			- Employees should be able to identify both internal and external threats.
			- Employees need to be aware of the company's security policies.

7. **Which of the following is a security approach that combines multiple security controls and defenses?**
	1. Countermeasure security
	2. Perimeter security
	3. Cumulative security
	4. ==Layered security==
	5. Network security
		- **Explanation**
		- Layered security, sometimes called defense in depth security, is a security approach that combines multiple security controls and defenses to create a cumulative effect.
		- Perimeter security includes firewalls with ACLs and a wireless network. 
		- Network security includes the installation and configuration of switches and routers, the implementation of VLANs, penetration testing, and the utilization of virtualization. 
		- A countermeasure is a means of mitigating a potential risk. Countermeasures reduce the risk of a threat agent exploiting a vulnerability.

8. **Which of the following items would be implemented at the Network layer of the security model?**
	1. Firewalls using ACLs
	2. Network plans
	3. ==Penetration testing==
	4. Wireless networks
		- **Explanation**
		- The installation and configuration of switches and routers, the implementation of VLANs, penetration testing, and virtualization are implemented at the Network layer.
		- Firewalls with ACLs and wireless networks are secured in the Perimeter layer.
		- Network plans are implemented at the Policies, Procedures, and Awareness layer.

9. **Which of the following is one of the MOST common attacks on employees?**
	1. Remote attack
	2. ==Phishing attack==
	3. DNS attack
	4. Password attack
		- **Explanation**
		- Phishing attacks are one of the most common attacks directed at employees. In most cases, employees are lured into clicking a link or downloading an attachment from a seemingly legitimate email.

10. **The Policies, Procedures, and Awareness layer of the security model includes which of the following? (Select two.)**
	- Environmental controls
	- ==User education==
	- Motion detectors
	- ==Employee onboarding==
	- Server cages
		- **Explanation**
		- User education and employee onboarding and off-boarding procedures are included in the Policies, Procedures, and Awareness layer.
		- The Physical layer deals with server cages, motion detectors, and environmental controls.

--- 
## Module 2
### 2.1 Quiz

1. **An employee stealing company data could be an example of which kind of threat actor?**
	1. External threat
	2. Persistent threat
	3. Non-persistent threat
	4. ==Internal threat==
		- Explanation
		- An internal threat consists of someone like an employee that uses their authorized privileges to carry out an attack.
		- A persistent threat is one that has a goal of remaining undetected and retaining access. While an internal threat could also be persistent, it does not need to be.
		- A non-persistent threat is generally a one-time event in which the malicious actor doesn't care if the attack is noticed. Again, it could also be an internal threat, but an internal threat does not necessarily have to be non-persistent.
		- An external threat attacks from the outside and seeks to gain unauthorized access to data.

2. **Which of the following is the BEST definition of the term _hacker?_**
	1. Any individual whose attacks are politically motivated.
	2. The most organized, well-funded, and dangerous type of threat actor.
	3. A threat actor who lacks skills and sophistication but wants to impress their friends or garner attention.
	4. A threat actor whose main goal is financial gain.
	5. ==A general term used to describe any individual who uses their technical knowledge to gain unauthorized access to an organization.==
		- Explanation
		- The term _hacker_ is a general term used to describe any individual who uses their technical knowledge to gain unauthorized access to an organization.
		- The following are specific types of hackers, also known as threat actors:
			- A hacktivist is any individual whose attacks are politically motivated.
			- A nation state is the most organized, well-funded, and dangerous type of threat actor.
			- An organized crime threat actor is a group of cybercriminals whose main goal is financial gain.
			- A script kiddie is a threat actor who lacks skills and sophistication but wants to impress their friends or garner attention. Script kiddies carry out an attack by using scripts or programs written by more advanced hackers.

3. **Which of the following threat actors seeks to defame, shed light on, or cripple an organization or government?**
	1. ==Hacktivist==
	2. Competitor
	3. Insider
	4. Script kiddie
	5. Nation state
		- Explanation
		- A hacktivist is any individual whose attacks are politically motivated. Instead of seeking financial gain, hacktivists want to defame, shed light on, or cripple an organization or government. Hacktivists often work alone. Occasionally, they create unified groups with like-minded hackers. For example, the website wikileaks.org is a repository of leaked government secrets, some of which have been obtain by hacktivists.
		- Script kiddies are usually motivated by the chance to impress their friends or garner attention in the hacking community. Insider threat actors can be motivated by negative feelings toward their employer, bribes from a competitor, or personal financial gain. Competitors could be motivated by financial gain, competitor defamation, or obtaining industry secrets.
		- There are two primary motives for nation state attacks, seeking to obtain sensitive information (such as government secrets) or seeking to cripple the target's network or infrastructure.

4. **The IT manager in your organization proposes taking steps to deflect a potential threat actor. The proposal includes the following:**
	- Create and follow onboarding and off-boarding procedures.
	- Employ the principal of least privilege.
	- Have appropriate physical security controls in place
	- Which type of threat actor do these steps guard against?
	1. ==Insider==
	2. Script kiddie
	3. Hacktivist
	4. Competition
		- Explanation
		- Because insiders are one of the most dangerous and overlooked threats to an organization, you need to take the appropriate steps to protect against them, such as requiring mandatory vacations, creating and following onboarding and off-boarding procedure, employing the principal of least privilege, and having appropriate physical security controls in place.
		- A script kiddie is an individual who carries out an attack by using scripts or programs written by more advanced hackers.
		- A hacktivist is any individual whose attacks are politically motivated.
		- A competitor threat actor carries out attacks on behalf of an organization and targets competing companies.

5. **A script kiddie is a threat actor who lacks knowledge and sophistication. Script kiddie attacks often seek to exploit well-known vulnerabilities in systems.** **What is the BEST defense against script kiddie attacks?**
	1. Properly secure and store data backups.
	2. Build a comprehensive security approach that uses all aspects of threat prevention and protection.
	3. Have appropriate physical security controls in place.
	4. ==Keep systems up to date and use standard security practices.==
	5. Implement email filtering systems.
		- Explanation
		- Because script kiddies lack knowledge and sophistication, their attacks often seek to exploit well-known vulnerabilities in systems. As such, defense against script kiddies involves keeping systems up-to-date and using standard security practices.
		- Having appropriate physical security controls in place is one of the steps that can be used to protect insider threat actors. Implementing email filtering systems and proper securing and storing data backups are two of the steps that can be used to protect against organized crime threat actors.
		- Because nation states use so many different attack vectors and unknown exploits, defending against these attacks involves building a comprehensive security approach that uses all aspects of threat prevention and protection.

6. **A hacker scans hundreds of IP addresses randomly on the internet until they find an exploitable target. What kind of attack is this?**
	1. Nation state attack
	2. ==Opportunistic attack==
	3. Insider attack
	4. Targeted attack
		- Explanation
		- In this scenario, the hacker is looking for an easy target and doesn't care what they are attacking. This is considered an opportunistic attack.
		- If the hacker had been targeting a certain individual, company, organization, or nation, it would have been considered a targeted attack.
		- An insider attack is accomplished by a threat agent who has authorized access to an organization and either intentionally or unintentionally carries out an attack.
		- A nation state attack is accomplished by a threat agent that is a sovereign state who may wage an all-out war on a target and have significant resources and money at their disposal.

7. **Match the general attack strategy on the left with the appropriate description on the right. (Each attack strategy may be used once, more than once, or not all.)**
	1. Stealing information.
		- ==Exploitation==
	2. Preparing a computer to perform additional tasks in the attack.
		- ==Staging==
	3. Crashing systems.
		- ==Exploitation==
	4. Gathering system hardware information.
		- ==Reconnaissance==
	5. Penetrating system defenses to gain unauthorized access.
		- ==Breaching==
	6. Configuring additional rights to do more than breach the system.
		- ==Escalating privileges==

8. **Match the general defense methodology on the left with the appropriate description on the right. (Each methodology may be used once, more than once, or not all.)**
	1. The constant change in personal habits and passwords to prevent anticipated events and exploitation.
		- ==Randomness==
	2. Diversifying layers of defense.
		- ==Variety==
	3. Giving users only the access they need to do their job and nothing more.
		- ==Principle of least privilege==
	4. Implementing multiple security measures to protect the same asset.
		- ==Layering==
	5. Eliminating single points of failure.
		- ==Layering==
	6. Giving groups only the access they need to do their job and nothing more.
		- ==Principle of least privilege==

9. Which of the following is the BEST example of the principle of least privilege?
	1. Lenny has been given access to files that he does not need for his job.
	2. Jill has been given access to all of the files on one server.
	3. Mary has been given access to all of the file servers.
	4. ==Wanda has been given access to the files that she needs for her job.==
		- Explanation
		- Wanda being given access only to what she needs to do her job is an example of the principle of least privilege.
		- The principle of least privilege states that users or groups are given only the access they need to do their jobs and nothing more.

10. **In which phase of an attack does the attacker gather information about the target?**
	1. Breach the system
	2. ==Reconnaissance==
	3. Exploit the system
	4. Escalating privileges
		- Explanation
		- Reconnaissance is the phase of an attack where the attacker is gathering information about the target. This can be done electronically using scanning tools or even physically by going through dumpsters.
		- Escalation of privileges comes at the end of the attack when the attacker gains access to unauthorized data.
		- Breaching or exploiting the system is when the attacker gains access to a system on the target network using a vulnerability.

---
### 2.2 Quiz
1. A collection of zombie computer have been set up to collect personal information. Which type of malware do the zombie computers represent?
	- ==Botnet==

2. Which kind of virus operates only in memory and usually exploits a trusted application like PowerShell to circumvent traditional endpoint security solutions
	- ==Fileless Virus==

3. Which of the following describes a logic bomb?
	- ==A program that preforms a malicious activity at a specific time or after a triggering event==

4. A type of malware that prevents the system from being used until the victim pays the attacker money is known as what?
	- ==Ransomware==

5. Which kind of malware provides an attacker with administrative control over a target computer through a backdoor?
	- ==Remote Access Trojan (RAT)==

6. Which of the following are characteristic of a rootkit?
	- ==Resides below regular antivirus software detection==
	- ==Requires administrator-level privileges for installation==

7. Which of the following best describes spyware?
	- ==It monitors the actions you take on your machine and sends the information back to its originating source ==

8. Which of the following is a program that appears to be a legitimate application, utility, game, or screensaver, but preforms malicious activities surreptitiously
	- ==Trojan Horse==

9. In 2001, a worm exploited vulnerabilities in Microsoft Internet Information Services (IIS) to infect over 250,000 systems in under nine hours. What was this worm called?
	- ==Code Red==

10. You have installed antivirus software on the computers on your network. You update the definition and engine files and configure the software to update those files every day. What else should you do to protect your systems from malware?
	- ==Schedule regular full-system scans==
	- ==Educate users about malware==

---
### 2.3 Quiz
1. Ron, a hacker, wants to get access to a prestigious law firm he has been watching for a while. June, an administrative assistant at the law firm, is having lunch at the food court around the corner from her office. Ron notices that June has a picture of a dog on her phone. He casually walks by and starts a conversation about dogs. Which phase of the social engineering process is Ron in?
	- ==Development Phase==

2. Social engineers are master manipulators. Which of the following are tactics they might use?
	- ==Moral obligation, ignorance, and threatening==

3. Any attack involving human interaction of some kind is referred to as what?
	- ==Social Engineering==

4. An organization's receptionist received a phone call from an individual claiming to be a partner in a high-level project and requesting sensitive information. The individual is engaging in which type of social engineering?
	- ==Authority==

5. Which of the following is a common social engineering attack?
	- ==Distributing hoax virus-information emails==

6. Which of the following BEST describes an inside attacker?
	- ==An unintentional threat actor. This is the most common threat.==

7. Which of the following are examples of social engineering attacks? (Select three.)
	- ==Shoulder Surfing==
	- ==Impersonation==
	- ==Keylogging==

8. Compliments, misinformation, feigning ignorance, and being a good listener are tactics of which social engineering technique?
	- ==Elicitation==

9. Pretending to be somebody else and approaching a target to extract information is called what?
	- ==Impersonation==

10. Jason is at home, attempting to access the website for his music store. When he goes to the website, it has a simple form asking for a name, email, and phone number. This is not the music store website. Jason is sure the website has been hacked. How did the attacker accomplish this hack?
	- ==DNS cache poisoning==

---
### 2.4 Quiz

1. Every ACME computer comes with the same account created at the factory. Which kind of vulnerability is this?
	- ==Default accounts and passwords==

2. In healthcare, regulations often dictate that important systems remain unpatched to maintain compliance. Which kind of vulnerability does this introduce?
	- ==Inherent vulnerabilities==

3. Which security control, if not applied, can allow an attacker to bypass other security controls?
	- ==Physical access control==

4. A user is able to access privileged administrative features with an account that is not granted administrator rights. Which type of vulnerability is this?
	- ==Privilege escalation==

5. The root account has all privileges and no barriers. Which of the following is another name for the root account?
	- ==Superuser account==

6. A wireless access point configured to use Wired Equivalent Privacy (WEP) is an example of which kind of vulnerability?
	- ==Weak security configurations==

7. Sometimes, an attacker's goal is to prevent access to a system rather than to gain access. This form of attack is often called a denial-of-service attack and causes which impact?
	- ==Availability loss==

8. When confidential or protected data is exposed, either intentionally or accidentally, it is considered to be which of the following?
	- ==Data breach==

9. DNS tunneling is a common method that allows an attacker to accomplish which attack?
	- ==Data exfiltration==

10. Which impact of vulnerabilities occurs when an attacker uses information gained from a data breach to commit fraud by doing things like opening new accounts with the victim's information?
	- ==Identity theft==

--- 
## Module 3
### Quiz 3.1

1. Which of the following are solutions that address physical security? (Select two.)
	- ==Escort Visitors at all times==
	- ==Require identification and name badges for all employees==

2. You are the security administrator for a small business. The floor plan for your organization is shown in the figure below. You've hired a third-party security consultant to review your organization's security measures. She has discovered multiple instances where unauthorized individuals have gained access to your facility, even to very sensitive areas. She recommends that you provide employees with access badges and implement access badge readers to prevent this from happening in the future. Click on the office locations where access badge readers would be most appropriate.
	![[Screenshot 2023-09-13 111456.png]]

3. If a fingerprint or retina scan is required to open a secured door, which kind of physical security has been implemented?
	- ==Biometric locks==

4. Which option is a benefit of CCTV?
	- ==Expand the area visible by security guards==

5. You want to use CCTV to increase your physical security, and you want the ability to remotely control the camera position. Which camera type should you choose?
	- ==PTZ==

6. Which of the following controls is an example of a physical access control method?
	- ==Locks on doors==

7. Which of the following can be used to stop piggybacking at a front entrance where employees should swipe smart cards to gain entry?
	- ==Deploy a mantrap==

8. After a security event that involves a breach of physical security, what is the term used for the new measures, incident review, and repairs meant to stop a future incident from occurring?
	- ==Recovery==

9. Which kind of access control technology allows more than just the identity of an individual to be transmitted wirelessly to either allow or deny access?
	- ==Smart Card==

10. Which of the following allows an easy exit of an area in the event of an emergency, but also prevents entry? (Select two.)
	- ==Double-entry door==
	- ==Turnstile==

---
### Quiz 3.2

1. Your company has five salesmen who work out of the office and frequently leave their laptops laying on their desks in their cubicles. You are concerned that someone might walk by and take one of these laptops. Which of the following is the BEST protection implementation to address your concerns?
	- ==Use cable locks to chain the laptops to the desks==

2. Your networking closet contains your network routers, switches, bridges, and some servers. You want to make sure an attacker is not able to gain physical access to the equipment in the networking closet. You also want to prevent anyone from reconfiguring the network to set up remote access or backdoor access. Which of the following measures are the best ways to secure your networking equipment from unauthorized physical access? (Select two. Each measure is part of a complete solution.)
	- ==Place your networking equipment in a room that requires key card entry.==
	- ==Place your networking equipment in a locked cage.==

3. You are an IT consultant. You are visiting a new client's site to become familiar with their network. As you walk around their facility, you note the following:
	- When you enter the facility, a receptionist greets you and escorts you through a locked door to the work area where the office manager sits.
	- The office manager informs you that the organization's servers are kept in a locked closet. An access card is required to enter the server closet.
	- She informs you that server backups are configured to run each night. A rotation of tapes are used as the backup media.
	- You notice the organization's network switch is kept in the server closet.
	- You notice that a router/firewall/content filter all-in-one device has been implemented in the server closet to protect the internal network from external attacks.
	- The office manager informs you that her desktop system no longer boots and asks you to repair or replace it, recovering as much data as possible in the process. You take the workstation back to your office to work on it.
	Which security-related recommendations should you make to this client?
	- ==Implement a hardware checkout policy.==

4. Which of the following is the most important thing to do to prevent console access to the router?
	- ==Keep the router in a locked room.==

5. Burning, pulping, and shredding are three ways to securely dispose of data in which form?
	- ==Paper==

6. A computer or small network that is not connected to the rest of the network or the internet is known as:
	- ==Air Gap==

7. Which device is used to allow a USB device to charge but blocks the data transfer capabilities of the device?
	- ==USB data blocker==

8. Which device is often employed by power companies to protect cabling infrastructure from having cables added or removed and to prevent emissions from being retrieved from the air?
	- ==PDS==

9. Which special network area is used to provide added protection by isolating publicly accessible servers?
	- ==DMZ==

10. A Faraday cage is used to prevent what from leaving an area?
	- ==Electromagnetic emissions==

---
### Quiz 3.3

1. It is important to follow correct procedures when running electrical cables next to data cables in order to protect against which environmental concern?
	- ==Electromagnetic Interference==

2. Most equipment is cooled by bringing cold air in the front and ducting the heat out of the back. What is the term for where the heat is sent in this type of scenario?
	- ==Hot aisle==

3. What is the recommended humidity level for server rooms?
	- ==50%==

4. Which deviation in power is the longest in duration?
	- ==Blackout==

5. Power, heating, ventilation, air conditioning systems (HVAC), and utilities are all components of which term?
	- ==Infrastructure==

6. You maintain a network for an industrial manufacturing company. You are concerned about the dust in the area getting into server components and affecting network availability. Which of the following should you implement?
	- ==Positive pressure system==

7. Components within your server room are failing at a rapid pace. You discover that the humidity in the server room is at 60% and the temperature is at 80 degrees. What should you do to help reduce problems?
	- ==Add a separate A/C unit in the server room==

8. Which device is used to ensure power to a server or network device during short power outages?
	- ==Uninterruptible power supply==

9. Which of the following fire extinguisher types is best used for the electrical fires that might result when working with computer components?
	- ==Class C==

10. You walk by the server room and notice that a fire has started. What should you do first?
	- ==Make sure everyone has cleared the area==

---
## Module 4
### Quiz 4.1 

1. You have hired 10 new temporary workers who will be with the company for three months. You want to make sure that the user accounts cannot be used for login after that time period. What should you do?
	- ==Configure account expiration in the user accounts.==

2. Which Microsoft tool can be used to review a system's security configuration against recommended settings?
	- ==Microsoft Security Compliance Toolkit==

3. Which type of update should be prioritized even outside of a normal patching window?
	- ==Critical updates==

4. Prepare to Document means establishing the process you will use to document your network. Which of the following makes this documentation more useful?
	- ==Have a printed hard copy kept in a secure location.==

5. Documenting procedures and processes are part of which milestone in the NSA's Manageable Network Plan?
	- ==Document Your Network==

6. In which milestone should you use a network scanner and then confirm the scan manually with a room-by-room walkthrough?
	- ==Map Your Network==

7. Windows Server Update Services (WSUS) is used to accomplish which part of a manageable network?
	- ==Patch Management==

8. You have recently been hired as the new network administrator for a startup company. The company's network was implemented prior to your arrival. One of the first tasks you need to complete in your new position is to develop a manageable network plan for the network. You have already completed the first and second milestones, in which documentation procedures were identified and the network was mapped. You are now working on the third milestone, which is identifying ways to protect the network. Which tasks should you complete as a part of this milestone? (Select two.)
	- ==Identify and document each user on the network.==
	- ==Physically secure high-value systems.==

9. For Milestone 4 (Reach Your Network), which of the following would be considered a secure protocol to use to reach your network?
	- ==SSH==

10. As you go through the process of making your network more manageable, you discover that employees in the sales department are on the same network segment as the human resources department. Which of the following steps can be used to isolate these departments?
	- ==Create a separate VLAN for each department.==

---
### Quiz 4.2

1. Which of the following tools can you use on a Windows network to automatically distribute and install software and operating system patches on workstations? (Select two.)
	- ==WSUS==
	- ==Group Policy==

2. Which of the following describes a configuration baseline?
	- ==A list of common security settings that a group or all devices share==

3. What should you consider security baselines?
	- ==Dynamic==

4. By definition, what is the process of reducing security exposure and tightening security controls?
	- ==Hardening==

5. Which of the following is the strongest form of multi-factor authentication?
	- ==A password, a biometric scan, and a token device==

6. You have recently experienced a security incident with one of your servers. After some research, you determine that a new hotfix has recently been released, which would have protected the server. Which of the following recommendations should you follow when applying the hotfix?
	- ==Test the hotfix and then apply it to all servers.==

7. Which of the following actions should you take to reduce the attack surface of a server?
	- ==Disable unused services==

8. Which of the following do security templates allow you to do? (Select two.)
	- ==Configure consistent security settings between devices==
	- ==Quickly apply settings to multiple computers==

9. You have just purchased a new network device and are getting ready to connect it to your network. Which of the following actions should you take to increase its security? (Select two.)
	- ==Change default account passwords.==
	- ==Apply all patches and updates.==

10. Which of the following is defined as an operating system that comes hardened and validated to a specific security level as defined in the Common Criteria for Information Technology Security Evaluation (CC)?
	- ==TOS==

---
### Quiz 4.3

1. You have placed a File Transfer Protocol (FTP) server in your DMZ behind your firewall. The FTP server is to be used to distribute software updates and demonstration versions of your products. However, users report that they are unable to access the FTP server. What should you do to enable access?
	- ==Open ports 20 and 21 for outbound connections.==

2. FTPS uses which mechanism to provide security for authentication and data transfer?
	- ==SSL==

3. To transfer files to your company's internal network from home, you use FTP. The administrator has recently implemented a firewall at the network perimeter and disabled as many ports as possible. Now, you can no longer make the FTP connection. You suspect the firewall is causing the issue. Which ports need to remain open so you can still transfer the files? (Select two.)
	- ==21==
	- ==20==

4. You want to close all ports associated with NetBIOS on your network's firewalls to prevent attacks directed against NetBIOS. Which ports should you close?
	- ==135, 137-139==

5. Which of the following file transfer protocols use SSH to provide confidentiality during the transfer? (Select two.)
	- ==SCP==
	- ==SFTP==

6. To increase security on your company's internal network, the administrator has disabled as many ports as possible. However, now you can browse the internet, but you are unable to perform secure credit card transactions. Which port needs to be enabled to allow secure transactions?
	- ==443==

7. You have a shared folder named Reports. Members of the Managers group have been given Write access to the shared folder. Mark Mangum is a member of the Managers group. He needs access to the files in the Reports folder, but he should not have any access to the Confidential.xls file. What should you do?
	- ==Add Mark Mangum to the ACL for the Confidential.xls file with Deny permissions.==

8. You want to give all managers the ability to view and edit a certain file. To do so, you need to edit the discretionary access control list (DACL) associated with the file. You want to be able to easily add and remove managers as their job positions change. What is the BEST way to accomplish this?
	- ==Create a security group for the managers. Add all users as members of the group. Add the group to the file's DACL.==

9. If Mark has a read-write permission to the share \\fileserver\securefiles and a read-only permission to the file coolstuff.docx on the NTFS file system shared by the file share, he is able to perform which action?
	- ==Read the file==

10. You have a file server named Srv3 that holds files used by the development department. You want to allow users to access the files over the network and control access to files accessed through the network or through a local logon. Which solution should you implement?
	- ==NTFS permissions and share permissions==

---
### Quiz 4.4

1. Which command should you use to display both listening and non-listening sockets on your Linux system? (Tip: enter the command as if in Command Prompt.)
	- ==netstat -a==

2. Which command should you use to scan for open TCP ports on your Linux system? (Tip: enter the command as if in Command Prompt.)
	- ==nmap -sT==

3. You need to increase the security of your Linux system by finding and closing open ports. Which of the following commands should you use to locate open ports?
	- ==nmap==

4. What does the **netstat -a** command show?
	- ==All listening and non-listening sockets==

5. You want to make sure no unneeded software packages are running on your Linux server.Select the command from the drop-down list that you can use to see all installed RPM packages.
	- ==yum list installed==

6. Which action would you use in a rule to disallow a connection silently?
	- ==Drop==

7. In which of the iptables default chains would you configure a rule to allow an external device to access the HTTPS port on the Linux server?
	- ==Input==

8. Which type of packet would the sender receive if they sent a connection request to TCP port 25 on a server with the following command applied?
	- ==RST==

9. You have configured the following rules. What is the effect?
	**sudo iptables -A INPUT -p tcp --dport 25 -m conntrack --ctstate NEW,ESTABLISHED -j ACCEPT  
	sudo iptables -A OUTPUT -p tcp --sport 25 -m conntrack --ctstate ESTABLISHED -j ACCEPT**
	- ==Allow SMTP traffic==

10. Which command would you use to list all of the currently defined iptables rules?
	- ==sudo iptables -L==

---
## Module 5
### Quiz 5.1
1. Where should an organization's web server be placed?
	- ==DMZ==

2. Which of the following is a privately controlled portion of a network that is accessible to some specific external entities?
	- ==Extranet==

3. You want to create a collection of computers on your network that appear to have valuable data but actually store fake data that could entice a potential intruder. Once the intruder connects, you want to be able to observe and gather information about the attacker's methods. Which feature should you implement?
	- ==Honeynet==

4. A honeypot is used for which purpose?
	- ==To delay intruders in order to gather auditing data==

5. Which of the following devices can apply quality of service and traffic-shaping rules based on what created the network traffic?
	- ==Application-aware devices==

6. You are the office manager of a small financial credit business. Your company handles personal financial information for clients seeking small loans over the internet. You are aware of your obligation to secure clients records, but the budget is an issue for your company. Which item would provide the BEST security for this situation?
	- ==All-in-one security appliance==
7. You are implementing security at a local high school that is concerned with students accessing inappropriate material on the internet from the library's computers. The students use the computers to search the internet for research paper content. The school budget is limited. Which content filtering option would you choose?
	- ==Restrict content based on content categories==

8. Which of the following BEST describes a honeyfile?
	- ==A single file setup to entice and trap attackers.==

9. Members of the sales team use laptops to connect to the company network. While traveling, they connect their laptops to the internet through airport and hotel networks. You are concerned that these computers could pick up viruses that could spread to your private network. You would like to implement a solution that prevents the laptops from connecting to your network unless antivirus software and the latest operating system patches are installed. Which solution should you use?
	- ==NAC==

10. A proxy server can be configured to do which of the following?
	- ==Restrict users on the inside of a network from getting out to the internet.==

---
### Quiz 5.2
1. Which of the following terms describes a network device that is exposed to attacks and has been hardened against those attacks?
	- ==Bastion or sacrificial host==

2. Of the following security zones, which one can serve as a buffer network between a private secured network and the untrusted internet?
	- ==DMZ==

3. Which of the following is the MOST likely to happen if the firewall managing traffic into the DMZ fails?
	- ==Only the servers in the DMZ are compromised, but the LAN will stay protected.==

4. You have a company network that is connected to the internet. You want all users to have internet access, but you need to protect your private network and users. You also need to make a web server publicly available to internet users. Which solution should you use?
	- ==Use firewalls to create a DMZ. Place the web server inside the DMZ and the private network behind the DMZ.==

5. How many network interfaces does a dual-homed gateway typically have?
	- ==3==

6. What needs to be configured on a firewall to allow traffic directed to the public resource in the DMZ?
	- ==Packet filters==

7. You have used firewalls to create a demilitarized zone. You have a web server that needs to be accessible to internet users. The web server must communicate with a database server for retrieving product, customer, and order information. How should you place devices on the network to best protect the servers? (Select two.)
	- ==Put the database server on the private network.==
	- ==Put the web server inside the DMZ.==

8. In which of the following situations would you most likely implement a demilitarized zone (DMZ)?
	- ==You want to protect a public web server from attack.==

9. Which of the following is another name for a firewall that performs router functions?
	- ==Screening router==

10. Which of the following is the BEST solution to allow access to private resources from the internet?
	- ==VPN==

---
### Quiz 5.3
1. Which of the following describes how access control lists can be used to improve network security?
	- ==An access control list filters traffic based on the IP header information, such as source or destination IP address, protocol, or socket number.==

2. Which of the following are features of an application-level gateway? (Select two.)
	- ==Stops each packet at the firewall for inspection==
	- ==Reassembles entire messages==

3. You want to install a firewall that can reject packets that are not part of an active session. Which type of firewall should you use?
	- ==Circuit-level gateway==

4. Jessica needs to set up a firewall to protect her internal network from the internet. Which of the following would be the BEST type of firewall for her to use?
	- ==Hardware==

5. You have been given a laptop to use for work. You connect the laptop to your company network, use it from home, and use it while traveling. You want to protect the laptop from internet-based attacks. Which solution should you use?
	- ==Host-based firewall==

6. You have just installed a packet-filtering firewall on your network. Which options are you able to set on your firewall? (Select all that apply.)
	- ==Destination address of a packet==
	- ==Port number==
	- ==Source address of a packet==

7. When designing a firewall, what is the recommended approach for opening and closing ports?
	- ==Close all ports; open only ports required by applications inside the DMZ.==

8. You connect your computer to a wireless network available at the local library. You find that you can access all of the websites you want on the internet except for two. What might be causing the problem?
	- ==A proxy server is blocking access to the websites.==

9. Which of the following best describes a stateful inspection?
	- ==Determines the legitimacy of traffic based on the state of the connection from which the traffic originated.==

10. Which of the following are characteristics of a packet-filtering firewall? (Select two.)
	- ==Filters IP address and port==
	- ==Stateless==

---
### Quiz 5.4
1. You want to connect your small company network to the internet. Your ISP provides you with a single IP address that is to be shared between all hosts on your private network. You do not want external hosts to be able to initiate connection to internal hosts. Which type of Network Address Translation (NAT) should you implement?
	- ==Dynamic==

2. Which NAT implementation assigns two IP addresses to the public NAT interface, allowing traffic to flow in both directions?
	- ==Dynamic and static==

3. Which device is NAT typically implemented on?
	- ==Gateway router==

4. Which problem does NAT help address?
	- ==The shortage of IPv4 addresses==

5. At which layer of the OSI model do NAT routers operate?
	- ==Layer 3 (Network layer)==

6. How many concurrent connections does NAT support?
	- ==5,000==

7. Which of the following does a NAT router use to associate a port number with a request from a private host?
	- ==PAT==

8. A network device is given an IP address of 172.16.0.55. Which type of network is this device on?
	- ==Class B private network==

9. You have a small network at home that is connected to the internet. On your home network, you have a server with the IP address of 192.168.55.199/16. You have a single public address that is shared by all hosts on your private network. You want to configure the server as a web server and allow internet hosts to contact the server to browse a personal website. What should you use to allow access?
	- ==Static NAT==

10. You are the network administrator for a small company that implements NAT to access the internet. However, you recently acquired five servers that must be accessible from outside your network. Your ISP has provided you with five additional registered IP addresses to support these new servers, but you don't want the public to access these servers directly. You want to place these servers behind your firewall on the inside network, yet still allow them to be accessible to the public from the outside. Which method of NAT translation should you implement for these servers?
	- ==Static==

---
### Quiz 5.5
1. A salesperson in your organization spends most of her time traveling between customer sites. After a customer visit, she must complete various managerial tasks, such as updating your organization's order database. Because she rarely comes back to your home office, she usually accesses the network from her notebook computer using Wi-Fi access provided by hotels, restaurants, and airports. Many of these locations provide unencrypted public Wi-Fi access, and you are concerned that sensitive data could be exposed. To remedy this situation, you decide to configure her notebook to use a VPN when accessing the home network over an open wireless connection. Which key steps should you take when implementing this configuration? (Select two.)
	- ==Configure the browser to send HTTPS requests through the VPN connection==
	- ==Configure the VPN connection to use IPsec==

2. A group of salesmen would like to remotely access your private network through the internet while they are traveling. You want to control access to the private network through a single server. Which solution should you implement?
	- ==VPN concentrator==

3. A VPN is primarily used for which of the following purposes?
	- ==Support secured communications over an untrusted network==

4. Which VPN implementation uses routers on the edge of each site?
	- ==Site-to-site VPN==

5. Which VPN tunnel style routes only certain types of traffic?
	- ==Split==

6. Which IPSec subprotocol provides data encryption?
	- ==ESP==

7. In addition to Authentication Header (AH), IPsec is comprised of what other service?
	- ==Encapsulating Security Payload (ESP)==

8. Which statement BEST describes IPsec when used in tunnel mode?
	- ==The entire data packet, including headers, is encapsulated==

9. Which VPN protocol typically employs IPsec as its data encryption mechanism?
	- ==L2TP==

10. Which of the following VPN protocols is no longer considered secure?
	- ==PPTP==

---
### Quiz 5.6
1. You are investigating the use of website and URL content filtering to prevent users from visiting certain websites. Which benefits are the result of implementing this technology in your organization? (Choose two.)
	- ==Enforcement of the organization's internet usage policy==
	- ==An increase in bandwidth availability==

2. Travis is sending a highly confidential email to Craig that contains sensitive data. Which of the following should Travis implement to ensure that only Craig is able to read the email?
	- ==Encryption==

3. Which of the following types of proxies would you use to remain anonymous when surfing the internet?
	- ==Forward==

4. As the security analyst for your organization, you have noticed an increase in emails that attempt to trick users into revealing confidential information. Which web threat solution should you implement to protect against these threats?
	- ==Anti-phishing software==

5. Which of the following are functions of gateway email spam filters? (Select two.)
	- ==Filters messages containing specific content==
	- ==Blocks email from specific senders==

6. You are configuring web threat protection on the network and want to block emails coming from a specific sender. Which of the following should be configured?
	- ==Spam filter==

7. As the security analyst for your organization, you have noticed an increase in user computers being infected with malware. Which two solutions should you implement and configure to remedy this problem? (Select two.)
	- ==Spam filters==
	- ==Virus scanner==

8. You are configuring web threat protection on the network and want to prevent users from visiting www.videosite.org. Which of the following needs to be configured?
	- ==Website filtering==

9. Which of the following types of proxies can be used for web filtering?
	- ==Transparent==

10. You are configuring web threat protection on the network and have identified a website that contains malicious content. Which of the following should you configure?
	- ==Web threat filtering==

---
### Quiz 5.7
1. Which of the following NAC agent types would be used for IoT devices?
	- ==Agentless==

2. Which of the steps in the Network Access Control (NAC) implementation process occurs once the policies have been defined?
	- ==Apply==

3. Which of the following defines all the prerequisites a device must meet in order to access a network?
	- ==Authentication==

4. Which of the following applies the appropriate policies in order to provide a device with the access it's defined to receive?
	- ==Authorization==

5. Which of the following NAC agent types creates a temporary connection?
	- ==Dissolvable==

6. What is Cisco's Network Access Control (NAC) solution called?
	- ==Identity Services Engine (ISE)==

7. You are configuring the security settings for your network. You have decided to configure a policy that requires any computer connecting to the network to run at least Windows 10 version 2004. Which of the following have you configured?
	- ==NAC==

8. Which of the following NAC agent types is the most convenient agent type?
	- ==Permanent==

9. You are part of a committee that is meeting to define how Network Access Control (NAC) should be implemented in the organization. Which step in the NAC process is this?
	- ==Plan==

10. Which of the following BEST describes zero-trust security?
	- ==Only devices that pass both authentication and authorization are trusted.==

---
### 5.8 Quiz
1. You are the security analyst for your organization and have discovered evidence that someone is attempting to brute-force the root password on the web server. Which classification of attack type is this?
	- ==Active==

2. Drag the network attack technique on the left to the appropriate description or example on the right. (Each technique may be used once, more than once, or not at all.)
	1. Perpetrators attempt to compromise or affect the operations of a system.
		- ==Active Attack==
	2. Unauthorized individuals try to breach a network from off-site.
		- ==External Attack==
	3. Attempting to find the root password on a web server by brute force.
		- ==Active Attack==
	4. Attempting to gather information without affecting the flow of information on the network.
		- ==Passive Attack==
	5. Sniffing network packets or performing a port scan.
		- ==Passive Attack==

3. An attacker sets up 100 drone computers that flood a DNS server with invalid requests. This is an example of which kind of attack?
	- ==DDoS==

4. In which of the following zones would a web server most likely be placed?
	- ==Low-trust zone==

5. Which area of focus helps to identify weak network architecture or design?
	- ==Documentation==

6. Which classification of attack type does packet sniffing fall under?
	- ==Passive==

7. Which area of focus do public-facing servers, workstations, Wi-Fi networks, and personal devices fall under?
	- ==Entry points==

8. Your network devices are categorized into the following zone types:
- No-trust zone
- Low-trust zone
- Medium-trust zone
- High-trust zone
Your network architecture employs multiple VLANs for each of these network zones. Each zone is separated by a firewall that ensures only specific traffic is allowed. Which of the following is the secure architecture concept that is being used on this network.
- ==Network Segmentation==

9. Your organization has started receiving phishing emails. You suspect that an attacker is attempting to find an employee workstation they can compromise. You know that a workstation can be used as a pivot point to gain access to more sensitive systems. Which of the following is the MOST important aspect of maintaining network security against this type of attack?
	- ==User education and training==

10. Which of the following is commonly created to segment a network into different zones?
	- ==VLANs==

---
### Quiz 5.9
1. While developing a network application, a programmer adds functionally that allows her to access the running program without authentication so she can capture debugging data. The programmer forgets to remove this functionality prior to finalizing the code and shipping the application. Which type of security weakness does this describe?
	- ==Backdoor==

2. An attacker was able to gain unauthorized access to a mobile phone and install a Trojan horse so that he or she could bypass security controls and reconnect later. Which type of attack is this an example of?
	- ==Backdoor==

3. In an effort to increase the security of your organization, programmers have been informed they can no longer bypass security during development. Which vulnerability are you attempting to prevent?
	- ==Backdoor==

4. Which of the following are characteristics of a complex password? (Select two.)
	- ==Has a minimum of eight characters==
	- ==Consists of letters, numbers, and symbols==

5. An attacker has gained access to the administrator's login credentials. Which type of attack has most likely occurred?
	- ==Password cracking==

6. When setting up a new wireless access point, what is the first configuration change that should be made?
	- ==Default login==

7. You've just deployed a new Cisco router that connects several network segments in your organization. The router is physically located in a server room that requires an ID card to gain access. You've backed up the router configuration to a remote location in an encrypted file. You access the router configuration interface from your notebook computer by connecting it to the console port on the router. You've configured the management interface with a username of admin and a password of password. What should you do to increase the security of this device?
	- ==Use a stronger administrative password.==

8. A relatively new employee in the data entry cubical farm was assigned a user account similar to the other data entry employees' accounts. However, audit logs have shown that this user account has been used to change ACLs on several confidential files and has accessed data in restricted areas. This situation indicates which of the following has occurred?
	- ==Privilege escalation==

9. An attacker has obtained the logon credentials for a regular user on your network. Which type of security threat exists if this user account is used to perform administrative functions?
	- ==Privilege escalation==

10. Travis and Craig are both standard users on the network. Each user has a folder on the network server that only they can access. Recently, Travis has been able to access Craig's folder. This situation indicates which of the following has occurred?
	- ==Privilege escalation==

---
### Quiz 5.10
1. Which common design feature among instant messaging clients make them less secure than other means of communicating over the internet?
	- ==Peer-to-peer networking==

2. Which type of application allows users to share and access content without using a centralized server?
	- ==Peer-to-peer software==

3. Which of the following methods did Microsoft introduce in Windows 10 to help distribute OS updates?
	- ==Peer-to-peer software==

4. Which of the following is a benefit of P2P applications?
	- ==Shared resources==

5. What do application control solutions use to identify specific applications?
	- ==Application signatures==

6. Which of the following is susceptible to social engineering exploits?
	- ==Instant messaging==

7. Which of the following is considered a major problem with instant messaging applications?
	- ==Loss of productivity==

8. You are the security analyst for your organization and have recently noticed a large amount of spim on the company mobile devices. Employees rely on the IM app to communicate with each other. Which of the following countermeasures should you implement?
	- ==Use an IM blocker.==

9. You have implemented a new application control solution. After monitoring traffic and use for a while, you have noticed an application that continuously circumvents blocking. How should you configure the application control software to handle this application?
	- ==Tarpit==

10. You are implementing a new application control solution. Prior to enforcing your application whitelist, you want to monitor user traffic for a period of time to discover user behaviors and log violations for later review. How should you configure the application control software to handle applications not contained in the whitelist?
	- ==Flag==

---
