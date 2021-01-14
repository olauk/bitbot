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


## Kontroll av Bit:Bot

### Kjør og sving
Vi kontrollerer fart og retning med hvor mye strøm som sendes til motoren. Forenklet så kalles dette _fart_ i blokkene i MakeCode og vi kan velge en prosentvis verdi fra 0 - 100.

Vi kan kontrollere bevegelse fremover og bakover med to ulike blokker. En angir kun fart og en angir både fart og varigheten av kjøringen i antall millisekunder.
Hent blokken ``||input:Når knapp A trykkes||``` fra ``||input:Inndata||`` og plasser den på arbeidsflaten.
Hent blokken ``||bitbot:Kjør fremover med fart og millisekunder||`` fra ``||bitbot: BitBot Kjøring||`` og plasser den i ``||input:Når knapp A trykkes||``

Last ned programmet til din micro:bit, koble den til Bit:bot og se hva som skjer når du trykker knapp A.

```blocks

bitbot.goms(BBDirection.Forward, 100, 1000)
``` 

### Step 2

```blocks
bitbot.goms(BBDirection.Forward, 60, 400)
bitbot.rotatems(BBRobotDirection.Left, 60, 400)
``` 
Congratulations, you did it!

```packets
        "BitBot": "github:4tronix/bitbot#1.4.6"
``` 
