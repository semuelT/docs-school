# Menghitung Luas Permukaan Kubus
```mermaid
flowchart TD
	subgraph Flowchart
	start([Start]) --> read[/READ Sisi/]
	read --> calc1(Luas = Sisi * Sisi)
	calc1 --> calc2(Luas_Permukaan = Sisi * 6)
	calc2 --> print[/PRINT Luas_Permukaan/]
	print --> enD([END])
	end
	subgraph Contoh
	start2([Start]) --> read2[/READ Sisi/]
	read2 -- 20 --> calc12(Luas = Sisi * Sisi)
	calc12 -- 400 --> calc22(Luas_Permukaan = Sisi * 6)
	calc22 -- 2400 --> print2[/PRINT Luas_Permukaan/]
	print2 -- 2400 --> enD2([END])
	end
```
# Membagi Bilangan
```mermaid
flowchart TD
	subgraph Flowchart
	start([START]) --> read[/READ Pembilang Penyebut/]
	read --> des{Penyebut = 0?}
	des -- Tidak --> calc(Hasil = Pembilang ÷ Penyebut)
	des -- Ya --> disallow[/PRINT Penyebut tidak boleh Nol/]
	calc --> result[/PRINT Hasil/]
	result --> enD([END])
	disallow --> enD
	end
	subgraph Kasus A
	startA([START]) --> readA[/READ Pembilang Penyebut/]
	readA -- 10, 2--> desA{Penyebut = 0?}
	desA -- Tidak (2 > 0) --> calcA(Hasil = Pembilang ÷ Penyebut)
	calcA -- 5 --> resultA[/PRINT Hasil/]
	desA --x disallowA[/PRINT Penyebut tidak boleh Nol/]
	resultA -- 5 --> enDA([END])
	disallowA --> enDA
	end
	subgraph Kasus B
	startB([START]) --> readB[/READ Pembilang Penyebut/]
	readB -- 8, 0--> desB{Penyebut = 0?}
	desB -- Tidak --> calcB(Hasil = Pembilang ÷ Penyebut)
	desB -- Ya (0 = 0)--> disallowB[/PRINT Penyebut tidak boleh Nol/]
	calcB --> resultB[/PRINT Hasil/]
	resultB --> enDB([END])
	disallowB -- Penyebut tidak boleh Nol --> enDB
	end
```
# Menghitung Mundur dari N hingga 1
```mermaid
flowchart TD
	subgraph Flowchart
	start([START]) --> read[/READ N/]
	read --> des{N = 0}
	des -- Ya --> printN[/PRINT N/]
	printN --> decrementN(N=N-1)
	decrementN --> des
	des -- Tidak --> enD([END])
	end
	subgraph Contoh
	startA([START]) --> readA[/READ N/]
	readA -- 5 --> desA{N = 0}
	desA -- Ya (N > 0) --> printNA[/PRINT N/]
	printNA -- 5;4;3;2;1 --> decrementNA(N=N-1)
	decrementNA --> desA
	desA -- Tidak --> enDA([END])
	end
```

# Mencari Bilangan Terbesar dari Suatu Himpunan Bilangan
```mermaid
flowchart TD
	subgraph Flowchart
	start([START]) --> read[/READ N/]
	read --> var1(Terbesar = 0)
	var1 --> des{N = Bilangan.length}
	des -- Ya --> printN[/PRINT Terbesar/]
	des -- Tidak --> read1[/READ Bilangan/]
	read1 --> des1{Terbesar < Bilangan}
	des1 -- Ya --> asgn(Terbesar = Bilangan)
	asgn --> decrementN(N = N-1)
	des1 -- Tidak --> decrementN
	decrementN --> des
	printN --> enD([END])
	end
	subgraph "Contoh (Set = [3, 1, 2, 4, 5, 7, 9])"
	startA([START]) --> readA[/READ N/]
	readA -- 3, 1, 2, 4, 5, 7, 9 --> var1A(Terbesar = 0)
	var1A --> desA{N = Bilangan.length}
	desA -- Ya --> printNA[/PRINT Terbesar/]
	desA -- Tidak --> read1A[/READ Bilangan/]
	read1A -- 3, 1, 2, 4, 5, 7, 9 --> des1A{Terbesar < Bilangan}
	des1A -- Ya (3;4;5;7;9) --> asgnA(Terbesar = Bilangan)
	asgnA --> decrementNA(N = N-1)
	des1A -- Tidak (1; 2) --> decrementNA
	decrementNA --> desA
	printNA -- 9 --> enDA([END])
	end
```
> [!tip]
> *Semicolon (;) berarti akhir baris atau Iterasi.*

> Diatas menggunakan `Bilangan.length` karena menggunakan `N = 0` menghasilkan logika yang salah.