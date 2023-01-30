<h1>PENDAHULUAN</h1>

SIBI (Sistem Isyarat Bahasa Indonesia) merupakan salah satu metode alternatif dalam menjalin komunikasi untuk penyandang tunarungu dan tunawicara kepada masyarakat normal. SIBI memanfaatkan gerakan tangan, wajah, tubuh yang menyerupai beberapa simbol yang memiliki suatu arti. Penggunaan SIBI diadaptasi dari ASL (American Sign Language) dan merupakan sistem bahasa yang direkomendasikan oleh pemerintah. Penelitian ini mengembangkan sistem untuk pengenalan Bahasa Isyarat SIBI menggunakan metode deteksi objek dengan menerapkan algoritma Convolutional Neural Network (CNN) untuk pemrosesan gambar. Peneliti menerapkan algoritma Convolutional Neural Network (CNN) dalam memproses gambar karena telah teruji sebagai salah satu algoritma yang sangat baik. Selanjutnya, total perolehan keseluruhan data adalah sebanyak 37 kelas, dan setiap kelas memiliki 1500 buah citra. Penelitian ini dimulai dari tahap akuisisi data, preprocessing, modeling, dan pengujian. Selanjutnya, peneliti melakukan implementasi sistem dengan menentukan beberapa variabel teknis dan library yang digunakan guna memperoleh hasil akurasi yang tinggi. Setelah tahapan tahapan di atas telah dilaksanakan, maka peneliti melakukan pengujian terhadap 3 model dalam hal mendeteksi objek Bahasa Isyarat SIBI. Hasil akurasi yang diperoleh dari pengujian 3 model tersebut adalah sebesar 100%

<h1>MODELLING</h1>

<h2>Parameter Training</h2>

![image](https://user-images.githubusercontent.com/108866174/215393156-7b66fb11-b69d-4232-b7e0-73ee929ab584.png)


<h2>Modelling Plot</h2>

![image](https://user-images.githubusercontent.com/108866174/215393430-ec1ac23c-6c7e-4283-a223-f8ccd6eadda0.png)

<h2>Hasil Training Model</h2>

![image](https://user-images.githubusercontent.com/108866174/215407831-b104b663-b405-4049-8965-ff3895d9427c.png)

Jika dilihat dari tabel diatas bahwasanya model no. 3 dengan menggunakan parameter Convolutional Layer sebanyak 5 yaitu (32,64,128,256,512), dengan penggunaan hidden layer sebanyak 2 yaitu (128,256) menghasilkan nilai akurasi yang sempurna yaitu 100% dan nilai loss terkecil diantara 3 model. Dapat dikatakan penggunaan parameter atau besarnya layer yang digunakan mempengaruhi model dengan penambahan hidden layer dan juga memperbesar jumlah neuron pada convolutional layer membuat model semakin baik dalam proses pelatihan. Selanjutnya pengujian semua model yang telah dibangun menggunakan data testing, pada Tabel IV merupakan hasil testing model.

<h2>Hasil Testing</h2>

![image](https://user-images.githubusercontent.com/108866174/215408419-4531af48-fff3-46f9-84f1-e464101ca9fe.png)

Dari tabel diatas hasil nilai tes akurasi dan loss nya, dimana ke 3 model mendapatkan akurasi 100% yang berarti model dapat memprediksi dengan benar dan akurat setiap Model 1 2 3 Convolutional Layer 5 (32,64,64,32,6 4) 5 (64,128,128,64 ,128) 5 (32,64,128,256 ,512) Hidden Layer 1 (128) 1 (128) 2 (128,256) Activation LayerInput ReLu ReLu ReLu Activation Layer Output Softmax Softmax Softmax Matrix Kernel (3 x 3) (3 x 3) (3 x 3) Stride Size (1 x 1) (1 x 1) (1 x 1) Max Pooling Layer 5 (2,2) 5 (2,2) 5 (2,2) kelas dari data test. Pada pengujian model no 3 adalah model yang mendapatkan nilai loss terkecil dan ketiga model yang sudah dibangun dapat dikatakan good fit karena mendapat akurasi mencapai 100%. Model no. 3 adalah model yang terbaik dan yang akan digunakan dalam tahap prototyping.

<h1>Prototyping</h1>

Proses prototyping dilakukan menggunakan webcam pada laptop atau komputer dengan menggunakan library TensorFlow dan Opencv. Pengenalan sign-language dilakukan secara realtime dengan mendeteksi gambar atau gesture tangan menggunakan video captured didalam Region of Interest (ROI), selanjutnya model akan mengenali objek yang berada di dalam ROI tersebut dan memprediksi objek atau melakukan labeling terhadap objek tersebut, dengan menggunakan model yang sudah dibangun pada proses sebelumnya.

![image](https://user-images.githubusercontent.com/108866174/215409058-41f02495-7959-4a0a-91a1-cafee1739a70.png)

![image](https://user-images.githubusercontent.com/108866174/215409410-24e7cad0-2e22-4333-a4fb-2ed82ed8dae5.png)

![image](https://user-images.githubusercontent.com/108866174/215409558-0dca9635-ad58-4ef8-b637-46ed699d38ae.png)

![image](https://user-images.githubusercontent.com/108866174/215409661-54998c11-d1e6-484e-af8a-8ed00284a3e5.png)

![image](https://user-images.githubusercontent.com/108866174/215409746-b73f9724-ab6d-4e7c-b5ff-e1a24d95a56b.png)

![image](https://user-images.githubusercontent.com/108866174/215409916-5f0e95cd-6b0f-429d-b342-1b4a79a5e183.png)

![image](https://user-images.githubusercontent.com/108866174/215410030-fbf92de7-47cb-48eb-8eac-989438c65381.png)

Dari hasil pengujian terhadap semua alphabet, dapat dikatakan model yang dibangun sudah sangat baik karena sudah dapat mengenali objek dengan baik dan benar dari akurasi test prototype secara langsung.

<h1>Kesimpulan</h1>

Berdasarkan penelitian yang telah dilakukan terhadap topik pengenalan Bahasa Isyarat SIBI Alphabet dapat diperoleh beberapa kesimpulan, yaitu ketika menentukan kombinasi dari hyperparameter arsitektur CNN, maka perlu melakukan trial dan error dengan berbagai uji coba kombinasi parameter karena banyak sekali kombinasi yang dapat dilakukan. Dalam penelitian ini kombinasi yang dilakukan yaitu hidden layer, convolutional layer, dan sudah mendapatkan akurasi yang baik dari 3 model yang dimiliki. Dari 3 model percobaan didapatkan 1 model terbaik yaitu ketika menggunakan convolutional layer sebanyak 5 yaitu (32,64,128,256,512), hidden layer sebanyak 2 yaitu (128,256), serta menggunakan Max Pooling 2 Dimensi sebagai pooling layer. Menggunakan fungsi aktivasi untuk layer input yaitu ReLU, fungsi aktivasi pada output layer yaitu Softmax dengan jumlah 37 neuron, dengan epochs sebanyak 25 untuk pelatihan, model di compile dengan optimizer Adam dengan learning rate default dari Keras yaitu 0.001 sebagai konfigurasi parameter terbaik yang digunakan untuk penelitian ini. Kemampuan model yang dihasilkan cukup kuat untuk dataset yang digunakan dalam penelitian ini. Mengenai performa dari 3 model yang dimiliki, semuanya mendapat akurasi sempurna yaitu 100% dan untuk pengujian model terbaik dalam proses prototyping untuk mendeteksi alphabet dari A – Z menggunakan gesture tangan secara realtime mendapatkan nilai rata-rata akurasi yaitu 96.57%. Jika dibandingkan dengan penelitian sebelumnya, hasil yang didapat pada penelitian ini lebih akurat dari penelitian oleh Sherryl Sugiono Sindarto et.al, yang mendapatkan akurasi 88%, selanjutnya penelitian dari Yolanda.D et.al, mendapat akurasi 60.58%, dan penelitian dari Sholawati, M et.al, mendapat akurasi 80.76%. Tim penyusun menyadari bahwa terdapat kekurangan dan kesalahan pada penelitian ini, baik dari segi penulisan atau perancangan. Oleh karena itu, kritik dan saran yang membangun dari para pembaca akan sangat berharga bagi tim penyusun untuk memperbaiki laporan selanjutnya. Pada penelitian terkait selanjutnya, data yang digunakan lebih bervariasi guna menghindari terjadinya overfitting dan menerapkan metode object tracking.





