# Flatten code

Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden (`[[3], 2]` gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir.  

**Örnek:**  
input: `[[1,'a',['cat'],2],[[[3]],'dog'],4,5]`  
output: `[1,'a','cat',2,3,'dog',4,5]`

**Çözüm:**
```python
l =  [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
flat_list = []
for i in l:
    if isinstance(i, list):        
        for j in i:
            flat_list.append(j)
        else: 
            flat_list.append(i)
print(flat_list)