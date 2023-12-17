<h1> 🔰 &nbsp; RISET INFORMATIKA C081 </h1>

<h2> Analisis sentimen penilaian user pada aplikasi KAI Access menggunakan Python dengan Algoritma SVM, Naive Bayes dan Random Forest  </h2>

<h2> Daftar Isi </h2>

<ol>
    <li> <a href="#latar_belakang"> Latar Belakang </a> </li>
    <li> <a href="#metode"> Metode </a> </li>
    <li> <a href="#data"> Data Penelitian </a> </li>
    <li> <a href="#data"> Referensi </a> </li>
    <li> <a href="#data"> Dataset </a> </li>
    <li> Coding </li>
    <li> Analisis </li>
    <li> Gambar Pendukung </li>
    <li> Mengatasi Error </li>
    <li> Draft Paper Publikasi </li>
</ol>

<h3 id="latar_belakang"> Latar Belakang </h3>
<p>Saat ini, aplikasi mobile menjadi komponen penting yang mempermudah memenuhi kebutuhan pengguna. Salah satunya adalah KAI Access, aplikasi layanan pemesanan tiket kereta api yang dilakukan secara online dengan memanfaatkan Internet. Dengan adanya kemudahan tersebut tak lantas dapat memuaskan pelanggan. Sistem juga memiliki celah yang perlu diperbaiki. Melalui pemahaman sentimen pengguna, pengembang aplikasi dapat merumuskan solusi untuk meningkatkan kualitas pelayanan yang akan diberikan. 
	
<p>Ulasan merupakan pendapat atau tanggapan yang diberikan oleh pengguna terkait pengalaman mereka dalam menggunakan suatu aplikasi. Ulasan ini biasanya memberikan pujian, kritik, atau saran terhadap pengalaman pengguna terhadap aplikasi tersebut. Google Play Store, sebuah platform distribusi utama untuk aplikasi Android, memfasilitasi pengguna untuk memberikan ulasan teks serta bintang penilaian berskala 1 hingga 5. </p>

<h3 id="metode"> Metode Yang Digunakan </h3>
<p>Saat ini, aplikasi mobile menjadi komponen penting yang mempermudah memenuhi kebutuhan pengguna. Salah satunya adalah KAI Access, aplikasi layanan pemesanan tiket kereta api yang dilakukan secara online dengan memanfaatkan Internet. Dengan adanya kemudahan tersebut tak lantas dapat memuaskan pelanggan. Sistem juga memiliki celah yang perlu diperbaiki. Melalui pemahaman sentimen pengguna, pengembang aplikasi dapat merumuskan solusi untuk meningkatkan kualitas pelayanan yang akan diberikan. </p>


<h3 id="data"> Data penelitian </h3>
<p>Data yang digunakan merupakan data publik yang bersumber dari fitur ulasan pengguna di Google Play Store. Pendekatan kuantitatif dengan mengambil dan mengolah data menggunakan google-play-scraper dngan fungsi reviews() yang akan mengambil data pada aplikasi yang dituju saja. </p>

<h3 id="referensi"> Referensi </h3>
<p></p>

<h3 id="dataset"> Dataset </h3>
<p> <a href="https://github.com/donxuiqote/riset_informatika_c081/blob/main/data_scrapping.ipynb"> Dataset </a> </p>

import pandas as pd
import numpy as np
import seaborn as sns

!pip install google-play-scraper
from google_play_scraper import Sort, reviews
result, continuation_token = reviews(
'com.kai.kaiticketing',
lang='id',
country='id',
sort=Sort.MOST_RELEVANT,
count=10000, # defaults to 100
filter_score_with=None
)

data = pd.DataFrame(np.array(result), columns=['review'])
data = data.join(pd.DataFrame(data.pop('review').tolist()))
scrappeddata1 = data[['content','score','at']]
sorteddata = scrappeddata1.sort_values(by='at', ascending=True)
sorteddata.head()
     
