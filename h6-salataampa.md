## Tehtävä x) Lue ja tiivistä
- Let's Encrypt:lta saa ilmaisia TLS/SSL-varmenteita, joiden avulla voidaan varmistaa verkkosivustojen HTTPS-salaus. Toiminta perustuu ACME-protokollaan.

- Let's Encrypt pystyy tunnistamaan julkisen avaimen avulla ACME-asiakasohjelman.

- Validointiprosessi on kaksi vaiheinen. Ensimmäisessä vaiheessa ACME-asiakasohjelma todistaa varmenteiden myöntäjälle web-palvelimen hallitsevan domainia. Seuraavaksi asiakasohjelma voi pyytää tai peruuttaa varmenteita kyseiselle domainille.

- Validointiprosessi ei voi käyttää HTTPS:ää, jonka vuoksi se on altis tietyille hyökkäyksille.

- Asiakas voi pyytää sertifikaatin käyttäen CSR:ää, kun hänet on varmennettu ja saanut oikeudet toimia tietylle domainille (Certificate Signing Request).

- Lähteet: https://letsencrypt.org/how-it-works/, https://go-acme.github.io/lego/usage/cli/obtain-a-certificate/index.html#using-an-existing-running-web-server, https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample


## Tehtävä a) Let's. Hanki ja asenna palvelimellesi ilmainen TLS-sertifikaatti Let's Encryptilta. Osoita, että se toimii.
- Aloitan tekemällä reiän palomuuriin:

<img width="583" height="287" alt="image" src="https://github.com/user-attachments/assets/7d16ec7a-1359-4cbe-b2d5-795faaa92791" />

<img width="568" height="170" alt="image" src="https://github.com/user-attachments/assets/1622a7bb-25ba-41be-8e8d-46e0c29047a5" />

- Varmistin, että kaikki tarvittavat kunnossa:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/6b4cd6bf-5dd6-402d-9b61-36d20234207e" />


- Sitten latasin certbotin:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/79614f10-d391-4951-8c95-8d0c66a9ddf9" />

- Sertifikaatin lisääminen domainille, mutta tässä tulee virheilmoitus:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/f939796a-911e-459b-a986-30560e232275" />

- Seuraavaksi koitin päivittää lataukset komennolla: sudo apt-get upgrade, mutta tämä ei auttanut:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/e1274eb2-2fdc-4b18-9488-59bad7d99a8b" />

- Tämän jälkeen olin aikomassa katsoa tiedostoa, mitä se pitää sisällään, olisiko siellä korjattavaa:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/9e87b42d-f178-40f6-91d7-8ee64b64b3d3" />

- Uutta yritystä eri komentomuodolla. Nyt olen jo lähempänä:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/05ddfe50-b815-467d-a587-7f42e6533e2d" />








## Tehtävä b) A-rating. Testaa oma sivusi TLS jollain yleisellä laadunvarmistustyökalulla, esim. SSLLabs 
