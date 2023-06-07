## Notes On Secure Coding 


<br><br>
 
 ### System Tenets
 
<br><br>
 
 **Session Management**
 Software require communications between its elements. There should be security in communication session to prevent the hijacking
 
 Session management refers to the design and implementation of security controls to ensure that communication channels are having CIA
 
 
 
<br><br>


**Good Enough Security**
<br><br>
* **Make security simple and just logical. You dont have security of national state grade security controls for protectic simple things**

* **Trade-offs exist between security and other aspects**

<br><br>

**Least Privilege**
<br><br>

* **Authorized entity will have roles and access control so no spread of inside threat will occur. Prevent a role or user having higher privilege for much of the time**

<br><br>
**Separation of Duties**
<br><br>
* **No single individual can abuse the system**


<br><br>
**Defense in Depth**
<br><br>
* **There should be layered security/defense and diversity defense**
<br>

* **No system is 100% secure - true goal of security is to make cost of compromising greater in time/effort/resources than it is worth**

<br>

* **Diversity of defense - layers should be dissimilar in nature**

<br><br>

**Fail-safe**
<br><br>
* **When a system experiences a errors it should be resilient and degrade gracefully, it should fail to a safe state**
  
**Economy of Mechanism**
<br><br>
* **Higher complexity generally results in less security due to lack of understanding and more attack vectors**
* **Follow this rule of thumb: eliminate all nonessential services and protocols**

<br><br>
**Complete Mediation**
<br><br>
* **Authorization is never circumvented, even with repeated access**


Example: security kernel
**Open Design**
<br><br>
* **Don't rely on security by obscurity** 
 
<br><br>
**Single Point of Failure**

<br><br>
* **No one single piece should be able to cause the whole system to fail**
<br><br>

### Security Models


**Multilevel Security Model**

<br><br>
**Add labels to entity or objects that can be classified into containers of security levels. Containers can be hierarchical in nature, ie. Top Secret, Secret, and Confidential.**

<br><br>
**Integrity Models**

<br><br>
**There are diff types of integrity models since integrity can be as important as, or even more important than, confidentiality**

<br><br>
**Biba Integrity Model**

<br><br>
**Integrity levels are the level of “trust” that can be placed in the accuracy of information based on the level specified- If a data has high integrity level then it is likely said to be highly secure and accurate**

**The Biba model’s rule states that the integrity level of a subject will be lowered if it acts on an object of a lower integrity level**


<br><br>
**Information Flow Models**

<br><br>
**This classification states that there is a series of models that explores aspects of data or information flow **

**Security of data is absolute priority and must be protected according to information flow - Information must be protected when at rest, in transit, and in use.**
  
<br><br>
**Brewer-Nash Model (Chinese Wall)**

<br><br>
**The Brewer-Nash model is a model designed to enforce confidentiality in business and enterprises - This suggest that there are info that are private to some departments only and not to**

<br><br>
**NIST CSF Model**
<br>
**This is the  National Institute of Standards and Technology (NIST) Cybersecurity Framework - This has 5 pillars- Identify, Protect, Detect, Respond, Recover**
 
 ### Other Security concepts
 
* **Unstructured threat - little or no resources, no specific motivation, typically only an annoyance**

* **Structured threat - specific mission, time and resources**

* **Highly structured threat - organized crime, crimeware**

* **Nation-state threat - When a highly structured threat is employed by a nation-state for example elements of espionage** 

* **Advanced persistent threat (APT) - multiple methods to penetrate and then live undetected**

<br><br><br>
**Insider vs outsider**

* **Criminals  may exists inside and outside of enterprises. Even common employee may pose security threats due to poor cybersecurity awareness.In modern security solution, there are monitors a system for both external and internal attacks.**

 
<br><br>
<br><br>
 
