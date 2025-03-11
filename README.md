# music-player

## Table of JavaScript Methods

| Method/Operator    | Description |
|-------------------|-------------|
| `new Audio()`     | Membuat objek audio baru untuk memutar suara di browser. |
| `.find()`         | Mencari elemen pertama dalam array yang memenuhi kondisi tertentu. |
| `?.` (Optional Chaining) | Mengakses properti atau metode dari objek secara aman tanpa error jika objek tersebut `null` atau `undefined`. |
| `.play()`         | Memulai pemutaran audio atau video. |
| `.pause()`        | Menghentikan sementara pemutaran audio atau video. |
| `.remove()`       | Menghapus elemen dari DOM. |
| `.sort()`         | Mengurutkan elemen dalam array. Secara default berdasarkan urutan Unicode. |
| `.filter()`       | Membuat array baru dengan elemen yang memenuhi kondisi tertentu. |
| `.forEach()`      | Menjalankan fungsi tertentu untuk setiap elemen dalam array. |
| `.map()`          | Membuat array baru dengan hasil dari pemanggilan fungsi pada setiap elemen array lama. |

## Example Usage

### `new Audio()`
```javascript
const sound = new Audio('audio.mp3');
sound.play();
```

### `.find()`
```javascript
const numbers = [10, 20, 30, 40];
const result = numbers.find(num => num > 25);
console.log(result); // 30
```

### `?.` (Optional Chaining)
```javascript
const user = { profile: { name: 'John' } };
console.log(user.profile?.name); // 'John'
console.log(user.address?.city); // undefined, tidak error
```

### `.play()` and `.pause()`
```javascript
const audio = new Audio('song.mp3');
audio.play();
setTimeout(() => audio.pause(), 5000); // Pause setelah 5 detik
```

### `.remove()`
```javascript
const element = document.getElementById('myElement');
element.remove();
```

### `.sort()`
```javascript
const fruits = ['banana', 'apple', 'cherry'];
fruits.sort();
console.log(fruits); // ['apple', 'banana', 'cherry']
```

### `.filter()`
```javascript
const ages = [18, 22, 15, 30];
const adults = ages.filter(age => age >= 18);
console.log(adults); // [18, 22, 30]
```

### `.forEach()`
```javascript
const colors = ['red', 'blue', 'green'];
colors.forEach(color => console.log(color));
```

### `.map()`
```javascript
const numbers = [1, 2, 3];
const squares = numbers.map(num => num * num);
console.log(squares); // [1, 4, 9]
```
