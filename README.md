# vSphere-Project
# VMware Project – NTI R10
**Supervised by:** Dr. Anwar Fouad  

## 👥 Team Members
1. Nada Shabaan Ahmed  
2. Omar Mohamed Abdelwahab  
3. Nada Mohamed  
4. Baraa Sabry  
5. Beshoy Maged  

---

## 🟩 Step 1: Create NTI Cluster
- Right-click on the region and choose **New Cluster**.  
- Enable **DRS** and **HA**, then complete the setup.  
- Move the existing ESXi hosts into the new NTI cluster after placing them in **maintenance mode**.  
- Exit maintenance mode and delete any attached VMs from disk.  

---

## 🟩 Step 2: Add Port Groups
- Create two port groups:  
  - **Production** – assigned unlimited bandwidth  
  - **Developer** – assigned limited bandwidth  

---

## 🟩 Step 3: Configure Networking for FT & vMotion
- Enable and verify the **vMotion Network** settings.  
- Add a **VMkernel adapter** for Fault Tolerance (FT) on the appropriate port group.  

---

## 🟩 Step 4: Create Production VMs
- Create two virtual machines:  
  - One as a **Web Server**  
  - One as a **Database Server**  
- Enable **Fault Tolerance** on the Database VM.  
- Place both VMs in the **Production Port Group**.  
- Apply a **DRS Rule** to keep both VMs on the same host.  

---

## 🟩 Step 5: Apply Fault Tolerance on the Database VM
- Enable **Fault Tolerance (FT)** for the DB VM to ensure continuous availability in case of failure.  

---

## 🟩 Step 6: Create VM Affinity Rule
- Create a rule named **"Web DB Policy"**.  
- Configure the rule to keep Web and DB VMs together or separate depending on desired behavior.
----
- Creating a new cluster to gather all the hosts in it
  <img width="943" height="586" alt="image" src="https://github.com/user-attachments/assets/903a264c-d656-4d22-8c04-0151e9e98ff3" />
Put each esxi host into maintenance mode in order to 
relocate it to the new cluster
<img width="1114" height="584" alt="image" src="https://github.com/user-attachments/assets/13d082f8-5b0e-4f32-aca3-5478a897985e" />
Creating a new distributed port group for production purpose
<img width="1131" height="595" alt="image" src="https://github.com/user-attachments/assets/dd69e144-4a25-4c7f-bbcb-e7c8a10ba935" />
 No traffic shaping for the production port group in order 
to get full bandwidth
<img width="1147" height="691" alt="image" src="https://github.com/user-attachments/assets/5b19c0ec-cbd3-43c5-b5d3-4c2bcfb471c7" />
 Creating a new cluster for developing purpose 
<img width="1310" height="647" alt="image" src="https://github.com/user-attachments/assets/efa64e8a-c8c3-47a4-b1b7-305e847a6622" />
Enabling traffic shaping in order to limit the network bandwidth
<img width="1187" height="670" alt="image" src="https://github.com/user-attachments/assets/23f87a49-3486-4601-bfaf-7465f1557ac0" />
 Vmsin developer port group in order to get limited bandwidth
<img width="1219" height="620" alt="image" src="https://github.com/user-attachments/assets/50fb26f3-d0b8-49bb-9b9e-bf5d25087cfe" />
Setting a vm kernel adapter to enable fault tolerance
<img width="1381" height="616" alt="image" src="https://github.com/user-attachments/assets/18ae01af-cc46-41c5-8b8e-07ec2d28f75f" />
 Enabling fault tolerance on a vm in order to provide high availability
<img width="1382" height="627" alt="image" src="https://github.com/user-attachments/assets/53e726f7-a34a-4426-bf56-74b6b801e73d" />
Grouping two vms together due to mutual reliance
<img width="1393" height="581" alt="image" src="https://github.com/user-attachments/assets/d3e14ac1-b5cf-4dcf-93bd-54edb09e9e05" />
