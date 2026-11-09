# Loggbok för projekt

## Inledning

## Mina bidrag till projektet:

### Få igång email mikrotjänst

Inledningsvis skulle jag se till att email-mikrotjänsten som var mitt bidrag till backend-tjänsten vi skapade i våras fortfarande fungerar. Jag testade detta i swagger genom att gå igenom alla endpoints som krävs för att lägga en beställnig, logga in med jwt-token som en vanlig användare, 

### Gemensam header och footer

Alla sidor ska visa en gemensam header och footer, en header som ska innehålla webshopens namn, innan inloggning en flik för att logga in en befintlig användare. För inloggad användare visas en flik för att visa produkter, en varukorg från vilken man lägger beställningar samt en knapp för att logga ut. I footern visas en copyrightsymbol, webshopens namn, årtal samt all rights reserved. För att skapa grundstrukturen för detta skapade jag en .tsx-sida var för header och footer med funktioner för att returnera det som ska visas i respektive sidhuvud och -fot. Innehållet i dessa har löpande lagts till under projektets gång.

### Konfigurera testmiljö och komponenttesta ProductCard

Jag har konfigurerat testmiljön i applikationen, genom att skapa konfigurationssidor.med en src

### Produkter ska få attribut: category och imageUrl i backend

Jag lade till två attribut som ska visas vid varje produkt, kategori och en url för att visa produktbild. I Produktsidan product-cart.ts, som ansvarar för att hämta produkter från backend, under exportfunktionen av typen Product som skickar vidare en produkt för att visas bland produktkorten, lade jag till attributen category:string och imageUrl:string vilket bestämmer att båda attributen ska utgöras av textsträngar. I ProductCard.tsx (produktkortssidan), under funktionen för att visa produktkorten lade jag till en img-tag (tag för att visa bilder i frontend) med src={product.imageUrl}, vilket hämtar 

### Uppdatera så att formuläret inkluderar category och imageUrl

Även formuläret för att ligga till en produkt på admin-sidan skulle visa ett fält för att lägga till kategori och produktbild. 

### Frontend ska kunna visa imageUrl för produkter

### Product-service endpoint & detaljvy för produkt

###

## Det agila arbetet
