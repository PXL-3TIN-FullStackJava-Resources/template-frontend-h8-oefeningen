## **Oefeningen: Data ophalen met HTTP**


### Oefening 1

Maak een nieuw Angular project h8-oefening1 in de root directory van deze repository.

Gebruik in deze oefening volgende API url:

```
https://overwatch-9dba4.firebaseio.com/heroes.json
```

Of onderstaande JSON file (plaats deze in de assets folder!). Let op, de JSON data heeft een eerder exotische structuur. Denk goed na hoe je hiermee omgaat in de frontend:
```
{
		"heroes":{
			"-KucXneLA4pEVjPOiosp": {
				"abilities":[
					"Heavy pulse rifle",
					"Helix rockets",
					"Sprint",
					"Biotic field",
					"Tactical visor"
				],
				"avatar":"https://d1u1mce87gyfbn.cloudfront.net/hero/soldier-76/hero-select-portrait.png",
				"class":"Offense",
				"difficulty":1,
				"dps":170,
				"name": "soldier 76"
			},
			"-Kuc_g9zO-ra_b0W2A0k": {
				"abilities":[
					"Storm bow",
					"Sonic arrow",
					"Scatter arrow",
					"Dragon strike"
				],
				"avatar":"https://d1u1mce87gyfbn.cloudfront.net/hero/hanzo/hero-select-portrait.png",
				"class":"Defence",
				"difficulty":3,
				"dps":92.5,
				"name": "Hanzo"
			},
			"-Kucft8njA3Hm461p4pA": {
				"abilities":[
					"Rocket hammer",
					"Barrier field",
					"Charge",
					"Fire strike",
					"Earthshatter"
				],
				"avatar":"https://d1u1mce87gyfbn.cloudfront.net/hero/reinhardt/hero-select-portrait.png",
				"class":"Tank",
				"difficulty":1,
				"dps":75,
				"name": "Reinhardt"
			},
			"-KucgrEnzfvlZpZj8S2Q": {
				"abilities":[
					"Sonic amplifier",
					"Crossfade",
					"Amp it up",
					"Sound barrier"
				],
				"avatar":"https://d1u1mce87gyfbn.cloudfront.net/hero/lucio/hero-select-portrait.png",
				"class":"Tank",
				"difficulty":2,
				"dps":75,
				"name": "Lucio"
			},
			"-Kud01oYGn7SD67qv66-": {
				"abilities":[
					"Shuriken",
					"Deflect",
					"Swift strike",
					"Dragonblade"
				],
				"avatar":"https://d1u1mce87gyfbn.cloudfront.net/hero/genji/hero-select-portrait.png",
				"class":"Offense",
				"difficulty":3,
				"dps":86.5,
				"name": "Genji"
			},
			"-KudJKHfWLFf5zBJ7e4G": {
				"abilities":[
					"Biotic Rifle",
					"Sleep dart",
					"Biotic grenade",
					"Nano boost"
				],
				"avatar":"https://d1u1mce87gyfbn.cloudfront.net/hero/ana/hero-select-portrait.png",
				"class":"Support",
				"difficulty":2,
				"dps":28,
				"name": "Ana"
			},
			"-KudTCdxcvBJk804xDzR": {
				"abilities":[
					"Rocket launcher",
					"Jump jet",
					"Concussive blast",
					"Barrage"
				],
				"avatar":"https://d1u1mce87gyfbn.cloudfront.net/hero/pharah/hero-select-portrait.png",
				"class":"Offensve",
				"difficulty":1,
				"dps":120,
				"name": "Pharah"
			}
		}
	}
```

De structuur van de heroes krijg je te zien als je op de link klikt. Voorzie een model en de nodige service om de data op te halen en te mappen naar een model.

Voorzie volgende 3 components met functionaliteiten:

*   Hero.component.ts
    *   Zorgt voor de weergave van een hero
    *   Krijgt één Hero object binnen van de parent (app.component.ts)
    *   Voor het weergeven van de rating, gebruik je een ster (&#9733;). Je kan dit op verschillende manieren doen (bv. Gebruik van een custom pipe & het innerHTML attribuut)
*   Search.component.ts
    *   Zorgt voor de zoek functionaliteit van onze applicatie en heeft 2 input velden: naam & rating. Koppel deze met 2-way binding.
    *   Koppel een event op (keyup) op het inputveld en op (change) op het dropdown menu. Bij het uitvoeren van het event, stuur je de ingegeven waardes terug naar de app.component.ts
*   App.component.ts:
    *   Zorgt voor het weergeven van de searchcomponent en de herocomponent per hero.
    *   Spreekt de service aan voor het ophalen van de data
    *   Voorzie een custom pipe voor het genereren van het aantal sterren.
    *   De afhandeling van de emitted event uit search.component.ts dient hier ook te gebeuren.

Een screenshot van het eindresultaat is terug te vinden op de volgende pagina.

![alt_text](https://i.imgur.com/Vc8xnN7.png "image_tooltip")

Controleer na het maken van deze oefening of je alle wijzigingen naar github hebt gepusht.

### Oefening 2
Maak een nieuw Angular project h8-oefening2 aan in de root directory van deze repository. Maak je eigen inmemory web api of Java spring boot API op basis die crud endpoints voorziet voor volgende data:
```
 {
				"bouwjaar": 2016,
				"merk":"Tesla",
				"prijs":60500,
				"stock":1,
				"type":"Model S"
},
{
				"bouwjaar": 2011,
				"merk":"Peugeot",
				"prijs":16200,
				"stock":3,
				"type":"Partner"
},
{
				"bouwjaar": 2011,
				"merk":"Porsche",
				"prijs":72480,
				"stock":2,
				"type":"911 Turbo"
}			

```


Voorzie de nodige service en model. Voorzie volgende components met de nodige functionaliteiten:

*   App.component.ts
    *   Aanspreken van de service voor alle requests
    *   Weergeven van de data uit onze backend in een tabel
    *   Bij het klikken op de knop “verkoop” wordt de stock verminderd met 1
        *   Als de stock op 0 komt, wordt het object verwijderd
    *   Zorgt voor de afhandeling van het voeg toe formulier
*   Auto-form.component.ts
    *   Weergave & validatie van het formulier
        *   Alle velden zijn verplicht
        *   Bouwjaar moet kleiner zijn dan 2018
        *   Bouwjaar, prijs & stock moeten een getal zijn
    *   De data wordt teruggegeven naar de parent component voor verdere afhandeling


![alt_text](https://i.imgur.com/H0Ued5R.png "image_tooltip")

Controleer na het maken van deze oefening of je alle wijzigingen naar github hebt gepusht.

### Oefening 3
Ga naar de map H8-oefening-debug. Vervolgens run je onderstaand commando in deze map op alle dependencies te installeren:
```
npm install
```

In dit project zitten verschillende fouten. Probeer aan de hand van de error messages in je IDE & developer console de fouten weg te werken zodat je een werkende applicatie krijgt.

Controleer na het maken van deze oefening of je alle wijzigingen naar github hebt gepusht.
