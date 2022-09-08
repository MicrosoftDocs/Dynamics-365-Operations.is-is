---
title: Opin API fyrir sýnileika birgða
description: Þessi grein lýsir opinberum API sem eru veitt af Birgðasýnileika.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 14812fc201ba1038a78ea3317686dbe189ffa687
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2022
ms.locfileid: "9423596"
---
# <a name="inventory-visibility-public-apis"></a>Opin API fyrir sýnileika birgða

[!include [banner](../includes/banner.md)]


Þessi grein lýsir opinberum API sem eru veitt af Birgðasýnileika.

Almennt REST API innbótar birgðasýnileikans kynnir ýmsar tilteknar endastöðvar samþættingar. Það styður fjórar aðalsamskiptaleiðir:

- Bókun á lagerbirgðum breytist í innbótina úr ytra kerfi
- Að setja upp eða hnekkja magni lagerbirgða í innbótinni úr ytra kerfi
- Að bóka frátekningartilvik í innbótina úr ytra kerfi
- Fyrirspurn um núverandi lagermagn úr ytra kerfi

Eftirfarandi tafla sýnir API sem eru í boði eins og er:

| Slóð | Aðferð | lýsing |
|---|---|---|
| /api/environment/{environmentId}/onhand | Bóka | [Stofna eitt tilvik lagerbreytinga](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Bóka | [Stofna mörg tilvik breytinga](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Bóka | [Stilla/hnekkja lagermagni](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Bóka | [Stofna eitt tilvik frátekningar](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Bóka | [Stofna mörg tilvik frátekningar](#create-multiple-reservation-events) |
| /api/umhverfi/{environmentId} /ábyrgð/afskilið | Bóka | [Snúa við einum pöntunarviðburði](#reverse-one-reservation-event) |
| /api/umhverfi/{environmentId} /onhand/unreserve/bulk | Bóka | [Snúa við mörgum pöntunarviðburðum](#reverse-multiple-reservation-events) |
| /api/umhverfi/{environmentId} /áhandar/breyta dagskrá | Bóka | [Búðu til eina áætlaða breytingu á hendi](inventory-visibility-available-to-promise.md) |
| /api/umhverfi/{environmentId} /áhandar/breyta áætlun/magn | Bóka | [Búðu til margar áætlaðar breytingar á hendi](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Bóka | [Senda fyrirspurn með bókunaraðferðinni](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | Sækja | [Senda fyrirspurn með aðferðinni sækja](#query-with-get-method) |
| /api/umhverfi/{environmentId} /úthlutun/úthluta | Bóka | [Búðu til einn úthlutunarviðburð](inventory-visibility-allocation.md#using-allocation-api) |
| /api/umhverfi/{environmentId} /úthlutun/afúthluta | Bóka | [Búðu til einn atburð sem ekki var úthlutað](inventory-visibility-allocation.md#using-allocation-api) |
| /api/umhverfi/{environmentId} /úthlutun/endurúthluta | Bóka | [Búðu til einn endurúthluta atburði](inventory-visibility-allocation.md#using-allocation-api) |
| /api/umhverfi/{environmentId} /úthlutun/neyta | Bóka | [Búðu til einn neysluviðburð](inventory-visibility-allocation.md#using-allocation-api) |
| /api/umhverfi/{environmentId} /úthlutun/fyrirspurn | Bóka | [Niðurstaða fyrirspurnaúthlutunar](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> {environmentId} hluti slóðarinnar er umhverfiskennið í Microsoft Dynamics Lifecycle Services (LCS).
> 
> Magn API getur skilað að hámarki 512 færslum fyrir hverja beiðni.

Microsoft hefur útvegað tilbúið beiðnasafn *Postman*. Þú getur flutt þetta safn inn í *Postman* hugbúnaðinn með því að nota eftirfarandi samnýttan tengil: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Finna endastöðin samkvæmt umhverfi Lifecycle Services

Örþjónusta birgðasýnileika er sett upp í Microsoft Azure Service Fabric, á mörgum staðsetningum og mörgum landsvæðum. Sem stendur er enginn miðlæg endastöð sem getur beint beiðni þinni sjálfkrafa á samsvarandi staðsetningu eða landsvæði. Þess vegna verður þú að setja saman upplýsingarnar í vefslóð með því að nota eftirfarandi mynstur:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Stutt heiti svæðisins er að finna í umhverfinu Microsoft Dynamics Lifecycle Services (LCS). Eftirfarandi tafla sýnir svæðin sem eru í boði eins og er.

| Azure-svæði        | Stutt heiti svæðis |
| ------------------- | ----------------- |
| Austur-Ástralía      | eau               |
| Suðaustur-Ástralía | seau              |
| Mið-Kanada      | cca               |
| Austur-Kanda         | eca               |
| Norður-Evrópa        | neu               |
| Vestur-Evrópa         | weu               |
| Austurhluti Bandaríkjanna             | eus               |
| Vesturhluti Bandaríkjanna             | wus               |
| Suðurhluti Bretlands            | suk               |
| Vesturhluti Bretlands             | wuk               |
| Austur-Japan          | ejp               |
| Vestur-Japan          | wjp               |
| Suður-Brasilía        | sbr               |
| Suður- og miðríki Bandaríkjanna    | scus              |

Númer eyjarinnar er þar sem LCS-umhverfið þitt er sett upp í Service Fabric. Það er engin leið til að fá þessar upplýsingar frá notendahliðinni.

Microsoft hefur skapað notandaviðmót í Power Apps svo þú getir fengið fullkláraða endastöð örþjónustunnar. Frekari upplýsingar er að finna í [Finna endastöð þjónustu](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Sannvottun

Öryggistákn verkvangsins er notað til að kalla á opið API birgðasýnileika. Þess vegna verður þú að búa til _Azure Active Directory (Azure AD) tákn_ með því að nota þitt Azure AD umsókn. Þá þarf að nota Azure AD táknið til að fá _aðgangsmerkið_ úr öryggisþjónustunni.

Microsoft útvegar tilbúið merkjasafn *Postman*. Þú getur flutt þetta safn inn í *Postman* hugbúnaðinn með því að nota eftirfarandi samnýttan tengil: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Til að ná í öryggistákn skal fylgja þessum skrefum.

1. Skráðu þig inn í Azure-gáttina og notaðu hana til að finna gildin `clientId` og `clientSecret` fyrir Dynamics 365 Supply Chain Management forritið þitt.
1. Sæktu Azure AD tákn (`aadToken`) með því að senda inn HTTP-beiðni sem er með eftirfarandi eiginleika:

   - **Vefslóð:**`https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
   - **Aðferð:** `GET`
   - **Meginefni (eyðublaðagögn):**

     | Lykill           | Virði                                            |
     | ------------- | -------------------------------------------------|
     | client_id     | ${aadAppId}                                      |
     | client_secret | ${aadAppSecret}                                  |
     | grant_type    | client_credentials                               |
     | umfang         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.sjálfgefið    |

   Þú ættir að fá Azure AD tákn (`aadToken`) sem svar. Niðurstaðan ætti að líkjast eftirfarandi dæmi.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "access_token": "eyJ0eX...8WQ"
   }
   ```

1. Settu saman JavaScript Object Notation (JSON) beiðni sem líkist eftirfarandi dæmi.

   ```json
   {
       "grant_type": "client_credentials",
       "client_assertion_type": "aad_app",
       "client_assertion": "{Your_AADToken}",
       "scope": "https://inventoryservice.operations365.dynamics.com/.default",
       "context": "{$LCS_environment_id}",
       "context_type": "finops-env"
   }
   ```

   Athugið eftirfarandi stig:

   - Gildið `client_assertion` verður að vera Azure AD táknið (`aadToken`) sem var móttekið í fyrra skrefi.
   - Gildið `context` verður að vera LCS-umhverfiskenni þar sem á að nota viðbótina.
   - Stilltu öll önnur gildi eins og sýnt er í dæminu.

1. Sæktu aðgangslykil (`access_token`) með því að senda inn HTTP-beiðni sem er með eftirfarandi eiginleika:

   - **VEFSLÓÐ:** `https://securityservice.operations365.dynamics.com/token`
   - **Aðferð:** `POST`
   - **HTTP-haus:** Hafðu með API-útgáfuna. (Lykillinn er `Api-Version` og gildið er `1.0`.)
   - **Meginefni efnis** - Nota skal JSON-beiðni sem var stofnuð í fyrra skrefi.

   Þú ættir að fá aðgangslykil (`access_token`) sem svar. Þú verður að nota þennan lykil sem handhafalykil til að kalla á API birgðasýnileika. Hér er dæmi.

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

> [!IMPORTANT]
> Þegar þú notar beiðasafnið *Postman* til að kalla á opið API birgðasýnileika þarftu að bæta við handhafalykli fyrir hverja beiðni. Til að finna handhafalykilinn skal velja flipann **Heimild** undir vefslóð beiðninnar, velja gerðina **Handhafalykill** og afrita aðgangslykilinn sem var sóttur í skrefinu á undan. Í síðari köflum þessarar greinar,`$access_token` verður notað til að tákna táknið sem var sótt í síðasta skrefi.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Stofna tilvik lagerbreytinga

Tvö API eru til staðar til að búa til tilvik lagerbreytinga:

- Stofna eina færslu: `/api/environment/{environmentId}/onhand`
- Stofna margar færslur: `/api/environment/{environmentId}/onhand/bulk`

Eftirfarandi tafla tekur saman merkingu hvers reits í meginmáli JSON.

| Kenni svæðis | Lýsing |
|---|---|
| `id` | Einkvæmt auðkenni fyrir tiltekið breytingartilvik. Ef endursending á sér stað vegna bilunar í þjónustu er þetta auðkenni notað til að tryggja að sami atburður verði ekki talinn tvisvar í kerfinu. |
| `organizationId` | Kennimerki fyrirtækisins sem er tengt við tilvikið. Þetta gildi er varpað í fyrirtæki eða auðkenni gagnasvæðis í Supply Chain Management. |
| `productId` | Kennimerki afurðarinnar. |
| `quantities` | Magnið sem lagerbirgðirnar þurfa að breytast um. Ef t.d. 10 nýjar bækur bætast í hilluna verður þetta gildi `quantities:{ shelf:{ received: 10 }}`. Ef þrjár bækur eru teknar úr hillunni eða seldar verður þetta gildi `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Gagnagjafi víddanna sem notaðar eru í tilviki og fyrirspurn bókunarbreytingar. Ef gagnagjafi er tilgreindur er hægt að nota sérstilltar víddir úr tilgreindum gagnagjafa. Birgðasýnileiki getur notað skilgreiningu víddar til að varpa sérstilltum víddum í almennar sjálfgefnar víddir. Ef ekkert `dimensionDataSource` gildi er tilgreint geturðu aðeins notað almennu [grunnvíddirnar](inventory-visibility-configuration.md#data-source-configuration-dimension) í fyrirspurnum þínum. |
| `dimensions` | Gagnvirkt par lyklagildis. Gildunum er varpað í sumar víddirnar í Supply Chain Management. Hins vegar getur þú einnig bætt við sérstilltum víddum (til dæmis _Uppruna_) til að gefa til kynna hvort tilvikið komi úr Supply Chain Management eða ytra kerfi. |

> [!NOTE]
> Færibreyturnar `siteId` og `locationId` setja saman [stillingu þáttunar](inventory-visibility-configuration.md#partition-configuration). Þú verður því að tilgreina þær í víddum þegar þú býrð til tilvik lagerbreytinga, stilla eða hnekkja lagermagni eða stofna frátekningartilvik.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Stofna eitt tilvik lagerbreytinga

Þetta API býr til eitt tilvik lagerbreytinga.

```txt
Path:
    /api/environment/{environmentId}/onhand
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
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

Eftirfarandi dæmi sýnir sýnishorn um efni meginmáls. Í þessu sýnishorni bókar þú tilvik breytingar fyrir afurðina *Bolur*. Þetta tilviki er úr sölustaðarkerfinu (POS) og viðskiptavinur hefur skilað rauðum stuttermabol aftur í verslunina. Þetta tilvik mun auka magn afurðarinnar *Bolur* um 1.

```json
{
    "id": "123456",
    "organizationId": "SCM_IV",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Eftirfarandi dæmi sýnir sýnishorn um efni meginmáls án `dimensionDataSource`. Í þessu tilfelli verður `dimensions` [grunnvíddir](inventory-visibility-configuration.md#data-source-configuration-dimension). Ef `dimensionDataSource` er stillt getur `dimensions` annaðhvort verið víddir gagnagjafa eða grunnvíddir.

```json
{
    "id": "123456",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Stofna mörg tilvik breytinga

Þetta API getur búið til margar færslur samtímis. Eini munurinn á þessu API og [API fyrir eitt tilvik](#create-one-onhand-change-event) eru gildin `Path` og `Body`. Fyrir þetta API gefur `Body` upp fylki af færslum. Hámarksfjöldi færslur er 512, sem þýðir að forritaskilin fyrir magnbreytingar geta stutt allt að 512 breytingartilvik í einu.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
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
        "id": "123456",
        "organizationId": "SCM_IV",
        "productId": "iv_postman_product_1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "posSiteId": "posSite1",
            "posLocationId": "posLocation1",
            "posMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "SCM_IV",
        "productId": "iv_postman_product_2",
        "dimensions": {
            "siteId": "iv_postman_site",
            "locationId": "iv_postman_location",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Stilla/hnekkja lagermagni

API fyrir _Stilla lagerbirgðir_ hnekkir núverandi gögnum fyrir tiltekna afurð.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

Eftirfarandi dæmi sýnir sýnishorn um efni meginmáls. Hegðun þessa API er frábrugðin hegðun API sem lýst er í [Búðu til breytingaviðburði á staðnum](#create-onhand-change-event) kafla fyrr í þessari grein. Í þessu sýnishorni mun magn afurðarinnar *Bolur* vera stillt á 1.

```json
[
    {
        "id": "123456",
        "organizationId": "SCM_IV",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "posSiteId": "iv_postman_site",
            "posLocationId": "iv_postman_location",
            "posMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Stofna tilvik frátekninga

Til að nota *Áskilið* API, þú verður að kveikja á pöntunareiginleikanum og ljúka við pöntunarstillinguna. Frekari upplýsingar er að finna í [Skilgreining frátekningar (valfrjálst)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Stofna eitt tilvik frátekningar

Hægt er að taka frá gagnvart mismunandi stillingum gagnagjafa. Til að stilla þessa gerð frátekningar skal fyst tilgreinga gagnagjafann í `dimensionDataSource` færibreytunni. Í `dimensions` færibreytunni skal síðan tilgreina víddir samkvæmt víddarstillingum í gagnagjafanum sem um ræðir.

Þegar þú kallar á API frátekningu er hægt að stjórna staðfestingu frátekningar með því að tilgreina Boolean `ifCheckAvailForReserv` færibreytu í meginmáli beiðninnar. Gildi `True` þýðir að staðfesting sé nauðsynleg og á móti merkir gildið `False` að staðfestingin er ekki nauðsynleg. Sjálfgefið gildi er `True`.

Ef þú vilt bakfæra frátekningu eða taka frá tiltekið birgðamagn skaltu stilla magnið á neikvætt gildi og stilla`ifCheckAvailForReserv` breytu til`False` að sleppa staðfestingunni. Það er líka sérstakt unreserve API til að gera slíkt hið sama. Munurinn er aðeins í því hvernig API-in tvö eru kölluð. Það er auðveldara að snúa við tilteknum pöntunarviðburði með því að nota`reservationId` með *fyrirvaralaus* API. Fyrir frekari upplýsingar, sjá [_Afpanta einn pöntunarviðburð_](#reverse-reservation-events) kafla.

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
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
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

Eftirfarandi dæmi sýnir sýnishorn um efni meginmáls.

```json
{
    "id": "reserve-0",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

Eftirfarandi dæmi sýnir árangursríkt svar.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Stofna mörg tilvik frátekningar

Þetta API er magnútgáfa af [API fyrir eitt tilvik](#create-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
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
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="reverse-reservation-events"></a>Snúið pöntunarviðburði

The *Áskilið* API þjónar sem andstæða aðgerð fyrir [*Fyrirvari*](#create-reservation-events) atburðir. Það veitir leið til að snúa við pöntunarviðburði sem tilgreint er af`reservationId` eða til að minnka pöntunarmagnið.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a> Snúa við einum pöntunarviðburði

Þegar fyrirvari er stofnaður, a`reservationId` verður innifalið í svarhlutanum. Þú verður að veita það sama`reservationId` að hætta við pöntunina og láta það sama fylgja með`organizationId` og`dimensions` notað fyrir pöntunar-API símtalið. Að lokum, tilgreinið`OffsetQty` gildi sem táknar fjölda hluta sem losa á frá fyrri fyrirvara. Fyrirvara getur annað hvort verið snúið við að fullu eða að hluta eftir því sem tilgreint er `OffsetQty`. Til dæmis, ef *100* einingar af hlutum voru fráteknar, þú getur tilgreint`OffsetQty: 10` að afskiptalaus *10* af upphaflegri áskilinni upphæð.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

Eftirfarandi kóði sýnir dæmi um líkamsefni.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

Eftirfarandi kóði sýnir dæmi um árangursríkan viðbragðsaðila.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Í svarhlutanum, hvenær`OffsetQty` er minna en eða jafnt og pöntunarmagnið,`processingStatus` mun vera "*árangur* "og`totalInvalidOffsetQtyByReservId` mun vera *0*.
>
> Ef`OffsetQty` er hærri en áskilin upphæð,`processingStatus` mun vera "*að hluta til velgengni* "og`totalInvalidOffsetQtyByReservId` verður munurinn á milli`OffsetQty` og áskilin upphæð.
>
>Til dæmis, ef pöntunin hefur magn af *10*, og`OffsetQty` hefur gildi á *12*,`totalInvalidOffsetQtyByReservId` væri *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a> Snúa við mörgum pöntunarviðburðum

Þetta API er magnútgáfa af [API fyrir eitt tilvik](#reverse-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Fyrirspurn um lagerbirgðir

Nota *Fyrirspurn við höndina* API til að sækja núverandi birgðagögn fyrir vörur þínar. API styður sem stendur fyrirspurnir um allt að 5000 einstaka hluti eftir`productID` gildi. Margfeldi`siteID` og`locationID` Einnig er hægt að tilgreina gildi í hverri fyrirspurn. Hámarksmörkin eru skilgreind með eftirfarandi jöfnu:

*NumOf(SiteID)\* NumOf(LocationID)<= 100*.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Senda fyrirspurn með bókunaraðferðinni

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

Í meginhluta þessarar beiðni er `dimensionDataSource` enn valfrjáls færibreyta. Ef hún er ekki stillt verður `filters` meðhöndlað sem *grunnvíddir*. Það eru fjórar áskildir reitir fyrir `filters`: `organizationId`, `productId`, `siteId` og `locationId`.

- `organizationId` ætti aðeins að innihalda eitt gildi, en það er samt fylki.
- `productId` gæti innihaldið eitt eða fleiri gildi. Ef það er tómt fylki verður öllum afurðum skilað.
- `siteId` og `locationId` eru notuð í þáttun í birgðasýnileika. Þú getur tilgreint fleiri en eitt `siteId` og `locationId` gildi í beiðni *Lagerfyrirspurnar*. Í núverandi útgáfu verður þú að tilgreina bæði `siteId` og `locationId` gildi.

Við mælum með að þú notir`groupByValues` færibreytu til að fylgja stillingum þínum fyrir flokkun. Frekari upplýsingar er að finna í [Skilgreining á stigveldi atriðaskráar](./inventory-visibility-configuration.md#index-configuration).

Færibreytan `returnNegative` stýrir því hvort niðurstöðurnar innihalda neikvæðar færslur.

> [!NOTE]
> Ef þú hefur virkjað breytingaáætlunina fyrir hendi og eiginleika sem hægt er að lofa (ATP), getur fyrirspurnin þín einnig innihaldið`QueryATP` Boolean færibreyta, sem stjórnar því hvort niðurstöður fyrirspurnar innihalda ATP upplýsingar. Fyrir frekari upplýsingar og dæmi, sjá [Birgðasýnileiki fyrirliggjandi breytingaráætlanir og hægt að lofa](inventory-visibility-available-to-promise.md).

Eftirfarandi dæmi sýnir sýnishorn um efni meginmáls.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "siteId": ["iv_postman_site"],
        "locationId": ["iv_postman_location"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Eftirfarandi dæmi sýnir hvernig á að spyrjast fyrir um allar vörur á tiltekinni síðu og staðsetningu.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "siteId": ["iv_postman_site"],
        "locationId": ["iv_postman_location"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Senda fyrirspurn með aðferðinni sækja

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

Hér er sýnishorn af fá vefslóð. Þessi beiðni um að sækja er nákvæmlega sú sama og bókunardæmið sem var sýnt hér á undan.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="available-to-promise"></a>ATP-afhendingarspá

Þú getur sett upp Birgðasýnileika til að gera þér kleift að skipuleggja framtíðar breytingar á hendi og reikna út ATP magn. ATP er magn vöru sem er tiltækt og hægt er að lofa viðskiptavinum á næsta tímabili. Notkun ATP útreiknings getur aukið getu þína til að uppfylla pöntunina til muna. Fyrir upplýsingar um hvernig á að virkja þennan eiginleika og hvernig á að hafa samskipti við birgðasýnileika í gegnum API þess eftir að eiginleikinn er virkjaður, sjá [Birgðasýnileiki fyrirliggjandi breytingaráætlanir og hægt að lofa](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Úthlutun

Úthlutunartengd API eru staðsett í [Úthlutun birgðasýnileika](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
