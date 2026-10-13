# Denník potravín

Jednoduchá webová aplikácia na zapisovanie jedla počas dňa: kalórie, bielkoviny, sacharidy a tuky.
Celá aplikácia je jeden súbor `index.html`, nepotrebuje server ani inštaláciu.

## Čo vie

- Denník po jedlách: raňajky, desiata, obed, olovrant, večera. Prechod medzi dňami šípkami alebo dátumom.
- Databáza ~90 bežných potravín s hodnotami na 100 g (orientačné), vyhľadávanie funguje aj bez diakritiky („ryza“ nájde „Ryža“).
- Zadanie množstva v gramoch alebo kusoch (vajce 55 g, krajec chleba 40 g, odmerka proteínu 30 g…).
- Vlastné potraviny z obalu (hodnoty na 100 g, voliteľne veľkosť porcie) a rýchly zápis porcie bez váženia.
- Denný cieľ kalórií a makier, súhrn dňa a podiel energie z makier.
- Graf posledných 7 dní s priemerom kalórií a bielkovín.
- Kopírovanie jedla z predošlého dňa, úprava a mazanie položiek s možnosťou „Späť“.
- Export a import zálohy (JSON).

## Spustenie

Otvor `index.html` v prehliadači. Záznamy sa ukladajú do `localStorage` daného prehliadača,
preto si občas urob zálohu cez **Ciele → Exportovať zálohu**.

Na mobile ju najľahšie sprístupníš cez GitHub Pages (Settings → Pages → vetva s `index.html`)
a potom „Pridať na plochu“.

Keď je stránka otvorená ako Artifact na claude.ai, ukladá záznamy súkromne do účtu prihláseného
používateľa namiesto prehliadača.
