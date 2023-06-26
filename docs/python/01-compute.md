## Python

Reference 
- AWS: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html
- GCP: https://cloud.google.com/python/docs/reference/compute/latest

# Supported use cases and equivalence matrix for Compute service

**Instances**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create instance | [`run_instances()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.run_instances) | [`create_instance()`](https://googleapis.dev/python/compute/latest/gapic/v1/api.html#google.cloud.compute_v1.VirtualMachineClient.create) |
| List instances | [`describe_instances()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_instances.html#describe-instances) | [`InstancesClient.list()`](https://cloud.google.com/python/docs/reference/compute/latest/google.cloud.compute_v1.services.instances.InstancesClient#google_cloud_compute_v1_services_instances_InstancesClient_list) |
| Start/stop instance | [`start_instances()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.start_instances), [`stop_instances()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.stop_instances) | [`start()`](https://googleapis.dev/python/compute/latest/gapic/v1/api.html#google.cloud.compute_v1.InstancesClient.start), [`stop()`](https://googleapis.dev/python/compute/latest/gapic/v1/api.html#google.cloud.compute_v1.InstancesClient.stop) |
| Terminate instance | [`terminate_instances()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.terminate_instances) | [`delete()`](https://googleapis.dev/python/compute/latest/gapic/v1/api.html#google.cloud.compute_v1.InstancesClient.delete) |
| Create tags | [`create_tags()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.create_tags) | [`add_tags()`](https://googleapis.dev/python/compute/latest/gapic/v1/api.html#google.cloud.compute_v1.InstancesClient.add_tags) |
| Describe tags | [`describe_tags()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.describe_tags) | [`get_tags()`](https://googleapis.dev/python/compute/latest/gapic/v1/api.html#google.cloud.compute_v1.InstancesClient.get) |
| Delete tags | [`delete_tags()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.delete_tags) | [`remove_tags()`](https://googleapis.dev/python/compute/latest/gapic/v1/api.html#google.cloud.compute_v1.InstancesClient.remove_tags) |

**SSH keys**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create SSH key pair | [`create_key_pair()`](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateKeyPair.html), [`import_key_pair()`](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ImportKeyPair.html) | [`create()`](https://cloud.google.com/compute/docs/reference/rest/v1/publicKeys/create) |
| Describe SSH key pairs | [`describe_key_pairs()`](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeKeyPairs.html) | [`list()`](https://cloud.google.com/compute/docs/reference/rest/v1/publicKeys/list) |
| Delete SSH key pair | [`delete_key_pair()`](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DeleteKeyPair.html) | [`delete()`](https://cloud.google.com/compute/docs/reference/rest/v1/publicKeys/delete) |

**VPCs**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create VPC | [`create_vpc()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.create_vpc) | [`insert()`](https://cloud.google.com/compute/docs/reference/rest/v1/networks/insert) |
| Describe VPCs | [`describe_vpcs()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.describe_vpcs) | [`list()`](https://cloud.google.com/compute/docs/reference/rest/v1/networks/list) |
| Delete VPC | [`delete_vpc()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.delete_vpc) | [`delete()`](https://cloud.google.com/compute/docs/reference/rest/v1/networks/delete) |

**Subnets**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create subnet | [`create_subnet()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.create_subnet) | [`insert()`](https://googleapis.dev/python/compute/latest/gapic/v1/api.html#google.cloud.compute_v1.ZonesClient.insert) |
| Describe subnets | [`describe_subnets()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.describe_subnets) | [`list()`](https://googleapis.dev/python/compute/latest/gapic/v1/api.html#google.cloud.compute_v1.ZonesClient.list) |
| Delete subnet | [`delete_subnet()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.delete_subnet) | [`delete()`](https://googleapis.dev/python/compute/latest/gapic/v1/api.html#google.cloud.compute_v1.ZonesClient.delete) |

**Security Groups**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create security group | [`create_security_group()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.create_security_group) | [`insert()`](https://cloud.google.com/compute/docs/reference/rest/v1/firewalls/insert) |
| Describe security groups | [`describe_security_groups()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.describe_security_groups) | [`list()`](https://cloud.google.com/compute/docs/reference/rest/v1/firewalls/list) |
| Delete security group | [`delete_security_group()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.delete_security_group) | [`delete()`](https://cloud.google.com/compute/docs/reference/rest/v1/firewalls/delete) |
| Authorize security group ingress | [`authorize_security_group_ingress()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.authorize_security_group_ingress) | [`add_allowed_rule()`](https://cloud.google.com/compute/docs/reference/rest/v1/firewalls/insert) |

**Load Balancers**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create load balancer (Layer-4) | [`create_load_balancer()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.create_load_balancer) (Network Load Balancer) | [`create_network_load_balancer()`](https://cloud.google.com/compute/docs/reference/rest/v1/networks/insert) |
| Create load balancer (Layer-7) | [`create_load_balancer()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/elbv2.html#ElasticLoadBalancingv2.Client.create_load_balancer) (Application Load Balancer) | [`create_http_health_check()`](https://cloud.google.com/compute/docs/reference/rest/v1/httpHealthChecks/insert), [`create_https_health_check()`](https://cloud.google.com/compute/docs/reference/rest/v1/httpsHealthChecks/insert), [`create_backend_service()`](https://cloud.google.com/compute/docs/reference/rest/v1/backendServices/insert), [`create_url_map()`](https://cloud.google.com/compute/docs/reference/rest/v1/urlMaps/insert), [`create_target_pool()`](https://cloud.google.com/compute/docs/reference/rest/v1/targetPools/insert) |
| Describe load balancers | [`describe_load_balancers()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/elbv2.html#ElasticLoadBalancingv2.Client.describe_load_balancers) | [`list()`](https://cloud.google.com/compute/docs/reference/rest/v1/loadBalancers/list) |
| Delete load balancer | [`delete_load_balancer()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/elbv2.html#ElasticLoadBalancingv2.Client.delete_load_balancer) | [`delete()`](https://cloud.google.com/compute/docs/reference/rest/v1/loadBalancers/delete) |

**Auto scaling groups**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create auto scaling group | [`create_auto_scaling_group()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.create_auto_scaling_group) | [`insert()`](https://cloud.google.com/compute/docs/reference/rest/v1/instanceGroupManagers/insert) |
| Describe auto scaling groups | [`describe_auto_scaling_groups()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.describe_auto_scaling_groups) | [`list()`](https://cloud.google.com/compute/docs/reference/rest/v1/instanceGroupManagers/aggregatedList) |
| Delete auto scaling group | [`delete_auto_scaling_group()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.delete_auto_scaling_group) | [`delete()`](https://cloud.google.com/compute/docs/reference/rest/v1/instanceGroupManagers/delete) |

**Elastic IPs**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create Elastic IP | [`allocate_address()`](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AllocateAddress.html) | [`create_address()`](https://cloud.google.com/compute/docs/reference/rest/v1/globalAddresses/insert) |
| Describe Elastic IPs | [`describe_addresses()`](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeAddresses.html) | [`list()`](https://cloud.google.com/compute/docs/reference/rest/v1/globalAddresses/aggregatedList) |
| Release Elastic IP | [`release_address()`](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ReleaseAddress.html) | [`delete()`](https://cloud.google.com/compute/docs/reference/rest/v1/globalAddresses/delete) |

**Tags**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create tags | [`create_tags()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.create_tags) | [`add_tags()`](https://cloud.google.com/compute/docs/reference/rest/v1/instances/addTags) |
| Describe tags | [`describe_tags()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.describe_tags) | [`list()`](https://cloud.google.com/compute/docs/reference/rest/v1/tags/list) |
| Delete tags | [`delete_tags()`](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.delete_tags) | [`remove_tags()`](https://cloud.google.com/compute/docs/reference/rest/v1/instances/removeTags) |
