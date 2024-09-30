# Tugas Praktikum 1 (Pertemuan ke 2) 

|Nama|NIM|Kelas|Mata Kuliah|
|----|---|-----|------|
|**Radityatama Nugraha**|**312310644**|**TI.23.A6**|**Pemrograman Orientasi Objek**|

![gambar](dokumentasi7/sss2.jpeg)

# Input Code :
## • Data Pesawat
```java
public class PesawatTempur {

    private final String warna;
    private int ketinggian; 
    private int kecepatan; 
    private int energi; 
    private String arah;
    private static final int MAX_KECEPATAN = 900;
    private static final int MAX_KETINGGIAN = 10000; 

    public PesawatTempur(String warna) {
        this.warna = warna;
        this.ketinggian = 0;
        this.kecepatan = 0;
        this.energi = 100;
        this.arah = "Utara";
    }
```
## • Fungsi Untuk Menyalakan Mesin
```java
public void nyalakanMesin() {
        System.out.println("Mesin pesawat dinyalakan...");
    }
```
## • Fungsi Untuk Terbang
```java
 public void terbang() {
        if (this.kecepatan > 0) {
            if (this.energi >= 10) { 
                this.energi -= 10; // 
                System.out.println("Pesawat terbang...");
            } else {
                System.out.println("Energi tidak cukup untuk terbang.");
            }
        } else {
            System.out.println("Pesawat harus memiliki kecepatan untuk terbang.");
        }
    }
```
## • Fungsi Untuk Menambah Kecepatan
```java
public void tambahKecepatan(int kecepatan) {
        this.kecepatan += kecepatan;
        if (this.kecepatan > MAX_KECEPATAN) {
            this.kecepatan = MAX_KECEPATAN; 
        }
        System.out.println("Kecepatan pesawat bertambah menjadi " + this.kecepatan + " km/jam");
    }
```
## • Fungsi Untuk Mengurangi Kecepatan
```java
public void kurangiKecepatan(int kecepatan) {
        this.kecepatan -= kecepatan;
        if (this.kecepatan < 0) {
            this.kecepatan = 0; 
        }
        System.out.println("Kecepatan pesawat berkurang menjadi " + this.kecepatan + " km/jam");
    }
```
## • Fungsi Untuk Belok
```java
public void belok(String arah) {
        this.arah = arah;
        System.out.println("Pesawat berbelok ke arah " + this.arah);
    }
```
## • Fungsi Untuk Turun
```java
public void turun() {
        if (this.ketinggian - 100 >= 0) {
            this.ketinggian -= 100;
            System.out.println("Pesawat turun ke ketinggian " + this.ketinggian + " meter");
        } else {
            System.out.println("Pesawat sudah berada di ketinggian minimum.");
        }
    }
```
## • Fungsi Untuk Naik
```java
public void naik() {
        if (this.ketinggian + 100 <= MAX_KETINGGIAN) {
            this.ketinggian += 100;
            System.out.println("Pesawat naik ke ketinggian " + this.ketinggian + " meter");
        } else {
            System.out.println("Tidak dapat naik, sudah mencapai ketinggian maksimum.");
        }
    }
```
## • Fungsi Untuk Menampilkan Informasi Pesawat
```java
public void infoPesawat() {
        System.out.println("------------------------");
        System.out.println("Informasi Pesawat:");
        System.out.println("Warna: " + this.warna);
        System.out.println("Ketinggian: " + this.ketinggian + " meter");
        System.out.println("Kecepatan: " + this.kecepatan + " km/jam");
        System.out.println("Energi: " + this.energi + "%");
        System.out.println("Arah: " + this.arah);
        System.out.println("------------------------");
    }
```

## • Membuat Objek Pesawat
```java
public static void main(String[] args) {

        PesawatTempur pesawat1 = new PesawatTempur("Putih");
```

## • Menampilkan Informasi awal pesawat
```java
        pesawat1.infoPesawat();
```

## • Menyalakan Mesin Pesawat
```java
        pesawat1.nyalakanMesin(); 
```

## • Menambah Kecepatan Pesawat
```java
        pesawat1.tambahKecepatan(200);
```

## • Terbang
```java
        pesawat1.terbang();
```

## • Belok Ke Arah Barat
```java
        pesawat1.belok("Barat");
```

## • Menambah Kecepatan Lagi
```java
        pesawat1.tambahKecepatan(100);
```

## • Menampilkan Informasi Pesawat
```java
        pesawat1.infoPesawat();
```

## • Mengurangi Kecepatan
```java
        pesawat1.kurangiKecepatan(50);
```

## • Turun
```java
        pesawat1.turun();
```

## • Naik
```java
        pesawat1.naik();
```

## • Menampilkan Informasi Pesawat
```java
        pesawat1.infoPesawat();
    }
}
```

# Output Code :
![gambar](dokumentasi7/sss3.png)
































































