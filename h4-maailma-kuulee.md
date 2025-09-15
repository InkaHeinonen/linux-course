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


- Seuraava yritys tapahtuu Linoden kautta, jossa kirjauduin vastaavasti Githubin kautta ja sivusto pyysi heti ensimmäiseksi myös maksutietoja. Kävin vaihtamassa OS-kohtaan Debian 13, joka minulla on verkkotietokoneessakin käytössä. Tässä oli oletuksena tuo Ubuntu. Debiania oli tarjolla 11-13, josta valitsin uusimman. 
- Tässä näkymä etusivulta:

<img width="1848" height="874" alt="image" src="https://github.com/user-attachments/assets/2425b4e6-af54-4d1d-9b3c-abc88f83e8e6" />

- Nopeustestin mukaan sopivin kansallisuus oli valita Frankfurt 2, DE, jossa tuli korkeimmat lukemat.
- Sitten valitsin edullisimman tuotepaketin: Shared CPU Linodes 5 $/kk.
- SSH:avaimeen minun tulee perehtyä ja sitä en tässä lisännyt. Käytän Linodea vain nyt kurssin ajan, joten en lisännyt Details-osioon mitään. 

<img width="1551" height="729" alt="image" src="https://github.com/user-attachments/assets/62ddc172-8e54-4e92-9744-a316c91758fa" />

<img width="734" height="879" alt="image" src="https://github.com/user-attachments/assets/6d49b055-d907-4783-89cb-91e892728154" />







## Tehtävä b) Tee alkutoimet omalla virtuaalipalvelimellasi: tulimuuri päälle, root-tunnus kiinni, ohjelmien päivitys.



## Tehtävä c) Asenna weppipalvelin omalle virtuaalipalvelimellesi. Korvaa testisivu. Kokeile, että se näkyy julkisesti. Kokeile myös eri koneelta, esim kännykältä.
