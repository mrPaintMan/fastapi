# Prestandamätningar

Oberoende TechEmpower prestandamätningar visar att **FastAPI**-applikationer som körs under Uvicorn är <a href="https://www.techempower.com/benchmarks/#section=test&runid=7464e520-0dc2-473d-bd34-dbdfd7e85911&hw=ph&test=query&l=zijzen-7" class="external-link" target="_blank">något av de snabbaste Python-ramverken som finns</a>, endast under Starlette och Uvicorn själva (används internt av FastAPI).

Men när du kontrollerar prestandamätningar och jämförelser bör du ha följande i åtanke.

## Prestandamätningar och hastighet

När du kollar på prestandamätningarna är det vanligt att se flera verktyg av olika typer jämföras som likvärdiga.

Specifikt, att se Uvicorn, Starlette och FastAPI jämförda tillsammans (bland många andra verktyg).

Ju enklare problemet som löses av verktyget är, desto bättre prestanda kommer det att få. Och de flesta prestandamätningar testar inte de extra funktioner som erbjuds av verktyget.

Hierarkin ser ut så här:

* **Uvicorn**: en ASGI-server
    * **Starlette**: (använder Uvicorn) ett web-mikroramverk
        * **FastAPI**: (använder Starlette) Ett API-mikroramverk med ett flertal ytterligare funktioner för att bygga API-er, med data-validering, osv.

* **Uvicorn**:
    * Kommer ha den bästa prestandan, eftersom den inte har mycket extra kod förutom själva servern.
    * Du skriver inte en applikation direkt i Uvicorn. Det skulle innebära att din kod skulle behöva inkludera mer eller mindre all kod som tillhandahålls av Starlette (eller **FastAPI**). Och om du gjorde det, skulle din slutliga applikation ha samma overhead som om du hade använt ett ramverk och minimerat din appkod och buggar.
    * Om du tänker jämföra Uvicorn, jämför det med Daphne, Hypercorn, uWSGI, etc. Applikationsservrar.
* **Starlette**:
    * Kommer ha den näst bästa prestandan, efter Uvicorn. Faktum är att Starlette använder Uvicorn för att köra. Så det kan antagligen bara bli "långsammare" än Uvicorn genom att behöva köra mer kod.
    * Men det ger dig verktygen för att bygga enkla webbapplikationer, med routing baserad på vägar, etc.
    * Om du tänker jämföra Starlette, jämför det med Sanic, Flask, Django, etc. Webb-ramverk (eller mikro-ramverk).
* **FastAPI**:
    * På samma sätt som Starlette använder Uvicorn och inte kan vara snabbare än det, använder **FastAPI** Starlette, så det kan inte vara snabbare än det.
    * FastAPI tillhandahåller fler funktioner ovanpå Starlette. Funktioner som du nästan alltid behöver när du bygger API:er, som datavalidering och serialisering. Och genom att använda det får du automatisk dokumentation gratis (den automatiska dokumentationen lägger inte ens till overhead för att köra applikationer, den genereras vid uppstart).
    * Om du inte använde FastAPI och använde Starlette direkt istället (eller ett annat verktyg, som Sanic, Flask, Responder, etc.) skulle du behöva implementera all datavalidering och serialisering själv. Så din slutliga applikation skulle fortfarande ha samma overhead som om den var byggd med FastAPI. Och i många fall är denna datavalidering och serialisering den största mängden kod som skrivs i applikationer.
    * Så genom att använda FastAPI sparar du utvecklingstid, buggar, rader kod, och du skulle förmodligen få samma prestanda (eller bättre) som om du inte använde det (eftersom du skulle behöva implementera allt i din egen kod).
    * Om du jämför FastAPI, jämför det med ett webbapplikationsramverk (eller verktygssats) som tillhandahåller datavalidering, serialisering och dokumentation, som Flask-apispec, NestJS, Molten, etc. Ramverk med integrerad automatisk datavalidering, serialisering och dokumentation.
