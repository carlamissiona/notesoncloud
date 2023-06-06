## Notes On Web Development

**Using Firebase**

<br>

**Firestore**
**`Cloud Firestore is a cloud-hosted, NoSQL database that your Apple, Android, and web apps can access directly via native SDKs. Cloud Firestore is also available in native Node.js, Java, Python, Unity, C++ and Go SDKs, in addition to REST and RPC APIs.`**

- From Firebase Website


<br>
**Steps**

*  On Firebase Navigation Click **Add Firebase to Your Web App**
*  **Go to Firestore add Collection call it `Message` then add a document to it**
```
    data_body: "Lorem ipsum dolor sit amet,"
    written_by: Miller
```
*  Install the firebase SDK to your frontend project on your local dev
*  **npm i firebase**
*  Add Firebase config
```
import firebase from 'firebase'
var firebaseConfig = {
    apiKey: "xxxxxxxxxxxxxxxx",
    authDomain: "xxxxxxxxxxxxxxxx",
    databaseURL: "xxxxxxxxxxxxxxxx",
    projectId: "xxxxxxxxxxxxxxxx",
    storageBucket: "xxxxxxxxxxxxxxxx",
    messagingSenderId: "xxxxxxxxxxxxxxxx",
    appId: "xxxxxxxxxxxxxxxx",
    measurementId: "xxxxxxxxxxxxxxxx"
  };
  
const firebaseApp=firebase.initializeApp(firebaseConfig);
const dbObjectFirestore=firebase.firestore();

export default dbObjectFirestore;
```


* On the code use the .data() to collect the firestore data on a for loop response from fetch of http get using dbObjectFirestore
```
import dbObjectFirestore from './firebase.config';

const fetchMessagess=async()=>{
    const response=db.collection('Messages');
    const data=await response.get();
}
...
const fetchMessages=async()=>{
    const response=db.collection('Messages');
    const data=await response.get();
    data.docs.forEach(item=>{
     setMessages([...msg,item.data()])
    })
}
```


