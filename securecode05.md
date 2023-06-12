## Notes On Secure Coding 


### Sensitive information leakage

This is a group of threats that are compromises data by applciation by way of maintaining and transmiting its data 

Mitigation to this vulnerability typically are the mechanics for value obfuscation, encryption,etc**




```
try {
  String passwordKey = "12345678890";
  MessageDigest md = MessageDigest.getInstance("SHA-256");  
  byte[] digest = md.digest(passwordKey.getBytes());       
  String hash = (new BigInteger(1, digest)).toString(16);  
} catch (NoSuchAlgorithmException e) {
  e.printStackTrace();
}

```


**the command : strings**

byte to strings 

<br>

### Sanitize the parameter value against injection attacks

<br>


### Code Corruption

<br>

**Make class methods final**

### Optional Type

```
Optional<String> a = webserviceComputingFunc(); 
String s = null;
if (a.isPresent()) {                    
  s = a.get();
}
s = a.orElse("Default");                    
s = a.orElseThrow();    


```


### Immutability

**Use final keyword**

* So no other class will change its definition


