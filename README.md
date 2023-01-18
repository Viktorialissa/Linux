# Linux
Linux course reports

## h1 - Virtuaali Linux

Install Debian 11-Bullseye virtual machine in VirtulBox

### *Kone:*
- Lenovo IdeaPad S340
- OS Windows 10
- AMD Ryzen 7 3700U with Radeon Vega Mobile Gfx 
- RAM 8Gt

### Asennus

Lataa Debian 11-Bullseye [Debianin sivulta](https://cdimage.debian.org/images/unofficial/non-free/images-including-firmware/current-live/amd64/iso-hybrid/).
Valitse versio:

  ![debian](https://user-images.githubusercontent.com/112398757/213287022-89a2cc06-e1dd-49c0-a770-be7ca019ebac.JPG)


Lataamisen jälkeen avaa VirtualBox ja paina kohtaa New.

  ![painanew](https://user-images.githubusercontent.com/112398757/213287365-b0901ffd-029b-460b-a28e-b1bb58dec628.JPG)


Näin luot uuden virtuaalikoneen. Anna sille nimi ja lisää lataamasi versio Debianista ISO image kohtaan. Paina seuraavaksi Next.

![nameandadd](https://user-images.githubusercontent.com/112398757/213287715-0bee0c9e-cee9-4278-af9b-d655fe9104a9.JPG)


Luo seuraavaksi käyttäjätunnukset ja paina Next:

![user](https://user-images.githubusercontent.com/112398757/213288693-aadcebc0-e67c-40ea-bf1c-4feb57e805c0.JPG)


Seuraavaksi valitse muistin ja prosessoreiden (4) määrä. Valittuasi nämä paina Next.

![ramcpu](https://user-images.githubusercontent.com/112398757/213289090-e76eeb04-551a-4eec-954c-16261d01bcc1.JPG)


Siirrytään virtuaalisen kovalevyn luontiin ja sille kannattaa laittaa kooksi 60GB. Tehtyäsi tämän paina Next.

![harddisksize](https://user-images.githubusercontent.com/112398757/213289426-6f77d654-3a42-4907-991b-8fa3e02d1b3e.JPG)


Nyt aukeaa hieno virtuaalikone. Ennen kuin painat Install Debian -kuvaketta voit muuttaa manuaalisesti pienen näytön kokoa. Paina näytöllä hiiren oikealla ja valitse applications -> settings -> display.

![installDebian](https://user-images.githubusercontent.com/112398757/213289882-1765a9a5-2950-4c84-bfda-acf1f0d9a50e.JPG)


Saatuasi displayn näkyviin voit valita paremman koon, jotta näyttö ei ole niin pieni. Resoluutio kohdasta voit valita paremman koon, kuten 1680x1024.

![dispaly](https://user-images.githubusercontent.com/112398757/213290186-a9638b5d-2651-4f4f-8f74-a65b1cdc1b6d.JPG)


Nyt voimme jatkaa Debianin asennukseen. Paina Install Debian -kuvaketta.

![installDebian](https://user-images.githubusercontent.com/112398757/213290409-b4f43c05-3c0e-4ed2-8df9-16f0a66e41e9.JPG)


Seuraavaksi aukeaa Welcome-näkymä, jossa kannattaa pitää American English vaihtoehto ja jatkaa eteenpäin.

![amenglish](https://user-images.githubusercontent.com/112398757/213290671-910542bd-83bf-428e-b1a4-17280ea45e28.JPG)


Seuraavaksi valitse sijaintisi aikavyöhykkeen mukaan. Voit joko painaa kartasta sijaintiasi tai valita Region-valikosta Euroopan ja Zone-valikosta Helsingin.

![location](https://user-images.githubusercontent.com/112398757/213290948-f5b8a461-58f1-4a4a-8eda-a80cc4454a62.JPG)


Seuraavaksi valitaan näppäimistöksi Finnish, jotta voimme kirjoittaa erikoismerkeillä. Erikoismerkkien toimivuutta voi kokeilla.

![keyboard](https://user-images.githubusercontent.com/112398757/213291201-94521e3f-0bd6-4591-9aa7-4e26b420459c.JPG)


Seuraavaksi Partitions-näkymässä valitse Erase disk ja jatka eteenpäin.

![erasedisk](https://user-images.githubusercontent.com/112398757/213291831-b2b32200-68d2-4d02-acb1-f950d25971d1.JPG)


Käyttäjien luonnissa kirjoita nimesi. Valitse helposti muistettava nimi kirjautuessasi sisään. Anna koneelle neutraali nimi. Aseta salasana, joka on standardien mukainen.

![users](https://user-images.githubusercontent.com/112398757/213292193-cb45bb82-d794-4bd0-9a42-158ad3b2721a.JPG)


Summary-näkymä on yhteenveto juuri tekemistä asetuksista, jonka jälkeen päästään asennukseen.

![summary](https://user-images.githubusercontent.com/112398757/213292393-6dea2691-a700-4283-850f-04576423f3ff.JPG)

Nyt asennus lähtee pyörimään ja tässä menee hetki.

![linuxasennus](https://user-images.githubusercontent.com/112398757/213292663-3d587f46-65de-45dc-b9de-26c0cc44646d.JPG)








