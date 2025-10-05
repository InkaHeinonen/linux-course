# Tehtävänanto h3

## Tehtävät x)

#### Name-based vs. IP-based Virtual Hosts
- Nettisivua voi ylläpitää eri tavoin, ja sivua perustaessa on syytä selvittää, mikä tapa on tarpeeseen sopivin. 
- Nimiperustaisessa virtuaalipalvelimessa tulee ylläpitäjän itse ilmoittaa ylläpidon nimen osana HTTP-otsikoita. Näin useampi ylläpitäjä voi jakaa saman IP-osoitteen. Nimi-perustainen on yksinkertaisempi, koska siinä itse tulee määrittää DNS-palvelun yhdistämään jokaisen ylläpitäjän nimi oikeaan IP-osoitteeseen ja määrittää Apache HTTP -palvelin tunnistamaan eri nimet. 
- IP-perusteisessa virtuaalipalvelimet käyttävät yhteyden IP-osoitetta määrittääkseen oikean virtuaalipalvelimen, jonka vuoksi jokaiselle palvelimelle on oltava erillinen IP-osoite.

#### Miten palvelin valitsee oikean nimiperustaisen virtuaalisen ylläpitäjän?
- Nimiperusteisen virtuaalikoneen selvityksen ensimmäinen vaihe on IP-perusteisen selvitys. 
- Nimi-perusteinen virtuaalikoneen selvitys rajaa sopivimmat vaihtoehdot parhaaseen IP-perustaiseen osumaan, jonka jälkeen nimi-perusteinen virtuaalikone valitsee sopivimman nimiperusteisen virtuaalikoneen. 
- Kun osumaehdotus saapuu, palvelin löytää parhaiten vastaavan <VirtualHost>- pyynnön jo käytetyn IP-osoitteen ja portin perusteella. Jos useampi kuin yksi virtuaalipalvelin sisältää tämän parhaiten vastaavan osoite- ja porttiyhdistelmän, Apache vertaa ServerName- ja ServerAlias-direktiivejä edelleen pyynnössä olevaan palvelimen nimeen.


- Lähteet: https://httpd.apache.org/docs/2.4/vhosts/name-based.html, https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address/



## Tehtävä a) Oman webbipalvelimen testaus localhost osoitteesta
- Webbipalvelimen testaus osoitteesta: http://site1.com:

<img width="1282" height="775" alt="image" src="https://github.com/user-attachments/assets/7b612e38-249c-44b0-9d21-5a3ff52458b4" />


- Sama näkymä komentoriviltä haettuna:

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/a5fbb856-a2bd-4031-8119-7ac3f4c95ed4" />



## Tehtävä b) Lokit
- Lokitiedostoja löydän esimerkiksi komennolla cd /var/log/, jonka jälkeen komennolla ls -l:

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/4e20c154-32db-42c1-8ecb-07817e555a25" />


- En kuitenkaan osaa etsiä reaaliaikaisia lokitietoja webbisivulla vierailusta. Tästä kuvasta katsottuna, ensimmäiset luvut vasemmalta ovat IP-osoitteeni, sitten päivämäärä. Lopussa näkyy webbiselain, jota käytetty kyseisenä ajankohtana. 

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/a10c8b9c-e543-4afa-92c1-0474f8d379c8" />



## Tehtävä c) Etusivu uusiksi
- Uuden sivun luominen lähteenä: https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address/

- Kuvassa tulee komentokehoite:you need to run systemctl reload apache2. Tämän jälkeen tuli salasanapyyntö, jonka jälkeen komentoja pystyi taas normaalisti lisäämään. 

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/cb16091d-58d8-4bbb-b561-a6b7f3feb335" />


- Tässä tuli ongelmia ja en löydä, mihin tuo pitäisi sijoittaa. Tarkisin ja tässä olen nyt ilmeisesti korvannut edellisen sivun tällä uudella, koska sivun tekstiksi tuli Deafault eikä enää se edellinen teksti. Kuvassa päätöntä ohjeiden seuraamista, koska todennäköisesti olen nyt korvannut uuden sivun vanhalla ja en saa tästä asiaa edistettyä. Joten olen jumissa.

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/61a0aeb9-8a6a-41e8-86c3-f07e05c5c741" />


- Tarkistin asiaa, niin samat oikeudet näkyvät site1.com ja hattu.example.com sivuilla:

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/35524aad-6f9d-434a-9c54-255993deac2b" />


- Nyt tulikin mielenkiintoinen asia eteen koittaessani saada ensimmäistä sivustoa pois päältä:

<img width="1067" height="435" alt="image" src="https://github.com/user-attachments/assets/b93f2917-2777-407f-8ce7-8f68040bccc5" />

<img width="1282" height="775" alt="image" src="https://github.com/user-attachments/assets/dab28bc8-62ab-4b7a-b58a-cd2cf3f64a3c" />

- Jotta en sekoita asiaa ``, jätän tämän tähän ja toivottavasti saan selville, miten tämä tulisi oikeaoppisesti tehdä. Tarkistin, joten teksti index.html:ssä on korvaantunut sanalla 'Default' ja jatkan tästä seuraavaan tehtävään. Tässä vaiheessa olen 2,5h lukenut internettiä ja koittanut tehtäviä tehdä tehtävästä a) alkaen. 

<img width="1067" height="485" alt="image" src="https://github.com/user-attachments/assets/1000824b-bdad-4e90-b8f7-cc4a87a0d964" />



## Tehtävä e) Validi HTML5-sivu
- Lähteenä: https://terokarvinen.com/2012/short-html5-page/

- Yritän kuvassa avata vanhaa index.html tiedostoa luodakseni sinne nettisivulle näkyvää materiaalia. Haasteena on tämä ja edellisellä yrittämällä tuli tieto, että ei ole oikeuksia muokata tiedostoa ilman sudoa, jonka jälkeen micron näkymä meni jumiin. Uudella yrittämällä tämä suostui sudona tallentamaan. 

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/62deac7e-f2a1-4d15-a8f6-e54be9c37a1b" />

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/b7ce3315-1251-4ed9-87ce-9145e005f33b" />


- Sudon kanssa muokatessa sain luotua perusmallisen sivuston, jonka tekstilähteenä: https://www.lipsum.com/. 

<img width="1282" height="775" alt="image" src="https://github.com/user-attachments/assets/6a629f4f-fc1b-4d35-b4a5-6f9a447e1dce" />



## Tehtävä f) curl -I' ja 'curl' -komennot
- Curl-komennolla saa tiedoston auki komentoriville, jonka avulla sen voi nopeasti lukea. Tämä on kätevää, jos tiedostossa ei ole paljoa sisältöä. Curl -I komennolla puolestaan saa auki ihan eri näkymän ja siitä saa tietoa esimerkiksi tiedostotyypistä, merkkimäärästä, päivämäärästä, serveristä ja muokkauspäivästä. 

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/c92faa30-49de-45cf-bdc1-9fe8fd8cf612" />

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/e8391bdc-2c01-4cb9-ab5d-33fe887fd08b" />


## Vapaaehtoinen tehtävä

<img width="1203" height="437" alt="image" src="https://github.com/user-attachments/assets/366e0a30-2a6c-4ea2-aa82-06da5e735789" />


### Lähteet:
- https://terokarvinen.com/linux-palvelimet/
- https://terokarvinen.com/2012/short-html5-page/
- https://httpd.apache.org/docs/2.4/vhosts/name-based.html
- https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address/
