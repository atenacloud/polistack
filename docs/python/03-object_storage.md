## Python

Reference 
- AWS: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html
- GCP: https://cloud.google.com/python/docs/reference/storage/latest

# Supported use cases and equivalence matrix for Object Store

| Functionality                | AWS S3                                  | GCP Storage                                           |
|------------------------------|-----------------------------------------|-------------------------------------------------------|
| Create bucket                | [create_bucket()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.create_bucket) | [Client.create_bucket()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.client.Client#create_bucket) |
| Delete bucket                | [delete_bucket()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.delete_bucket) | [Client.delete_bucket()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.client.Client#delete_bucket) |
| List buckets                 | [list_buckets()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.list_buckets) | [Client.list_buckets()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.client.Client#list_buckets) |
| Upload object                | [upload_file()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.upload_file) | [Blob.upload_from_filename()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.blob.Blob#upload_from_filename) |
| Download object              | [download_file()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.download_file) | [Blob.download_to_filename()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.blob.Blob#download_to_filename) |
| Delete object                | [delete_object()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.delete_object) | [Blob.delete()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.blob.Blob#delete) |
| Copy object                  | [copy_object()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.copy_object) | [Blob.copy()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.blob.Blob#copy) |
| Get object metadata          | [head_object()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.head_object) | [Blob.reload()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.blob.Blob#reload) |
| List objects in a bucket     | [list_objects()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.list_objects) | [Bucket.list_blobs()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.bucket.Bucket#list_blobs) |
| Generate pre-signed URL       | [generate_presigned_url()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.generate_presigned_url) | [Blob.generate_signed_url()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.blob.Blob#generate_signed_url) |
| Get bucket ACL               | [get_bucket_acl()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.get_bucket_acl) | [Bucket.acl](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.bucket.Bucket#acl) |
| Set bucket ACL               | [put_bucket_acl()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.put_bucket_acl) | [Bucket.acl.save()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.bucket.BucketACL#save) |
| Get object ACL               | [get_object_acl()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.get_object_acl) | [Blob.acl](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.blob.Blob#acl) |
| Set object ACL               | [put_object_acl()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.put_object_acl) | [Blob.acl.save()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.blob.BlobACL#save) |
| Enable versioning            | [put_bucket_versioning()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.put_bucket_versioning) | [Bucket.versioning_enabled](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.bucket.Bucket#versioning_enabled) |
| Disable versioning           | [put_bucket_versioning()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.put_bucket_versioning) | [Bucket.versioning_enabled](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.bucket.Bucket#versioning_enabled) |
| List object versions         | [list_object_versions()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.list_object_versions) | [Bucket.list_blobs()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.bucket.Bucket#list_blobs) (with `versions=True`) |
| Enable server-side encryption| [put_bucket_encryption()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.put_bucket_encryption) | [Bucket.default_kms_key_name](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.bucket.Bucket#default_kms_key_name) |
| Disable server-side encryption| [put_bucket_encryption()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.put_bucket_encryption) | [Bucket.default_kms_key_name](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.bucket.Bucket#default_kms_key_name) |
| Enable object-level encryption| [put_object()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.put_object) (with `ServerSideEncryption`) | [Blob.upload_from_filename()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.blob.Blob#upload_from_filename) (with `predefined_acl='private'`) |
| Disable object-level encryption| [put_object()](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html#S3.Client.put_object) | [Blob.upload_from_filename()](https://cloud.google.com/python/docs/reference/storage/latest/google.cloud.storage.blob.Blob#upload_from_filename) |

