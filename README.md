# terraform-demo2e
---
#Import existing S3 Bucket
---
## Note: navigate to “.tf” files. Open “resource_s3.tf” and update the “bucket” argument.
---
#Once you clone this repo run below commands:
---
terraform init

---
terraform validate

---
terraform import "aws_s3_bucket.bucket1" idktecharcho-first-st-bucket

---
#if below error come then ensure that bucket1 exists or else you can create it with different name and ensure you update the command with that name.
---
aws_s3_bucket.bucket1: Importing from ID "idktecharcho-first-st-bucket"...
aws_s3_bucket.bucket1: Import prepared!
  Prepared aws_s3_bucket for import
aws_s3_bucket.bucket1: Refreshing state... [id=idktecharcho-first-st-bucket]
╷
│ Error: Cannot import non-existent remote object
│
│ While attempting to import an existing object to "aws_s3_bucket.bucket1", the provider
│ detected that no object exists with the given id. Only pre-existing objects can be
│ imported; check that the id is correct and that it is associated with the provider's
│ configured region or endpoint, or use "terraform apply" to create a new remote object for
│ this resource.

---
terraform plan

---
terraform apply

---
terraform destroy
