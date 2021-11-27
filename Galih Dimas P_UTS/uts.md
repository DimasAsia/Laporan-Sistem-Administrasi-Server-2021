# Laporan UTS Instalasi Windows Server 2022

Pada kesempatan kali ini terdapat soal, yang menginstruksikan untuk melakukan instalasi windows server 2022 pada virtual machine.

![gambar soal](asset/1.PNG)

Dari penjelasan soal diatas kita melakukan penginstalan windows server 2022 pada virtual machine. Soal UTS dapat diaskes [Disini.](https://yptorid-my.sharepoint.com/:w:/g/personal/aldo_ittelkom-sby_ac_id/EahwnD4AudVAqCDtSDN9JVsBTLMMU-hBAnMwq-2TthH9dA?e=gpexdw)

## Installation windows server 2022
---
### 1. Download file iso windows server 2022


- Open link berikut untuk mendownload file windows server 2022

    https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022
        
    - Download windows server 2022 file iso

        ![](asset/0.png)
    

### 2. Open virtualbox untuk langkah awal instalasi pada virtualbox


- Tampilan virtualbox awal

     ![](asset/3.png)
    
- Create new virtual machine untuk windows server 2022

    ![](asset/2.png)

- Beri nama untuk virtual machine tersebut

    ![](asset/4.png)

-  Setting aloksai RAM dan juga setting disk baik size maupun type yang digunakan pada virtual machine

    - Setting RAM

        ![](asset/5.png)
    
    - Create Disk
    
        ![](asset/6.png)
    
    - Setting Disk type
    
        ![](asset/7.png)

        ![](asset/8.png)
    
    - Setting location and size of Disk
    
        ![](asset/9.png)

- Hasil create virtual machine

    ![](asset/10.png)

)

### 3. Setting pada storage untuk select iso file windows server dan juga setting network 


- Open setting pada virtual machine yang telah dibuat

    ![](asset/11.png)

    - Setting storage iso

        ![](asset/12.png)

        ![](asset/13.png)

        ![](asset/14.png)

        ![](asset/15.png)

        ![](asset/16.png)

    - Setting network

        ![](asset/17.png)
    

### 4. Open virtual machine yang telah dibuat

- start virtual machine windows server 2022

    ![](asset/18.png)

- instalasi wizzard windows server 2022

    ![](asset/19.png)

- install windows server 2022

    ![](asset/20.png)

    - select windows server 2022 desktop experience  
            
        ![](asset/21.png)

    - setuju license terms
            
        ![](asset/22.png)

    - select windows server 2022 install microsoft server advanced
            
        ![](asset/23.png)

    - location installation of windows server 2022

         ![](asset/24.png)

    - installation progress

         ![](asset/25.png)

    - custom password administrator 

         ![](asset/26.png)
    
    - tampilan lock desktop dari windows server 2022

         ![](asset/27.png)

    - akses menu dengan input "ctrl + alt + delet" lalu masukkan password administrator yang telah dibuat

         ![](asset/28.png)

    -  windows server 2022 berhasil di install

         ![](asset/29.png)

## Installation Add-ons Windows Server 2022
- Rename nama computer untuk memudahkan

    - open windows powershell

        ![](asset/30.png)

    - rename nama computer menjadi Server 2022
        ![](asset/31.png)
---
### Installation Active Directory Domain Services
- open server manager

    ![](asset/32.png)
- buka manage lalu pilih add roles dan features

    ![](asset/33.png)

- klik next

    ![](asset/34.png)
- pilih role based installation
  
    ![](asset/35.png)
- pilih server from the server pool
  
    ![](asset/36.png)
- add fitur active directory domain service
  
    ![](asset/37.png)
---
### Installation DNS server
- add fitur dns
  
    ![](asset/38.png)
---
### Installation Net Framework 3.5
- add fitur Net Framework 3.5 yang include net 2.0 dan 3.0 dan group policy management
  
    ![](asset/39.png)
- next step
  
    ![](asset/40.png)
- next step
  
    ![](asset/41.png)
- Install add-ons yang sudah di tambahkan
  
    ![](asset/42.png)
- progress installation 
  
    ![](asset/43.png)
- result progress installation 
  
    ![](asset/44.png)

## Promote Server to a Domain Controller
---
### setting ip static melalui cmd
- open command promt (cmd)
  
    ![](asset/45.png)
- masukkan command SConfig
  
    ![](asset/46.png)
- pilih network setting
  
    ![](asset/47.png)
- pilih ip
  
    ![](asset/48.png)
- setting ip static dengan ip baru
  
    ![](asset/49.png)
- proses setting ip static berhasil
  
    ![](asset/50.png)
- open network setting
  
    ![](asset/51.png)
- ethernet lalu change adapter
  
    ![](asset/52.png)
- open properties dari ethernet
  
    ![](asset/53.png)
- input preferred dns sesuai dengan yang tadi tertera di cmd 
  
    ![](asset/54.png)
- open server manager  lihat notifikasi dan klik Promote Server to a Domain Controller
  
    ![](asset/55.png)
- create new forest dan masukkan nama domain yang kita inginkan
  
    ![](asset/56.png)
- pilih functional windows server 2016 dan juga checklist dns dan gc kemudian input password sesuai keinginan
  
    ![](asset/57.png)
- skip, next step
  
    ![](asset/58.png)
- input nama netbiosnya
  
    ![](asset/59.png)
- skip, next step
  
    ![](asset/60.png)
- check kembali apa sudah benar sesuai dengan apa yang diinginkan
  
    ![](asset/61.png)
- ketika All prerequisite checks passed successfully muncul lalu install
  
    ![](asset/62.png)
- installation progress
  
    ![](asset/63.png)
- login dengan password yang tadi dibuat
  
    ![](asset/64.png)
- check dengan "netdom query fsmo" saya berhasil melakukan Promote Server to a Domain Controller
  
    ![](asset/65.png)

terima kasih, sekian dari laporan yang di buat oleh
## Galih Dimas Prastowo  (1202190018)