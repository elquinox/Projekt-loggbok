# Loggbok för projekt

## Inledning

Vi har under detta projektarbeta utvecklat en fullstack-webshop byggd med en mikrotjänstbaserad arkitektur. Vi har under denna termin utvecklat frontenddelen till mikrotjänsterna vi utvecklade i våras. Arbetet har omfattat utveckling av funktionalitet, löpande förbättringar av användargränssnittet samt konfigurering av testmiljö och automatiserade tester. Mina bidrag har varit att få igång projektets email-mikrotjänst, utveckla en gemensam layout, utöka produktinformationen med nya attribut samt implementera funktionalitet för att visa enskilda produkter med kategori och bild samt att konfigurera testmiljö och skriva komponenttester som kan köra både lokalt och i GitHub.

## Mina bidrag till projektet:

### Få igång email mikrotjänst

Inledningsvis skulle jag se till att email-mikrotjänsten som var mitt bidrag till backend-tjänsten vi skapade i våras fortfarande fungerar. Jag testade detta i swagger genom att gå igenom alla endpoints som krävs för att lägga en beställnig, logga in med jwt-token som en vanlig användare, hämta produkter, skapa order och se att bekräftelsemailet skrevs ut i konsollfönstret lokalt. 

### Gemensam header och footer

Alla sidor ska visa en gemensam header och footer, en header som ska innehålla webshopens namn, innan inloggning en flik för att logga in en befintlig användare. För inloggad användare visas en flik för att visa produkter, en varukorg från vilken man lägger beställningar samt en knapp för att logga ut. I footern visas en copyrightsymbol, webshopens namn, årtal samt all rights reserved. För att skapa grundstrukturen för detta skapade jag en .tsx-sida var för header och footer med funktioner för att returnera det som ska visas i respektive sidhuvud och sidfot. Innehållet i dessa har löpande lagts till under projektets gång.

### Konfigurera testmiljö och komponenttesta ProductCard

Jag har konfigurerat testmiljön i applikationen, genom att skapa konfigurations- och setup-filer med Vitest och React Testing library för att nödvändiga beroenden skulle köras. Sedan skrev jag komponenttest för ProductCard som verivierar att produktiformationen visas korrekt och att funktionen onAdd anropas med rätt produkt när användaren klickar på "lägg till i varukorg". 
Testerna kan köras lokalt genom att köra kommandot "npm test" i utvecklingsmiljöns terminal och körs även vid build i GitHub Actions-flödet vid koduppladdning (push). På så sätt kontolleras automatiskt att grundläggande funktionalitet vidmakthålls under projektets gång vid framtida koduppändring.

### Produkter ska få attribut: category och imageUrl i backend

Jag lade till två attribut som ska visas vid varje produkt, kategori och en url för att visa produktbild. I Produktsidan product-cart.ts, som ansvarar för att hämta produkter från backend, under exportfunktionen av typen Product som skickar vidare en produkt för att visas bland produktkorten, lade jag till attributen category:string och imageUrl:string vilket bestämmer att båda attributen ska utgöras av textsträngar. I ProductCard.tsx (produktkortssidan), under funktionen för att visa produktkorten lade jag till en img-tag (tag för att visa bilder i frontend) med src={product.imageUrl}, vilket hämtar en bild från en webbadress. 

### Uppdatera så att formuläret inkluderar category och imageUrl

Även formuläret för att lägga till en produkt på admin-sidan skulle visa ett fält för att lägga till kategori och produktbild. Jag uppdaterade produktformuläret i adminProductPage.tsx genom att lägga till const [category, setCategory] och const [imageUrl, setImageUrl] och sedan en input-tag var för imageUrl samt category. På så sätt kan en admin välja kategori för en produkt och klistra in en länk till en produktbild för ett mer detaljerat produktkort.


### Frontend ska kunna visa imageUrl för produkter
Jag har uppdaterat frontend så att produktbilder visas med hjälp av det nya attributet imageUrl. Funkitonen implementerades på både produktsidan (ProductCard.tsx) och adminsidan (adminProductPage.tsx). När en produkt hämtas från backend finns en bildadress kopplad till den som används i frontend för att visa en bild på produkten. Jag uppdaterade testet för ProductCard för att säkerställa att både kategori och imageUrl hämtas och visas korrekt.


### Product-service endpoint & detaljvy för produkt

###

## Det agila arbetet

Vi har använt trello för att strukturera och dela upp arbetet, där vi infogat uppgifterna från backloggen. Vi har haft Weekly planning varje måndag där vi planerat och delat upp arbetet inför veckan, Daily standups de övriga veckodagarna där vi stämt av arbetet och kommit överrens om vidare uppdelning av arbetet när någon del blivit klar, samt Sprint retrospect på fredagar där vi redovisat veckans arbete genom att visa en demo över sidans uppdaterade funktioner. Vi har använt Start-Stop-Continue för att diskutera vad vi ska börja göra mer av, vad vi ska upphöra med och vad vi ska fortsätta med, för att löpande förbättra och effektivisera vårt arbete. Vi har använt Scrum poker, en metod för att uppskatta varje uppgifts omfattning där var och en av gruppmedlemmarna röstar genom att ge poängen 1, 3, 5, 8 eller 13 för uppskattad omfattning av uppgiften, för att ge arbetet en jämlik och rättvis fördelning.
