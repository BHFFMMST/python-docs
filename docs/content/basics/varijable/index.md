# Varijable

Python za razliku od jezika kao što su java, C#, C++... nema komandu za "deklarisanje" varijable. 
> Deklarisanje varijable bi unutar navedenih jezika funkcionisalo tako što biste dali tip varijable, nakon čega biste naveli ime same varijable.
Primjer unutar jave:
```java
int varijabla;
```

Kako onda kreiramo varijable u pythonu? Tako što im damo vrijednost. Pomoću operatora "=" dodjeljujemo vrijednost varijablama. Više o ovome operatoru unutar sekciji za [operatore](/content/basics/operatori/).

Dakle, varijabla se kreiraju u momentu kada im damo vrijednost
```python
x = 1
b = "primjer"
```

## Tipovi varijabli

Šta to znači za tipove varijabli? Python ih automatski zadaje kada varijabli damo vrijednost, te čak automatski mijenja tip u slučaju promjene vrijednosti iste varijable. 

U primjeru iznad varijabla "x" će dobiti tip **int**, tj. integer što predstavlja cijeli broj, dok će varijabla "y" dobiti tip **str**, tj. string.

Šta ako želimo kreirati varijablu specifičnog tipa? Tada ćemo koristiti takozvani "casting" da striktno konvertujemo vrijednost u zadani tip varijable.
```python
x = str(1)
```

Generalno "casting" kao koncept se može koristiti i za konvertovanje već postojeće varijable u drugi tip. Razlog je najčešće korištenje brojnih vrijednosti kao string ili obrnuto.

Osnovni tipovi varijabli koji postoje u pythonu (i većini ostalih programskih jezika) su:

- str - string, tekstualni tip varijable
- int - cijeli broj
- float - decimalni broj
- bool - binarni tip podatka, može sadržavati samo vrijednosti "True" i "False" tj. 0 ili 1

## Brojevi

Numerički tipovi varijabli u pythonu su int i float. 

Int je cijeli broj, pozitivan ili negativan beskonačne dužine
```python
x = 1
y = -1
z = 125871726508610512
```

Float je decimalni broj, pozitivan ili negativan beskonačne dužine
```python
x = 1.0
y = 1.5
z = -3.41
```

## Stringovi

Stringovi su tekstualni tip varijable.

Stringove možemo definisati i sa jednostrukim i dvostrukim navodnicima
```python
x = "primjer"
y = 'primjer'
# oba načina su validna
```

Također možemo kreirati string od više linija sa trostrukim navodnicima
```python
x = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
y = '''Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.'''
# oba načina su validna
```

## Imenovanje varijabli

Jedna od početničkih greški je loše imenovanje varijabli. Svaki jezik ima osnovne uslove imenovanja varijabli:

- varijabla mora kao prvi karakter imati ili slovo ili donju crtu
- varijabla ne smije imati razmak unutar imena
- ...

```python
2x = 1 # nije validno ime
x = 1 # validno ime
```

Navedeni uslovi regulišu da su imena varijabli validna, ali ne i dobra.
Ime same varijable treba biti deskriptivno, jednostavno i jasno, da u kasnijem korištenju varijable se može na osnovu imena zaključiti šta ona predstavlja.

Uzet ćemo primjer da želimo kreirati varijablu koja predstavlja ime korisnika
```python
x = "Ahmed" # nedeskriptivno ime, gdje se iz imena ne moze zakljuciti sta ona predstavlja
imeKorisnika = "Ahmed" #deskriptivno ime varijable
```

Postoji više načina kako se pravilno pišu imena varijabli koja sadrže više riječi unutar sebe, od kojih najčešći u upotrebi su:

- camel case: prva riječ počinje sa malim slovom, dok svaka sljedeća velikim (imeKorisnika, brojGodinaKorisnika)
- snake case: svaka riječ je odvojena donjom crtom (ime_korisnika, broj_godina_korisnika)

Također, imena varijabli su "case-sensitive"
```python
x = 1
X = 2
# x i X ce biti dvije razlicite varijable
```