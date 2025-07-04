# Program Deteksi Influence Pewarnaan Graf Menggunakan Algoritma Genetika - Kelompok 3

## Komputasi Paralel dan Terdistribusi - C

### Anggota Kelompok:
1. Kholid Fahmi Nasution
2. Nayata Sandra Claudia Nasution
3. Fatihannisa Listy Zulmi
4. Johanes Alberto Siahaan
5. Ronaldo Damianus Parulian Silitonga
6. Lidya Alya Zahra
7. Yusuf Kala
8. Rizky Alpariji
9. Nur Annisa Balqis
10. Aqila Eling Febrianti
11. Muhammad Azi Maulana Manru
12. Frederick Godiva
13. Lukman Nur Hakim
14. Briyan Yehezkhiel
15. Kyla Zahra Winnetou
16. Najwa Afifi Situmorang

## Gambaran Umum Proyek

Proyek ini bertujuan untuk mendeteksi pengaruh (influence) dalam pewarnaan graf menggunakan Algoritma Genetika. Kami menerapkan metode ini pada dataset interaksi sosial untuk mengidentifikasi komunitas atau kelompok berpengaruh dalam jaringan.

## Langkah-langkah yang Dilakukan

1.  **Instalasi dan Import Library:** Menginstal library yang dibutuhkan (`deap`, `pandas`, `networkx`, `matplotlib`, `seaborn`, `sklearn`, `numpy`, `re`, `random`).
2.  **Memuat dan Membaca Dataset:** Memuat data dari file CSV (`dataset_akhir_fix.csv`) dan melakukan pra-pemrosesan data, termasuk konversi kolom ID menjadi string.
3.  **Ekstraksi Fitur:** Mengekstrak kolom-kolom relevan seperti `user_id_str`, `conversation_id_str`, `retweet_count`, `reply_count`, `quote_count`, dan `favorite_count`.
4.  **Pembangunan Graf dari Dataset:** Membuat graf NetworkX di mana node merepresentasikan pengguna dan percakapan, serta edge merepresentasikan interaksi dengan bobot berdasarkan total interaksi sosial.
5.  **Implementasi Pewarnaan Graf Menggunakan Algoritma Genetika:**
    *   **Inisialisasi Algoritma Genetika dengan DEAP:** Mengonfigurasi komponen algoritma genetika, termasuk definisi individu, fungsi evaluasi (menggunakan modularitas), crossover, mutasi, dan seleksi.
    *   **Implementasi dan Eksekusi Algoritma Genetika:** Menjalankan algoritma genetika untuk deteksi komunitas.
    *   **Deteksi Komunitas:** Menetapkan label komunitas yang diperoleh dari algoritma genetika ke node-node graf.
6.  **Evaluasi Hasil:** Menghitung metrik evaluasi seperti Modularity, Silhouette Coefficient, dan Adjusted Rand Index (ARI) untuk menilai kualitas deteksi komunitas.
7.  **Optimalisasi Deteksi Komunitas:**
    *   **Pendekatan Fixed Weighting:** Mengoptimalkan penugasan komunitas dengan menggunakan bobot tetap untuk fitur interaksi sosial saat membangun graf dan kemudian menjalankan algoritma genetika.
    *   **Optimalisasi Lebih Lanjut dengan Algoritma Genetika:** Melakukan optimalisasi lebih lanjut pada parameter algoritma genetika untuk meningkatkan nilai modularitas.

## Hasil dan Analisis

*   **Visualisasi Graf:** Menampilkan visualisasi graf dengan node diwarnai berdasarkan komunitas yang terdeteksi.
*   **Analisis Distribusi Fitur:** Memvisualisasikan distribusi fitur interaksi sosial sebelum dan setelah transformasi logaritmik.
*   **Metrik Evaluasi:** Melaporkan nilai Modularity, Silhouette Coefficient, dan Adjusted Rand Index (ARI) pada setiap tahap evaluasi dan optimalisasi.

Dari hasil yang diperoleh:
*   **Modularity:** Nilai modularitas meningkat secara signifikan setelah optimalisasi menggunakan algoritma genetika, menunjukkan struktur komunitas yang lebih baik.
*   **Silhouette Coefficient:** Nilai Silhouette Coefficient juga menunjukkan peningkatan, meskipun masih dalam rentang negatif, menandakan bahwa klaster masih belum sepenuhnya terpisah dengan jelas berdasarkan fitur yang digunakan.
*   **Adjusted Rand Index (ARI):** Nilai ARI yang tinggi menunjukkan konsistensi dalam penugasan label komunitas oleh algoritma.

Proyek ini menunjukkan potensi Algoritma Genetika dalam mendeteksi komunitas berpengaruh dalam jaringan interaksi sosial berdasarkan data yang diberikan.
