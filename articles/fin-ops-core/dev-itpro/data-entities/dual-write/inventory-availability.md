---
title: Birgðir til ráðstöfunar í tvíritun
description: Í þessari grein eru veittar upplýsingar um hvernig skuli athuga birgðir til ráðstöfunar í tvíritun.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 442486550d3a7c5132e26f663caaa7c2c02eeb6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289209"
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

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla     | lýsing
---|---|---
[Lagerbirgðafærslur CDS-birgða](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[Beiðnir um lager CDS-birgða](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
