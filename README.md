; Expert-system-identifikasi-jenis-bunga-iris
; Nama : Siti Hashifah Qatrunnada
; NIM : 21/483101/TK/53401

; TUGAS AI CLIPS (Expert System Identifikasi Jenis Bunga Iris)
; Program ini akan menetukan jenis bunga iris berdasarkan kriteria yang dimasukkan, seperti petal, sepal, dan warna bunga

;Jenis Bunga Iris Setosa
(defrule setosa
(petal 1)
(sepal1 1)
(sepal2 1)
(warna 1 | 2)
=>
(printout t crlf "Bunga ini merupakan bungan Iris Setosa!" crlf crlf))

;Jenis Bunga Iris Versicolor
(defrule versicolor
(petal 2)
(sepal1 2)
(sepal2 2)
(warna 3 )
=>
(printout t crlf "Bunga ini merupakan bungan Iris Versicolor!" crlf crlf))

;Jenis Bunga Iris Virginica
(defrule virginica
(petal 3)
(sepal1 3)
(sepal2 2)
(warna 2 | 4)
=>
(printout t crlf "Bunga ini merupakan bungan Iris Virginica!" crlf crlf))

(defrule nothing1
(petal 1)
(sepal1 2 | 3)
(sepal2 1 | 2)
(warna 1| 2 | 3 | 4)
=>
(printout t crlf "Maaf, jenis bunga tidak ditemukan :( " crlf crlf))

(defrule nothing2
(petal 2)
(sepal1 1 | 3)
(sepal2 1 | 2)
(warna 1| 2 | 3 | 4)
=>
(printout t crlf "Maaf, jenis bunga tidak ditemukan :( " crlf crlf))

(defrule nothing3
(petal 3)
(sepal1 1 | 2)
(sepal2 1 | 2)
(warna 1| 2 | 3 | 4)
=>
(printout t crlf "Maaf, jenis bunga tidak ditemukan :( " crlf crlf))

(defrule nothing4
(petal 1)
(sepal1 1)
(sepal2 2)
(warna 1| 2 | 3 | 4)
=>
(printout t crlf "Maaf, jenis bunga tidak ditemukan :( " crlf crlf))

(defrule nothing5
(petal 1)
(sepal1 1)
(sepal2 1)
(warna 3 | 4)
=>
(printout t crlf "Maaf, jenis bunga tidak ditemukan :( " crlf crlf))

(defrule nothing6
(petal 2)
(sepal1 2)
(sepal2 1)
(warna 1| 2 | 3 | 4)
=>
(printout t crlf "Maaf, jenis bunga tidak ditemukan :( " crlf crlf))

(defrule nothing7
(petal 2)
(sepal1 2)
(sepal2 2)
(warna 1| 2 | 4)
=>
(printout t crlf "Maaf, jenis bunga tidak ditemukan :( " crlf crlf))

(defrule nothing8
(petal 3)
(sepal1 3)
(sepal2 1)
(warna 1| 2 | 3 | 4)
=>
(printout t crlf "Maaf, jenis bunga tidak ditemukan :( " crlf crlf))

(defrule nothing9
(petal 3)
(sepal1 3)
(sepal2 2)
(warna 1 | 3)
=>
(printout t crlf "Maaf, jenis bunga tidak ditemukan :( " crlf crlf))

(defrule input
(initial-fact)
=>
(printout t crlf "Program ini akan menentukan jenis bunga Iris :)

Masukkan kriteria bunga
Berapa panjang petal(daun mahkota)?
1: 1-2cm
2: 4-5cm
3: 6-7cm 
-> ")
(assert (petal =(read)))

(printout t crlf "panjang sepal(daun kelopak)? 
1: pendek
2: sedang
3: panjang 
-> ")
(assert (sepal1 =(read)))

(printout t crlf "ketebalan sepal(daun kelopak)? 
1: lebar 
2: tipis 
-> ")
(assert (sepal2 =(read)))

(printout t crlf "warna bunga?
1: putih
2: merah muda dengan bercak-bercak ungu
3: ungu atau biru keunguan
4: ungu tua
-> ")
(assert (warna =(read)))
(printout t crlf "Jenis bunga:" ))
