# File_Recovery-using-Autopsy

## Aim
The objective of this guide is to demonstrate how to:  
 - Create a **Virtual Hard Disk (VHD)**.  
 - Add images to the disk, delete them, and recover them using **Autopsy**.  
 - Understand the forensic recovery process for deleted files.  
 - Learn how to remove the virtual disk after completing the experiment.

## Virtual Disk Creation & File Recovery using Autopsy 


## Step 1: 
   Create a Virtual Hard Disk (VHD) 

### **1. Open Disk Management**  
- Press **Windows + X** → Click **Disk Management** 

![image](https://github.com/user-attachments/assets/cd108ac7-133c-4ff2-8cc4-37d8b9e2047b)


### **2. Create a New VHD**  
- Click **Action** (top menu) → **Create VHD**.  

![image](https://github.com/user-attachments/assets/e8ff97d9-7eeb-4fbc-b310-9accb6f251d3)


### **3. Choose File Location & Size**  
- Click **Browse** and select where to save the VHD file (e.g, `C:\new VHD.vhd`)
- Set the **size** (e.g: `1GB`) 
- Choose **VHD (Fixed Size)** and Click **OK**

![image](https://github.com/user-attachments/assets/c12e71fe-7af0-4f18-a429-bead57aca378)


### **4. Initialize the Disk**  
- In **Disk Management**, find your new disk (marked as "Not Initialized").  

![image](https://github.com/user-attachments/assets/8254ec35-fe12-45ea-be86-a8b420820a6f)


- Right-click the disk → Click **Initialize Disk**.

![image](https://github.com/user-attachments/assets/b62aca2a-9b7c-4852-b853-5ba60480b1d5)


- Select **MBR (Master Boot Record)**. 

![image](https://github.com/user-attachments/assets/a5c29b82-8030-4f1a-86a2-36d8baac8a98)


### **6. Create & Format the Partition**  
- Right-click the **Unallocated Space** → Click **New Simple Volume**.  
![image](https://github.com/user-attachments/assets/8c9c4972-7f84-44b0-bd4f-ef7f5f3b7c28)

![image](https://github.com/user-attachments/assets/5e7acaec-cbff-4b8f-bbed-bf72074a3897)

![image](https://github.com/user-attachments/assets/2b30f330-5510-451f-8d41-e6fec21ec00c)



- Click **Next** → **Click on Mount in the following empty NTFS folder** → **Browse** → **Assign a drive letter (e.g., `C: or D:`)** → **New folder** → **OK**

![image](https://github.com/user-attachments/assets/193e0439-26c8-4193-b620-bf661865ba54)

![image](https://github.com/user-attachments/assets/0dbf67aa-82a0-4d61-ad06-f6ccc7502ebd)

![image](https://github.com/user-attachments/assets/5008d65b-fb44-4f5f-ab5b-7b2b4129a642)

- Click **next** → **Finish**. 

---

## **Step 2: Add & Delete Files for Recovery** 

### **1. Copy Files to the Virtual Disk**  
- Open **File Explorer** → Go to the new drive (`C: or D:`), where the folder created in the previous step
- Create a new folder (`TestFolder`) and copy **images or files** into it.  

### **2. Delete the Files**  
- Select any one or two images → Press **Delete**.  
- Empty the **Recycle Bin** to permanently delete them.  

---

## **Step 3: Recover Deleted Files Using Autopsy**  
### **1. Open Autopsy & Create a New Case** 

- Launch **Autopsy** and **Run as a administrator**  
- Click **Create New Case**.  

![image](https://github.com/user-attachments/assets/41363997-b59f-409b-babc-f6b8fad61991)


- Enter a **Case Name** (e.g., `Autopsy1`).  
- Choose a **Case Folder** location.  
- Click **Next** → Click **Finish**.  

![image](https://github.com/user-attachments/assets/5a79d0b1-f785-4894-a5d6-730db4650915)


### **2. Add the Virtual Disk as an Evidence Source**  
- Click **Add Data Source**  → **Select Host**

![image](https://github.com/user-attachments/assets/eaa59a6f-7178-4813-a7d1-05129c304b5a)


- Select **Local Disk** → **next** 

![image](https://github.com/user-attachments/assets/351168db-db48-40b6-807a-18cbffa0114a)


- Select Disk → **Choose the VHD drive (`Drive1`)**
![image](https://github.com/user-attachments/assets/026fc312-e81d-416c-b730-e64e97736492)


- Click **Next** → Keep default settings → Click **Finish**.  
- Wait for Autopsy to process the disk.  

### **3. Recover Deleted Files**  
- Go to **File Views** (left panel).  

![image](https://github.com/user-attachments/assets/fcb12989-49b9-4ca8-b41c-55a497398e79)


- Click **Deleted Files** → Find your deleted images.  
- Right-click an image → Click **Extract File**.  

![image](https://github.com/user-attachments/assets/facf22f3-f85f-4529-a679-6454b9c0a26e)

- Select a folder to see the recovered files (e.g., `C:\image_recovery`).  

**Your deleted images are now recovered!**  

---

## **Step 4: Delete the Virtual Disk (Optional Cleanup)** 

### **1. Detach the VHD**  
- Open **Disk Management** (`Win + X` → Disk Management).  
- Find the **virtual disk** (`C: or D:`).  
- Right-click the disk (not the partition) → Click **Detach VHD**.  

### **2. Delete the VHD File**  
- Open **File Explorer**.  
- Go to the location where you saved the `.vhd` file (e.g., `C:\new VHD.vhd`).  
- **Delete** the `.vhd` file.  
- Empty the **Recycle Bin**.  

**Your virtual disk is completely removed!**  
 
---

 OUTPUT :
 ![425719626-22141e09-d638-46d3-959d-edae99b483d0](https://github.com/user-attachments/assets/342a6db3-78aa-4b61-a948-fff6bbefcffd)




## Result :
 This guide covers creating a Virtual Hard Disk (VHD), adding, deleting, and recovering images using Autopsy, and safely deleting the virtual disk after the experiment.
