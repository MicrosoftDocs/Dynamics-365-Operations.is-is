---
title: Innbót birgðasýnileika
description: Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla innbót birgðasýnileika fyrir Dynamics 365 Supply Chain Management.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574223"
---
# <a name="inventory-visibility-add-in"></a>Innbót birgðasýnileika

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Innbót birgðasýnileika er sjálfstæð og einstaklega sveigjanleg örþjónusta sem býður upp á rakningu lagerbirgða í rauntíma og veitir þar af leiðandi alhliða yfirlit yfir sýnileika birgða.

Allar upplýsingar sem tengjast birgðum á lager eru fluttar út í þjónustuna í nánast rauntíma í gegnum SQL-samþættingu á lágu stigi. Ytri kerfi fá aðgang að þjónustunni í gegnum RESTful API til að spyrjast fyrir um lagerbirgðir á uppgefnum víddasamstæðum, sem fær þá lista yfir lausar lagerstöður.

Birgðasýnileiki er örþjónusta byggð á Microsoft Dataverse, sem þýðir að hægt er að stækka hana með því að smíða Power Apps og nota Power BI til að bjóða upp á sérsniðna virkni til að uppfylla kröfur fyrirtækisins. Einnig er hægt að uppfæra vísinn til að gera birgðafyrirspurnir.

Birgðasýnileiki býður upp á grunnstillingarvalkosti sem gerir því kleift að samþættast við mörg kerfi þriðja aðila. Hann styður staðlaða birgðavídd, sérsniðna stækkunarhæfni og staðlað, stillanlegt magn sem er reiknað út.

Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla innbót birgðasýnileika fyrir Dynamics 365 Supply Chain Management og hvernig á að nota forritunarviðmót þess (API).

## <a name="install-the-inventory-visibility-add-in"></a>Setja upp innbót birgðasýnileika

Setja þarf upp innbót birgðasýnileika með því að nota Microsoft Dynamics Lifecycle Services (LCS). LCS er samstarfsgátt sem býður upp á umhverfi ásamt safni af reglulega uppfærðum þjónustum sem hjálpa til við að stjórna líftíma forritsins fyrir Dynamics 365 Finance and Operations forritin þín.

Frekari upplýsingar er að finna í [Tilföng Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).

### <a name="prerequisites"></a>Forkröfur

Áður en þú setur upp innbót birgðasýnileika þarftu að gera eftirfarandi:

- Fá LCS-innleiðingarverk með að minnsta kosti einu virku umhverfi í notkun.
- Gangið úr skugga um að skilyrðum fyrir uppsetningu innbóta sem gefnar eru upp í [Yfirliti innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) sé lokið. Sýnileiki birgða krefst ekki tengingu tvöföldrar skráningar.
- Hafa skal samskipti við teymi birgðasýnileika á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) til að fá eftirfarandi þrjár áskildar skrár:

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - `Inventory Visibility Integration.zip` (ef útgáfan af Supply Chain Management sem er keyrð er eldri en útgáfa 10.0.18)

> [!NOTE]
> Ríkin sem eru studd eins og er eru Kanada, Bandaríkin og Evrópusambandið (ESB).

Ef einhverjar spurningar vakna um þessi skilyrði er hægt að hafa samband við vöruteymi birgðasýnileika.

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Setja upp Dataverse

Fylgdu þessum skrefum til að setja upp Dataverse.

1. Bætið þjónustureglu við leigjandann:

    1. Setjið upp Azure AD PowerShell-einingu v2 eins og lýst er í [Setja upp Azure Active Directory PowerShell fyrir graf](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).
    1. Keyra eftirfarandi PowerShell-skipun.

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. Stofnið forritsnotanda fyrir birgðarsýnileika í Dataverse:

    1. Opnið vefslóð Dataverse umhverfisins.
    1. Farið í **Ítarleg stilling \> Kerfi \> Öryggi \> Notendur** og stofnið notanda forrits. Notið yfirlitsvalmyndina til að breyta síðuyfirlitinu í **Notendur forritsins**.
    1. Veljið **Nýtt**. Stilla forritskenni á *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*. (Auðkenni hlutar verður sjálfkrafa hlaðið þegar breytingarnar eru vistaðar.) Hægt er að sérstilla nafnið. Til dæmis er hægt að breyta því í *Birgðasýnileiki*. Þegar þessu er lokið skal velja **Vista**.
    1. Veljið **Úthluta hlutverki** og veljið því næst **Kerfisstjóri**. Ef til er hlutverk sem heitir **Common Data Service Notandi** skal líka velja það.

    Frekari upplýsingar eru í [Stofna notanda forrits](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

1. Flytjið inn `Inventory Visibility Dataverse Solution.zip` skrána sem inniheldur Dataverse skilgreiningar tengdra eininga og Power Apps:

    1. Opnið síðuna **Lausnir**.
    1. Velja **Innflutningur**.

1. Flytjið inn flæði fyrir ræsingu skilgreiningaruppfærslu:

    1. Opna Microsoft Flow síðuna.
    1. Gangið úr skugga um að tengingin sem heitir *Dataverse (eldra efni)* sé til. (Ef það er ekki til skal stofna það.)
    1. Flytja inn `Inventory Visibility Configuration Trigger.zip`-skrá. Þegar hún hefur verið flutt inn birtist ræsihnappurinn undir **Mín verkflæði**.
    1. Frumstilla eftirfarandi fjórar breytur út frá umhverfisupplýsingum:

        - Azure AD-leigjandakenni
        - Biðlarakenni Azure-forritsins
        - Leynilykill biðlara Azure-forritsins
        - Endastöð sýnileika birgða

            Frekari upplýsingar um þessa breytu er að finna í hlutanum [Setja upp samþættingu fyrir Sýnileika birgða](#setup-inventory-visibility-integration) seinna í þessu efnisatriði.

        ![Ræsing skilgreiningar](media/configuration-trigger.png "Ræsing skilgreiningar")

    1. Veljið **Kveikja á**.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Setja upp innbótina

Til að setja upp innbót birgðasýnileika skal gera eftirfarandi:

1. Skráðu þig inn í gátt [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Á heimasíðunni skal velja verkið þar sem umhverfið er í notkun.
1. Á verksíðunni skal velja umhverfið þar sem á að setja upp innbótina.
1. Á heimasíðu umhverfisins skal fletta niður á hlutann **Innbætur umhverfis** í hlutanum **Power Platform samþætting** þar sem hægt er að finna heiti Dataverse-umhverfisins.
1. Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.

    ![Heimasíða umhverfis í LCS](media/inventory-visibility-environment.png "Heimasíða umhverfis í LCS")

1. Veldu tengilinn **Setja upp nýja innbót**. Listi yfir tiltækar innbætur opnast.
1. Velja **Sýnileiki birgða** í listanum.
1. Sláðu inn gildi fyrir eftirfarandi reiti fyrir umhverfið þitt:

    - **Auðkenni AAD-forritsins (biðlara)**
    - **AAD-leigjandakenni**

    ![Uppsetningarsíða innbótar](media/inventory-visibility-setup.png "Uppsetningarsíða innbótar")

1. Samþykktu skilmálana með því að velja gátreitinn **Skilmálar**.
1. Velja **Setja upp**. Staða innbótarinnar birtist sem **Er í uppsetningu**. Þegar henni er lokið skal uppfæra síðuna til að sjá stöðuna breytast í **Uppsett**.

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>Fjarlægja innbótina

Til að fjarlægja innbótina skal velja **Fjarlægja**. Þegar LCS er uppfært verður innbót birgðasýnileikans fjarlægð. Fjarlægingarferlið mun fjarlægja innbótarskráninguna og ræsir einnig vinnslu til að hreinsa öll viðskiptagögn sem vistuð eru í þjónustunni.

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>Nota gögn lagerbirgða úr Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Nota samþættingarpakka birgðasýnileika

Ef keyrð er útgáfa 10.0.17 eða eldri af Supply Chain Management skal hafa samband við stuðningshóp vegna innleiðingar birgðasýnileika á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) til að fá skráarpakkann. Virkjaðu svo pakkann í LCS.

> [!NOTE]
> Ef villa vegna misræmis útgáfu kemur upp í uppsetningunni þarf að flytja inn handvirkt X++ verkið í þróunarumhverfið. Síðan skal stofna virkjanlega pakkann í þróunarumhverfinu og setja hann upp í þróunarumhverfinu.
> 
> Kóðinn fylgir með Supply Chain Management útgáfu 10.0.18. Ef sú útgáfa eða nýrri er keyrð þarf ekki uppsetningu.

Gangið úr skugga um að kveikt sé á eftirfarandi eiginleikum í umhverfi Supply Chain Management. (Sjálfgefið er að kveikt sé á þessu.)

| Lýsing eiginleika | Kóðaútgáfa | Skipta milli klasa |
|---|---|---|
| Gera notkun birgðavídda í InventSum-töflu virka eða óvirka | 10.0.11 | InventUseDimOfInventSumToggle |
| Gera notkun birgðavídda í InventSumDelta-töflu virka eða óvirka | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Setja upp samþættingu fyrir Sýnileika birgða

1. Í Supply Chain Management skal opna vinnusvæðið **[Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og kveikja á eiginleikanum **Samþætting sýnileika birgða**.
1. Farið í **Birgðastjórnun \> Uppsetning \> Samþætting færibreyta sýnileika birgða** og færið inn vefslóð umhverfisins þar sem birgðasýnileiki er keyrður.

    Finnið Azure-svæði LCS-umhverfisins og færið síðan inn vefslóðina. Vefslóðin er með eftirfarandi skjámynd:

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    Í Evrópu verður umhverfið til dæmis með eina af eftirfarandi vefslóðum:

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    Eftirfarandi svæði eru í boði sem stendur.

    | Azure-svæði | Stutt heiti svæðis |
    |---|---|
    | Austur-Ástralía | eau |
    | Suðaustur-Ástralía | seau |
    | Mið-Kanada | cca |
    | Austur-Kanda | eca |
    | Norður-Evrópa | neu |
    | Vestur-Evrópa | weu |
    | Austurhluti Bandaríkjanna | eus |
    | Vesturhluti Bandaríkjanna | wus |

1. Farið í **Birgðastjórnun \> Reglubundið \> Samþætting sýnileika birgða** og virkjið verkið. Öll tilvik birgðabreytinga úr Supply Chain Management verða nú bókuð í birgðasýnileika.

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>Almennt API innbótar birgðasýnileika

Almennt REST API innbótar birgðasýnileikans kynnir ýmsar tilteknar endastöðvar samþættingar. Það styður þrjár aðalsamskiptaleiðir:

- Bókun á lagerbirgðum breytist í innbótina úr ytra kerfi
- Fyrirspurn um núverandi lagermagn úr ytra kerfi
- Sjálfvirk samstilling við lagerbirgðir Supply Chain Management

Sjálfvirk samstilling er ekki hluti af almennu API. Þess í stað er það meðhöndlað í bakgrunni fyrir umhverfi þar sem innbót birgðasýnileika er virk.

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Sannvottun

Öryggistákn verkvangsins er notað til að kalla á innbót birgðasýnileika. Þess vegna þarf að búa til *Azure Active Directory (Azure AD) tákn* með því að nota Azure AD-forritið. Þá þarf að nota Azure AD táknið til að fá *aðgangsmerkið* úr öryggisþjónustunni.

Sækja merki öryggisþjónustu á eftirfarandi hátt:

1. Skráðu þig inn í Azure-gátt og notaðu hana til að finna `clientId` og `clientSecret` Supply Chain Management forritið.
1. Sækja Azure Active Directory tákn (`aadToken` ) með því að senda inn HTTP beiðni með eftirfarandi eiginleikum:
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Aðferð** - `GET`
    - **Meginefni (eyðublaðagögn)**:

        | lykill | gildi |
        | --- | --- |
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | tilföng | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. Þú ættir að fá `aadToken` svar, sem líkist eftirfarandi dæmi.

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

1. Búa skal til JSON-beiðni sem líkist eftirfarandi:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Hvar:
    - Gildið `client_assertion` verður að vera `aadToken` sem var móttekið í fyrra skrefi.
    - Gildið `context` verður að vera umhverfiskenni þar sem á að nota viðbótina.
    - Stillið öll önnur gildi eins og sýnt er í dæminu.

1. Sendið inn HTTP-beiðni með eftirfarandi eiginleikum:
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **Aðferð** - `POST`
    - **HTTP** - Inniheldur API-útgáfu (lykilinn er `Api-Version` og gildið er `1.0`)
    - **Meginefni efnis** - Nota skal JSON-beiðni sem var stofnuð í fyrra skrefi.

1. Þú færð `access_token` í staðinn. Þetta er það sem þú þarft sem handhafalykill til að kalla í API birgðasýnileikans. Eftirfarandi er dæmi.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>Skilgreina API fyrir sýnileika birgða

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

Sjálfgefna mælingarmagnið er tengt við Supply Chain Management. Hins vegar gætir þú viljað hafa magn sem er gert úr samsetningu sjálfgefinna mælinga. Til að gera þetta er hægt að hafa skilgreiningu á sérsniðnu magni, sem verður bætt við úttak lagerfyrirspurnar.

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
