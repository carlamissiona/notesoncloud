
## Notes On Cloud Native



### Knative
 
<br>

**What is Serverless - one characteristic is to scale work amount to zero - Also could mean no server node**

Every HTTP request is a “unit of work” therefore the serverless principle thinks it is a good component to scale to zero


Knative requires networking service kubernetes operator  - we use Istio

Knative consists of two independent and primary components

* Serving

* Eventing

<br><br>

**Knative has CLI tool called KN**

```
curl -L https://github.com/knative/client/releases/download/knative-v${KNATIVE_VERSION}/kn-linux-amd64 
-o /usr/bin/kn && chmod +x /usr/bin/kn
```

Check Knative CLI version

```
kn version
```


### To Get Knative Serving Running ###

Install necessary Customer Resource Definitions , serving core yml, **knative serving service crd** , and the networking that establishes the connection between Knative and Istio
<br><br>

**kubectl get deployments,pods,services --namespace knative-serving | grep 'Running'**

<br>

### Knative Service Control Plane ###

* activator _manages requests and reporting metrics to the autoscaler_

* autoscaler _manages request metrics and adjusts the number of pods required_

* controller _manages the public Knative objects and autoscaling CRDs_

* webhook _manages Kubernetes API calls as well as CRD insertions and updates_

<br>

**sample-server-kn-service.yaml**

<br><br>

```
 
apiVersion: serving.knative.dev/v1
kind: Service
metadata:
  name: helloworld
spec:
  template:
    spec:
      containers:
        - image: jmalloc/echo-server:0.3.1 

```


**kubectl create namespace hello**

**kubectl label namespace hello istio-injection=enabled**

 
 
kubectl describe namespace hello

With the namespace created, declare your new Knative service:

 

**kubectl create --namespace hello --filename sample-server-kn-service.yaml**

The Knative service has been created:

kubectl get ksvc --namespace hello  
 
 


 
