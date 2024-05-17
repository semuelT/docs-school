---
tags:
  - Catatan
share: "true"
---
Psudocode *(kode semu)* adalah suatu bahasa buatan manusia yang sifatnya informal sebagai representasi algoritma. *Psudocode* dibuat untuk menutupi kekurangan diagram alir dalam merepresentasikan konsep konsep pemrograman ter-struktur. *Psudocode* memungkinkan representasi langkah langkah yang lebih detail dan dekat bahasa pemrograman. *Psudocode* menggunakan sistem pernyataan per baris dan indentasi untuk menunjukan struktur.

## Kasus Penggunaan:
	Mesin Pembayaran Bakso
`Diagram Alir`
```mermaid
flowchart TB
	in[(Input)] --- in1[Total Bayar] 
	in[(Input)] --- in2[Jumlah Uang]
	in1 --> op1[Apakah Jumlah Uang >= Total Bayar]
	in2 --> op1[Apakah Jumlah Uang >= Total Bayar]
	op1 --> rs1[Iya]
	op1 --> rs2[Tidak]
	rs1 --> en1[[Tunjukkan Kembalian]]
	rs2 --> en2[[Pembayaran Gagal]]
```

`Kode Python`
```python
total_bayar = 150
print("Total pembayaran adalah", total_bayar)
jumlah_uang = 100

if total_bayar == jumlah_uang:
	print("Pembayaran berhasil!")
elif jumlah_uang <= total_bayar:
	print("Uang anda tidak cukup!")
else:
	print("Pembayaran berhasil! Kembalian:", jumlah_uang-total_bayar)
```