# Unos i ispis

U prethodnim modulima smo predstavili kako kreirati varijable i koje operacije možemo raditi sa njima.

## Ispis

Da bismo ispisali rezultate operacija sa našim varijablama koristimo funkciju "print()"
```python
x = 1
print(x)
```

```python
Output: 1
```

Unutar print funkcije možemo ispisati i više varijabli tako što ih odvojimo sa zarezom unutar print funkcije
```python
x = 1
y = 2
z = 3
print(x, y, z)
```

```python
Output: 1 2 3
```

Možemo i raditi sve postojeće operacije unutar print funkcije nakon čega ćemo kao izlaz dobiti rezultat nakon izvršenja istih
```python
x = 1
y = 2
a = "hello "
b = "world"
print(x + y)
print(a + b)
```

```python
Output: 3
        hello world
```

Print funkcija ne ispisuje samo varijable, već i konkretne vrijednosti koje joj zadamo
```python
x = 1
print(1)
print("Vrijednost varijable x je: ", x)
```

```python
Output: 1
        Vrijednost varijable x je: 1
```

## Unos

Da bismo omogućili korisniku da unosi svoje vrijednosti u program koristimo funkciju "input()".
```python
x = input("Unesite cijeli broj: ")
print(x)
```

Izvršenje programa se pauzira sve dok korisnik ne unese vrijednost i pritisne enter, nakon čega se ispiše vrijednost varijable.

> Znanje iz prethodnih modula možete iskoristiti za kreiranje programa koji izvršavaju različite matematičke zadatke. Npr. Računanje i ispis površine pravougaonika korisnički unesenih dimenzija