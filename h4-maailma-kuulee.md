## Tehtävä x)

#### Pilvipalvelimen vuokraus ja asennus
- Virtuaaliset yksityispalvelimet ja verkkotunnukset ostetaan yrityksiltä.
- Voit vuokrata ja asentaa oma pilvipalvelin internettiin, jonka palvelimeen vuokrattu domainnimi osoittaa.
- Pilvipalvelimen voi vuokrata itselleen parhaimmaksi kokemastaan paikasta. Tähän voi hyödyntää Githubin Education pakettia, suosia Suomalaista ja käyttää rahaa sen vuokraamiseen tarpeiden tarvitseman määrän. Githubin Education paketti tarjoaa alennuskoodin, jolla voi ainakin kurssin ajaksi itselleen vuokrata palvelimen maksutta.
- Palvelimen vuokraus onnistuu suoraan palvelutarjoajien sivuilta step-by-step.


#### Palvelin suojaan palomuurilla
- Palvelimelle on syytä asentaa palomuuri, joka toimii suodattimena.
- Palomuuri valvoo verkkoliikennettä ja estävää luvattoman pääsyn datakeskuksiin tai pilvessä oleviin palveluihin.
- Osa pilvipalvelimista saattaa kaupitella heidän omaa palomuuriaan ja näitä voikin kilpailuttaa omien tarpeiden ja mieltymysten mukaisesti. 
- Komentokeskuksessa SHH-yhteyden ottamiseksi käytetään komentoa: $ ssh root@ (tähän IP-osoite)
- Virtuaalipalvelinta käyttäessä ensimmäistä kertaa, kannattaa hakea tiedot päivityksistä koneen terminaalin kautta: $ sudo apt-get update. Sitten palomuurin asennus komennolla: $ sudo apt-get install ufw ja palomuuriin reikä porttia varten: $ sudo ufw allow 22/tpc. Palomuurin takaisin päälle komennolla: $ sudo ufw enable. 


#### Kotisivut palvelimelle
- Virtuaalipalvelimen luominen terminaalissa komennolla:$ sudo adduser (oma nimi), sitten hyvän salasanan luominen.
- Käyttäjästä pääkäyttäjä komennolla: $ sudo adduser (oma nimi) sudo
- Uuden käyttäjän tunnusten toimimisen testaaminen: ensin SSH-yhteyden avaus virtuaalipalvelimeen ja sitten tietojen päivitys saatavilla olevista päivityksistä:
    $ ssh (oma nimi)@(IP-osoite)
    $ sudo apt-get update
- Juuren lukitus komennolla: $ sudo usermod –lock root
- Vielä voi kokeilla oman domainnimen pingausta komennolla: $ ping (omanimi).me. Tähän päästyäni domainnimi olisi todennäköisesti muodossa inkaheinonen.me
- Toinen reikä palomuuria varten komennolla: $ sudo ufw allow 80/tcp


#### Palvelimen ohjelmien päivitys
- Palvelimen ohjelmat voidaan päivittää komennoilla:
    $ sudo apt-get update
    $ sudo apt-get upgrade
    $ sudo apt-get dist-upgrade

- Lähteet: https://susannalehto.fi/2022/teoriasta-kaytantoon-pilvipalvelimen-avulla-h4/



## Tehtävä a) Vuokraa oma virtuaalipalvelin haluamaltasi palveluntarjoajalta. 
- Olin tehnyt kaksi hakemus Githubin Educationiin, jotka hylätty. Kolmannella kerralla ei hakemuksen lähetys onnistunut, vaikka olin korjannut tarvittavat toimet hakemuksen hyväksymiseksi. Päädyin siis vuokraamaan tässä tapauksessa omakustanteisesti palvelimen Digital Ouceanilta, koska tässä työajassa en ehtinyt tarpeeksi perehtyä vagrant:n käyttöön. 
- Aluksi reksiteröidyin Githubin käyttäjällä ja lisäsin maksutiedot tililleni.
- Valitsin sivuvalikosta Droplets, jonka jälkeen tuli kuvanmukainen virheilmoitus. Merikaapelien katkosten vuoksi sivu ei toimi, joten pitää kokeilla toista paikkaa. Tässä vaiheessa yritin poistaa maksutietoja, mutta sivusto ei tarjonnut siihen mahdollisuutta, vaikka sivuston ohjeessa kyseisessä paikassa kuuluisi olla delete-painike. Lopulta deaktivoin käyttäjäni ja toivon, että ylimääräisiä maksuja ei ala tililtä lähtemään. 

<img width="1762" height="816" alt="image" src="https://github.com/user-attachments/assets/1756c351-b864-4b67-a7ec-0e9b71a09c4d" />

<img width="1300" height="520" alt="image" src="https://github.com/user-attachments/assets/54b688ec-9876-4fbe-b09b-b260ca4ec873" />


- Seuraava yritys tapahtuu Linoden kautta, jossa kirjauduin vastaavasti Githubin kautta ja sivusto pyysi heti ensimmäiseksi myös maksutietoja.
- Tässä näkymä etusivulta:

<img width="1848" height="874" alt="image" src="https://github.com/user-attachments/assets/2425b4e6-af54-4d1d-9b3c-abc88f83e8e6" />


- Nopeustestin mukaan sopivin kansallisuus oli valita Frankfurt 2, DE, jossa tuli korkeimmat lukemat.
- Sitten valitsin edullisimman tuotepaketin: Shared CPU Linodes 5 $/kk.
- SSH:avaimeen minun tulee perehtyä ja sitä en tässä lisännyt. Käytän Linodea vain nyt kurssin ajan, joten en lisännyt Details-osioon mitään.
- Kävin vaihtamassa OS-kohtaan Debian 13, joka minulla on verkkotietokoneessakin käytössä. Tässä oli oletuksena tuo Ubuntu. Debiania oli tarjolla 11-13, josta valitsin uusimman.
- Mahdollisimman vähän lisätoimintoja, jotta kokeilu pysyisi yksinkertaisena ja edullisena.

<img width="1551" height="729" alt="image" src="https://github.com/user-attachments/assets/62ddc172-8e54-4e92-9744-a316c91758fa" />

<img width="734" height="879" alt="image" src="https://github.com/user-attachments/assets/6d49b055-d907-4783-89cb-91e892728154" />

<img width="1590" height="851" alt="image" src="https://github.com/user-attachments/assets/65694399-ac96-419f-9559-94b9bc038b39" />


- Noin minuutin odotuksen jälkeen boottaus oli valmis ja etusivunäkymä tällainen:
<img width="1584" height="813" alt="image" src="https://github.com/user-attachments/assets/73ef163a-8890-45f5-abd7-90dda196c252" />


- Virtuaalipalvelimen vuokraus on nyt hoidettu ja enää jäljellä oli domainnimen vuokraaminen.
- Vuokrasin domainnimen NameCheapilta. Hintaeroa ei juurikaan ollut .me tai .com alkuiseen ja valitsin siis .com. Ennen nimen ostoa tuli ensin rekisteröityä. Sivusto tarjosi promokoodia, jolla sain tämän vuodeksi hintaan 5,54 euroa. Mitään ylimääräistä en tässäkään osta lisäksi.

<img width="1736" height="837" alt="image" src="https://github.com/user-attachments/assets/8d940eb7-0f2b-43ce-926d-2b092de2a5db" />


- Seuraavaksi domainnimi tuli yhdistää Linodelta hankitulle virtuaalipalvelimelle. Poistin kaikki turhat Host records -listalla olleet tiedostot. Sitten tein uuden tiedoston, jonka on tarkoitus ohjata domainnimi virtuaalipalvelimeni IP-osoitteeseen. Klikkasin punaista tekstiä Add new record ja lisäsin uudet tiedostot, joiden arvoksi asetin virtuaalipalvelimen IP-osoitteen ja TTL-sarakkeeseen arvoksi 5 minuuttia, jotta muutettuja tietoja haettaisiin 5 minuutin välein.

<img width="1810" height="903" alt="image" src="https://github.com/user-attachments/assets/ad32d38a-751b-48eb-95ba-d783eabebb00" />

<img width="1457" height="787" alt="image" src="https://github.com/user-attachments/assets/86480f08-043a-4ae0-b6d6-df7ba6eae51e" />




## Tehtävä b) Tee alkutoimet omalla virtuaalipalvelimellasi: tulimuuri päälle, root-tunnus kiinni, ohjelmien päivitys.
- Tero Karvisen ohjeella: https://terokarvinen.com/2017/first-steps-on-a-new-virtual-private-server-an-example-on-digitalocean/ tuli ensimmäiset haasteet vastaan. Kokeilin sulkea virtuaalikoneen kokonaan Shut downista, jos tämä auttaisi. Sama ilmoitus kuitenkin toistuu aina noin 1 min viiveellä. 

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/a127e64f-d15e-45bd-85bd-a1b0ebea41c1" />

Tämän jälkeen löysin Youtube-videon, jonka avulla koitin suorittaa: https://www.youtube.com/watch?v=KEK-ZxrGxMA 

<img width="976" height="891" alt="image" src="https://github.com/user-attachments/assets/c79c87ad-cb67-4a76-958b-bb5b43fd62b6" />


- Nyt koitin videon ohjetta selatessa kuitenkin tehdä root-avain, joka voisi auttaa Linoden kautta kirjautumiseen. Erona vielä huomasin, että omani oli encrypted-tilassa, jonka kävin vielä samasta paikasta poistamassa. 

<img width="1575" height="526" alt="image" src="https://github.com/user-attachments/assets/e90cf6f1-d4ee-4897-b02a-e70bc46d5eb4" />

<img width="1174" height="794" alt="image" src="https://github.com/user-attachments/assets/993ccaa1-d3fa-4656-ad78-b84630f803ec" />

<img width="1583" height="658" alt="image" src="https://github.com/user-attachments/assets/9a2a09df-119c-4f3a-9309-0fc961b6ae48" />


- Opettaja Tero Karvisen ohjeissa havaitsin lukevan, että root@10.0.0.1 osiossa tuleekin poistaa 10.0.0.1 ja lisätä siihen oma IP-osoite. Nyt lisäsin sen ja tuli kuvanmukainen ilmoitus.

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/4b04087c-8552-4306-853b-4f58ae4972d5" />


- En ole varma johtuuko tämä encryptauksen poisottamisesta, joten menen laittamaan sen takaisin. Tämä ei kuitenkaan vaikuta mihinkään. Linodesin omassa komentoikkunassa ei ole mahdollista nuolinäppäimillä liikkua ja en löydä ohjeistusta, miten siellä tulisi eri tavalla liikkua. Youtube-videossa käyttäjä kirjoittaa alkuun root, joka ohjaa suoraan kysymään salasanaa root-käyttäjälle. Minulla ei anna vaihtoehtoa liikkumiseen ja kokeilin kirjoittaa root annettuun kohtaan ja root-salasanan antamisella ei ole merkitystä ja en pääse asiassa eteenpäin.
- Kokeilen komentoriviin ilmestyneen ilmoituksen mukaan toimia ja toivoin parasta:

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/c605dce9-8b83-4e94-9422-d8ea0fb9671b" />


- Tässä jo kohta 3h kotitehtäviä tehdessä meinasi hämmennys iskeä, kunnes pääsin eteenpäin hieman:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/fc4fec09-285b-466e-bff5-fb83e120c765" />

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/07e69a51-c046-4ebb-b479-c29e3ac4de64" />


- Suljin terminaalin ja kokeilin jatkaa tästä eteenpäin, kun root@-komennolla kirjauduin äsken sisään:
<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/12306d55-7f42-4719-95ec-ddb5c40328ea" />

- Tämän jälkeen tein ensin käyttäjän ja sitten käyttäjästä pääkäyttäjän komennoilla, mutta nämä olivatkin jo aiemmin tehtyjä. Admin-komentoa ei kuitenkaan jostain syystä tunnistettu:

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/14fa96b9-2dfc-4185-b619-58e6fc203b2f" />

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/e9608c0f-2eab-4a0a-83d6-442ae8de51f7" />


- Pääkäyttäjän luominen ei täysin onnistunut. Jatkan eteenpäin tästä ja kysyn oppitunnilla neuvoa asiaan lukitsemalla juuren käyttäjän, mutta ilmoituksessa kerrotaan vain sen olemassaolosta. 

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/d7141c36-ebd0-47c7-ad3a-1d5861fe4a13" />



### Ohjelmien päivitys

- Jatkan eteenpäin päivittämällä ohjelmat ja havaitsen päivityksissä menevän poikkeavan pitkään. Ennen ollut muutaman sekunnin, nyt useamman minuutin. 
          $ sudo apt-get update
          $ sudo apt-get upgrade


- Palomuuriin reikä julkista palvelinta varten:
          sudo uwf allow 80/tcp


### Tulimuuri päälle

- HUOM!! Huomasin oikovani tehtävässä ja palomuuri jäi erikseen asentamatta root-käyttäjänä. Normikäyttäjänä näytti, että tämä olisi jo asennettu. Nyt kokeilin uudestaan tehdä reiän palomuuriin:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/a21d08d9-3fa6-4631-8b84-693c9f108bf9" />

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/55813aad-6fa0-42ad-9077-2f66d4364eba" />


- Vaikka nyt pääsinkin eteenpäin, ei kuitenkaan SHH-yhteydellä saa käyttäjäni tunnuksia avatuksi:
<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/97991d2f-6836-48eb-b4bd-31c53922b07a" />


- Kokeilin domainnimeni pingaamista komennolla:
          ping inkaheinonen.com

- Pingaus kesti kauan ja suljin terminaalin

  <img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/49b861fa-9cda-424d-b9e1-e8bab444db6b" />


### Root-kiinni
- Juuren lukitus komennolla:
          $ sudo usermod --lock root


## Tehtävä c) Asenna weppipalvelin omalle virtuaalipalvelimellesi. Korvaa testisivu. Kokeile, että se näkyy julkisesti. Kokeile myös eri koneelta, esim kännykältä.


- Apache2 oli jo asennettu ja näkymä kokeillessani nettisivua inkaheinonen.com. Tässä en jostain syystä pysty lisäämään reikää palomuuriin. Tämä voi olla syy, miksi sivua ei pysty lataamaan. Tämä pitää myös oppitunnilla selvittää ja kysyä. 

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/68df4341-290d-4ee4-b9d3-795d8e9be081" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/4fefc96a-427f-4906-b46e-6d348c066e43" />
