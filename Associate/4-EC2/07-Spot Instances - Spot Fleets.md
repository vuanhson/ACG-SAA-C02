## Spot Instances & Spot Fleets

### Spot instances
Amazon EC2 Spot Instances let you take advantage of unused EC2 capacity in the AWS Cloud. Spot Instances are available at up to a 90% discount compared to On-Demand prices. You can use Spot Instances for various stateless, fault-tolerant, or flexible applications, such as big data, containerized workloads, CI/CD, web servers, high-performance computing (HPC), and other test and development workloads.

To use Spot Instances, you must first decide on your maximum Spot price. The instance will be provisioned so long as the Spot price is BELOW your maximum Spot price. The hourly Spot price varies depending on capacity and region. If the Spot price goes above your maximum, you have two minutes to choose whether to stop or terminate your instance

You may also use a Spot block to stop your Spot Instances from being terminated even if the Spot price goes over your max Spot price. You can set Spot blocks for between one to six hours currently.

Spot Instances are useful for the following tasks:
- Big data and analytics
- Containerized workloads
- CI/CD and testing
- Web services
- Image and media rendering
- High-performance computing

Spot Instances are not good for:
- Persistent workloads
- Critical jobs
- Databases

Spot Instance requests: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-requests.html

### Spot Fleets
A Spot Fleet is a collection of Spot Instances and, optionally, On-Demand Instances.

The Spot Fleet attempts to launch the number of Spot Instances and On-Demand Instances to meet the target capacity you specified in the Spot Fleet request. The request for Spot Instances is fulfilled if there is available capacity and the maximum price you specified in the request exceeds the current Spot price. The Spot Fleet also attempts to maintain its target capacity fleet if your Spot Instances are interrupted.

Spot Fleets will try and match the target capacity with your price restraints:
- Set up different launch pools. Define things like EC2 instance type, operating system, and Availability Zone.
- You can have multiple pools, and the fleet will choose the best way to implement depending on the strategy you define.
- Spot fleets will stop launching instances once you reach your price threshold or capacity desire.

You can have the following strategies with Spot Fleets:
- **capacityOptimized** The Spot Instances come from the pool with optimal capacity for the number of instances launching.
- **lowestPrice** The Spot Instances come from the pool with the lowest price. This is the default strategy.
- **diversified** The Spot Instances are distributed across all pools.
- **InstancePoolsToUseCount** The Spot Instances are distributed across the number of Spot Instance pools you specify. This parameter is valid only when used in combination with lowestPrice.

### Exam Tips
- Spot Instances save up to 90% of the cost of On-Demand Instances.
- Useful for any type of computing where you don’t need persistent storage.
- You can block Spot Instances from terminating by using Spot block.
- A Spot Fleet is a collection of Spot Instances and, optionally, On-Demand Instances.
- If the Spot instance is terminated by Amazon EC2, you will not be charged for a partial hour of usage. However, if you terminate the instance yourself, you will be charged for any hour in which the instance ran.