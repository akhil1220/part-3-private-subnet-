## Creating Private subnet ##
## Overview ##
In this project i created a Private subnet in my VPC.

## Architecture Diagram ##
<pre>
+-----------------------------------+    
|          VPC (10.0.0.0/16)        |                           
|                                   |
|   +--------------------------+    |
|   |     Internet Gateway  2  |    | 
|   +------------+-------------+    |
|                |                  |
|   +--------------------------+    |
|   |      Route Table         |    |
|   |    0.0.0.0/0 → IGW       |    |
|   +------------+-------------+    |
|                |                  |
|   +--------------------------+    |
|   |      Private  Subnet     |    |
|   |      (10.0.1.0/24)       |    |                        
|   +--------------------------+    |
|          Network ACL              |
+-----------------------------------+
</pre>

## steps to create A private subnet ##
1. I have used all the resources that i have created in my last project where i have created a **Virtual private cloud** and added required **public subnet, internet gateway, Network ACL and security group**.
2. Next  i created a private subnet and selected a different **Availability zone**. And also Assigned different **CIDR Block (10.0.1.0/24)**.
3 Added route table and attached to my private subnet.
4. Finally to round off i have set up a **Network ACL** and did not add any inbound and out bound rules for now. Then attached This Network ACL to private subnet.
   
## Screeenshots ##

## *Private Subnet* ##
  <img width="2930" height="1022" alt="Image 11-4-25 at 2 45 AM" src="https://github.com/user-attachments/assets/85959202-5d59-497d-a563-695aafe1eeff" />


## *Route table* ##

<img width="2924" height="970" alt="Image 11-4-25 at 2 52 AM" src="https://github.com/user-attachments/assets/01a3a73d-7dcc-4e51-8457-81d425874f6a" />

## *Network ACL* ##
<img width="2928" height="958" alt="Image 11-4-25 at 2 51 AM" src="https://github.com/user-attachments/assets/bc2cb867-9368-48a5-966e-9a6ea0d5d191" />

## Key learnings ##
1. Learned about the importance of creating a different CIDR block for each individual subnet.
2. Learned how to create a private subnet.
3. Gained knowledge on creating Network ACL.

## Next Steps ##
In the next project i will use this set and will launch VPC resources.

  
