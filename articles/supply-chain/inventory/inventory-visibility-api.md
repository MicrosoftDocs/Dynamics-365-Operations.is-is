---
title: Opin API fyrir sýnileika birgða
description: Þetta efnisatriði útskýrir opin API sem birgðasýnileiki býður upp á.
author: yufeihuang
ms.date: 09/30/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 43fa94118c4d76e021bb635d720208d5f971db19
ms.sourcegitcommit: 49f29aaa553eb105ddd5d9b42529f15b8e64007e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2021
ms.locfileid: "7592489"
---
# <a name="inventory-visibility-public-apis"></a>Opin API fyrir sýnileika birgða

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Þetta efnisatriði útskýrir opin API sem birgðasýnileiki býður upp á.

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
| /api/environment/{environmentId}/onhand/indexquery | Sækja | [Senda fyrirspurn með bókunaraðferðinni](#query-with-post-method) |
| /api/environment/{environmentId}/onhand/indexquery | Bóka | [Senda fyrirspurn með aðferðinni sækja](#query-with-get-method) |

Microsoft hefur útvegað tilbúið beiðnasafn *Postman*. Þú getur flutt þetta safn inn í *Postman* hugbúnaðinn með því að nota eftirfarandi samnýttan tengil: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

> [!NOTE]
> {environmentId} hluti slóðarinnar er umhverfiskennið í Microsoft Dynamics Lifecycle Services (LCS).

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

Númer eyjarinnar er þar sem LCS-umhverfið þitt er sett upp í Service Fabric. Sem stendur er engin leið til að fá þessar upplýsingar notandamegin.

Microsoft hefur skapað notandaviðmót í Power Apps svo þú getir fengið fullkláraða endastöð örþjónustunnar. Frekari upplýsingar er að finna í [Finna endastöð þjónustu](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Sannvottun

Öryggistákn verkvangsins er notað til að kalla á opið API birgðasýnileika. Þess vegna þarf að búa til _Azure Active Directory (Azure AD) tákn_ með því að nota Azure AD-forritið. Þá þarf að nota Azure AD táknið til að fá _aðgangsmerkið_ úr öryggisþjónustunni.

Microsoft útvegar tilbúið merkjasafn *Postman*. Þú getur flutt þetta safn inn í *Postman* hugbúnaðinn með því að nota eftirfarandi samnýttan tengil: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Til að ná í öryggistákn skal fylgja þessum skrefum.

1. Skráðu þig inn í Azure-gáttina og notaðu hana til að finna gildin `clientId` og `clientSecret` fyrir Dynamics 365 Supply Chain Management forritið þitt.
1. Sæktu Azure AD tákn (`aadToken`) með því að senda inn HTTP-beiðni sem er með eftirfarandi eiginleika:

   - **VEFSLÓÐ:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **Aðferð:** `GET`
   - **Meginefni (eyðublaðagögn):**

     | Lykill           | Virði                                |
     | ------------- | ------------------------------------ |
     | client_id     | ${aadAppId}                          |
     | client_secret | ${aadAppSecret}                      |
     | grant_type    | client_credentials                   |
     | tilföng      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

   Þú ættir að fá Azure AD tákn (`aadToken`) sem svar. Niðurstaðan ætti að líkjast eftirfarandi dæmi.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "expires_on": "1610466645",
       "not_before": "1610462745",
       "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
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
       "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
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

   Þú ættir að fá aðgangslykil (`access_token`) sem svar. Þú verður að nota þennan lykil sem handhafalykil til að kalla á API birgðasýnileika. Eftirfarandi er dæmi.

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

> [!IMPORTANT]
> Þegar þú notar beiðasafnið *Postman* til að kalla á opið API birgðasýnileika þarftu að bæta við handhafalykli fyrir hverja beiðni. Til að finna handhafalykilinn skal velja flipann **Heimild** undir vefslóð beiðninnar, velja gerðina **Handhafalykill** og afrita aðgangslykilinn sem var sóttur í skrefinu á undan. Í síðari hlutum í þessum efnisatriði verður `$access_token` notað til að tákna lykilinn sem var sóttur í síðasta skrefi.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Stofna tilvik lagerbreytinga

Tvö API eru til staðar til að búa til tilvik lagerbreytinga:

- Stofna eina færslu: `/api/environment/{environmentId}/onhand`
- Stofna margar færslur: `/api/environment/{environmentId}/onhand/bulk`

Eftirfarandi tafla tekur saman merkingu hvers reits í meginmáli JSON.

| Kenni svæðis | lýsing |
|---|---|
| `id` | Einkvæmt auðkenni fyrir tiltekið breytingartilvik. Þetta auðkenni er notað til að tryggja að ef samskipti við þjónustuna klikka við bókun verður sama tilvikið ekki talið tvisvar sinnum í kerfinu ef það er sent inn á nýjan leik. |
| `organizationId` | Kennimerki fyrirtækisins sem er tengt við tilvikið. Þetta gildi er varpað í fyrirtæki eða auðkenni gagnasvæðis í Supply Chain Management. |
| `productId` | Kennimerki afurðarinnar. |
| `quantities` | Magnið sem lagerbirgðirnar þurfa að breytast um. Ef t.d. 10 nýjar bækur bætast í hilluna verður þetta gildi `quantities:{ shelf:{ received: 10 }}`. Ef þrjár bækur eru teknar úr hillunni eða seldar verður þetta gildi `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Gagnagjafi víddanna sem notaðar eru í tilviki og fyrirspurn bókunarbreytingar. Ef gagnagjafi er tilgreindur er hægt að nota sérstilltar víddir úr tilgreindum gagnagjafa. Birgðasýnileiki getur notað skilgreiningu víddar til að varpa sérstilltum víddum í almennar sjálfgefnar víddir. Ef ekkert `dimensionDataSource` gildi er tilgreint geturðu aðeins notað almennu [grunnvíddirnar](inventory-visibility-configuration.md#data-source-configuration-dimension) í fyrirspurnum þínum. |
| `dimensions` | Gagnvirkt par lyklagildis. Gildunum er varpað í sumar víddirnar í Supply Chain Management. Hins vegar getur þú einnig bætt við sérstilltum víddum (til dæmis _Uppruna_) til að gefa til kynna hvort tilvikið komi úr Supply Chain Management eða ytra kerfi. |

> [!NOTE]
> Færibreyturnar `SiteId` og `LocationId` setja saman [stillingu þáttunar](inventory-visibility-configuration.md#partition-configuration). Þú verður því að tilgreina þær í víddum þegar þú býrð til tilvik lagerbreytinga, stilla eða hnekkja lagermagni eða stofna frátekningartilvik.

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId": "Red"
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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Stofna mörg tilvik breytinga

Þetta API getur búið til margar færslur samtímis. Eini munurinn á þessu API og [API fyrir eitt tilvik](#create-one-onhand-change-event) eru gildin `Path` og `Body`. Fyrir þetta API gefur `Body` upp fylki af færslum.

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
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
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

Eftirfarandi dæmi sýnir sýnishorn um efni meginmáls. Hegðun þessa API er frábrugðin hegðun API sem lýst er í hlutanum [Stofna tilvik lagerbreytinga](#create-onhand-change-event) fyrr í þessu efnisatriði. Í þessu sýnishorni mun magn afurðarinnar *Bolur* vera stillt á 1.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId": "0001"
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

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Til að API *Frátekningar* þarftu að opna eiginleika frátekningar og ljúka við skilgreiningu frátekningar. Frekari upplýsingar er að finna í [Skilgreining frátekningar (valfrjálst)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Stofna eitt tilvik frátekningar

Hægt er að taka frá gagnvart mismunandi stillingum gagnagjafa. Til að stilla þessa gerð frátekningar skal fyst tilgreinga gagnagjafann í `dimensionDataSource` færibreytunni. Í `dimensions` færibreytunni skal síðan tilgreina víddir samkvæmt víddarstillingum í gagnagjafanum sem um ræðir.

Þegar þú kallar á API frátekningu er hægt að stjórna staðfestingu frátekningar með því að tilgreina Boolean `ifCheckAvailForReserv` færibreytu í meginmáli beiðninnar. Gildi `True` þýðir að staðfesting sé nauðsynleg og á móti merkir gildið `False` að staðfestingin er ekki nauðsynleg. Sjálfgefið gildi er `True`.

Ef þú vilt hætta við frátekningu eða afturkalla frátekningu á tilgreindu birgðamagni skaltu stilla magnið á neikvætt gildi og stilla `ifCheckAvailForReserv` færibreytuna á `False` til að sleppa villuleitinni.

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Stofna mörg tilvik frátekningar

Þetta API er magnútgáfa af [API fyrir eitt tilvik](#create-one-reservation-event).

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

## <a name="query-on-hand"></a>Fyrirspurn um lagerbirgðir

API fyrir _Fyrirspurn um lagerbirgðir_ er notað til að sækja núverandi gögn um lagerbirgðir fyrir afurðirnar þínar.

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

- `organizationId` ætti að innihalda aðeins eitt gildi en það er samt enn fylki.
- `productId` getur innihaldið eitt eða fleiri gildi. Ef það er tómt fylki verður öllum afurðum skilað.
- `siteId` og `locationId` eru notuð í þáttun í birgðasýnileika. Þú getur tilgreint fleiri en eitt `siteId` og `locationId` gildi í beiðni *Lagerfyrirspurnar*. Í núverandi útgáfu verður þú að tilgreina bæði `siteId` og `locationId` gildi.

Færibreytan `groupByValues` ætti að fylgja stillingu þinni fyrir atriðaskráningu. Frekari upplýsingar er að finna í [Skilgreining á stigveldi atriðaskráar](./inventory-visibility-configuration.md#index-configuration).

Færibreytan `returnNegative` stýrir því hvort niðurstöðurnar innihalda neikvæðar færslur.

Eftirfarandi dæmi sýnir sýnishorn um efni meginmáls.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

Eftirfarandi dæmi sýna hvernig á að spyrjast fyrir um allar afurðir á tilteknu svæði og staðsetningu.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Senda fyrirspurn með aðferðinni sækja

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
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

Hér er sýnishorn af sækja-vefslóð. Þessi beiðni um að sækja er nákvæmlega sú sama og bókunardæmið sem var sýnt hér á undan.

```txt
/api/environment/{environmentId}/onhand/indexquery?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
