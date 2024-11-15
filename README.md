# PengecakanAngka
 Tugas 1-Muhammad Azhari Nur Pratama-2210010326
## 1. Deskripsi Program:
• GUI terdiri dari JTextField untuk input angka dan tombol Cek
• Saat tombol ditekan, program akan memvalidasi input dan
menampilkan hasilnya pada JLabel

## 2. Komponen GUI: 
JFrame, JPanel, JLabel, JTextField, JButton

## 3. Logika Program: 
Kondisional (if-else), Validasi input

## 4. Events:
A.ActionListener untuk tombol Cek
~~~
private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
     try{
        int angka = Integer.parseInt(jTextField1.getText());
         String hasil = "Angka " + angka;

         // Mengecek apakah angka genap atau ganjil
         if (angka % 2 == 0) {
             hasil += " adalah Genap";
         } else {
             hasil += " adalah Ganjil";
         }
~~~
B.KeyAdapter pada JTextField untuk membatasi input hanya angka
~~~
private void jTextField1KeyTyped(java.awt.event.KeyEvent evt) {                                     
       if (!Character.isDigit(evt.getKeyChar())) {
         evt.consume();
         }
~~~
5. Variasi:
• Tambahkan fitur untuk memeriksa apakah angka tersebut adalah bilangan prima
~~~
if (isPrime(angka)) {
             hasil += " dan bilangan prima";
         } else {
             hasil += " dan bukan bilangan prima";
         }
private boolean isPrime(int number) {
         if (number <= 1) return false;
         for (int i = 2; i <= Math.sqrt(number); i++) {
             if (number % i == 0) return false;
         }
         return true;
     }
 ~~~
• Gunakan JOptionPane untuk menampilkan pesan hasil dan error
 ~~~
 } catch (NumberFormatException e) {
         JOptionPane.showMessageDialog(this, "Masukkan angka yang valid!", "Error", JOptionPane.ERROR_MESSAGE);
     }

~~~
• Implementasikan FocusListener untuk membersihkan JTextField saat mendapatkan focus
~~~
private void jTextField1FocusGained(java.awt.event.FocusEvent evt) {                                        
       jTextField1.setText("");
    }
~~~
    
## Contoh Gambar Project Setelah di Run
![](https://github.com/Azharipratama09/PengecakanAngka/blob/main/Cuplikan%20layar%202024-11-04%20095400.png)
 

## Indikator Penilaian:

| No  | Komponen         |  Persentase  |
| :-: | --------------   |   :-----:    |
|  1  | Komponen GUI     |    20    |
|  2  | Logika Program   |    20    |
|  3  | Event    |    15    |
|  4  | Kesesuaian UI     |    15    |
|  5  | Memenuhi Variasi |    30    |
|     | TOTAL        | 100 |

## Pembuat

Nama:Muhammad Azhari Nur Pratama
NPM:2210010326
