- (un)signed repræsentation
	- TJEK ANTAL 0'ER SKREVET
	- overflow i positiv retning -> fra høj værdi til lav
	- overflow i negativ retning -> fra lav til høj
		- `-TMin` overflower i negativ retning til `TMIN`
	- blandet beregnes som unsigned
		- Bit repræsentation bruges unsigned
- Parallelitet
	- Tæl cykluser: Husk at pipeline ordentligt
		- 16 tal ganget sammen kræver ikke 8+6+5+5=24 cykluser, da nogle af stykkerne i anden omgang kan pipelines lige efter første 
		- ![](image%201.png)
- Assembly og program-trace
	- Argumenter er caller-saved
	- Sæt overskydende felter "UK" (ukendt) i traces
	- Rækken efter RET skal stadig have værdier
		- Værdier er kendt, bare ikke instruktion
		- Dermed er værdier på rækken derefter heller ikke kendt
		- ![](Pasted%20image%2020240528124218.png)
- BRUG KORREKTE DATATYPER
	- STÅR DER LONG SÅ BRUG LONG
- Parallelism
	- signal before unlocking