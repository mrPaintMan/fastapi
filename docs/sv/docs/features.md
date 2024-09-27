# Funktioner

## FastAPI-funktioner

**FastAPI** ger dig följande:

### Baserat på öppna standarder

* <a href="https://github.com/OAI/OpenAPI-Specification" class="external-link" target="_blank"><strong>OpenAPI</strong></a> för API-skapande, inklusive deklarationer av <abbr title="även känd som: endpoints, routes">väg</abbr> <abbr title="även känd som HTTP-metoder, såsom POST, GET, PUT, DELETE">operationer</abbr>, parametrar, begärningskroppar, säkerhet, etc.
* Automatisk datamodell-dokumentation med <a href="https://json-schema.org/" class="external-link" target="_blank"><strong>JSON Schema</strong></a> (eftersom OpenAPI i sig själv är baserat på JSON Schema).
* Utformad kring dessa standarder, efter en noggrann studie. Istället för ett eftertänkt lager ovanpå.
* Detta möjliggör också automatisk **klientkodgenerering** på många språk.

### Automatiska dokument

Interaktiv API-dokumentation och utforskningswebbgränssnitt. Eftersom ramverket är baserat på OpenAPI, finns det flera alternatic, 2 är inkluderade som standard.

* <a href="https://github.com/swagger-api/swagger-ui" class="external-link" target="_blank"><strong>Swagger UI</strong></a>, med interaktiv utforskning, kalla och testa ditt API direkt från webbläsaren.

![Swagger UI interaction](https://fastapi.tiangolo.com/img/index/index-03-swagger-02.png)

* Alternativ API dokumentation med <a href="https://github.com/Rebilly/ReDoc" class="external-link" target="_blank"><strong>ReDoc</strong></a>.

![ReDoc](https://fastapi.tiangolo.com/img/index/index-06-redoc-02.png)

### Bara modern python

Allt är baserat på grundläggande **Python typ** deklarationer (tack vare Pydantic). Man behöver inte lära sig någon ny syntax. Bara vanlig modern Python.

Om du behöver en 2 minuters uppfriskare om hur man använder python typer (även om du inte använder FastAPI), titta på den korta handledningen: [Python Types](python-types.md){.internal-link target=_blank}.

Du skriver standard Python med typer:

```Python
from datetime import date

from pydantic import BaseModel

# Deklarera en variabel som en str
# och få editor stöd inom funktionen
def main(user_id: str):
    return user_id


# En Pydantic modell
class User(BaseModel):
    id: int
    name: str
    joined: date
```

Det kan sedan användas som:

```Python
my_user: User = User(id=3, name="John Doe", joined="2018-07-19")

second_user_data = {
    "id": 4,
    "name": "Mary",
    "joined": "2018-11-30",
}

my_second_user: User = User(**second_user_data)
```

/// info

`**second_user_data` betyder:

Skicka direkt nycklarna och värdena från `second_user_data` uppslagsverket(Python typen dict) som nyckel-värde-argument, motsvarande till: `User(id=4, name="Mary", joined="2018-11-30")`

///

### Redigerarstöd

Hela ramverket var utformat för att vara enkelt och intuitivt att använda, alla beslut testades på flera redigerare redan innan utvecklingen började, för att säkerställa den bästa utvecklarupplevelsen.

I enkäterna bland Python-utvecklare är det tydligt <a href="https://www.jetbrains.com/research/python-developers-survey-2017/#tools-and-features" class="external-link" target="_blank">att en av de mest använda funktionerna är "automatkomplettering"</a>.

Hela **FastAPI** ramverket är baserat på att uppfylla det. Autokomplettering ska fungera överallt.

Du kommer sällan behöva gå tillbaka och titta på dokumentationen.

Här är hur din editor möjligtvis kan hjälpa dig:

* in <a href="https://code.visualstudio.com/" class="external-link" target="_blank">Visual Studio Code</a>:

![editor support](https://fastapi.tiangolo.com/img/vscode-completion.png)

* in <a href="https://www.jetbrains.com/pycharm/" class="external-link" target="_blank">PyCharm</a>:

![editor support](https://fastapi.tiangolo.com/img/pycharm-completion.png)

Du kommer att få komplettering i din kod som du trodde var omäjlig innan. Till exempel, `price` nyckeln innan för en JSON kropp (som kan vara nästad) som kommer från ett anrop.

Du slipper att skriva fel nyckel namn, gå fram o tillbaka mellan dokumentation, eller scrolla upp o ner för att hitta att du till slut använde `username` eller `user_name`.

////////////////////////////////////////////////
Här är Filip

n dokument, eller scrolla upp och ner för att se om du äntligen använde `username` eller `user_name`.

### Kort

Det har rimliga **standardinställningar** för allt, med valfria konfigurationer överallt. Alla parametrar kan finjusteras för att göra det du behöver och för att definiera den API du behöver.

Men som standard, fungerar allt **"bara"**.

### Validering

* Validering för de flesta (eller alla?) Python **datatyper**, inklusive:
* JSON-objekt (`dict`).
* JSON-array (`list`) som definierar typ av objekt.
* Sträng (`str`) fält, som definierar minimi- och maxlängder.
* Tal (`int`, `float`) med minimi- och maxvärden, etc.

* Validering för mer exotiska typer, som:
* URL.
* E-post.
* UUID.
* ...och andra.

All validering hanteras av det väletablerade och robusta **Pydantic**.

### Säkerhet och autentisering

Säkerhet och autentisering integrerat. Utan några kompromisser med databaser eller datamodeller.

Alla säkerhetsscheman definierade i OpenAPI, inklusive:

* HTTP Basic.
* **OAuth2** (även med Here is the translated text to Swedish:

**Beroenden.**
* Stöd för komplexa användarautentiseringssystem, **databasanslutningar**, osv.
* **Inga kompromisser** med databaser, frontends, osv. Men enkel integration med alla av dem.

### Obegränsade "plug-ins"

Eller på ett annat sätt, inga behov av dem, importera och använd den kod du behöver.

All integration är utformad för att vara så enkel att använda (med beroenden) att du kan skapa en "plug-in" för din applikation på 2 kodrader med samma struktur och syntax som används för dina *vägoperationer*.

### Testad

* 100% <abbr title="Mängden kod som automatiskt testas">testtäckning</abbr>.
* 100% <abbr title="Python-typannoteringar, med detta kan din redigerare och externa verktyg ge dig bättre stöd">typannoterad</abbr> kodbas.
* Används i produktionsapplikationer.

## Starlette-funktioner

**FastAPI** är helt kompatibel med (och baserad på) <a href="https://www.starlette.io/" class="external-link" target="_blank"><strong>Starlette</strong></a>. Så, vilken ytterligare... Here is the translated text in Swedish:

de du har kommer också att fungera.

Inklusive externa bibliotek som också är baserade på Pydantic, såsom <abbr title="Object-Relational Mapper">ORM</abbr>:er, <abbr title="Object-Document Mapper">ODM</abbr>:er för databaser.

Detta betyder också att i många fall kan du skicka samma objekt du får från en begäran **direkt till databasen**, eftersom allt valideras automatiskt.

Detta gäller också åt andra hållet, i många fall kan du bara skicka objektet du får från databasen **direkt till klienten**.

Med **FastAPI** får du alla funktioner från **Pydantic** (eftersom FastAPI baseras på Pydantic för all datahantering):

* **Ingen hjärnknas**:
* Ingen ny mikrospråkdefinition för schema att lära sig.
* Om du känner till Python-typer vet du hur man använder Pydantic.
* Arbetar bra med din **<abbr title="Integrated Development Environment, similar to a code editor">IDE</abbr>/<abbr title="A program that checks for code errors">linter</abbr>/hjärna**:
* Eftersom pydantic datakonstruktioner helt enkelt är
