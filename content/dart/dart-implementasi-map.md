---
title: "Dart Map"
date: 2019-11-18T18:45:15+07:00
draft: false
banner: https://res.cloudinary.com/w-cotutorial/image/upload/q_auto:low/dart/dart_map_j37c4c.jpg
tiny: https://res.cloudinary.com/w-cotutorial/image/upload/q_10,ar_5:3,c_fill/dart/dart_map_j37c4c.jpg
categories:
  - dart
tags:
  - dart
  - basic
author: 
- wisnuwiry  
---

### Apa itu Map?

Map yaitu suatu objek yang terdiri dari **key** dan **value**. Map **key** sebagai kunci inisialisasi yang dapat dipanggi dan di manipulasi, dan sedangkan **value** sebagai nilai atau isi yang ada pada key tersebut. 

Pada Map ini ada juga aturan penulisanya juga, untuk `key` harus bertipe [String](/dart/dart-tipe-data-string/) dan `value` di map nilainya bisa bersifat apa saja/dynamic. 

Map kita diperbolehkan mengedit suatu element pada Map, tapi hanya untuk `value` nya saja dan untuk `key` tidak diperbolehkan untuk mengedit saat runtime.

Untuk mendeklarasikan map terdiri dari dua cara yaitu:

- Map [Literal](#1-literal)
- Map [Constructor](#2-constructor)

Berikut macam-macam cara untuk mendeklarasikan sebuah Map:

## 1. Literal
Pada pendeklarasian Map Literal ini teman-teman perlu menggukan kode kurung kurawal/keriting sepasang `{}`. Berikut contoh sintaksnya:
```dart
var nama_variabel = { key1:value1, key2:value2 }
```
Pada kode diatas ada `key1` dan `key2` sebagai kata kunci/key dalam map, dan sedangakan `value1` dan `value2` sebagai value/nilai dari kata kunci map tersebut. Berikut contoh kodenya:

```dart
void main() { 
   var profile = {'name':'Dart','platform':'Any'}; 
   print(profile); 
}
```
maka ouputnya:
```
{name: Dart, platform: Any}
```
ataupun jika ingin menginisialisasikan secara spesifik per key anda gunakan sintaks berikut:

```dart
variabel_map[key]
```
contoh kode
```dart
void main() { 
   var profile = {'name':'Dart','platform':'Any'};
   print(profile['name']); 
}
```
output:
```
Dart
```

---

## 2. Constructor

Pada pendeklarasian kali ini yaitu Map constructor, cuma perlu dua langkah saja yaitu:

1. Langkah 1 Mendeklarasikan Map
  ```dart
  var nama_variabel = new Map()
  ```
2. Langkah 2 Menginisialisasian
  ```dart
  nama_map[key]=value
  ```

Berikut contoh full kodenya:
```dart
void main() {
  var language = new Map();
  language['name'] = 'Dart'; //penambahan data pada map
  language['like'] = 'YES';
  print(language);
}
```
Pada contoh diatas awal mulanya variabel `language` berupa map yang kosong kemudian pada line ke 3-4 ada proses penambahan map elemen.
Output:
```
{name: Dart, like: Yes}
```

---

## Property
Pada Dart Map telah disediakan berbagai macam properti diantaranya sebagai berikut:

Property | Deskripsi
---------|----------
[keys](#keys) | Mengembalikan semua `key` pada Map tersebut
values | Mengembalikan semua `value` pada Map tersebut
lenght | Mengembalikan jumlah panjang pada Map tersebut
isEmpty | Mengembalikan **true** jika elemen map kosong/tidak berisi, **false** jika tidak
isNotEmpty | Mengembalikan **true** jika elemen map tersebut tidak kosong. **false** jika tidak.

Berikut contoh-contoh dari property Map:

### keys
```dart
void main() {
  var profile = {'name' : 'Jhon', 'age': 12, 'avatar' : 'image.jpg'};
  print(profile.keys);
}
```
output: 

```
(name, age, avatar)
```

Pada property ini berfungsi untuk mengembalikan sebuah daftar key dari suatu map.

---

### values
```dart
void main() {
  var profile = {'name' : 'Jhon', 'age': 12, 'avatar' : 'image.jpg'};
  print(profile.values);
}
```
