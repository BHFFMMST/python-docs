# Nizovi

Često se javljaju problemi koji zahtijevaju veliki broj podataka. Kada bi za svaku od njih 
koristili posebne varijable, imali bi smo veliki broj varijabli. To bi dosta otežalo rad i
čitljivost koda. U takvim siutacijama se koriste **nizovi**. 
>**Niz** je složena promjeniva koja se koritsti za pohranu višeg broja istih varijabli.

>Postoje jednodimenzonalni i višedimenzionalni nizovi.

<pre>
```python
import array

ime_varijble = array(tip_podatka,[elementi])
```
</pre>

>Da bi se radilo sa nizovima potrebno je uključiti  array modlul.

>Elementi niz se pišu unutar srednih zagrada i odvajaju se zarezom.

>Svaka element  u nizu ima svoj redni broj(indeks), pomoću koje se može pristupati tom elementu.

>Indeksi počinju sa brojem 0.

> Tip podatak govori koja vrsta podataka se nalazi unutar niza.

i se korisiti za tip podataka int. f za float.

<pre>
```python
import array as arr

niz = arr.array('i',[1, 2, 3, 4, 5])
print(niz[0])
print(niz[1])
print(niz[4])
```
</pre>

<pre>
```python
Output: 1
        2
        5
```
</pre>

>**Niz** se može mjenati i dozvoljava duplikate.

> Funkcija **append()** dodaje na kraj niza samo jedan elemenat.

> Funkcija **extend()** dodaje na kraj niza više elemenata.

<pre>
```python
import array as arr

niz = arr.array('i',[1, 2, 3, 4, 5])
niz[3] = 6
niz.append(7)
niz.extend([8, 8, 10])
print(niz)
```
</pre>

<pre>
```python
Output: array('i', [1, 2, 3, 6, 5, 7, 8, 8, 10])
```
</pre>

>Za printanje samo elemenata niza koristi se **for** petlja

<pre>
```python
import array as arr

niz = arr.array('i',[1, 2, 3, 4, 5])

for i in niz:
    print(i)
```
</pre>
<pre>
```python
Output: 1
        2
        3
        4
        5
```
</pre>

>Za dodavanje elemenata u niz na određeno mjesto, umijesto na kraj, koristi se funkcija **insert()**.

>Za izbacivanje elemenata iz niza koristi se funkcija **remove()**.

Funkcja **remove** će izbaciti prvi element koji ima vrijednost koja joj se proslijedi, ukoliko imamo više 
elemenata iste vrijednosti.

>Za izbacivanje elemenata na određenoj poziciji koristi se funkcija **pop()**

<pre>
```python
import array as arr

niz = arr.array('i',[1, 2, 3, 4, 5])
niz.insert(0, 2)
niz.remove(3)
niz.pop(3)

for i in niz:
    print(i)
```
</pre>

<pre>
```python
Output: 2
        1
        5
```
</pre>

>Višedimenzionalni niz
<pre>
```python
import numpy as np


niz = np.array([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]])
print(niz)
```
</pre>
<pre>
```python
Output: array([[ 1,  2,  3,  4],
               [ 5,  6,  7,  8],
               [ 9, 10, 11, 12]])
```
</pre>

##Liste

**Liste** su najčešće korišteni  tip podataka za pohranu višeg broja podataka.

>**Lista** je složena promjeniva koja se koristi za pohranu višeg broja varijabli.

Liste i nizovi su slični. Ali za razliku od nizova, **liste** mogu u sebi sadržati različite vrte varijabli.

<pre>
```python
lista = ["Hello", "world", "!"]
```
</pre>

>Elementi liste se pišu unutar srednih zagrada i odvajaju se zarezom.

>Svaka element  u listi ima svoj redni broj(indeks), pomoću koje se može pristupati tom elementu.

>Indeksi počinju sa brojem 0.

<pre>
```python
broj = 3
lista = ["Hello", 0, [1, 2, 3], broj, 4.5]
print(lista[0])
print(lista[2])
print(lista[2][1])
```
</pre>
<pre>
```python
Output: Hello
        [1, 2, 3]
        2
```
</pre>

Tip podatka kao što je string, može bit indeksiran. Indeksira se kao lista koja sadrži znakove u stringu.

<pre>
```python
string = "Hello world"
print(string[6])
```
</pre>
<pre>
```python
Output: w       
```
</pre>

>Liste se mogu sabirati i množiti na isti način kao i stringovi.
```python
lista = [1, 2, 3]
print(lista + [4, 5, 6])
pritn(lista * 2)
```
</pre>
<pre>
```python
Output: [1, 2, 3, 4, 5, 6]
        [1, 2, 3, 1, 2, 3]       
```
</pre>

>Za provjeru da li se element nalazi u listi, koristi se **in** operator.
```python
lista = ["pas", "macka", "patka"]
print("pas" in lista)
pritn("krava" in lista)
```
</pre>
<pre>
```python
Output: True
        False      
```
</pre>

>Liste se mogu mjenati i koriste se funkcije kao što su **append()**, **insert()**, **remove()**, **pop()**.



```python
lista = [1, 2, 3]
lista.append(4)
lista.insert(0, 0)
lista.remove(2)
lista.pop(1)
print(lista)
```
</pre>
<pre>
```python
Output: [0, 3, 4]           
```
</pre>


>Za broj elemenata liste korsiti se funkcija **len()**


```python
lista = [1, 2, 3]
print(len(lista))
```
</pre>
<pre>
```python
Output: 3           
```
</pre>

>Za sortiranje liste korisit se funkcija **sort()**.

```python
lista1= [74, 98, 125, 34, 172]
lista2 = ["mango", "jabuka", "banana", "kivi"]
lista1.sort()
lista2.sort()
print(lista1)
print(lista2)
```
</pre>
<pre>
```python
Output: [34,74, 98, 125, 172]
        ["banana", "jabuka", "kivi", "mango"]           
```
</pre>


