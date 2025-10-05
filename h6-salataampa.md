# Tehtävänanto h6

## Tehtävä x) Lue ja tiivistä
- Let's Encrypt:lta saa ilmaisia TLS/SSL-varmenteita, joiden avulla voidaan varmistaa verkkosivustojen HTTPS-salaus. Toiminta perustuu ACME-protokollaan.

- Let's Encrypt pystyy tunnistamaan julkisen avaimen avulla ACME-asiakasohjelman.

- Validointiprosessi on kaksi vaiheinen. Ensimmäisessä vaiheessa ACME-asiakasohjelma todistaa varmenteiden myöntäjälle web-palvelimen hallitsevan domainia. Seuraavaksi asiakasohjelma voi pyytää tai peruuttaa varmenteita kyseiselle domainille.

- Validointiprosessi ei voi käyttää HTTPS:ää, jonka vuoksi se on altis tietyille hyökkäyksille.

- Asiakas voi pyytää sertifikaatin käyttäen CSR:ää, kun hänet on varmennettu ja saanut oikeudet toimia tietylle domainille (Certificate Signing Request).

- SSL manuaalinen kongfiguraatio Apachella vaatii vähintään seuraavat:

        LoadModule ssl_module modules/mod_ssl.so
        
        Listen 443
        <VirtualHost *:443>
            ServerName www.example.com
            SSLEngine on
            SSLCertificateFile "/path/to/www.example.com.cert"
            SSLCertificateKeyFile "/path/to/www.example.com.key"
        </VirtualHost>

- Lähteet: https://letsencrypt.org/how-it-works/, https://go-acme.github.io/lego/usage/cli/obtain-a-certificate/index.html#using-an-existing-running-web-server, https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample


## Tehtävä a) Let's. Hanki ja asenna palvelimellesi ilmainen TLS-sertifikaatti Let's Encryptilta. Osoita, että se toimii.
- Aloitin potkaisemalla demonia komennolla: sudo systemctl reload apache2.
- Varmistin tietokoneelta ja puhelimelta, että sivu toimii. Kaikki päällisin puolin kunnossa.
- Sitten tein palomuuriin reiän:

<img width="583" height="287" alt="image" src="https://github.com/user-attachments/assets/7d16ec7a-1359-4cbe-b2d5-795faaa92791" />

<img width="568" height="170" alt="image" src="https://github.com/user-attachments/assets/1622a7bb-25ba-41be-8e8d-46e0c29047a5" />

- Varmistin, että kaikki tarvittavat kunnossa:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/6b4cd6bf-5dd6-402d-9b61-36d20234207e" />


- Sitten latasin certbotin:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/79614f10-d391-4951-8c95-8d0c66a9ddf9" />

- Sertifikaatin lisääminen domainille, mutta tässä tulee virheilmoitus:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/f939796a-911e-459b-a986-30560e232275" />

- Tämän jälkeen olin aikomassa katsoa tiedostoa, mitä se pitää sisällään, olisiko siellä korjattavaa:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/9e87b42d-f178-40f6-91d7-8ee64b64b3d3" />

- Uutta yritystä eri komentomuodolla. Nyt olen jo lähempänä:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/05ddfe50-b815-467d-a587-7f42e6533e2d" />

- Käytin päivittämiseen aiemmin vahingossa komentoa: sudo apt-get uograde. Nyt teen sen komennolla kuitenkin: sudo apt-get update:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/adee23f2-f9c1-4953-bb61-e64f78a742e9" />

<img width="817" height="526" alt="image" src="https://github.com/user-attachments/assets/303c2000-d6e9-424e-97ff-b2dddec1d0c8" />

- Tein kansion komennolla: mkdir -p /home/inka/public-sites/inkaheinonen
  
- Tarkistin, mitä index.html kansiossa on ja korjasin tekstejä:
<img width="817" height="347" alt="image" src="https://github.com/user-attachments/assets/ca8c88e7-c6ae-4ff7-b71c-1468483debfa" />

- En ymmärrä, miksi tämä ei nyt toimi ja kokeilin antaa samoja komentoja uudestaan:
<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/796bb9aa-7c9e-4214-baef-b52f02494048" />

- Nyt löytyi todennäköisesti syy:
<img width="610" height="138" alt="image" src="https://github.com/user-attachments/assets/c87f4120-372c-4fcb-9415-a4dca0d75e0c" />

- Menin Linodeen Reboottaamaan kuvassa olevasta 3-pisteen kohdasta: Reboot. Tämä kesti noin 1min. Tämän jälkeen tuli kuitenkin sama ilmoitus, joten tämä ei auttanut yhteyden saamiseksi. Edeltävällä oppitunnilla tähän oli selitys, mikä auttaisi. En internetistä löydä tieto asiaan ja tehtävä jää valitettavasti tähän. 
<img width="1019" height="278" alt="image" src="https://github.com/user-attachments/assets/43769759-df5b-47a8-bfb0-9c94d40f8dd7" />

- Tarkistin alussa olevista lähteistä, onko siellä vinkkejä. Kuten tiivistelmässä lukee, niin konfiguraatio vaatii tietyt tiedot. En tosiaan keksi, mihin nämä tulisivat nyt liittää: 
    - SSL manuaalinen kongfiguraatio Apachella vaatii vähintään seuraavat:

        LoadModule ssl_module modules/mod_ssl.so
        
        Listen 443
        <VirtualHost *:443>
            ServerName www.example.com
            SSLEngine on
            SSLCertificateFile "/path/to/www.example.com.cert"
            SSLCertificateKeyFile "/path/to/www.example.com.key"
        </VirtualHost>




## Tehtävä b) A-rating. Testaa oma sivusi TLS jollain yleisellä laadunvarmistustyökalulla, esim. SSLLabs 
- Tässä vaiheessa testasin TSL -salaukseni luokitusta seuraavalla verkkosivulla: Qualys SSL labs - SSL Server Test. Syötin hakukenttään inkaheinonen.com ja odotin tuloksia.

- Kuten edeltävässä tehtävässä oli havaittavissa yhteysongelmia, niin ne ilmenee myös tässä:
<img width="1282" height="775" alt="image" src="https://github.com/user-attachments/assets/628271ae-a0de-4a7f-861d-c9cb6d670501" />

- Omaa sivua hakiessa, näkyy kuitenkin sivun lataavan:
<img width="577" height="84" alt="image" src="https://github.com/user-attachments/assets/ad7c28cb-3db2-4353-b516-480512bd1fa7" />


### Lähteet:
- https://terokarvinen.com/linux-palvelimet/
- https://letsencrypt.org/how-it-works/
- https://go-acme.github.io/lego/usage/cli/obtain-a-certificate/index.html#using-an-existing-running-web-server
- https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample
