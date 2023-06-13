## Python

Reference: 
- AWS: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html
- GCP: https://cloud.google.com/kubernetes-engine/docs/reference/rest

**Table: Kubernetes**

| Functionality                | AWS EKS                                 | GCP Kubernetes Engine                              |
|------------------------------|-----------------------------------------|----------------------------------------------------|
| Create cluster               | [create_cluster()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.create_cluster) | [create_cluster()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters/create) |
| Delete cluster               | [delete_cluster()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.delete_cluster) | [delete_cluster()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters/delete) |
| Describe cluster             | [describe_cluster()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.describe_cluster) | [get_cluster()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters/get) |
| List clusters                | [list_clusters()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.list_clusters) | [list_clusters()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters/list) |
| Scale cluster                | [update_cluster_config()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.update_cluster_config) | [update_cluster()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters/update) |
| Get cluster status           | [describe_cluster()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.describe_cluster) | [get_cluster()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters/get) |
| Get cluster credentials      | [describe_cluster()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.describe_cluster) | [get_cluster()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters/get) |
| List node groups             | [list_nodegroups()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.list_nodegroups) | [list_node_pools()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters.nodePools/list) |
| Create node group            | [create_nodegroup()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.create_nodegroup) | [create_node_pool()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters.nodePools/create) |
| Delete node group            | [delete_nodegroup()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.delete_nodegroup) | [delete_node_pool()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters.nodePools/delete) |
| Describe node group          | [describe_nodegroup()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.describe_nodegroup) | [get_node_pool()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters.nodePools/get) |
| Update node group            | [update_nodegroup_config()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/eks.html#EKS.Client.update_nodegroup_config) | [update_node_pool()](https://cloud.google.com/kubernetes-engine/docs/reference/rest/v1/projects.zones.clusters.nodePools/update) |