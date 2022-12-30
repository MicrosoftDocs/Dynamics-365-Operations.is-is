---
title: Stofneiningar ferðar
description: Í þessari grein eru upplýsingar um einingar stofnunar gagna ferðar hópa saman þeim gagnaverum sem þurfa að búa til virka ferð.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6234dfa61a5859e2ecaca75594c69c49ba326629
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167672"
---
# <a name="voyage-creation-entities"></a>Stofneiningar ferðar

[!include [banner](../includes/banner.md)]

Einingar stofnunar gagna ferðar hópa saman þeim gagnaverum sem þurfa að búa til virka ferð. Þú eða flutningamiðlari getið notað þessar gagnaeiningar til að búa til upplýsingar um ferð, gáma, fólíó og ferðalínufærslur sem vísa í fyrirliggjandi innkaupapöntunar- eða flutningspöntunarlínur.

## <a name="voyages-itmtableentity"></a>Ferðir (ITMTableEntity)

Ferðin táknar ferð vöru á innleið og þjónar sem kostnaðarþáttur á hæsta stigi heildarkostnaðar. Þar er að finna upplýsingar um hausstig sem tengjast skipinu, upprunalega höfn og endanlega höfn. Þessi virkni er studd af `ITMTableEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Afhendingarmáti | ITMTable.DlvModeId | Nvarchar(10) | Nr. | Nr. |
| Ráðlegging miðlara | ITMTable.ITMBrokerAdvised | Datetime | Nr. | Nr. |
| Fundur viðskiptavinar | ITMTable.ITMCustomerAppointment | Datetime | Nr. | Nr. |
| Afhent í vöruhúsi | ITMTable.ITMDelAtWarehouse | Datetime | Nr. | Nr. |
| Leiðbeiningar um afhendingu | ITMTable.ITMDeliveryInstructions | Datetime | Nr. | Nr. |
| Brottfarartími | ITMTable.ITMDepartureDate | Datetime | Nr. | Nr. |
| Vörur losaðar | ITMTable.ITMGoodsReleased | Datetime | Nr. | Nr. |
| Dagsetning staðbundins flutnings | ITMTable.ITMLocalTransportDate | Datetime | Nr. | Nr. |
| Staðbundinn flutningstími | ITMTable.ITMLocalTransportTime | Int | Nr. | Nr. |
| Upprunalegt farmbréf sent | ITMTable.ITMOriginalBOLSebt | Datetime | Nr. | Nr. |
| Upprunaleg skjöl móttekin | ITMTable.ITMOriginalDocsReceived | Datetime | Nr. | Nr. |
| Staða innkaupapöntunar | ITMTable.ITMPurchStatus | Int | Nr. | Nr. |
| Staðfestingardagsetning | ITMTable.ITMVerificationDate | Datetime | Nr. | Nr. |
| Kennimerki tollfærslu | ITMTable.ShipCustomsEntryId | Nvarchar(20) | Nr. | Nr. |
| Sendingardagsetning | ITMTable.ShipDate | Datetime | Nr. | Nr. |
| Lýsing | ITMTable.ShipDescription | Nvarchar(60) | Nr. | Nr. |
| Skjöl móttekin | ITMTable.ShipDocReceived | Int | Nr. | Nr. |
| Áætluð afhendingardagsetning | ITMTable.ShipEstDlvDate | Datetime | Nr. | Nr. |
| Áætlaður komutími til afhendingarhafnar | ITMTable.ShipEstPortDate | Datetime | Nr. | Nr. |
| Frá höfn | ITMTable.ShipFromPort | Nvarchar(20) | Nr. | Nr. |
| Grunnflugfarmbréf/farmbréf | ITMTable.ShipHAWB | Nvarchar(20) | Nr. | Nr. |
| Ferð | ITMTable.ShipId | Nvarchar(20) | **Já** | **Já** |
| Bókunartilvísun | ITMTable.ShipIdExternal | Nvarchar(20) | Nr. | Nr. |
| Sniðmát ferðar | ITMTable.ShipJourneyId | Nvarchar(20) | Nr. | Nr. |
| Staðbundinn miðlari | ITMTable.ShipLocalForwarder | Nvarchar(20) | Nr. | Nr. |
| Aðalflugfarmbréf/farmbréf | ITMTable.ShipMAWB | Nvarchar(20) | Nr. | Nr. |
| Mæling | ITMTable.ShipMeasurement | Tölustafir(32; 6) | Nr. | Nr. |
| Mælieining | ITMTable.ShipMeasurementUnit | Int | Nr. | Nr. |
| Fjöldi bretta | ITMTable.ShipNoOfPallets | Int | Nr. | Nr. |
| Ferð í biðstöðu | ITMTable.ShipPending | Int | Nr. | Nr. |
| Athugasemdir | ITMTable.ShipRemarks | Nvarchar(MAX) | Nr. | Nr. |
| Leiga | ITMTable.ShipRental | Int | Nr. | Nr. |
| Staða ferðar | ITMTable.ShipStatusId | Nvarchar(20) | Nr. | Nr. |
| Láta stemma í númeri | ITMTable.ShipTallyInNumber | Nvarchar(20) | Nr. | Nr. |
| Til hafnar | ITMTable.ShipToPort | Nvarchar(20) | Nr. | Nr. |
| Dagsetning mats | ITMTable.ShipValuationDate | Datetime | Nr. | Nr. |
| Flutningsfyrirtæki | ITMTable.ShipVendAccount | Nvarchar(20) | Nr. | Nr. |
| Skip | ITMTable.ShipVesselId | Nvarchar(20) | Nr. | **Já** |
| Ytra kenni ferðar | ITMTable.ShipVoyage | Nvarchar(20) | Nr. | Nr. |

### <a name="number-sequences-for-voyages"></a>Númeraraðir fyrir ferðir

Sameiginleg númeraröð ferða stýrir úthlutun á ferðakennum.

Gildið sem er sent til gagnaeiningar sem **Ferðakenni** (`ShipId`) er notað til að bera kennsl á fyrirliggjandi skrá fyrir uppfærslu. Ef sú skrá er ekki til fer hegðunin eftir því hvort úthlutaða númeraröðin er stillt til að leyfa handvirk færslu:

- Ef handvirk færsla er virk er ný færsla stofnuð sem notar gildið sem sent var.
- Ef handvirk færsla er ekki virk er næsta númer í úthlutuðu númeraröðinni notað í staðinn fyrir gildið sem gefið var upp.

Á meðan á innflutningslotu stendur er haldið eftir gildi staðgengils sem er flutt inn sem kenni ferðar. Þessi hegðun tryggir að gámur og ferðalínur sem vísa til staðgengill eru innifalin í ferðinni, og að þær séu uppfærðar til að endurspegla gildið sem er úthlutað úr númeraröðinni.

### <a name="automatic-cost-transactions"></a>Sjálfvirkar kostnaðarfærslur

Hægt er að bæta sjálfvirkum kostnaði við ferð af síðunni **Sjálfvirkur kostnaður** í Microsoft Dynamics 365 Supply Chain Management (**Heildarkostnaður \> Kostnaður \> Sjálfvirk kostnaðaruppsetning**). Einnig er hægt að búa til skrár fyrir sjálfvirkan kostnað með því að nota gögn um kostnaðarfærslu fyrir hvert kostnaðarsvæði sem heildarkostnaður styður.

Sjálfvirkur kostnaður sem er stilltur í Supply Chain Management er lagður á ferðina þegar ferðalína er stofnuð. Enginn kostnaður verður sýnilegur á móti færslunni fyrr en hausfærsla hennar er tengdur við línuna.

## <a name="shipping-containers-itmcontainersentity"></a>Gámar (ITMContainersEntity)

Gámur táknar efnislegan gám sem vörur eru fluttar í. Þessi efnislegi gámur gæti verið vöruflutningagámur fyrir sjófrakt eða stakur vörubretti fyrir flugfrakt. Í gámnuum eru upplýsingar sem eru á hausstigi og tengjast auðkenni gáms, innsiglisnúmeri og gámagerð. (Gámagerðin veitir upplýsingar um vídd). Þessi virkni er studd af `ITMContainersEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Brottfarartími | ITMContainers.ITMDepartureDate | Datetime | Nr. | Nr. |
| Dagsetning staðbundins flutnings | ITMContainers.ITMLocalTransportDate | Datetime | Nr. | Nr. |
| Staðbundinn flutningstími | ITMContainers.ITMLocalTransportTime | Int | Nr. | Nr. |
| Upprunaleg ferð | ITMContainers.OrigShipId | Nvarchar(20) | Nr. | Nr. |
| Raunþyngd | ITMContainers.ShipActualWeight | Tölustafir(32; 6) | Nr. | Nr. |
| Ráðlegging miðlara | ITMContainers.ShipBrokerAdvised | Datetime | Nr. | Nr. |
| Gámur | ITMContainers.ShipContainerId | Nvarchar(20) | **Já** | **Já** |
| Gámagerð | ITMContainers.ShipContainerTypeId | Nvarchar(20) | Nr. | Nr. |
| Einingargerð | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | Nr. | Nr. |
| Breytt í leigu | ITMContainers.ShipConvertedToRental | Int | Nr. | Nr. |
| Fundur viðskiptavinar | ITMContainers.ShipCustomerAppointment | Datetime | Nr. | Nr. |
| Sendingardagsetning | ITMContainers.ShipDate | Datetime | Nr. | Nr. |
| Afhent í vöruhúsi | ITMContainers.ShipDelAtWarehouse | Datetime | Nr. | Nr. |
| Leiðbeiningar um afhendingu | ITMContainers.ShipDeliveryInstructions | Datetime | Nr. | Nr. |
| Upphafsdagsetning gerðarprófunarvottorðs | ITMContainers.ShipECAppliedDate | Datetime | Nr. | Nr. |
| Lokadagsetning gerðarprófunarvottorðs | ITMContainers.ShipECExpiryDate | Datetime | Nr. | Nr. |
| Númer gerðarprófunarvottorðs | ITMContainers.ShipECNum | Nvarchar(20) | Nr. | Nr. |
| Móttökudagsetning gerðarprófunarvottorðs | ITMContainers.ShipECReceivedDate | Datetime | Nr. | Nr. |
| Áætluð afhendingardagsetning | ITMContainers.ShipEstDlvDate | Datetime | Nr. | Nr. |
| Áætlaður komutími til afhendingarhafnar | ITMContainers.ShipEstPortDate | Datetime | Nr. | Nr. |
| Væntanleg hleðsludagsetning | ITMContainers.ShipExpectedLoadingDate | Datetime | Nr. | Nr. |
| Frá höfn | ITMContainers.ShipFromPort | Nvarchar(20) | Nr. | Nr. |
| Lýsing á vörum | ITMContainers.ShipGoodsDesc | Nvarchar(60) | Nr. | Nr. |
| Vörur losaðar | ITMContainers.ShipGoodsReleased | Datetime | Nr. | Nr. |
| GPS-staðsetningartæki | ITMContainers.ShipGPSUnit | Nvarchar(30) | Nr. | Nr. |
| Grunnflugfarmbréf/farmbréf | ITMContainers.ShipHAWB | Nvarchar(20) | Nr. | Nr. |
| Ferð | ITMContainers.ShipId | Nvarchar(20) | **Já** | **Já** |
| Sniðmát ferðar | ITMContainers.ShipJourneyId | Nvarchar(20) | Nr. | Nr. |
| Staðbundinn miðlari | ITMContainers.ShipLocalForwarder | Nvarchar(20) | Nr. | Nr. |
| Mæling | ITMContainers.ShipMeasurement | Tölustafir(32; 6) | Nr. | Nr. |
| Mælieining | ITMContainers.ShipMeasurementUnit | Int | Nr. | Nr. |
| Fjöldi kassa | ITMContainers.ShipNoOfCartons | Tölustafir(32; 6) | Nr. | Nr. |
| Upprunalegt farmbréf sent | ITMContainers.ShipOriginalBOLSebt | Datetime | Nr. | Nr. |
| Upprunaleg skjöl móttekin | ITMContainers.ShipOriginalDocsReceived | Datetime | Nr. | Nr. |
| Innsiglisnúmerið okkar | ITMContainers.ShipOurSealNum | Nvarchar(20) | Nr. | Nr. |
| Notað | ITMContainers.ShipPendingUsed | Int | Nr. | Nr. |
| Staða innkaupapöntunar | ITMContainers.ShipPurchStatus | Int | Nr. | Nr. |
| Gerð kælingar | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | Nr. | Nr. |
| Athugasemdir | ITMContainers.ShipRemarks | Nvarchar(MAX) | Nr. | Nr. |
| Leiga | ITMContainers.ShipRental | Int | Nr. | Nr. |
| Hægt að skila | ITMContainers.ShipReturnable | Int | Nr. | Nr. |
| Staða ferðar | ITMContainers.ShipStatusId | Nvarchar(20) | Nr. | Nr. |
| Innsiglisnúmer flutningsfyrirtækis | ITMContainers.ShipTheirSealNum | Nvarchar(20) | Nr. | Nr. |
| Til hafnar | ITMContainers.ShipToPort | Nvarchar(20) | Nr. | Nr. |
| Staðfestingardagsetning | ITMContainers.ShipVerificationDate | Datetime | Nr. | Nr. |
| Skip | ITMContainers.ShipVesselId | Nvarchar(20) | Nr. | **Já** |

### <a name="voyage-id-validation"></a>Staðfesting ferðakennis

Kenni gámsins er ekki stýrt af númeraröð. Það er aðeins einkvæmt aðeins í samhengi við ferðina sem það er notað.

Ef gámaeiningin (`ITMContainersEntity`) er notuð óháð ferðaeiningunni (`ITMTableEntity`) verður **Ferðakenni** (`ShipId`) gildið að passa við fyrirliggjandi færslu í ferðatöflunni. Að öðrum kosti mistekst innflutningurinn.

Ef gámur (`ITMContainersEntity`) og ferðaeining (`ITMTableEntity`) eru notuð sem hluti af sama innflutningsferli, verður ferðaeining að koma á undan til að búa til gám. Að öðrum kosti er ekki hægt að staðfesta gildi **Kenni ferðar** (`ShipId`). Ef gildi staðgengils er notaður fyrir **Ferðakenni** (`ShipId`) gildið er aðeins hægt að búa til tengingu ef sami staðgengill er notaður sem **Ferðakenni** (`ShipId`) gildið í gámnum.

### <a name="other-field-validations"></a>Staðfestingar á öðrum reit

Eftirfarandi tafla sýnir reitina í töflunni yfir gáma(`ITMContainers`) sem eru staðfestir miðað við uppsetningartöflur fyrir heildarkostnað. Það sýnir einnig gögn um einingar heildarkostnað sem farmflytjandi getur notað til að lesa gildin sem eru til staðar og tryggja að gild gildi séu móttekin í umhverfinu.

| Reitur í ITMContainers töflu | Gagnaeining heildarkostnaðar |
|---|---|
| Gámagerð | ITMShippingContainerTypeEntity |
| Lýsing á vörum | ITMGoodsDescriptionEntity |
| Gerð kælingar | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Fólíó (ITMFolioEntity)

Fólíó táknar flokkun vara í gámi fyrir tollskýrslur. Í fólíóinu eru upplýsingar á hausstigi sem tengjast tollmiðlara og lýsing á vörunni. Þessi virkni er studd af `ITMFolioEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Ráðlegging miðlara | ITMFolioTable.ShipBrokerAdvised | Datetime | Nr. | Nr. |
| Eftirlitsnúmer farms | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | Nr. | Nr. |
| Fundur viðskiptavinar | ITMFolioTable.ShipCustomerAppointment | Datetime | Nr. | Nr. |
| Tollmiðlari | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | Nr. | Nr. |
| Tollkenni | ITMFolioTable.ShipCustomsId | Nvarchar(60) | Nr. | Nr. |
| Fyrirtæki | ITMFolioTable.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| Afhent í vöruhúsi | ITMFolioTable.ShipDelAtWarehouse | Datetime | Nr. | Nr. |
| Leiðbeiningar um afhendingu | ITMFolioTable.ShipDeliveryInstructions | Datetime | Nr. | Nr. |
| Skjöl móttekin | ITMFolioTable.ShipDocReceived | Int | Nr. | Nr. |
| Áætluð afhendingardagsetning | ITMFolioTable.ShipEstDlvDate | Datetime | Nr. | Nr. |
| Áætlaður komutími til afhendingarhafnar | ITMFolioTable.ShipEstPortDate | Datetime | Nr. | Nr. |
| Útflutningsaðili | ITMFolioTable.ShipExporterId | Nvarchar(20) | Nr. | Nr. |
| Nafn | ITMFolioTable.ShipExporterName | Nvarchar(60) | Nr. | Nr. |
| Dagsetning fólíós | ITMFolioTable.ShipFolioDate | Datetime | Nr. | Nr. |
| Fólíó | ITMFolioTable.ShipFolioId | Nvarchar(20) | **Já** | **Já** |
| Frá höfn | ITMFolioTable.ShipFromPort | Nvarchar(20) | Nr. | Nr. |
| Lýsing á vörum | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | Nr. | Nr. |
| Vörur losaðar | ITMFolioTable.ShipGoodsReleased | Datetime | Nr. | Nr. |
| Grunnflugfarmbréf/farmbréf | ITMFolioTable.ShipHAWB | Nvarchar(20) | Nr. | Nr. |
| Ferð | ITMFolioTable.ShipId | Nvarchar(20) | Nr. | **Já** |
| Mæling | ITMFolioTable.ShipMeasurement | Tölustafir(32; 6) | Nr. | Nr. |
| Mælieining | ITMFolioTable.ShipMeasurementUnit | Int | Nr. | Nr. |
| Fjöldi kassa | ITMFolioTable.ShipNoOfCartons | Tölustafir(32; 6) | Nr. | Nr. |
| Upprunalegt farmbréf sent | ITMFolioTable.ShipOriginalBOLSebt | Datetime | Nr. | Nr. |
| Upprunaleg skjöl móttekin | ITMFolioTable.ShipOriginalDocsReceived | Datetime | Nr. | Nr. |
| Staða innkaupapöntunar | ITMFolioTable.ShipPurchStatus | Int | Nr. | Nr. |
| Athugasemdir | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | Nr. | Nr. |
| Staða ferðar | ITMFolioTable.ShipStatusId | Nvarchar(20) | Nr. | Nr. |
| Kóði tollflokks | ITMFolioTable.ShipTariffCode | Nvarchar(10) | Nr. | Nr. |
| Til hafnar | ITMFolioTable.ShipToPort | Nvarchar(20) | Nr. | Nr. |
| Dagsetning mats | ITMFolioTable.ShipValuationDate | Datetime | Nr. | Nr. |
| Staðfestingardagsetning | ITMFolioTable.ShipVerificationDate | Datetime | Nr. | Nr. |
| Lykill lánardrottins | ITMFolioTable.VendAccount | Nvarchar(20) | Nr. | Nr. |

### <a name="number-sequences-for-folios"></a>Númeraraðir fyrir fólíó

Númeraröðin fyrir fólíó stýrir úthlutun á fólíókennum.

Gildið sem er sent til gagnaeiningar sem **Fólíókenni** (`FolioId`) er notað til að bera kennsl á fyrirliggjandi skrá fyrir uppfærslu. Ef sú skrá er ekki til fer hegðunin eftir því hvort úthlutaða númeraröðin er stillt til að leyfa handvirk færslu:

- Ef handvirk færsla er virk er ný færsla stofnuð sem notar gildið sem sent var.
- Ef handvirk færsla er ekki virk er næsta númer í úthlutuðu númeraröðinni notað í staðinn fyrir gildið sem gefið var upp.

Á meðan á innflutningsferlinu stendur er gildi staðgengils haldið eftir sem fólíóauðkenni. Þessi hegðun tryggir að gámur og ferðalínur sem vísa til staðgengill eru tengdar á réttan hátt, og að þær séu uppfærðar til að endurspegla gildið sem er úthlutað úr númeraröðinni.

### <a name="field-validations"></a>Villuleitir reita

Reiturinn **Vörulýsing** í fólíótöflunni (`ITMFolioTable`) er staðfestur á móti uppsetningartöflu heildarkostnaðar sem ber sama nafn. Flutningsmiðlari getur notað gagnaeininguna `ITMGoodsDescriptionEntity` heildarkostnaður til að lesa gildin sem eru til staðar og tryggja að gild gildi séu móttekin í umhverfinu.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Línur ferðar fyrir innkaupapantanir (ITMPurchaseLineEntity)

Lína ferðar táknar eina innkaupapöntunarlínu sem er með í ferðinni. Þessum tengslum er komið á í reitunum **Innkaupapöntunarnúmer** og **Innkaupapöntunarlínunúmer**. Lína ferðar vísar til hverrar fyrri færslu sem var stofnuð fyrir ferðina, gáminn og fólíó. Þessi virkni er studd af `ITMPurchaseLineEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Gjaldmiðill | ITMLine.CurrencyCode | Nvarchar(3) | Nr. | Nr. |
| Nettóupphæð | ITMLine.LineAmountMST | Tölustafir(32; 6) | Nr. | Nr. |
| Innkaupalínunúmer | ITMLine.RefRecId | Tölustafir(32; 6) | **Já** | Nr. |
| Gámur | ITMLine.ShipContainerId | Int | Nr. | Nr. |
| Fyrirtæki | ITMLine.ShipDataArea | Nvarchar(20) | **Já** | Nr. |
| Uppgefið magn | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nr. | Nr. |
| Fólíó | ITMLine.ShipFolioId | Tölustafir(32; 6) | Nr. | Nr. |
| Ferð | ITMLine.ShipId | Nvarchar(20) | **Já** | Nr. |
| Vörunúmer | ITMLine.ShipItemId | Nvarchar(20) | Nr. | Nr. |
| Mæling | ITMLine.ShipMeasurement | Nvarchar(20) | Nr. | Nr. |
| Mælieining | ITMLine.ShipMeasurementUnit | Tölustafir(32; 6) | Nr. | Nr. |
| Fjöldi kassa | ITMLine.ShipNoOfCartons | Int | Nr. | Nr. |
| Staðsetning | ITMLine.ShipPosition | Tölustafir(32; 6) | Nr. | Nr. |
| Magn | ITMLine.ShipQty | Int | Nr. | Nr. |
| Innkaupapöntunarnúmer | ITMLine.TransRefId | Tölustafir(32; 6) | **Já** | Nr. |
| Eining | ITMLine.UnitId | Int | Nr. | Nr. |
| Rúmmál | ITMLine.Volume | Nvarchar(10) | Nr. | Nr. |
| Vægi | ITMLine.Weight | Tölustafir(32; 6) | Nr. | Nr. |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Línur ferðar fyrir flutningspantanir (ITMTransferLineEntity)

Lína ferðar táknar eina flutningspöntunarlínu sem er með í ferðinni. Þessum tengslum er komið á í reitunum **Flutningspöntunarnúmer** og **Flutningspöntunarlínunúmer**. Lína ferðar vísar til hverrar fyrri færslu sem var stofnuð fyrir ferðina, gáminn og fólíó. Þessi virkni er studd af `ITMTransferLineEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Gjaldmiðill | ITMLine.CurrencyCode | Nvarchar(3) | Nr. | Nr. |
| Nettóupphæð | ITMLine.LineAmountMST | Tölustafir(32; 6) | Nr. | Nr. |
| Gámur | ITMLine.ShipContainerId | Int | Nr. | Nr. |
| Fyrirtæki | ITMLine.ShipDataArea | Nvarchar(20) | **Já** | Nr. |
| Uppgefið magn | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nr. | Nr. |
| Fólíó | ITMLine.ShipFolioId | Tölustafir(32; 6) | Nr. | Nr. |
| Ferð | ITMLine.ShipId | Nvarchar(20) | **Já** | Nr. |
| Vörunúmer | ITMLine.ShipItemId | Nvarchar(20) | Nr. | Nr. |
| Mæling | ITMLine.ShipMeasurement | Nvarchar(20) | Nr. | Nr. |
| Mælieining | ITMLine.ShipMeasurementUnit | Tölustafir(32; 6) | Nr. | Nr. |
| Fjöldi kassa | ITMLine.ShipNoOfCartons | Int | Nr. | Nr. |
| Staðsetning | ITMLine.ShipPosition | Tölustafir(32; 6) | Nr. | Nr. |
| Magn | ITMLine.ShipQty | Int | Nr. | Nr. |
| Númer flutningslínu | ITMLine.TransferLineNumber | Tölustafir(32; 6) | **Já** | Nr. |
| Flutningspöntunarnúmer | ITMLine.TransRefId | Tölustafir(32; 6) | **Já** | Nr. |
| Eining | ITMLine.UnitId | Int | Nr. | Nr. |
| Rúmmál | ITMLine.Volume | Nvarchar(10) | Nr. | Nr. |
| Vægi | ITMLine.Weight | Tölustafir(32; 6) | Nr. | Nr. |

### <a name="reference-table"></a>Tilvísanatafla

Línur ferðar eru búnar til í gegnum tengingu við opna pöntunarlínu á innleið. Þessi lína getur verið á innkaupapöntun, eða það er hægt að fá færslu á flutningspöntun. Reiturinn `RefTableId` í ferðalínutöflunni (`ITMLine`) tilgreinir hvaða raðartegund línunnar tengist með því að vísa í töflunúmer. Ef vísað er til tiltekinna töflunúmera í töflunni þar sem verið er að búa til gögnin, er einingum skipt eftir þeim gildum.

Gildin fyrir viðmiðunartöfluna (`RefTableId`) og færslugerðina (`TransType`) eru sjálfgefin á annaðhvort í einingu innkaupalínu heildarkostnaðar eða einingu flutningslínu heildarkostnaðar.

### <a name="validation"></a>Villuleit

Í ferðalínu er vísað beint í færslu ferðar, færslu gáms og fólíó-færslu. Ef eining innkaupalínu (`ITMPurchaseLinesEntity`) eða eining flutningslína (`ITMPurchaseLinesEntity`) er notuð óháð þeim aðilum sem notaðir eru til að búa til þessar tilvísunarfærslur verða gildi **Ferðakenni** (`ShipId`), **Gámur** (`ShipContainerId`) og **Fólíó** (`ShipFolioId`) að passa við fyrirliggjandi færslu í samsvarandi töflum. Að öðrum kosti mistekst innflutningurinn.

Ef önnur eining línu er notaður sem hluti af sama innflutninglotu verða hinir aðilarnir að koma á undan því að búa til ferðalínu. Annars er ekki hægt að staðfesta gildin. Ef gildi staðgengils er notaður fyrir ferð eða fólíó númer er aðeins hægt að búa til tengingu ef sami staðgengill er notaður fyrir ferð eða folio númer í einingu ferðalínu.

Ef innkaupapöntunar- eða flutningspöntunarlína er þegar úthlutað til núverandi ferðalínu verður nýja ferðalínan ekki búin til. Áður en hægt er að tengja pöntunarlínuna við nýja ferð verður að fjarlægja hana úr núverandi ferð.

### <a name="order-line-identification"></a>Auðkenni pöntunarlínu

Ferðalínur vísa beint í viðmiðunargildin **Færslukenni** (`RefRecId`), **Kenni birgðavíddar** (`InventDimId`) og **Kenni birgðafærslu** (`InventTransId`). Þessi gildi þurfa ekki lengur að vera með þegar gagnaeiningin er notuð. Þess í stað þarf nú að taka pöntunarlínunúmerið með. Saman gera pöntunarlínunúmerið og pöntunarnúmerið kleift að bera kennsl á hvert þessara tilvísunargilda.

### <a name="voyage-line-quantity"></a>Magn í línu ferðar

Þar sem ferðalína er beintengd pöntunarlínu er gildið **Magn** (`ShipQty`) sem er slegið inn með því að nota eininguna sem krefst þess að gildin stemmi. Villuleit er keyrð á móti magninu á annaðhvort innkaupapöntunarlínunni eða færslulínunni. Ef staðfestingin mistókst verður ekki unnið úr færslunni.

### <a name="calculated-fields"></a>Reiknuð svæði

Reitirnir **Þyngd** og **Rúmmál** eru reiknaðir til að samþykkja gildi sem eru móttekin í gegnum gagnaeininguna. Ef engin gildi eru gefin upp eru gildi kerfisins notuð til að uppfæra þessa reiti, ef gildi kerfisins eru tiltæk. Fyrir heildarkostnað eru gildin reiknuð út á eftirfarandi hátt:

- *Þyngd* = *Magn* × *Brúttóþyngd vöru*
- *Rúmmál* = *Magn* × (*Brúttódýpt vöru* × *Brúttóhæð vöru* × *Brúttóbreidd vöru*)

## <a name="sequencing"></a>Röðun

Vegna tengsla á milli taflanna verður að stofna færslu ferðar fyrst. Aðeins er hægt að búa til línu ferðar eftir að ferðin, gámurinn og fólíóin hafa verið búin til.

Til að búa til ferð án staðfestingarviðvörunar verður kerfið að vinna úr eftirfarandi einingum í eftirfarandi röð:

1. Ferðir (`ITMTableEntity`)
1. Gámar (`ITMContainersEntity`)
1. Fólíó (`ITMFolioTableEntity`)
1. Línur ferðar (`ITMPurchaseLinesEntity` eða `ITMTransferLinesEntity`)
