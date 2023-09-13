- F
	- Udstille CRUD funktionalitet i backend (bibliotek), til k/v (Key/value pairs)
	- Hente k/v pairs fra en liste af forskellige backends (biblioteker)
		- Grupper k/v i forhold til hvilken backend de kommer fra, og hvilket miljø(?)
	- Hostdiscovery i frontend
	- Access rights management på front- og backend så man kun kan redigere visse felter
	- Log ændringer så der kan læses en liste af hvornår og af hvem ændringer er udført.
- A
	- Et system leveret som en web-applikation hvor brugeren, i første omgang en udvikler, men med den endelige kunde i tankerne under udvikling, kan redigerer . Der skal altså ikke blokeres for at applikationen kan tilpasses ikke-tech-savvy brugere. Brugeren skal efter login kunne danne sig et overblik over hvilke værdier de kan ændre, og til hvilke muligheder, og hvilket miljø de er i.
- C
	- Udviklet af ekstern partner på 3 måneder, hvilket sætter begrænsninger på scope
	- Udviklere er uni-studerende, og har dermed begrænsede færdigheder
	- Udviklet i samarbejde med Nykredit
	- Fungerer i micro-service baseret miljø
- T
	- Et sprog der faciliterer OOP
		- Skal skrives som OOP
		- Muligvis bestemt af eksisterende bibliotek
	- hosting???
- O
	- K/V
	- Backends
	- User
		- Role / Permission
	- Log
	- ???
		- Der skal stå mere men vi er dumme
- R
	- Et adminstrationsværktøj der bruges til at ændre parametre som andre applikationer læser. Kun brugere med tilstrækkelige rettigheder kan redigere, og alle ændringer logges så det senere kan audites eller rulles tilbage.

### Spørgsmål
- Standalone program (webapplikation). Er web et krav eller bare cross-platform? Hvor let skal det være at sætte op? Altså er web et krav fordi en hver skal kunne åbne uden installation?
- Hvad tænker du eventuelt om at det primært skal være udviklet efter OOP paradigmet? Ser du, som mere erfaren end os, nogle barrierer vi ville skulle navigere.
- Hvad er vores ansvarsområde ang. biblioteket / backenden? Hvor meget findes i forvejen, f.eks. mulighed for at hente K/V fra  DB, eller at skrive tilbage? 
	- Er backenden standalone eller en udvidelse af det eksisterende bibliotek? Skal vi redigere/tilføje til eksisterende bibliotekskode eller lave en ny service der interfacer med jeres biblioteker (stadig i backend)?
		- Hvordan fungere det rent organisatorisk hvis vi skal ændre eksisterende kode
		- Hvis vi skal udvide eksisterende kodebase, hvilken tech-stack bruger den så?
	- Snakker vi direkte med asortimentet af databaser, eller håndteres det andetsteds?
- Ang. host discovery, vil der så findes en liste af backends frontenden kan forsøge at forbinde til, eller skal vi lave noget der f.eks. kontakter en central server for at registrere sig

### Videre

- Objects
	- 

| Events \\ Classes |     | 
| ----------------- | --- |
