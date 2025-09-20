# Tehtävä h5 Nimekäs
- tämän kerran lukuläksy on etsiä itse laadukkaat lähteet kaikkiin vieraisiin käsitteisiin ja työkaluihin. Vastaukset tulevat osaksi analyysiä ja tulkintaa, erillisiä tiivistelmiä ei tällä kertaa tehdä

- alidomain = Alidomain on verkkotunnuksen liite, kuten osoitteessa inkaheinonen.com alidomainena voisi olla 'about' (about.inkaheinonen.com)
- DNS = DNS on internetin nimipalvelujärjestelmä, joka kääntää helpommin tunnetut nettisivut IP-osoitteiksi. Esimerkiksi inkaheinonen.com kääntyy IP-osoitettaanu numeraaliseksi osoitteeksi 10.0.0.1 etc. 
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

####  Tulokset sivustolta www.inkaheinonen.com host- ja dig-komennoilla
-





#### Tulokset sivustolta about.inkaheinonen.com host- ja dig-komennoilla
-




#### Tulokset sivustolta (pienyrittäjä) host- ja dig-komennoilla
- 



#### Tulokset sivustolta (suuryrittäjä) host- ja dig-komennoilla



