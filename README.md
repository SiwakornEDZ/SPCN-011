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
# 2.ทำการติดตั้ง Ununtu
![image](https://user-images.githubusercontent.com/87377798/208241968-95d921e6-46c0-429d-8452-1187fc7eab46.png)







