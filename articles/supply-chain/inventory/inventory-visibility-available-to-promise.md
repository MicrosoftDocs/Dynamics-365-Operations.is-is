---
title: Birgðasýnileiki fyrirliggjandi breytingaráætlanir og hægt að lofa
description: Þessi grein lýsir því hvernig á að tímasetja framtíðar breytingar á hendi og reikna út magn sem er tiltækt til að lofa (ATP).
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 4a0edeedfe42b43ef36c8ca091b01eef815f3632
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856194"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Birgðasýnileiki fyrirliggjandi breytingaráætlanir og hægt að lofa

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp *Skiptaáætlun fyrir hendi* eiginleiki til að skipuleggja breytingar á hendi í framtíðinni og reikna út magn sem hægt er að lofa (ATP). ATP er magn vöru sem er tiltækt og hægt er að lofa viðskiptavinum á næsta tímabili. Notkun þessa útreiknings getur aukið getu þína til að uppfylla pöntunina til muna.

Fyrir marga framleiðendur, smásala eða seljendur er það ekki nóg bara að vita hvað er til staðar. Þeir verða að hafa fullan sýnileika í framtíðinni. Þetta framtíðarframboð ætti að taka tillit til framtíðarframboðs, framtíðareftirspurnar og ATP.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a> Virkjaðu og settu upp eiginleikana

Áður en þú getur notað ATP verður þú að setja upp eina eða fleiri reiknaðar mælikvarða til að reikna út ATP magn. Þú verður líka að kveikja á eiginleikanum og stilla ATP stillingar í Microsoft Power Apps.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>Settu upp reiknaðar mælikvarða fyrir ATP magn

The *ATP reiknaður mælikvarði* er fyrirfram skilgreind útreiknuð mælikvarði sem venjulega er notaður til að finna það magn sem er í boði í dag. The *framboðs magn* er summan af stærðum fyrir þá líkamlegu mælikvarða sem hafa breytitegund af *viðbót*, og *eftirspurn eftir magni* er summan af stærðum fyrir þá líkamlegu mælikvarða sem hafa breytitegund af *frádráttur*.

Þú getur bætt við mörgum reiknuðum mælikvarða til að reikna út mörg ATP magn. Samt sem áður ætti heildarfjöldi aðgreindra líkamlegra mælikvarða yfir allar ATP-reiknaðar mælingar að vera færri en níu.

> [!IMPORTANT]
> Reiknaður mælikvarði er samsetning líkamlegra mælikvarða. Formúla hennar getur aðeins innihaldið líkamlegar mælingar án afrita, ekki reiknaðar mælikvarða.

Til dæmis setur þú upp eftirfarandi reiknaða mælikvarða:

**Fáanlegt á staðnum** = (*PhysicalInvent* + *Á hendi* + *Ótakmarkað* + *Gæðaskoðun* + *Á heimleið*) - (*ReservPhysical* + *SoftReservePhysical* + *Á útleið*)

Summan (*PhysicalInvent* + *Á hendi* + *Ótakmarkað* + *Gæðaskoðun* + *Á heimleið*) táknar framboð og summan (*ReservPhysical* + *SoftReservePhysical* + *Á útleið*) táknar eftirspurn. Þess vegna er hægt að skilja reiknaða mælikvarða á eftirfarandi hátt:

**Fáanlegt á staðnum** = *Framboð* –*Heimta*

Þú getur bætt við öðrum reiknuðum mælikvarða til að reikna út **Við höndina líkamlega** ATP magn.

**Við höndina líkamlega** = (*PhysicalInvent* + *Á hendi* + *Ótakmarkað* + *Gæðaskoðun* + *Á heimleið*) - (*Á útleið*)

Það eru átta aðskildar líkamlegar mælingar á þessum tveimur ATP reiknuðu mælikvarða: *PhysicalInvent*, *hendi*, *·*, *·*, *heimleið*, *·*, *·*, og *Á útleið*.

Fyrir frekari upplýsingar um reiknaðar mælikvarða, sjá [Reiknaðar ráðstafanir](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Kveiktu á eiginleikum breytingaáætlunar fyrir hendi og stilltu ATP stillingar

Fylgdu þessum skrefum til að kveikja á *Skiptaáætlun fyrir hendi* lögun í Power Apps og stilltu ATP stillingarnar.

1. Skrá inn Power Apps, og opnaðu Birgðasýnileika.
1. Opnaðu síðuna **Skilgreining**.
1. Á **Eiginleikastjórnun** flipann, kveiktu á *OnhandChangeSchedule* eiginleiki.
1. Veldu **ATP stilling** flipa.
1. Þegar þú spyrð um Birgðasýnileika mun það gefa niðurstöðu sem inniheldur hverja ATP reiknaða mælingu sem þú bætir við hér. Veldu **Bæta við** að bæta við nýjum reiknuðum mælikvarða fyrir ATP.
1. Stilltu eftirfarandi svæði:

    - **Uppruni gagna** – Veldu gagnagjafann sem tengist útreiknaðri mælingu.
    - **Reiknaður mælikvarði** – Veldu reiknaða mælikvarða sem tengist völdum gagnagjafa og sem þú vilt nota til að finna tiltækt magn sem er í boði.
    - **Dagskrá Tímabil** – Sláðu inn fjölda daga sem notendur geta skoðað og sent inn áætlaðar breytingar á hendi þegar valinn reiknaður mælikvarði er notaður. Notendur sem biðja um hlutabréfaupplýsingar munu fá birgðamagn, áætlaðar breytingar á hendi og ATP fyrir hvern dag á þessu tímabili, frá og með núverandi dagsetningu. Veldu heiltölu á milli 1 og 7.

    > [!IMPORTANT]
    > Áætlunartímabilið inniheldur núverandi dagsetningu. Þess vegna geta notendur tímasett breytingar á hendi til að eiga sér stað hvenær sem er frá núverandi dagsetningu (deginum þegar breytingin er send) til (áætlunartímabil - 1) daga í framtíðinni.

1. Veldu **Vista**.
1. Endurtaktu skref 5 til 7 þar til þú hefur bætt við öllum reiknuðum mælikvarða sem þú þarft fyrir ATP.
1. Þegar þú hefur lokið við að stilla allar nauðsynlegar stillingar skaltu velja **Uppfærðu stillingar**.

Fyrir frekari upplýsingar, sjá [Ljúktu við og uppfærðu stillingarnar](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Hvernig breytingaáætlunin og ATP útreikningar virka

An *breytingaáætlun fyrir hendi* setur fram væntanlegar dagsetningar og magn áætlaðra breytinga. Þú getur sent inn áætlun um breytingar á birgðum í Birgðasýnileika, að því tilskildu að dagsetningarnar séu innan þess tímabils sem skilgreint er af **Dagskrártímabil** stilling (sjá [Virkjaðu og settu upp eiginleikana](#setup) kafla). Notendur sem spyrjast fyrir um hlutabréfaupplýsingar munu fá á lager magn, áætlaðar breytingar á hendi og ATP fyrir hvern dag á því tímabili.

Áætlaðar breytingar eru upphaflega óskuldbundnar og hafa því ekki áhrif á raunverulegt magn þitt í kerfinu. Til að framfylgja breytingunum verður þú að leggja fram *breytingaviðburður á hendi*, sem uppfærir raunverulegt tiltækt magn á lager. Þú verður síðan að afturkalla áætlaða breytingu með því að senda inn breytingaáætlun fyrir hendi fyrir samsvarandi neikvætt magn.

Til dæmis leggur þú inn pöntun fyrir 10 hjól og býst við að þau berist á morgun. Þess vegna sendir þú inn breytingaáætlun sem hefur innleiðingarmagnið 10 og er dagsett fyrir morgundaginn. Þegar pöntunin berst daginn eftir bætir þú hjólunum við á lagerinn þinn. Þú verður síðan að skuldbinda breytinguna á kerfinu þínu til að uppfæra raunverulegt magn sem er í boði. Til að framfylgja breytingunni sendir þú inn breytingatilvik sem hefur 10 á heimleið. Þú afturkallar síðan áætlaða breytingu með því að senda inn breytingaáætlun fyrir hendi sem hefur magn á heimleið upp á -10.

Þegar þú spyrð um Birgðasýnileika fyrir magn á lager og ATP, skilar það eftirfarandi upplýsingum fyrir hvern dag á áætlunartímabilinu:

- **Dagsetning** – Dagsetningin sem niðurstaðan á við. Tímabelti er Coordinated Universal Time (UTC).
- **Á lager magn** – Raunverulegt magn á lager fyrir tilgreinda dagsetningu. Þessi útreikningur er gerður í samræmi við ATP reiknaða mælikvarða sem er stilltur fyrir Birgðasýnileika.
- **Áætlað framboð** – Samtala alls áætlaðs magns á heimleið sem hefur ekki orðið efnislega tiltækt til tafarlausrar neyslu eða sendingar frá tilgreindri dagsetningu.
- **Áætluð eftirspurn** – Samtala alls áætluðu magns á útleið sem hefur ekki verið neytt eða sent frá tilgreindri dagsetningu.
- **ATP magn** – Lágmarks áætluð birgðamagn sem er tiltækt frá tilgreindri dagsetningu til loka áætlunartímabilsins. Þetta magn inniheldur allar áætlaðar magnleiðréttingar. Það er hámarksmagnið sem hægt er að lofa á núverandi degi fyrir afhendingu eða neyslu þann dag.

Til dæmis, ef núverandi dagsetning er 1. febrúar 2022 og áætlunartímabilið er 7, geta notendur sent inn áætlaðar breytingar á hendi sem búist er við að eigi sér stað frá 1. febrúar til 7. febrúar 2022. Í þessu tilviki er ATP-magnið fyrir 3. febrúar, til dæmis, reiknað út frá birgðamagni fyrir þann dag og áætluðu magni frá 3. febrúar til 7. febrúar.

## <a name="example"></a>Dæmi

Eftirfarandi dæmi sýnir hvernig röð áætlaðra breytinga á magni hefur áhrif á magnið á lager og ATP sem Birgðasýnileiki tilkynnir. Það sýnir einnig hvernig á að framkvæma áætlunarbreytingar, hvernig breyting á áætlun hefur áhrif á niðurstöðurnar og hvað getur gerst ef þú framkvæmir ekki áætlaða breytingu.

Niðurstöðurnar í þessu dæmi sýna a *spáð fyrir hendi* gildi. Þetta gildi inniheldur allar áætlaðar uppfærslur til skýringar en er í raun ekki tilkynnt þegar þú spyrð um Birgðasýnileika.

1. Eftirfarandi stillingar eru stilltar fyrir kerfið þitt á **ATP stilling** síðu inn Power Apps:

    - **ATP reiknaður mælikvarði** – Þú ert með útreiknaðan mælikvarða sem er nefndur *Á hendi*. Það er reiknað sem *Á hendi = Framboð – Eftirspurn*. Þú velur þann mælikvarða hér.
    - **Dagskrártímabil** - Þú velur *7*.

1. Eftirfarandi skilyrði gilda einnig:

    - Núverandi dagsetning er 1. febrúar 2022.
    - Núverandi magn á lager er 20.

1. Fyrir núverandi dagsetningu (1. febrúar 2022) sendir þú inn áætlað eftirspurnarmagn upp á 3 til Birgðasýnileika. Þess vegna er áætlað magn á lager 17. Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætlað fyrir hendi | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | | | 17 | 17 |
    | 2022-02-04 | 20 | | | 17 | 17 |
    | 2022-02-05 | 20 | | | 17 | 17 |
    | 2022-02-06 | 20 | | | 17 | 17 |
    | 2022-02-07 | 20 | | | 17 | 17 |

1. Á núverandi dagsetningu (1. febrúar 2022) leggur þú fram áætlað framboðsmagn upp á 10 fyrir 3. febrúar 2022. Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætlað fyrir hendi | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | 10 | | 27 | 27 |
    | 2022-02-04 | 20 | | | 27 | 27 |
    | 2022-02-05 | 20 | | | 27 | 27 |
    | 2022-02-06 | 20 | | | 27 | 27 |
    | 2022-02-07 | 20 | | | 27 | 27 |

1. Á núverandi dagsetningu (1. febrúar 2022) sendir þú inn eftirfarandi áætlaðar magnbreytingar:

    - Krafa um 15 magn fyrir 4. febrúar 2022
    - Framboðsmagn 1 fyrir 5. febrúar 2022
    - Framboðsmagn 3 fyrir 6. febrúar 2022

    Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætlað fyrir hendi | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 12 |
    | 2022-02-02 | 20 | | | 17 | 12 |
    | 2022-02-03 | 20 | 10 | | 27 | 12 |
    | 2022-02-04 | 20 | | sept | 12 | 12 |
    | 2022-02-05 | 20 | 1 | | 13 | 13 |
    | 2022-02-06 | 20 | 3 | | 16 | 16 |
    | 2022-02-07 | 20 | | | 16 | 16 |

1. Á núverandi dagsetningu (1. febrúar 2022) sendir þú áætlað eftirspurnarmagn 3. Þess vegna verður þú að framkvæma þessa breytingu þannig að hún endurspeglast í raunverulegu magni þínu. Til að framfylgja breytingunni, sendir þú inn breytingatilvik sem hefur útgöngumagnið 3. Þú afturkallar síðan áætlaða breytingu með því að senda inn breytingaáætlun fyrir hendi sem hefur útgangsmagn upp á -3. Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætlað fyrir hendi | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 17 | | 0 | 17 | 12 |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | sept | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |

1. Daginn eftir (2. febrúar 2022) færist áætlunartímabilið fram um einn dag. Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætlað fyrir hendi | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | sept | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |
    | 2022-02-08 | 17 | | | 16 | 16 |

1. Hins vegar, tveimur dögum síðar (4. febrúar 2022), er framboðsmagnið 10 sem átti að vera 3. febrúar enn ekki komið. Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætlað fyrir hendi | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-04 | 17 | | sept | 2 | 2 |
    | 2022-02-05 | 17 | 1 | | 3 | 3 |
    | 2022-02-06 | 17 | 3 | | 6 | 6 |
    | 2022-02-07 | 17 | | | 6 | 6 |
    | 2022-02-08 | 17 | | | 6 | 6 |
    | 2022-02-09 | 17 | | | 6 | 6 |
    | 2022-02-10 | 17 | | | 6 | 6 |

    Eins og þú sérð, hafa áætlaðar (en ekki skuldbundnar) breytingar á á lager ekki áhrif á raunverulegt magn á lager.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a> Sendu breytingaráætlanir, breyttu atburði og ATP fyrirspurnir í gegnum API

Þú getur notað eftirfarandi forritunarviðmót (API) vefslóðir til að senda inn tímabundnar breytingaráætlanir, breyta atburðum og fyrirspurnum.

| Slóð | Aðferð | Lýsing |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | Búðu til eina áætlaða breytingu á hendi. |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | Búðu til margar áætlaðar breytingar á hendi. |
| `/api/environment/{environmentId}/onhand` | `POST` | Búðu til einn breytingaviðburð fyrir hendi. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Búðu til marga breytingaviðburði. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | Fyrirspurn með því að nota`POST` aðferð. |
| `/api/environment/{environmentId}/onhand` | `GET` | Fyrirspurn með því að nota`GET` aðferð. |

Fyrir frekari upplýsingar, sjá [Birgðasýnileiki opinber API](inventory-visibility-api.md).

### <a name="create-one-on-hand-change-schedule"></a>Búðu til eina breytingaáætlun fyrir hendi

Stundabreytingaáætlun er búin til með því að senda inn a`POST` beiðni til viðeigandi vefslóð birgðasýnileikaþjónustu (sjá [Sendu breytingaráætlanir, breyttu atburði og ATP fyrirspurnir í gegnum API](#api-urls) kafla). Þú getur líka sent inn magnbeiðnir.

Aðeins er hægt að búa til breytingaáætlun fyrir hendi ef áætluð dagsetning er á milli núverandi dagsetningar og loka núverandi áætlunartímabils. Datetime sniðið ætti að vera *ár-mánaðar-dagur* (til dæmis, **2022-02-01**). Tímasniðið verður að vera nákvæmt aðeins til dags.

Þetta API býr til eina breytingaáætlun fyrir hendi.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

Eftirfarandi dæmi sýnir sýnishorn um efni meginmáls án `dimensionDataSource`.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>Búðu til margar breytingaáætlanir fyrir hendi

Þetta API getur búið til margar færslur samtímis. Eini munurinn á þessu API og API fyrir einn viðburð er`Path` og`Body` gildi. Fyrir þetta API gefur `Body` upp fylki af færslum. Hámarksfjöldi skráa er 512. Þess vegna getur forritaskilin fyrir magnbreytingaáætlun stutt allt að 512 áætlaðar breytingar í einu.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
                },
            },
        },
        ...
    ]
```

Eftirfarandi dæmi sýnir sýnishorn um efni meginmáls.

```json
[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>Stofna tilvik lagerbreytinga

Viðburðir fyrir staðbreytingar eru gerðar með því að senda inn a`POST` beiðni til viðeigandi vefslóð birgðasýnileikaþjónustu (sjá [Sendu breytingaráætlanir, breyttu atburði og ATP fyrirspurnir í gegnum API](#api-urls) kafla). Þú getur líka sent inn magnbeiðnir.

> [!NOTE]
> Breytingar við hendina eru ekki einstakar fyrir ATP virkni en eru hluti af venjulegu Inventory Visibility API. Þetta dæmi hefur verið tekið með vegna þess að atburðir skipta máli þegar þú vinnur með ATP. Viðburðir breytinga á staðnum líkjast pöntunum fyrir breytinga á hendi, en viðburðarskilaboð verða að vera send á aðra API vefslóð og viðburðir nota`quantities` í staðinn fyrir`quantityByDate` í meginmáli skilaboðanna. Fyrir frekari upplýsingar um breytingatilvik og aðra eiginleika birgðasýnileika API, sjá [Birgðasýnileiki opinber API](inventory-visibility-api.md#create-one-onhand-change-event).

Eftirfarandi dæmi sýnir meginmál beiðninnar sem inniheldur einn breytingatburð á hendi.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Spurðu fyrirhugaðar breytingar á hendi og ATP niðurstöður

Þú getur spurt um tímabundnar breytingar og ATP niðurstöður með því að senda annað hvort a`POST` beiðni eða a`GET` beiðni á viðeigandi API vefslóð (sjá [Sendu breytingaráætlanir, breyttu atburði og ATP fyrirspurnir í gegnum API](#api-urls) kafla).

Í beiðni þinni skaltu stilla`QueryATP` til *satt* ef þú vilt spyrjast fyrir um tímabundnar breytingar og ATP niðurstöður.

- Ef þú ert að senda inn beiðnina með því að nota`GET` aðferð, stilltu þessa færibreytu í vefslóðinni.
- Ef þú ert að senda inn beiðnina með því að nota`POST` aðferð, stilltu þessa færibreytu í meginmáli beiðninnar.

> [!NOTE]
> Burtséð frá því hvort`returnNegative` færibreyta er stillt á *satt* eða *rangt* í meginmáli beiðninnar mun niðurstaðan innihalda neikvæð gildi þegar þú biður um áætlaðar breytingar á hendi og ATP niðurstöður. Þessi neikvæðu gildi verða tekin með vegna þess að ef aðeins eftirspurnarpantanir eru áætlaðar, eða ef framboðsmagn er minna en eftirspurnarmagn, verður áætlað magn breytinga á lager neikvæð. Ef neikvæð gildi væru ekki tekin með væru niðurstöðurnar ruglingslegar. Fyrir frekari upplýsingar um þennan valkost og hvernig hann virkar fyrir aðrar tegundir fyrirspurna, sjá [Birgðasýnileiki opinber API](inventory-visibility-api.md#query-with-post-method).

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Eftirfarandi dæmi sýnir hvernig á að búa til beiðni meginmál sem hægt er að senda til Birgðasýnileika með því að nota`POST` aðferð.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "siteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="get-method-example"></a>GET aðferð dæmi

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

Eftirfarandi dæmi sýnir hvernig á að búa til vefslóð beiðni sem a`GET` beiðni.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Niðurstaðan af þessu`GET` beiðni er nákvæmlega sú sama og niðurstaðan af`POST` beiðni í fyrra dæmi.

### <a name="query-result-example"></a>Dæmi um niðurstöður fyrirspurnar

Bæði fyrri fyrirspurnadæmin gætu gefið eftirfarandi svar. Fyrir þetta dæmi er kerfið stillt með eftirfarandi stillingum:

- **ATP reiknaður mælikvarði:** *iv.onhand = pos.inbound – pos.outbound*
- **Dagskrártímabil:** *7*

Hér er dæmi um svarhlutann.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
