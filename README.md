# tugas-kelompok4-Object-Detection

# Praktik OpenCV:Part 4 Object Detection

Repository ini berisi hasil praktik Kelompok 1 untuk mata kuliah **Praktik Machine Learning / Pengolahan Citra Digital**. Proyek ini mencakup implementasi pendeteksian objek menggunakan library OpenCV dan Haar Cascade Classifier, mulai dari deteksi wajah statis hingga pelacakan kendaraan secara real-time, serta analisis tahapan Cascade Classifier Training. Kode dipraktikkan beserta dokumentasi yang menjelaskan langkah-langkahnya.

## Anggota Kelompok 1
**Informatika – Universitas Teknologi Sumbawa**
* **Sherly Novia Indriani** - 231001057
* **Dinda Oktavia Pratiwi** - 231001026
* **Ahsanul Ikram** - 231001077
* **Wanda Setya Budi** - 231001008

**Dosen Pengampu:** Herfandi, Ph.D.

---

## Alat dan Library
Untuk menjalankan proyek ini, kami menggunakan:
* **Bahasa:** Python 3.x
* **Library Utama:**
    * OpenCV (opencv-python)
    * NumPy
    * Matplotlib
* **Lain-lain:** Haar Training GUI (Amin Ahmadi)
* **Editor:** JupyterLab / Jupyter Notebook

---

## Langkah-Langkah Praktik
Dokumentasi ini menjelaskan proses yang dilakukan di dalam file kodingan:

### 1. Persiapan dan Import Model Cascade
Menginisialisasi library dan memuat model kecerdasan buatan bawaan OpenCV berekstensi `.xml` menggunakan `cv2.CascadeClassifier()`.

### 2. Deteksi Multi-Objek pada Gambar Statis
Mendeteksi Wajah, Mata, dan Senyuman pada file gambar. Menggunakan teknik *Region of Interest* (ROI) untuk mengoptimalkan kinerja algoritma dengan membatasi area pencarian mata dan senyuman hanya di dalam area wajah.

### 3. Pembuatan Custom Bounding Box & Deteksi Real-Time
Mengakses webcam melalui `cv2.VideoCapture(0)` untuk deteksi *real-time*. Kami juga membuat fungsi kustom `draw_ped()` untuk menggambar kotak pelindung (*bounding box*) yang dilengkapi dengan latar warna solid dan label teks.

### 4. Deteksi Kendaraan dan Pejalan Kaki
Memuat model `cars.xml` dan `haarcascade_fullbody.xml` untuk mendeteksi mobil dan postur manusia dari file video `.mp4`. Pemrosesan dioptimalkan dengan memperkecil ukuran *frame* (resize) sebesar 50% untuk menjaga kelancaran *Frame Per Second* (FPS).

### 5. Analisis Cascade Classifier Training
Menganalisis proses di balik layar pembuatan file `.xml` menggunakan himpunan gambar positif dan negatif. Pelatihan dievaluasi berdasarkan log indikator *Hit Rate* (HR) dan *False Alarm* (FA) per tahapannya.

---

## Video Presentasi
Penjelasan detail mengenai proses yang dilakukan, hasil yang didapat, dan analisis atau penjelasan singkat mengenai kode yang diimplementasikan dapat dilihat pada video presentasi YouTube kami berikut:
👉 [https://youtu.be/hbu9swQJ2Wc]
