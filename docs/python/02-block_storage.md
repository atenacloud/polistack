## Python

Reference 
- AWS: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html
- GCP: https://cloud.google.com/python/docs/reference/compute/latest

# Supported use cases and equivalence matrix for Volumes, Snapshots and Images


**Table 1: Volumes and Snapshots**

| Functionality                | AWS EBS                                 | GCP Compute Engine                                    |
|------------------------------|-----------------------------------------|-------------------------------------------------------|
| Create volume                | [create_volume()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.create_volume) | [disks().insert()](https://cloud.google.com/python/docs/reference/compute/latest/disks/insert) |
| Delete volume                | [delete_volume()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.delete_volume) | [disks().delete()](https://cloud.google.com/python/docs/reference/compute/latest/disks/delete) |
| Describe volumes             | [describe_volumes()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.describe_volumes) | [disks().get()](https://cloud.google.com/python/docs/reference/compute/latest/disks/get) |
| Attach volume                | [attach_volume()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.attach_volume) | [instances().attach_disk()](https://cloud.google.com/python/docs/reference/compute/latest/instances/attach_disk) |
| Detach volume                | [detach_volume()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.detach_volume) | [instances().detach_disk()](https://cloud.google.com/python/docs/reference/compute/latest/instances/detach_disk) |
| Create snapshot              | [create_snapshot()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.create_snapshot) | [snapshots().insert()](https://cloud.google.com/python/docs/reference/compute/latest/snapshots/insert) |
| Delete snapshot              | [delete_snapshot()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.delete_snapshot) | [snapshots().delete()](https://cloud.google.com/python/docs/reference/compute/latest/snapshots/delete) |
| Describe snapshots           | [describe_snapshots()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.describe_snapshots) | [snapshots().get()](https://cloud.google.com/python/docs/reference/compute/latest/snapshots/get) |
| Create volume from snapshot   | [create_volume()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.create_volume) (with `SnapshotId`) | [disks().insert()](https://cloud.google.com/python/docs/reference/compute/latest/disks/insert) (with `sourceSnapshot`) |
| List volumes                 | [describe_volumes()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.describe_volumes) | [disks().list()](https://cloud.google.com/python/docs/reference/compute/latest/disks/list) |
| List snapshots               | [describe_snapshots()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.describe_snapshots) | [snapshots().list()](https://cloud.google.com/python/docs/reference/compute/latest/snapshots/list) |
| Modify volume                | [modify_volume()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.modify_volume) | [disks().resize()](https://cloud.google.com/python/docs/reference/compute/latest/disks/resize) |

**Table 2: Images**

| Functionality                | AWS EC2                                 | GCP Compute Engine                                    |
|------------------------------|-----------------------------------------|-------------------------------------------------------|
| Create image from volume      | [create_image()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.create_image) | [images().insert()](https://cloud.google.com/python/docs/reference/compute/latest/images/insert) |
| Delete image                 | [deregister_image()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.deregister_image) | [images().delete()](https://cloud.google.com/python/docs/reference/compute/latest/images/delete) |
| Describe images              | [describe_images()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.describe_images) | [images().get()](https://cloud.google.com/python/docs/reference/compute/latest/images/get) |
| Create disk from image        | [create_volume()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ebs.html#EBS.Client.create_volume) (with `ImageId`) | [disks().insert()](https://cloud.google.com/python/docs/reference/compute/latest/disks/insert) (with `sourceImage`) |
| List images                  | [describe_images()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.describe_images) | [images().list()](https://cloud.google.com/python/docs/reference/compute/latest/images/list) |
| Recover image from snapshot   | [register_image()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.register_image) | [images().insert()](https://cloud.google.com/python/docs/reference/compute/latest/images/insert) (with `sourceSnapshot`) |
