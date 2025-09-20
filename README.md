# aws-secure-ami
Automating the creation of secure Amazon Machine Images (AMIs) with AWS EC2 Image Builder. Includes image pipelines, recipes, and build components to keep AMIs patched, hardened, and consistent for faster, reliable server deployments.


## 🎥 Demo Video  

[Watch the video](https://youtu.be/a8pgmX_f9yI?si=jtL81ObC3ui2tV54)


This project walks through how I create a **secure Amazon Machine Image (AMI)** in AWS using **EC2 Image Builder**.  

An **AMI (Amazon Machine Image)** is a pre-configured template that includes:
- ✅ Operating system  
- ✅ Configurations  
- ✅ Software packages  

Instead of building a server from scratch each time, I simply launch new instances from this AMI.  


## 🔑 Why EC2 Image Builder?  
EC2 Image Builder helps me:
- Automate AMI creation  
- Keep AMIs **patched, hardened, and consistent**  
- Save time and reduce human error  


## 🛠️ Step-by-Step Process  

1. **Search for EC2 Image Builder** in the AWS console.  
2. **Create an Image Pipeline** – this is the set of instructions AWS follows to build the AMI.  
3. **Define the Image Recipe** – like a cooking recipe 🍰, it specifies:  
   - Base image (Amazon Linux, Ubuntu, etc.)  
   - Build components (e.g., update Linux kernel, install software, harden security)  
4. **Add Build Components** – for example:  
   - Update Linux kernel (to ensure the OS is patched and secure)  
   - Optional: install Apache, Nginx, or other tools  
5. **Skip/Adjust Test Components & Storage Volume** (if not needed).  
6. **Workflow** – leave default (AWS will handle build, test, and distribution).  
7. **Infrastructure Configuration** – the environment where the build runs (instance type, VPC, security groups, IAM role).  


## 📌 Example Choices in My Demo  
- Base image: **Amazon Linux (latest version)**  
- Build component: **Update Linux kernel**  
- Workflow: Default  
- Infrastructure config: Default  


## 🎯 Outcome  
By the end of this process, I have:  
- A **secure, patched AMI**  
- A reusable template for launching consistent, hardened servers  
- An automated pipeline I can rerun or schedule  

