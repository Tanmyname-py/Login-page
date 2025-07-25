Tentu! Saya akan **menjelaskan kode CSS** yang Anda berikan secara lengkap dan **membuat panduan belajar** agar Anda bisa memahami dan menulis kode seperti ini dengan mudah.

---

## 🧾 Penjelasan Lengkap Kode CSS

### 1. **Import Font**

```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;...&display=swap');
```

* Mengimpor font **Poppins** dari Google Fonts.
* Digunakan untuk seluruh elemen di halaman.

---

### 2. **Reset dan Styling Global**

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', 'sans-serif';
}
```

* Menghapus margin & padding default browser.
* `box-sizing: border-box` → ukuran elemen termasuk padding dan border.
* Atur font default ke `Poppins`.

---

### 3. **Section - Latar Belakang**

```css
section {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100vh;
  background: url('bg.jpg') no-repeat;
  background-position: center;
  animation: animateBg 5s linear infinite;
}
```

* **Layout:** menggunakan Flexbox untuk menempatkan isi ke tengah secara horizontal & vertikal.
* **Ukuran:** memenuhi seluruh layar (`100vh`).
* **Background:** gambar `bg.jpg`, tidak mengulang, dan di tengah.
* **Animasi:** memutar warna (`hue-rotate`) secara terus menerus.

---

### 4. **Animasi Filter Warna**

```css
@keyframes animateBg {
  100% {
    filter: hue-rotate(360deg);
  }
}
```

* Efek warna latar belakang berputar 360 derajat secara halus.

---

### 5. **Kotak Login**

```css
.login-box {
  width: 400px;
  height: 400px;
  background: transparent;
  border-radius: 20px;
  border: 2px solid rgba(255,255,255,.5);
  display: flex;
  justify-content: center;
  align-items: center;
  backdrop-filter: blur(15px);
}
```

* **Ukuran tetap:** 400x400 piksel.
* **Desain kaca buram:** `backdrop-filter: blur(15px)` dan border semi-transparan.
* **Posisi tengah isi:** `flex`.

---

### 6. **Judul Form**

```css
h2 {
  font-size: 2em;
  color: #fff;
  text-align: center;
}
```

* Teks besar dan putih, rata tengah.

---

### 7. **Input Box**

```css
.input-box {
  width: 310px;
  margin: 30px 0;
  border-bottom: 2px solid #fff;
  position: relative;
}
```

* Input dibungkus dengan border bawah putih.
* Posisi relatif agar label dan ikon bisa diposisikan absolut.

---

### 8. **Label**

```css
.input-box label {
  position: absolute;
  top: 50%;
  left: 5px;
  transform: translateY(-50%);
  transition: .5s;
  color: #fff;
}
```

* Label berada di dalam input (placeholder style).
* Saat user mengetik / focus, label naik ke atas:

```css
.input-box input:focus~label,
.input-box input:valid~label {
  top: -5px;
}
```

---

### 9. **Input Field**

```css
.input-box input {
  background: transparent;
  border: none;
  outline: none;
  color: #fff;
  font-size: 1em;
  padding: 0 35px 0 5px;
}
```

* Input transparan & teks putih.

---

### 10. **Ikon dalam Input**

```css
.input-box .icon {
  position: absolute;
  right: 8px;
  color: #fff;
  font-size: 1.2em;
}
```

* Diletakkan di kanan input menggunakan posisi absolut.

---

### 11. **Checkbox dan Lupa Password**

```css
.remember-forgot {
  display: flex;
  justify-content: space-between;
  font-size: .9em;
  color: #fff;
}
```

* Terdiri dari checkbox "Remember me" dan link "Forgot password?".
* Hover link menjadi underline.

---

### 12. **Tombol Login**

```css
button {
  width: 100%;
  height: 40px;
  background: #fff;
  color: #000;
  border-radius: 40px;
  font-weight: 500;
  cursor: pointer;
}
```

* Tombol putih, teks hitam, membulat penuh (pill shape).

---

### 13. **Tautan Registrasi**

```css
.register-link {
  text-align: center;
  font-size: .9em;
  color: #fff;
  margin: 25px 0 10px;
}
.register-link a:hover {
  text-decoration: underline;
}
```

---

### 14. **Responsif di HP Kecil**

```css
@media (max-width: 360px) {
  .login-box {
    width: 100%;
    height: 100vh;
    border: none;
    border-radius: 0;
  }
  .input-box {
    width: 290px;
  }
}
```

* Jika layar sangat kecil (≤360px), login-box menyesuaikan layar penuh dan tanpa border radius.

---

## 📘 Panduan Belajar Agar Bisa Memahami Kode Ini

Berikut alur belajar bertahap yang disarankan:

---

### 🔹 **Level 1: Dasar CSS**

1. **Pahami selector dasar**: `*`, `div`, `.class`, `#id`
2. **Properti umum**: `margin`, `padding`, `color`, `background`, `font-family`
3. **Box model** dan `box-sizing`
4. Gunakan situs seperti:

   * [W3Schools CSS Tutorial](https://www.w3schools.com/css/)
   * [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS)

---

### 🔹 **Level 2: Layout & Responsif**

1. **Flexbox**:

   * Properti: `display: flex`, `justify-content`, `align-items`
   * Latihan: [Flexbox Froggy](https://flexboxfroggy.com/)
2. **Media queries**:

   * Belajar membuat tampilan responsif untuk HP/tablet.

---

### 🔹 **Level 3: Animasi dan Efek Visual**

1. Belajar:

   * `@keyframes`
   * `transition`
   * `transform`
   * `filter`
2. Eksperimen dengan `backdrop-filter`, efek blur, dan transparansi.

---

### 🔹 **Level 4: Struktur Proyek & Integrasi HTML**

Pelajari bagaimana CSS ini terhubung dengan **HTML** dan **ikon** (seperti dari Font Awesome atau Bootstrap Icons).

Contoh HTML dasar:

```html
<section>
  <div class="login-box">
    <form>
      <h2>Login</h2>
      <div class="input-box">
        <span class="icon">🔒</span>
        <input type="password" required>
        <label>Password</label>
      </div>
      <div class="remember-forgot">
        <label><input type="checkbox"> Remember me</label>
        <a href="#">Forgot Password?</a>
      </div>
      <button type="submit">Login</button>
      <div class="register-link">
        <p>Don't have an account? <a href="#">Register</a></p>
      </div>
    </form>
  </div>
</section>
```

---

### 🎯 Kesimpulan

Dengan rutin latihan dan mencoba contoh proyek kecil seperti login form ini, Anda akan bisa:

* Membuat desain modern
* Mengerti struktur HTML + CSS
* Menerapkan animasi & responsif

---

Jika Anda mau, saya bisa bantu **buatkan HTML lengkap** yang cocok dengan CSS di atas untuk langsung Anda coba dan eksperimen. Mau?
