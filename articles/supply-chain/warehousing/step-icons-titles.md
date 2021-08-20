---
title: Úthluta skrefatáknum og titlum fyrir Warehouse Management farsímaforritið
description: Í þessu efnisatriði er því lýst hvernig á að úthluta skrefatáknum og titlum fyrir ný eða sérstillt verkflæði fyrir Warehouse Management farsímaforritið.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: d1d595e7f8ae3cf344c891844845738a4592328eecc326f11e9a2aa0e303785a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733349"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Úthluta skrefatáknum og titlum fyrir Warehouse Management farsímaforritið

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er því lýst hvernig á að úthluta skrefatáknum og skrefatitlum fyrir ný eða sérstillt verkflæði fyrir Warehouse Management farsímaforritið.

Eftirfarandi mynd sýnir hvernig skrefatákn og titlar birtast í Warehouse Management farsímaforritinu.

![Dæmi um skrefatákn og skrefatitil í farsímaforriti Warehouse Management.](media/step-icon-example.png "Dæmi um skrefatákn og skrefatitil í Warehouse Management farsímaforritinu")

## <a name="turn-on-this-feature-in-your-system"></a>Kveikja á þessum eiginleika í kerfinu

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Notandastillingar, tákn og titlar skrefa fyrir nýja vöruhúsaforritið*

## <a name="standard-step-ids-classes-and-icons"></a>Stöðluð kenni, klasar og tákn skrefa

Hvert skref í verkflæði er auðkennt með skrefakenni og hvert skrefakenni er með samsvarandi skrefaklasa. Tákn og titill skrefsins eru tilgreind í hverjum skrefaklasa.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>Skrefakenni og skrefaklasar

Eftirfarandi tafla sýnir hvert skrefakenni sem er í boði eins og er og samsvarandi skrefaklasa. Stýringarheiti aðalfærslureitsins er notað sem skrefakennið.

Fyrir dæmi sem sýnir hvernig þessi skrefakenni og -klasar eru notuð skal sjá innleiðingu `WHSMobileAppStepInfoBuilder.stepId()` aðferðarinnar í hlutanum [Dæmi: Úthluta táknum og titlum skrefa fyrir sérstillt flæði](#example) síðar í þessu efnisatriði.

| Kenni skrefs | Klasi skrefs |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| Flutningsaðili | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| Staðfesting | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Förgun | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| Innkaupanúmer | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| Styrkleiki | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| Frágangur | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| Magn | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| Vægi | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>Tiltæk skrefatákn

Kerfið inniheldur safn staðlaðra skrefatákna sem er einnig hægt að nota fyrir sérstilltu skrefin. Ekki er hægt að hlaða upp sérsniðnum skrefatáknum eins og er. Því þarf alltaf að velja eitt af stöðluðu skrefatáknunum.

Eftirfarandi tafla sýnir hvert staðlað skrefatákn sem er í boði sem stendur og heiti þess.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Um skrefatákn"><br>Um</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Bæta við númeraplötu eða skrefatákni atriðis"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Skrefatákn ráðstöfunarrunu"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Skrefatákn flutningsaðila"><br>Flutningsaðili</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Skrefatákn framleiðsluþyngdarmerkis"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Skrefatákn þyngdarmerkingar framleiðsluþyngdar"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Skrefatákn vartölu"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Skrefatákn inn- eða útskráningarkennis"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Skrefatákn undireiningar númeraplötu"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Skrefatákn klasakennis"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Skrefatákn klasastaðsetningar"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Skrefatákn skilgreiningarkennis"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Skrefatákn skilgreinds reits"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Skrefatákn gáms eða númeraplötu"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Skrefatákn sameiningar frá númeraplötukenni"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Skrefatákn sameiningar til númeraplötukennis"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Skrefatákn gámagerðar"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Skrefatákn talningar"><br>Talning</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Skrefatákn ástæðukóða talningar"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Skrefatákn kóða upprunalands"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Skrefatákn förgunar"><br>Förgun</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Skrefatákn lokaskrefs"><br>Lokið</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Skrefatákn staðfestingar á innskráningu ökumanns"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Skrefatákn innskráningarkennis ökumanns"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Skrefatákn útskráningarkennis ökumanns"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Skrefatákn lokadagsetningar"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Skrefatákn svæðis"><br>Svæði</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Skrefatákn frá ráðstöfunarrunu"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Skrefatákn frá birgðastöðu"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Skrefatákn eigindarkennis"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Skrefatákn birgðarrunukennis"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Skrefatákn litakennis birgða"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Skrefatákn birgðastaðsetningar"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Skrefatákn raðnúmerakennis birgða"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Skrefatákn stærðarkennis birgða"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Skrefatákn birgðastöðukennis"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Skrefatákn birgðastílkennis"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Skrefatákn útgáfukennis birgða"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Skrefatákn vörukennis"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Skrefatákn ITM-gáms"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Skrefatákn ITM-sendingarkennis"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Skrefatákn kanban-spjaldkennis"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Skrefatákn kanban- eða spjaldkennis"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Skrefatákn númeraplötukennis"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Skrefatákn hleðslukennis"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Skrefatákn númeraplötustaðsetningar"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Skrefatákn staðsetningar eða númeraplötu"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Skrefatákn athugunar staðsetningar eða númeraplötu"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Skrefatákn staðsetningar eða númeraplötu frá"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Skrefatákn staðsetningar eða númeraplötu til"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Skrefatákn langs ferlis lokið"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Skrefatákn sundurliðunar á yfirnúmeraplötu"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Skrefatákn sameiningar gámakennis"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Skrefatákn línunúmers blandaðrar númeraplötu"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Skrefatákn þyngdar á útleið"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Skrefatákn eiganda"><br>Eigandi</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Skrefatákn yfirnúmeraplötu"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Skrefatákn staðfestingar"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Skrefatákn innkaupapöntunarlínunúmers"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Skrefatákn innkaupapöntunarnúmers"><br>Innkaupanúmer</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Skrefatákn fullrar staðsetningar"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Skrefatákn styrkleika"><br>Styrkleiki</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Skrefatákn prentaraheitis"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Skrefatákn framleiðslukennis"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Skrefatákn afurðarstaðfestingar"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Skrefatákn frágangs"><br>Frágangur</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Skrefatákn frágangsklasakennis"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Skrefatákn magns"><br>Magn</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Skrefatákn magnleiðréttingar á innleið"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Skrefatákn of lítils magns"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Skrefatákn notkunarmagns"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Skrefatákn frágangsmagns"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Skrefatákn rýrnunarmagns"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Skrefatákn staðfestingarmagns"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Skrefatákn tilkynningar um lok vinnslu"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Skrefatákn staðsetningarkennis móttöku"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Skrefatákn gámafjarlægingar"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Skrefatákn RMA-númers"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Skrefatákn pöntunarvals"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Skrefatákn ástæðu of lítillar tiltektar"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Skrefatákn staðsetningarkennis röðunar"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Skrefatákn númeraplötukennis markmiðs"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Skrefatákn til línunúmers"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Skrefatákn til staðsetningar"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Skrefatákn til númers"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Skrefatákn til vöruhúss"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Skrefatákn farmflutningskennis"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Skrefatákn runukennis lánardrottins"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Skrefatákn kennis bylgjumerkis"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Skrefatákn magns bylgjumerkis"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Skrefatákn þyngdar"><br>Vægi</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Skrefatákn notkunarþyngdar"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Skrefatákn leiðréttingargerðar vöruhúsakerfis"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Skrefatákn móttökufráviks vöruhúsakerfis"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Skrefatákn staðsetningarkennis vöruhúsakerfis"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Skrefatákn vinnukennis"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Skrefatákn vinnukennis sem á að hætta við"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Skrefatákn númeraplötukennis vinnu"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Skrefatákn frágangsklasa fyrir númeraplötukenni vinnu"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Skrefatákn vinnuhópakennis"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Skrefatákn svæðiskennis"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Dæmi: Úthluta táknum og titlum skrefa fyrir verkflæði

Þetta dæmi útskýrir hvernig á að setja upp tákn og titla skrefa fyrir sérsniðið verkflæði. Aðstæðurnar byggjast á dæmi um sérsniðið verkflæði sem er kynnt og kannað nánar í eftirfarandi bloggfærslu: [Farsímaforrit vöruhúsakerfis sérstillt](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). Verkflæðið virkar á eftirfarandi hátt:

1. Forritið sýnir síðu sem biður starfsmann að gefa upp gámakenni (t.d. með því að skanna strikamerki).
1. Ef gámakennið er gilt opnar forritið nýja síðu sem biður starfsmanninn um þyngdina. (Ef gámakennið er ógilt er starfsmanninum vísað á fyrstu síðuna.)
1. Þegar starfsmaðurinn slær inn gilda þyngd, geymir kerfið þyngdina og flytur starfsmanninn aftur á fyrstu síðuna.

Eftirfarandi mynd sýnir þetta verkflæði.

![Skýringarmynd verkflæðis.](media/step-icons-example-task-flow.png "Skýringarmynd verkflæðis")

### <a name="create-a-step-class-for-the-container-input-page"></a>Stofna skrefaklasa fyrir innsláttarsíðu gámsins

Innsláttarsíða gámsins gerir starfsmanni kleift að skanna eða færa inn gámakenni.

![Innsláttarsíða gáms.](media/step-icons-example-container-input.png "Innsláttarsíða gáms")

Á innsláttarsíðu gámsins er stýringarheiti færslureitsins `ContainerId`. Þar sem þetta stýringarheiti er ekki í [lista yfir skrefakenni](#step-ids-classes) verður ekki hægt að finna fyrirliggjandi skref sem byggir á því. Því þarf að stofna skrefaklasa sem stendur fyrir skrefið. Eftirfarandi er dæmi.

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

Kennimerki skrefatáknsins er geymt í `defaultStepIcon` klasameðlimnum og titill skrefsins er geymt í `defaultStepTitle` klasameðlimnum.

Til að úthluta skrefatákni skal stilla `defaultStepIcon` á eitt af kennum táknsins sem eru sýnd í hlutanum [Tiltæk skrefatákn](#step-icons) fyrr í þessu efnisatriði.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Nota staðlað eða sérstillt tákn og titil skrefs fyrir innslátt þyngdar

Innsláttarsíða þyngdar gerir starfsmanni kleift að slá inn þyngd.

![Innsláttarsíða þyngdar.](media/step-icons-example-weight-input.png "Innsláttarsíða þyngdar")

Á innsláttarsíðu þyngdar er stýringarheiti færslureitsins `Weight`, sem er í [listanum yfir skrefakenni](#step-ids-classes). Þar af leiðandi þarf ekki að breyta neinu fyrir þetta skref ef tákn og titill skrefsins sem eru skilgreind í `WHSMobileAppStepWeight` klasanum reynast í lagi.

Ef hinsvegar kosið er að nota annað tákn eða titil fyrir þetta skref er hægt að hnekkja annaðhvort `stepId()` aðferðinni eða `stepInfo()` aðferðinni í smiðsklasanum. Hvert verkflæði er með sinn eigin smið skrefaupplýsinga.

#### <a name="override-the-stepid-method"></a>Hnekkja stepId() aðferðinni

Eftirfarandi dæmi sýnir eina leið sem til að breyta smiðsklasa með því að hnekkja `stepId()` aðferðinni.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

Þú býrð svo til skrefflokk fyrir `NewWeight` skrefið. Kóðinn ætti að líkjast kóðanum fyrir `ContainerId` dæmið sem sýnt var fyrr í þessu efnisatriði.

#### <a name="override-the-stepinfo-method"></a>Hnekkja stepInfo() aðferðinni

Eftirfarandi dæmi sýnir eina leið sem til að breyta smiðsklasa með því að hnekkja `stepInfo()` aðferðinni.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

Þú smíðar síðan `WHSMobileAppStepInfo` hlut og stillir táknið og/eða titilinn beint.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Setja upp og tengja farsímaforrit vöruhúsakerfis](install-configure-warehouse-management-app.md)
- [Notandastillingar fartækis](mobile-device-user-settings.md)
