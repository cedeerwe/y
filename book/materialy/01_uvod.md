---
jupytext:
  text_representation:
    format_name: myst
kernelspec:
  display_name: Python 3
  name: python3
---

# Úvod

Hlavnou časťou našej akadémie sú nami pripravené materiály na štúdium. Skôr, ako sa do nich pustíte, máme pre vás niekoľko rád o tom, ako si z nich zobrať čo najviac.

## Metódy a ich vymýšľanie

Cieľom našej akadémie je, aby ste vedeli zodpovedať na najrôznejšie otázky zo sveta, ktoré vás napadnú. To môžme dosiahnuť viacerými spôsobmi.

```{code-cell} ipython3
:tags: [remove-input]
import graphviz

d = graphviz.Digraph()
for i in range(1,5):
    d.edge("Schopnosť vymýšľať metódy", f"Metóda {i}")
    for j in range(2*i-1, 2*(i+1)):
        d.edge(f"Metóda {i}", f"Otázka {j}")
d
```

Môžme vás začať učiť používať rôzne metódy na riešenie úloh. Tento prístup je celkom štandardný, používa sa napríklad aj vo väčšine škôl. Naučia vás používať konkrétne postupy, ktoré sa dajú aplikovať na konkrétne problémy. Hlavný problém tohto prístupu je, že akonáhle sa stretnete s problémom, na ktorého riešenie neviete napasovať žiadnu zo svojich naučených prístupov, narazili ste na prekážku. Táto prekážka pravdaže nie je neprekonateľná, ale keďže ste sa doteraz nesústredili na prekonávanie takýchto prekážok, bude pre vás často náročné ju prekonať.

V našej akadémii sa chceme sústrediť práve na schopnosť prekonávať takéto prekážky. Nie je naším cieľom naučiť vás konkrétne metódy, namiesto toho by sme vás radi učili schopnosť takéto metódy vymýšľať. Tento cieľ je náročnejší a výrazne abstraktnejší. Neexistuje totiž presný zoznam vecí, ktoré sa máte naučiť, aby ste v tomto boli dobrí. Ako sa teda môžme v tomto zlepšovať? Tak ako vo všetkom ostatnom - precvičovaním.

Každá stránka našich materiálov je ukončená otázkou, nad ktorou by ste sa mali poriadne zamyslieť a zodpovedať si ju predtým, ako sa pustíte ďalej. Najčastejšie síce tieto otázky čiastočne zodpovieme za vás, vašim cieľom by ale nemalo byť zistiť odpovede na všetky otázky, ktoré vám kladieme. Tak ako sme si povedali vyššie, našim cieľom je precvičiť si našu schopnosť vymýšľať si tieto metódy a odpovede sami.

Náš prístup nie je lepší ako tradičný školský. Je odlišný. Každý z nich má svoje výhody. Ak sa učíte iba metódy, budete mať problém riešiť problémy, ktoré nie sú riešiteľné vašim arzenálom metód. Ak sa budete učiť vymýšľať metódy, bude vám dlhšie trvať vyriešiť ľubovoľný problém, lebo v tom nemáte prax. Keďže je ale naším cieľom zlepšiť sa v odpovedaní na najrozličnejšie otázky z celého sveta, jediná cesta je naozaj zlepšiť sa vo vymýšľaní metód riešenia úloh.

Ak aj nezvládnete na všetky otázky zodpovedať, to v skutočnosti vôbec nevadí. Dôležité je, aby ste nad nimi zamýšľali a skúšali ich vyriešiť. Aj športovcom sa nedarí prekonať svetový rekord, ale napriek tomu to skúšajú a stále sa zlepšujú.

V skratke: **Nečítajte tieto materiály ako knihu**. Hlavná časť týchto materiálov leži *medzi* stránkami, kde by ste mali tráviť najviac času. Tam sa rozvíjate v schopnostiach, na ktoré sú tieto materiály sústredené. 



## Práca v skupine

Aj keď sa naše materiály dajú študovať aj osamote, vôbec to neodporúčame. Naozaj. Čítať samostatne je úplne v poriadku, ale rozmýšľať nad problémami je vždy lepšie v skupinách. Každý ďalší pohľad na vec prinesie nový uhol a nový vhľad do problematiky. Občas sa stane, že jeden z vás nebude rozumieť argumentom druhého. Pri riešení týchto situácií sa zlepšíte v argumentovaní, vysvetľovaní, pochopeniu druhých. Tieto schopnosti sú v živote veľmi dôležité a náročne sa získavajú.

Naša akadémia má v Bratislave pravidelné stretnutia, kde sa skupiny ľudí prelúskavajú našimi materiálmi. Ak ste z okolia, odporúčame vám na tieto stretnutia chodiť a spoločne s lektormi posúvať svoje vedomosti ďalej.

Ak máte do Bratislavy ďaleko, dohodnite sa so svojimi kamarátmi na stretnutiach, kde si budete spoločne týmito materiálmi prechádzať. Je to skoro rovnako dobré, ako chodiť na spoločné stretnutia do Bratislavy.
