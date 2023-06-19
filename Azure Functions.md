1. Different plant type like consumption(serverless),app service plan, functions premium
2. has support for docker as well.
3. need storage account to store different files.
4. can be created inside a VPC but requires standard or premium tiers
5. can have input and output bindings

## Durable Functions
https://www.youtube.com/watch?v=SJTnCGPo6qk
![[Pasted image 20230616122936.png]]

1. It is used to support long running tasks.
2. For example we are calling a api and it is taking very long time to process then we cannot wait for that to come as the default runtime for azure function is 30 mins max.
3. So what we can do is create a durable function and we will have a state like if the execution of that function is pending or completed.
4. Basically we get a url which we can hit and check the status of the durable function.
5. We can also interrupt the runtime of the durable function as well.