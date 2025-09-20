# Reverse code a list

Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. 

**Örnek:**  
input: `[[1, 2], [3, 4], [5, 6, 7]]`  
output: `[[[7, 6, 5], [4, 3], [2, 1]]`

**Çözüm:**
```python
l = [[1, 2], [3, 4], [5, 6, 7]]
reverse = []
for i in l[::-1]:
    reverse.append(i[::-1])
print(reverse)