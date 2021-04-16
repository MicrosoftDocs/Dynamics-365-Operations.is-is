---
title: Birgðir til ráðstöfunar í tvíritun
description: Í þessu efnisatriði eru veittar upplýsingar um hvernig skuli athuga birgðir til ráðstöfunar í tvíritun.
author: yijialuan
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 9d9b7970720218fbcf2f512345ade672810440b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748566"
---
# <a name="inventory-availability-in-dual-write"></a>Birgðir til ráðstöfunar í tvíritun

[!include [banner](../../includes/banner.md)]

Með því að nota birgðaframboð er hægt að athuga birgðirnar áður en afurð er bætt við síðuna **Tilboð**, **Pantanir** eða **Reikningar** í Microsoft Dynamics 365 Sales. Til dæmis eru birgðir athugaðar og uppfyllingardagsetning ákvörðuð sem eitt lykilverk í ferlinu [prospect-to-cash](dual-write-prospect-to-cash.md).

Ef ekki eru til nægar birgðir er hægt að áætla afhendingardagsetningu sem byggist á áætlaðri birgðamóttöku og vandamálum. Einnig er hægt að skoða „hægt að lofa“ upplýsingar um afurðina þar sem hægt er að finna „hægt að lofa“-magnið innan fyrirfram skilgreindra tímamarka.

## <a name="on-hand-inventory"></a>Lagerbirgðir

Í Dynamics 365 Sales hefur verið bætt nýjum **Lagerbirgðir** hnapp við hausinn á síðunum **Tilboð**, **Pantanir** og **Reikningar**. Þegar þessi hnappur er valinn birtist svargluggi þar sem hægt er að tilgreina fyrirtækið og afurðina sem athuga á lagerbirgðir á. Þessi gluggi sýnir sömu upplýsingar og [Lagerbirgðir](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Glugginn skilar birgðaupplýsingum úr Dynamics 365 Supply Chain Management. Þessar upplýsingar innihalda eftirfarandi magn:

- Lagerbirgðir
- Frátekið magn á lager
- Tiltækt magn á lager
- Pantað magn
- Magn í pöntun
- Frátekið pantað magn
- Heildarmagn tiltækt

## <a name="atp-information"></a>ATP-upplýsingar

Í Sales hefur nýjum hnappi **ATP-upplýsinga** verið bætt við vörulínur á síðunum **Tilboð**, **Pantanir** og **Reikningar**. Þegar þessi hnappur er valinn birtist svargluggi þar sem hægt er að tilgreina fyrirtækið, afurðina, birgðasvæðið, vöruhúsið og pöntunarmagnið. Þessi gluggi hefur sömu stillingarnar og lýst er í [Pöntun lofað](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Glugginn skilar ATP upplýsingum frá Supply Chain Management. Þessar upplýsingar innihalda eftirfarandi magn:

- ATP-magn
- Magn innhreyfingar
- Magn úthreyfingar
- Lagerbirgðir

## <a name="how-it-works"></a>Hvernig það virkar

Þegar hnappurinn **Lagerbirgðir** er valinn á síðunni **Tilboð**, **Pantanir** eða **Reikningar** er sjálfkrafa komið á tengingu við API fyrir **Lagerbirgðir**. API reiknar lagerbirgðir fyrir viðkomandi afurð. Niðurstaðan er geymd í töflunum **InventCDSInventoryOnHandRequestEntity** og **InventCDSInventoryOnHandEntryEntity** og er svo skrifuð í Dataverse með tvöfaldri skráningu. Til að nota þessa virkni þarf að keyra eftirfarandi kort með tvöfaldri skráningu. Sleppa upphaflegri samstillingu þegar kortin eru keyrð.

- Lagerbirgðafærslur CDS-birgða (msdyn_inventoryonhandentries)
- Beiðnir um lager CDS-birgða (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Sniðmát
Eftirfarandi sniðmát eru í boði fyrir birgðagögn á lager.

Finance and Operations-smáforrit | Forrit viðskiptavinatengsla | lýsing 
---|---|---
[Lagerbirgðafærslur CDS-birgða](#145) | msdyn_inventoryonhandentries |
[Beiðnir um lager CDS-birgða](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>Lagerbirgðafærslur CDS-birgða (msdyn_inventoryonhandentries)

Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Dataverse.

Svæði í Finance and Operations | Gerð vörpunar | Reitur viðskiptavinatengsla | Sjálfgildi
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>Beiðnir um lager CDS-birgða (msdyn_inventoryonhandrequests)

Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Dataverse.

Svæði í Finance and Operations | Gerð vörpunar | Reitur viðskiptavinatengsla | Sjálfgildi
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]