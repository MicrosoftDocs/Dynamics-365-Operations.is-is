---
title: Birgðir til ráðstöfunar í tvíritun
description: Í þessu efnisatriði eru veittar upplýsingar um hvernig skuli athuga birgðir til ráðstöfunar í tvíritun.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443873"
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
