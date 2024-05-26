# Capstone_Project_Module_3_Yunella
Bank Marketing Campaign Model Prediction

**Context Business**

Jenis produk keuangan dalam masyarakat semakin bervariasi. Salah satu produk keuangan adalah Deposito Berjangka. Mekanisme Deposito Berjangka adalah nasabah menyetorkan sejumlah uangnya ke bank atau lembaga keuangan, dan uang tersebut baru boleh ditarik setelah jangka waktu tertentu. Sebagai imbalannya, nasabah akan diberikan bunga tetap sesuai dengan jumlah nominal uang yang disetorkan.
Meski demikian, bank tetap harus bersaing agar tidak kehilangan nasabah. Salah satu cara untuk mendapatkan pelanggan baru adalah dengan melakukan marketing campaign.

**Problem Statements**

Proses marketing/pemasaran pastinya mengeluarkan biaya yang banyak untuk menghubungi calon nasabah satu per satu dalam rangka memberikan informasi terkait adanya produk Deposito Berjangka. Apalagi jika harus semua nasabah yang dihubungi, pastinya ini akan memakan banyak biaya, waktu, dan energi, berhubung media pemasaran yang digunakan adalah media telepon satu per satu.

Agar biaya yang dikeluarkan perusahakaan lebih optimal dan bertujuan dapat semuanya terkonversi menjadi nasabah baru, perusahaan meminta bantuan Data Scientist untuk memprediksi calon nasabah baru yang memang benar-benar tertarik untuk membuka Deposito Berjangka dan yang tidak tertarik. 
Dengan adanya hasil prediksi dari Data Scientist, harapannya perusahaan dapat menekan biaya marketing untuk nasabah yang memang diprediksi sebagai potential nasabah.

**Goal**

Dari permasalahan tersebut, perusahaan dapat mengetahui yang mana saja merupakan calon nasabah yang diprediksi akan membuka Deposito Berjangka sehingga perusahaan dapat fokus memasarkan informasi terbaru, campaign atau semua hal terkait marketing Deposito Berjangka hanya ke nasabah yang diprediksi tertarik saja.

**Kesimpulan**

1. Pada model benchmarking kita menggunakan **f1 score sebagai metrix evaluation** untuk pemilihan model. 
Kerugian perusahaan dari False Negatif (saat nasabah tertarik Deposito Berjangka namun kita prediksi tidak tertarik) adalah perusahaan akan kehilangan potential nasabah dan nasabah tersebut akhirnya membuka Deposito Berjangka di bank lain (competitor).

Kerugian perusahaan dari False Positif (saat nasabah tidak tertarik Deposito Berjangka namun kita prediksi tertarik) adalah perusahaan mengalami kerugian biaya marketing yang tidak tepat sasaran, menghabiskan banyak waktu untuk menghubungi calon nasabah namun tidak terkonversikan dengan pembukaan Deposito Berjangka.

Oleh karena ini, kita memakai f1 score sebagai rataan harmonik dari recall dan presisi untuk memilih model algoritma.

3. Model **Gradient Boosting Classifier (GBC)** memiliki nilai tertinggi dalam benchmarking. Model GBC adalah hasil modifikasi dari metode boosting pada umumnya.

4. Hasil prediksi model kita berhasil mendapatkan 64% nasabah yang benar-benar tertarik dari keseluruhan nasabah yang tertarik membuka Deposito Berjangka, serta berhasil menghemat biaya marketing dengan mengurangi 82% nasabah yang tidak tertarik untuk tidak perlu kita tawarkan produk Deposito Berjangka.

5. Model kita memiliki ketepatan prediksi senilai 77% yang artinya apabila model memprediksi nasabah tertarik maka kemungkinan prediksi tersebut benar adalah 77% (dari nilai presisi). 

6. Biaya marketing yang sia-sia adalah biaya yang diberikan kepada 18% nasabah yang diprediksi tertarik namun ternyata tidak tertarik (dari nilai recall kelas 0).

7. Dari hasil feature importance diketahui 5 fitur paling penting adalah : pdays, contact, month, balance, age.

8. Rata-rata nasabah yang tertarik membuka Deposito Berjangka memiliki kriteria sebagai berikut:
   berusia : rata-rata 42 tahun
   
   memiliki saldo rekening : rata-rata 1812 USD
   
   dikontak sebanyak : rata-rata 2 kali selama marketing berlangsung
   
   dihubungi marketing : rata-rata 69 hari yang lalu
   
   bekerja : bagian Management
   
   rumah : tidak memiliki rumah
   
   loan : tidak memiliki pinjaman
   
   contact : melalui celluar
   
   hasil marketing sebelumnya : tidak diketahui (berarti nasabah yang belum berhasil atau gagal di masa marketing sebelumnya memiliki kemungkinan tertarik yang besar pada masa marketing sekarang ini)


9. Biaya marketing $4000 untuk menarik 200 nasabah baru ($20/orang) tanpa menggunakan model, menjadisejumlah $1640 untuk menarik 128 nasabah baru ($12.8/orang) dengan bantuan model. Hal ini akan menekan biaya marketing sebesar 36%.
