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

<img width="1282" height="775" alt="image" src="https://github.com/user-attachments/assets/f719b671-67f0-427c-9975-c565e532deae" />

- Minun pitää vielä perehtyä, mistä löydän tiedoston, josta pääsisin muuttamaan teksisisällön. Sama näkymä komentoriviltä haettuna:

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/6d2bc761-6929-4790-b34f-9bd96315c213" />




