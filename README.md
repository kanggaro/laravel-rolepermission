## Tugas 13 - Laravel Multi Role Application
### IDENTITAS
NRP | Nama
-|-
5025201028 | Muhammad Abror Al Qushoyyi

### Link Youtube 
- [MultiRole Application](https://youtu.be/2mYDdAVLSw8)

### Deskripsi Singkat :
Aplikasi ini di desain memiliki permission sesuai dengan rolenya masing masing dengan menggunakan laravel 8
Peran dan permission dibuat beberapa jenis pengguna dengan peran dan izin berbeda, maksudnya beberapa pengguna hanya melihat daftar modul item, beberapa pengguna juga dapat mengedit modul item, untuk menghapus dan lain-lain.<br>
<br>
Dalam contoh ini terdapat tiga modul seperti yang tercantum di bawah ini:
- manajemen pengguna
- Manajemen Peran
- Manajemen Produk
<br>
Setelah mendaftarkan pengguna, Anda tidak memiliki peran apa pun, sehingga Anda dapat mengedit detail Anda dan menetapkan peran admin untuk Anda dari Manajemen Pengguna. Setelah itu Anda dapat membuat peran Anda sendiri dengan izin seperti daftar peran, pembuatan peran, edit peran, hapus peran, daftar produk, pembuatan produk, edit produk, hapus produk. Anda dapat memeriksa dengan menetapkan pengguna baru dan memeriksanya.

### Berdasarkan clean architecture
+ Entitas apa saja yang terlibat didalam aplikasi tersebut
    - Entitas utama yang terlibat antara lain : users, products, roles, permission, role_has_permissions, model_has_permissions, password_resets, personal_acces_tokens, migrations
    - Berikut design database dari laravel multi role application
	![Design Database](https://github.com/kanggaro/laravel-rolepermission/assets/90663373/87ff6757-1bbb-4049-81b5-28519cafdda3)
    
+ Usecase
	- Role Management dapat melakukan create new role, show role, Edit role, dan delete role
	- User Management dapat melakukan create new user, Show detail User, Edit User, dan delete user
	- Product dapat melakukan create new product, show detail product, edit product, dan delete product
+ Controller, Middleware dan Library tambahan beserta fungsinya
	- Paket Spatie untuk mengatur middleware dari role dan permission secara lebih sederhana
	- Seeder untuk permission sesuai dengan rolenya
	- product migration digunakan untuk table product
+ DB, external interfaces: struktur tabel database yang digunakan.
	- menggunakan composer
	- DB yang digunakan import dari `php artisan migrate`
