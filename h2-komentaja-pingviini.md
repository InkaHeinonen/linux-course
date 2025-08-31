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
  
- Tämän jälkeen kirjoitin Python-lauseketta alla olevan kuvakaappauksen mukaisesti. Tämän jälkeen tallensin tekstin Ctrl + S ja painoin F4. Tästä ei kuitenkaan tapahtunut mitään ja en ole varma, miten tämän tulisi toimia. Tätä pitääkin kysyä seuraavalla oppitunnilla. 

<img width="1280" height="749" alt="image" src="https://github.com/user-attachments/assets/f15e5b9f-9dfd-4be0-b23a-3428b4717df4" />

Lähteenä: https://github.com/terokarvinen/micro-jump 

