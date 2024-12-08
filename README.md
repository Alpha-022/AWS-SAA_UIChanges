## Scribe no. 1
https://scribehow.com/shared/Creating_an_IAM_User_and_User_Group_in_AWS_Management_Console__hWNiiXlcRJKFqYZZEJD-cg

**Small UI Change**: The **`Create User`** button has been replaced with a **`Next`** button. On the next page, users can optionally select tags before clicking the **`Create User`** button to complete the process.


## Scribe no. 6
https://scribehow.com/shared/Playing_with_EC2_Instance_Metadata_Service_and_Dynamic_Data__6NCryFcnSFWRrA8ooVRjuQ

Lab not working


## Scribe no. 21

https://scribehow.com/shared/Understand_AWS_Elastic_Load_Balancing_Listeners___tkzQLJhSiulmm_3Ro3kBw

**Port Configuration**: The port should be set to `8080`; however, in the screenshot, it is shown as 880.

![image](https://github.com/user-attachments/assets/5447566c-9fd2-4ea0-b15f-ad97748ef4b1)

## Scribe no. 37 
https://scribehow.com/shared/Getting_started_with_Amazon_ElastiCache_for_Memcached__dSMaRWzMSaCrgzs25HfUsg

**New Option**: A new option, **`Valkey`**, has been added alongside `Redis` and `Memcached` when clicking on **Get Started.**

![image](https://github.com/user-attachments/assets/38113e51-0027-420b-8547-5457abefddb4)

**Suggestion**: We should mention that tags are not being added here and we are proceeding without adding tags. This is important because if the **`Add Tags`** button is clicked and the user proceeds without adding tags, they will encounter an error.

## Scribe no. 44
https://scribehow.com/shared/Creating_your_first_AWS_Lambda_Function__yiSoRke_T3q56oZpUcRduA

**UI Changes in Source Code Section**: The UI in the source code section has been updated, and the "Test" button is no longer available. However, you can revert to the old UI by clicking "Switch to Old Editor" and then click on "Test." Additionally, the "Configure Test Event" option is now available in the dropdown menu under "Test."

![image](https://github.com/user-attachments/assets/42c03f5e-846a-4002-818a-f667b53d9aea)

![image](https://github.com/user-attachments/assets/f594df8b-4b9f-4def-b52f-e7889731c3eb)


## Scribe no. 45 

https://scribehow.com/shared/Exploring_Lambda_Functions__Monitoring_and_more__kwARer8ERkqkvd-kw14AOg

**Massive UI Change**: This may require creating a new scribe from scratch.

## Scribe no. 47 
https://scribehow.com/shared/Creating_Your_First_Auto_Scaling_Group__cy6hH_s6QAivHx_E_hThaQ

**Launch Template Issue**: When creating a launch template for the first time, it may automatically select a subnet or security group, which needs to be manually removed.

Additionally, for the **`Shutdown Behavior`** and **`Stop Hibernate Behavior`** settings, you must select "Don't include in launch template."

## Scribe no. 48
https://scribehow.com/shared/Exploring_API_Gateway__Stages_and_more__yqZ2Rt04SnGpnp7gsBKq9g

**Clarification**: In some areas, we should mention that we are just exploring the options and not actually creating them. This applies to items like keys, usage plans, and similar configurations.

## Scribe no. 54 
https://scribehow.com/shared/Calling_APIs_from_EC2_instances_using_crontab__x4aebBgOQRKkfJk-xwPB9Q

**Typo Correction**: There is a typo in the command; it should be `crontab`, not `corntab`.

![image](https://github.com/user-attachments/assets/05b6003f-a4b0-494c-91a9-c8e22e1cbe5c)


**Suggestion - Add a Note**: To make the `crontab` command work, you need to install `cronie` by running the following command:

```bash
sudo yum install cronie
```

## Scribe no. 60 
https://scribehow.com/shared/Creating_a_Public_Website_with_S3__VYqpxEKzQdOsAo8AoInkow


**Correction**: The provided code is incorrect.

***Given Code***:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "_",
      "Action": [
        "s3:GetObject"
      ],
      "Resource": ["arn:aws:s3:::_**_yourbucketname_**_/*"]
    }
  ]
}

```

***Corrected Code***:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": [
        "s3:GetObject"
      ],
      "Resource": ["arn:aws:s3:::_**_yourbucketname_**_/*"]
    }
  ]
}

```

***Difference***:

-   `"Principal": "_"` should be corrected to `"Principal": "*"`.

**Instruction Update**: Instead of saying "Tick the checkbox **`Block all public access`** and click on the **`Save changes`** button," we should say:

"Remove the tick from the **`Block all public access`** checkbox and then click the **`Save changes`** button."

## Scribe no. 63
https://scribehow.com/shared/Implementing_S3_Event_Notifications_with_AWS_Lambda__t1vK-oRGRn-k9y2U8UX04w

**UI Changes in Source Code Section**: The UI in the source code section has been updated, and the "Test" button is no longer available. However, you can revert to the old UI by clicking "Switch to Old Editor" and then click on "Test." 

## Scribe no. 66
https://scribehow.com/shared/Exploring_Bucket_and_Object_ACLs_in_S3__BVuROwhZQbmQA242AGmm0Q

**UI Change**: The Lifecycle Rule UI has changed. Now, you need to click on the options provided in the **`Lifecycle Rule Actions`**.

![image](https://github.com/user-attachments/assets/17526e7b-30fe-4956-b821-a30c2622f776)


## Scribe no. 67
https://scribehow.com/shared/Exploring_S3_Cross_Region_and_Same_Region_Replication__HYQKmaZDRb-0ZTqI4xjIEA

**Correction**: There is a mistake in the text. Users need to click on **my-aws-bucket-in28minutes**, so the bucket name in both steps should be corrected. The screenshot is correct, only the text needs to be updated.

![image](https://github.com/user-attachments/assets/d2b84491-dcb1-4317-945f-4ef659b9477f)

![image](https://github.com/user-attachments/assets/438116bf-7702-4ee0-87ad-3528c091d45f)


## Scribe no. 68
https://scribehow.com/shared/Exploring_S3_Object_Level_Configurations__l8RyHKvKQhGX0Ku5DLQ_3g

**Metadata Edit Issue**: The metadata edit option is not working. To update object metadata, use the improved **Copy** action and select **Specify settings**.

## Scribe no. 96 
https://scribehow.com/shared/Creating_Your_First_RDS_Database_in_AWS__npccXKYTRse0Ba8bG3fncg

**Storage Autoscaling**: Storage autoscaling is available under the **`Additional Storage Configuration`** section.


## Scribe no. 97
https://scribehow.com/shared/Creating_an_EC2_instance_to_connect_to_RDS_Database__eVVBl7QmRFiYSohIAJ9KTw

**Final Step**: The last step should be to launch the instance. If it is not launched, the next lab will not work.

## Scribe no. 130
https://scribehow.com/shared/Deleting_Network_Load_Balancers_and_Target_Groups__oMl66DGvSteQCpdGZVQsYg

**Suggestion**: Add a note to disable deletion protection if the deletion of the load balancer fails. To do this, edit the load balancer attributes.

## Scribe no. 116
https://scribehow.com/shared/Creating_an_SNS_Topic_and_Registering_a_Lambda_to_Subscribe__alURWvWeReuDCX6Pdnv6tw

**UI Changes in Source Code Section**: The UI in the source code section has been updated, and the "Test" button is no longer available. However, you can revert to the old UI by clicking "Switch to Old Editor" and then click on "Test." 


## Scribe no. 124 
https://scribehow.com/shared/Using_Multiple_Target_Groups_for_Microservices_Architectures__HHBKBtxGTPGY0iqlxkT5eg

**Suggestion**: The Bash script should be provided for copying, so learners don't need to write it manually.

# General problem

**Issue with EC2 Instance Connect**: Labs related to EBS or steps involving the EC2 connect process may cause problems, as I personally faced the issue: _EC2 Instance Connect is unable to connect to your instance._

**Solution**: To resolve this, go to the security group and allow inbound SSH traffic (port 22) by following these steps:

-   **Type**: SSH
-   **Protocol**: TCP
-   **Port Range**: 22
-   **Source**: Your IP address (e.g., `203.0.113.0/32`) or a broader range (e.g., `0.0.0.0/0` for all IPs, but this is not recommended for production).

**Example: Scribe no. 84:**
https://scribehow.com/shared/1__Mounting_Elastic_Block_Storage_onto_a_EC2_Instance__kRmkYfQGQCupLyZZBty4sw
