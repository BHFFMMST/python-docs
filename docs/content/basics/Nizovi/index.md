# Nizovi

Često se javljaju problemi koji zahtijevaju veliki broj podataka. Kada bi za svaku od njih koristili posebne varijable, imali bi smo veliki broj varijabli. To bi dosta otežalo rad i čitljivost koda. U takvim situacijama se koriste **nizovi**.
> **Niz** je složena promjeniva koja se koritsti za pohranu višeg broja istih varijabli.
> Postoje jednodimenzonalni i višedimenzionalni nizovi.

```python
import array

ime_varijble = array(tip_podatka,[elementi])
```

> Da bi se radilo sa nizovima potrebno je uključiti array modul.
> Elementi niz se pišu unutar srednih zagrada i odvajaju se zarezom.
> Svaka element  u nizu ima svoj redni broj(indeks), pomoću koje se može pristupati tom elementu.
> Indeksi počinju sa brojem 0.
> Tip podatak govori koja vrsta podataka se nalazi unutar niza.

"i" se korisiti za tip podataka int. "f" za float.

```python
import array as arr

niz = arr.array('i',[1, 2, 3, 4, 5])
print(niz[0])
print(niz[1])
print(niz[4])
```

```python
Output: 1
        2
        5
```

> **Niz** se može mijenati i dozvoljava duplikate.

> Funkcija **append()** dodaje na kraj niza samo jedan elemenat.

> Funkcija **extend()** dodaje na kraj niza više elemenata.

```python
import array as arr

niz = arr.array('i',[1, 2, 3, 4, 5])
niz[3] = 6
niz.append(7)
niz.extend([8, 8, 10])
print(niz)
```

```python
Output: array('i', [1, 2, 3, 6, 5, 7, 8, 8, 10])
```

Za printanje samo elemenata niza koristi se [for petlja](/content/basics/Petlje)

```python
import array as arr

niz = arr.array('i',[1, 2, 3, 4, 5])

for i in niz:
    print(i)
```

```python
Output: 1
        2
        3
        4
        5
```

> Za dodavanje elemenata u niz na određeno mjesto, umijesto na kraj, koristi se funkcija **insert()**.

> Za izbacivanje elemenata iz niza koristi se funkcija **remove()**.

Funkcija **remove** će izbaciti prvi element koji ima vrijednost koja joj se proslijedi, ukoliko imamo više 
elemenata iste vrijednosti.

> Za izbacivanje elemenata na određenoj poziciji koristi se funkcija **pop()**

```python
import array as arr

niz = arr.array('i',[1, 2, 3, 4, 5])
niz.insert(0, 2)
niz.remove(3)
niz.pop(3)

for i in niz:
    print(i)
```

```python
Output: 2
        1
        5
```

## Višedimenzionalni niz

```python
import numpy as np

niz = np.array([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]])
print(niz)
```

```python
Output: array([[ 1,  2,  3,  4],
               [ 5,  6,  7,  8],
               [ 9, 10, 11, 12]])
```

## Liste

**Liste** su najčešće korišteni  tip podataka za pohranu višeg broja podataka.

> **Lista** je složena promjeniva koja se koristi za pohranu višeg broja varijabli.

Liste i nizovi su slični. Ali za razliku od nizova, **liste** mogu u sebi sadržati različite vrte varijabli.

```python
lista = ["Hello", "world", "!"]
```

> Elementi liste se pišu unutar srednih zagrada i odvajaju se zarezom.

> Svaka element  u listi ima svoj redni broj (indeks), pomoću koje se može pristupati tom elementu.

> Indeksi počinju sa brojem 0.

```python
broj = 3
lista = ["Hello", 0, [1, 2, 3], broj, 4.5]
print(lista[0])
print(lista[2])
print(lista[2][1])
```

```python
Output: Hello
        [1, 2, 3]
        2
```

> Tip podatka kao što je string, može bit indeksiran. Indeksira se kao lista koja sadrži znakove u stringu.

```python
string = "Hello world"
print(string[6])
```

```python
Output: w       
```

> Liste se mogu sabirati i množiti na isti način kao i stringovi.

```python
lista = [1, 2, 3]
print(lista + [4, 5, 6])
pritn(lista * 2)
```

```python
Output: [1, 2, 3, 4, 5, 6]
        [1, 2, 3, 1, 2, 3]       
```

> Za provjeru da li se element nalazi u listi, koristi se **in** operator.

```python
lista = ["pas", "macka", "patka"]
print("pas" in lista)
pritn("krava" in lista)
```

```python
Output: True
        False      
```

> Liste se mogu mjenati i koriste se funkcije kao što su **append()**, **insert()**, **remove()**, **pop()**.

```python
lista = [1, 2, 3]
lista.append(4)
lista.insert(0, 0)
lista.remove(2)
lista.pop(1)
print(lista)
```

```python
Output: [0, 3, 4]           
```

> Za broj elemenata liste korsiti se funkcija **len()**

```python
lista = [1, 2, 3]
print(len(lista))
```

```python
Output: 3           
```

>Za sortiranje liste korisit se funkcija **sort()**.

```python
lista1= [74, 98, 125, 34, 172]
lista2 = ["mango", "jabuka", "banana", "kivi"]
lista1.sort()
lista2.sort()
print(lista1)
print(lista2)
```

```python
Output: [34,74, 98, 125, 172]
        ["banana", "jabuka", "kivi", "mango"]           
```


