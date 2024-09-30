# FastAPI

<style>
.md-content .md-typeset h1 { display: none; }
</style>

<p align="center">
  <a href="https://fastapi.tiangolo.com"><img src="https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png" alt="FastAPI"></a>
</p>
<p align="center">
    <em>FastAPI ramverk, hög prestanda, snabbt att lära sig, snabbt att koda, redo för produktion</em>
</p>
<p align="center">
<a href="https://github.com/fastapi/fastapi/actions?query=workflow%3ATest+event%3Apush+branch%3Amaster" target="_blank">
    <img src="https://github.com/fastapi/fastapi/workflows/Test/badge.svg?event=push&branch=master" alt="Test">
</a>
<a href="https://coverage-badge.samuelcolvin.workers.dev/redirect/fastapi/fastapi" target="_blank">
    <img src="https://coverage-badge.samuelcolvin.workers.dev/fastapi/fastapi.svg" alt="Täckning">
</a>
<a href="https://pypi.org/project/fastapi" target="_blank">
    <img src="https://img.shields.io/pypi/v/fastapi?color=%2334D058&label=pypi%20package" alt="Paketversion">
</a>
<a href="https://pypi.org/project/fastapi" target="_blank">
    <img src="https://img.shields.io/pypi/pyversions/fastapi.svg?color=%2334D058" alt="Pythonversioner som stöds">
</a>
</p>

---

**Dokumentation**: <a href="https://fastapi.tiangolo.com/sv/" target="_blank">https://fastapi.tiangolo.com/sv/</a>

**Källkod**: <a href="https://github.com/fastapi/fastapi" target="_blank">https://github.com/fastapi/fastapi</a>

---

FastAPI är ett modernt, snabbt (högpresterande), web-ramverk för att skapa Python-API:er med hjälp av Pythons standard typ tips.

Dess nyckelfunktioner är:

* **Hastiget**: Väldigt högpresterande, i klass med **NodeJS** och **Go** (tack vare Starlette och Pydantic). [En av de snabbaste ramverken tillgängliga](#performance)
* **Snabbt att koda**: Ökar utveklingshastigheten med mellan 200% och 300%. *
* **Färre buggar**: Minskar ungefär 40% av buggar skapade av utvecklaren. *
* **Intuitivt**: Utmärkt redigeringsstöd. <abbr title="även kallat auto-complete, autocompletion, IntelliSense">Kodkomplettering</abbr> överallt. Mindre felsökning.
* **Enkelt**: Designad för att vara lätt att använda och lära sig. Mindre tid att läsa dokumentation.
* **Kort**: Minimera kodduplicering. Flera funktioner från varje parameterdeklaration. Färre buggar.
* **Robust**: Få produktionsklar kod. Med automatisk, interaktiv dokumentation.
* **Standardbaserad**: Baserad på (och fullt kompatibel med) de öppna API-standarderna: <a href="https://github.com/OAI/OpenAPI-Specification" class="external-link" target="_blank">OpenAPI</a> (tidigare känt som Swagger) och <a href="https://json-schema.org/" class="external-link" target="_blank">JSON Schema</a>.

<small>* Uppskattning baserad på testning i ett internt utvecklingsteam som bygger produktionsapplikationer.</small>

## Sponsorer

<!-- sponsorer -->

{% if sponsors %}
{% for sponsor in sponsors.gold -%}
<a href="{{ sponsor.url }}" target="_blank" title="{{ sponsor.title }}"><img src="{{ sponsor.img }}" style="border-radius:15px"></a>
{% endfor -%}
{%- for sponsor in sponsors.silver -%}
<a href="{{ sponsor.url }}" target="_blank" title="{{ sponsor.title }}"><img src="{{ sponsor.img }}" style="border-radius:15px"></a>
{% endfor %}
{% endif %}

<!-- /sponsors -->

<a href="https://fastapi.tiangolo.com/fastapi-people/#sponsors" class="external-link" target="_blank">Andra sponsorer</a>

## Åsikter

"_[...] Jag använder **FastAPI** mycket numera. [...] Jag planerar faktiskt att använda det för alla mina teams **ML tjänster på Microsoft**. Vissa av dom kommer integreras i kärnprodukten **Windows** och några **Office** produkter._"

<div style="text-align: right; margin-right: 10%;">Kabir Khan - <strong>Microsoft</strong> <a href="https://github.com/fastapi/fastapi/pull/26" target="_blank"><small>(ref)</small></a></div>

---

"_Vi valde **FastAPI** biblioteket för att skapa en **REST** server som kan användas för att få **prognoser**. [för Ludwig]_"

<div style="text-align: right; margin-right: 10%;">Piero Molino, Yaroslav Dudin, och Sai Sumanth Miryala - <strong>Uber</strong> <a href="https://eng.uber.com/ludwig-v0-2/" target="_blank"><small>(ref)</small></a></div>

---

"_**Netflix** är glada att kunna tillkännage att vi släpper källkoden till vårt **krishanterings**-Orkestreringsramverk: **Dispatch**! [byggt med **FastAPI**]_"

<div style="text-align: right; margin-right: 10%;">Kevin Glisson, Marc Vilanova, Forest Monsen - <strong>Netflix</strong> <a href="https://netflixtechblog.com/introducing-dispatch-da4b8a2a8072" target="_blank"><small>(ref)</small></a></div>

---

"_Jag är stormförtjust i **FastAPI**. Det är så roligt!_"

<div style="text-align: right; margin-right: 10%;">Brian Okken - <strong><a href="https://pythonbytes.fm/episodes/show/123/time-to-right-the-py-wrongs?time_in_sec=855" target="_blank">Python Bytes</a> podcast värd</strong> <a href="https://twitter.com/brianokken/status/1112220079972728832" target="_blank"><small>(ref)</small></a></div>

---

"_Helt ärligt, vad du har byggt ser superbra och polerat ut. På många sätt är det vad jag ville att **Hug** skulle vara - det är riktigt inspirerande att se någon bygga det._"

<div style="text-align: right; margin-right: 10%;">Timothy Crosley - <strong>Skaparn av <a href="https://www.hug.rest/" target="_blank">Hug</a></strong> <a href="https://news.ycombinator.com/item?id=19455465" target="_blank"><small>(ref)</small></a></div>

---

"_Om du vill lära dig ett **modernt ramverk** för att byffa REST APIer, kolla in **FastAPI** [...] Det är snabbt, enkelt att använda och lätt att lära sig [...]_"

"_We've switched over to **FastAPI** for our **APIs** [...] I think you'll like it [...]_"
"_Vi har gått över till **FastAPI** för våra **APIer** [...] Jag tror du kommer gilla det [...]_"

<div style="text-align: right; margin-right: 10%;">Ines Montani - Matthew Honnibal - <strong>grundarna av <a href="https://explosion.ai" target="_blank">Explosion AI</a> - skaparna av <a href="https://spacy.io" target="_blank">spaCy</a></strong> <a href="https://twitter.com/_inesmontani/status/1144173225322143744" target="_blank"><small>(ref)</small></a> - <a href="https://twitter.com/honnibal/status/1144031421859655680" target="_blank"><small>(ref)</small></a></div>

---

"_Om någon söker ramverk för att bygga ett produktionsredo Python API skulle jag starkt rekommendera **FastAPI**. Det är **vackert designat**, **enkelt att använda** och **väldigt skalbart**, det har blivit en **nyckelkomponent** i våran API-först utvecklingsstratergi och står för många automationer och tjänster såsom vårt Virtual TAC Engineer._"

<div style="text-align: right; margin-right: 10%;">Deon Pillsbury - <strong>Cisco</strong> <a href="https://www.linkedin.com/posts/deonpillsbury_cisco-cx-python-activity-6963242628536487936-trAp/" target="_blank"><small>(ref)</small></a></div>

---

## **Typer**, FastAPI för CLI:er

<a href="https://typer.tiangolo.com" target="_blank"><img src="https://typer.tiangolo.com/img/logo-margin/logo-margin-vector.svg" style="width: 20%;"></a>

Om du bygger en <abbr title="Command Line Interface">CLI</abbr> app till för terminalen istället för ett web API, kolla in <a href="https://typer.tiangolo.com/" class="external-link" target="_blank">**Typer**</a>.

**Typer** är FastAPIs lillebror. Och är avsedd att vara **FastAPI för CLI:er**. ⌨️ 🚀

## Krav

FastAPI står på axlarna av jättar:

* <a href="https://www.starlette.io/" class="external-link" target="_blank">Starlette</a> för web-delarna.
* <a href="https://docs.pydantic.dev/" class="external-link" target="_blank">Pydantic</a> för data-delarna.

## Installation

Skapa och aktivera en <a href="https://fastapi.tiangolo.com/sv/virtual-environments/" class="external-link" target="_blank">virtuell miljö</a> och installera sedan FastAPI:

<div class="termy">

```console
$ pip install "fastapi[standard]"

---> 100%
```

</div>

**Notera**: Säkerställ att du har `"fastapi[standard]"` inom citationstecken för att säkerställa att det fungerar på samtliga terminaler.

## Exempel

### Skapa

* Skapa filen `main.py` med:

```Python
from typing import Union

from fastapi import FastAPI

app = FastAPI()


@app.get("/")
def read_root():
    return {"Hello": "World"}


@app.get("/items/{item_id}")
def read_item(item_id: int, q: Union[str, None] = None):
    return {"item_id": item_id, "q": q}
```

<details markdown="1">
<summary>Eller använd <code>async def</code>...</summary>

Om din kod använder `async` / `await`, använd `async def`:

```Python hl_lines="9  14"
from typing import Union

from fastapi import FastAPI

app = FastAPI()


@app.get("/")
async def read_root():
    return {"Hello": "World"}


@app.get("/items/{item_id}")
async def read_item(item_id: int, q: Union[str, None] = None):
    return {"item_id": item_id, "q": q}
```

**Notera**:

Om du inte redan känner till det, Kolla in _"In a hurry?"_ avsnittet av <a href="https://fastapi.tiangolo.com/async/#in-a-hurry" target="_blank">`async` och `await` i dokumentationen</a>.

</details>

### Kör

Kör server med:

<div class="termy">

```console
$ fastapi dev main.py

 ╭────────── FastAPI CLI - Development mode ───────────╮
 │                                                     │
 │  Serving at: http://127.0.0.1:8000                  │
 │                                                     │
 │  API docs: http://127.0.0.1:8000/docs               │
 │                                                     │
 │  Running in development mode, for production use:   │
 │                                                     │
 │  fastapi run                                        │
 │                                                     │
 ╰─────────────────────────────────────────────────────╯

INFO:     Will watch for changes in these directories: ['/home/user/code/awesomeapp']
INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
INFO:     Started reloader process [2248755] using WatchFiles
INFO:     Started server process [2248757]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
```

</div>

<details markdown="1">
<summary>Om kommandot <code>fastapi dev main.py</code>...</summary>

Kommandot `fastapi dev` läser `main.py` filen, upptäcker **FastAPI** appen i filen, och startar en <a href="https://www.uvicorn.org" class="external-link" target="_blank">Uvicorn</a> server.

Som standard kommer `fastapi dev` starta med auto-omladdning (auto reload) för lokal utveckling.

Du kan läsa mer om det i <a href="https://fastapi.tiangolo.com/fastapi-cli/" target="_blank">FastAPI CLI dokumentationen</a>.

</details>

### Checka

Öppna länken <a href="http://127.0.0.1:8000/items/5?q=enSöksträng" class="external-link" target="_blank">http://127.0.0.1:8000/items/5?q=enSöksträng</a> i webbläsaren.

Du kommer se JSON svaret:

```JSON
{"item_id": 5, "q": "enSöksträng"}
```

Du har alltså nu redan skapat ett API som:

* Tar emot ett HTTP anrop i <abbr  title="Även kallat path(s)">_vägarna_</abbr> `/` och `/items/{item_id}`.
* Tar emot `GET` <abbr title="Även kallat HTTP metoder"><em>operationer</em></abbr> i båda <abbr title="Även kallat path(s)">_vägarna_</abbr>  
* Har en _vägparameter_ `item_id` som bör vara av typen `int`.
* Har en frivillig _frågeparameter_ `q` som bör vara av typen `str`.

### Interaktiv API dokumentation

Gå nu till <a href="http://127.0.0.1:8000/docs" class="external-link" target="_blank">http://127.0.0.1:8000/docs</a>.

Där finner du den automatiskt skapade interaktiva API dokumentationen (tillhandahållet av <a href="https://github.com/swagger-api/swagger-ui" class="external-link" target="_blank">Swagger UI</a>).

![Swagger UI](https://fastapi.tiangolo.com/img/index/index-01-swagger-ui-simple.png)

### Alternativ API dokumentation

Gå nu vidare till <a href="http://127.0.0.1:8000/redoc" class="external-link" target="_blank">http://127.0.0.1:8000/redoc</a>.

Där finns den alternativa auto-skapade dokumentationen (tillhandahållet av <a href="https://github.com/Rebilly/ReDoc" class="external-link" target="_blank">ReDoc</a>):

![ReDoc](https://fastapi.tiangolo.com/img/index/index-02-redoc-simple.png)

## Exempel på uppgradering

Modifiera `main.py` filen för att ta emot en anropskropp (body) från ett `PUT` anrop.

Skapa anropskroppen med standard Python typer, med hjälp av Pydantic.

```Python hl_lines="4  9-12  25-27"
from typing import Union

from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()


class Item(BaseModel):
    name: str
    price: float
    is_offer: Union[bool, None] = None


@app.get("/")
def read_root():
    return {"Hello": "World"}


@app.get("/items/{item_id}")
def read_item(item_id: int, q: Union[str, None] = None):
    return {"item_id": item_id, "q": q}


@app.put("/items/{item_id}")
def update_item(item_id: int, item: Item):
    return {"item_name": item.name, "item_id": item_id}
```
`fastapi dev` servern borde laddas om automatiskt.

### Uppgradering: interaktiva API dokumentationen

Gå nu till <a href="http://127.0.0.1:8000/docs" class="external-link" target="_blank">http://127.0.0.1:8000/docs</a>.

* Den interaktiva API dokumentationen kommer att vara automatiskt uppdaterad med den nya anropskroppen:

![Swagger UI](https://fastapi.tiangolo.com/img/index/index-03-swagger-02.png)

* Klicka på knappen "Try it out", den låter dig fylla i parametrarna och direkt interagera med ditt API:

![Swagger UI interaction](https://fastapi.tiangolo.com/img/index/index-04-swagger-03.png)

* Klicka sedan på "Eexcute" knappen, användargränssnittet kommer kommunicera med ditt API, skicka parametrarna, hämta svaret och visa dem på skärmen:

![Swagger UI interaction](https://fastapi.tiangolo.com/img/index/index-05-swagger-04.png)

### Uppgradering av den alternativ API dokumentationen

Och nu, gå till <a href="http://127.0.0.1:8000/redoc" class="external-link" target="_blank">http://127.0.0.1:8000/redoc</a>.

* Den alternativa dokumentationen kommer också att reflektera den nya frågeparametern (query-parameter) och anropskroppen:

![ReDoc](https://fastapi.tiangolo.com/img/index/index-06-redoc-02.png)

### Sammanfattning

Sammanfattningsvis deklarerar du typer av parametrar, anropskroppar och annat **en gång**, som funktionsparametrar.

Du gör detta med hjälp av Pythons moderna standard typer.

Du behöver inte lärra dig ny syntax, metoder eller klasser för ett specifikt bibliotek, etc.

Endast standard **Python**.

Exempelvis, för en `int`:

```Python
item_id: int
```

eller för en mer komplex `Item` modell:

```Python
item: Item
```

...och med endast denna deklaration får du:

* Redigeringsstöd som inkluderar:
    * Kodkomplettering.
    * Typkontrollering.
* Validering av data:
    * Tydliga automatiska felmeddelanden när datan är ogiltig.
    * Validering även för djupt nestlade JSON objekt.
* <abbr title="även kallat: serialisering, parsing (eng), marshalling (eng)">Konvertering</abbr> av inkommande data som kommer från nätverket till Pythons datatyper. Konvertering sker från:
    * JSON.
    * Vägparametrar (path parameters).
    * Frågeparameters (query parameters).
    * Kakor (cookies).
    * Sid-huvuden (headers).
    * Formulär.
    * Filer.
* <abbr title="även kallat: serialisering, parsing (eng), marshalling (eng)">Konvertering</abbr> av utgående data från Python datatyper till nätverksdata (som JSON): Konvertering sker från:
    * Python typer (`str`, `int`, `float`, `bool`, `list`, m. fl.).
    * `datetime` objekt.
    * `UUID` objekt.
    * Databasmodeller.
    * ...och många fler.
* Automatisk och interaktiv API dokumentation, med 2 olika användargränssnitt:
    * Swagger UI.
    * Redoc.

---

Med återblick på tidigare kodexempel; **FastAPI** kommer:

* Validera att typen av `item_id` är `int` för både `GET` och `PUT` anrop.
    * Om så ej är fallet kommer klienten få ett använbart och tydligt felmeddelande.
* Leta efter en valfri frågeparameter vid namn `q` (såsom i `http://127.0.0.1:8000/items/foo?q=enSöksträng`)
    * Eftersom `q` parametern är deklarerad med `= None`, så är den valfri.
    * Utan `None` skulle den vara nödvändig (likt anropskroppen för `PUT` anrop).
* Läsa anropskroppen som JSON för `PUT` anrop till `/items/{item_id}`:
    * Kontrollera att anropskroppen har attributen `name`, som bör ha typen `str`.
    * Kontrollera att anropskroppen har attributen `price`, som ska ha typen `float`.
    * Leta den valfria attributen `is_offer`, som bör ha typen `bool` om den finns.
    * Detta skulle också fungera för djupt nestlade JSON objekt.
* Konvertera från och till JSON automatiskt.
* Dokumentera allt enligt OpenAPI, så det kan användas för:
    * Interaktiva dokumentationssystem.
    * Automatiska kodgenereringssystem för klienter, för många olika språk.
* Erbjuda 2 web-gränssnitt för interaktiv dokumentation direkt.

---

Vi har bara skrapat på ytan men du förstår nog redan hur allt hänger ihop. 

Testa att byta ut raden med:

```Python
    return {"item_name": item.name, "item_id": item_id}
```

...från:

```Python
        ... "item_name": item.name ...
```

...till:

```Python
        ... "item_price": item.price ...
```

...och se hur din kodredigerare kommer autokomplettera attributerna och känna av dess typer:

![editor support](https://fastapi.tiangolo.com/img/vscode-completion.png)

För ett mer komplett exempel, som inkluderar fler funktionaliteter, se <a href="https://fastapi.tiangolo.com/tutorial/">Tutorial - Användarguide</a>

**Spoiler alert**: Tutorial - Användarguide innehåller:

* Deklarationer av **parametrar** från andra ställen såsom: **sidhuvuden** (headers), **kakor** (cookies), **formulärfält** och **filer**.
* Hur man skapar **valideringsregler** såsom `maximum_length` eller `regex`.
* Ett väldigt kraftfullt och enkelt **<abbr title="även känt som komponents, resurs, leverantörs, tjänst, injectables">Beroende-injections</abbr>**system.
* Säkerhet och autentisering, inklusive stöd för **OAuth2** med **JWT tokens** och **HTTP Basic** autentisering.
* Mer avancerade (men lika lätta) tekniker för att deklarera **djupt nestlade JSON modeller** (med hjälp av Pydantic).
* **GraphQL** integration med <a href="https://strawberry.rocks" class="external-link" target="_blank">Strawberry</a> och andra bibliotek.
* Ett flertal extra fnktionaliteter (med hjälp av Starlette), såsom: 
    * **WebSockets**.
    * Extremt enkla tester baserade på HTTPX och `pytest`.
    * **CORS**
    * **Kak-sessioner** (Cookie sessions)
    * ...och mer.

## Prestanda

Oberoende TechEmpower prestandamätningar visar att **FastAPI** applikationer som kör under Uvicorn är <a href="https://www.techempower.com/benchmarks/#section=test&runid=7464e520-0dc2-473d-bd34-dbdfd7e85911&hw=ph&test=query&l=zijzen-7" class="external-link" target="_blank">ett av de snabbaste python ramverken som finns</a>, endast slagna av Starlette och Uvicorn själva (som används internt av FastAPI). (*)

För att lära sig mer om detta, se ektionen <a href="https://fastapi.tiangolo.com/sv/benchmarks/" class="internal-link" target="_blank">Prestandamätningar</a>

## Beroenden

FastAPI är beroende av paketen Pydantic och Starlette.

### `standard` paketen

När du installerar FastAPI med `pip install "fastapi[standard]"`så medföljer `standard` gruppern av tillvalspaket:

Används av Pydantic:

* <a href="https://github.com/JoshData/python-email-validator" target="_blank"><code>email-validator</code></a> - för epost-validering.

Används av Starlette:

* <a href="https://www.python-httpx.org" target="_blank"><code>httpx</code></a> - Nödvändig om du vill använda testklienten `TestClient`.
* <a href="https://jinja.palletsprojects.com" target="_blank"><code>jinja2</code></a> - Nödvändig för att använda standard konfigurationsmallen.
* <a href="https://github.com/Kludex/python-multipart" target="_blank"><code>python-multipart</code></a> - Nödvändig om du vill ha stöd för formulär <abbr title="Konverterar strängen som kommer från ett HTTP anrop till Python data">"parsing"</abbr>, med `request.form()`.

Används av både FastAPI och Starlette:

* <a href="https://www.uvicorn.org" target="_blank"><code>uvicorn</code></a> - för servern som laddar och tillhandahåller din applikation. Detta inkluderar `uvicorn[standard]`, som i sin tur inkluderar paket (såsom `uvloop`) som behövs för att tillhandahålla applikationen på ett högpresterande sätt.
* `fastapi-cli` - för att möjliggöra `fastapi` kommandot.

### Utan `standard` paketen

Om du inte vill inkludera `standard` tillvalspaketen kan du installera FastAPI med `pip install fastapi` istället för `pip install "fastapi[standard]"`.

### Fler tilläggspaket 

Det finns fler tilläggspaket som du kan vara intresserad av.

Fler tilläggspaket för Pydantic:

* <a href="https://docs.pydantic.dev/latest/usage/pydantic_settings/" target="_blank"><code>pydantic-settings</code></a> - för hantering av inställningar.
* <a href="https://docs.pydantic.dev/latest/usage/types/extra_types/extra_types/" target="_blank"><code>pydantic-extra-types</code></a> - för extra typer att använda med Pydantic.

Fler tilläggspaket för FastAPI:

* <a href="https://github.com/ijl/orjson" target="_blank"><code>orjson</code></a> - Nödvändig om du vill använda `ORJSONResponse`.
* <a href="https://github.com/esnme/ultrajson" target="_blank"><code>ujson</code></a> - Nödvändig om du vill använda `UJSONResponse`.

## Licens

Detta projekt är licensierat i enlighet med villkoren i MIT licensen.
