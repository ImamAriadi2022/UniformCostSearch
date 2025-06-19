# Implementasi Uniform Cost Search (UCS)

Proyek ini adalah implementasi algoritma **Uniform Cost Search (UCS)** dengan Python untuk menemukan jalur dengan biaya terendah dalam sebuah graf.

## ✨ Fitur

-   Menemukan jalur paling optimal (biaya terendah) dari titik awal ke tujuan.
-   Menampilkan urutan node pada jalur dan total biayanya.
-   Implementasi murni dengan Python tanpa dependensi eksternal.
-   Mudah untuk dikustomisasi dengan graf, titik awal, dan tujuan yang berbeda.

## 🚀 Panduan Penggunaan

Ikuti langkah-langkah berikut untuk menjalankan proyek ini di komputer lokal Anda.

### Prasyarat

-   [Python 3.8](https://www.python.org/downloads/) atau versi lebih baru
-   [Git](https://git-scm.com/downloads/)

### Langkah 1: Clone Repositori

Buka terminal atau Command Prompt Anda dan jalankan perintah berikut untuk mengunduh proyek:
```bash
git clone [https://github.com/ImamAriadi2022/UniformCostSearch.git](https://github.com/ImamAriadi2022/UniformCostSearch.git)
cd UniformCostSearch
```

### Langkah 2: Buat dan Aktifkan Virtual Environment

Sangat disarankan untuk menggunakan *virtual environment* agar dependensi proyek tidak tercampur dengan instalasi Python global Anda.

**Buat environment:**
```bash
python -m venv venv
```

**Aktifkan environment:**
-   **Di Windows:**
    ```bash
    .\venv\Scripts\activate
    ```
-   **Di macOS / Linux:**
    ```bash
    source venv/bin/activate
    ```
Setelah diaktifkan, Anda akan melihat `(venv)` di awal baris terminal Anda.

### Langkah 3: Buat File `requirements.txt`

Proyek ini sebenarnya tidak memiliki dependensi eksternal. Namun, dalam proyek Python pada umumnya, file `requirements.txt` digunakan untuk mendaftar semua pustaka yang dibutuhkan.

1.  Buat file baru dengan nama `requirements.txt` di dalam direktori proyek.
2.  Biarkan file ini **kosong** untuk saat ini, karena tidak ada pustaka yang perlu diinstal.

### Langkah 4: Install Dependensi (Jika Ada)

Jalankan perintah berikut. Perintah ini akan membaca file `requirements.txt` dan menginstal pustaka yang terdaftar. Karena file tersebut kosong, perintah ini tidak akan menginstal apa pun, tetapi ini adalah langkah standar yang penting.

```bash
pip install -r requirements.txt
```

### Langkah 5: Jalankan Skrip

Sekarang Anda siap menjalankan skrip utama untuk melihat algoritma UCS beraksi.

```bash
python main.py
```

Anda akan melihat output yang menunjukkan jalur dan biaya terendah berdasarkan graf yang telah didefinisikan di dalam skrip:

```
Path: S -> A -> C -> G
Cost: 7
```

## 🔧 Kustomisasi (Menggunakan Graf Anda Sendiri)

Anda dapat dengan mudah mengubah graf, titik awal, dan tujuan dengan mengedit file `main.py`.

1.  Buka file `main.py`.
2.  Ubah `graph`, `start_node`, atau `goal_node` sesuai kebutuhan Anda.

**Contoh Modifikasi:**

```python
# main.py

# ... (fungsi uniform_cost_search ada di sini) ...

if __name__ == '__main__':
    # --- UBAH DI BAGIAN INI ---

    # 1. Definisikan graf Anda
    graph = {
        'A': [('B', 5), ('C', 2)],
        'B': [('A', 5), ('D', 4)],
        'C': [('A', 2), ('D', 7), ('E', 1)],
        'D': [('B', 4), ('C', 7), ('E', 3)],
        'E': [('C', 1), ('D', 3)]
    }

    # 2. Tentukan titik awal dan tujuan
    start_node = 'A'
    goal_node = 'E'

    # --- JANGAN UBAH BAGIAN DI BAWAH ---
    path, cost = uniform_cost_search(graph, start_node, goal_node)
    print(f"Path: {' -> '.join(path)}")
    print(f"Cost: {cost}")
```

Jalankan kembali `python main.py` untuk melihat hasil dari graf baru Anda.

## 👤 Penulis

-   **Imam Ariadi** - [ImamAriadi2022](https://github.com/ImamAriadi2022)