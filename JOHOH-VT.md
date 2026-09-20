# Johdatus ohjelmointiin 

Kurssin tehtäviä, vastauksia ja kuvia. 
- Tehtävät ovat numeroitu siinä järjestyksessä kuin ne ovat Moodlessa.





<details>
  
<summary> Viikkotehtävät 1: Tulostus ja matematiikka </summary>
  
<p>









<details>
  
<summary> Toteutus </summary>
  
<p>

Päätin tehdä koko harjoituksen 1-5 yhteen ohjelmaan. Tämä helpottaa arviointia ja auttaa minua oppimaan paremmin.

Tehtävässä ja alkuun pääsemisessä oli hyvin raskasta se, että VScode on pakattu täyteen automaattisia täyttö ja avustus ohjelmia, joista on oppimiseen lähinnä haittaa.
Sain nämä kuitenkin pienen työstön jälkeen poistettua käytöstä.

Tässä harjoituksessa ainoa asia mihin käytin tekoälyä oli Python sanaston luomiseen discord palvelimelle. Siitä oli paljon hyötyä.
Käytin myös Googlea apuna ohjelman luomiseen, sillä minulle tuli ongelma sellaisen loopin tekemisessä, joka kysyisi tehtävän jälkeen uudestaan "minkä harjoitus tehtävän haluat suorittaa?".
Tähän löysin vastauksen "while True:" eli silmukka käynnistyy kun koodi saapuu sen kohdalle ja ainut tapa poistua siitä on 0 eli "break"

<img width="885" height="589" alt="image" src="https://github.com/user-attachments/assets/85091473-61ce-4eb3-ba10-cef0f2cd1f8a" />



<br><br>

## Koodi ##

def select_number():
    tehtävä = (1, 2, 3, 4, 5)  
    while True:    
                    
        valinta = int(input("Minkä harjoitustehtävän haluat suorittaa, 1, 2, 3, 4, 5? poistu 0: "))
        
        if valinta == 0:
            print("Poistuit.")
            break

        while valinta < 1 or valinta > 5:
            valinta = int(input("Valitse yksi tehtävänumero 1 ja 5 välillä: "))

        # tehtävä 1
        if valinta == 1:
                print("Hello world!")
                print("Veeti Tuomisto")
                print("2001")
                print("Lahti")
        
        # tehtävä 2                                        
        elif valinta == 2:
                hinta = float(input("Anna tuotteen veroton hinta: "))
                print(f"hinta alv kanssa: {hinta * 1.24}")
        
        # tehtävä 3
        elif valinta == 3:
                matka = int(input("Matkan pituus (km)?: "))
                kulutus = float(f"{matka / 100}")
                print(f"Polttoaineen kultus tälle matkalle: {kulutus * 6.5}")

        # tehtävä 4
        elif valinta == 4:
                aika = int(input("Anna minuutit: "))
                print(f"{aika // 60}t {aika % 60}min")

        # tehtävä 5
        elif valinta == 5:
                numero1 = int(input("Anna 1-1000000 senttiä: "))
                tulos1 = numero1 // 50
                jakojäännös1 = numero1 % 50
                print(f"50 snt kolikoita {tulos1} kpl")           #50snt

                numero2 = jakojäännös1
                tulos2 = numero2 // 20
                jakojäännös2 = numero2 % 20
                print(f"20 snt kolikoita {tulos2} kpl")           #20snt
                
                numero3 = jakojäännös2
                tulos3 = numero3 // 10
                jakojäännös3 = numero3 % 10
                print(f"10 snt kolikoita {tulos3} kpl")           #10snt
                
                numero4 = jakojäännös3
                tulos4 = numero4 // 5
                jakojäännös4 = numero4 % 5
                print(f"5 snt kolikoita {tulos4} kpl")             #5snt

                numero5 = jakojäännös4
                tulos5 = numero5 // 2
                jakojäännös5 = numero5 % 2
                print(f"2 snt kolikoita {tulos5} kpl")             #2snt

                numero6 = jakojäännös5
                tulos6 = numero6 // 1
                jakojäännös6 = numero6 % 1
                print(f"1 snt kolikoita {tulos6} kpl")             #1snt

select_number()

<br><br>

<img width="1280" height="1439" alt="image" src="https://github.com/user-attachments/assets/987bb1a3-d1a4-4ae8-bccf-e9550ae66167" />




</p>

</details>








<details>

<summary> 1. Hello, world! </summary>

<p>

<br><br>
Tehtävä 1 oli perus print("Hello, world!") alotus tehtävä.

<img width="585" height="322" alt="image" src="https://github.com/user-attachments/assets/0a361362-38d3-4bde-a0e4-32a10693f883" />

</p>

</details>









<details>

<summary> 2. Arvolisävero laskuri </summary>

<p>

Tehtävä 2 oli arvolisäverolaskuri. Tehtävässä käytin float(), jotta laskuri toimisi mahdollisimman tarkasti. 
Toinen mainittava on f" joka mahdollisti lyhyen siistin koodin, jossa print() toimii laskutoimituksena ja vastauksena.

<img width="645" height="235" alt="image" src="https://github.com/user-attachments/assets/53661900-cc6a-4ba3-84bd-701e0d302373" />

</p>

</details>









<details>

<summary> 3. Polttoaine laskuri </summary>

<p>

Tehtävässä 3 vaadittiin taas float() ja f". Tällä kertaa käytin tehtävässä myös int(), vaikka float() olisi voinut antaa tarkemmat lukemat. 
Valitsin int(), koska mielestäni se on tarpeeksi että ohjelma laskee km tarkkuudella, eikä input desimailit tee tarpeeksi merkittävää muutosta esim. 75km matkalla.

<img width="738" height="338" alt="image" src="https://github.com/user-attachments/assets/ac5b91a3-fec9-457e-991c-3d6da607e9ac" />


</p>

</details>









<details>

<summary> 4. Tunnit ja minuutit </summary>

<p>

Tehtävä 4:ssä kävin lisäämässä Python sanastooni 7 kpl matemaattisia merkkejä. Tehtävässä käytin int() eli käyttäjä voi syöttää vain minuutteja ja print(f"{}{}").
Tehtävän olisi varmasti voinut tehdä vain kahdella linellä esim. jälkimmäinen line olisi voinut olla print(f"{aika // 60}t {aika % 60}), mutta tajusin sen vasta täällä gitissä.

Korjattu

<img width="567" height="290" alt="image" src="https://github.com/user-attachments/assets/868407ab-b64a-4104-b2ec-a591420fe7b3" />

<br><br>
Vanha

<img width="605" height="295" alt="image" src="https://github.com/user-attachments/assets/38a5e434-79fa-4796-8cff-62b05315ccce" />




</p>

</details>









<details>

<summary> 5. Kolikko laskuri </summary>

<p>

Tehtävä 5 oli haastava. Tein sen alkuun hieman eri tavalla ja minulla oli ennen printtiä line joka poistaa desimailit tuloksesta, mutta vaihdoin sen  // ja poistin ylimääräisen linen.
Kun tehtävästä sai yhden osuuden tehtyä se oli helppo kopioida ja muuttaa vain arvot.

<img width="778" height="972" alt="image" src="https://github.com/user-attachments/assets/f77293bf-6935-4b76-a0bd-bc96ee1b4d04" />

</p>

</details>














</p>

</details>

<br><br>
