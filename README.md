## Project TeacherConnect

- TeacherConnect er en platform, hvor universitetsstuderende kan booke møder med respektive forelæsere, for og få hjælp til et givet fag.

# Analyse (hvad systemet skal kunne):
Klienten skal via sin universitets mail logges ind på vores system. Systemet skal derefter videreføre klienten til vedkommendes tilhørende linje og fag. Herefter vil klienten kunne trykke sig ind på fag, og de tilliggende forelæsere. Der vil derefter være mulighed for at booke et møde med den valgte forelæser. 

# Design (hvordan):
Vi tager i vores projekt udgangspunkt i CBS. Eftersom vi benytter os af objektorienteret programmering, kan projektet senere hen også videreføres til andre universiteter. Dette vil ske i form af inheritance. 

Når den studerende (brugeren) tilgår vores platform vil de få muligheden for at logge ind med deres CBS mail og adgangskode. Ved successful log-in vil de blive videreført til vores overordnet “startside”. Vi vil integrerer systemet sådan, at det via din CBS bruger kan se hvilken uddannelsestype du er i gang med, samt hvilken studieretning du studerer på. Den studerende vil efterfølgende få givet muligheden for at vælge det specifikke fag, vedkommende ønsker samtalen skal tage udgangspunkt i. Når man klikker på det ønskede fag, får brugeren mulighed for at vælge en ud af 10 forhåndsbesluttede emner. Disse emner er valgt af forelæseren/øvelseslæreren, som de mener er de 10 mest populære emner brugerne søger hjælp til. Hvis man vil have hjælp til et emne som ikke er på listen får man mulighed for, at skrive en kommentar hvor vedkommende kan specificere hvilket område brugeren ønsker samtalen skal tage udgangspunkt i. f.eks. kunne dette være, at brugeren vil have en samtale i Programmering og udvikling af små systemer samt databaser med fokus på “scoping”. 

Som en ekstra funktion, har vi tænkt at implementere en slags rangeringsliste alt efter popularitet. Dette betyder at hvis scoping ikke var en del af de 10 populære, men 5 brugere skriver en kommentar om scoping, indikerer det at den er mere væsentlig end en af de andre emner på listen, og derfor prioriteret. Vi vil derfor lave en funktion der gør det muligt, kun at have de mest relevante emner på listen, og efterhånden skifte dem ud alt efter popularitet. Dette ville også gøre det muligt for en forelæser at se hvad han/hun evt. skal lægge mere vægt på i en fremtidig forelæsning.

For at gøre det så let for brugeren som overhovedet muligt, samt at sikre os at vi får et emne som er gyldigt i forhold til fagets undervisning, vil vi på hjemmesiden have en sektion hvor vi anbefaler at brugeren, at direkte kopiere emnet som de har spørgsmål til. På den måde gør vi det let for begge parter, samt sikrer at vi får et emne som der faktisk er blevet undervist i.
Til hvert hovedfag er der tilknyttet de respektive forelæsere. Man får derefter muligheden for at vælge hvilken forelæser som man ønsker at booke en samtale med. Systemet vil derefter i form af klik på forelæser føre klienten videre til et interface, som skal indeholde muligheder hvor den ønskede forelæser er til rådighed. Dette interface vil indeholde en kalender med ledige tider for den respektive forelæser (office hours). De ledige tider afhænger dermed af hvornår forelæseren har markeret, at de har ledig tid til rådgivning. Klienten vælger herefter en af de ledige muligheder for at reservere tiden. Når tiden er reserveret vil brugeren (den studerende) blive sendt videre til en side med bekræftelse. Brugeren skal samtidig have mulighed for at kunne klikke sig ind og se hvilke møder de har booket. De skal samtidig have muligheden for og kunne aflyse et booket møde, hvis brugeren bliver hindret i og kunne dukke op. Dette tænker vi kunne være i form af en “min side”. 

Mht. lokation har vi valgt, at det skal være på forelæserens kontor.

# Kravspecifikationer:

### Aktører:
- Studerende
- Forelæsere på universiteter
- Ledelsen på universiteter (vision til videreudvikling?)

### Liste over kravspecifikationer:

__Studerende__
1. Skal kunne logge på og se oversigt over alle ens fag
2. Skal være fokuseret på den enkeltes studieretning
3. Skal kunne specificeres pr. semester
4. Skal kunne specificeres pr. fag med tilhørende forelæsere
5. Skal kunne kontakte forelæsere for det valgte fag
6. Skal kunne bestille møder med forelæsere for det respektive fag
7. Skal kunne vælge tid til mødet ud fra tilgængelige tider hos forelæseren
8. Skal kunne slette møder

__Forelæsere på universiteter__
 1. Skal kunne logge på og se oversigt over alle de fag man underviser i
 2. Skal kunne specificeres pr. semester
 3. Skal kunne se en oversigt over alle forespørgsler indenfor et givent fag
 4. Skal kunne se en oversigt over alle forespørgsler samt fag
 5. Skal kunne kontakte studerende for en given forespørgsel
 6. Skal kunne slette møder

__Ledelsen på universiteter (vision til videreudvikling?)__
 1. Skal logge ind som administrator
 2. Skal kunne se en oversigt over alle forelæsere
 3. Skal kunne tilknytte/administrere forelæsere til fag pr. semester
 4. Skal kunne se den enkelte forelæsers mødeplan
 5. Skal kunne administrere alle brugere (studerende og forelæsere) på programmet

## Klassediagram:
![Klassediagram](https://i.imgur.com/LyofN1C.png)
