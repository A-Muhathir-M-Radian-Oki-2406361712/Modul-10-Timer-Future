# Explaining The Commit

## Experiment 1.2
Pada experiment 1.2, saya menambahkan beberapa kalimat "Muhathir's Computer: Add such a sentence" setelah spawner. Hasilnya adalah kalimat tersebut muncul sebelum "howdy!". Hal ini menunjukkan bahwa di thread utama, spawner menjalankan task secara *asynchronous* akan tereksekusi eksekutor yang ada di akhir main() dari antrean sesudah kode yang secara *synchronous* tereksekusi di thread utama.

## Experiment 1.3
Pada experiment 1.3, saya menambahkan beberapa spawner yg similiar dengan spawner pertama. Hasilnya adalah semua kalimat yang mencetak "howdy(ies)" muncul sebelum "done!". Hal ini menunjukkan bahwa semua task yang dijalankan oleh spawner akan tereksekusi secara *asynchronous* di thread utama secara berurutan sehingga string "done" yang dipending selama 2 detik akan dicetak setelah pencetakan "howdy(ies)" selesai. Saya juga mencoba ketika spawner tidak pernah didrop, alhasil *process* tidak akan selesai karena eksekutor terus menunggu di loop ketika antrean kosong (snippet loop eksekutor dapat dilihat di line 75 main.rs).