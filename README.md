# Aplikasi Web "Polr"
<h1 align="center"><img src="https://camo.githubusercontent.com/5e2eb23b0fb9b832458552e0f0a74a137208a9bce0942aa752a58e9e861a5864/68747470733a2f2f692e696d6775722e636f6d2f636b49364754752e706e67"> </h1>

## Sekilas Tentang Polr (Bani)

Aplikasi ini merupakan peringkas ataupun penyingkat sebuah tautan yang cepat, dan memberikan pengguna kemudahan untuk mengubah tautan panjang menjadi lebih pendek dan memudahkan user untuk mencantumkan brand sehingga tautan tersebut lebih mudah diingat dan diakses. Aplikasi ini sangat mudah digunakan dengan tampilan yan gminimalis dan modern, sehingga tidak perlu banyak waktu bagi pengguna untuk bisa mempelajari ataupun menggunakan aplikasi ini.


## Instalasi (amin Mufti)

#### Prasyarat, apa saja yang harus diinstal sebelumnya
  - Apache <br>
    `sudo apt install apache2`
  - PHP >= 5.5.9 <br>
    `sudo apt install php`
  - MariaDB or MySQL >= 5.5, SQLite alternatively <br>
    `sudo apt install php-mysql`
  - composer <br>
    `sudo apt install composer`
  - PHP requirements:
    - OpenSSL PHP Extension <br>
      `sudo apt install php-openssl`
    - PDO PHP Extension <br>
      `sudo apt install php-pdo`
    - PDO MySQL Driver (php5-mysql on Debian & Ubuntu, php5x-pdo_mysql on FreeBSD) <br>
      `sudo apt install php5-mysql`
    - Mbstring PHP Extension <br>
      `sudo apt install php-mbstring`
    - Tokenizer PHP Extension <br>
      `sudo apt install php-tokenizer`
    - JSON PHP Extension <br>
      `sudo apt install php-json`
    - PHP curl extension <br>
      `sudo apt isntall php-curl`

#### Langkah instalasi dalam CLI (Ubuntu). 
##### 1. Download File Instalasi
- Buka aplikasi terminal dan gunakan *superuser* <br>
  `sudo su` kemudian ketikan password (jika menggunakan password)
- Berpindah ke directory `/var/www`, jika folder tidak ada, ketikan perintah `mkdir /var/www` <br>
  `cd /var/www`
- Clone (download) aplikasi Polr dengan menggunakan **git** <br>
  `git clone https://github.com/cydrobolt/polr.git --depth=1`
- Set *permission* dari directory **polr** yang telah diclone
  `chmod -R 755 polr`
  
##### 2. Menginstall `composer` dependencies
- Masuk ke dalam directory `polr` <br>
  `cd /polr`
- Mendownload `composer` package <br>
  `curl -sS https://getcomposer.org/installer | php`
- Install dependencies ke aplikasi **polr** <br>
  `php composer.phar install --no-dev -o`
  <br>
  Jika **composer** gagal untuk menginstall dependencies dikarenakan versi **PHP** yang berbeda,<br>
  hapus file `composer.lock`, dan install **composer** kembali <br>
  `rm composer.lock` <br>
  `php composer.phar install --no-dev -o`

##### 3. Menjalankan Polr
Untuk menjalankan **Polr** di Apache, harus membuat file konfigurasi apache baru di folder dalam sistem operasi konfigurasi Apache (contoh `/etc/apache2/sites-enabled` atau `/etc/httpd/sites-enabled`) atau tambahkan virtual host dalam file `httpd-vhosts.conf` seperti:

Ganti `example.com` dengan alamat server eksternal dan restart Apache ketika selesai.

---
**NOTE**

It works with almost all markdown flavours (the below blank line matters).

---



## Cara Pemakaian (Mufti amin)
#### Tampilan Aplikasi Web
![1](https://user-images.githubusercontent.com/48195354/111268258-9f721100-865f-11eb-9e79-d09a03f3d33f.jpeg)
![2](https://user-images.githubusercontent.com/48195354/111268282-a731b580-865f-11eb-8857-8f8fbe4e5d45.jpeg)
![3](https://user-images.githubusercontent.com/48195354/111268287-a9940f80-865f-11eb-995b-12be3d671281.jpeg)
![4](https://user-images.githubusercontent.com/48195354/111268291-aac53c80-865f-11eb-9de9-e47b1b341045.jpeg)
![5](https://user-images.githubusercontent.com/48195354/111268295-abf66980-865f-11eb-9def-179c25e34216.jpeg)
![6](https://user-images.githubusercontent.com/48195354/111268298-ac8f0000-865f-11eb-9f0c-28a897391d99.jpeg)
#### Fungsi-fungsi utama
![7](https://user-images.githubusercontent.com/48195354/111268299-adc02d00-865f-11eb-831c-001a714a5d38.jpeg)
![WhatsApp Image 2021-03-15 at 10 03 47 PM](https://user-images.githubusercontent.com/48195354/111268300-adc02d00-865f-11eb-9c44-c1a51b677893.jpeg)
#### Isi dengan data real/dummy (jangan kosongan) dan sertakan beberapa screenshot


## Pembahasan (Abdan)

**Polr** --  Modern, minimalist, modular, and lightweight URL shortener.-- ditulis menggunakan bahasa ditulis dalam bahasa pemrograman PHP yang support untuk penggunaan MySQL. Sebagai salah satu CMS yang paling banyak digunakan di dunia, aplikasi ini menawarkan berbagai kelebihan, diantaranya :
- Open source
- Tampilan antarmuka yang Modern dan simple interface untuk memanage link dan instansinya
- _Intrepid_, dalam artian lain, mudah digunakan
- Run on your own domain to adjust your branding to perfection
- Menggunakan Semantic REST API, sehingga dapat diintegrasikan dengan layanan yang lain _(Other services)_
- Proses [Instalasi](https://docs.polrproject.org/en/latest/user-guide/installation/) yang cukup mudah untuk developer
- Dapat digunakan sebagai [extensi browser](https://github.com/cleverdevil/Polr.safariextension) pada safari.
 
Tentu saja, sebuah aplikasi pasti memiliki kekurangan. Kekurangan yang dimiliki **Polr** antara lain :
- Penggunaan **Polr** harus membutuhkan instalasi via web app, tentu hal tersebut tidak sesimple menggunakan url shortener sejenis 
- Dalam beberapa kasus, seringkali ditemukan bug yang terjadi saat menggunakan polr
- Penyingkatan link _(URS Shortener)_ pada **Polr** tidak _customizable_

Jika dibandingkan dengan aplikasi sejenis, seperti [bit.ly](https://app.bitly.com/), kami dapat memberikan gambaran sebagai berikut
- `Polr` Gratis, `bit,ly` juga gratis, namun untuk beberapa fitur bit.ly memerlukan biaya berlangganan.
- `Polr` open source dan self hosted, `bit.ly` melakukan _hosting_ dari web host nya.
- `Polr` memiliki opsi untuk dijadikan extensi di salah satu browser, `bit.ly` tidak.
    
    
## Referensi

1. [About Polr](https://polrproject.org) - Polr
2. [How to install Polr](https://docs.polrproject.org/en/latest/user-guide/installation/) - PolrProject
3. [Extension for Safari](https://github.com/cleverdevil/Polr.safariextension) - Github
