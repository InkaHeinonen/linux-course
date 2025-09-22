# Tehtävä h5 Nimekäs
- tämän kerran lukuläksy on etsiä itse laadukkaat lähteet kaikkiin vieraisiin käsitteisiin ja työkaluihin. Vastaukset tulevat osaksi analyysiä ja tulkintaa, erillisiä tiivistelmiä ei tällä kertaa tehdä

- alidomain = Alidomain on verkkotunnuksen liite, kuten osoitteessa inkaheinonen.com alidomainena voisi olla 'about' (about.inkaheinonen.com)
- DNS = DNS on internetin nimipalvelujärjestelmä, joka kääntää helpommin tunnetut nettisivut IP-osoitteiksi. Esimerkiksi inkaheinonen.com kääntyy IP-osoitettaanu numeraaliseksi osoitteeksi 10.0.0.1 etc.
- dig-komento = 
- host-komento = 
  
- Lähteet: https://tnnet.fi/blogi/dns-hallinta-mita-se-on/ 


### Tehtävä a) Nimi
Laita julkinen nimi osoittamaan omaan koneeseesi.

- Tehtävän olinkin tehnyt jo edelliseen tehtävään, joten kopioin sieltä tähän tehdyt toimet.

- Vuokrasin domainnimen NameCheapilta. Hintaeroa ei juurikaan ollut .me tai .com alkuiseen ja valitsin siis .com. Ennen nimen ostoa tuli ensin rekisteröityä. Sivusto tarjosi promokoodia, jolla sain tämän vuodeksi hintaan 5,54 euroa. Mitään ylimääräistä en tässäkään osta lisäksi.

<img width="1736" height="837" alt="image" src="https://github.com/user-attachments/assets/8d940eb7-0f2b-43ce-926d-2b092de2a5db" />


- Seuraavaksi domainnimi tuli yhdistää Linodelta hankitulle virtuaalipalvelimelle. Poistin kaikki turhat Host records -listalla olleet tiedostot. Sitten tein uuden tiedoston, jonka on tarkoitus ohjata domainnimi virtuaalipalvelimeni IP-osoitteeseen. Klikkasin punaista tekstiä Add new record ja lisäsin uudet tiedostot, joiden arvoksi asetin virtuaalipalvelimen IP-osoitteen ja TTL-sarakkeeseen arvoksi 5 minuuttia, jotta muutettuja tietoja haettaisiin 5 minuutin välein.

<img width="1810" height="903" alt="image" src="https://github.com/user-attachments/assets/ad32d38a-751b-48eb-95ba-d783eabebb00" />

<img width="1457" height="787" alt="image" src="https://github.com/user-attachments/assets/86480f08-043a-4ae0-b6d6-df7ba6eae51e" />




### Tehtävä b) Alidomain
Tee kaksi uutta alidomainia, jotka osoittava omaan koneeseesi. 
- Lähteenä: https://www.namecheap.com/support/knowledgebase/article.aspx/9776/2237/how-to-create-a-subdomain-for-my-domain, https://www.namecheap.com/support/knowledgebase/article.aspx/579/2237/which-record-type-option-should-i-choose-for-the-information-im-about-to-enter https://www.namecheap.com/support/knowledgebase/article.aspx/319/2237/how-can-i-set-up-an-a-address-record-for-my-domain

- Avasin Namecheap-sivustosta Domain List:n auki ja sieltä painoin Manage sekä Advanced DNS.
- Lisäsin Type-kohtaan CNAME Record, josta Host-kohtaan siirsin www ja Value-kohtaan inkaheinonen.com. Tämä toimii testattuna oikein.
- Kahteen muuhun kohtaan Type-osiossa on  A Record ja Host-kohdissa @ sekä about. Näissä on Value-osiossa oma IP-osoitteeni. Alussa pidin TTL 5minuutissa ja testasin, onko toimivuudessa eroa, onko se automatic. Eroa ei kuitenkin havaittu ja edelleenkään about.inkaheinonen.com ei toimi. 

<img width="1044" height="275" alt="image" src="https://github.com/user-attachments/assets/cb003b85-4994-4888-b02f-9b125a59673f" />

<img width="1225" height="633" alt="image" src="https://github.com/user-attachments/assets/7b014aad-2ed6-4ae5-a974-527b4ee55d2e" />

- Testasin seuraavaksi ohjeiden mukaisesti tehdyt toimet, toimiiko myös sivut www- sekä about.-näkymillä:
<img width="531" height="151" alt="image" src="https://github.com/user-attachments/assets/ce39b8c6-f326-4e12-82fc-21b366124be1" />

<img width="1059" height="579" alt="image" src="https://github.com/user-attachments/assets/4da87b09-e52a-45e7-9176-7963bb07b3a8" />


- Asia korjaantuikin, kun päivitin Namecheap-sivun.

<img width="522" height="147" alt="image" src="https://github.com/user-attachments/assets/ce4350b6-0cf6-432f-abda-ae85c29d37b2" />





### Tehtävä c) Tutki jonkin nimen DNS-tietoja 'host' ja 'dig'-komennoilla. 
- Asensin työasemalleni "DNS Utilities" -paketin, jotta pääsen tarkastelemaan host- ja dig-komennoilla DNS-tietoja.
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/aad798fc-f2ce-4f13-9a57-05a3c525ad70" />

- Kokeilin komentoa 'dig inkaheinonen.com' ja tästä tuli virheilmoituksena Not command found.
- Latasin bind+-lisäsoan vielä kuvanmukaisesti:

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/cc49331d-808b-44ab-b086-c8bd6a6c536d" />


- Manuaalin aukeiseminen komennollla: 'man host'.
- Kuvassa manuaali komennosta 'host':
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/fbaf8c70-542d-437c-bebb-cc18ce38df6e" />

- Huomasin, että olin ladannut paketin, mutta unohtanut antaa komennon 'sudo apt-get upgrade'. Nyt dig-komento toimii. Ennen tätä näkymä oli kuvan mukainen:
<img width="454" height="78" alt="image" src="https://github.com/user-attachments/assets/750fce81-7cee-4c39-a64f-7bf9eca35562" />

- Manuaalin aukaiseminen komennolla: 'man dig'.
- Kuvassa manuaali komennosta 'dig':
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/3674c552-becf-4a34-b7f9-1fd4917f5b47" />
- Dig-komenti näyttää hieman enemmän tietoja ja host-komenti alustavasti vain IP-osoitteen sekä sähköpostin välitykseen liittyviä tietoja. 

#### Dig-komennon tulkinta
- Käytän kuvassa esimerkkikuvaa allaolevista internet-sivuista.
<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/f8250565-4c3e-4ed1-adfc-06425ef3e582" />

- HEADER-osio kertoo, onnistuiko pyyntö ja kuinka monta tietoa on kussakin osiossa. Kuvassa lukee mm. NOERROR, joten pyyntö     onnistui. 

- QUESTION-osio kertoo, mitä pyysin, eli tietoa sivusta inkaheinonen.com

- ANSWER-osio kertoo DNS-serverilta saadut tiedot, kuten IP-osoitteen ja datan tyypit.

- Lopussa näkyy, kuinka kauan tietojen haku kesti, serveri, milloin tietojen haku oli suoritettu sekä viestin koko. 


####  Tulokset sivustolta www.inkaheinonen.com host- ja dig-komennoilla
##### Host-komennolla
- Kuvassa näkyy: 
<img width="722" height="207" alt="image" src="https://github.com/user-attachments/assets/5d8b6376-cdf0-462b-9c75-686900823921" />



##### Dig-komennolla
- Kuvassa näkyy: 
<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/8da4c440-5016-4239-9fb6-859482bf0951" />




#### Tulokset sivustolta about.inkaheinonen.com host- ja dig-komennoilla
##### Host-komennolla
- Kuvassa näkyy: 
<img width="513" height="86" alt="image" src="https://github.com/user-attachments/assets/8727d97c-03cb-42c3-afab-82d65d03ac77" />


##### Dig-komennolla
- Kuvassa näkyy:
- 
<img width="710" height="443" alt="image" src="https://github.com/user-attachments/assets/0e572071-cb5e-4603-9bfd-dfc51ed69682" />


#### Tulokset sivustolta www.kromfohrlander.fi (koirani rotuyhdistyksen www-sivut) host- ja dig-komennoilla
##### Host-komennolla
- Kuvassa näkyy:

<img width="653" height="202" alt="image" src="https://github.com/user-attachments/assets/d95a96b0-3baf-4f5d-8ea8-8652d375a392" />


##### Dig-komennolla
- Kuvassa näkyy:

<img width="703" height="465" alt="image" src="https://github.com/user-attachments/assets/14697649-80af-43a1-9af3-6bd9a8e3543b" />


#### Tulokset sivustolta www.prisma.fi host- ja dig-komennoilla
##### Host-komennolla
- Kuvassa näkyy:

<img width="533" height="122" alt="image" src="https://github.com/user-attachments/assets/247e6056-74f1-4cfe-953f-cde52f2145a9" />


##### Dig-komennolla
- Kuvassa näkyy:
- 
<img width="702" height="451" alt="image" src="https://github.com/user-attachments/assets/f7c41c69-8b80-4458-8223-514e19e623fe" />


- Lähteet: https://phoenixnap.com/kb/linux-host, https://medium.com/@adil_94543/dns-resolution-using-linux-command-74d43fa642de, https://blog.globalping.io/how-to-read-a-dig-result-a-guide-for-network-novices/ 
