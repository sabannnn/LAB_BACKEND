#LAPORAN LAB BACKEND

##1.PENDAHULUAN
Proyek ini dikembangkan menggunakan framework Nest.js, sebuah framework progresif berbasis Node.js yang dirancang untuk membangun aplikasi server-side yang efisien, andal, dan scalable. NestJS dikembangkan dengan dukungan penuh terhadap TypeScript dan menggabungkan prinsip Object-Oriented Programming (OOP), Functional Programming (FP), dan Functional Reactive Programming (FRP). Arsitektur yang terstruktur dan modular memudahkan pengembangan aplikasi yang maintainable dan scalable.
###Tujuan dan Fitur Proyek
Dalam proyek ini, NestJS digunakan untuk membangun aplikasi backend dengan tiga fitur utama:
-Chat Real-Time: Menggunakan WebSocket untuk komunikasi instan.
-Manajemen Profil Pengguna: untuk pengelolaan data pengguna yang terstruktur.
-Sistem Autentikasi yang Aman:Mengontrol akses ke dalam sistem menggunakan JWT.
###Keunggulan NestJS
1. Arsitektur Terstruktur dengan Konsep Modular
NestJS membagi aplikasi ke dalam modul, controller, dan service. Setiap modul bertanggung jawab atas fitur spesifik, misalnya:
•	AuthModule untuk autentikasi.
•	ChatModule untuk komunikasi real-time.
•	UserModule untuk pengelolaan data pengguna.
Controller menangani routing HTTP/WebSocket, sedangkan service mengelola logika bisnis. Struktur ini meningkatkan keterbacaan kode dan memungkinkan pengembangan fitur baru tanpa mengganggu kode yang sudah ada.
2. Dependency Injection (DI) yang Powerful
NestJS menyediakan sistem Dependency Injection (DI) yang memungkinkan komponen untuk saling bergantung dengan lebih fleksibel. Contoh: ChatService bisa di-inject ke dalam ChatController tanpa perlu inisialisasi manual. Ini mengurangi boilerplate code dan meningkatkan kemudahan dalam pengujian unit.
3. Dukungan TypeScript yang Lengkap
NestJS dirancang dengan TypeScript, yang menyediakan type checking statis untuk mencegah kesalahan umum seperti ketidaksesuaian tipe data atau properti yang tidak terdefinisi. Pada proyek ini, Prisma (ORM) menghasilkan type definitions otomatis dari skema database, memastikan konsistensi antara database dan aplikasi.

##2.STRUKTUR FOLDER
BACKEND
├── node_modules
├── prisma
│   └── schema.prisma
├── public
│   ├── backgrounds
│   ├── chats.html
│   ├── index.html
│   ├── index.css
│   ├── script.js
│   └── script2.js
├── src
│   ├── chat
│   │   ├── chat.gateway.spec.ts
│   │   ├── chat.gateway.ts
│   │   ├── chat.module.ts
│   │   └── chat.service.ts
│   ├── decorator
│   │   └── user.decorator.ts
│   ├── dto
│   │   ├── create-mahasiwa.dto.ts
│   │   ├── login-user.dto.ts
│   │   └── register-user.dto.ts
│   ├── entity
│   │   └── user.entity.ts
│   ├── guards
│   │   └── auth.guard.ts
│   ├── mahasiswa-profile
│   │   ├── (beberapa file mahasiswa-profile)
│   ├── profile
│   │   ├── profile.controller.spec.ts
│   │   ├── profile.controller.ts
│   │   ├── profile.module.ts
│   │   ├── profile.service.spec.ts
│   │   └── profile.service.ts
│   ├── socket
│   │   ├── socket.gateway.spec.ts
│   │   ├── socket.gateway.ts
│   │   ├── socket.module.ts
│   │   ├── socket.service.spec.ts
│   │   └── socket.service.ts
│   ├── app.controller.spec.ts
│   ├── app.controller.ts
│   ├── app.module.ts
│   ├── app.service.ts
│   └── auth.module.ts
│   ├── main.ts
│   └── prisma.ts
├── test
├── uploads
├── .env
├── .eslintrc.js
├── .gitignore
├── .prettierrc
├── nest-cli.json
├── package-lock.json
└── package.json
└── README.md
##3.TEKNOLOGI YANG DIGUNAKAN
1.	NestJS 
-Framework utama untuk pengembangan backend
-Menggunakan TypeScript sebagai bahasa pemrograman
-Mendukung Dependency Injection dan Decorators
-Terintegrasi dengan berbagai tools dan libraries
2.	Prisma ORM 
-Type-safe database access
-Auto-generated migrations
-Powerful query builder
-Database  PostgreSQL
3.	TypeScript 
o	Superset dari JavaScript yang menambahkan static types
o	Meningkatkan maintainability dan scalability kode
o	Memberikan developer experience yang lebih baik
4.	WebSocket 
-Implementasi komunikasi real-time
-Menggunakan socket.io untuk manajemen koneksi
5.	Authentication & Authorization 
-JWT (JSON Web Tokens) untuk authentication
-Guards untuk protection routes
-Custom decorators untuk role-based access
6.  HTML, CSS, JavaScript
   Bahasa-bahasa yang digunakan untuk membangun tampilan antarmuka pengguna (front-end), terutama file-file statis yang disimpan dalam folder public. HTML digunakan untuk struktur konten, CSS untuk styling, dan JavaScript untuk interaksi dinamis di sisi klien.
##4.INSTALASI PROYEK NEST
1.install NestJS CLI
npm i -g @nestjs/cli
2.inisialisasi proyek
nest new nama_proyek
3.masuk direktori
cd nama_proyek
4.setup swagger
npm i –save @nestjs/swagger
5.buka folder di VSCODE
code .
##5.PENJELASAN SETIAP FILE



