# Nerode és Myhill tételei

## Automaták és átmenetfüggvények kiterjesztései

Van egy sima automatánk, és az átmenetfüggvényt kiterjesztjük a következőképpen:

- az üres szó hatására egyhelyben maradunk
- egy állapotból egy szó hatására történő átmenetet is definiáljuk
    - végigmegyünk azon, hogy a szó betűi milyen állapotokba visznek minket, ezt megtehetjük persze mert az automata determinisztikus

## Nerode-Myhill tétel

### Szintaktikus jobbkongruencia

Definiáljuk a ρ_L ekvivalenciarelációt a szigmacsillag felett a következőképpen:

`egy x és y szó akkor és csak akkor áll relációban, ha bármely z szót a szigmacsillagból x és y végére írunk, akkor vagy bennevan L-ben az xz és az yz is, vagy egyik sincs`

- **Lemma 2.2** ρ_L jobbkongruencia szigmacsillag felett, mert
    - x és y relációban állnak, u és z szigmacsillagbeli szó
    - ekkor x(uz) pontosan akkor van benne L-ben, ha y(uz) is
    - de az asszociativitás miatt (xu)z is pontosan akkor van benne L-ben ha (yu)z is
    - ez azt jelenti, hogy ekkor xu és yu -nak relációban kell állniuk egymással
    - tehát x ρ_L y => xu ρ_L y aka ρ_L jobbkongruencia
- **Lemma 2.3** Minden L szigmacsillag efletti nyelvre ρ_L szaturálja L-et
    - vegyünk x,y szavakat amik egy osztályban vannak, vagyis x ρ_L y
    - ekkor xz pontosan akkor van benne L-ben ha yz is (def szerint)
    - válasszuk z-t epszilonnak
    - ekkor x pontosan akkor van benne L-ben ha y is
    - vagyis minden osztályban lévő szavak vagy fixen benne vannak az L-ben, vagy fixen nem, mert ha x bennevan akkor y is, mert relációban állnak
- **Lemma 2.4** ρ_L a legbővebb olyan jobbkongruencia, ami szaturálja L-et
    - vegyünk két x,y szót amik relációban vannak
    - legyen z további tetszőleges szó
    - ekkor xz ρ yz mivel ρ jobbkongruencia
    - mivel ρ szaturálja L-et ezért xz eleme a nyelvnek akkor és csak akkor ha yz is
    - akkor y ρ_L y is igaz, vagyis biztos hogy ρ részhalmaza ρ_L-nek


