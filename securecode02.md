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
Defense in Depth
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
Open Design
Don't rely on security by obscurity
Example: modern cryptography relies on the secrecy of the key, not secrecy of the algorithm
Least Common Mechanism
Prevent inadvertent sharing of information by using separate processes when possible
Psychological Acceptability
Users will try to get around security if it is seen as an obstacle
Weakest Link
Adding to the security of a system is most effective when applied to the weakest link
Leveraging Existing Components
Pros: increase efficiency and security
Cons: monoculture environment (failures have a larger footprint)
Single Point of Failure
No one single piece should be able to cause the whole system to fail

Security Models


 
