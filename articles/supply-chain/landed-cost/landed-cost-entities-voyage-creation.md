---
title: Voyage sköpunareiningar
description: Þetta efnisatriði veitir upplýsingar um gagnaeiningar fyrir stofnun ferð, sem flokka gagnaeiningarnar sem þarf til að búa til vinnuferð.
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
ms.openlocfilehash: 17f63af3ce1f858ed3e2086fc81c5e17c5e76be0
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813171"
---
# <a name="voyage-creation-entities"></a>Voyage sköpunareiningar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Gagnaeiningarnar fyrir ferðina flokka saman gagnaeiningarnar sem þarf til að búa til vinnuferð. Þú eða flutningsmiðlarinn þinn getur notað þessar gagnaeiningar til að búa til ferð-, flutningsgáma-, folio- og siglingalínuskrár sem vísa til núverandi kaupandapöntunar eða flutningspöntunarlína.

## <a name="voyages-itmtableentity"></a>Voyages (ITMTableEntity)

Ferðin táknar ferðalag vöru á heimleið og þjónar sem hæsta kostnaðarsvæði í Landkostnaði. Það inniheldur upplýsingar á hausstigi sem tengjast skipinu, upprunahöfn og ákvörðunarhöfn. Þessi virkni er studd af`ITMTableEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Afhendingarmáti | ITMTable.DlvModeId | Nvarchar(10) | Nr. | Nr. |
| Ráðlegging miðlara | ITMTable.ITMBrokerAdvised | Datetime | Nr. | Nr. |
| Fundur viðskiptavinar | ITMTable.ITMCustomer Appointment | Datetime | Nr. | Nr. |
| Afhent í vöruhúsi | ITMTable.ITMDelAtWarehouse | Datetime | Nr. | Nr. |
| Leiðbeiningar um afhendingu | ITMTable.ITMDeliveryInstructions | Datetime | Nr. | Nr. |
| Brottfarartími | ITMTable.ITMDepartureDate | Datetime | Nr. | Nr. |
| Vörur losaðar | ITMTable.ITMGoods Gefið út | Datetime | Nr. | Nr. |
| Dagsetning staðbundins flutnings | ITMTable.ITMLocalTransportDate | Datetime | Nr. | Nr. |
| Staðbundinn flutningstími | ITMTable.ITMLocalTransportTime | Int | Nr. | Nr. |
| Upprunalegt farmbréf sent | ITMTable.ITMOriginalBOLSebt | Datetime | Nr. | Nr. |
| Upprunaleg skjöl móttekin | ITMTable.ITMOriginalDocsReceived | Datetime | Nr. | Nr. |
| Staða innkaupapöntunar | ITMTable.ITMPurchStatus | Int | Nr. | Nr. |
| Staðfestingardagsetning | ITMTable.ITMVerificationDate | Datetime | Nr. | Nr. |
| Kennimerki tollfærslu | ITMTable.ShipCustomsEntryId | Nvarchar (20) | Nr. | Nr. |
| Sendingardagsetning | ITMTable.ShipDate | Datetime | Nr. | Nr. |
| Lýsing | ITMTable.ShipDescription | Nvarchar(60) | Nr. | Nr. |
| Skjöl móttekin | ITMTable.ShipDocReceived | Int | Nr. | Nr. |
| Áætluð afhendingardagsetning | ITMTable.ShipEstDlvDate | Datetime | Nr. | Nr. |
| Áætlaður komutími til afhendingarhafnar | ITMTable.ShipEstPortDate | Datetime | Nr. | Nr. |
| Frá höfn | ITMTable.ShipFromPort | Nvarchar (20) | Nr. | Nr. |
| Heimilisflug/farskírteini | ITMTable.ShipHAWB | Nvarchar (20) | Nr. | Nr. |
| Ferð | ITMTable.ShipId | Nvarchar (20) | **Já** | **Já** |
| Bókunartilvísun | ITMTable.ShipIdExternal | Nvarchar (20) | Nr. | Nr. |
| Sniðmát ferðar | ITMTable.ShipJourneyId | Nvarchar (20) | Nr. | Nr. |
| Staðbundinn miðlari | ITMTable.ShipLocalForwarder | Nvarchar (20) | Nr. | Nr. |
| Skipstjóri flugleið/farskírteini | ITMTable.ShipMAWB | Nvarchar (20) | Nr. | Nr. |
| Mæling | ITMTable.ShipMeasurement | Númeric(32, 6) | Nr. | Nr. |
| Mælieining | ITMTable.ShipMeasurementUnit | Int | Nr. | Nr. |
| Fjöldi bretta | ITMTable.ShipNoOfPallets | Int | Nr. | Nr. |
| Ferð í biðstöðu | ITMTable.ShipPending | Int | Nr. | Nr. |
| Athugasemdir | ITMTable.ShipRemarks | Nvarchar(MAX) | Nr. | Nr. |
| Leiga | ITMTable.Ship Rental | Int | Nr. | Nr. |
| Staða ferðar | ITMTable.ShipStatusId | Nvarchar (20) | Nr. | Nr. |
| Tölum saman | ITMTable.ShipTallyInNumber | Nvarchar (20) | Nr. | Nr. |
| Til hafnar | ITMTable.ShipToPort | Nvarchar (20) | Nr. | Nr. |
| Dagsetning mats | ITMTable.ShipValuationDate | Datetime | Nr. | Nr. |
| Flutningsfyrirtæki | ITMTable.ShipVendAccount | Nvarchar (20) | Nr. | Nr. |
| Skip | ITMTable.ShipVesselId | Nvarchar (20) | Nr. | **Já** |
| Ytra kenni ferðar | ITMTable.ShipVoyage | Nvarchar (20) | Nr. | Nr. |

### <a name="number-sequences-for-voyages"></a>Númeraraðir fyrir siglingar

Sameiginleg númeraröð fyrir ferðir stýrir úthlutun ferðakennimerkja.

Gildið sem er sent til gagnaeiningarinnar sem **Ferðaskilríki** (`ShipId`) gildi er notað til að auðkenna núverandi skrá til uppfærslu. Ef sú skrá er ekki til, fer hegðunin eftir því hvort úthlutað númeraröð er stillt til að leyfa handvirka innslátt:

- Ef handvirk færsla er virkjuð er ný færsla búin til sem notar samþykkt gildi.
- Ef handvirk færslu er ekki virkjuð er næsta númer í úthlutaðri númeraröðinni notað í stað gildisins sem hefur verið samþykkt.

Meðan á innflutningslotunni stendur, er staðgengilsgildinu sem er flutt inn sem ferðakennslu haldið eftir. Þessi hegðun tryggir að flutningsgáma- og siglingalínur sem vísa til staðgengils eru með í ferðinni og að þær séu uppfærðar til að endurspegla gildið sem er úthlutað úr númeraröðinni.

### <a name="automatic-cost-transactions"></a>Sjálfvirk kostnaðarfærslur

Hægt er að bæta sjálfvirkum kostnaði við ferð frá **Bílakostnaður** síðu í Microsoft Dynamics 365 Supply Chain Management (**Landaður kostnaður \> Kostnaðaruppsetning \> Bílakostnaður**). Einnig er hægt að búa til færslur fyrir sjálfvirkan kostnað með því að nota kostnaðarfærslugagnaeiningar fyrir hvert kostnaðarsvæði sem landaður kostnaður styður.

Sjálfvirkur kostnaður sem er stilltur í Supply Chain Management er settur á ferðina þegar siglingalína er búin til. Enginn kostnaður verður sýnilegur á móti færslunni fyrr en hausskráin er tengd línuupplýsingum.

## <a name="shipping-containers-itmcontainersentity"></a>Sendingargámar (ITMContainersEntity)

Sendingagámur táknar líkamlegan gám sem vörur eru fluttar í. Þessi efnislegi gámur gæti verið vörugámur fyrir sjófrakt eða eitt bretti fyrir flugfrakt. Sendingargámurinn inniheldur upplýsingar á hausstigi sem tengjast auðkenni sendingargáms, innsiglisnúmeri og gerð flutningsgáms. (Gámgerðin gefur upplýsingar um vídd.) Þessi virkni er studd af`ITMContainersEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Brottfarartími | ITMContainers.ITMDepartureDate | Datetime | Nr. | Nr. |
| Dagsetning staðbundins flutnings | ITMContainers.ITMLocalTransportDate | Datetime | Nr. | Nr. |
| Staðbundinn flutningstími | ITMContainers.ITMLocalTransportTime | Int | Nr. | Nr. |
| Upprunaleg ferð | ITMContainers.OrigShipId | Nvarchar (20) | Nr. | Nr. |
| Raunþyngd | ITMContainers.ShipActualWeight | Númeric(32, 6) | Nr. | Nr. |
| Ráðlegging miðlara | ITMContainers.ShipBrokerAdvised | Datetime | Nr. | Nr. |
| Gámur | ITMContainers.ShipContainerId | Nvarchar (20) | **Já** | **Já** |
| Gámagerð | ITMContainers.ShipContainerTypeId | Nvarchar (20) | Nr. | Nr. |
| Einingargerð | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | Nr. | Nr. |
| Breytt í leigu | ITMContainers.ShipConvertedToRental | Int | Nr. | Nr. |
| Fundur viðskiptavinar | ITM Containers.Ship Customer Appointment | Datetime | Nr. | Nr. |
| Sendingardagsetning | ITMContainers.ShipDate | Datetime | Nr. | Nr. |
| Afhent í vöruhúsi | ITMContainers.ShipDelAtWarehouse | Datetime | Nr. | Nr. |
| Leiðbeiningar um afhendingu | ITMContainers.ShipDeliveryInstructions | Datetime | Nr. | Nr. |
| Upphafsdagsetning gerðarprófunarvottorðs | ITMContainers.ShipECAppliedDate | Datetime | Nr. | Nr. |
| Lokadagsetning gerðarprófunarvottorðs | ITMContainers.ShipECExpiryDate | Datetime | Nr. | Nr. |
| Númer gerðarprófunarvottorðs | ITMContainers.ShipECNum | Nvarchar (20) | Nr. | Nr. |
| Móttökudagsetning gerðarprófunarvottorðs | ITMContainers.ShipECReceivedDate | Datetime | Nr. | Nr. |
| Áætluð afhendingardagsetning | ITMContainers.ShipEstDlvDate | Datetime | Nr. | Nr. |
| Áætlaður komutími til afhendingarhafnar | ITMContainers.ShipEstPortDate | Datetime | Nr. | Nr. |
| Væntanleg hleðsludagsetning | ITMContainers.ShipExpectedLoadingDate | Datetime | Nr. | Nr. |
| Frá höfn | ITMContainers.ShipFromPort | Nvarchar (20) | Nr. | Nr. |
| Lýsing á vörum | ITMContainers.ShipGoodsDesc | Nvarchar(60) | Nr. | Nr. |
| Vörur losaðar | ITMContainers.ShipGoods Gefið út | Datetime | Nr. | Nr. |
| GPS-staðsetningartæki | ITMContainers.ShipGPSUnit | Nvarchar(30) | Nr. | Nr. |
| Heimilisflug/farskírteini | ITMContainers.ShipHAWB | Nvarchar (20) | Nr. | Nr. |
| Ferð | ITMContainers.ShipId | Nvarchar (20) | **Já** | **Já** |
| Sniðmát ferðar | ITMContainers.ShipJourneyId | Nvarchar (20) | Nr. | Nr. |
| Staðbundinn miðlari | ITMContainers.ShipLocalForwarder | Nvarchar (20) | Nr. | Nr. |
| Mæling | ITMContainers.ShipMeasurement | Númeric(32, 6) | Nr. | Nr. |
| Mælieining | ITMContainers.ShipMeasurementUnit | Int | Nr. | Nr. |
| Fjöldi kassa | ITMContainers.ShipNoOfCartons | Númeric(32, 6) | Nr. | Nr. |
| Upprunalegt farmbréf sent | ITMContainers.ShipOriginalBOLSebt | Datetime | Nr. | Nr. |
| Upprunaleg skjöl móttekin | ITMContainers.ShipOriginalDocsReceived | Datetime | Nr. | Nr. |
| Innsiglisnúmerið okkar | ITMContainers.ShipOurSealNum | Nvarchar (20) | Nr. | Nr. |
| Notað | ITMContainers.ShipPendingUsed | Int | Nr. | Nr. |
| Staða innkaupapöntunar | ITMContainers.ShipPurchStatus | Int | Nr. | Nr. |
| Gerð kælingar | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | Nr. | Nr. |
| Athugasemdir | ITMContainers.ShipRemarks | Nvarchar(MAX) | Nr. | Nr. |
| Leiga | ITMContainers.Ship Rental | Int | Nr. | Nr. |
| Hægt að skila | ITMContainers.ShipReturnable | Int | Nr. | Nr. |
| Staða ferðar | ITMContainers.ShipStatusId | Nvarchar (20) | Nr. | Nr. |
| Innsiglisnúmer flutningsfyrirtækis | ITMContainers.ShipTheirSealNum | Nvarchar (20) | Nr. | Nr. |
| Til hafnar | ITMContainers.ShipToPort | Nvarchar (20) | Nr. | Nr. |
| Staðfestingardagsetning | ITMContainers.ShipVerificationDate | Datetime | Nr. | Nr. |
| Skip | ITMContainers.ShipVesselId | Nvarchar (20) | Nr. | **Já** |

### <a name="voyage-id-validation"></a>Voyage ID staðfesting

Auðkenni sendingargáma er ekki stjórnað af númeraröð. Það er aðeins einstakt í samhengi við siglinguna sem það er notað á.

Ef flutningsgámaeiningin (`ITMContainersEntity`) er notað óháð ferðaeiningu (`ITMTableEntity`), the **Ferðaskilríki** (`ShipId`) gildi verður að passa við núverandi skrá í ferðatöflunni. Annars mun innflutningurinn mistakast.

Ef flutningsgámaeiningin (`ITMContainersEntity`) og ferðaeiningin (`ITMTableEntity`) eru notuð sem hluti af sömu innflutningslotu, verður ferðaeiningin að fara á undan stofnun flutningsgáms. Annars er **Ferðaskilríki** (`ShipId`) gildi er ekki hægt að staðfesta. Ef staðgengilsgildi er notað fyrir **Ferðaskilríki** (`ShipId`) gildi, þá er aðeins hægt að stofna sambandið ef sami staðgengill er notaður og **Ferðaskilríki** (`ShipId`) gildi í flutningsgámaeiningunni.

### <a name="other-field-validations"></a>Aðrar vettvangsprófanir

Eftirfarandi tafla sýnir reiti í flutningsgámatöflunni (`ITMContainers`) sem eru staðfestar gegn uppsetningartöflum fyrir landað kostnað. Það sýnir einnig landaða kostnaðargagnaeiningar sem flutningsmiðlari getur notað til að lesa núverandi gildi og tryggja að gild gildi berist í umhverfi þínu.

| Reitur í ITMContainers töflunni | Landað kostnaðargagnaeining |
|---|---|
| Gámagerð | ITMShippingContainerTypeEntity |
| Lýsing á vörum | ITMGoodsDescriptionEntity |
| Gerð kælingar | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Folios (ITMFolioEntity)

Folio táknar flokkun hluta í flutningsgámi að því er varðar tollskýrslur. Blaðið inniheldur upplýsingar á hausstigi sem tengjast tollmiðlaranum og vörulýsingu. Þessi virkni er studd af`ITMFolioEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Ráðlegging miðlara | ITMfolioTable.Ship Broker Advised | Datetime | Nr. | Nr. |
| Eftirlitsnúmer farms | ITMFolioTable.ShipCargoControlNumber | Nvarchar (20) | Nr. | Nr. |
| Fundur viðskiptavinar | ITMFolioTable.Ship Customer Appointment | Datetime | Nr. | Nr. |
| Tollmiðlari | ITMFolioTable.Ship CustomsBroker | Nvarchar (20) | Nr. | Nr. |
| Tollkenni | ITMFolioTable.ShipCustomsId | Nvarchar(60) | Nr. | Nr. |
| Fyrirtæki | ITMFolioTable.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| Afhent í vöruhúsi | ITMFolioTable.ShipDelAtWarehouse | Datetime | Nr. | Nr. |
| Leiðbeiningar um afhendingu | ITMfolioTable.ShipDeliveryInstructions | Datetime | Nr. | Nr. |
| Skjöl móttekin | ITMFolioTable.ShipDocReceived | Int | Nr. | Nr. |
| Áætluð afhendingardagsetning | ITMfolioTable.ShipEstDlvDate | Datetime | Nr. | Nr. |
| Áætlaður komutími til afhendingarhafnar | ITMFolioTable.ShipEstPortDate | Datetime | Nr. | Nr. |
| Útflutningsaðili | ITMfolioTable.ShipExporterId | Nvarchar (20) | Nr. | Nr. |
| Nafn | ITMfolioTable.ShipExporterName | Nvarchar(60) | Nr. | Nr. |
| Dagsetning fólíós | ITMFolioTable.ShipFolioDate | Datetime | Nr. | Nr. |
| Fólíó | ITMFolioTable.ShipFolioId | Nvarchar (20) | **Já** | **Já** |
| Frá höfn | ITMfolioTable.ShipFromPort | Nvarchar (20) | Nr. | Nr. |
| Lýsing á vörum | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | Nr. | Nr. |
| Vörur losaðar | ITMFolioTable.Ship Goods útgefin | Datetime | Nr. | Nr. |
| Heimilisflug/farskírteini | ITMfolioTable.ShipHAWB | Nvarchar (20) | Nr. | Nr. |
| Ferð | ITMfolioTable.ShipId | Nvarchar (20) | Nr. | **Já** |
| Mæling | ITMFolioTable.ShipMeasurement | Númeric(32, 6) | Nr. | Nr. |
| Mælieining | ITMFolioTable.ShipMeasurement Unit | Int | Nr. | Nr. |
| Fjöldi kassa | ITMFolioTable.ShipNoOfCartons | Númeric(32, 6) | Nr. | Nr. |
| Upprunalegt farmbréf sent | ITMFolioTable.ShipOriginalBOLSebt | Datetime | Nr. | Nr. |
| Upprunaleg skjöl móttekin | ITMFolioTable.ShipOriginalDocsReceived | Datetime | Nr. | Nr. |
| Staða innkaupapöntunar | ITMFolioTable.ShipPurchStatus | Int | Nr. | Nr. |
| Athugasemdir | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | Nr. | Nr. |
| Staða ferðar | ITMFolioTable.ShipStatusId | Nvarchar (20) | Nr. | Nr. |
| Kóði tollflokks | ITMFolioTable.Ship TariffCode | Nvarchar(10) | Nr. | Nr. |
| Til hafnar | ITMfolioTable.ShipToPort | Nvarchar (20) | Nr. | Nr. |
| Dagsetning mats | ITMFolioTable.Ship ValuationDate | Datetime | Nr. | Nr. |
| Staðfestingardagsetning | ITMfolioTable.ShipVerificationDate | Datetime | Nr. | Nr. |
| Lykill lánardrottins | ITMfolioTable.VendAccount | Nvarchar (20) | Nr. | Nr. |

### <a name="number-sequences-for-folios"></a>Númeraraðir fyrir folio

Númeraröðin fyrir folio stjórnar úthlutun folio auðkenna.

Gildið sem er sent til gagnaeiningarinnar sem **Folio auðkenni** (`FolioId`) gildi er notað til að auðkenna núverandi skrá til uppfærslu. Ef sú skrá er ekki til, fer hegðunin eftir því hvort úthlutað númeraröð er stillt til að leyfa handvirka innslátt:

- Ef handvirk færsla er virkjuð er ný færsla búin til sem notar samþykkt gildi.
- Ef handvirk færslu er ekki virkjuð er næsta númer í úthlutaðri númeraröðinni notað í stað gildisins sem hefur verið samþykkt.

Meðan á innflutningslotunni stendur er staðgengilsgildinu sem er flutt inn sem folio-auðkenni haldið eftir. Þessi hegðun tryggir að siglingalínur sem vísa til staðgengils séu rétt tengdar og að þær séu uppfærðar til að endurspegla gildið sem er úthlutað úr númeraröðinni.

### <a name="field-validations"></a>Staðfestingar á vettvangi

The **Vörulýsing** reit í folio töflunni (`ITMFolioTable`) er staðfest á móti samnefndri uppsetningartöflu Landed cost. Flutningsmaður getur notað`ITMGoodsDescriptionEntity` Landað kostnaðargagnaeining til að lesa núverandi gildi og tryggja að gild gildi berist í umhverfi þínu.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Ferðalínur fyrir innkaupapantanir (ITMPurchaseLineEntity)

Ferðalínan táknar eina innkaupapöntunarlínu sem er innifalin í ferðinni. Þetta samband er komið á í gegnum **Innkaupapöntunarnúmer** og **Innkaupalínunúmer** sviðum. Ferðalínan vísar í hverja fyrri skrá sem var búin til fyrir ferðina, flutningsgáminn og blaðið. Þessi virkni er studd af`ITMPurchaseLineEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Gjaldmiðill | ITMLine.CurrencyCode | Nvarchar(3) | Nr. | Nr. |
| Nettóupphæð | ITMLine.LineAmountMST | Númeric(32, 6) | Nr. | Nr. |
| Innkaupalínunúmer | ITMLine.RefRecId | Númeric(32, 6) | **Já** | Nr. |
| Gámur | ITMLine.ShipContainerId | Int | Nr. | Nr. |
| Fyrirtæki | ITMLine.ShipDataArea | Nvarchar (20) | **Já** | Nr. |
| Uppgefið magn | ITMline.ShipDeclaredQty | Nvarchar(4) | Nr. | Nr. |
| Fólíó | ITMLine.ShipFolioId | Númeric(32, 6) | Nr. | Nr. |
| Ferð | ITMLine.ShipId | Nvarchar (20) | **Já** | Nr. |
| Vörunúmer | ITMLine.ShipItemId | Nvarchar (20) | Nr. | Nr. |
| Mæling | ITMLine.ShipMeasurement | Nvarchar (20) | Nr. | Nr. |
| Mælieining | ITMLine.ShipMeasurementUnit | Númeric(32, 6) | Nr. | Nr. |
| Fjöldi kassa | ITMLine.ShipNoOfCartons | Int | Nr. | Nr. |
| Staða | ITMLine.ShipPosition | Númeric(32, 6) | Nr. | Nr. |
| Magn | ITMLine.ShipQty | Int | Nr. | Nr. |
| Innkaupapöntunarnúmer | ITMLine.TransRefId | Númeric(32, 6) | **Já** | Nr. |
| Eining | ITMLine.UnitId | Int | Nr. | Nr. |
| Rúmmál | ITMLine.Volume | Nvarchar(10) | Nr. | Nr. |
| Vægi | ITMLine.Þyngd | Númeric(32, 6) | Nr. | Nr. |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Ferðalínur fyrir millifærslupantanir (ITMTransferLineEntity)

Ferðalínan táknar eina flutningspöntunarlínu sem er innifalin í ferðinni. Þetta samband er komið á í gegnum **Flytja pöntunarnúmer** og **Flytja línunúmer** sviðum. Ferðalínan vísar í hverja fyrri skrá sem var búin til fyrir ferðina, flutningsgáminn og blaðið. Þessi virkni er studd af`ITMTransferLineEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Gjaldmiðill | ITMLine.CurrencyCode | Nvarchar(3) | Nr. | Nr. |
| Nettóupphæð | ITMLine.LineAmountMST | Númeric(32, 6) | Nr. | Nr. |
| Gámur | ITMLine.ShipContainerId | Int | Nr. | Nr. |
| Fyrirtæki | ITMLine.ShipDataArea | Nvarchar (20) | **Já** | Nr. |
| Uppgefið magn | ITMline.ShipDeclaredQty | Nvarchar(4) | Nr. | Nr. |
| Fólíó | ITMLine.ShipFolioId | Númeric(32, 6) | Nr. | Nr. |
| Ferð | ITMLine.ShipId | Nvarchar (20) | **Já** | Nr. |
| Vörunúmer | ITMLine.ShipItemId | Nvarchar (20) | Nr. | Nr. |
| Mæling | ITMLine.ShipMeasurement | Nvarchar (20) | Nr. | Nr. |
| Mælieining | ITMLine.ShipMeasurementUnit | Númeric(32, 6) | Nr. | Nr. |
| Fjöldi kassa | ITMLine.ShipNoOfCartons | Int | Nr. | Nr. |
| Staða | ITMLine.ShipPosition | Númeric(32, 6) | Nr. | Nr. |
| Magn | ITMLine.ShipQty | Int | Nr. | Nr. |
| Númer flutningslínu | ITMLine.TransferLineNumber | Númeric(32, 6) | **Já** | Nr. |
| Flutningspöntunarnúmer | ITMLine.TransRefId | Númeric(32, 6) | **Já** | Nr. |
| Eining | ITMLine.UnitId | Int | Nr. | Nr. |
| Rúmmál | ITMLine.Volume | Nvarchar(10) | Nr. | Nr. |
| Vægi | ITMLine.Þyngd | Númeric(32, 6) | Nr. | Nr. |

### <a name="reference-table"></a>Tilvísanatafla

Ferðalínur eru búnar til í gegnum tengingu við opna pöntunarlínu á heimleið. Þessi lína getur verið á innkaupapöntun, eða hún getur verið móttökufærsla á millifærslupöntun. The`RefTableId` reit í töflunni fyrir siglingalínu (`ITMLine`) tilgreinir hvaða pöntunartegund línan tengist með því að vísa í töflunúmerið. Ef vísað er til ákveðinna töflunúmera í töflunni þar sem verið er að búa til gögnin er einingunum skipt út frá þeim gildum.

Gildin fyrir viðmiðunartöfluna (`RefTableId`) og viðskiptategund (`TransType`) eru óbein í vali á annaðhvort landaða kostnaðarkaupalínueiningunni eða landaða kostnaðartilfærslulínueiningunni.

### <a name="validation"></a>Villuleit

Ferðalína vísar beint til ferðaskrár, flutningsgámaskrár og folioskrá. Ef innkaupalínueiningin (`ITMPurchaseLinesEntity`) eða flutningslínueining (`ITMPurchaseLinesEntity`) er notað óháð einingunum sem eru notaðar til að búa til þessar tilvísunarskrár, the **Ferðaskilríki** (`ShipId`), **·** (`ShipContainerId`), og **Folio** (`ShipFolioId`) gildi verða að passa við núverandi færslu í samsvarandi töflum. Annars mun innflutningurinn mistakast.

Ef önnur hvor línueiningin er notuð sem hluti af sömu innflutningslotunni verða þessir aðrir aðilar að fara á undan stofnun ferðalínu. Annars er ekki hægt að staðfesta gildin. Ef staðgengilsgildi er notað fyrir ferðina eða folionúmerið er aðeins hægt að stofna sambandið ef sami staðgengill er notaður fyrir ferðina eða folionúmerið í ferðalínueiningunni.

Ef innkaupapöntun eða flutningspöntunarlína er þegar úthlutað á núverandi ferðalínu, verður nýja ferðalínan ekki búin til. Áður en hægt er að úthluta pöntunarlínunni í nýja ferð þarf að fjarlægja hana úr núverandi ferð.

### <a name="order-line-identification"></a>Auðkenning pöntunarlínu

Ferðalínur vísa beint til tilvísunarinnar **Skrá auðkenni** (`RefRecId`), **auðkenni** (`InventDimId`), og **Birgðafærslukenni** (`InventTransId`) gildi. Þessi gildi þurfa ekki lengur að vera með þegar gagnaeiningin er notuð. Þess í stað þarf nú að fylgja pöntunarlínunúmerinu. Saman gera pöntunarlínunúmerið og pöntunarnúmerið kleift að auðkenna hvert þessara viðmiðunargilda.

### <a name="voyage-line-quantity"></a>Magn ferðalínu

Vegna þess að ferðalína er beintengd pöntunarlínu, er **Magn** (`ShipQty`) gildi sem er slegið inn með því að nota eininguna krefst þess að gildin passi. Staðfesting er keyrð á móti magninu á annað hvort innkaupapöntunarlínunni eða millifærslulínunni. Ef staðfesting mistekst verður skráningin ekki unnin.

### <a name="calculated-fields"></a>Reiknuð svæði

The **Þyngd** og **Bindi** reiknaðir reitir taka við gildunum sem berast í gegnum gagnaeininguna. Ef engin gildi eru gefin upp eru kerfisgildin notuð til að uppfæra þessa reiti, ef kerfisgildi eru tiltæk. Fyrir landaðan kostnað eru gildin reiknuð á eftirfarandi hátt:

- *Þyngd* = *Magn* ×*Heildarþyngd vöru*
- *Bindi* = *Magn* × (*Brúttó dýpt* ×*Heildarhæð vöru* ×*Heildarbreidd vöru*)

## <a name="sequencing"></a>Röðun

Vegna ósjálfstæðis á milli taflna verður að búa til ferðina fyrst. Aðeins er hægt að búa til ferðalínuna eftir að ferðin, flutningsgámurinn og blöðin hafa verið búin til.

Til að búa til ferð án staðfestingarviðvarana verður kerfið að vinna úr einingunum í eftirfarandi röð:

1. Ferðir (`ITMTableEntity`)
1. Sendingargámar (`ITMContainersEntity`)
1. Folios (`ITMFolioTableEntity`)
1. Ferðalínur (`ITMPurchaseLinesEntity` eða`ITMTransferLinesEntity`)
