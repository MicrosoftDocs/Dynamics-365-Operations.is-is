---
title: Samþætta við kerfi þriðju aðila fyrir framkvæmd framleiðslu
description: Þetta efni útskýrir hvernig þú getur samþætt Microsoft Dynamics 365 Supply Chain Management með þriðju aðila framleiðslukerfi (MES).
author: t-benebo
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 14e86a49777eefefae711bfe0d756361b09d69c2
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778450"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Samþætta við kerfi þriðju aðila fyrir framkvæmd framleiðslu

[!include [banner](../includes/banner.md)]

Sumar framleiðslustofnanir sem nota Microsoft Dynamics 365 Supply Chain Management nota innbyggða virkni í Dynamics 365 til að stjórna framleiðslustarfsemi þeirra fyrir vélar, búnað og starfsfólk. Hins vegar nota aðrar framleiðslustofnanir, sérstaklega þær sem hafa háþróaðar framleiðslukröfur, þriðja aðila framleiðslukerfi (MES) í staðinn. Stofnanir gætu valið MES lausn frá þriðja aðila vegna þess að hún er til dæmis sérstaklega sniðin að lóðréttri atvinnugrein þeirra.

Í samþættu lausninni eru gagnaskipti að fullu sjálfvirk og eiga sér stað í nánast rauntíma. Þess vegna er gögnum haldið til haga í báðum kerfum og ekki er þörf á handvirkri gagnafærslu. Til dæmis, þegar efnisnotkun er skráð í MES, tryggir samþættingin að sama neysla sé einnig skráð í Dynamics 365. Þess vegna eru uppfærðar birgðaskrár tiltækar fyrir önnur mikilvæg ferli, svo sem áætlanagerð og sölu.

Lausnin gerir það hraðara, auðveldara og ódýrara fyrir notendur Supply Chain Management að samþætta MES frá þriðja aðila. Það býður upp á eftirfarandi eiginleika:

- Viðskiptaviðburðir og viðmót sem styðja [helstu framkvæmdarferli framleiðslu](#processes-available-for-mes-integration)
- Miðstýrt mælaborð þar sem þú getur fylgst með vinnsluferli atburða og bilað og lagað ferla sem mistakast

Eftirfarandi mynd sýnir dæmigert safn viðskiptaviðburða, ferla og skilaboða sem skiptast á í samþættri lausn.

![Dæmigerð samþættingaratburðarás.](media/3p-mes-scenario.png "Dæmigerð samþættingaratburðarás.")

## <a name="turn-on-the-mes-integration-feature"></a>Kveiktu á MES samþættingareiginleikanum

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Framleiðslustýring*
- **Eiginleikaheiti:** *Samþætting framleiðslukerfis*

## <a name="processes-available-for-mes-integration"></a>Ferlar í boði fyrir MES samþættingu

Þú getur virkjað eitthvað af eða öllum eftirfarandi ferlum fyrir samþættingu.

| Heiti ferlis | Lýsing |
|---|---|
| Losa framleiðslupantanir og framleiðslupöntunarstöðu breyta viðskiptaviðburðum | Þetta ferli veitir viðskiptaviðburð sem MES getur hlustað á, til að fá upplýsingar um framleiðslupantanir sem ætti að framleiða. Búist er við að tilvísunargögnum sem tengjast framleiðslupöntuninni verði deilt frá Supply Chain Management til MES í gegnum Open Data Protocol (OData) eða gagnaeiningar. |
| Hefja framleiðslupöntun | Þetta ferli veitir Supply Chain Management upplýsingar um framleiðslupantanir sem verið er að hefja með því að nota MES. Það tryggir að bæði kerfin hafi uppfærða sýn á alla framleiðslustarfsemi. |
| Tilkynntu framleitt eða eytt magn | Þetta ferli veitir Supply Chain Management upplýsingar um vöru- og villumagn sem er tilkynnt um framleiðsluverk með því að nota MES. Það tryggir að umsjónarmenn á verkstæði hafi uppfærða sýn á framvindu framleiðsluáætlunar. |
| Tilkynna efnisnotkun | Þetta ferli veitir Supply Chain Management upplýsingar frá MES um magn efna sem er neytt. Það gerir uppfærðar birgðaskrár aðgengilegar öðrum mikilvægum ferlum, svo sem áætlanagerð og sölu. |
| Tilkynna tíma sem notaður hefur verið í aðgerðina | Þetta ferli veitir Supply Chain Management upplýsingar um þann tíma sem er notaður í tiltekna aðgerð. |
| Ljúka framleiðslupöntun | Þetta ferli upplýsir Supply Chain Management um að MES hafi uppfært framleiðslupöntun í lokastöðu *Lokað*. Þessi staða gefur til kynna að ekki verði meira magn framleitt á framleiðslupöntuninni. |

## <a name="monitor-incoming-messages"></a>Fylgstu með skilaboðum sem berast

Til að fylgjast með skilaboðum sem berast í kerfið skaltu opna **Samþætting framkvæmdarkerfa í framleiðslu** síðu. Þar er hægt að skoða, vinna úr og leysa vandamál.

## <a name="call-the-api"></a>Hringdu í API

Til að hringja í MES samþættingar API, sendu a`POST` beiðni á eftirfarandi endapunktsslóð:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Meginmál beiðninnar sem þú sendir ætti að líkjast eftirfarandi dæmi. Skiptu um gildi fyrir`_companyId`,`_messageType`, og`_messageContent` eins og krafist er. Fyrir upplýsingar um hinar ýmsu skilaboðagerðir sem API styður og hvernig á að hanna innihald þeirra, sjá næsta kafla.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API skilaboðategundir og innihald

Þessi hluti lýsir hverri tegund skilaboða sem hægt er að skiptast á í gegnum MES samþættingar API.

### <a name="start-production-order-message"></a>Byrja framleiðslupöntun skilaboð

Fyrir *hefja framleiðslupöntun* skilaboð, the`_messageType` gildi er `ProdProductionOrderStart`. Eftirfarandi tafla sýnir reiti sem þessi skilaboð styðja.

| Heiti reits | Staða | Gerð |
|---|---|---|
| `ProductionOrderNumber` | Skylda | Strengur |
| `StartedQuantity` | Valfrjálst | Rauntala |
| `StartedDate` | Valfrjálst | Dagsetning |
| `AutomaticBOMConsumptionRule` | Valfrjálst | Enum (FlushingPrincip\| Alltaf\| Aldrei) |

### <a name="report-as-finished-message"></a>Tilkynna sem lokið skilaboð

Fyrir *skýrslu sem lokið* skilaboð, the`_messageType` gildi er `ProdProductionOrderReportFinished`. Eftirfarandi tafla sýnir reiti sem þessi skilaboð styðja.

| Heiti reits | Staða | Gerð |
|---|---|---|
| `ProductionOrderNumber` | Skylda | Strengur |
| `ReportFinishedLines` | Skylda | Listi yfir línur (að minnsta kosti ein), sem hver um sig inniheldur farminn sem lýst er í næstu töflu |

Eftirfarandi tafla sýnir reiti sem hver lína í`ReportFinishedLines` kafla í`ProdProductionOrderReportFinished` skilaboð styður.

| Heiti reits | Staða | Gerð |
|---|---|---|
| `LineNumber` | Valfrjálst | Rauntala |
| `ItemNumber` | Valfrjálst | Strengur|
| `ProductionType` | Valfrjálst | Enum (MainItem\| Formúla\| BOM\| Sam_vara\| Eftir vöru\| Enginn), stækkanlegur |
| `ReportedErrorQuantity` | Valfrjálst | Rauntala|
| `ReportedGoodQuantity` | Valfrjálst | Rauntala|
| `ReportedErrorCatchWeightQuantity` | Valfrjálst | Rauntala |
| `ReportedGoodCatchWeightQuantity` | Valfrjálst | Rauntala |
| `AcceptError` | Valfrjálst |Boole |
| `ErrorCause` | Valfrjálst | Enum (Engin\| Efni\| Vél\| OperatingStaff), stækkanlegt |
| `ExecutedDateTime` | Valfrjálst | DateTime-gildi |
| `ReportAsFinishedDate` | Valfrjálst | Dagsetning |
| `AutomaticBOMConsumptionRule` | Valfrjálst | Enum (FlushingPrincip\| Alltaf\| Aldrei) |
| `AutomaticRouteConsumptionRule` | Valfrjálst |Enum (RouteDependent\| Alltaf\| Aldrei) |
| `RespectFlushingPrincipleDuringOverproduction` | Valfrjálst | Boole |
| `ProductionJournalNameId` | Valfrjálst | Strengur |
| `PickingListProductionJournalNameId` | Valfrjálst | Strengur|
| `RouteCardProductionJournalNameId` | Valfrjálst | Strengur |
| `FromOperationNumber` | Valfrjálst | Heiltala|
| `ToOperationNumber` | Valfrjálst | Heiltala|
| `InventoryLotId` | Valfrjálst | Strengur |
| `BaseValue` | Valfrjálst | Strengur |
| `EndJob` | Valfrjálst | Boole |
| `EndPickingList` | Valfrjálst | Boole |
| `EndRouteCard` | Valfrjálst | Boole |
| `PostNow` | Valfrjálst | Boole |
| `AutoUpdate` | Valfrjálst | Boole |
| `ProductColorId` | Valfrjálst | Strengur|
| `ProductConfigurationId` | Valfrjálst | Strengur |
| `ProductSizeId` | Valfrjálst | Strengur |
| `ProductStyleId` | Valfrjálst | Strengur |
| `ProductVersionId` | Valfrjálst | Strengur |
| `ItemBatchNumber` | Valfrjálst | Strengur |
| `ProductSerialNumber` | Valfrjálst | Strengur |
| `LicensePlateNumber` | Valfrjálst | Strengur |
| `InventoryStatusId` | Valfrjálst | Strengur |
| `ProductionWarehouseId` | Valfrjálst | Strengur |
| `ProductionSiteId` | Valfrjálst | Strengur |
| `ProductionWarehouseLocationId` | Valfrjálst | Strengur |
| `InventoryDimension1` til `InventoryDimension12` | Valfrjálst | Strengur |

12 stækkanlegu stærðirnar (`InventoryDimension1` í gegnum`InventoryDimension12`) krefjast sérsniðnar og eru ekki alltaf notaðar. Fyrir frekari upplýsingar um þau, sjá [Bættu við nýjum birgðavíddum með framlengingu](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Skilaboð um efnisnotkun (vallisti).

Fyrir *efnisnotkun (vallisti)* skilaboð, the`_messageType` gildi er `ProdProductionOrderPickingList`. Eftirfarandi tafla sýnir reiti sem þessi skilaboð styðja.

| Heiti reits | Staða | Gerð |
|---|---|---|
| `ProductionOrderNumber` | Skylda | Strengur |
| `JournalNameId` | Valfrjálst | Strengur |
| `PickingListLines` | Skylda | Listi yfir línur (að minnsta kosti ein), sem hver um sig inniheldur farminn sem lýst er í næstu töflu |

Eftirfarandi tafla sýnir reiti sem hver lína í`PickingListLines` kafla í`ProdProductionOrderPickingList` skilaboð styður.

| Heiti reits | Staða | Gerð |
|---|---|---|
| `ItemNumber` | Skylda | Strengur |
| `ConsumptionBOMQuantity` | Valfrjálst | Rauntala |
| `ProposalBOMQuantity` | Valfrjálst | Rauntala |
| `ScrapBOMQuantity` | Valfrjálst | Rauntala |
| `BOMUnitSymbol` | Valfrjálst | Strengur |
| `ConsumptionInventoryQuantity` | Valfrjálst | Rauntala |
| `ProposalInventoryQuantity` | Valfrjálst | Rauntala |
| `ConsumptionCatchWeightQuantity` | Valfrjálst | Rauntala |
| `ProposalCatchWeightQuantity` | Valfrjálst | Rauntala |
| `ConsumptionDate` | Valfrjálst | Dagsetning |
| `OperationNumber` | Valfrjálst | Heiltala |
| `LineNumber` | Valfrjálst | Rauntala |
| `PositionNumber` | Valfrjálst | Strengur |
| `IsConsumptionEnded` | Valfrjálst | Boole |
| `ErrorCause` | Valfrjálst | Enum (Engin\| Efni\| Vél\| OperatingStaff), stækkanlegt |

### <a name="time-used-for-operation-route-card-message"></a>Tími notaður fyrir aðgerð (leiðarkort) skilaboð

Fyrir *tími notaður til notkunar (leiðarkort)* skilaboð, the`_messageType` gildi er `ProdProductionOrderRouteCard`. Eftirfarandi tafla sýnir reiti sem þessi skilaboð styðja.

| Heiti reits | Staða | Gerð |
|---|---|---|
| `ProductionOrderNumber` | Skylda | Strengur |
| `JournalNameId` | Valfrjálst | Strengur |
| `RouteCardLines` | Skylda | Listi yfir línur (að minnsta kosti ein), sem hver um sig inniheldur farminn sem lýst er í næstu töflu |

Eftirfarandi tafla sýnir reiti sem hver lína í`RouteCardLines` kafla í`ProdProductionOrderRouteCard` skilaboð styður.

| Heiti reits | Staða | Gerð |
|---|---|---|
| `OperationNumber` | Skylda | Skylt, heiltala |
| `OperationPriority` | Valfrjálst | Enum (Aðal\| Annað 1\| Annað 2\| ...\| Secondary20) |
| `OperationId` | Valfrjálst | Strengur |
| `OperationsResourceId` | Valfrjálst | Strengur |
| `Worker` | Valfrjálst | Strengur |
| `HoursRouteCostCategoryId` | Valfrjálst | Strengur |
| `QuantityRouteCostCategoryId` | Valfrjálst | Strengur |
| `HourlyRate` | Valfrjálst | Rauntala |
| `Hours` | Valfrjálst | Rauntala |
| `GoodQuantity` | Valfrjálst | Rauntala |
| `ErrorQuantity` | Valfrjálst | Rauntala |
| `CatchWeightGoodQuantity` | Valfrjálst | Rauntala |
| `CatchWeightErrorQuantity` | Valfrjálst | Rauntala |
| `QuantityPrice` | Valfrjálst | Rauntala |
| `ProcessingPercentage` | Valfrjálst | Rauntala |
| `ConsumptionDate` | Valfrjálst | Dagsetning |
| `TaskType` | Valfrjálst | Enum (QueueBefore\| Uppsetning\| Ferli\| Skarast\| Flutningur\| Biðröð Eftir\| Byrði) |
| `ErrorCause` | Valfrjálst | Enum (Engin\| Efni\| Vél\| OperatingStaff), stækkanlegt |
| `OperationCompleted` | Valfrjálst | Boole |
| `BOMConsumption` | Valfrjálst | Boole |
| `ReportAsFinished` | Valfrjálst | Boole |

### <a name="end-production-order-message"></a>Skilaboð um lok framleiðslupöntunar

Fyrir *enda framleiðslupöntun* skilaboð, the`_messageType` gildi er `ProdProductionOrderEnd`. Eftirfarandi tafla sýnir reiti sem þessi skilaboð styðja.

| Heiti reits | Staða | Gerð |
|---|---|---|
| `ProductionOrderNumber` | Skylda | Strengur |
| `ExecutedDateTime` | Valfrjálst | DateTime-gildi |
| `EndedDate` | Valfrjálst | Dagsetning |
| `UseTimeAndAttendanceCost` | Valfrjálst | Boole |
| `AutoReportAsFinished` | Valfrjálst | Boole |
| `AutoUpdate` | Valfrjálst | Boole |

## <a name="receive-feedback-about-the-state-of-a-message"></a>Fáðu endurgjöf um stöðu skilaboða

Eftir að MES hefur sent skilaboð til Supply Chain Management gæti verið viðeigandi fyrir Supply Chain Management að skila endurgjöf um stöðu skilaboðanna. Hér eru nokkur dæmi um tilvik þar sem þessi hegðun gæti átt við:

- Það er enginn aðili sem ber ábyrgð á stöðugu eftirliti með MES samþættingu.
- Sá sem ber ábyrgð á eftirliti með MES samþættingu vill fá tilkynningu í tölvupósti þegar skilaboð mistekst, svo hann viti að hann þurfi að grípa til aðgerða.
- MES verður að sýna villuboð til að tilkynna rekstraraðila verkstæðisgólfs eða einhvern úr upplýsingatæknideild að þeir verði að grípa til aðgerða.
- MES verður að endurreikna pöntunaráætlunina eftir að hann fær bilunarskilaboð (til dæmis vegna þess að framleiðslupöntun tókst ekki að hefjast).

Í þessum tilvikum geturðu nýtt þér staðlaða viðvörunareiginleikann í Supply Chain Management. Fyrir upplýsingar um hvernig staðlaðar viðvaranir virka, sjá eftirfarandi úrræði:

- Hjálparefni: [Yfirlit yfir viðvaranir](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Myndband: [Valkostir viðvörunarreglu í Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Til dæmis gætirðu sett upp eftirfarandi viðvaranir til að veita endurgjöf um stöðu skilaboða:

- Búðu til viðskiptaviðburð ("Senda ytra") sem er notaður þegar skilaboð eru *Mistókst*.
- Sendu tilkynningu og tölvupóst til upplýsingatæknistjóra eða framleiðslugólfstjóra.