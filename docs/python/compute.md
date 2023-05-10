## Python

# Supported use cases and equivalence matrix for Compute service

**Instances**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create instance | `create_instances()` | `create_instance()` |
| Start/stop instance | `start_instances()`, `stop_instances()` | `start()`, `stop()` |
| Terminate instance | `terminate_instances()` | `delete()` |
| Create tags | `create_tags()` | `add_tags()` |
| Describe tags | `describe_tags()` | `get_tags()` |
| Delete tags | `delete_tags()` | `remove_tags()` |

**SSH keys**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create SSH key pair | `create_key_pair()`, `import_key_pair()` | `create()` |
| Describe SSH key pairs | `describe_key_pairs()` | `list()` |
| Delete SSH key pair | `delete_key_pair()` | `delete()` |

**VPCs**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create VPC | `create_vpc()` | `insert()` |
| Describe VPCs | `describe_vpcs()` | `list()` |
| Delete VPC | `delete_vpc()` | `delete()` |

**Subnets**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create subnet | `create_subnet()` | `insert()` |
| Describe subnets | `describe_subnets()` | `list()` |
| Delete subnet | `delete_subnet()` | `delete()` |

**Security groups**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create security group | `create_security_group()` | `insert()` |
| Describe security groups | `describe_security_groups()` | `list()` |
| Delete security group | `delete_security_group()` | `delete()` |
| Authorize security group ingress | `authorize_security_group_ingress()` | `add_allowed_rule()` |

**Load balancers**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create load balancer (Layer-4) | `create_load_balancer()` (Network Load Balancer) | `create_network_load_balancer()` |
| Create load balancer (Layer-7) | `create_load_balancer()` (Application Load Balancer) | `create_http_health_check()`, `create_https_health_check()`, `create_backend_service()`, `create_url_map()`, `create_target_pool()` |
| Describe load balancers | `describe_load_balancers()` | `list()` |
| Delete load balancer | `delete_load_balancer()` | `delete()` |

**Auto scaling groups**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create auto scaling group | `create_auto_scaling_group()` | `insert()` |
| Describe auto scaling groups | `describe_auto_scaling_groups()` | `list()` |
| Delete auto scaling group | `delete_auto_scaling_group()` | `delete()` |

**Elastic IPs**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create Elastic IP | `allocate_address()` | `create_address()` |
| Describe Elastic IPs | `describe_addresses()` | `list()` |
| Release Elastic IP | `release_address()` | `delete()` |

**Tags**

| Functionality | AWS EC2 | Google Cloud Compute Engine |
| --- | --- | --- |
| Create tags | `create_tags()` | `add_tags()` |
| Describe tags |