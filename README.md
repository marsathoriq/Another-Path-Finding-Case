# Dynamic Programming : Another Path Finding Case
### **_(Ubah file README.md ini setelah program diselesaikan)_**

## Latar Belakang
*Path Finding* adalah masalah yang berfokus untuk mencari langkah paling optimum untuk bergerak dari posisi asal ke posisi akhir dengan batasan-batasan (*constraints*) tertentu. 

## Spesifikasi
Buatlah dalam bahasa pemrograman **_Go_**, sebuah web service berupa **_REST API_**, yang dapat mengeja (dalam bahasa Indonesia) dari angka yang diberikan serta menuliskan angka yang tepat dari masukkan ejaan angka (dalam bahasa Indonesia juga), dengan ketentuan-ketentuan sebagai berikut :

1. Terdapat 2 buah endpoint API yang perlu dibuat, yaitu '**GET** /spell' yang menerima parameter angka, serta '**POST** /read' yang menerima body/payload berupa text/ejaan. Jika input parameter atau body/payload tidak valid, maka berikan response keterangan error/gagal dengan format dibebaskan.

2. Sebagai REST API, maka response harus berupa JSON. Struktur data response JSON dibebaskan.

3. Program dibuat dengan mengikuti standar development resmi Go (lihat referensi #3), yaitu environment kode program berada pada ```$GOPATH/src/```, misalkan ```$GOPATH/src/github.com/Indonesian-Numeral-Spellers```.

4. Arsitektur program dibebaskan (boleh mengikuti referensi-referensi _REST API with Go_ dari internet), namun harus tetap tersusun dengan rapi dan mengerti apa kegunaan setiap fungsi, file, serta package.

5. Batasan kasus uji : 2000000000 (dua milyar)

## Contoh Kasus Uji
### Contoh Kasus Uji 1 : Pengejaan
Request :
```
GET '/spell?number=123456'
```
Response :
```JSON
STATUS CODE 200
{
    "status" : "OK",
    "text" : "seratus dua puluh tiga ribu empat ratus lima puluh enam"
}
```
### Contoh Kasus Uji 2 : Pembacaan
Request:
```JSON
POST '/read'
{
    "text" : "seribu sembilan ratus sembilan puluh tujuh"
}
```
Response :
```JSON
STATUS CODE 200
{
    "status" : "OK",
    "number" : 1997
}
```

## Bonus
Buatlah sebuah aplikasi mobile atau website dengan tampilan menarik, yang menggunakan kedua API tersebut. Semakin menarik tampilan, semakin tinggi poin yang akan didapat.

Teknologi yang direkomendasikan : **React.js**

## Penilaian
- Kebenaran fungsionalitas program.
- Kebenaran API.
- Pemahaman tentang bahasa pemrograman **Go** serta **REST API**.
- Kerapihan _repository_ & kode, termasuk **README** (fungsi program, contoh request & response dari setiap endpoint) dan **arsitektur kode Go**.
- UI (bonus).

Nilai maksimum yang bisa didapatkan adalah **1600 (2600 dengan bonus)** poin. <br>
_(Seribu Enam Ratus)_

## Referensi Pengerjaan _(sangat disarankan untuk diikuti dengan baik)_
1. https://golang.org/doc/install
2. https://github.com/golang/go/wiki/SettingGOPATH
3. https://golang.org/doc/code.html#Introduction
4. https://tour.golang.org/welcome/1
5. https://openclassrooms.com/en/courses/3432056-build-your-web-projects-with-rest-apis/3496011-identify-examples-of-rest-apis
6. https://www.codementor.io/codehakase/building-a-restful-api-with-golang-a6yivzqdo