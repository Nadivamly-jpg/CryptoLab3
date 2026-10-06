# CryptoLab — Implementasi Kriptosystem Sederhana

Implementasi tugas A Kriptography PSDKU 2026–2027 menggunakan **Python + Flask**.

## Fitur
1. Shift Cipher
2. Substitution Cipher
3. Affine Cipher
4. Vigenere Cipher
5. Hill Cipher
6. Permutation Cipher
7. One-time Pad
8. Mode Text dan File
9. Tampilan ciphertext tanpa spasi/kelompok 5 melalui fungsi backend `group5`
10. Simpan ciphertext
11. OTP key generator 10.000 huruf
12. Byte-safe file encryption sehingga file biner dapat didekripsi kembali

## Menjalankan
Windows:
```bat
py -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python app.py
```
Buka http://127.0.0.1:5000

## Contoh kunci text
- Shift: `3`
- Substitution: `qwertyuiopasdfghjklzxcvbnm`
- Affine: `5,8`
- Vigenere: `kripto`
- Hill: `3 3; 2 5`
- Permutation: `3 1 4 2`
- OTP: generate 10.000 huruf

## Catatan implementasi file
Spesifikasi tugas meminta setiap byte file diproses, termasuk header. Karena itu mode File menggunakan transformasi byte-safe. Untuk Vigenere/OTP pada mode Text, hanya huruf a-z yang diproses dan karakter lain dibuang saat ciphertext ditampilkan, sesuai spesifikasi tugas.

Untuk Hill file, matriks 2x2 dipakai dengan modulus 256. Untuk Substitution file, kunci adalah 256-byte permutation dalam HEX.
