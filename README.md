# 📌 Laporan Design Pattern 
## 📝 Raflee Caesar Dano Malik

---

## 🔌 Adapter Design Pattern

### 📌 Konsep "Adapter Design Pattern"
Adapter Design Pattern bekerja seperti penerjemah yang membantu dua pihak dengan bahasa berbeda agar bisa berkomunikasi. **Target** adalah cara standar yang diharapkan klien untuk berinteraksi, sedangkan **Adaptee** memiliki kemampuan yang dibutuhkan tetapi dengan cara yang berbeda. **Adapter** berperan sebagai jembatan yang mengubah perintah dari Target menjadi sesuatu yang bisa dipahami oleh Adaptee, sehingga klien tetap bisa menggunakan fitur yang ada tanpa perlu mengubah kode yang sudah ada.

![Adapter Design Pattern](https://github.com/user-attachments/assets/3798f760-2359-44bb-b3b2-2f9e97aa44b1)

### 📌 Class Diagram "Adapter Design Pattern"
Diagram ini menunjukkan hubungan antara kelas-kelas dalam sistem manajemen karyawan dengan pola **Adapter Design Pattern**.

- **Employee** adalah kelas utama yang menyimpan data karyawan seperti nama, posisi, tahun direkrut, gaji, dan tanggal perekrutan.
- **Manager, Intern, Engineer** adalah turunan dari Employee yang menambahkan atribut spesifik masing-masing.
- **EmployeeAdapter** bertindak sebagai perantara antara Employee dan antarmuka **IEmployee**, yang hanya memiliki metode `get_info()`.
- **Adapter** memungkinkan kelas yang sudah ada untuk digunakan dengan cara yang lebih sesuai dengan kebutuhan sistem, tanpa harus mengubah kode aslinya.

![Class Diagram - Adapter Pattern](https://github.com/user-attachments/assets/de2ea333-a0d1-463a-8450-052fe9faf0aa)

### 📌 Use Case Diagram "APP"
![Use Case Diagram - APP](https://github.com/user-attachments/assets/56d850f4-8cd8-4795-9e71-d3f6da226786)

### 📌 Sequence Diagram "Adapter Design Pattern"
Sequence diagram ini menggambarkan bagaimana sistem menangani input pengguna untuk membuat dan menampilkan informasi karyawan.

1. Pengguna memasukkan data ke dalam **Main Program**.
2. Main Program memanggil **EmployeeAdapter** untuk membuat objek karyawan melalui metode `create_employee()`.
3. **EmployeeAdapter** menginisialisasi objek **Employee** (bisa berupa **Manager, Intern, atau Engineer**) dan mengembalikannya.
4. Saat sistem membutuhkan informasi karyawan, `get_info()` dipanggil pada **EmployeeAdapter**.
5. **EmployeeAdapter** meminta `get_annual_salary()` dari objek **Employee**.
6. Setelah data dikembalikan, program menampilkan informasi karyawan kepada pengguna.

![Sequence Diagram - Adapter Pattern](https://github.com/user-attachments/assets/a5600da3-24ad-4814-810e-c746e1290d69)

---

## 🎯 Strategy Design Pattern

### 📌 Konsep "Strategy Design Pattern"
**Strategy Design Pattern** memungkinkan kita memilih algoritma atau strategi yang berbeda secara dinamis tanpa mengubah kode inti.

![Konsep Strategy Design Pattern](https://github.com/user-attachments/assets/8a1a21c6-8797-4e98-816a-f454a3a96990)

### 📌 Class Diagram "Strategy Design Pattern"
Class diagram di bawah ini menunjukkan implementasi **Strategy Design Pattern** dalam manajemen karyawan.

- **EmployeeContext** bertindak sebagai perantara yang menyimpan objek **Employee** dan strategi yang digunakan.
- **EmployeeStrategy** adalah antarmuka yang menentukan metode `get_info()`.
- **ManagerStrategy, EngineerStrategy, dan InternStrategy** adalah implementasi spesifik dari strategi tersebut.
- **Employee** adalah kelas dasar yang memiliki atribut umum, sedangkan **Manager, Engineer, dan Intern** adalah subclass yang menambahkan atribut spesifik masing-masing.

![Class Diagram - Strategy Pattern](https://github.com/user-attachments/assets/e967a281-4f17-4f0e-a4c1-a695c6d81fd6)

### 📌 Use Case Diagram "APP"
![Use Case Diagram - APP](https://github.com/user-attachments/assets/140990d1-64d8-4d7d-88f5-80da7e7f1b11)

### 📌 Sequence Diagram "Strategy Design Pattern"
Sequence diagram ini menggambarkan bagaimana **Strategy Design Pattern** bekerja dalam konteks manajemen karyawan.

1. **Client** terlebih dahulu menetapkan strategi yang akan digunakan (`set_strategy(ManagerStrategy)`) ke dalam **EmployeeContext**.
2. Saat **Client** meminta informasi karyawan (`get_employee_info()`), **EmployeeContext** meneruskan permintaan ke **EmployeeStrategy**.
3. **EmployeeStrategy** mengarahkannya ke strategi konkret, dalam hal ini **ManagerStrategy**.
4. **ManagerStrategy** mengambil informasi spesifik karyawan, termasuk menghitung gaji tahunan (`get_annual_salary()`).
5. Data yang telah diformat dikembalikan ke **EmployeeContext** dan akhirnya diterima oleh **Client**.

![Sequence Diagram - Strategy Pattern](https://github.com/user-attachments/assets/36895c84-95ba-4164-aefe-8e040edc40d5)


---

## 🖥️ CLI Apps
### 📌 Tampilan Aplikasi Command Line

![CLI Home Screen](https://github.com/user-attachments/assets/5e61e7ca-92b6-4c3d-bbe9-ce8e27d5a3f1)

![CLI Add Employee](https://github.com/user-attachments/assets/d5139071-7fc7-42db-b46d-bd3c51bea370)

![CLI View Employee](https://github.com/user-attachments/assets/a1d129ff-2d4d-4ba4-a272-7e3f81f9069c)

---



