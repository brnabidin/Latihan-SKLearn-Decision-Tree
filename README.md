# Latihan-SKLearn-Decision-Tree

**Tahapan Latihan**

Dataset iris terdiri dari 4 atribut yaitu panjang sepal, lebar sepal, panjang petal, dan lebar petal. Terdapat 3 kelas target pada dataset ini. Data ini digunakan untuk masalah klasifikasi, di mana kita memprediksi jenis spesies sebuah bunga berdasarkan atribut-atribut yang diberikan.

Tahapan yang ada pada latihan ini antara lain:

- Ubah dataset ke dalam dataframe.

- Hapus kolom 'Id' pada dataframe serta pisahkan antara atribut dan label. 

- Bagi dataset menjadi data latih dan data uji.

- Buat dan latih model Decision Tree.

- Lakukan pengujian model dengan menggunakan data uji. 

- Lakukan prediksi dengan model yang telah dilatih.

- Visualisasi model Decision Tree yang telah dilatih.

**Codelab**

Pertama kita akan mengimpor library yang dibutuhkan dan mempersiapkan dataset. Dataset dapat anda unduh di tautan https://www.kaggle.com/uciml/iris berikut. Setelah data diunduh, masukkan berkas Iris.csv ke dalam Google Colab. Lalu jangan lupa konversi dataset menjadi Pandas dataframe.

![1](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/1ed92f55-97a9-4d9b-a667-3afec77009d2)

Untuk melihat informasi mengenai data, gunakan fungsi info(). Selain itu, Anda juga bisa melihat lima data teratas pada dataset menggunakan fungsi head(). 

![2](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/7f3cf519-5523-4eed-86cd-abcb96d93a96)

![dos_4ca58d1a98ad8f0348b2c83a85dcc43120211126141211](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/f2cf13d6-8925-4c1f-8123-b6a8352bd19b)

Dari output di atas, kita dapat mengidentifikasi kolom yang tidak penting pada dataset yaitu kolom "Id". Untuk menghilangkan kolom tersebut, gunakan fungsi drop().

![3](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/a226316a-5e65-4464-8154-76af0f107994)

Sebelum melatih model kita perlu memisahkan atribut dengan label. Selain itu, kita juga perlu membagi dataset menjadi data latih dan data uji. Jalankan kode berikut untuk menerapkan tahapan di atas.

![4](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/96a9d88a-bb66-4ebd-b872-fe098976c360)

Selanjutnya, definisikan model decision tree yang akan kita gunakan. Kemudian,  latih model menggunakan data latih menggunakan fungsi fit().

![5](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/6fe40463-8324-49b0-9f51-1b9ccc8ffb87)

Setelah model dilatih, uji model menggunakan data uji untuk melihat seberapa baik model yang telah kita buat. Pengujian model ini bisa dilakukan dengan menggunakan fungsi predict(). 

Berikutnya, gunakan metrik akurasi untuk melihat seberapa baik model yang telah kita latih. Penjelasan terkait metrik akurasi ini akan dibahas pada modul selanjutnya.

![6](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/348470a4-21b2-42d6-a2a5-30771a37738a)

![dos_3b619564fdc0353bdcbd7b0f95dc889f20211126141845](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/4338c6f0-5050-45ae-be30-9de41a8658f4)

Nah, kita bisa mencoba model yang telah kita buat untuk memprediksi spesies dari sebuah bunga Iris. Masih ingat bukan, atribut yang menjadi masukan dari model adalah panjang sepal, lebar sepal, panjang petal, dan lebar petal? Kita akan memasukkan nilai yang sesuai dengan format tersebut secara berurutan dalam satuan centimeter. Pada contoh berikut, kita ingin memprediksi spesies dari sebuah bunga iris  yang memiliki panjang sepal 6,2 centimeter, lebar sepal 3,4 centimeter, panjang petal 5,4 centimeter, dan lebar petal 2,3 centimeter.

![7](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/6699168e-6552-4bbe-acbe-3f2fc78cbd26)

![dos_28d001bfed0394b10d341d2368b4515c20211126142114](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/25ec623b-3375-4066-a03e-96d19ed94fa5)

Selain melakukan prediksi, kita juga bisa melihat visualisasi dari decision tree yang kita buat terhadap data menggunakan library Graphviz. Hasil dari graphviz adalah dot file yang akan muncul pada folder file di panel sebelah kiri Google Colab (jika Anda menggunakan Google Colab).

![8](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/0dfa879c-4f75-4a32-98ea-60d2f7b856fd)

Setelah kode di atas berhasil dijalankan, Anda akan mendapatkan output berupa berkas iris_tree.dot, sebagai berikut:

![dos_e9b911bee3d5626b117170348e180db720211126142239](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/1926479f-72b0-487e-842d-a8ce2bffca50)

Untuk mengunduh berkas iris_tree.dot pada gambar di atas, kita dapat melakukan klik kanan pada berkas tersebut kemudian mengunduhnya.

Jika kita ingin melihat visualisasi decision tree, lakukan konversi dot file ke dalam file png menggunakan situs konversi berkas berikut ini : https://onlineconvertfree.com/converter/images/.

Catatan : Jangan lupa ganti opsi ke images sebelum menekan tombol convert

Berikut merupakan hasil visualisasi dari model decision tree yang telah kita gunakan:

![dos_9cbc824c85fd2e6f398131863e4d474720211126142343](https://github.com/brnabidin/Latihan-SKLearn-Decision-Tree/assets/67081096/c38d333e-32bb-41d2-b704-535e30449454)

Selamat! Anda telah berhasil membuat sebuah model decision tree untuk klasifikasi spesies bunga Iris. Anda juga telah berhasil menguji model anda untuk memprediksi spesies dari sebuah bunga iris. Untuk belajar lebih mendalam tentang decision tree, kunjungi tautan berikut 
https://towardsdatascience.com/decision-trees-in-machine-learning-641b9c4e8052 yah.
