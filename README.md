# Web-Task

## x) 

Valitsin Indie Hackers -Podcastin jakson #007: Building an Open-Source Publishing Platform That Makes $63,000/mo with John O'Nolan of Ghost

- Teki WordPressillä Open-Source Julkaisualustan, joka levisi monien yritysten käyttöön. 

- Tekijät sovelsivat ideoita ja ominaisuuksia muista sovelluksista ja palveluista, joita ei ollut ennen julkaisualustoissa tai blogauspalveluissa ja implementoivat niitä omaan versioonsa. 

- Oppivat ottamaan huomioon palautteet ja kommentit vain tietyissä määrin, välttyäkseen joutumasta jatkuvaan päivitys- ja korjauskierteeseen. (kaikkia ei voida tyydyttää, mutta järkevimmät ja tarpeellisimmat pyynnöt otetaan huomioon)

- Aloittivat suunnitelemalla alustan, joka nimenomaan toimii heille sopivana alustana ja saatuaan sen valmiiksi alkavat kehittää muiden potentiaalisten asiakkaiden toiveiden suuntaan.

- Podcastissa haastateltava vetoaa siihen, että on parempi tähdätä keskimääräistä sopivan paljon suurempaan palkkaan ja rakentaa idea sen suuntaisesti, sen sijaan että tähtää miljooniin. 



## a)

Tein oppitunnin aikana testiksi niin, että tavallisen apache2 palvelimen kotisivun sijasta sivu näyttää echo -komennolla pelkän "Moi" tekstin. 

![kuva](https://user-images.githubusercontent.com/105205141/216312373-dc734686-c53d-46af-8a0c-364cb4780a0a.png)

## b) 

Tein oppitunnilla myös käyttäjäsivun tehtävän mukaan, jossa tein sivun osoitteessa localhost/~seikku/
Loin HTML-tiedoston sille, johon kirjoitin seuraavanlaisen tekstin: 

![kuva](https://user-images.githubusercontent.com/105205141/216312911-f3a6762d-af72-4556-b9c4-e41865ca2d4d.png)

## c) 

Tein uuden käyttäjän "seikkutest", ja tein käyttäjälle oman hakemiston komennolla:

    sudo useradd -m seikkutest -s /bin/bash
    sudo passwd seikkutest
    (salasana)
    
Tämän jälkeen kirjauduin ulos päätilistäni uudelle testitililleni onnistuneesti painamalla vasemmasta yläkulmasta näyttöä "Applications" > "Log out" > "Switch User"

Yritin tehdä uudessa käyttäjässä sudokomentoja, mutta unohdin antaa tilille sudo-oikeudet.
Kävin siis varsinaisella sudokäyttäjällä lisäämällä ne: 

    sudo visudo
    
Tämä avaa näkymän, jossa voin lisätä sudo-oikeudet uudelle käyttäjälleni kirjoittamalla tiedoston pohjalle:

    seikkutest ALL=(ALL) ALL
    
Sitten palasin takaisin testikäyttäjälle ja onnistuneesti käynnistin apache2 palvelimeni 

    sudo service apache2 start
    
Tämän jälkeen testasin toimiiko kyseinen sivu, ja tein hakemiston public_html, jonka sisälle laitoin käyttäjälle html-tiedoston.

![kuva](https://user-images.githubusercontent.com/105205141/216318813-06b4da86-8994-46cb-8430-2c52a292f754.png)

## d)

Tässä HTML-tiedoston sisältö:

![kuva](https://user-images.githubusercontent.com/105205141/216318337-89731823-c18e-41d2-b8c2-2e64f6d57a11.png)

Tallensin muutokset, poistuin html tiedostosta ja kokeilin sivua selaimella: 

![kuva](https://user-images.githubusercontent.com/105205141/216319018-e1c0e20b-c336-47cb-a26f-0be420de2f36.png)


# Lähteet: 

Podcast: https://www.indiehackers.com/podcast/007-john-onolan-of-ghost
