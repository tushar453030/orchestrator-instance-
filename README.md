# orchestrator-instance-
Different practices to scale in or out the number of instances available to handle the load by using Kubernetes, AWS services.

# Kubernetes 
Docker orchestrator tool that helps us to manage the number of instances running and up all the time.
Below are some screenshots to support the above statement.
![3](https://user-images.githubusercontent.com/93340408/181780039-f87dbc72-64fd-475d-9433-ebc8cda529c2.png)

As I deleted one of the pod but rather than goes down it restarted because in the deployment.yaml there is a parameter called replicas which I have set to 3. So every time an instance of pod goes down another new intance turn up.

# AWS Auto-Scaling-Group
