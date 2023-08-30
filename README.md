# New York TLC Trip Record Analysis

## Background
Dalam era transportasi yang terus berkembang, peningkatan mobilitas penduduk kota dan permintaan layanan transportasi yang lebih efisien telah mendorong pertumbuhan industri transportasi berbasis aplikasi. Salah satu layanan yang populer di New-York adalah TLC atau Taxi and Limousine Commission, yang telah mengalami pertumbuhan pesat dalam beberapa tahun terakhir..

## Dataset
Dataset yang digunakan bersumber dari TLC Trip New York Januari 2023.

## Problem Statement
Industri TLC ini memiliki tantangan penting dalam mengoptimalkan penggunaan armada taksi mereka. Dalam konteks ini, penggunaan optimal merujuk pada pengaturan yang cerdas dan efisien dari armada taksi, dengan tujuan mengurangi waktu tunggu pelanggan, meningkatkan efisiensi operasional, dan pada akhirnya, meningkatkan pengalaman pelanggan. Hal yang bisa dipertimbangkan :

- Waktu padat transaksi
- Hari padat transaksi
- Lokasi penjemputan dan pengantaran transaksi
- Waktu dan jarak tempuh transaksi
- Kemacetan lalu lintas
- Mobilisasi Armada
- Metode Pembayaran

## Data Understanding
Untuk kasus ini, kita menggunakan dataset NYC TLC Trip Record tahun 2023. Berikut adalah penjelasan untuk tiap kolom databasenya

- VendorID: Kode yang menunjukkan penyedia LPEP yang menyediakan rekaman. 
  - 1 = Creative Mobile Technologies, LLC. 
  - 2 = VeriFone Inc.
- lpep_pickup_datetime: Tanggal dan waktu saat meteran diaktifkan.
- lpep_dropoff_datetime: Tanggal dan waktu saat meteran dinon-aktifkan.
- Store_and_fwd_flag: catatan perjalanan disimpan di memori kendaraan sebelum dikirim ke vendor, aka “store and forward,” karena kendaraan tidak memiliki koneksi ke server. 
  - Y = store and forward trip 
  - N = not a store and forward trip
- RateCodeID: Kode tarif akhir yang berlaku pada akhir perjalanan.. 
  - 1 = Standard rate 
  - 2 =JFK 
  - 3 =Newark 
  - 4 =Nassau or Westchester 
  - 5 =Negotiated fare 
  - 6 =Group ride
- Passenger_count: Jumlah penumpang.
- Trip_distance: Jarak dalam mil.
- PULocationID: Zona saat meteran diaktifkan.
- DOLocationID: Zona saat meteran dinon-aktifkan.
- Payment_type: Kode numerik yang menandakan pembayaran yang dilakukan oleh penumpang. 
  - 1 = Credit card 
  - 2 = Cash 
  - 3 = No charge 
  - 4 = Dispute 
  - 5 = Unknown 
  - 6 = Voided trip
- Fare_amount: Tarif waktu dan jarak dihitung dengan meteran. Ekstra Lain-lain Ekstra dan biaya tambahan. Saat ini, ini hanya mencakup
  jam sibuk dan biaya malam
- MTA_tax: Pajak MTA sebesar $0,50 secara otomatis berdasarkan tarif meteran yang digunakan.
- Improvement_surcharge: Biaya tambahan perbaikan sebesar $0,30
- Tip_amount: Tip yang diberikan penumpang untuk pembayaran credit card
- Tolls_amount: Total biaya tol jika melewati tol.
- Total_amount: Total biaya yang dibayarkan oleh penumpang.
- Trip_type: Kode yang menandakan penumpang memesan melalui aplikasi atau mencari taxi secara acak di jalan. 
  - 1 = Street-hail 
  - 2 = Dispatch
- eHail fee adalah biaya atau tambahan biaya yang dikenakan kepada pengguna layanan taksi atau transportasi berbasis aplikasi ketika mereka memesan taksi melalui platform elektronik atau aplikasi.
- Congestion surcharge adalah biaya tambahan yang dikenakan kepada pengguna layanan transportasi, seperti taksi atau layanan berbasis aplikasi, ketika mereka menggunakan layanan tersebut dalam kondisi lalu lintas yang padat atau di daerah-daerah dengan kemacetan tinggi.