# Proyek Akhir Pemrograman Berbasis Objek 1

Proyek ini adalah contoh sederhana aplikasi pengolahan data mahasiswa menggunakan Java sebagai tugas akhir dari mata kuliah pemrograman berbasis objek 1.

## Deskripsi

Aplikasi ini menerima input berupa Merek Baju dan Kode Baju, dan memberikan output berupa informasi detail dari Baju, Merek, Kode, Warna, Ukuran.

Aplikasi ini mengimplementasikan beberapa konsep penting dalam pemrograman berorientasi objek (OOP) seperti Class, Object, Atribut, Method Constructor, Method Mutator, Method Accessor, Encapsulation, Inheritance, Overloading, Overriding, Seleksi, Perulangan, IO Sederhana, Array, dan Error Handling.

## Penjelasan Kode

Berikut adalah bagian kode yang relevan dengan konsep OOP yang dijelaskan:

1. **Class** adalah template atau blueprint dari object. Pada kode ini, `Baju`, `BajuDetail`, dan `Main` adalah contoh dari class.

```bash
public class Baju {
    ...
}

public class BajuDetail extends Baju {
    ...
}

public class Main {
    ...
}
```

2. **Object** adalah instance dari class. Pada kode ini, `baju = new BajuDetail(merk, kodeBaju);` adalah contoh pembuatan object.

```bash
baju = new BajuDetail(merk, kodeBaju);
```

3. **Atribut** adalah variabel yang ada dalam class. Pada kode ini, `merk` dan `kodeBaju` adalah contoh atribut.

```bash
String merk;
String kodeBaju;
```

4. **Constructor** adalah method yang pertama kali dijalankan pada saat pembuatan object. Pada kode ini, constructor ada di dalam class `Baju` dan `BajuDetail`.

```bash
public Baju(String merk, String kodeBaju) {
        this.merk = merk;
        this.kodeBaju = kodeBaju;
}

 public BajuDetail(String merk, String kodeBaju) {
        super(merk, kodeBaju);
}
```

5. **Mutator** atau setter digunakan untuk mengubah nilai dari suatu atribut. Pada kode ini, `setMerek` dan `setKodeBaju` adalah contoh method mutator.

```bash
public void setMerk(String merk) {
        this.merk = merk;
}

public void setKodeBaju(String kodeBaju) {
        this.kodeBaju = kodeBaju;
}
```

6. **Accessor** atau getter digunakan untuk mengambil nilai dari suatu atribut. Pada kode ini, `getMerek`, `getKodeBaju` adalah contoh method accessor.

```bash
public String getMerk() {
        return merk;;
}

public String getKodeBaju() {
        return kodeBaju;
}
```

7. **Encapsulation** adalah konsep menyembunyikan data dengan membuat atribut menjadi private dan hanya bisa diakses melalui method. Pada kode ini, atribut `merek` dan `KodeBaju` dienkapsulasi dan hanya bisa diakses melalui method getter dan setter.

```bash
private String merk;
private String kodeBaju;
```

8. **Inheritance** adalah konsep di mana sebuah class bisa mewarisi property dan method dari class lain. Pada kode ini, `bajuDetail` mewarisi `baju` dengan sintaks `extends`.

```bash
public class BajuDetail extends Baju {
    ...
}
```

9. **Polymorphism** adalah konsep di mana sebuah nama dapat digunakan untuk merujuk ke beberapa tipe atau bentuk objek berbeda. Ini memungkinkan metode-metode dengan nama yang sama untuk berperilaku berbeda tergantung pada tipe objek yang mereka manipulasi, polymorphism bisa berbentuk Overloading ataupun Overriding. Pada kode ini, method `displayInfo(String)` di `Baju` merupakan overloading method `displayInfo` dan `displayInfo` di `BajuDetail` merupakan override dari method `displayInfo` di `Baju`.

```bash
public String DisplayInfo() {
  return "Merk: " + getMerk() + "\nKode Baju: " + getKodeBaju();
}

@Override
public String DisplayInfo() {
    ...
}
```

10. **Seleksi** adalah statement kontrol yang digunakan untuk membuat keputusan berdasarkan kondisi. Pada kode ini, digunakan seleksi `if else` dalam method `getKodeWarna` dan seleksi `switch` dalam method `getKodeUkuran`.

```bash
public String getKodeWarna() {
  String kodeWarna = getKodeBaju().substring(0, 2);
  switch (kodeWarna) {
    case "01":
      return "Merah";
    case "02":
      return "Biru";
    default:
      return "Warna Lain";

}

public String getKodeUkuran() {
  String kodeUkuran = getKodeBaju().substring(2, 4);
  switch (kodeUkuran) {
    case "01":
      return "Kecil";
    case "02":
      return "Sedang";
    case "03":
      return "Besar";
    default:
      return "Ukuran Lain";
    }
}
```

11. **Perulangan** adalah statement kontrol yang digunakan untuk menjalankan blok kode berulang kali. Pada kode ini, digunakan loop `for` untuk meminta input dan menampilkan data.

```bash
for (int i = 0; i < bajuArray.length; i++) {
    ...
}
```

12. **Input Output Sederhana** digunakan untuk menerima input dari user dan menampilkan output ke user. Pada kode ini, digunakan class `Scanner` untuk menerima input dan method `System.out.println` untuk menampilkan output.

```bash
Scanner scanner = new Scanner(System.in);
System.out.print("Masukkan Nama Mahasiswa ke-" + (i + 1) + ": ");
String nama = scanner.nextLine();

System.out.println("Detail Baju: ");
System.out.println(baju.DisplayInfo());
```

13. **Array** adalah struktur data yang digunakan untuk menyimpan beberapa nilai dalam satu variabel. Pada kode ini, `BajuDetail[] mahasiswas = new BajuDetail[2];` adalah contoh penggunaan array.

```bash
BajuDetail[] bajuArray = new BajuDetail[2];
```

14. **Error Handling** digunakan untuk menangani error yang mungkin terjadi saat runtime. Pada kode ini, digunakan `try catch` untuk menangani error.

```bash
try {
    // code that might throw an exception
} catch (Exception e) {
            System.out.println("Kesalahan Umum: " + e.getMessage());
}
```

## Usulan nilai

| No  | Materi         |  Nilai  |
| :-: | -------------- | :-----: |
|  1  | Class          |    5    |
|  2  | Object         |    5    |
|  3  | Atribut        |    5    |
|  4  | Constructor    |    5    |
|  5  | Mutator        |    5    |
|  6  | Accessor       |    5    |
|  7  | Encapsulation  |    5    |
|  8  | Inheritance    |    5    |
|  9  | Polymorphism   |   10    |
| 10  | Seleksi        |    5    |
| 11  | Perulangan     |    5    |
| 12  | IO Sederhana   |   10    |
| 13  | Array          |   15    |
| 14  | Error Handling |   15    |
|     | **TOTAL**      | **100** |

## Pembuat

Nama: Muhammad Rizki Insani
NPM: 2210010075
