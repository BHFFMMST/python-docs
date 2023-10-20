# Funkcije

Funkcije predstavljaju imenovane blokove koda koji su namijenjeni za izvršavanje određenih zadataka, a mogu se pozivati iz drugih dijelova programa. Jednom napisana funkcija se može pozivati više puta, što je i njena svrha, na taj način se izbjegava ponavljanje istog koda više puta.

## Definisanje funkcije

U nastavku je primjer definisanja funkcije koja ispisuje pozdravnu poruku:

```python
def print_pozdrav():
    print("Pozdrav!")

print_pozdrav()
```

Ovaj primjer pokazuje najjednostavniju strukturu funkcije. Ključna riječ `def` označava početak **definicije funkcije**, nakon koje slijedi ime funkcije, u ovom slučaju je to `print_pozdrav`, zatim se navode zagrade u kojima se mogu navesti parametri funkcije. U ovom slučaju funkcija nema parametre, pa su zagrade prazne, i one su obavezne, bez obzira da li funkcija ima ili nema parametre, a nako toga slijedi dvotačka. 

Sve naredbe koje pripadaju funkciji moraju da se nalaze u bloku koda koji je uvučen u odnosu na definiciju funkcije. U ovom slučaju je to samo jedna naredba, ali ih može biti više.

Kada smo definisali funkciju, možemo je pozvati u bilo kojem dijelu programa i to na način da navedemo ime funkcije, praćeno zagradama u kojima se navode argumenti koje prosljeđujemo funkciji. To se naziva **poziv funkcije**. U ovom slučaju funkcija nema parametre, pa su zagrade prazne.

## Parametri funkcije

Funkcija može imati jedan ili više parametara, a oni se navode u zagradama prilikom definisanja funkcije. Parametri su promjenljive koje se koriste unutar funkcije i njihove vrijednosti se prosljeđuju prilikom poziva funkcije. U nastavku je primjer funkcije koja ispisuje pozdravnu poruku za prosljeđeno ime:

```python
def print_pozdrav(ime):
    print(f"Pozdrav {ime}!")

print_pozdrav("BHFF")
```

U ovom slučaju funkcija ima jedan parametar, a to je `ime`. Funkcija sada očekuje da se prilikom poziva proslijedi jedan argument, koji će se dodjeliti parametru `ime` u funkciji. U ovom slučaju je to string `"BHFF"`.


**Razlika između parametara i argumenata?**

Parametri su promjenljive koje se navode *prilikom definisanja funkcije*, a argumenti su vrijednosti koje se prosljeđuju *prilikom poziva funkcije*. U prethodnom primjeru, argument je `"BHFF"` koji je prosljeđen funkciji `print_pozdrav`, a vrijednost tog argumenta je dodjeljena parametru `ime` u funkciji. 

**Napomena:** Nerijetko se ova dva pojma koriste naizmjenično, ali je važno razumjeti razliku između njih.

## Prosljeđivanje argumenata funkciji

U prethodnom primjeru smo naveli funkciju sa jednim parametrom, ali kako smo već ranije naveli, funkcija može imati više parametara. Kada funkcija ima više parametara, očekivano je da se prilikom poziva funkcije proslijedi isti broj argumenata. prosljeđivanje argumenata funkciji se može uraditi na dva načina, koristeći poziciju - **pozicioni argumenti** ili koristeći ključnu riječ parametra - **ključni argumenti**. 

### Pozicioni argumenti (positional arguments)

Prilikom poziva funkcije, Python mora da zna koji argument se prosljeđuje kojem parametru, a to se u ovom slučaju određuje na osnovu redoslijeda navođenja argumenata. U nastavku je primjer funkcije koja ispisuje informaciju o ljubimcu:

```python
def opisi_ljubimca(ime_ljubimca, vrsta_ljubimca):
    print(f"Moj kućni ljubimac je {vrsta_ljubimca}, a zove se {ime_ljubimca}.")

opisi_ljubimca("Leksi", "pas")
```

U ovom slučaju funkcija ima dva parametra, `ime_ljubimca` i `vrsta_ljubimca`. Kada pozivamo ovu funkciju, potrebno je da argumente proslijedimo u istom redoslijedu kao što su navedeni parametri. U ovom slučaju, prvi argument je `"Leksi"` i on se prosljeđuje prvom parametru `ime_ljubimca`, a drugi argument je `"pas"` i on se prosljeđuje drugom parametru `vrsta_ljubimca`.

**Napomena:** Ukoliko se argumenti ne proslijede u istom redoslijedu kao što su navedeni parametri, može doći do neočekivanog rezultata.


### Ključni argumenti (keyword arguments)

Ključni argumenti se koriste kada želimo da proslijedimo argumente funkciji na osnovu imena parametra, a ne na osnovu pozicije. U nastavku je prethodni primjer koji koristi ključne argumente u pozivu funkcije:

```python
def opisi_ljubimca(ime_ljubimca, vrsta_ljubimca):
    print(f"Moj kućni ljubimac je {vrsta_ljubimca}, a zove se {ime_ljubimca}.")

opisi_ljubimca(vrsta_ljubimca="pas", ime_ljubimca="Leksi")
```

U ovom slučaju, prvo navodimo ime parametra, a zatim vrijednost koju želimo da proslijedimo. Na ovaj način, redoslijed argumenata nije bitan, jer se argumenti prosljeđuju na osnovu imena parametra, prema tome, možemo i ovako pozvati funkciju:

```python
opisi_ljubimca(ime_ljubimca="Leksi", vrsta_ljubimca="pas")
```

**Napomena:** Moguće je kombinovati pozicione i ključne argumente, ali je važno da se prvo navedu pozicioni argumenti, a zatim ključni argumenti.


### Proizvoljan broj argumenata

Funkcija može imati proizvoljan broj argumenata, a to se postiže tako što se parametar navodi sa prefiksom `*`. U nastavku je primjer takve funkcije:

```python
def napuni_listu(*elementi):
    lista = []

    for element in elementi:
        lista.append(element)
    
    return lista
```

Ova funkcija prima proizvoljan broj argumenata, a zatim ih dodaje u listu i vraća konstruisanu listu. Kada pozivamo ovu funkciju, možemo proslijediti proizvoljan broj argumenata:

```python
spisak = napuni_listu("jabuka", "kruška", "šljiva")
print(spisak)
```

## Predefinisane vrijednosti parametara

Kada pišemo funkciju, možemo navesti predefinisanu (zadanu) vrijednosti (default value) parametara. Ako se prilikom poziva funkcije ne proslijedi argument za taj parametar, funkcija će koristiti predefinisanu vrijednost, a ako se proslijedi argument, funkcija će koristiti vrijednost koja je prosljeđena. U nastavku je primjer funkcije koja ispisuje informaciju o ljubimcu, ali ovaj put sa predefinisanim parametrom `vrsta_ljubimca`:

```python
def opisi_ljubimca(ime_ljubimca, vrsta_ljubimca="pas"):
    print(f"Moj kućni ljubimac je {vrsta_ljubimca}, a zove se {ime_ljubimca}.")

opisi_ljubimca(ime_ljubimca="Leksi")
```

U ovom slučaju, funkcija ima predefinisani parametar `vrsta_ljubimca` koji ima vrijednost `"pas"`. Kada pozivamo funkciju, možemo proslijediti argument za taj parametar, ali to nije obavezno, jer će funkcija koristiti predefinisanu vrijednost. 

Za opis nekog drugog ljubimca, možemo proslijediti argument za taj parametar:

```python
opisi_ljubimca(ime_ljubimca="Čupka", vrsta_ljubimca="mačka")
```

**Napomena:** Parametri sa predefinisanom vrijednošću moraju biti navedeni nakon parametara bez predefinisane vrijednosti. Ovo Python-u omogućava da na ispravan način interpretira argumente na osnovu pozicije.

### Opcioni parametri

Ponekad ima smisla da neki parametri budu opcioni, za to se koriste predefinisane vrijednosti parametara. Posmatrajmo primjer:

```python
def opisi_ljubimca(ime_ljubimca, vrsta_ljubimca, starost_ljubimca=None):
    if starost_ljubimca:
        print(f"Moj kućni ljubimac je {vrsta_ljubimca}, a zove se {ime_ljubimca} i ima {starost_ljubimca} godina.")
    else:
        print(f"Moj kućni ljubimac je {vrsta_ljubimca}, a zove se {ime_ljubimca}.")

```

Kada pozivamo funkciju, možemo proslijediti argument za parametar `starost_ljubimca`, ali to nije obavezno, jer je taj parametar opcioni. Ukoliko se proslijedi taj argument, funkcija će ispisati više informacija o ljubimcu, a ako se ne proslijedi, funkcija će ispisati samo ime i vrstu ljubimca.

```python
opisi_ljubimca(ime_ljubimca="Leksi", vrsta_ljubimca="pas", starost_ljubimca=3)

opisi_ljubimca(ime_ljubimca="Čupka", vrsta_ljubimca="mačka")
```

## Povratna vrijednost funkcije

Funkcija može da vrati neki rezultat, a to se naziva **povratna vrijednost funkcije**. Ključna riječ `return` označava povratnu vrijednost funkcije, a nakon nje se navodi vrijednost koju funkcija vraća, ta vrijednost se vraća na mjesto poziva funkcije. U nastavku je primjer jedne takve funkcije:

```python
def kvadriraj(broj):
    return broj * broj
```

Ova funkcija prima jedan parametar `broj`, a zatim vraća kvadrat tog broja. Kada pozivamo ovu funkciju, možemo rezultat dodijeliti nekoj promjenljivoj:

```python
broj = 5
kvadrat = kvadriraj(broj)
print(f"Kvadrat broja {broj} je {kvadrat}.")
```

U ovom slučaju, funkcija `kvadriraj` vraća kvadrat broja `5`, koji se dodjeljuje promjenljivoj `kvadrat`. Povratne vrijednosti omogućavaju da se ključni dijelovi koda izdvajaju u funkcije, a zatim da se rezultat tih funkcija koristi u drugim dijelovima programa, što doprinosi boljoj čitljivosti i održavanju programa jer se pojednostavljuje glavni dio programa.


**Napomena:** Funkcija koja ne vraća nikakvu vrijednost, takva funkcija se naziva **void** funkcija i u Python-u takve funkcije zapravo vraćaju `None`.


### Povratak više vrijednosti

Funkcija može vratiti više vrijednosti, a to se postiže tako što se vrijednosti odvoje zarezom. U nastavku je primjer takve funkcije:

```python
def povrsina_i_obim_kvadrata(stranica):
    povrsina = stranica * stranica
    obim = 4 * stranica
    return povrsina, obim
```

Ova funkcija prima jedan parametar `stranica`, a zatim vraća površinu i obim kvadrata. Kada pozivamo ovu funkciju, možemo rezultat dodijeliti dvjema promjenljivim:

```python
stranica = 5
povrsina, obim = povrsina_i_obim_kvadrata(stranica)
print(f"Površina kvadrata sa stranicom {stranica} je {povrsina}, a obim je {obim}.")
```
