# Štoperica — PIC16F88 & Flowcode

Digitalna štoperica realizovana na mikrokontroleru PIC16F88 u Flowcode okruženju. Projekat je rađen kao laboratorijska vježba iz predmeta Praktična nastava.

## Funkcionalnosti

| Taster | Funkcija |
|--------|----------|
| Start | Pokreće mjerenje vremena |
| Stop | Zaustavlja mjerenje |
| Lap | Zamrzava prikaz dok tajmer nastavlja raditi u pozadini |
| Reset | Vraća sve vrijednosti na nulu |

Vrijeme se prikazuje na LCD ekranu u formatu MM:SS:ss (minute, sekunde, stotinke).

## Kako radi

Program u glavnoj petlji čita stanje tastera i na osnovu toga upravlja stanjem štoperice. Brojač stotinki se povećava u svakom ciklusu — kad stigne do 100, sekunde se povećaju za jedan i stotinke se resetuju. Kad sekunde stignu do 60, isti princip se primjenjuje za minute. Lap funkcija sprema trenutne vrijednosti u posebne varijable dok mjerenje nastavlja normalno.

## Hardver

- Mikrokontroler: PIC16F88
- LCD: 16x2, 4-bitna komunikacija, port B
- Tasteri: 3x digitalni taster na portu A

## Screenshotovi

### Globalne varijable

![Varijable](https://raw.githubusercontent.com/redzictarik/FlowCode--STOPERICA/main/preview.webp)

Definirane varijable za stanja (start, stop, reset, loop) i mjerenje (minute, sekunde, stotinke). Duplikati varijabli (minute1, sekunde1, stotinke1) služe za Lap funkciju.

### Dijagram toka

![Dijagram toka](https://raw.githubusercontent.com/redzictarik/FlowCode--STOPERICA/main/prva.webp)

Kompletan program u Flowcode okruženju — inicijalizacija, glavna petlja s grananjima za tastere i logika ispisa na LCD.

### Simulacija — rad štoperice

![Simulacija u radu](https://raw.githubusercontent.com/redzictarik/FlowCode--STOPERICA/main/druga.webp)

Prikaz simulacije dok štoperica mjeri vrijeme. LCD prikazuje izmjerenu vrijednost u formatu M:SS:ds.

### Simulacija — početno stanje

![Početno stanje](https://raw.githubusercontent.com/redzictarik/FlowCode--STOPERICA/main/treca.webp)

Stanje nakon pokretanja ili resetovanja — sve varijable na nuli, sistem spreman za mjerenje.

### Simulacija — Lap funkcija

![Lap funkcija](https://raw.githubusercontent.com/redzictarik/FlowCode--STOPERICA/main/cetvrta.webp)

Prikaz više uzastopnih prolaznih vremena. Dok je LCD zamrznut na međuvremenu, tajmer u pozadini nastavlja raditi.

## Tehnologije

- Flowcode
- PIC16F88

## Autor

Ahmed Mrakanović, ETŠ Tuzla
