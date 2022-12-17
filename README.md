## SPCN-011
สร้าง vm and ct on Proxmox cluster
# 1. create master vm (ubuntu-22.04)
![314460557_3384473538440414_6715910365347806246_n](https://user-images.githubusercontent.com/87377798/208240803-0e73fe16-179a-44fc-85c1-a066c57750e3.png)
# ตั้งชื่อ VM
![318755304_882856849517098_5037035500090954956_n](https://user-images.githubusercontent.com/87377798/208241286-65055094-0d8c-4c4d-b0e4-f410e313186c.png)
# เลือก OS ที่ต้องการติดตั้ง
![317332603_873316707424601_673092639177208994_n](https://user-images.githubusercontent.com/87377798/208241404-521e0500-3808-45b5-bc13-4aacb1586532.png)
# เลือก Bios และ กดติดตัั้ง Qemu Agent
![319288050_6096201857059687_2342501563599706103_n](https://user-images.githubusercontent.com/87377798/208241495-c47c4f8a-ce93-4163-8004-e1c00bba5ea6.png)
# เลือก Storage และเลือก storage size 32GB(Defalult)
![316935628_1593933581076656_1650177453456337731_n (1)](https://user-images.githubusercontent.com/87377798/208241583-1d083b5b-eae2-4642-8993-e284c95f2cfc.png)
# เลือก Socket และ Core ของ CPU ในระบบ Cpucore(1-2core)
![image](https://user-images.githubusercontent.com/87377798/208241671-4c7edcc6-702a-4bae-a7c2-b706059ce7d3.png)
# เลือกความจุของ Memory (2048 Mib)
![image](https://user-images.githubusercontent.com/87377798/208241739-4f3fcfa2-0b68-40c4-9ac8-8d51ad4e68b1.png)
# เลือก Network Device
![image](https://user-images.githubusercontent.com/87377798/208241789-aa0113ab-7004-4753-abd3-e9850949b917.png)
# เมื่อกด Create เสร็จสิ้นจะได้ result ดังรูป
![image](https://user-images.githubusercontent.com/87377798/208241896-817b7686-ded9-48be-b5fe-55896fdc835b.png)
# ทำการติดตั้ง Ununtu
![image](https://user-images.githubusercontent.com/87377798/208241968-95d921e6-46c0-429d-8452-1187fc7eab46.png)
![image](https://user-images.githubusercontent.com/87377798/208242012-e650a89c-b0bc-44c3-a322-c55f952c31d8.png)
![image](https://user-images.githubusercontent.com/87377798/208242025-79ad1964-a2dc-40f9-954a-da9e862104be.png)
![image](https://user-images.githubusercontent.com/87377798/208242044-37ed7f50-b1ca-422d-9c51-52f5099523b1.png)
![image](https://user-images.githubusercontent.com/87377798/208242086-1005960f-a014-45e7-bc54-800d6633ffcb.png)
![image](https://user-images.githubusercontent.com/87377798/208242105-33200f86-0f15-405a-afb2-172d4da7f65e.png)
![image](https://user-images.githubusercontent.com/87377798/208242114-5394a91e-4328-4703-b067-24452c603339.png)
![image](https://user-images.githubusercontent.com/87377798/208242135-f3d9d66d-16ef-4483-8e1f-0166f904e91f.png)
![image](https://user-images.githubusercontent.com/87377798/208242164-83308920-5870-4774-809e-86fc04ce2a99.png)
![image](https://user-images.githubusercontent.com/87377798/208242174-0a1614c9-48e2-4d1d-a638-dd7fb204b31d.png)
![image](https://user-images.githubusercontent.com/87377798/208242242-8bea8cf2-be48-49ea-b207-56a4b8c0b13b.png)
![image](https://user-images.githubusercontent.com/87377798/208242338-da38569c-a5e3-4f3e-a60c-93888ddf7428.png)
![image](https://user-images.githubusercontent.com/87377798/208242359-785bfdac-39ad-4678-ad6f-0878f8313464.png)
![image](https://user-images.githubusercontent.com/87377798/208242366-2d1fa090-e786-4359-91de-452a8812d706.png)
![image](https://user-images.githubusercontent.com/87377798/208242689-92cc34d9-ee85-42fa-91ae-3ad194500d35.png)
# คำสั่ง set time 
- date
- sudo timedatectl set-timezone Asia/Bangkok

![image](https://user-images.githubusercontent.com/87377798/208243350-559667c4-bafa-4c73-b6c7-39d165a8280d.png)
# คำสั่ง check Storage
- df -h

![image](https://user-images.githubusercontent.com/87377798/208243366-e01da2c7-8303-4b6f-a295-a077cbcaa287.png)
# คำสั่ง upgrade packgage
- sudo apt upgrade; sudo apt upgrade -y
![image](https://user-images.githubusercontent.com/87377798/208243338-780adb8b-7c3f-4618-a975-c9a4c7f8839d.png)
# คำสั่ง install QeMU Agent
- sudo apt install qemu-guest-agent
![image](https://user-images.githubusercontent.com/87377798/208243656-8c9b0c30-aa00-4d5d-96dd-2afd8c6168fd.png)
# คำสั่ง  QeMU Agent
- sudo systemctl start qemu-guest-agent
- sudo systemctl status qemu-guest-agent

![image](https://user-images.githubusercontent.com/87377798/208243764-18d95e9c-dcdd-4942-adde-3fd44902fbcf.png)
# คำสั่งติดตั้ง Editor nano
- sudo -i ตัดการพิม sudo
- apt install nano
- nano /etc/sudoers.d/siwakorn198
- siwakorn198 ALL=(ALL) NOPASSED: ALL
![image](https://user-images.githubusercontent.com/87377798/208244500-a02e66d0-deae-4332-bd65-4ce263b3abe5.png)
# คำสั่งติดตั้งและใช้งาน ping 
- apt install iputils-ping
![image](https://user-images.githubusercontent.com/87377798/208244673-ac9b68d9-d931-49ba-8b45-47a429a706e4.png)
- ping 1.1.1.1
![image](https://user-images.githubusercontent.com/87377798/208244717-dbe72a1a-4b0d-4f26-8a59-647b1ce51c0b.png)
# คำสั่งติดตั้งและใช้งาน dns-dig
- apt install dnsutils
- dig
![image](https://user-images.githubusercontent.com/87377798/208244834-325297ed-142f-47cc-8da4-ae5f3e8a83fc.png)
# คำสั่งติดตั้งและใช้งาน ntpdate
- apt install ntpdate
![image](https://user-images.githubusercontent.com/87377798/208244901-90c280ce-5603-4792-b45b-1bd9c96a57d3.png)
- ntpdate th.pool.ntp.org
![image](https://user-images.githubusercontent.com/87377798/208244976-c72658f6-58b8-43f2-97d9-85eccd83e0fc.png)
# คำสั่งติดตั้งและใช้งาน crontab
- apt install cron 
- crontab -e
- พิมคำสั่งใน Editor @hourly /usr/sbin/ntpdate th.pool.ntp.org
![image](https://user-images.githubusercontent.com/87377798/208245215-e6ac9c94-fb77-4d5a-8012-650b8b2e5b52.png)

# clone master vm to tamplate
- กดคลิกขวาที่ VM ที่เราสร้างไว้ และเลือก Convert to template

![image](https://user-images.githubusercontent.com/87377798/208247970-2bbc5e54-a552-4a37-a7ab-7599fa8c7cdb.png)

- จะได้ตัว VM เป็นแบบ template ดังรูป

![image](https://user-images.githubusercontent.com/87377798/208248036-a1b09d65-3333-4816-9fde-b0afac525cf8.png)

# clone from template สร้าง vm ใหม่จำนวน 2 vm
- กดคลิกขวาที่ template และเลือก clone

![image](https://user-images.githubusercontent.com/87377798/208248091-038a78d5-8b04-4247-aa2f-fffbd7d487d0.png)

- ตั้งชื่อ VM ที่เรา clone ออกมาทั้ง 2 ตัว

- ตัวที่ 1
- 
![image](https://user-images.githubusercontent.com/87377798/208248138-a72ac484-886c-49e0-9a61-42a4740dfcaa.png)

- ตัวที่ 2

![image](https://user-images.githubusercontent.com/87377798/208248180-c3d31dcf-9af1-4922-89ca-aafdffcc3253.png)


```
sudo hostnamectl set-hostname [ชื่อที่ต้องการเปลี่ยน]
```


# 2. create vm from other os
  
  
  
# 3.create container template (select from CT list)
 - คลิกที่ Create CT
 ![314428517_1526729121088217_7066711563116917479_n](https://user-images.githubusercontent.com/87377798/208245886-9e74ed75-00b8-40f9-b1b2-37f0bcf635fc.png)
 - ตั้งชื่อ ใส่รหัสและ LOAD SSH Public Key File
 
 ![image](https://user-images.githubusercontent.com/87377798/208246167-a1bb2852-d04a-4e7e-8149-b468086aca8b.png)
 - เลือก Template
 
 ![image](https://user-images.githubusercontent.com/87377798/208246201-27447e12-146a-4974-a522-d2e2e6372f09.png)
 - เลือก Disk 
 
 ![image](https://user-images.githubusercontent.com/87377798/208246251-a0802ca4-12bf-4ebf-a3a1-619d9bf0adfa.png)
 - เลือก Cpu
 
 ![image](https://user-images.githubusercontent.com/87377798/208246269-a24bc473-1b18-4824-94af-8d1afdf54198.png)
 - เลือก Memory
 
 ![image](https://user-images.githubusercontent.com/87377798/208246283-da128b08-97ab-4224-9b0d-cf11bf0b6540.png)
 - เลือก IPv4 เป็น DHCP และ IPv6 เป็น SLAAC ดังรูป
 
 ![image](https://user-images.githubusercontent.com/87377798/208246369-8ff6a0dc-31dd-4b4b-a101-b9c7a980372c.png)
 - สร้างเสร็จสิ้น
 
 ![image](https://user-images.githubusercontent.com/87377798/208246483-af447f36-0b27-402a-96a5-ae95ab8f40af.png)
 - รันผ่าน Console
 
 ![image](https://user-images.githubusercontent.com/87377798/208246720-c694d652-ea1f-45b5-a051-c82f9ca31bed.png)
 
 # คำสั่งติดตั้งและใช้งาน htop
 - apt install htop
 - htop
 
 ![image](https://user-images.githubusercontent.com/87377798/208246899-eab9b05b-2241-46ab-b6c6-b6e42ae75023.png)
 
 # คำสั่งสร้างไฟล์และอ่านไฟล์
 สร้างไฟล์ชื่อ 2456.data ขนาด 2GB
 - dd if=/dev/zero of=2456.data bs=512 count=2M
 
 ![image](https://user-images.githubusercontent.com/87377798/208247177-ae6ea0e2-72b8-48c7-8f1c-7df854e3a8b2.png)
 
 อ่านไฟล์ชื่อ 2456.data
 
 - dd if=2456.data of=/dev/null bs=512 count=2M
 
 ![image](https://user-images.githubusercontent.com/87377798/208247244-2ed95823-146b-4a34-8d4e-d5b5048747fb.png)


 

 


 
 
































