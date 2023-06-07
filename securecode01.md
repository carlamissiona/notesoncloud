## Notes On Secure Coding 


<br><br>


### Secure Software Concepts

* **Secure Software Concepts**

* **Secure Software Concepts- Concepts from information security domain**

*  _**CIA**_ **common concepts in security: confidentiality, integrity, and availability (CIA).**

* **Confidentiality is the concept of preventing the exposure of information to unauthorized users.**

* **Confidentiality is also keeping secrets secret.Having Authorized parties makes the means there is authorization**  

* **Some methods of keeping data confidential:**

 1. Access controls
 2. Encryption

<br>

### Factors to Apply or Implement Confidentiality Controls 


 1. Failure to protect key
 2. Failure to use algorithms from approved cryptographic libraries [ Using own crypto, may lead to failure ] 
 3. Ask these questions :  - Who are the party authorized to see what specific data  - What mechanism should be employed to enforce confidentiality

* **Integrity much like confidentiality, integrity refers to protecting the data from unauthorized alteration. Users can be authorized to alter or view information 
  so integrity controls need authorization scheme to prevent controlling alterations, including deletions**
  
* **In order to imlement integrity security controls ask the ff questions -Who is authorized to alter which specific data element -What mechanism should be employed to detect errors and enforce integrity -What are the business requirements with respect to data collection, transfer, storage, and use with respect to integrity**

* **A system of access control mechanisms, with diff levels of access with respect to read, write, and delete will place a piece integrity assurance in system**

* **Availability means resolving specific two issues: ensuring systems are available for authorized users when they require those systems and denying access to unauthorized users.**

* **Balancing the pillars in CIA triad helps define the security requirement that should be design in system**

* **Authentication is the process of determining the identity of a user  this element of security is giving differentiation of authorized and unauthorized users**

* **To help in authentication process a user can provide**

<br>

```
 1.Something you know (passwords)

 2.Something you have (ATM card)

 3.Something about you (biometrics)
 ```
 <br>
 
 * **Multifactor authentication  is simply the combination of two or more layers of authentication. Five broad categories of authentication can be used: what you are (for example, biometrics), what you have (for instance, tokens), what you know (passwords and other information), somewhere you are (location), and something you do (physical performance).**



 <br>
 
 * **Identity management (IDM) refers to the collection of policies, processes, and technologies for managing digital identity information**


 <br>
 
 * **Identity management (IDM) must be scalable - In the enterprises there are third-party enterprise-class IDM systems that provide services such as password resets, password synchronization, single sign-on, and multiple identity methods.**

* **Identity Attributes the elements of an identity? examples like identity—name, department, location, login ID, identification number, e-mail address, and others**

<br><br>
* **Certificates**

* **When there is a process of presentation of a certificate - this is Certificate-based authentication**
* _A digital certificate is a digital file that is sent as an attachment to a message orobjects - dc are verified beforehand

* **SSH Keys access credentials used in Secure Shell (SSH) connection -used for automated processes and service also used in single sign-on (SSO) systems **

* **X.509 standard, certificate manipulation is stated and controlled by the X.509 standard** 
```

•    Serial number 

•    Signature algorithm  The hashing and digital signature algorithms 

•    Issuer  (The CA that generated and digitally signed the certificate)

•    Validity 

•    Subject  (Field for owner of the certificate)

•    Public key   

•    Certificate usage

•    Version number

```


<br>

* **Single sign-on makes it possible for a user, after authentication, to have their credentials reused on other applications reuse the credentials against another system. Methods Kerberos and Security Assertion Markup Language. Also includes the OpenID protocol.**

* **Authorization is the process of giving access to a user with the process or resources in a system**

* **Common access control models include**
   
      1. Mandatory access control (MAC), 
      2. Discretionary access control (DAC), 
      3. Role-based access control (RBAC), and rule-based access control (RBAC)


* **Accountability -Accounting is a means of measuring activity - specifically in security this is the recording of actions and the users performing them (logging)**

* **When the transaction is crucial accounting or logging then is a requirement so they may be audited at a later date and time. Auditing is management’s way to observe the operation**

* **Audit logs enhance security but it is not a security control in of themselves**
 
* **To maintain an audit logs  these elements are necessary 1. A monitoring system 2.detection 3. Response process.**

<br><br><br>
### Secure development lifecycle model 

* 1. Add a process checks to include security elements in the software development process. This addition will enhance security quality of software or reduce bugs

* **If the product or software maitains quality but lacks security, then the result is a set of vulnerabilities**

* **If the product or software maitains securityquality but lacks quality, then the result is a set of misbehaviors or illogical features**

### Security Features != Secure Software

* **Secure software development is about ensuring that all components of a finished software are constructed in a fashion where they work securely**


* **The key element of SDL**

* **Passing Gates and Reviewing Security Requirements**

* **Bug Tracking**

* **Threat modeling you have tocommunicate information associated with a threat to the development team**

* **Fuzzing is a test technique with proper inputs does system display logical outputs for undesired behaviors. This explores potential vulnerability**

* **Security Reviews adding a series mini security review enhance SDL. Here the security elements in place are under examination**

* **Bug Mitigation Teams can**

•   Do nothing

•   Warn the user

•   Remove the problem

•   Fix the problem


