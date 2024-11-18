<h1 align="center"> NLP With HuggingFace Transformers </h1>
<p align="center"> Berisi tentang pipeline dari HuggingFace Transformers untuk keperluan NLP (Natural Language Processing)</p>

<div align="center">

<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
<img src="https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white">
<img src="https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white">

</div>

<h2 align="center"> Analisis </h1>

- Zero-Shot Classification merupakan teknik dalam pemrosesan NLP (Natural Language Processing) dimana model dapat mengklasifikasikan teks kedalam kategori tertentu tanpa membutuhkan pelatihan khusus pada kategori tersebut. Teknik ini akan memungkinkan model untuk memahami hubungan teks dan label kandidat berdasarkan konteks,  meskipun label tesebut belum pernah ditemukan selama pelatihan model. Dalam pipeline ini defaultnya menggunakan model "facebook/bart-large-mnli", namun dapat diubah dengan menggunakan parameter tambahan. Urutan label kandidat berdasarkan probabilitas kecocokan, dari yang tertinggi ke terendah.
Dari model yang dibuat, label "transport" memiliki persentase yang tertinggi. Hal tersebut menunjukkan bahwa model menganggap teks ini paling relevan dengan kategori "transport.

- Text generation merupakan salah satu teknik dalam NLP yang akan membuat teks secara otomatis. Model ini akan membuat teks berdasarkan prompt awal yang diberikan dan akan melanjutkan teks tersebut berdasarkan konteks input. Model ini sangat mudah digunakan untuk membuat konten kreatif. Namun model ini memiliki kontrol yang terbatas dalam membuat teks, sehingga akan sulit memprediksi arah teks yang dihasilkan meskipun parameter dikontrol.

- Fill-mask merupakan teknik untuk mengisi token yang kosong (<mask>) dalam sebuah kalimat dengan prediksi kata yang paling memungkinkan berdasarkan pada konteksnya. Dalam model yang dibuat, ditambahkan dengan parameter "top_k=2" yang berarti output yang ditampilkan adalah 2 kata prediksi teratas. Modek ini dapat digunakan untuk memahami konteks atau menghasilkan rekomendasi kata dalam berbagai bahasa (jika modelnya mendukung). Model ini memiliki keterbatasan dalam memprediksi kata yang hanya akan memprediksi satu token pada posisi <mask>. Model ini cocok digunakan untuk autokoreksi yang berfungsi untuk melengkapi kalimat dengan kata yang hilang.

- NER (Named Entity Recognition) merupakan model yang mengidentifikasi dan mengelompokkan entitas tertentu (seperti nama, lokasi, organisasi, dll.) dalam teks. Model membaca teks dan memprediksi label untuk setiap token berdasarkan konteksnya.Label mencakup kategori seperti B-PER (beginning of a person), I-PER (inside a person name), dll. Akurasi dari model ini bergantung pada model pralatih dan dataset pelatihannya. Model ini dapat diterapkan pada analisis teks secara otomatis untuk menemukan nama orang, organisasi, atau lokasi dari dokumen.

- Question-answering merupakan pipeline yang memiliki fungsi untuk menjawab pertanyaan berdasarkan konteks yang diberikan. Model tersebut hanya bisa menjawab jika konteks mencakup informasi yang relevan. Model ini memberikan jawaban pendek dari teks, bukan penjelasan mendalam.

- Sentiment-analysis merupakan pipeline yang berfungsi untuk menganalisis apakah teks mengandung sentimen positif, negatif, atau netral. Model ini Dapat menganalisis banyak data teks secara otomatis dan dapat memahami perasaan atau opini orang terhadap produk, layanan, atau isu tertentu. Namun model ini memiliki kekurangan yaitu terkadang model kesulitan dengan sentimen yang lebih kompleks atau ambigu.

- Summarization merupakan pipeline yang berfungsi untuk merangkum atau meringkas teks panjang menjadi bentuk yang lebih singkat, sambil mempertahankan informasi penting dan inti dari teks asli. Model ini dapat membantu pembaca untuk memahami inti dari teks panjang tanpa harus membaca seluruhnya. Model ini mungkin kesulitan merangkum teks yang sangat teknis atau sangat panjang dengan keakuratan tinggi.

- Dalam NLP terdapat pipeline yang berguna untuk menerjemahkan kalimat dari satu bahasa menjadi bahasa lainnya. Pengaturan bahasa yang diubah dapat diatur pada "translation_id_to_en", misalnya "translation_en_to_id" maka pipeline tersebut akan menerjemahkan dari Bahasa Inggris ke Bahasa Indonesia.
