- Focus på C#
- Ladestander der lader billigt intelligent, fra en app. Regner måske ud hvornår man skal afsted.
- Grafer i app, oplys bruger
- App skal interface med mock stander, siden faktisk kommunikation nok ikke bliver muligt indenfor vores tidsramme.
- Teknologiske krav
	- C# og azure
	- Foretrækker React
		- React router, ikke Next
			- Eller hvad? Så længe det er statisk
		- Tailwind
		- Vite
		- https://ui.shadcn.com/
	- Deploy til azure pipelines
		- Kør git i azure
	- Azure functions
		- Ikke "Manage azure functions"
		- bare "Azure functions App"
- **Mange point at hive i at have brugt flere "komplicerede" servicer**
	- Langt ude over niveau, konceptuelt. Simpelt i praksis.
		
- Kombiner 3 apps funktionaliteter
	- Tesla app til at overvåge bilens batteriniveau
		- Tesla app
	- App til lader som givet en strømpris udregner priser, og måske kan schedule ladninger manuelt
		- TrueEnergi
			- Sætter bil til at lade når det er billigt
			- Virker med flere brands af ladere
		- Easee
	- 3. app til at overvåge strømpriser for hvornår der skal lades
- IQ plug lader

Man kan med nemid få adgang til brugers strømaftale på en eller anden måde. Måske el-net.


På langt sigt, integrer https://starti.app