### @activities 1

## Introduksjon Bit:Bot 

### Introduksjon Bit:Bot @unplugged

Bit:bot er en robotbil som er laget spesiel til bruk sammen med micro:bit.
![BitBot oversikt](https://github.com/olauk/static/blob/master/bitbotXL.png?raw=true)

### Kjøring med Bit:bot @unplugged

Bit:bot styres av to motorer. En motor på hvert hjul. Ved å bestemme fart og retning på motorene kan vi kontrollere bilen.
![BitBot motorer](https://github.com/olauk/static/blob/master/bitbotXLmotor.png?raw=true)

### Lys på Bit:Bot @unplugged

Bit:bot har 12 LED-lys. 6 på hver "arm". Disse kan stilles inn i ulike farger og kan kontrolleres hver for seg eller samlet.
![BitBot LED](https://github.com/olauk/static/blob/master/bitbotXLled.png?raw=true)

### Sensorer på Bit:Bot @unplugged

__Bit:bot har to linjesensorer montert på undersiden.__ 
Linjesensorene oppfatter om bilen kjører på et lyst eller mørkt underlag.

__Bit:bot har to lyssensorer.__ 
De er montert ytterst på hver av "armene" på bilen. Disse måler lysstyrke som en verdi mellom 0 og 255.

I tillegg kan man montere på en __Ultralydsensor__ som måler avstand. Den monteres i kontakten helt fremst på bitbot. Denne kan måle avstand i cm frem til nærmeste hindring.
![BitBot sensor](https://github.com/olauk/static/blob/master/bitbotXLsensor.png?raw=true)

### Annet utstyr på Bit:Bot @unplugged

Bit:bot har en __buzzer__ som er en enkel høyttaler. Den kan brukes til å lage lyd med blant annet blokkene fra kategorien ``||music:musikk||``.

Bit:bot har kontakter som lar deg koble til to __servomotorer__. På denne måten kan man bruke Bit:bot som en strømkilde i prosjekter hvor man skal bruke servomotorer.

Bit:bot har en __penneholder__ hvor man kan plassere en tusj eller penn til å tegne mønster.
![BitBot utstyr](https://github.com/olauk/static/blob/master/bitbotXLbuzz.png?raw=true)

### Sammenkobling av Bit:bot og Micro:bit @unplugged

__Micro:bit__ kobles til __Bit:bot__ ved å plassere micro:biten i _kantkontakten_ foran batteriene på bit:boten. Pass på at micro:bit blir stående med skjerm og knappene bort fra batteriene på bit:bot.

Nå er Bit:bot og Micro:bit klar til å programmeres. Micro:biten kan fint stå plassert i bit:bot når man kobler til USB-kabel i datamaskinen, eller kobler til iPad via bluetooth.
![BitBot tilkobling](https://github.com/olauk/static/blob/master/BitBot_microbit.jpg?raw=true)


## Kontroll av Bit:Bot

### Kjør fremover
Vi kontrollerer fart og retning med hvor mye strøm som sendes til motoren. Forenklet så kalles dette _fart_ i blokkene i MakeCode og vi kan velge en prosentvis verdi fra 0 - 100.

Vi kan kontrollere bevegelse fremover og bakover med to ulike blokker. 
``||bitbot:Kjør fremover med fart||`` som kun angir fart. (Her kan du tenke at bit:bot vil kjøre, helt til du gir en ny kommando i programmet.) 

``||bitbot:Kjør fremover med fart i millisekunder||``   angir både fart og varigheten av kjøringen i antall millisekunder.

### Legg til blokker
Hent blokken ``||input:Når knapp A trykkes||`` fra ``||input:Inndata||`` og plasser den på arbeidsflaten.

Hent blokken ``||bitbot:Kjør fremover med fart i millisekunder||`` fra ``||bitbot: BitBot Kjøring||`` og plasser den i ``||input:Når knapp A trykkes||``

Sett _fart_ til __100%__ og _varighet_ til __1000 millisekunder__.


Last ned programmet til din micro:bit, koble den til Bit:bot og se hva som skjer når du trykker knapp A.

```blocks
input.onButtonPressed(Button.A, function (){
bitbot.goms(BBDirection.Forward, 100, 1000)
})
``` 
```ghost
bitbot.go(BBDirection.Forward, 100)
bitbot.rotate(BBRobotDirection.Left, 20)
```

### Legg til en sving
Vi får Bit:bot til å svinge med ``||bitbot:Snu til venstre/høyre med fart||``. Her har vi også mulighet til å velge blokker som angir kun fart eller fart og millisekunder.

Hent blokken ``||bitbot:Snu til venstre/høyre med fart i millisekunder||`` fra ``||bitbot: Bitbot Kjøring||`` og plasser den under ``||bitbot:Kjør fremover med fart i millisekund||``

Sett _fart_ til __20%__ og _varighet_ til __500 millisekunder__.

Last ned programmet til din micro:bit, koble den til Bit:bot og se hva som skjer når du trykker knapp A.

```blocks
input.onButtonPressed(Button.A, function (){
bitbot.goms(BBDirection.Forward, 100, 1000)
bitbot.rotatems(BBRobotDirection.Left, 20, 500)
})
``` 
```ghost
bitbot.go(BBDirection.Forward, 100)
bitbot.rotate(BBRobotDirection.Left, 20)
```
### Oppdrag 1: @showdialog

Oppdrag 1:

Du skal nå endre i ditt program slik at Bit:bot kjører 1 meter frem, snur 180 grader og kjører 1 meter tilbake.


Prøv selv uten å se på hintet. Bit:bot kjører litt forskjellig ut i fra hvor nye batterier man har, så verdiene i hintet trenger ikke å stemme helt hos deg.


```package
bitbot=github:4tronix/bitbot
``` 

