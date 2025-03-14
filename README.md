# ***Music Player***

## Table of JavaScript Methods

| Method                  | Description |
|-------------------------|-------------|
| `new Audio()`           | Membuat objek audio baru yang memungkinkan kita untuk memutar file suara dalam JavaScript. Dengan metode ini, kita bisa menambahkan efek suara atau musik ke dalam aplikasi web tanpa perlu menggunakan elemen HTML `<audio>`. Objek `Audio` memiliki berbagai metode seperti `.play()`, `.pause()`, dan `.volume`. |
| `.find()`               | Metode array yang digunakan untuk mencari elemen pertama dalam array yang memenuhi kondisi yang ditentukan dalam callback function. Jika ada elemen yang cocok, metode ini mengembalikan elemen tersebut. Jika tidak ada yang cocok, hasilnya adalah `undefined`. Metode ini tidak mengubah array asli. |
| `?.` (Optional Chaining) | Operator yang digunakan untuk mengakses properti atau metode dari objek secara aman tanpa harus memeriksa apakah objek tersebut `null` atau `undefined`. Jika objek atau properti yang diakses tidak ada, hasilnya akan `undefined` tanpa menyebabkan error, sehingga mencegah runtime error pada objek bersarang (nested objects). |
| `.play()`               | Metode yang digunakan untuk memulai pemutaran file audio atau video yang dimuat dalam elemen HTML `<audio>` atau `<video>`. Jika pemutaran berhasil, metode ini mengembalikan `Promise`. Jika pemutaran gagal karena masalah seperti kebijakan browser, perlu penanganan dengan `.catch()`. |
| `.pause()`              | Metode yang digunakan untuk menghentikan sementara pemutaran audio atau video yang sedang berjalan. Berbeda dengan `.stop()`, metode ini hanya menghentikan sementara, sehingga pemutaran bisa dilanjutkan dari titik terakhir. |
| `.remove()`             | Metode yang digunakan untuk menghapus elemen dari DOM secara langsung tanpa perlu merujuk ke elemen induk. Berguna dalam manipulasi DOM ketika elemen sudah tidak diperlukan lagi, misalnya saat menutup modal atau menghapus item dari daftar. |
| `.sort()`               | Metode array yang digunakan untuk mengurutkan elemen dalam array berdasarkan kondisi tertentu. Secara default, metode ini mengurutkan elemen sebagai string dalam urutan leksikografis (sesuai kode ASCII). Untuk sorting angka atau kriteria lain, kita bisa menggunakan fungsi perbandingan sebagai argumen. Metode ini mengubah array asli. |
| `.filter()`             | Metode array yang membuat array baru yang hanya berisi elemen-elemen yang memenuhi kondisi dalam callback function. Metode ini tidak mengubah array asli, tetapi mengembalikan array baru yang berisi elemen yang lolos filter. Cocok digunakan untuk menyaring data berdasarkan kondisi tertentu. |
| `.forEach()`            | Metode array yang mengeksekusi fungsi callback untuk setiap elemen dalam array tanpa mengembalikan nilai. Metode ini sering digunakan untuk iterasi dan manipulasi elemen dalam array, tetapi tidak bisa menghentikan iterasi lebih awal seperti `for` loop. |
| `.map()`                | Metode array yang membuat array baru dengan hasil pemanggilan fungsi callback pada setiap elemen dalam array asli. Berbeda dengan `.forEach()`, metode ini mengembalikan array baru dengan elemen yang sudah dimodifikasi, sehingga cocok untuk transformasi data. |

## Example Usage

### `new Audio()`
```javascript
const sound = new Audio('sound.mp3');
sound.play(); // Memutar audio
sound.volume = 0.5; // Mengatur volume ke 50%
```

### `.find()`
```javascript
const numbers = [10, 20, 30, 40];
const result = numbers.find(num => num > 25);
console.log(result); // 30
```

### `?.` (Optional Chaining)
```javascript
const user = { profile: { name: "Alice" } };
console.log(user?.profile?.name); // "Alice"
console.log(user?.address?.city); // undefined (tanpa error)
```

### `.play()` dan `.pause()`
```javascript
const music = new Audio('music.mp3');
music.play().then(() => {
  console.log("Musik sedang diputar");
}).catch(error => {
  console.log("Gagal memutar musik", error);
});
setTimeout(() => music.pause(), 5000); // Pause setelah 5 detik
```

### `.remove()`
```javascript
const element = document.getElementById("myElement");
element.remove(); // Menghapus elemen dari DOM
```

### `.sort()`
```javascript
const fruits = ["banana", "apple", "cherry"];
fruits.sort();
console.log(fruits); // ["apple", "banana", "cherry"]

const numbers = [5, 2, 10, 1];
numbers.sort((a, b) => a - b); // Mengurutkan angka secara numerik
console.log(numbers); // [1, 2, 5, 10]
```

### `.filter()`
```javascript
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // [2, 4]
```

### `.forEach()`
```javascript
const names = ["Alice", "Bob", "Charlie"];
names.forEach(name => console.log(name));
```

### `.map()`
```javascript
const numbers = [1, 2, 3];
const squared = numbers.map(num => num * num);
console.log(squared); // [1, 4, 9]
```
