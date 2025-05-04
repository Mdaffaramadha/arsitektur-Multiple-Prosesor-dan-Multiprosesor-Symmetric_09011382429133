# Arsitektur Multiple Prosesor dan Multiprosesor Symmetric

- ***Multiple Prosesor***

1. CPU (Central Processing Unit)
   
Terdapat empat CPU yang masing-masing merupakan prosesor utama yang bekerja secara paralel. Setiap CPU dapat mengerjakan tugas sendiri atau bekerja sama dalam pemrosesan data. Ini adalah inti dari sistem multiprosesor.

2. Cache Memory
   
Masing-masing CPU memiliki cache memory sendiri. Cache ini adalah memori kecil berkecepatan tinggi yang digunakan untuk menyimpan data atau instruksi yang sering digunakan, agar CPU dapat mengaksesnya dengan cepat tanpa harus mengambilnya dari memori utama.

3. Disk Controller & Disk
   
Ini adalah komponen yang menghubungkan sistem multiprosesor dengan media penyimpanan (harddisk). Disk controller mengatur bagaimana data dibaca dan ditulis ke dalam disk.

4. Network Controller & Network
   
Berfungsi untuk menghubungkan sistem ke jaringan, sehingga bisa berkomunikasi dengan komputer lain. Network controller mengatur lalu lintas data dari dan ke jaringan.

5. Bus
    
Bus merupakan jalur komunikasi utama yang menghubungkan seluruh komponen: CPU, cache, memory, disk, dan jaringan. Semua transfer data antar komponen terjadi melalui bus ini.

6. Main Memory (Memori Utama)
    
Ini adalah RAM yang digunakan untuk menyimpan data dan instruksi program yang sedang dijalankan. Semua CPU dapat mengakses memori utama ini secara bersama-sama.






![Image](https://github.com/user-attachments/assets/97fb3062-4a02-44b1-aca0-c187e69fded8)





Kesimpulan:

Arsitektur multiple prosesor adalah desain sistem komputer yang menggunakan lebih dari satu unit pemrosesan pusat (CPU) untuk menjalankan berbagai proses secara bersamaan. Dalam sistem ini, setiap CPU memiliki cache memory sendiri yang berfungsi sebagai penyimpanan sementara berkecepatan tinggi untuk mempercepat akses data dan instruksi. Semua CPU tersebut terhubung satu sama lain dan ke komponen utama lainnya seperti memori utama (RAM), disk, serta jaringan melalui satu jalur komunikasi bersama yang disebut bus.

Penggunaan arsitektur ini memberikan banyak keunggulan, terutama dalam hal kinerja dan efisiensi pemrosesan. Dengan adanya banyak CPU, sistem dapat membagi tugas menjadi beberapa bagian dan menjalankannya secara paralel, sehingga pekerjaan selesai lebih cepat dibandingkan sistem dengan satu prosesor. Ini sangat bermanfaat untuk sistem yang membutuhkan daya komputasi besar seperti server, superkomputer, dan aplikasi berat yang memerlukan pemrosesan data dalam jumlah besar secara cepat, seperti pengolahan video, rendering grafis, simulasi ilmiah, hingga kecerdasan buatan (AI).

Selain peningkatan kinerja, arsitektur multiple prosesor juga meningkatkan keandalan dan kestabilan sistem. Jika satu CPU mengalami gangguan, CPU lain masih dapat melanjutkan proses, asalkan sistem mendukung pengelolaan beban kerja secara dinamis. Namun, untuk mengoptimalkan pemanfaatan sistem ini, dibutuhkan perangkat lunak (sistem operasi dan aplikasi) yang mampu mengatur distribusi tugas ke tiap CPU secara efisien.

Dengan kata lain, arsitektur multiple prosesor adalah solusi teknologi modern untuk memenuhi kebutuhan komputasi tingkat tinggi yang menuntut kecepatan, efisiensi, dan stabilitas dalam satu sistem yang terintegrasi.



- ***Multiprosesor Symmetric***


Penjelasan Arsitektur Multiprosesor Symmetric (SMP)

Arsitektur Multiprosesor Symmetric (SMP) adalah sistem komputer yang memiliki lebih dari satu unit pemrosesan (CPU) yang bekerja secara paralel dan setara. Setiap CPU dalam sistem ini memiliki akses yang sama terhadap semua sumber daya seperti memori utama dan perangkat input/output.

Komponen-Komponen Utama:

1. CPU (Central Processing Unit)

Beberapa CPU bekerja secara bersamaan dan saling berbagi tugas. Semua CPU memiliki kedudukan yang setara, tidak ada yang menjadi pusat kendali. Semua dapat menjalankan proses dan mengakses memori maupun perangkat input/output.

2. Local Memory

Setiap CPU dilengkapi dengan memori lokal. Fungsi dari memori lokal adalah untuk menyimpan data atau instruksi sementara agar proses dapat berjalan lebih cepat. Meski memiliki memori lokal, semua CPU tetap bisa mengakses memori utama.

3. Main Memory (Memori Utama)

Merupakan tempat penyimpanan utama yang dapat diakses oleh seluruh CPU. Digunakan untuk menyimpan data dan instruksi yang dibutuhkan oleh sistem secara umum.

4. System Bus

Jalur komunikasi yang menghubungkan semua CPU, memori utama, dan perangkat input/output. Semua pertukaran data antar komponen dilakukan melalui bus ini. Karena digunakan bersama, penggunaan bus yang terlalu padat bisa menyebabkan keterlambatan akses data.

5. I/O Device (Perangkat Input/Output)

Semua perangkat seperti keyboard, mouse, printer, dan jaringan terhubung ke sistem dan bisa diakses oleh setiap CPU melalui bus.

6. Bus Controller

Komponen yang mengatur lalu lintas data di jalur komunikasi (bus). Berfungsi mencegah konflik dan memastikan bahwa data bisa mengalir dengan teratur saat lebih dari satu CPU ingin mengakses sumber daya yang sama.

![Image](https://github.com/user-attachments/assets/70967141-bdd4-4d2b-9b3a-1e6593d9725e)


Kesimpulan:

Arsitektur multiprosesor symmetric (SMP) adalah sistem komputer yang menggunakan beberapa CPU yang bekerja secara bersamaan dan memiliki akses yang setara ke memori utama dan perangkat I/O. Tujuan utama arsitektur ini adalah untuk meningkatkan kinerja sistem melalui pemrosesan paralel. Dengan membagi beban kerja ke beberapa prosesor, sistem dapat menyelesaikan tugas lebih cepat dan efisien. Namun, karena semua komponen menggunakan satu jalur komunikasi (bus), performa bisa terhambat jika terlalu banyak CPU yang aktif secara bersamaan. Arsitektur ini cocok digunakan untuk aplikasi yang membutuhkan daya komputasi tinggi seperti server dan sistem multitasking berat.


***Perbedaan Utama Arsitektur Multiple Prosesor dan Multiprosesor Symmetric (SMP):***

Arsitektur Multiple Prosesor merupakan sistem dengan banyak CPU yang bisa memiliki fungsi berbeda atau setara, tergantung desainnya. Akses memori bisa dibagi atau terdistribusi, dan komunikasi antar CPU bisa melalui jalur khusus. Sementara itu, arsitektur Multiprosesor Symmetric (SMP) adalah sistem dengan beberapa CPU yang memiliki hak dan fungsi yang setara, dan semuanya berbagi akses yang sama ke memori utama serta perangkat I/O melalui satu system bus. SMP lebih sederhana namun memiliki keterbatasan dalam skalabilitas karena satu jalur komunikasi digunakan bersama. Intinya, perbedaan terletak pada akses memori, hubungan antar CPU, dan cara komunikasi data antar komponen.
