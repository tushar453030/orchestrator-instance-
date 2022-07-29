# Instance orchestrator
Different practices to scale in or out the number of instances available to handle the load by using Kubernetes, AWS services.

# Kubernetes 
Docker orchestrator tool that helps us to manage the number of instances running and up all the time.
Below are some screenshots to support the above statement.
![3](https://user-images.githubusercontent.com/93340408/181780039-f87dbc72-64fd-475d-9433-ebc8cda529c2.png)

As I deleted one of the pod but rather than goes down it restarted because in the deployment.yaml there is a parameter called replicas which I have set to 3. So every time an instance of pod goes down another new intance turn up.

# AWS Auto-Scaling-Group
When creating an auto scaling group in Aws it asked for template for making the EC2 instance automatically selecting the AMI image for linux and storage type.

![aws1](https://user-images.githubusercontent.com/93340408/181785919-9f908724-f056-470d-a95c-b124ae98c57c.png)
As one can see desired intances is 2 minimum it can have one and 4 at max.

If we look into the instances section there are automatically two EC2 instances created.
![aws2](https://user-images.githubusercontent.com/93340408/181786193-4a94ff62-96aa-43dd-9833-114e2414de94.png)

Now if we terminate one of them the next instance will come up automatically
![aws3](https://user-images.githubusercontent.com/93340408/181786468-918a2897-3531-4a48-8e71-aef7b1ae33d5.png)
![aws4](https://user-images.githubusercontent.com/93340408/181786478-7cc7514a-0476-4894-b52c-6fcd726a2f37.png)
if we go in the auto-scaling group console there we see an request of turning up a new instance initiated as soon as one the instance turns down.

![aws5](https://user-images.githubusercontent.com/93340408/181786838-24e78b2f-96e8-4bb4-91df-757e4ea289d4.png)
Another instance shown up. Therefore high availablity.
