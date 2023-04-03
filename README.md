kind: Deployment
apiVersion: apps/v1
metadata:
   name: mydeployments
spec:
   replicas: 2
   selector:     
    matchLabels:
     name: deployment
   template:
     metadata:
       name: testpod
       labels:
         name: deployment
     spec:
      containers:
        - name: c00
          image: ubuntu
          command: ["/bin/bash", "-c", "while true; do echo Technical-Guftgu; sleep 5; done"]
