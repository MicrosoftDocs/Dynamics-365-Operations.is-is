---
title: Innbót birgðasýnileika
description: Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla innbót birgðasýnileika fyrir Dynamics 365 Supply Chain Management.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625066"
---
# <a name="inventory-visibility-add-in"></a>Innbót birgðasýnileika

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Innbót birgðasýnileika er sjálfstæð og einstaklega sveigjanleg örþjónusta sem býður upp á rakningu lagerbirgða í rauntíma og veitir þar af leiðandi alhliða yfirlit yfir sýnileika birgða.

Allar upplýsingar sem tengjast birgðum á lager eru fluttar út í þjónustuna í nánast rauntíma í gegnum SQL-samþættingu á lágu stigi. Ytri kerfi fá aðgang að þjónustunni í gegnum RESTful API til að spyrjast fyrir um lagerbirgðir á uppgefnum víddasamstæðum, sem fær þá lista yfir lausar lagerstöður.

Birgðasýnileiki er örþjónusta byggð á Common Data Service, sem þýðir að hægt er að stækka hana með því að smíða Power Apps og nota Power BI til að bjóða upp á sérsniðna virkni til að uppfylla kröfur fyrirtækisins. Einnig er hægt að uppfæra vísinn til að gera birgðafyrirspurnir.

Birgðasýnileiki býður upp á grunnstillingarvalkosti sem gerir því kleift að samþættast við mörg kerfi þriðja aðila. Hann styður staðlaða birgðavídd, sérsniðna stækkunarhæfni og staðlað, stillanlegt magn sem er reiknað út.

Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla innbót birgðasýnileika fyrir Dynamics 365 Supply Chain Management og hvernig á að nota forritunarviðmót þess (API).

## <a name="install-the-inventory-visibility-add-in"></a>Setja upp innbót birgðasýnileika

Setja þarf upp innbót birgðasýnileika með því að nota Microsoft Dynamics Lifecycle Services (LCS). LCS er samstarfsgátt sem býður upp á umhverfi ásamt safni af reglulega uppfærðum þjónustum sem hjálpa til við að stjórna líftíma forritsins fyrir Dynamics 365 Finance and Operations forritin þín.

Frekari upplýsingar er að finna í [Tilföng Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).

### <a name="prerequisites"></a>Forkröfur

Áður en þú setur upp innbót birgðasýnileika þarftu að gera eftirfarandi:

- Fá LCS-innleiðingarverk með að minnsta kosti einu virku umhverfi í notkun.
- Búa til beta-lykla fyrir tilboðin þín í LCS.
- Virkja beta-lykla fyrir tilboðin þín fyrir notendur þína í LCS.
- Hafa skal samband við vöruteymi birgðasýnileika hjá Microsoft og gefa upp umhverfiskenni þar sem á að nota innbót birgðasýnileika.

Ef einhverjar spurningar vakna um þessi skilyrði er hægt að hafa samband við vöruteymi birgðasýnileika.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Setja upp innbótina

Til að setja upp innbót birgðasýnileika skal gera eftirfarandi:

1. Skráðu þig inn í gátt [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Á heimasíðunni skal velja verkið þar sem umhverfið er í notkun.
1. Á verksíðunni skal velja umhverfið þar sem á að setja upp innbótina.
1. Á heimasíðu umhverfisins skal fletta niður á hlutann **Innbætur umhverfis**. Ef hlutinn er ekki sýnilegur skal ganga úr skugga um að unnið hafi verið úr beta-lyklum forkröfu.
1. Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
    ![Heimasíða umhverfis í LCS](media/inventory-visibility-environment.png "Heimasíða umhverfis í LCS")
1. Veldu tengilinn **Setja upp nýja innbót**. Listi yfir tiltækar innbætur opnast.
1. Veldu **Birgðaþjónustu** úr listanum. (Athugið að þetta kann nú að vera skráð sem **Innbót birgðasýnileika fyrir Dynamics 365 Supply Chain Management**.)
1. Sláðu inn gildi fyrir eftirfarandi reiti fyrir umhverfið þitt:

    - **AAD-forritskenni**
    - **AAD-leigjandakenni**

    ![Uppsetningarsíða innbótar](media/inventory-visibility-setup.png "Uppsetningarsíða innbótar")

1. Samþykktu skilmálana með því að velja gátreitinn **Skilmálar**.
1. Velja **Setja upp**. Staða innbótarinnar birtist sem **Er í uppsetningu**. Þegar henni er lokið skal uppfæra síðuna til að sjá stöðuna breytast í **Uppsett**.

### <a name="get-a-security-service-token"></a>Sækja merki öryggisþjónustu

Til að sækja merki öryggisþjónustu skal gera eftirfarandi:

1. Sæktu `aadToken` og kallaðu á endastöðina: https://securityservice.operations365.dynamics.com/token.
1. Skiptu út `client_assertion` í meginmálinu og settu inn `aadToken`.
1. Skiptu út samhengi meginmálsins fyrir umhverfið þar sem á að nota innbótina.
1. Skiptu út umfangi meginmálsins fyrir eftirfarandi:

    - Umfang fyrir MCK - „https://inventoryservice.operations365.dynamics.cn/.default“  
    (Hægt er að finna Azure Active Directory forritskennið og leigjandakennið fyrir MCK í `appsettings.mck.json`.)
    - Umfang fyrir PROD - „https://inventoryservice.operations365.dynamics.com/.default“  
    (Hægt er að finna Azure Active Directory forritskennið og leigjandakennið fyrir PROD í `appsettings.prod.json`.)

    Niðurstaðan ætti að líkjast eftirfarandi dæmi.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. Þú færð `access_token` í staðinn. Þetta er það sem þú þarft sem handhafalykill til að kalla í API birgðasýnileikans. Eftirfarandi er dæmi.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a>Fjarlægja innbótina

Til að fjarlægja innbótina skal velja **Fjarlægja**. Uppfærðu LCS og innbót birgðasýnileika verður fjarlægð. Fjarlægingarferlið fjarlægir innbótarskráninguna og ræsir einnig vinnslu til að hreinsa öll viðskiptagögn sem vistuð eru í þjónustunni.

## <a name="inventory-visibility-add-in-public-api"></a>Almennt API innbótar birgðasýnileika

Almennt REST API innbótar birgðasýnileikans kynnir ýmsar tilteknar endastöðvar samþættingar. Það styður þrjár aðalsamskiptaleiðir:

- Bókun á lager breytist í innbótina úr ytra kerfi.
- Fyrirspurn um núverandi lagermagn úr ytra kerfi.
- Sjálfvirk samstilling við lager Supply Chain Management.

Sjálfvirka samstillingin er ekki hluti af almennu API en er í staðinn meðhöndluð í bakgrunni fyrir umhverfi sem hafa virkjað innbót birgðasýnileika.

### <a name="authentication"></a>Sannvottun

Öryggismerki verkvangs er notað til að kalla á innbót birgðasýnileika, þannig að nauðsynlegt er að búa til Azure Active Directory merki með því að nota Azure Active Directory-forritið.

Frekari upplýsingar um hvernig á að sækja öryggismerkið er að finna í [Setja upp innbót birgðasýnileika](#install-add-in).

### <a name="configure-the-inventory-visibility-api"></a>Skilgreina API fyrir sýnileika birgða

Áður en þjónustan er notuð þarf að ljúka við skilgreiningarnar sem lýst er í eftirfarandi undirköflum. Skilgreiningin kann að vera mismunandi eftir því hverjar upplýsingar um umhverfið þitt eru. Hún inniheldur fyrst og fremst fjóra hluti:

- [Deildaskipting](#partitioning)
- [Víddarskilgreiningar](#dimension-configurations)
- [Lyklun](#indexing)
- [Sérsniðin mæling](#custom-measurement)

#### <a name="partitioning"></a>Deildaskipting

Skipting getur haft umtalsverð áhrif á afköst API fyrir sýnileika birgða. Það er góð hugmynd að skilgreina skema sem leyfir smá flokkun á gögnum en leyfir samtímis gagnlegar gagnafyrirspurnir.

`organizationId` (`dataAreaId` í Supply Chain Management) verður alltaf hluti af skiptingunni og birgðasýnileiki er sjálfgefið stilltur á skiptingu eftir víddum sem *Svæði + Staðsetning*. Þetta þýðir að alltaf þurfi að senda fyrirspurn á þjónustuna með þessum víddum sem skilgreindar eru í síunum.

> [!NOTE]
> *Svæði* og *Staðsetning* eru tvær almennar sjálfgefnar víddir í birgðasýnileika. Í Supply Chain Management eru þessar víddir kallaðar *Svæði* (`InventSiteId`) og *Vöruhús* (`InventLocationId`)

### <a name="dimension-configurations"></a>Víddarskilgreiningar

Sýnileiki birgða mun bjóða upp á lista yfir almennar sjálfgefnar víddir til að virkja samþættingu margra upprunakerfa.

Í eftirfarandi töflu er listi yfir birgðavíddir sem verða sjálfgefin víddarheiti í birgðasýnileika.

| Tegund víddar | Heiti víddar |
|---|---|
| Afurð | `ColorId` |
| Afurð | `SizeId` |
| Afurð | `StyleId` |
| Afurð | `ConfigId` |
| Rakning | `BatchId` |
| Rakning | `SerialId` |
| Staður | `LocationId` |
| Staður | `SiteId` |
| Birgðastaða | `StatusId` |
| Miðast við vöruhús | `WMSLocationId` |
| Miðast við vöruhús | `WMSPalletId` |
| Miðast við vöruhús | `LicensePlateId` |

> [!NOTE]
> Gerð víddar sem er skráð í fyrri töflu er aðeins til viðmiðunar. Ekki þarf að skilgreina gerð víddar í birgðasýnileika.

Ef sérstillt vídd er til staðar og þarf að flytjast yfir í sjálfgefið gildi þegar birgðasýnileiki notar hana, er hægt að skilgreina heiti **Sérsniðinnar víddar** í birgðasýnileika.

Ytri kerfi fá aðgang að sýnileika birgða í gegnum RESTful API sem bjóða upp á lagerupplýsingar um uppgefin víddarsett sem senda á fyrirspurn um. Fyrir samþættinguna, gerir birgðasýnileiki þér kleift að stilla *ytri gagnagjafa rásar* og upprunavíddina við *markvíddina* í birgðasýnileika.

Markvíddirnar ættu að vera eitt af eftirfarandi:

- Sjálfgefnar víddir í birgðasýnileika
- Sérsniðnar víddir

Tilgangurinn með víddarskilgreiningunni er sá að staðla samþættingu margra kerfa fyrir fyrirspurnina á víddum og bókunartilvikinu með víddum.

#### <a name="indexing"></a>Lyklun

Oftast verður fyrirspurn um birgðir ekki bara um hæsta stig „samtölunnar“, heldur viltu hugsanlega sjá niðurstöður teknar saman eftir birgðavíddum.

Sýnileiki birgða veitir sveigjanleika með því að gera þér kleift að setja upp vísa sem byggja á víddinni eða samsetningu víddanna.

> [!NOTE]
> Sem stendur er aðeins hægt að skilgreina vísa fyrir fimm að hámarki. Þú þarft að íhuga vandlega hvaða vídd eða víddarsamsetningu þú notar fyrir innleiðingu til að tryggja að hún uppfylli þarfir fyrirtækisins þíns. Til dæmis, ef ætlunin er að senda fyrirspurn um afurðir eins og hér segir:

- Spyrjast fyrir um samanlagðar afurðir á lager af víddunum *Litur* og *Stærð*.
- Í sumum tilfellum er bara ætlunin að spyrjast fyrir um afurðina í heild sinni.

Þú hefðir þá tvær vísanir sem eru skilgreindar á eftirfarandi hátt:

- `["ColorId", "SizeId"]`
- `[]`

Tómi hornklofinn mun safna saman eftir auðkenni afurðar innan skiptingar.

Vísunin skilgreinir hvernig hægt er að flokka niðurstöðurnar samkvæmt fyrirspurnarstillingunni `groupBy`. Í þessu tilfelli, ef þú skilgreinir ekki eitthvað `groupBy` gildi, færðu samtölur eftir `productid`. Annars, ef skilgreint er `groupBy` sem `groupBy=ColorId&groupBy=SizeId` færðu margar línur til baka, sem byggja á mismunandi samsetningu á lit og stærð í kerfinu.

Hægt er að setja skilyrði fyrirspurnar í meginmál beiðninnar.

Hér er dæmi um fyrirspurn um afurðina með lita- og stærðarsamsetningu.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>Sérsniðin mæling

Sjálfgefið mælingarmagn er tengt við Supply Chain Management, en þú gætir hinsvegar viljað hafa magn sem er gert úr samsetningu sjálfgefinna mælinga. Til að gera þetta er hægt að hafa skilgreiningu á sérsniðnu magni, sem verður bætt við úttak lagerfyrirspurnar.

Virknin gerir einfaldlega kleift að skilgreina safn mælinga sem verður bætt við og/eða safn mælinga sem verður dregið frá til að búa til sérsniðnu mælinguna.

Til dæmis með eftirfarandi fyrirspurnarskilyrði muntu skilgreina magn sérsniðinnar mælingar sem `MyCustomAvailableforReservation` sem tilheyrandi notkunarkerfi notar.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Notkunarkerfi | Reiknaðar mælingar | Gagnaveita | Umbreytir | Útreikningsgerð umbreytis |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | samlagning |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | samlagning |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Frádráttur |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | samlagning |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Frádráttur |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | samlagning |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | samlagning |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Frádráttur |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Frádráttur |

Þannig mun fyrirspurnin um sérsniðna magnmælingu skila eftirfarandi úttaki.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

`MyCustomAvailableforReservation` úttakið byggir á útreikningsstillingu í sérsniðnum mælingum sem:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Bókun lagerbreytinga

Nákvæm vefslóð sem tilvikið verður bókað á mun ráðast af landsvæði notanda. Hún verður á forminu:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Þegar hún er vottuð verður þessi vefslóð notuð ásamt HTTP `POST`-aðferðinni til að senda breytingatilvik lagers á þjónustuna.

Sérstakur haus er notaður til að eiga samskipti við Dynamics 365 þjónustuna í gegnum HTTP-beiðnir, þar sem umhverfiskennið er tilgreint fyrir tilvik Supply Chain Management sem gögnin eru tengd við. Dæmi:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Fyrirspurn um bókun lagerbreytinga, dæmi 1

Þetta dæmi sýnir aðstæður þar sem víddarskilgreining verður sett upp í Power Apps.

Notaðu eftirfarandi fyrirspurn til að skilgreina víddarvörpunina í Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Nú er hægt að tilgreina `dimensionDataSource` og nota sérsniðnar víddir í fyrirspurnum. Kerfið mun umbreyta sérsniðnum víddum í grunnvíddir.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Fyrirspurn um bókun lagerbreytinga, dæmi 2

Þetta dæmi sýnir aðstæður þar sem engar varpanir eru settar upp fyrir víddarskilgreininguna í Power Apps, þannig að bókunin ætti einnig að nota grunnvíddirnar. Allar víddir verða að vera grunnvíddir þegar reiturinn `dimensionDataSource` er núll, tómur eða með stafabil.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>Eiginleikar JSON-skjalareits

Reitirnir úr dæmum JSON-fyrirspurna sem boðið var upp á hér á undan eru með eiginleikana sem gefnir eru upp í eftirfarandi töflu.

| Kenni svæðis | lýsing |
|---|---|
| `id` | Einkvæmt auðkenni fyrir tiltekið breytingartilvik. Þetta auðkenni er notað til að tryggja að ef samskipti við þjónustuna klikka við bókun, myndi endursending á tilvikinu ekki leiða til þess að sama tilvikið yrði talið tvisvar í kerfinu. |
| `organizationId` | Kennimerki fyrirtækisins sem tengt er við tilvikið. Þetta varpar í fyrirtækiskenni eða gagnasvæðiskenni Supply Chain Management. |
| `productId` | Kennimerki afurðar sem um ræðir. |
| `quantity` | Magnið sem á lager þarf að breytast um. Ef til dæmis 10 nýjum beyglum var bætt við hilluna, þá væri þetta gildi 10. Ef 3 beyglur yrðu síðan teknar úr hillunni eða seldar, þá væri þetta gildi -3. |
| `dimensionDataSource` | Gagnagjafi víddanna sem notaðar eru í breytingartilviki og fyrirspurn bókunar. Ef gagnagjafi er tilgreindur er hægt að nota sérstilltar víddir úr tilgreindum gagnagjafa. Með víddaskilgreiningunni getur birgðasýnileiki varpað sérstilltu víddunum í almennu sjálfgefnu víddirnar. Ef `dimensionDataSource` er ekki tilgreint er aðeins hægt að nota almennar sjálfgefnar víddir í fyrirspurnunum.   |
| `dimensions` | Gagnvirkur poki af lykla-/gildispörum. Þetta mun varpa í sumar víddirnar í Supply Chain Management, en einnig er hægt að bæta við sérstilltum víddum (eins og *Uppruni*) sem kann að gefa til kynna ef tilvikið kom frá Supply Chain Management eða ytra kerfi. |

### <a name="querying-current-on-hand"></a>Spyrjast fyrir um núverandi lagerbirgðir

Endastöðin til að spyrjast fyrir um núverandi lagerbirgðir verður með svipaða vefslóð:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Send verður fyrirspurn á hana með HTTP `POST`-aðferðinni.

#### <a name="current-on-hand-query-example-1"></a>Núverandi lagerfyrirspurn, dæmi 1

Þetta dæmi sýnir aðstæður þar sem búið er að ljúka víddarskilgreiningunni í Power Apps.

Notaðu eftirfarandi fyrirspurn til að skilgreina víddarvörpunina í Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Nú er hægt að tilgreina `dimensionDataSource` og nota sérsniðnar víddir í fyrirspurnum. Kerfið mun umbreyta sérsniðnum víddum í grunnvíddir. Hægt er að tilgreina `DimensionDataSource` í `filters` og tilgreina sérsniðnar víddir bæði í `filters` og `groupByValues`. Kerfið mun umbreyta sérsniðnum víddum í grunnvíddir.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Núverandi lagerfyrirspurn, dæmi 2

Þetta dæmi sýnir aðstæður þar sem engar varpanir eru settar upp fyrir víddarskilgreininguna í Power Apps, þannig að bókunin ætti einnig að nota grunnvíddirnar. Allar víddir verða að vera grunnvíddir þegar reiturinn `dimensionDataSource`, undir `filters` er núll, tómur eða með stafabil.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Dæmi um niðurstöður

Fyrirspurnirnar sem sýndar voru í fyrra dæminu gætu skilað niðurstöðum sem þessari.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Athugið að magnreitirnir eru skipulagðir sem orðabók yfir mælingar og tengd gildi þeirra.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]