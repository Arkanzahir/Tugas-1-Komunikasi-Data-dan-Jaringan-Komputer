## Tugas 1 Jarkom - Subnetting & Routing
Nama: Mohamad Arkan Zahir Asyafiq
NRP: 50272411201. 

1. Perhitungan Base Network
   NRP: 5027241120

   Perhitungan: 5027241120 mod 256 = 160

   Base Network: 10.160.0.02. 

   Total Host yang Dibutuhkan:768 host (Termasuk 6 LAN dan 2 WAN link)

<img width="712" height="516" alt="Screenshot 2025-11-11 193059" src="https://github.com/user-attachments/assets/74a7c226-7444-4dc5-912b-08636991e847" />

2. Topologi JaringanTopologi ini dirancang dengan 5 LAN di Kantor Pusat (menggunakan VLAN) dan 1 LAN di Kantor Cabang, sesuai dengan requirement soal.

  <img width="1913" height="758" alt="Screenshot 2025-11-10 223420" src="https://github.com/user-attachments/assets/82981e39-f17e-4657-b248-ca7d0c42d891" />

3. Tabel Hasil VLSM
Perhitungan alokasi IP untuk 6 Jaringan LAN (5 di Pusat, 1 di Cabang) dan 2 Jaringan WAN berdasarkan kebutuhan host dari soal.

<img width="1191" height="258" alt="Screenshot 2025-11-11 134830" src="https://github.com/user-attachments/assets/aee5195f-4b90-4702-aa9a-a358d6f51c78" />

4. Tabel Hasil CIDR & Visualisasi Supernetting
   a. Tabel Hasil CIDR (Tabel Routing)
      <img width="1197" height="104" alt="Screenshot 2025-11-11 134936" src="https://github.com/user-attachments/assets/b575a86f-4741-4eee-9505-3b354fa497bb" />

   b. Tabel Visualisasi Supernetting
   <img width="849" height="289" alt="Screenshot 2025-11-11 135036" src="https://github.com/user-attachments/assets/1ec3a1aa-743f-4a47-9515-269179f8f85e" />

5. Hasil Pengujian Konektivitas
   Bukti pengujian konektivitas untuk membuktikan Inter-VLAN routing dan WAN routing berfungsi penuh.
   
   Tes 1: Dari Kantor Pusat ke Kantor Cabang
   Tes ini dilakukan dari PC-SEKRETARIAT-1 (VLAN 10) ke PC-PENGAWAS-CABANG-1 (Cabang).
   <img width="513" height="216" alt="Screenshot 2025-11-10 230329" src="https://github.com/user-attachments/assets/cce58952-a062-47e0-b67b-d1859e2e8706" />

   Tracert (Pusat ke Cabang)
   Tes ini membuktikan rute paket data telah sesuai dengan desain, yaitu melewati 3 router: R-PUSAT -> R-UTAMA -> R-CABANG.
   
   <img width="621" height="199" alt="Screenshot 2025-11-10 230336" src="https://github.com/user-attachments/assets/e82be22f-11f2-45f9-9c0f-72b9fe00aa00" />

   Tes 2: Dari Kantor Cabang ke Kantor Pusat
   
   Tes ini dilakukan dari PC-PENGAWAS-CABANG-1 (Cabang) untuk membuktikan rute baliknya.

   Ping (Cabang ke Pusat - Sekretariat)

   Tes ini membuktikan PC Cabang bisa mencapai VLAN 10 (Sekretariat) di Pusat.
   
   <img width="508" height="228" alt="Screenshot 2025-11-11 135806" src="https://github.com/user-attachments/assets/fa32bd68-bb71-4ccc-afea-a753fd1df484" />

   Ping (Cabang ke Pusat - Server)
   
   Tes ini membuktikan PC Cabang bisa mencapai VLAN 60 (Server) di Pusat.

   <img width="562" height="225" alt="Screenshot 2025-11-11 135844" src="https://github.com/user-attachments/assets/196b2c4f-1eab-4979-9cab-446d2a532f4a" />

   


