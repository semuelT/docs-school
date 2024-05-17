# Makna setiap objek Diagram alir

## Garis Alir
```mermaid
flowchart LR
	A --> B
```
Anak panah arah yang menunjukan aliran program dair awal hingga akhir.
## Terminator
```mermaid
flowchart LR
	a(Terminator)
```
Digunakan untuk menunjukan titik awal dan akhir sebuah program/algoritma.
## Blok Proses
```mermaid
flowchart LR
a[Proses]
```
## Blok Keputusan/Control Flow
```mermaid
flowchart LR
	a{Blok Keputusan/Titik Cabang}
```
Melambangkan titik dimana program bercabang.

# Contoh contoh Diagram
## Menghitung Luas Permukaan Kubus
```mermaid
flowchart TD
	st([START]) --> read[/READ Sisi/]
	read --> cl["Luas = Sisi * Sisi"]
	cl --> cl2[Luas Permukaan = Luas * 6]
	cl2 --> out[/PRINT Luas Permukaan/]
	out --> en([END])
```