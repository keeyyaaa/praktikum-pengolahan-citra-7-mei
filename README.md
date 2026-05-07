# praktikum-pengolahan-citra-7-mei

Nama: Ica Rizqiah

Nim: 312410554

Kelas: I241E

---

## 📝 Deskripsi Proyek
Proyek ini merupakan implementasi dan analisis komparatif dari algoritma pendeteksian tepi (Edge Detection) pada citra medis (dataset Kanker). Proyek ini dibagi menjadi tiga tugas utama:
1. **Tugas 1:** Implementasi fungsi konvolusi dan operator Sobel secara manual (dari *scratch*).
2. **Tugas 2:** Analisis *Parameter Sweep* pada metode Canny dan perbandingannya dengan Sobel.
3. **Tugas 3:** Pembuatan aplikasi Web Interaktif menggunakan Streamlit.

---

## 🚀 Fitur & Analisis

### 1️⃣ Tugas 1: Sobel Edge Detection (Manual)
Pada bagian ini, deteksi tepi dilakukan dengan membangun fungsi konvolusi 2D secara mandiri menggunakan `numpy` dengan *padding reflect*. 
* **Metode:** Menggunakan kernel Gx (horizontal) dan Gy (vertikal) berukuran 3x3.
* **Evaluasi:** Hasil Sobel manual dibandingkan dengan fungsi `cv2.Sobel` bawaan OpenCV, dan tingkat kemiripannya diukur menggunakan **RMSE (Root Mean Square Error)**.

 |Hasil Tugas 1 |
|:---:|
| <img src="tugas 1.png" width="1000"> |

### 2️⃣ Tugas 2: Canny Parameter Sweep
Eksperimen ini bertujuan untuk melihat sensitivitas metode Canny terhadap perubahan parameter.
* **Dataset:** 3 citra medis kanker dengan karakteristik berbeda (kontras rendah, noise, dll).
* **Visualisasi:** Menggunakan **Heat Map** (berwarna *Purples*) untuk memetakan jumlah piksel tepi yang terdeteksi pada berbagai kombinasi *Low Threshold* dan *High Threshold*.
* **Hasil:** Semakin rendah nilai threshold, program menjadi semakin sensitif dan mendeteksi lebih banyak garis tepi (noise ikut terdeteksi).

 | Hasil Tugas 2 | Hasil Tugas 2 | Hasil Tugas 2 |
|:---:|:---:|:---:|
| <img src="tugas2 1.png" width="1000"> | <img src="tugas2 2.png" width="1000"> | <img src="tugas2 3.png" width="1000"> |




### 3️⃣ Tugas 3: Streamlit Web App 🐈
Aplikasi web interaktif dengan antarmuka yang ramah pengguna.
* **Fitur:** - *Upload* gambar citra medis secara langsung.
  - *Slider* interaktif untuk mengatur parameter Sobel (Kernel Size, Threshold) dan Canny (Sigma, Low/High Threshold).
  - Statistik *real-time* (Waktu Komputasi, Jumlah Tepi, Edge Density).
  - Fitur unduh (Download) hasil gambar deteksi tepi.

---
 | Tugas 3 |
|:---:|
| <img src="tugas 3.png" width="1000"> |

## 🛠️ Cara Menjalankan Aplikasi (How to Run)

1. Pastikan Python sudah terinstall di komputermu.
2. Clone repository ini ke komputer lokal.
3. Buka terminal dan arahkan ke folder proyek.
4. Install semua *library* yang dibutuhkan dengan perintah berikut:
   ```bash
   pip install opencv-python numpy matplotlib scikit-image Pillow streamlit
Untuk menjalankan Web App (Tugas 3), ketik perintah ini di terminal:

Bash
streamlit run app.py

