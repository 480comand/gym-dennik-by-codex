# Denník potravín

Webová aplikácia na zapisovanie jedla, inšpirovaná MyFitnessPal a Kalorickými tabuľkami:
kalórie, bielkoviny, sacharidy, tuky, pitný režim a aktivita. Celá aplikácia je jeden súbor
`index.html`, nepotrebuje server ani inštaláciu.

## Hlasový zápis

Ťukni na mikrofón a povedz napríklad:

> Na raňajky dve vajcia, krajec chleba s maslom a kávu. Na obed 150 gramov kuracích pŕs a 200 g ryže, k tomu pol litra vody.

Aplikácia z vety vytiahne jednotlivé potraviny, množstvá (gramy, kusy, krajce, lyžice, deci,
deka, poháre…) a jedlo dňa. Pred pridaním ukáže zoznam na kontrolu: pri každej položke sa dá
zmeniť množstvo, jedlo dňa alebo zvoliť inú podobnú potravinu. Voda sa pripočíta k pitnému režimu.

- **V prehliadači** (Chrome, Edge, Safari) nahráva priamo cez mikrofón (Web Speech API, slovenčina)
  a vetu rozpoznáva priamo v aplikácii, bez internetovej AI.
- **Ako Artifact na claude.ai** sa diktuje mikrofónom na klávesnici telefónu a vetu rozpozná Claude.
  Zvládne aj jedlá, ktoré nie sú v databáze (napr. „rizoto s hubami“), a odhadne ich hodnoty.

## Čo ešte vie

- Denník po jedlách: raňajky, desiata, obed, olovrant, večera, druhá večera.
- Súhrn dňa v štýle MyFitnessPal: **cieľ − jedlo + aktivita = zostáva**, energia aj v kJ,
  makrá a podiel energie z makier, séria dní so zápisom.
- Pitný režim po pohároch (250 ml) s denným cieľom.
- Aktivita: posilňovňa, beh, bicykel… Spálené kalórie sa počítajú z trvania a hmotnosti
  (MET) a pripočítajú sa k cieľu; hodnotu z hodiniek sa dá prepísať.
- Databáza ~100 bežných potravín s hodnotami na 100 g (orientačné), vyhľadávanie aj bez diakritiky.
- Vlastné potraviny z obalu, rýchly zápis porcie bez váženia, kopírovanie jedla z predošlého dňa.
- Graf posledných 7 dní, export a import zálohy (JSON).

## Spustenie

Otvor `index.html` v prehliadači. Záznamy sa ukladajú do `localStorage` daného prehliadača,
preto si občas urob zálohu cez **Ciele → Exportovať zálohu**. Mikrofón v prehliadači funguje
len cez `https://` alebo `localhost`, napríklad cez GitHub Pages (Settings → Pages).

Keď je stránka otvorená ako Artifact na claude.ai, ukladá záznamy súkromne do účtu prihláseného
používateľa namiesto prehliadača.
