---
title: Samþætta við kerfi þriðju aðila fyrir framkvæmd framleiðslu
description: Þessi grein útskýrir hvernig hægt er að samþætta Microsoft Dynamics 365 Supply Chain Management við framkvæmd framleiðslu kerfi þriðja aðila (MES).
author: johanhoffmann
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8629ef2581a114609d14999a3c1fc48b49c988e0
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336216"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Samþætta við kerfi þriðju aðila fyrir framkvæmd framleiðslu

[!include [banner](../includes/banner.md)]

Sum framleiðslufyrirtæki sem nota Microsoft Dynamics 365 Supply Chain Management nota staðbundna virkni í Dynamics 365 til að stýra framleiðslustarfsemi sinni fyrir vélar, búnað og starfskrafta. Hins vegar nota önnur framleiðslufyrirtæki, einkum þær sem eru með háþróaðar framleiðslukröfur, framkvæmdarkerfi framleiðslu (MES) frá þriðja aðila í staðinn. Fyrirtæki gætu valið MES-lausn frá þriðja aðila vegna þess að hún er til dæmis sniðin sérstaklega að flestum eða öllum þrepum iðnaðar þeirra.

Í samþættri lausn eru gagnaskipti að fullu sjálfvirk og eiga sér stað í nær rauntíma. Þess vegna er gögnum haldið uppfæraðu í báðum kerfum, og engin handvirk gagnafærsla er nauðsynleg. Til dæmis, þegar efnisnotnun er skráð í MES, tryggir samþættingin að sama notkun sé einnig skráð í Dynamics 365. Þess vegna eru uppfærðar birgðafærslur aðgengilegt öðrum mikilvægum ferlum, svo sem áætlanagerð og sölu.

Lausnin gerir það hraðar, auðveldara og ódýrara fyrir notendur Supply Chain Management að samþætta við þriðja aðila MES. Það býður upp á eftirfarandi eiginleika:

- Viðskiptatilvik og viðmót sem styðja við [helstu framleiðslu- og framkvæmdaferli](#processes-available-for-mes-integration)
- Miðlægt stjórnborð þar sem hægt er að rekja úrvinnsluferli tilviksins, keyra úrræðaleit og lagfæra ferli sem mistakast

Eftirfarandi skýringarmynd sýnir dæmigert safn viðskiptatilvika, ferla og skilaboða sem skiptast á í samþættri lausn.

![Dæmigerðar aðstæður samþættingar.](media/3p-mes-scenario.png "Dæmigerðar aðstæður samþættingar.")

## <a name="turn-on-the-mes-integration-feature"></a>Kveiktu á samþættingareiginleikanum fyrir MES

Stjórnandi þarf að kveikja á honum í kerfinu þínu áður en hægt er að nota þennan eiginleika eins og lýst er í eftirfarandi ferli.

1. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
1. Gakktu úr skugga um að leyfislykillinn **Tími og viðvera** sé virkur (hann sýnir gátmerki). Þessi leyfislykill er áskilinn vegna þess að hann stjórnar virkni og gögnum framkvæmd framleiðslu. Ef það er ekki virkt skaltu gera eftirfarandi skref:
    1. Setjið kerfið í viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
    1. Á síðunni **Skilgreining leyfis** skal velja gátreitinn **Tími og viðvera**.
    1. Slökkvið á viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)
1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.
1. Notið vinnusvæðið [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eiginleikanum *Samþætting framleiðslukerfis*. (Sem hluti af Supply Chain Management, útgáfa 10.0.29, er sjálfgefið kveikt á þessum eiginleika.)

## <a name="processes-available-for-mes-integration"></a>Ferlar í boði fyrir MES-samþættingu

Hægt er að virkja eitt eða öll af eftirfarandi ferlum til samþættingar.

| Heiti ferlis | Lýsing |
|---|---|
| Framleiðslupantanir losaðar og staða framleiðslupöntunar breytt eftir viðskiptatilvikum | Þetta ferli veitir viðskiptatilvik sem MES getur hlustað á, til að fá upplýsingar um framleiðslupantanir sem ætti að framleiða. Gert er ráð fyrir að tilvísunargögnum sem tengjast framleiðslupöntuninni sé deilt frá Supply Chain Management til MES í gegnum Open Data Protocol (OData) eða gagnaeiningar. |
| Hefja framleiðslupöntun | Þetta ferli veitir Supply Chain Management upplýsingar um framleiðslupantanir sem eru að hefjast með því að nota MES. Það tryggir að bæði kerfin hafi uppfært yfirlit yfir alla framleiðslustarfsemi. |
| Tilkynna um framleitt magn eða rýrnnunarmagn | Þetta ferli veitir Supply Chain Management upplýsingar um gott magn og villumagn sem tilkynnt er um í framleiðsluverki með MES. Það tryggir að yfirmenn í vinnusal hafi uppfært yfirlit yfir framvindu framleiðsluáætlunarinnar. |
| Skýrsla um efnisnotkunina | Þetta ferli veitir Supply Chain Management upplýsingar frá MES um magn efnis sem er neytt. Það gerir uppfærðar birgðafærslur aðgengilegt öðrum mikilvægum ferlum, svo sem áætlanagerð og sölu. |
| Tilkynna tímann sem farið er í aðgerðina | Þetta ferli veitir Supply Chain Management upplýsingar um tímann sem er notaður fyrir tiltekna aðgerð. |
| Ljúka framleiðslupöntun | Þetta ferli upplýsir Supply Chain Management um að MES hafi uppfært framleiðslupöntun í endanlega stöðu *Lokið*. Þessi staða gefur til kynna að ekki verði framleitt meira magn miðað við framleiðslupöntunina. |

## <a name="monitor-incoming-messages"></a>Fylgjast með skilaboðum á innleið

Til að fylgjast með komandi skilaboðum til kerfisins skaltu opna síðuna **Samþætting framkvæmdar framleiðslukerfa**. Þar er hægt að skoða, vinna úr og leysa úr vandamálum.

Öll skilaboð fyrir tiltekna framleiðslupöntun eru meðhöndluð í þeirri röð sem þau eru móttekin. Hins vegar má ekki vinna skilaboð fyrir mismunandi framleiðslupantanir í móttekinni röð vegna þess að runuvinnsla er unnin samhliða. Ef um bilun er að ræða mun runuvinnslan reyna að vinna úr hverjum skilaboðum þrisvar sinnum áður en það er sett í stöðu sem *Mistókst*.

## <a name="call-the-api"></a>Kalla á forritaskil (API)

Sendið `POST` beiðni á eftirfarandi vefslóð endastöðvar til að kalla á MES-samþættingu API:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Meginmál beiðninnar sem þú sendir ætti að líkjast eftirfarandi dæmi. Skipta út gildunum fyrir `_companyId`, `_messageType` og `_messageContent` eftir þörfum. Frekari upplýsingar um ýmsar tegundir skilaboða sem API styður og hvernig á að hanna efni þeirra er að finna í næsta hluta.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>Silaboðagerðir forritaaskila (API) og efni

Þessi hluti lýsir hverri skilaboðagerð sem hægt er að skiptast á í gegnum MES-samþættingu API.

### <a name="start-production-order-message"></a>Hefja skilaboð framleiðslupantanir

Fyrir skilaboðin *ræsa framleiðslupöntun* er `_messageType` gildið `ProdProductionOrderStart`. Eftirfarandi tafla sýnir reitina sem þessi skilaboð styðja.

| Nafn svæðis | Staða | Gerð |
|---|---|---|
| `ProductionOrderNumber` | Skylda | Strengur |
| `StartedQuantity` | Valfrjálst | Rauntala |
| `StartedDate` | Valfrjálst | Dagsetning |
| `AutomaticBOMConsumptionRule` | Valfrjálst | Enum (FlushingPrincip \| Alltaf \| Aldrei) |

### <a name="report-as-finished-message"></a>Bóka skilaboð sem tilbúin

Fyrir skilaboðin *Tilkynna sem lokið* er `_messageType` gildið `ProdProductionOrderReportFinished`. Eftirfarandi tafla sýnir reitina sem þessi skilaboð styðja.

| Nafn svæðis | Staða | Gerð |
|---|---|---|
| `ProductionOrderNumber` | Skylda | Strengur |
| `ReportFinishedLines` | Skylda | Listi yfir línur (að minnsta kosti ein), sem hver inniheldur farminn sem lýst er í næstu töflu |

Á eftirfarandi töflu má sjá þá reiti sem hver lína í `ReportFinishedLines` hluta `ProdProductionOrderReportFinished` skilaboðanna styður.

| Nafn svæðis | Staða | Gerð |
|---|---|---|
| `LineNumber` | Valfrjálst | Rauntala |
| `ItemNumber` | Valfrjálst | Strengur|
| `ProductionType` | Valfrjálst | Fasttexti (MainItem \| Formúla \| Uppskrift \| Co_Product \| By_Product \| ekkert), stækkanlegt |
| `ReportedErrorQuantity` | Valfrjálst | Rauntala|
| `ReportedGoodQuantity` | Valfrjálst | Rauntala|
| `ReportedErrorCatchWeightQuantity` | Valfrjálst | Rauntala |
| `ReportedGoodCatchWeightQuantity` | Valfrjálst | Rauntala |
| `AcceptError` | Valfrjálst | Enum (Já \| Nei) |
| `ErrorCause` | Valfrjálst | Fasttexti (Ekkert \| Efni \| Vél \| OperatingStaff), framlengjanlegt |
| `ExecutedDateTime` | Valfrjálst | DateTime-gildi |
| `ReportAsFinishedDate` | Valfrjálst | Dagsetning |
| `AutomaticBOMConsumptionRule` | Valfrjálst | Enum (FlushingPrincip \| Alltaf \| Aldrei) |
| `AutomaticRouteConsumptionRule` | Valfrjálst |Enum (RouteDependent \| Alltaf \| Aldrei) |
| `RespectFlushingPrincipleDuringOverproduction` | Valfrjálst | Enum (Já \| Nei) |
| `ProductionJournalNameId` | Valfrjálst | Strengur |
| `PickingListProductionJournalNameId` | Valfrjálst | Strengur|
| `RouteCardProductionJournalNameId` | Valfrjálst | Strengur |
| `FromOperationNumber` | Valfrjálst | Heiltala|
| `ToOperationNumber` | Valfrjálst | Heiltala|
| `InventoryLotId` | Valfrjálst | Strengur |
| `BaseValue` | Valfrjálst | Strengur |
| `EndJob` | Valfrjálst | Enum (Já \| Nei) |
| `EndPickingList` | Valfrjálst | Enum (Já \| Nei) |
| `EndRouteCard` | Valfrjálst | Enum (Já \| Nei) |
| `PostNow` | Valfrjálst | Enum (Já \| Nei) |
| `AutoUpdate` | Valfrjálst | Enum (Já \| Nei) |
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

12 víddirnar sem hægt er að lengja (`InventoryDimension1` til og með `InventoryDimension12`) krefjast sérstillingar og eru ekki alltaf notaðar. Frekari upplýsingar um þær eru í [Bæta við nýjum birgðavíddum með viðbót](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Efnisnotkun (tiltektarlisti) skilaboð

Fyrir *Efnisnotkun (tiltektarlisti)* skilaboðin er `_messageType` gildið `ProdProductionOrderPickingList`. Eftirfarandi tafla sýnir reitina sem þessi skilaboð styðja.

| Nafn svæðis | Staða | Gerð |
|---|---|---|
| `ProductionOrderNumber` | Skylda | Strengur |
| `JournalNameId` | Valfrjálst | Strengur |
| `PickingListLines` | Skylda | Listi yfir línur (að minnsta kosti ein), sem hver inniheldur farminn sem lýst er í næstu töflu |

Á eftirfarandi töflu má sjá þá reiti sem hver lína í `PickingListLines` hluta `ProdProductionOrderPickingList` skilaboðanna styður.

| Nafn svæðis | Staða | Gerð |
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
| `IsConsumptionEnded` | Valfrjálst | Enum (Já \| Nei) |
| `ErrorCause` | Valfrjálst | Fasttexti (Ekkert \| Efni \| Vél \| OperatingStaff), framlengjanlegt |
| `InventoryLotId` | Valfrjálst | Strengur |

### <a name="time-used-for-operation-route-card-message"></a>Tími sem notaður er til að skrifa (leiðarspjald) skilaboð

Fyrir *Tími sem notaður er til að skrifa (leiðarspjald)* skilaboð er `_messageType` gildið `ProdProductionOrderRouteCard`. Eftirfarandi tafla sýnir reitina sem þessi skilaboð styðja.

| Nafn svæðis | Staða | Gerð |
|---|---|---|
| `ProductionOrderNumber` | Skylda | Strengur |
| `JournalNameId` | Valfrjálst | Strengur |
| `RouteCardLines` | Skylda | Listi yfir línur (að minnsta kosti ein), sem hver inniheldur farminn sem lýst er í næstu töflu |

Á eftirfarandi töflu má sjá þá reiti sem hver lína í `RouteCardLines` hluta `ProdProductionOrderRouteCard` skilaboðanna styður.

| Nafn svæðis | Staða | Gerð |
|---|---|---|
| `OperationNumber` | Skylda | Heiltala |
| `OperationPriority` | Valfrjálst | Fasttexti (Aðal \| Auka1 \| Auka2 \| ... \| Auka20) |
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
| `TaskType` | Valfrjálst | Fasttexti (QueueBefore \| Uppsetning \| Ferli \| Skörun \| Flutningur \| QueueAfter \| Byrði) |
| `ErrorCause` | Valfrjálst | Fasttexti (Ekkert \| Efni \| Vél \| OperatingStaff), framlengjanlegt |
| `OperationCompleted` | Valfrjálst | Enum (Já \| Nei) |
| `BOMConsumption` | Valfrjálst | Enum (Já \| Nei) |
| `ReportAsFinished` | Valfrjálst | Enum (Já \| Nei) |

### <a name="end-production-order-message"></a>Skilaboð um að ljúka framleiðslupöntun

Fyrir skilaboðin *ljúka framleiðslupöntun* er `_messageType` gildið `ProdProductionOrderEnd`. Eftirfarandi tafla sýnir reitina sem þessi skilaboð styðja.

| Nafn svæðis | Staða | Gerð |
|---|---|---|
| `ProductionOrderNumber` | Skylda | Strengur |
| `ExecutedDateTime` | Valfrjálst | DateTime-gildi |
| `EndedDate` | Valfrjálst | Dagsetning |
| `UseTimeAndAttendanceCost` | Valfrjálst | Enum (Já \| Nei) |
| `AutoReportAsFinished` | Valfrjálst | Enum (Já \| Nei) |
| `AutoUpdate` | Valfrjálst | Enum (Já \| Nei) |

## <a name="other-production-information"></a>Aðrar vöruupplýsingar

Skilaboðin styðja aðgerðir eða viðburði sem eiga sér stað í vinnusal. Þau eru unnin með MES samþættingarrammanum sem lýst er í þessari grein. Hönnunin gerir ráð fyrir að aðrar tilvísunarupplýsingar sem á að deila með MES (svo sem vörutengdar upplýsingar eða reikningur fyrir uppskrift eða leið (með sérstakri uppsetningu og stillingartíma) sem notaðar eru í tiltekinni framleiðslupöntun) verði sóttar með [Gagnaeiningum](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#data-entities) úr kerfinu með skráarflutningi eða OData.

## <a name="receive-feedback-about-the-state-of-a-message"></a>Fá endurgjöf um stöðu skilaboða

Eftir að MES hefur sent skilaboð til Supply Chain Management gæti skipt máli að stjórnendur Supply Chain Management skili athugasemdum um ástand skilaboðanna. Hér eru nokkur dæmi um tilvik þar sem þessi hegðun gæti átt við:

- Það er enginn aðili ábyrgur fyrir því að hafa stöðugt eftirlit með MES-samþættingunni.
- Einstaklingurinn sem er ábyrgur fyrir því að hafa eftirlit með samþættingu MES vill fá tilkynningu með tölvupósti þegar skilaboð mistakast, svo að viðkomandi viti að þörf sé á því að grípa til aðgerða.
- MES verður að sýna villuboð til að láta stjórnanda í vinnusal eða einhvern úr tæknideildinni vita að hann þurfi að grípa til aðgerða.
- MES verður að endurreikna pöntunaráætlunina eftir að hún fær villuboð (t.d. vegna þess að framleiðslupöntun mistókst að ræsa).

Í þessum tilvikum geturðu nýtt þér hefðbundna viðvörunareiginleikann í Supply Chain Management. Sjá eftirfarandi tilföng um frekari upplýsingar um hvernig staðlaðar viðvaranir virka:

- Hjálpargrein: [Yfirlit yfir viðvaranir](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Myndband: [Valkostir viðvaranareglu í fjármála- og reksturs](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Til dæmis væri hægt að setja upp eftirfarandi viðvaranir til að gefa endurgjöf um ástand skilaboða:

- Stofna viðskiptatilvik („Senda annars staðar“) sem er notaður þegar skilaboðin eru *Mistókst*.
- Senda tilkynningu og tölvupóst til kerfisstjóra eða framleiðslustjóra framleiðslugólfs.

