# IT-CUP-SOAL-KEEMPAT
```

#Deklarasi Variabel
Jml_ayam = 0
jml_kandang = 0
berat_ayam = []
ukuran_kandang = []
biaya_kandang = []



def min_biaya(jml_ayam, jml_kandang, berat_ayam, ukuran_kandang, biaya_kandang):
    berat_ayam.sort(reverse=True)
    kandang = sorted(zip(ukuran_kandang,biaya_kandang), key=lambda x: x[1])
    
    total_biaya = 0
    indeks_kandang = 0
    
    for berat in berat_ayam:

        while indeks_kandang < jml_kandang and kandang[indeks_kandang][0] == 0:
            indeks_kandang += 1
        
        if indeks_kandang == jml_kandang:
            return -
        
        total_biaya += berat * kandang[indeks_kandang][1]
        kandang[indeks_kandang] = (kandang[indeks_kandang][0]-1,kandang[indeks_kandang][1])
    
    return total_biaya

#misal
Jml_ayam = 6
jml_kandang = 2
berat_ayam = [4,1,5,2,3,2]
ukuran_kandang = [3,4]
biaya_kandang = [5,2]

print(min_biaya(Jml_ayam,jml_kandang,berat_ayam,ukuran_kandang,biaya_kandang))






```
