# 🌍 Venus – Level 01

## 📜 Deskripsi Misi

Setelah berhasil masuk ke server **Venus** via SSH, saya membaca misi pertama yang terdapat pada file `mission.txt`:

> User **sophia** has saved her password in a hidden file in this folder. Find it and log in as sophia.

Tugasnya cukup jelas yaitu menemukan file tersembunyi yang berisi password milik user **sophia**, kemudian login sebagai user tersebut.

---

## 🛠️ Langkah Penyelesaian

1. **Masuk ke server Venus via SSH**

   ```bash
   ssh hacker@venus.hackmyvm.eu -p 5000
   # Password: havefun!
   ```

2. **Melihat isi folder beserta file tersembunyi**  
   Gunakan opsi `-la` pada perintah `ls` untuk menampilkan semua file, termasuk yang tersembunyi:

   ```bash
   ls -la
   ```

   Dari hasilnya, terlihat sebuah file bernama `.myhiddenpazz`.

3. **Membaca isi file tersembunyi**  
   File `.myhiddenpazz` ternyata berisi password user **sophia**:

   ```bash
   cat .myhiddenpazz
   ```

   Output:

   ```
   Y1o645M3mR84ejc
   ```

4. **Login sebagai user sophia**  
   Gunakan perintah `su` untuk berganti user:

   ```bash
   su sophia
   # Password: Y1o645M3mR84ejc
   ```

5. **Berhasil login** 🎉
