# Java-HiLo-spel

## Labb 1

### Beskrivning

#### Den här labben kommer ni att göra ett HiLo-spel.

HiLo står för High-Low, och går ut på att datorn slumpar fram ett tal mellan 1 och ett maxtal. Spelaren skall sedan försöka gissa vilket tal datorn tänker på. Om användaren gissar för högt skall spelet säga att gissningen var för hög, och samma om den var för låg. På detta sätt är det tänkt att spelaren skall lista ut vilket tal datorn fick fram vid slumpgenereringen.

I den här versionen skall det finns tre olika svårighetsgrader: lätt, mellan och svår. De olika svårighetsgraderna avgör vilket maxtal som programmet kommer att ha när det slumpar ut det rätta svaret.

Lätt skall ge ett tal 1 - 10.

Mellan skall ge ett tal 1 - 100.

Svårt skall ge ett tal 1 - 1000.

Användaren skall få välja svårighetsgrad när hen först startar spelet.

När en spelomgång har spelats klart skall antalet försök skrivas ut på skärmen.

# Programmering
#####  För att programmera detta spel skall ni skriva tre stycken metoder.
Nedan följer en beskrivning av de tre, och lite tips för hur ni kan skriva dem.

# public static void main(String[] args) {...}
#### Man måste alltid ha en main-metod, så ni skall såklart ha en i det här spelet också.

Denna metod ska först skriva ut huvudmenyn, vilket låter användaren välja svårighetsgrad.
(Om ni vill göra det enkelt för er, gör som i exemplet. Låt användaren mata in heltal, och bestäm att 0 betyder lätt, 1 mellan och 2 svår)

Efter att valet av svårighetsgrad tagits emot skall metoden playGame anropas, med svårighetsgraden som argument. Detta spelar klart själva spelomgången.

När spelomgången är slut, så returnerar playGame antalet gissningar det tog för användaren att klara spelet. Detta bör ni spara undan.

Main-metoden ska slutligen skriva ut antalet gissningar. Sedan är spelet över!

# public static int playGame(int maxNumber) {...}
#### Detta är metoden som kör själva spelet.
Den slumpar först fram ett tal. Sedan låter den användaren gissa fram tills att hen har gissat rätt. Till slut returnerar metoden antalet gissningar användaren tog på sig.

Utförlig beskrivning

playGame tar emot ett argument maxNumber som helt enkelt är vilket maxnummer som ska användas när den slumpar fram ett tal.
(Exempel: Om spelaren väljer "lätt" svårighetsgrad, ska metoden anropas med värdet 10)

Efter detta skall metoden slumpa fram själva numret.
(koden för att slumpa fram ett nummer i Java står längst ned i detta dokument, ni kan kopiera den)

När spelet har slumpat fram ett nummer är det dags för spelaren att börja gissa.

Spelet ska fortsätta fråga efter gissningar fram tills dess att spelaren har gissat rätt.
(Ni vill alltså köra "gissnings-koden" flera gånger, fram tills dess att användarens svar är lika med det framslumpade numret)

För varje gissning skall först ett tal hämtas från användaren.
Sedan ska programmet skriva ut om talet var för högt, lågt eller om det var rätt tal. Detta gör ni genom att anropa metoden giveResponse.
Sedan ska programmet öka en variabel, som innehåller antalet gissningar, med 1. (Fundera på var ni bör deklarera denna variabel, så att den inte nollställs för varje gissning)

När användaren till slut har gissat rätt är gissningsfasen är över.

Då ska antalet gissningar (som ni räknade ovan) returneras.


# public static void giveResponse(int answer, int guess) {...}
#### Den här metoden skall skriva ut respons till användaren. Den skriver ut om gissningen var för hög, om den var för låg eller om den var rätt.

Den tar emot två argument: answer är det rätta svaret och guess är gissningen som gjordes.
Metoden skall nu jämföra dessa två tal, och skriva ut ett lämpligt meddelande.

## Tips
#### För att slumpa fram ett tal i Java kan följande kodrad användas:

int number = (int)(Math.random() * max) +1;


Den här kodraden deklarerar en heltalsvariabel som heter number, och ger den sedan ett värde som ligger mellan 1 och max, där max är en annan heltalsvariabel.