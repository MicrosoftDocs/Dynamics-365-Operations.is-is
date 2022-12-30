---
title: Breytingaáætlun á lager og ATP-afhendingarspá Inventory Visibility
description: Þessi grein lýsir því hvernig á að áætla framtíðar breytingar á lager og reikna út tiltækt-til-loforðs magn (ATP).
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
ms.openlocfilehash: f831c5d5719bbbd72c7cff37b8b35826f48ce6e4
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719292"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Breytingaáætlun á lager og ATP-afhendingarspá Inventory Visibility

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp eiginleikann *Breytingaráætlun á lager* til að áætla framtíðar breytingar á lager og reikna út tiltækt-til-loforðs magn (ATP). ATP (tiltækt-til-loforðs) er magn vöru sem er tiltækur og hægt er að lofa viðskiptavini á næsta tímabili. Notkun þessa útreiknings getur aukið til muna uppfyllingargetu pöntunar.

Fyrir marga framleiðendur, smásala eða söluaðila eða seljendur er ekki nóg að vita bara hvað er á lager núna. Þeir verða að hafa fullan sýnileika yfir tiltækileika í framtíðinni. Þetta framtíðarframboð ætti að taka tillit til framboðs, eftirspurnar og ATP í framtíðinni.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>Virkja og setja upp eiginleika

Áður en hægt er að nota ATP þarf að setja upp eina eða fleiri reiknaðar mælingar til að reikna út magn ATP. Þú verður einnig að kveikja á eiginleikanum og stilla ATP stillingar í Microsoft Power Apps.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>Setja upp reiknaðar mælingar fyrir ATP-magn

*ATP reiknuð mæling* er fyrirfram skilgreind reiknuð mæling sem er yfirleitt notuð til að finna magn á lager sem er tiltækt núna. *Birgðamagn* er samtala magns fyrir þær efnislegu ráðstafanir sem hafa breytingalykil *viðbótar* og *eftirspurnarmagn* er samtala magns fyrir þær efnislegu ráðstafanir sem hafa breytingalykil *frádrátt*.

Þú getur bætt við mörgum reiknuðum mælingum til að reikna út ólíkt magn ATP. Hins vegar ætti heildarfjöldi mismunandi efnislegra ráðstafana á öllum ATP reiknuðum ráðstöfunum að vera minni en níu.

> [!IMPORTANT]
> Reiknuð mæling er samsetning efnislegra mælinga. Formúla þess getur aðeins falið í sér efnislegar mælieiningar án tvítekninga, ekki reiknaðar mælingar.

Til dæmis er hægt að setja upp eftirfarandi reiknuð mæling:

**Tiltækt á lager** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*ReservPhysical* + *SoftReservePhysical* + *Outbound*)

Summan (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) táknar framboð og summan (*ReservPhysical* + *SoftReservePhysical* + *Outbound*) táknar eftirspurn. Því er hægt að skilja reiknaða mælingu á eftirfarandi hátt:

**Tiltækt á lager** = *Framboð* – *Eftirspurn*

Þú getur bætt við annarri reiknaðri mælingu til að reikna út **efnislegt ATP-magn á lager**.

**Á lager-efnislegt** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*Outbound*)

Reiknað er með átta mismunandi efnislegum ráðstafanir á þessum tveimur ATP mælingum: *PhysicalInvent*, *OnHand*, *Unrestricted*, *QualityInspection*, *Inbound*, *ReservPhysical*, *SoftReservePhysical*, og *Outbound*.

Frekari upplýsingar um reiknaðar mælingar eru í [Reiknaðar mælingar](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Kveiktu á eiginleikanum Breytingaáætlun á lager og stilltu ATP stillingar

Fylgdu eftirfarandi skrefum til að kveikja á eiginleikanum *Breytingaáætlun á lager* í Power Apps og stilltu ATP stillingar.

1. Skráðu þig inn á Power Apps og opnaðu sýnileika birgða.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Eiginleikastjórnun** skal kveikja á eiginleikanum *OnhandChangeSchedule*.
1. Velja flipann **ATP-stilling**.
1. Þegar þú leggur fyrirspurn fyrir Inventory Visibility mun það veita niðurstöðu sem inniheldur hverja ATP reiknaða mælingu sem þú bætir við hér. Veldu **Bæta við** til að bæta við nýrri reiknaðri mælingu við ATP.
1. Stilltu eftirfarandi svæði:

    - **Gagnauppspretta** – Veljið gagnauppsprettuna sem tengist reiknaðri mælingu.
    - **Reiknuð mæling** – Veldu reiknaða mælingu sem er tengdur við valda gagnagjafa og sem á að nota til að finna tiltækt magn á lager.
    - **Áætla tímabil** – Sláðu inn fjölda daga sem notendur geta skoðað og sent inn áætlaðar breytingar á lager þegar valin reiknuð mæling er notuð. Notendur sem biðja um upplýsingar um birgðir fá magn á lager, áætlaðar breytingar á lager og ATP fyrir hvern dag á því tímabili sem hefjast á núverandi degi. Veldu heiltala á bilinu 1 til 7.

    > [!IMPORTANT]
    > Áætlunartímabilið inniheldur núverandi dagsetningu. Því geta notendur skipulagt breytingar á lager hvenær sem er frá núverandi (deginum sem breytingin er send inn) í gegnum (áætlunartímabil – 1) daga fram í tímann.

1. Veldu **Vista**.
1. Endurtakið skref 5 til 7 þar til öllum reiknaðar mælingar sem þarf fyrir ATP hefur verið bætt við.
1. Þegar þú hefur lokið við að stilla allar nauðsynlegar stillingar skaltu velja **Uppfæra stillingu**.

Frekari upplýsingar eru í [Ljúka við og uppfæra skilgreininguna](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Hvernig breytingaráætlun á lager og ATP útreikninga virka

*Breytingaráætlun á lager* ákvarðar áætlaðar dagsetningar og magn breytinga á lager. Hægt er að senda breytingaráætlun á lager til Inventory Visibility, að því tilskildu að dagsetningarnar séu innan tímabilsins sem skilgreint er í stillingunum **Áætlunartímabil** (sjá hlutann [Virkja og setja upp eiginleika](#setup)). Notendur sem biðja um upplýsingar um birgðir fá magn á lager, áætlaðar breytingar á lager og ATP fyrir hvern dag á því tímabili.

Áætlaðar breytingar eru í upphafi ósamþykktar og hafa því ekki áhrif á raunverulegt magn á lager í kerfinu. Til að staðfesta breytingar þarftu að senda inn *breytingartilvik á lager* sem uppfærir raunverulegt magn sem er í boði á lager. Þú verður að breyta áætlaðri breytingu aftur með því að senda inn breytingaráætlun á lager fyrir samsvarandi neikvætt magn.

Til dæmis er hægt að panta 10 reiðhjól og reikna með að það komi á morgun. Þess vegna getur þú sent inn breytingaráætlun um lagerbirgðir sem hefur magnið 10 og er dagsett fyrir morgundaginn. Þegar pöntunin berst næsta dag bætir þú reiðhjólunum við efnislegar lagerbirgðir. Þú verður þá að framkvæma breytingu á kerfinu þínu til að uppfæra raunverulegar lagerbirgðir. Til að gera breytinguna sendir þú inn breytingartilvik á lager sem hefur magn á innleið sem nemur 10. Þú afturkallar síðan áætlaða breytingu með því að senda inn breytingaráætlun á lager sem hefur innflutt magn -10.

Þegar þú sendir fyrirspurn til Inventory Visibility fyrir magn á lager og ATP-magn, skilar það eftirfarandi upplýsingum fyrir hvern dag á áætlunartímabilinu:

- **Dagsetning** – Dagsetning þegar niðurstaðan á við. Tímabeltið er Samræmdur heimstími (UTC).
- **Lagerbirgðir** – Raunverulegar lagerbirgðir fyrir tilgreinda dagsetningu. Þessi útreikningur er gerður í samræmi við ATP útreiknaðan mælikvarða sem er stilltur fyrir Inventory Visibility.
- **Áætlað framboð** – Samtala allra áætlaðra magns á innleið sem ekki er orðið efnislega tiltækt til notkunar strax eða senda frá og með tilgreindum degi.
- **Áætluð eftirspurn** – Summa alls áætlaðs magns á útleið sem ekki hefur verið notað eða sent frá og með tilgreindri dagsetningu.
- **ATP magn** – Lágmarks áætlað magn á lager sem er tiltækt frá tilgreindum degi til loka áætlunartímabilsins. Þetta magn inniheldur allar áætlaðar magnleiðréttingar. Það er hámarksmagnið sem hægt er að lofa á þeim degi sem afhending eða notkun á sér stað þann daginn.

Ef núverandi dagsetning er t.d. 1. febrúar 2022 og áætlað tímabil er 7. geta notendur sent inn áætlaðar breytingar á lager sem gert er ráð fyrir að verði frá 1. febrúar til og með 7. febrúar 2022. Í þessu tilviki er ATP-magnið fyrir t.d. 3. febrúar reiknað út frá magni á lager þann dag og áætluðu magni frá 3. febrúar til og með 7. febrúar.

## <a name="example"></a>Dæmi

Eftirfarandi dæmi sýnir hvernig röð breytinga á áætluðu magni hefur áhrif á magn á lager og ATP sem Inventory Visibility greinir frá. Hún sýnir einnig hvernig á að gera áætlaða breytingu, hvaða áhrif staðfest breyting hefur á niðurstöðurnar og hvað getur átt sér stað ef þú gerir ekki áætlaða breytingu.

Niðurstöðurnar í þessu dæmi sýna *áætlað gildi á lager*. Þetta gildi felur í sér allar áætlaðar uppfærslur til skýringar en er í raun ekki tilkynnt þegar þú sendir fyrirspurn til Inventory Visibility.

1. Eftirfarandi stillingar eru stilltar fyrir kerfið þitt á síðunni **ATP-stillingar** á Power Apps:

    - **ATP reiknuð mæling** – Þú ert með reiknaða mælingu sem er nefndur *Á lager*. Það er reiknað sem *Á lager = Framboð – Eftirspurn*. Þú velur mælieininguna hér.
    - **Áætlunartímabil** – Þú velur *7*.

1. Eftirfarandi skilyrði gilda einnig:

    - Núverandi dagsetning er 1. febrúar 2022.
    - Núverandi magn á lager er 20.

1. Fyrir núverandi dagsetningu (1. febrúar 2022) sendir þú áætlað magn eftirspurnar upp á 3 til Inventory Visibility. Þess vega er áætlað magn á lager 17. Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætluð lagerstaða | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 02-01-2022 | 20 | | 3 | 17 | 17 |
    | 02-02-2022 | 20 | | | 17 | 17 |
    | 02-03-2022 | 20 | | | 17 | 17 |
    | 02-04-2022 | 20 | | | 17 | 17 |
    | 02-05-2022 | 20 | | | 17 | 17 |
    | 02-06-2022 | 20 | | | 17 | 17 |
    | 02-07-2022 | 20 | | | 17 | 17 |

1. Á núverandi degi (1. febrúar 2022) leggur þú fram áætlaðan birgðamagn upp á 10 fyrir 3. febrúar 2022. Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætluð lagerstaða | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 02-01-2022 | 20 | | 3 | 17 | 17 |
    | 02-02-2022 | 20 | | | 17 | 17 |
    | 02-03-2022 | 20 | 10 | | 27 | 27 |
    | 02-04-2022 | 20 | | | 27 | 27 |
    | 02-05-2022 | 20 | | | 27 | 27 |
    | 02-06-2022 | 20 | | | 27 | 27 |
    | 02-07-2022 | 20 | | | 27 | 27 |

1. Á núverandi dagsetningu (1. febrúar 2022) sendir þú inn eftirfarandi breytingar á áætluðu magni:

    - Eftirspurnarmagn 15 fyrir 4. febrúar 2022
    - Framboðsmagn 1 fyrir 5. febrúar 2022
    - Framboðsmagn 3 fyrir 6. febrúar 2022

    Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætluð lagerstaða | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 02-01-2022 | 20 | | 3 | 17 | 12 |
    | 02-02-2022 | 20 | | | 17 | 12 |
    | 02-03-2022 | 20 | 10 | | 27 | 12 |
    | 02-04-2022 | 20 | | sept | 12 | 12 |
    | 02-05-2022 | 20 | 1 | | 13 | 13 |
    | 02-06-2022 | 20 | 3 | | 16 | 16 |
    | 02-07-2022 | 20 | | | 16 | 16 |

1. Á núverandi degi (1. febrúar 2022) sendir þú áætlað magn eftirspurnar 3. Þess vegna verður þú að skuldbinda þig til að gera þessa breytingu þannig að hún endurspeglist í raunverulegu magni lagerbirgða. Til að gera breytinguna sendir þú inn breytingartilvik á lager sem hefur magn á útleið sem nemur 3. Þú afturkallar síðan áætlaða breytingu með því að senda inn breytingaráætlun á lager sem hefur útflutt magn -3. Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætluð lagerstaða | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 02-01-2022 | 17 | | 0 | 17 | 12 |
    | 02-02-2022 | 17 | | | 17 | 12 |
    | 02-03-2022 | 17 | 10 | | 27 | 12 |
    | 02-04-2022 | 17 | | sept | 12 | 12 |
    | 02-05-2022 | 17 | 1 | | 13 | 13 |
    | 02-06-2022 | 17 | 3 | | 16 | 16 |
    | 02-07-2022 | 17 | | | 16 | 16 |

1. Næsta dag (2. febrúar 2022) færist áætlunartímabilið fram um einn dag. Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætluð lagerstaða | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 02-02-2022 | 17 | | | 17 | 12 |
    | 02-03-2022 | 17 | 10 | | 27 | 12 |
    | 02-04-2022 | 17 | | sept | 12 | 12 |
    | 02-05-2022 | 17 | 1 | | 13 | 13 |
    | 02-06-2022 | 17 | 3 | | 16 | 16 |
    | 02-07-2022 | 17 | | | 16 | 16 |
    | 02-08-2022 | 17 | | | 16 | 16 |

1. Tveimur dögum síðar (4. febrúar 2022) hefur framboðsmagnið af 10 sem áætlað var að yrði 3. febrúar hins vegar enn ekki borist. Eftirfarandi tafla sýnir niðurstöðuna.

    | Dagsetning | Á lager | Áætlað framboð | Áætluð eftirspurn | Áætluð lagerstaða | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 02-04-2022 | 17 | | sept | 2 | 2 |
    | 02-05-2022 | 17 | 1 | | 3 | 3 |
    | 02-06-2022 | 17 | 3 | | 6 | 6 |
    | 02-07-2022 | 17 | | | 6 | 6 |
    | 02-08-2022 | 17 | | | 6 | 6 |
    | 02-09-2022 | 17 | | | 6 | 6 |
    | 02-10-2022 | 17 | | | 6 | 6 |

    Eins og sjá má hafa áætlaðar (en ekki skuldbundnar) breytingar á lagerbirgðum ekki áhrif raunverulegt magn lagerbirgða.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>Senda inn breytingaráætlun, breyta tilvikum og ATP fyrirspurnir í gegnum API

Hægt er að nota eftirfarandi forritaskil (API) til að senda inn vefslóðir til að senda inn breytingaráætlanir á lager, breyta tilvikum og fyrirspurnum.

| Slóð | Aðferð | Lýsing |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | Stofna eina áætlaða lagerbreytingu. |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | Stofna margar áætlaðar lagerbreytingar. |
| `/api/environment/{environmentId}/onhand` | `POST` | Stofna eitt tilvik lagerbreytinga. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Stofna mörg tilvik breytinga. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | Senda fyrirspurn með `POST`-aðferðinni. |
| `/api/environment/{environmentId}/onhand` | `GET` | Senda fyrirspurn með `GET`-aðferðinni. |
| `/api/environment/{environmentId}/onhand/exactquery` | `POST` | Nákvæm fyrirspurn með `POST`-aðferðinni. |

Frekari upplýsingar eru í [Opin API fyrir sýnileika birgða](inventory-visibility-api.md).

### <a name="create-one-on-hand-change-schedule"></a>Stofna breytingaráætlun á lager

Breytingaráætlun á lager er stofnuð með því að senda `POST` beiðni á vefslóð þjónustu Inventory Visibility (sjá hlutann [Senda inn breytingaráætlun, breyta tilvikum og ATP fyrirspurnir í gegnum API](#api-urls)). Einnig er hægt að senda inn magnbeiðnir.

Aðeins er hægt að búa til breytta áætlun á lager ef áætluð dagsetning er frá núverandi dagsetningu til loka yfirstandandi áætlunar. Snið dagsetningar og tíma á að vera *ár-mánuður-dagur* (til dæmis **2022-02-01**). Tímasniðið verður aðeins að vera nákvæmt til dagsins í dag.

Þetta API býr til eina breytingaráætlun á lager.

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

### <a name="create-multiple-on-hand-change-schedules"></a>Stofna margar áætlanir lagerbreytinga

Þetta API getur búið til margar færslur samtímis. Eini munurinn á þessu API og API fyrir eitt tilvik eru gildin `Path` og `Body`. Fyrir þetta API gefur `Body` upp fylki af færslum. Hámarksfjöldi skráa í hverri runu er 512. Því getur breytingaráætlun á lager fyrir magnútgáfu API stutt allt að 512 áætlaðar breytingar í einu.

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

Breytingartilvik á lager er stofnuð með því að senda `POST` beiðni á vefslóð þjónustu Inventory Visibility (sjá hlutann [Senda inn breytingaráætlun, breyta tilvikum og ATP fyrirspurnir í gegnum API](#api-urls)). Einnig er hægt að senda inn magnbeiðnir.

> [!NOTE]
> Breytingatilvik á lager eru ekki einkvæmir fyrir eiginleika ATP en eru hluti af hinu hefðbundna API Inventory Visibility. Þetta dæmi hefur verið tekið með vegna þess að tilvik skipta máli þegar unnið er með ATP. Breytingatilvik á lager líkjast bókunum á lager en skilaboð tilvika verða að vera send á annað vefslóð API og tilvik eru notaðir í `quantities` staðinn `quantityByDate` í meginmáli skilaboðanna. Frekari upplýsingar um breytingartilvik og aðra eiginleika Inventory Visibility API, er að finna í [Opin API fyrir Inventory Visibility](inventory-visibility-api.md#create-one-onhand-change-event).

Eftirfarandi dæmi sýnir meginmál beiðni sem inniheldur eitt breytingartilvik á lager.

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

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Senda fyrirspurn um breytingar á lager og ATP niðurstöður

Þú getur lagt fram fyrirspurn um breytingaráætlun á lager og ATP niðurstöður með því að senda annað hvort `POST` beiðni eða `GET` beiðni á viðeigandi vefslóð þjónustu Inventory Visibility (sjá hlutann [Senda inn breytingaráætlun, breyta tilvikum og ATP fyrirspurnir í gegnum API](#api-urls)).

Í beiðni þinni, stilltu `QueryATP` á *rétt* ef þú vilt spyrja um áætlaðar breytingar á lager og ATP niðurstöður.

- Ef þú ert að senda beiðnina með því að nota `GET` aðferðina skaltu setja þessa færibreytu í vefslóðina.
- Ef þú ert að senda beiðnina með því að nota `POST` aðferðina skaltu setja þessa færibreytu í meginmáli beiðni.

> [!NOTE]
> Óháð því hvort `returnNegative` færibreytan er stillt á *rétt* eða *rangt* í meginmáli beiðninnar, mun niðurstaðan innihalda neikvæð gildi þegar þú spyrð um áætlaðar breytingar á lager og ATP niðurstöður. Þessi neikvæðu gildi verða tekin með vegna þess að ef aðeins eftirspurnarpöntun er áætluð, eða ef framboðsmagn er minna en eftirspurnarmagn, verður áætluð breyting á lager neikvæð. Ef neikvæð gildi væru ekki tekin með væru niðurstöðurnar ruglingslegar. Frekari upplýsingar um þennan valkost og hvernig hann virkar fyrir aðrar tegundir af fyrirspurnum eru í [Opin API fyrir Inventory Visibility](inventory-visibility-api.md#query-with-post-method).

### <a name="query-by-using-the-post-method"></a>Senda fyrirspurn með POST-aðferðinni

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

Eftirfarandi dæmi sýnir hvernig hægt er að búa til meginmál fyrirspurn um yfirlit sem hægt er að senda inn í Inventory Visibility með því að nota `POST` aðferðina.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "SiteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="query-by-using-the-get-method"></a>Senda fyrirspurn með GET-aðferðinni

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

Eftirfarandi dæmi sýnir hvernig á að búa til vefslóð fyrir fyrirspurn um yfirlit sem `GET` beiðni.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Niðurstaða þessarar `GET` beiðni er nákvæmlega sú sama og niðurstaða `POST` beiðninnar í fyrra dæminu.

### <a name="exact-query-by-using-the-post-method"></a>Nákvæm fyrirspurn með POST-aðferðinni

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
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
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Eftirfarandi dæmi sýnir hvernig hægt er að búa til nákvæmt meginmál fyrirspurnar sem hægt er að senda inn í Inventory Visibility með því að nota `POST` aðferðina.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "dimensions": ["SiteId", "LocationId"],
        "values": [
            ["1", "11"]
        ]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="query-result-example"></a>Dæmi um niðurstöðu fyrirspurnar

Hvert og eitt af dæmum um fyrirspurn hér á undan gæti leitt til eftirfarandi svars. Þetta kerfi er til dæmis stillt með eftirfarandi stillingum:

- **ATP reiknuð mæling:** *iv.onhand = pos.inbound – pos.outbound*
- **Áætla tímabil:** *7*

Hér er dæmi um meginmál svarsins.

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
