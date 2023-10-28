# Operatori

Operatori se koriste za izvršavanje različitih operacija na varijablama i vrijednostima. 
U prethodnom segmentu smo spomenuli operator "=" što je u pythonu operator dodjele, a ne matematički operator jednako.
Šta to znači? Vrijednosti sa desne strane od "=" se dodjeljuju u varijablu sa lijeve strane "=".

```python
x = 1 # 1 se dodjeljuje u x
y = x # vrijednost od x se dodjeljuje u y, te ce y imati vrijednost 1
```

> NOTE: # je znak za komentar unutar pythona. Sve iza znaka "#" se ignoriše prilikom izvršavanja koda.

## Matematički operatori

Za izvršenje osnovnih matematičkih operacija koristimo operatore:

- +,  sabiranje/dodavanje
- -, oduzimanje
- *, množenje
- /, dijeljenje
- %, modul (vraća ostatak prilikom cjelobrojnog dijeljenja)
- **, eksponencijacija
- //, cjelobrojno dijeljenje

```python
x = 1 + 2 # 3
x = 2 - 1 # 1
x = 2 * 2 # 4
x = 4 / 2 # 2
x = 12 / 2 # 0
x = 3 ** 2 # 9
x = 5 // 2 # 2
```

## Operatori dodjele

Pored osnovnog znaka "=" imamo dodatne operatore dodjele:

- =, primjer: x = 5, isto kao: x = 5	
- +=, primjer: x += 3, isto kao: x = x + 3	
- -=, primjer: x -= 3, isto kao: x = x - 3	
- *=, primjer: x *= 3, isto kao: x = x * 3	
- /=, primjer: x /= 3, isto kao: x = x / 3	
- %=, primjer: x %= 3, isto kao: x = x % 3	
- //=, primjer: x //= 3, isto kao: x = x // 3	
- **=, primjer: x **= 3, isto kao: x = x ** 3

## Operatori komparacije

Operatori komparacije se koriste za poređenje dvije vrijednosti/varijable:

- ==, jednako, x == y	
- !=, nije jednako, x != y	
- \>, veće od, x > y	
- <, manje od, x < y	
- \>=, veće ili jednako, x >= y	
- <=, manje ili jednako, x <= y

Navedeni operatori kao rezultat vraćaju bool varijablu vrijednosti True ili False zavisno od rezultata komparacije.

## Prioriteti operacija

Kao i u matematici, operatori unutar programskih jezika imaju različite prioriteta tokom njihovih izvršenja. Unutar pythona, od najvećeg do najnižeg prioriteta:

- ()	
- **
- \*  /  //  %
- \+  -
- ==  !=  >  >=  <  <=
- not	logičko "ne"
- and	logičko "i"
- or	logičko "ili"

> Na logičke operatore ćemo se više osvrnuti unutar modula o if-else naredbama