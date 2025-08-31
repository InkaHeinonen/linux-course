## Tehtävä nro X)
- Jokaisella komennolla on oma tehtävänsä ja niiden kirjoitusasussa tulee olla tarkkana, kuten isot ja pienet kirjaimet.
- Komennolla voit liikkua hakemistossa, tehdä sinne muutoksia, ladata sisältöä sekä tarkastella tiedostojen sisältöä.
- Komentoja on huomattava määrä ja niiden käyttöä on syytä harjoite työskentelyn sujuvoittamiseksi

- Lähteenä: https://terokarvinen.com/2020/command-line-basics-revisited/?fromSearch=command%20line%20basics%20revisited

## Tehtävä a) Micro-editorin asennus
- Käytössä Windows 11 järjestelmä, VirtualBox 7.2.0, Ubuntu

- Micro-editoria asentaakseni katsoin internetistä keskustelupalstoilta mielipiteitä ja löysin linkistä selkeän ohjeen ja neuvon eri pluginsien asentamiseksi. Jatkoin kuitenkin asentamista Tero Karvisen ohjeella screenshotin mukaisilla komennoilla:
<img width="897" height="713" alt="image" src="https://github.com/user-attachments/assets/851f67e9-64c9-44ea-a8a6-fbed5b103a88" />
  
- Lähteenä: https://youtu.be/kqCQLyrEZww?si=iCqq82dUgDOhsw_b , https://micro-editor.github.io/ https://terokarvinen.com/2022/micro-editor-plugin-hello-world/?fromSearch=micro


## Tehtävä b) Kolmen eri komentoriviohjelman asennus
- Aihealue on itselleni vieras ja lähdin selvittämään, mitkä ovat aloittelijalle sopivimmat ohjelmat. Vaihtoehtoja oli lukuisia ja google-haulla pääasiallisesti tuli ehdotuksena eri komentoja, joita käyttää. En siis löytänyt haullani vielä useaa ehdotusta hyödyllisistä ohjelmista. Luotan hakusanojeni kehittyvän, kun opin aiheesta lisää.


#### Shutter
- Shutter-ohjelman asensin aluksi helpottamaan screen shottien ottamista ja jakamista git hubiin, ennenkuin havaitsin sen lopulta olleen turha ohjelma ja voin toteuttaa saman asian jo tietokoneen omalla toiminnollani. Shutter-ohjelmalla voi kuitenkin kätevästi valita, mihin näyttökuva tallennetaan ja löytää se komentorivihakemistostani jälkeenpäinkin

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/5e917048-136b-4e1d-8b79-e6bf63501777" />


#### Nethack
- Opintojen aineistoissa oli maininta pelistä, joten mielenkiinnosta latasin kyseisen ohjelmiston. Pelaamaan en ehtinyt enempää, mutta näyttökuvassa on latauksen jälkeinen näkymä ja muutama steppi eteenpäin:
<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/eddde4e8-96c5-46a1-acb9-a0dfadd615bb" />

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/f93ad426-4bae-405f-b7b1-e8aa5416fabd" />

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/1d936174-2d45-41f6-bc7d-7d26221a055e" />


#### Micro-jump
- Tero Karvisen opintomateriaalissa on ohjeet micro-jumpin lataukseen:
  
$ sudo apt-get update
$ sudo apt-get -y install micro fzf exuberant-ctags
$ micro --plugin install jump

- Latauksen jälkeen ohjelman saa auki:
$ micro tero.py
  
- Tämän jälkeen kirjoitin Python-lauseketta alla olevan kuvakaappauksen mukaisesti. Tämän jälkeen tallensin tekstin Ctrl + S ja painoin F4. Tästä ei kuitenkaan tapahtunut mitään ja en ollut aluksi varma, miten tämä toimii. 

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/f15e5b9f-9dfd-4be0-b23a-3428b4717df4" />

- Hoksasin kokeilla F4 sijaan painaa kannettavalla tietokoneellani Fn + F4, joka aukaisi kuvan mukaisen valikon:

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/270ba36c-0b97-456b-bf1e-f56ade1bf436" />

Lähteenä: https://github.com/terokarvinen/micro-jump 


### Kolmen eri ohjelman samanaikainen asennus
- Löysin mallin, jolla voisi kolme eri ohjelmaa asentaa. Ohjelmaesimerkkeinä toimivat Jump F4 symbol jump. Palettero command palette, Runit F5 compile. Latasin nämä jo aiemmin, mutta en hoksannut niiden voineen jo kuulua edellisen tehtävänannon kolmeen ladattavaan ohjelmistoon. En vielä löytänyt kuitenkaan, miten nämä voisi hakea screenshotille listauksena, että ovat jo asennettuna. 
- Komentokehoite edellä mainittujen asentamiseen:
  1. $ sudo apt-get update
  2. $ sudo apt-get -y install micro fzf exuberant-ctags
  3. $ micro --plugin install jum
  4. $ micro --plugin install palettero
  5. $ micro --plugin install runit

Lähteenä: https://terokarvinen.com/get-started-micro-editor/?fromSearch=micro%20editor 



## Tehtävä c) FHS - Important directories
### Navigointi kohteeseen: /

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/2ed0a986-11cb-438c-9c15-5f064d998017" />


### Navigointi kohteeseen: /home/
- En ole varma, tulisiko pwd-komennolla tässä näkyä sijaintina /home, mutta sain tähän sijainniksi 'inka' tai /home/inka/. Tähän en hae tiedostokansiota, koska epäilen tämän tehtävän olevan jollain tavalla väärin tehty. 
- Youtube-videoissa ja internetin keskustelupalsoilta löysin navigointiohjeita vain osoitteeseen /home/user/

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/fb585e26-b979-40c6-90a6-7a2bdd023321" />

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/cde0ade8-9966-40e4-808c-2696e7fd271c" />

Tämän kuvan lähteenä: https://linuxconfig.org/single-linux-command-to-return-to-home-directory 

- Lähteitä: https://youtu.be/3E0x-9kfyCY?si=QzKBTs878fcuueuz, https://askubuntu.com/questions/863762/how-to-navigate-to-home-directory, https://linuxconfig.org/single-linux-command-to-return-to-home-directory 

### Navigointi kohteeseen: /home/inka/
- Navigointi komennolla: cd ja avaan edeltävällä oppitunnilla luodun kansion, joka on tyhjä.

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/c322d3e5-b085-4db3-8b09-afdb57a98262" />

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/676b49c5-d6b5-4eba-898a-0794c81ac970" />


### Navigointi kohteeseen: /var/log/
- Navigointi kohteeseen komennolla: cd /var/log/, josta avasin sysstat. Sysstat-kansiosta löytyi tekstitiedosto, joka ei kuitenkaan ollut heti luettavissa.

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/54341967-c7fb-44e5-862b-14a70c7aa96e" />

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/961418f5-2ff1-48d4-a05d-dc5a32f325a4" />


### Navigointi kohteeseen: /Media/
- Navigointi kohteeseen komennolla: cd Media. Kuten kuvasta näkyy, kansio on tyhjä.

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/3c4a0b6e-0a1a-46e0-b98c-c2d57c4ed764" />


### Navigointi kohteeseen:/etc/
- Navigointi kohteeseen komennolla: cd /etc/, jonka jälkeen listauksen avaus komennolla: ls

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/74ff0e1c-db97-43cd-91bc-155a46ad67ee" />

- Listauksesta hain muutaman virheklikkauksen jälkeen NetworkManager, josta avasin VPN. Tämä kuitenkin oli tyhjä, joten koitin System-connectionia, josta löytyikin yksi tiedosto

<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/61e1834e-ff6c-42f9-9078-21039501e623" />



## Tehtävä d) The Friendly M
- Kuvaavia esimerkkejä grep-komennon käytöstä.
- Komentoriville kirjoitan man grep, josta avautuu kuvan mukainen näkymä:
<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/222865df-5801-4718-bf7c-dcf864c928bb" />

- Näkymässä voi hakea tiettyä sanaa kirjoittamalla komentoriville /, jonka jälkeen haluttu sana. Tässä esimerkissä kirjoitin /pattern
<img width="817" height="485" alt="image" src="https://github.com/user-attachments/assets/7b89550e-e6bf-4b97-8bf6-3c1292647416" />













