---
jupytext:
  text_representation:
    format_name: myst
kernelspec:
  display_name: Python 3
  name: python3
---

# Šestka v šiestich IV.

Ýzyho testy vyzerajú takto:

```{code-cell} ipython3
:tags: [raises-exception]

from random import randint # sprístupníme si funkciu na vygenerovanie náhodných celých čísel

def hod_kockou(): # zadefinujeme si vlastnú funkciu "hod_kockou" 
    return randint(1, 7) # vygenerujeme celé číslo medzi 1 (vrátane) a 7 (nevrátane)

# testy
def otestuj_hod_kockou(N):
    for i in range(N):
        assert(hod_kockou() in [1,2,3,4,5,6])

# spustenie testu
otestuj_hod_kockou(10000)
```
A sme našli našu chybu. Očividne generujeme niečo iné, ako výsledky hodov kockou. Keď sa pozrieme na dokumentáciu funkcie `randint`, zistíme nasledovné.

```{code-cell} ipython3
help(randint)
```
Takže je to celé jasné. Ýzy spravil chybu v simulácií v tom, že si zle prečítal a vyskúšal dokumentáciu, pretože oba koncové body sú zahrnuté. Opravený Ýzyho kód simulácie teda vyzerá takto:

```{code-cell} ipython3
def hod_kockou_spravne(): 
    return randint(1, 6) 

def sestka_v_siestich_hodoch():
    return any(hod_kockou_spravne() == 6 for i in range(6))

pocet_pokusov = 1000000
sum(sestka_v_siestich_hodoch() for i in range(pocet_pokusov)) / pocet_pokusov 
```
Tento výsledok sa zhoduje s výsledkom matematických výpočtov. Ýzy teda konečne prišiel spokojný k záveru, že sa mu úlohu podarilo vyriešiť. 

Samotný výsledok Ýzyho až tak nezaujal. Veď ani pôvodný príklad nebol v skutočnosti až taký zaujímavý. Omnoho zaujimavejší preňho bol proces, ako sa k výsledku dostal. V prvom výsledku mal až dve chyby, ktoré si postupne sám zvládol nájsť tým, že sa snažil k riešeniu dostať rôznymi spôsobmi. Ako hovorieval dedo Yvan: "*Keby ti vždy musel niekto skontrolovať správnosť tvojich výsledkov, tvoja práca je polo-zbytočná.*". V duchu tejto filozofie sa odvtedy malý Ýzy vždy vytešoval z toho, keď sa mu podarilo nájsť si vlastnú chybu. Stával sa tým nezávislejším a z pohľadu svojho deda menej zbytočným.

```{admonition} Poznámka o chybách
V tradičných učebniciach môžete byť zvyknutí na to, že v nej nie sú chyby. Tento zvyk považujú v Ystotne za mierne škodlivý. Na jednej strane je síce pekné oprieť sa o poznatky o ktorých vieme, že sú správne. Dodáva nám to istý komfort. Na druhej strane ale čitateľ často skĺzne do toho, že text slepo číta a nezamýšľa sa nad ním. Tomuto sa v Ystotne vyhýbajú tým, že vo svojich textoch majú občas schválne chyby. Keďže tento text je o zápiskoch Yzidora z Ystotny, môžete v ňom tiež očakávať chyby.
```

Malý Ýzy vypočítal úlohu, ktorú si sám zadal a niečo sa nové naučil. Trocha málo sa naučil matematiky a programovania, trocha viac ohľadom vlastných chýb. Odpoveď mu ukázala, že po šiestich hodoch šestkov je iba $66\%$ pravdepodobnosť na to, že padne aspoň jedna šestka. To je výrazne menej, ako bolo jeho pôvodných $100%$.

```{admonition} Úloha
:class: tip
Koľkokrát by musel malý Ýzy hodiť kockou, aby mu padla na $100\%$?
```