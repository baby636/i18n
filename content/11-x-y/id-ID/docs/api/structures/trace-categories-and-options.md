# Objek TraceCategoriesAndOptions

* `categoryFilter` String - A filter to control what category groups should be traced. A filter can have an optional '-' prefix to exclude category groups that contain a matching category. Keduanya disetakan dan mengecualikan pola kategori dalam satu daftar yang sama tidak dapat dilakukan. Contoh: `test_MyTest*`, `test_MyTest*,test_OtherStuff`, `-excluded_category1,-excluded_category2`.
* `traceOptions` String - Mengontrol jenis pelacakan apa yang diaktifkan, urutan yang dipisahkan koma dari string berikut: `record-until-full`, `record-continuously`, `trace-to-console`, `enable-sampling`, `enable-systrace`, e.g. `'record-until-full,enable-sampling'`. 3 pilihan pertama adalah mode perekaman jejak dan karenanya saling eksklusif. Jika lebih dari satu mode perekaman jejak muncul di string ` traceOptions ` yang terakhir diutamakan. Jika tidak ada mode perekaman jejak ditentukan, mode perekaman `record-until-full`. Opsi jejak pertama-tama akan diatur ulang ke opsi default (`record_mode` diatur ke `record-until-full`, `enable_sampling` dan `enable_systrace` diatur ke `false`) sebelum opsi yang diurai dari `traceOptions` diaplikasikan.