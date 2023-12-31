<h1> 🔰 &nbsp; RISET INFORMATIKA C081 </h1>
<p align=”center”>
<img width=”200" height=”200" src="https://github.com/donxuiqote/riset_informatika_c081/assets/113412835/c1cea88e-afaf-4d95-9e2c-e312d6a94b90">
</p>

<p> Endin Rahmanda - 20081010070  </p>

<h2> Daftar Isi </h2>

<ol>
    <li> <a href="#latar_belakang"> Latar Belakang </a> </li>
    <li> <a href="#metode"> Metode </a> </li>
    <li> <a href="#data"> Data Penelitian </a> </li>
    <li> <a href="#referensi"> Referensi </a> </li>
    <li> <a href="#dataset"> Dataset </a> </li>
    <li> <a href="#coding"> Coding </a> </li>
    <li> <a href="#analisis"> Analisis </a> </li>
    <li> <a href="#pendukung"> Fambar Pendukung </a> </li>
    <li> Mengatasi Error </li>
    <li> Draft Paper Publikasi </li>
</ol>

<h3 id="latar_belakang"> Latar Belakang </h3>
<p>Saat ini, aplikasi mobile menjadi komponen penting yang mempermudah memenuhi kebutuhan pengguna. Salah satunya adalah KAI Access, aplikasi layanan pemesanan tiket kereta api yang dilakukan secara online dengan memanfaatkan Internet. Dengan adanya kemudahan tersebut tak lantas dapat memuaskan pelanggan. Sistem juga memiliki celah yang perlu diperbaiki. Melalui pemahaman sentimen pengguna, pengembang aplikasi dapat merumuskan solusi untuk meningkatkan kualitas pelayanan yang akan diberikan. 
	
<p>Ulasan merupakan pendapat atau tanggapan yang diberikan oleh pengguna terkait pengalaman mereka dalam menggunakan suatu aplikasi. Ulasan ini biasanya memberikan pujian, kritik, atau saran terhadap pengalaman pengguna terhadap aplikasi tersebut. Google Play Store, sebuah platform distribusi utama untuk aplikasi Android, memfasilitasi pengguna untuk memberikan ulasan teks serta bintang penilaian berskala 1 hingga 5. </p>

<h3 id="metode"> Metode Yang Digunakan </h3>
<p>Saat ini, aplikasi mobile menjadi komponen penting yang mempermudah memenuhi kebutuhan pengguna. Salah satunya adalah KAI Access, aplikasi layanan pemesanan tiket kereta api yang dilakukan secara online dengan memanfaatkan Internet. Dengan adanya kemudahan tersebut tak lantas dapat memuaskan pelanggan. Sistem juga memiliki celah yang perlu diperbaiki. Melalui pemahaman sentimen pengguna, pengembang aplikasi dapat merumuskan solusi untuk meningkatkan kualitas pelayanan yang akan diberikan. </p>


<h3 id="data"> Data penelitian </h3>
<p>Data yang digunakan merupakan data publik yang bersumber dari fitur ulasan pengguna di Google Play Store. Pendekatan kuantitatif dengan mengambil dan mengolah data menggunakan google-play-scraper dngan fungsi reviews() yang akan mengambil data pada aplikasi yang dituju saja.

<a href="https://github.com/donxuiqote/riset_informatika_c081/blob/main/data_scrapping.ipynb"> Proses data scrapping </a>. Dari data yang telah discrape, akan diambil content review, score (skala rating 1 - 5), year, month, dan day, dan menambahkan kolom sentimen dengan kriteria :

<table>
	<tr>
		<td>Skor</td>
		<td>Sentimen</td>
	</tr>
	<tr>
		<td>1</td>
		<td>Negatif</td>
	</tr>
		<tr>
		<td>2</td>
		<td>Negatif</td>
	</tr>
		<tr>
		<td>3</td>
		<td>Netral</td>
	</tr>
		<tr>
		<td>4</td>
		<td>Positif</td>
	</tr>
		<tr>
		<td>5</td>
		<td>Positif</td>
	</tr>
</table>

Pada data penelitian juga dilakukan text-processing :
<ul>
	<li>Hapus URL / link, hastag, karakter / emoji, tanda baca, spasi </li>
	<li>Tokenizing</li>
	<li>Filtering</li>
	<li>Stopword</li>
</ul>

</p>

<h3 id="referensi"> Referensi </h3>

<ul>
	<li> <i> Referensi 1 </i> </li>
	
</ul>
<p> </p>

<h3 id="dataset"> Dataset </h3>
<p>
Dari <a href="https://github.com/donxuiqote/riset_informatika_c081/blob/main/data_scrapping.ipynb"> Proses data scrapping </a>, dapat diperoleh <a href="https://github.com/donxuiqote/riset_informatika_c081/blob/main/dataset.csv"> Dataset </a> sebagai berikut
	
<img src="https://github.com/donxuiqote/riset_informatika_c081/assets/113412835/314215fb-20ff-44fe-a0aa-594b8fc61891"> </img>

<ul>
	<li>terdapat 6959 data untuk penilaian bintang 1</li>
	<li>terdapat 1386 data untuk penilaian bintang 2</li>
	<li>terdapat 759 data untuk penilaian bintang 3</li>
	<li>terdapat 579 data untuk penilaian bintang 5</li>
	<li>terdapat 317 data untuk penilaian bintang 4</li>
</ul>

<img src="https://github.com/donxuiqote/riset_informatika_c081/blob/main/images/Screenshot%20(319).png">


</p>

<h3 id="coding"> Coding </h3>
<p>
<a href="https://github.com/donxuiqote/riset_informatika_c081/blob/main/coding.ipynb"> Coding </a> menggunakan Jupyter Notebook
</p>

<h3 id="analisis"> Analisis </h3>
<p>

 
Analisis sebagai berikut
	
<img src="https://github.com/donxuiqote/riset_informatika_c081/blob/main/images/Screenshot%20(324).png">
</p>

<h3 id="pendukung"> Gambar Pendukung </h3>
<p>
Dari proses data scrapping, dapat diperoleh <a href="https://github.com/donxuiqote/riset_informatika_c081/blob/main/dataset.csv"> Dataset </a> sebagai berikut
<img src="https://github.com/donxuiqote/riset_informatika_c081/blob/main/images/Screenshot%20(324).png">
</p>
