## Notes On Secure Coding 


<br><br>


### Security Governance & Policy

**Security Governance - This is administration of an organization's security program**
 
  **Approaches to Security Governance - Top-down & Bottom-up**

  **Top-down**
    **Upper management makes security policies**
    **Lower professionals flesh out security policies**
   
   
  **Bottom-up**
    **IT staff makes security decisions**


**Strategic Plan**

  * **Long-term Plan - Lifetime: 5 years**

  * **Tactical Plan - Project & hiring plans, budget strategy**

  * **Operation Plan- Training plans, Software deployment plans** 


 
 
 **Security Policy**

 * Requires support of senior management to succeed

 * Evidence of due care and due diligence

 * According to security principles like privacy, password management, etc

<br>

 **Confidentiality Requirements**

* Use of password masking and encryption 

* Use of TLS communication this is protection for data in transit

* Logfiles should not include sensitive information

* Do not use FTP use SFTP FTPS


 **Integrity Requirements**

* Code injection is integrity threat - use input validation for mitigation of sql injection 

* Message Digest, Hashing, CRC & checksum


 **Availability Requirements**

* Make highly available infrastructure, graceful-degradation and fail-safe security 

<br>



**Static Application Security Testing**

* Helps identify errorneous or security flawed code
* These tools helps provide mitigations for vulnerabilities in security 
* With these kind of testing flaws will be found out early in SDLC
* Most solutions are platform or language independent

<br>
<br>

**CVE Common Vulnerability Exposure**

* Lists of common identifiers for publicly known cyber security vulnerabilities
 
<br>

**CVE Common Weakness Enumeration**

* A list developed by community of common software security weaknesses 
<br>
<br>
<br>

**The Protection Of Information In Computer Systems** 
<br>
<br>

**Change Management**
* **Changes can lead to security issues -So prevent compromise after change**
 
* **Do These Mitigations**
  * Monitor change
  * Test change
  * Allow rollback of change
  * Inform users of change
  * Analyze effects of change
  * Minimize negative impact of change
  * Allow review of change by Change Approval Board (CAB)
 <br>



