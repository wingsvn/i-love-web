
# sprint 13

## 02.09.2024 leervragen

**formuleer 2-3 leervragen als uitgangspunt voor deze sprint.**

* hoe kan ik routing implementeren in mijn squadpage via frameworks?
* hoe maak ik gebruik van Sveltekit?
* hoe zet ik een project met een framework op?
* hoe kan ik op een efficiënte manier aan verschillende projecten tegelijkertijd werken (management)?
* hoe haal ik data op uit een headless CMS door middel van frameworks?
* wat doet Svelte?
* hoe plan ik mijn tijd in?
* hoe kan ik mijn bewijslast op de juiste manier opleveren?
* hoe kan ik mijn sterke en zwakke punten gebruiken om anderen te helpen?


zone of proximal development
* things you can do on your own
* things you can do with a bit of help
* things you can't yet do, no matter how much help you get

## 04.09.2024 talk/workshop: svelte, sveltekit & directus

**nodejs**
* een javascript runtime`
* routes, fetch, API, data rendering

**sveltekit**
* a library geschreven in svelte
* een web framework van svelte
* heel snel webpagina's genereren
* server-side + client=side rendering
* progressive enhancement: form, enhanced=true
* treeshaking: geen dubbele code
* html, css en javascript worden in één bestand gedaan voor eindgebruikers
* folder based routing: geen route meer schrijven
* GET en POST worden onder water afgehandeld
* server-side rendering only mode --> `export let csr=false` = client-side rendering stoppen
* laadt alleen wat nodig is

**svelte**
* een compiler
* reactive state: kan automatisch veranderingen meenemen
* kan html, css en javascript combineren
* draait o.a. op pinautomaten
* frameworks, zoals svelte, worden gebruikt voor een betere developer experience


**hoe maak ik gebruik van sveltekit?**

open de terminal in je editor en voer de volgende commands uit:

* `npm create svelte@latest my-app` selecteer skeleton project + typescript: no
* `cd my-app`
* `npm install`
* `npm run dev` het starten van je ontwikkelomgeving
* open `http://localhost:5173` in je browser
* `h + enter` voor hulp en shortcuts

### sources
[directus x svelte](https://docs.directus.io/blog/getting-started-directus-sveltekit.html)

[github create a svelte project](https://github.com/ju5tu5/squadpage-sveltekit)


## 09.09.2024 figma workshop: kill your darlings

* shortcut **r** - het maken van een vierkant
* shortcut **o** - het maken van een cirkel
* **cmd+g** - het groeperen van objecten/items
* **cmd+]** - het naar voor plaatsen van een object/item
* **alt** - het aanpassen van de lengte of breedte van een object
* **cmd+shift+g** - het uit elkaar halen van objecten binnen een groep 
* **alt=shift** - het gelijkmatig aanpassen van alle zijden van een object/item


## 11.09.2024 workshop creative coding

### progressive enhancement in svelte
* **progressive enhancement**: a strategy in webs design that pouts emphasis on web content first, allowing everyone to acces the base content and functionality of a web page, whilst users with additional browser features or faster internet acces receive the enhance version instead.

* **creative coding === progressive enhancement === content first**: basis laag + animaties en effecten er boven op


**progressive enhancement: content first** (stappenplan: sveltekit opzetten)
1. maak een tijdelijke kopie van de folder van de squadpage repo
2. installeer een clean install van Sveltekit voor de squadpage
3. voeg in `/routes/+page.js` deze regel code toe `export let car = false`
4. neem in `/lib/fetch-node.js` de code over uit hetzelfde bestand van je laatste node.js project uit sprint 12
5. importeer deze functie in `routes/+page.server.js`
6. check aan de hand van het voorbeeld of je alles goed hebt gedaan hebt
7. copy/paste jullie toegevoegde svelte code terug in `/route/+page.svelte`


### creative coding with css

**enhancement example with css** 
1. scroll-snapping (non-breaking enhancement)
2. scroll animation-timeline (breaking enhancement - gebruik daarom @support (feature detection), dit maakt het een progressive enhancement)


**svelte extensions/pluggins**
* svelte for VS code
* svelte intellisense
* svelte 3 snippets


**creative coding with js**

* special svelte element: `<svelte:window on:mousemove={followPointer}/>`

* `export let csr = true` client-side rendering van javascript aanzetten
* `export let csr = false` er mag geen client-side rendering van javascript gebruikt worden

* 'onMount': functie van Sveltekit, die wordt meegestuurd naar client, bij laden wordt  `onMount` text weergegeven....
* animeren met custom properties
* pas als een svelte component in de document gerenderd is, kan je de DOM manipuleren. Hiervoor gebruik je de `onMOunt` callback function. dit kan handig zijn als je bijvoorbeeld met client-side javascript ...
* svelte heeft ingebouwde _animation_, _transition_, _tween_ en _motion modules_. Hiermee kan je makkelijk op css transitions en animation gebaseerde animaties aan elementen in een svelte component toevoegen.
* zoek op: **svelte transitions** in docs 


## 16.09.2024 workshop prioriteren: van epic, langs (user)stories, naar taken

epic: een handige manier om werk te organiseren en een hiërarchie te creëren door grote projecten en opdrachten op te splitsen in kleinere stukken, waar je tijdens een sprint aan kan werken.
* eg. de website van ... optimaliseren voor zoekmachines
* eg. een nieuwe e-commerce website lanceren
* de website van ... verbeteren

stories maken van epics
eg. een nieuwe e-commerce website lanceren
* een winkelmandje toevoegen
* betalingsmogelijkheden toevoegen
* een klantenservice portaal toevoegen

eg. een bestaande website verbeteren voor ...
* de website sneller maken --> testen
* de website gebruiksvriendelijker maken --> testen
* een website toegankelijker maken --> testen

userstories maken van stories
eg. een winkelmandje toevoegen
* als bezoeker wil ik producten in mijn winkelmandje kunnen doen om overzicht te houden van wat ik aanschaf.
* als bezoeker wil ik producten kunnen verwijderen uit mijn winkelmandje als ik iets gevonden heb wat beter past bij wat ik nodig heb.
* als bezoeker wil ik overzicht houden op het uit te geven bedrag om het gevoel te hebben in controle te zijn.

stories vs user stories
met user stories kun je echt taken maken en heb je meer grip in wat je moet doen.

taken
eg. een winkelmandje toevoegen
* database voor winkelmandje
* overzicht winkelmandje tonen in html
* producten verwijderen uit database
* producten uit het overzicht verwijderen
* interface ontwerpen voor bedieningspaneel voor verwijderen van producten
* interface voor pop-up 'verder shoppen of doorgaan naar betaling'
* icon/knop voor winkelmandje ontwerpen


planning poker
* een consensus-gebaseerde techniek voor het schatten van de moeilijkheidsgraad van een taak

MoSCoW
* must haves: dit moet af op de deadline.. las het niet af is dan is het project gefaald
* should haves: dit zou eigenlijk best wel af moeten, het project is een beetje jammer al het niet af is.
* could haves: dit kan, mits we tijd over hebben
* want to have but will not have this time around: dit zijn goede ideeën en nuttig om te noteren, maar we komen er nu niet aan toe (misschien volgende sprint?)



## 18.09.2024 wrap-up: hoe lever je een project op?

* refactored code: gestructureerde code (conventies), semantiek, geen commented code, geen console.log(), goede tabs, etc..
* readMe.md: kenmerken, live link, screenshots, instructies (uitleg over het gebruik), installatiehandleiding, CMS uitleg, huisstijl, bijdragen (hints voor volgende dev teams), gebruikte bronnen, badges met gebruikte technologie
* live zetten: GitHub pages, Vercel, Netlify, onrender


# sprint 14

## 23.09.2024


## 26.09.2024
* [analyseren van accessibility tool button](https://github.com/fdnd-agency/buurtcampus-oost/issues/155)
* [ontwerpen van accessibility tool button](https://github.com/fdnd-agency/buurtcampus-oost/issues/136)

## 27.09.2024
* ik heb een code/design review gedaan op de code van yujing [code/design review: issues](https://github.com/lisagjh/voorhoede/issues/4) [code/design review: issues](https://github.com/lisagjh/voorhoede/issues/5)
* [accessibility test](https://github.com/fdnd-agency/buurtcampus-oost/issues/140)


# sprint 15 choices choices

# 14.10.2024 Hoe kies je een nieuw tech-stack?

Welke factoren komen kijken bij het kiezen van een tech-stack?
* schaalbaarheid
* expertise
* kosten
* performance
* onderhoud
* grootte van je team

Verder moet je nog rekening houden met
* user experience
* content manager experience
* developer experience




