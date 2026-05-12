# Explaining The Commit

## Experiment 1.2
Pada experiment 1.2, saya menambahkan beberapa kalimat "Muhathir's Computer: Add such a sentence" setelah spawner. Hasilnya adalah kalimat tersebut muncul sebelum "howdy!". Hal ini menunjukkan bahwa di thread utama, spawner menjalankan task secara *asynchronous* akan tereksekusi eksekutor dari antrean sesudah kode yang secara *synchronous* tereksekusi di thread utama.