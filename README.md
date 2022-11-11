# Exorde-labs
<b>A first "beta" Linux version of the participation module is available</b>
- Source https://github.com/exorde-labs/ExordeModuleCLI/tree/main
# Setup VPS
<table border="1px">
  <tr>
    <th>Komponen</th>
    <th>OS</th>
  </tr>
  <tr>
    <td>Spesifikasi</td>
    <td>Ubuntu 20.04 atau lebih tinggi.</td>
  </tr>
</table>

# Tutorial Exorde Labs 👇🏽
## 1. Bahan/Tools yang diperlukan
    sudo apt update -y && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt install docker-ce && sudo apt install -y build-essential libssl-dev libffi-dev git curl screen    
<b>Download folder Exorde</b>

    git clone https://github.com/exorde-labs/ExordeModuleCLI.git
    
## 2. Setup & Menajalankan Node
### 2.1 Masuk ke folder Exorde Labs
Untuk menjalankan node kita harus masuk ke foldernya terlebih dahulu.

    cd ExordeModuleCLI
    docker build -t exorde-cli . 
Tunggu sampe Docker selesai ngebuild Exorde CLI-nya.
### 2.2 Jalankan Screen & Node
    screen -S exorde      
###
    docker run -it exorde-cli -m Address0x -l 2   
Note!
Ganti Address0x dengan Address kalian. <b>CONTOH :</b>


    docker run -it exorde-cli -m 0xfB4280EB536b05c0AsEdEAFA8dc7C1CC69EBf2Db -l 2
<b><i>Tunggu sampai selesai dan Exorde sudah berjalan. Kalian juga bisa menutup screen dengan cara</i></b>


    Control + A dan D
    
 Hasil jika kalian sukses menjalankan Exorde Labs
<img width="793" alt="Screenshot 2022-11-09 at 3 51 21 PM" src="https://user-images.githubusercontent.com/82705116/200785526-146e22d5-95e2-40ad-86b9-65fc0a4943e3.png">

<b>UPDATE!!</b>
Jika kalian sudah memakai tutor diatas, silahkan update exorde kalian!!


    docker rm Exorde
    docker run -d -it --name Exorde exorde-cli -m $WALLET_ADDRESS -l 4
    docker logs -f Exorde

## Bantuan
Untuk melihat kembali screen Exorde kita bisa menggunakan <b>Command</b> dibawah ini.


    screen -Rd exorde
