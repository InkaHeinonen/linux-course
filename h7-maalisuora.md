# Tehtävänanto h7

## Tehtävä a) Kirjoita ja aja "Hei maailma" kolmella kielellä.

### Bash
- Aloitin scriptin luomisen luomalla helloworld.sh tiedoston ja tarkastin, että se löytyy luettelosta. 

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/1f3c4139-6ead-4bc3-98c4-b93a532a0a09" />

<img width="817" height="432" alt="image" src="https://github.com/user-attachments/assets/d9bffa1e-65f0-4eb7-b560-70ebb1d72a8a" />

- Kuten ensimmäisestä kuvasta näkyy, oikeudet ovat scriptin ajamiseen jo heti oikeat, joten niitä ei tarvitse muuttaa komennolla: chmod a+x helloworld.sh -komennolla. Tämän saatoin tehdä tunnilla jo, joten kotitehtäviä tehdessä se olikin jo valmiina oikein.
- Tässä kuvassa näkyy, että scripti ei vielä toimi tiedoston sijaitessa vielä väärässä paikassa:
<img width="398" height="58" alt="image" src="https://github.com/user-attachments/assets/5bfc9092-a704-4a75-a30e-1fa219f0d34c" />

- Seuraavaksi koitan ajaa scriptiä kotihakemiston kautta eri komennolla, mutta scripti ei toimi vieläkään ja käyn tekstitiedostosta poistamassa kommentin:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/06b98c27-20bc-4a5e-9a0f-46a383704665" />
- Ja kuten näkyy, niin nyt tämä toimii:
<img width="1092" height="330" alt="image" src="https://github.com/user-attachments/assets/ad1430d7-8410-4d35-a8c1-0b9c2f44c90c" />



### Python3
- Loin tekstitiedoston komennolla: micro helloworld.py:
<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/c2a23d14-6baa-49ec-b2c3-80dcf064bc50" />

- Testasin ja komento toimii ilman oikeuden määritystä:
<img width="817" height="371" alt="image" src="https://github.com/user-attachments/assets/d4ae28b5-6762-425b-b8eb-c4f6217810b3" />



### C++
- Aloitin päivittämällä asennuspaketit ja asensin ohjeen mukaisesti tiedoston build-essential-ohjelmiston.
<img width="817" height="409" alt="image" src="https://github.com/user-attachments/assets/9c80b9c8-9cb0-405f-af09-94fb3a1afbd2" />

- Sitten loin tekstitiedoston komennolla: micro helloworld.cpp
<img width="817" height="368" alt="image" src="https://github.com/user-attachments/assets/981aebb7-be60-4c72-a26e-2db536b41632" />

- Sitten käänsin GNU C++ kääntäjää käyttäen lähdekoodin suoritettavaksi ohjelmaksi komennolla: g++ helloworld.cpp -o helloworld
- Lopulta suoritin ohjelman ja se toimii myös ilman oikeuksien määrittelemistä:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/07c79332-1c90-466e-8c04-0e9563485f3c" />


## Tehtävä b) Lähdeviitteet. Tarkista ja tarvittaessa lisää lähdeviitteet kaikkiin raportteihisi h1 alkaen.
- Lähdeviitteet käyty korjaamassa jokaiseen tehtävään.


## Tehtävä c) Laita Linuxiin uusi, itse tekemäsi komento niin, että kaikki käyttäjät voivat ajaa sitä.
- Loin tiedoston sudolla julkiseen kansiopaikkaan:
<img width="596" height="118" alt="image" src="https://github.com/user-attachments/assets/f8076d99-b64d-4201-a51a-79f4d0a82d44" />

- Tekstitiedostoon lisäsin kuvan mukaisen sisällön:
<img width="457" height="209" alt="image" src="https://github.com/user-attachments/assets/fa738868-dab1-4db8-99fe-ca9092cc8d0b" />

- Seuraavaksi annoin oikeudet tiedostolle komennolla: chmod a+x /usr/local/bin/listaus.sh ja ajoin komennon:
<img width="434" height="106" alt="image" src="https://github.com/user-attachments/assets/2b0d0244-2f06-47e8-b07d-d7ec59f34544" />





### Lähteet:
- https://terokarvinen.com/linux-palvelimet/
- https://terokarvinen.com/2018/hello-python3-bash-c-c-go-lua-ruby-java-programming-languages-on-ubuntu-18-04/ 
- https://github.com/johannaheinonen/johanna-test-repo/blob/main/linux-01102025.md
