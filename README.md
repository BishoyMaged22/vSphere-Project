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
<img width="975" height="315" alt="image" src="https://github.com/user-attachments/assets/b825f3c8-9349-4e06-a112-1b4e0213717d" />
<img width="975" height="279" alt="image" src="https://github.com/user-attachments/assets/6957c7fb-06f4-4c29-aa38-228a06be0a53" />
<img width="975" height="458" alt="image" src="https://github.com/user-attachments/assets/9400f82c-91bf-4cd7-9793-f0b0ed027bba" />
<img width="975" height="587" alt="image" src="https://github.com/user-attachments/assets/c2fe6c10-742b-48c7-a07c-aca6cb57c6b4" />
<img width="975" height="601" alt="image" src="https://github.com/user-attachments/assets/11f68ba1-6242-4b40-b8aa-97a839a7fa37" />
<img width="975" height="455" alt="image" src="https://github.com/user-attachments/assets/93cb9487-fe70-4db6-9d62-3c685f166ce1" />
<img width="928" height="522" alt="image" src="https://github.com/user-attachments/assets/b239ae3c-491f-4659-b574-6109f276c833" />
<img width="975" height="592" alt="image" src="https://github.com/user-attachments/assets/9fcb52cc-3d2d-4fc1-81d3-beb2b3f47a02" />
<img width="975" height="582" alt="image" src="https://github.com/user-attachments/assets/8d082679-6619-4a6d-9902-0102253dc80f" />
<img width="975" height="318" alt="image" src="https://github.com/user-attachments/assets/5c3a3d8c-ec7f-4b39-a853-66943011467f" />
