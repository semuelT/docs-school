---
tags:
  - Catatan
title: Psudocode
---
Psudocode *(kode semu)* adalah suatu bahasa buatan manusia yang sifatnya informal sebagai representasi algoritma. *Psudocode* dibuat untuk menutupi kekurangan [[./Diagram alir|Diagram alir]] dalam merepresentasikan konsep konsep pemrograman ter-struktur. *Psudocode* memungkinkan representasi langkah langkah yang lebih detail dan dekat bahasa pemrograman. *Psudocode* menggunakan sistem pernyataan per baris dan indentasi untuk menunjukan struktur.

## Aktivitas Terkait
![[../Media/Aktivitas AP-K10-01-U.png|Aktivitas AP-K10-01-U.png]]
## Kasus Penggunaan:
```
Mesin Pembayaran Bakso
```
```mermaid
flowchart TB
	in([START]) --> re["BACA Jumlah Uang dan Total Bayar"] 
	re --> op[Apakah Jumlah Uang >= Total Bayar]
	op --> rs1[Iya]
	op --> rs2[Tidak]
	rs1 --> en1([Tunjukkan Kembalian])
	rs2 --> en2([Pembayaran Gagal])
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