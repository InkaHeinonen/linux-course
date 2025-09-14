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



## Tehtävä b) Tee alkutoimet omalla virtuaalipalvelimellasi: tulimuuri päälle, root-tunnus kiinni, ohjelmien päivitys.



## Tehtävä c) Asenna weppipalvelin omalle virtuaalipalvelimellesi. Korvaa testisivu. Kokeile, että se näkyy julkisesti. Kokeile myös eri koneelta, esim kännykältä.
