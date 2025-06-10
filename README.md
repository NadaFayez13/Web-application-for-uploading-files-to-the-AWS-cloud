# CLOUDY FILES

This project is a cloud-based web application that allows users to securely upload and access their files at any time. Once a file is uploaded through the user interface, it is automatically classified and stored in **Amazon S3**, with download links generated on the spot—making the process smooth, fast, and efficient.
The backend is built using **Flask**, and integrates with AWS services such as **EC2** for **24/7** hosting, and **S3** for scalable, secure storage. File handling and AWS operations are powered by the boto3 SDK, and the frontend is designed to support common file formats like **PDF**, **JPG**, **PNG**, and **TXT**.


## **Cloud Infrastructure**
### **Virtual Private Cloud (VPC):**
We created a fully isolated VPC to serve as the secure network layer of the application. It includes **private IP address** management, **DNS** support, and custom **route tables** to control inbound and outbound traffic. This ensures a tightly secured and performance-optimized environment.

### **Security Configurations:**
Custom Security Groups were used to define which ports and IP ranges are allowed to connect to the server. This firewall-level configuration protects the EC2 instance by restricting access to only necessary services (**HTTP on port 80 ,HTTPS on port 443**).

### **Amazon EC2:**
Our application runs on a **t2.micro EC2 instance** hosted inside our VPC. The instance is assigned both public and private IPs and is connected to an IAM Role that allows it to communicate directly with Amazon S3, without the need to expose credentials.

### **Billing and Monitoring:**
We set up a **CloudWatch dashboard** to monitor **CPU and network usage** in real-time, along with a **billing alarm** that sends alerts if cloud spending exceeds a defined threshold. This ensures both **performance and cost-efficiency**.


