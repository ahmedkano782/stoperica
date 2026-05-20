# Štoperica

Projekat rađen u Flowcode-u kao simulacija digitalne štoperice. Koristi PIC 16F88 mikrokontroler i LCD displej za prikaz vremena u realnom vremenu.

## Kako radi

Program u glavnoj petlji kontinuirano povećava brojač stotinki. Kad stotinke dođu do 100, povećaju se sekunde i stotinke se resetuju. Isto važi za sekunde — kad stignu do 60, povećaju se minute. Trenutno stanje se uvijek ispisuje na LCD u formatu minute:sekunde:stotinke.

Na svakom prolasku kroz petlju program čita stanje sva četiri tastera i reaguje na onaj koji je pritisnut:

| Taster | Funkcija |
|--------|----------|
| Start | Pokreće mjerenje — ulazi u petlju brojanja |
| Stop | Zaustavlja mjerenje — čeka dok se ne pritisne Start ili Reset |
| Lap | Bilježi trenutne minute, sekunde i stotinke kao međuvrijeme |
| Reset | Postavlja sve vrijednosti na nulu i čeka novi Start |

## Tehnologije

- Flowcode
- PIC 16F88
- LCD displej

## Autor

Ahmed Mrakanović, ETŠ Tuzla
