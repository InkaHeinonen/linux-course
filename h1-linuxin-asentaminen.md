# Tehtävänanto h1

## 2. Linuxin asentaminen
- Käytössä Windows 11 järjestelmä, VirtualBox 7.2.0
- Virtuaaliboxi ladattu osoitteesta https://www.virtualbox.org/wiki/Downloads.
- Internet-selaimena Google Chrome

  ## Virtuaaliboxin asennus
- Aloitusajankohta klo 19.15.
- Etusivulta valitsin alaotsikon VirtualBox 7.2.0 platform packages-alta paketin: Windows-hosts, josta klikkasin.
- Klikatessa oikeaa pakettia, tietokoneelle latautui tiedosto nimeltä VirtualBox-7.2.0.-170228-Win.
- Avasin ladatun tiedoston, jonka jälkeen tietokoneen ruudulle tuli ilmoitus: "Sallitko tämän sovelluksen tehdä muutoksia tähän laitteeseen?". Ilmoituksessa oli valintanapit Kyllä ja Ei, josta valitsin Kyllä.
- Valintanappia painettuani, aukesi Installer:n etusivu, jossa vaihtoehtona painaa Next tai Cancel. Valitsin Next. 
- Seuraavalla sivulla on lisenssi, joka tuli hyväksyä sekä painaa Next.
- Seuraavalla sivulla voi valita itselleen sopivamman paikan asennukselle. En tehnyt muutoksia sijaintiin ja painoin Next.
- Tämän jälkeen tuli varoitussivu, jossa kerrotaan latauksen aikana internet-yhteyden katkeavan ja yhteyttä vaativat asiat olisi syytä sulkea ennen latausta. Tässä vaiheessa tallensin raportin. 
- Seuraavalla sivulla kerrotaan, mitä Oracle Virtualbox 7.2.0 Python vaatii ja nämä on mahdollista asentaa jälkikäteenkin. Vaihtoehtopainikkeet Kyllä ja Ei, josta painoin Kyllä.
- Sivuksi aukesi otsikolla Custom Setup, jossa mahdollista valita aloitukseen mieluisat vaihtoehdot. Jätin kaikki valinnat, jotka olivat valmiina. Jokaisessa ruudussa on valinta ja painoin Next.
- Sivunäkymän otsikkona Ready to Install, josta painoin Install. Asennusajankohtana klo 19.28 ja asennus kesti alle 1min.
- Asennuksen jälkeen tulee ilmoitus toteutuneesta asennuksesta ja kysymys, avataanko Virtuaaliboksi. Valitsin painikkeen Finish.

## Debian ISO imagen lataus
- Painoin ladatakseni täältä sivustolta: https://cdimage.debian.org/debian-cd/13.0.0-live/amd64/iso-hybrid/, tämän:debian-live-13.0.0-amd64-xfce.iso (3.5G). Painaessani tätä, sivusto latasi noin 3min, jonka jälkeen ladatut tiedostot-kansioon latautui noin 5 minuutissa. Latauksen aukaistaessani, tuli ilmoitus, haluanko avata sovelluksen ja painoin Avaa. Lataus avautui tietokoneelleni DVD-asemana. 
- 
- 

## Virtuaalitietokoneen asennus virtuaaliboksiin
- Avasin virtuaaliboksin, josta painoin "New"
  1. Virtuaalikoneen nimeksi annoin: test-debian-live-13.0.0-amd64-xfce.iso
  2. Folder: pidin valmiiksi ehdotetun
  3. ISO image: C:\Users\juuli\Downloads\debian-live-13.0.0-amd64-xfce.iso
  4. Edition: tämän kohdan jätin tyhjäksi
  5. OS: Linux
  6. OS Distribution: Debian
  7. OS Version (Debian 32-bit)
  8. Valitse alhaalta Proceed with unattended installation. Tämä oli valmiiksi valittuna ja pidin sen. Lopulta painoin Next.
- Seuraavalla sivulla loin käyttäjän, valmis käyttäjänimeiehdotuksen pidin ja keksin oman salasanan.
- Viereisestä laatikosta Host ja Domain name:n pidin valmiiksiehdotettuina. Painoin Install in Backround sekä alhaalta painoin Install guest addditions ja painoin N
- Seuraavalla sivulla RAM-muistiksi valitsin 4096 MB, CPU 2, disc size valmiiksi ehdotettu 20,00 GB. EFI: jätin painamatta, joten sitä en ottanut käyttöön.
- Seuraavalta sivulta painoin Next ja Finish lukiessani, että tiedot täsmäävät ja ovat oikein valittu. 
