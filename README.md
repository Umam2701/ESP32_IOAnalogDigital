# DASAR PEMROGRAMAN ESP32 UNTUK PEMROSESAN DATA INPUT/OUTPUT ANALOG DAN DIGITAL

ESP-32 adalah mikrokontroler yang dikenalkan oleh Espressif System merupakan penerus dari mikrokontroler ESP8266. Pada mikrokontroler ini sudah tersedia modul WiFi dalam chip sehingga sangat mendukung untuk membuat sistem aplikasi Internet of Things. Perbedaan antara ESP32 dengan ESP8266 adalah pada bagian prosesornya. ESP32 sudah Dual-Core 32 bit, jelas lebih cepat ESP32 secara kinerja. Selain itu modul ini juga mempunyai bluetooth, satu fitur yang tidak ada di ESP8266.


**ALAT DAN BAHAN** 
1) ESP32
2) Breadboard
3) Kabel jumper
4) Potensiometer 10k Ohm (1)
5) Sensor Capacitive Soil Moisture
6) LED (5) dan Push Button (3)
7) Multimeter
8) Resistor 330,1K, 10K Ohm (@ 3)


**LANGKAH KERJA**
1)  Pertama install board ESP32 pada Arduino IDE
2)  Mengakses GPIO ESP32 <br />

    *GPIO 1* - Rangkaian dengan 1 LED dengan 1 button. Kendalikan LED tersebut dengan button yang ada.
      
     https://user-images.githubusercontent.com/118170084/209113109-dd368fd0-cdb1-4a63-995a-49d100cd21df.mp4

     Analisa : Pada langkah ini menggunakan 1 LED dan 1 Button. Ketika script GPIO 1 di run, maka output yang dihasilkan yaitu jika button di push maka LED akan menyala, dan LED akan mati jika button dilepas.
    
     *GPIO 2* - Kemudian, tambahkan 1 LED dan 1 button lagi. Untuk LED kedua ini, buat interval waktu 2 detik. Jadi walaupun button tetap ditekan, jika waktunya sudah habis, maka LED akan mati.
    
     https://user-images.githubusercontent.com/118170084/209113309-07147da6-15a6-4671-8308-92cd9acda3ed.mp4
   
     Analisa : Pada percobaan GPIO 2 ini ditambahkan 1 LED dan 1 Button lagi. Output yang dihasilkan yaitu jika button ditekan maka LED akan menyala dan mati selama waktu yang ditentukuan. LED akan mati jika button tidak ditekan.
   
     *GPIO 3* - Kemudian, tambahkan 3 LED dan 1 button. Kendalikan 3 LED ini dengan 1 button tersebut agar bisa menyala berurutan.
   
     https://user-images.githubusercontent.com/118170084/209113435-8b718fcb-63ab-4c69-a7e6-27132ddf21ac.mp4

     Analisa : Pada percobaan GPIO 3, output yang dihasilkan yaitu ketika button ditekan maka LED akan menyala running dari kiri ke kanan dengan interval masing-masing LED selama 1 sekon. Dan LED akan mati ketika button tidak ditekan.
   
   
3) Mengakses PWM ESP32 <br />
   
   *- Menyalakan 1 LED (PWM 1)*
   
   https://user-images.githubusercontent.com/118170084/209116921-7d02a986-6f15-42e3-b912-0606ee0a7f83.mp4
 
   Analisa : Pada percobaan PWM 1 mengunakan 1 LED yang akan dinyalakan dan dimatikan selama waktu yang ditentukan yaitu 0,015 detik.
   
   *- Menyalakan 3 LED (PWM 2)*
   
   https://user-images.githubusercontent.com/118170084/209117170-259f3ec4-045f-4b4f-b796-8af0594fee2f.mp4

   Analisa : Untuk percobaan PWM 2 ini sama seperti PWM 1 hanya saja menggunakan 3 LED yang akan dinyalakan dan dimatikan secara bersamaan.

4) ADC dan DAC <br />

   *- ADC DAC 1* - Buatlah rangkaian seperti ini dengan script di bawah. Kemudian putar potensiometer agar menghasilkan nilai 0 dan 4095. Lihat hasilnya.
   
   https://user-images.githubusercontent.com/118170084/209121132-85250035-d8b6-4d93-b9e4-6b35ca038c5a.mp4


   Analisa : Output pada percobaan ADC/DAC 1 yaitu apabila potensio diputar ke kanan maka nilainya akan bertambah sampai maksimum 4095 (3,3V), dan apabila diputar ke kiri maka nilainya akan berkurang sampai minimum 0 (0 V) dengan waktu 0,5 sekon tiap pembacaan pada serial monitor.
   
   *- ADC DAC 2* - Kemudian tambahkan LED pada rangkaian tersebut. Putar potensio dan lihat apa yang terjadi pada LED dan serial monitor.
   
   https://user-images.githubusercontent.com/118170084/209121331-cd978a52-ab92-4027-aacc-61f49f9d5dd8.mp4

   Analisa : Untuk output pada ADC/DAC 2 ini sama seperti ADC/DAC 1, hanya saja ditambahkan LED. Jadi ketika potensio diputar ke kanan (nilainya bertambah), maka LED akan menyala lebih terang dari kondisi awal. Dan ketika potensio diputar ke kiri, maka LED akan redup lalu kemudian mati jika nilainya mencapai 0.
