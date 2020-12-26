# Docker Spark Cluster
Ini adalah hasil modifikasi dari [repo punya gettyimages](https://github.com/gettyimages/docker-spark).

## Langkah Penggunaan
1. Fork/Clone repo ke komputer yang ingin digunakan
2. Masuk ke direktori
3. Masukkan perintah `docker build -t rizkiv1/spark:latest .` untuk membuat images baru dengan nama rizkiv1/spark.
4. Masukkan perintah `docker-compose up -d` untuk menjalankan container. Agar memiliki 2 worker container tambahkan parameter `--scale worker=n` dengan `n` adalah jumlah worker yang ingin dijalankan.
5. Untuk mengakses web UI dari master, buka `http://${Alamat_Host}:8080`. Disini kita dapat melihat worker yang jalan.


## Menjalankan Contoh Program
1. jalankan perintah `docker exec -it docker-spark_master_1 /bin/bash bin/run-example SparkPi 10` untuk menjalankan program contoh SparkPi.
