- Nama: Acik Imtia Chana
- NIM: 235150701111038
- Kelas: TI-C

Aplikasi menggunakan Retrofit
- Data: https://jsonplaceholder.typicode.com/posts

1. Menambahkan Dependency di build.gradle(:app)
   ![image](https://github.com/user-attachments/assets/49257d21-4b9c-40cd-b1f5-9d12d3c7bd1e)

3. Membuat model data Post.kt -> Model Data
   ![image](https://github.com/user-attachments/assets/165718b9-6baa-4371-9d7d-9744f6b6cb5f)

5. Membuat Retrofit: ApiService.kt -> Interface Retrofit
   ![image](https://github.com/user-attachments/assets/b658bd9f-5e4d-4d99-af94-a1fa0cce627f)

7. Melengkapi MainActivity.kt -> Menampilkan list post
   ![image](https://github.com/user-attachments/assets/184a00f2-9cd0-4c38-91e6-3a9828d1bcca)

9. Membuat Adapter: PostAdapter.kt ->  Adapter untuk RecyclerView
    ![image](https://github.com/user-attachments/assets/f0e1158f-940f-45c9-a436-dd03c424e40a)

11. Membuat Detail: DetailActivity.kt -> Menampilkan detail post yang diklik
    ![image](https://github.com/user-attachments/assets/8ef9e75e-c007-491e-a105-72968492963d)



Layout XML
1. activity_main.xml
   ![image](https://github.com/user-attachments/assets/9cb4c15e-7081-446f-8cfc-8c8494b699fc)
   Penjelasan:
   File activity_main.xml digunakan sebagai layout utama untuk halaman pertama (MainActivity). Layout ini menampilkan daftar data post yang diambil dari API serta informasi identitas pengguna (nama dan NIM) di bagian atas halaman. Umumnya, file ini menggunakan LinearLayout vertikal agar elemen-elemen seperti TextView dan RecyclerView tersusun dari atas ke bawah. TextView pertama digunakan untuk menampilkan nama dan NIM pengguna, sedangkan RecyclerView berfungsi untuk menampilkan daftar post yang diambil dari endpoint https://jsonplaceholder.typicode.com/posts. Nantinya, setiap item pada daftar ini akan menggunakan layout dari file item_post.xml.

3. item_post.xml
   ![image](https://github.com/user-attachments/assets/2aa90613-814d-4b00-b702-d5ff974064a4)
   Penjelasan:
   item_post.xml adalah layout yang digunakan sebagai tampilan untuk setiap item di dalam RecyclerView. Layout ini biasanya dibungkus menggunakan CardView untuk memberikan tampilan kotak dengan efek bayangan yang lebih menarik. Di dalam CardView, terdapat TextView yang digunakan untuk menampilkan judul post (title) dari data yang didapat melalui Retrofit. File ini akan digunakan berulang kali oleh PostAdapter untuk menampilkan semua data post dalam bentuk daftar scrollable.

5. activity_detail.xml
   ![image](https://github.com/user-attachments/assets/f244eb0e-e570-4cdc-87da-106c0ca4e1f1)
   Penjelasan:
   activity_detail.xml digunakan untuk halaman kedua (DetailActivity) yang muncul saat salah satu item di RecyclerView diklik. Layout ini menampilkan detail lengkap dari post yang dipilih, terdiri atas nama dan NIM pengguna, judul post, dan isi lengkap dari post (body). Agar tampilan tetap nyaman ketika konten post cukup panjang, layout utama biasanya dibungkus menggunakan ScrollView, lalu di dalamnya digunakan LinearLayout vertikal untuk menyusun semua elemen TextView. TextView pertama menampilkan informasi identitas (nama dan NIM), TextView kedua menampilkan title, dan TextView ketiga menampilkan isi body dari post yang diklik.


