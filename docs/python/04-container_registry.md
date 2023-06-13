## Python 

Reference
- AWS: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html
- GCP: https://cloud.google.com/python/docs/reference/artifactregistry/latest

# Supported use cases and equivalence matrix for Container Registry

**Table: Container Registry**

| Functionality                | AWS ECR                                 | GCP Container Registry                              |
|------------------------------|-----------------------------------------|----------------------------------------------------|
| Create repository            | [create_repository()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.create_repository) | [create_repository()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#create_repository) |
| Delete repository            | [delete_repository()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.delete_repository) | [delete_repository()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#delete_repository) |
| Describe repository          | [describe_repositories()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.describe_repositories) | [get_repository()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#get_repository) |
| List repositories            | [describe_repositories()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.describe_repositories) | [list_repositories()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#list_repositories) |
| Upload image                 | [put_image()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.put_image) | [upload_file()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#upload_file) |
| Delete image                 | [batch_delete_image()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.batch_delete_image) | [delete_package()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#delete_package) |
| List images                  | [describe_images()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.describe_images) | [list_packages()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#list_packages) |
| Get image details            | [describe_images()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.describe_images) | [get_package()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#get_package) |
| List repositories in registry| [describe_repositories()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.describe_repositories) | [list_repositories()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#list_repositories) |
| Set repository IAM policy    | [set_repository_policy()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.set_repository_policy) | [update_repository()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#update_repository) |
| Get repository IAM policy    | [get_repository_policy()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.get_repository_policy) | [get_repository()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#get_repository) |
| Tag image                    | [put_image()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.put_image) | [tag_version()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#tag_version) |
| List image tags              | [describe_images()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.describe_images) | [list_tags()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#list_tags) |
| Delete image tag             | [untag_resource()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ecr.html#ECR.Client.untag_resource) | [untag_version()](https://cloud.google.com/python/docs/reference/artifactregistry/latest/artifactregistry_v1beta2.ArtifactRegistryClient#untag_version) |

