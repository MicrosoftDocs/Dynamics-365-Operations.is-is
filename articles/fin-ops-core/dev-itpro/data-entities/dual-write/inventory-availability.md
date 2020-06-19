---
title: Birgðir til ráðstöfunar í tvíritun
description: Í þessu efnisatriði eru veittar upplýsingar um athugun á birgðaframboði í tvíritun.
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
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426983"
---
# <a name="inventory-availability"></a>Birgðir til ráðstöfunar

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Með því að nota birgðir til ráðstöfunar er hægt að skoða birgðirnar áður en afurð er bætt við skjámyndirnar **Tilboð**, **Pantanir** eða **Reikningar** í líkanadrifnum forritum í Dynamics 365. Birgðaskoðun og ákvörðun á uppfyllingardagsetningu er til dæmis lykilþáttur í ferlinu [prospect-to-cash](dual-write-prospect-to-cash.md). Ef ekki eru til nægar birgðir er hægt að áætla afhendingardagsetningu sem byggist á áætlaðri birgðamóttöku og vandamálum. Einnig er hægt að skoða „hægt að lofa“ upplýsingar um afurðina þar sem hægt er að finna „hægt að lofa“-magnið innan fyrirfram skilgreindra tímamarka.

## <a name="on-hand-inventory"></a>Lagervörur 

Efst á skjámyndunum **Tilboð**, **Pantanir** eða **Reikningar** í Dynamics 365 Sales er nýjum hnapp **Lagerbirgðir** bætt við. Þegar smellt er á hnappinn birtist svargluggi og hægt er að tilgreina fyrirtækið og afurðina sem á að skoða lagerbirgðir fyrir. Hann skilar birgðaupplýsingum úr Dynamics 365 Supply Chain Management og sýnir sömu upplýsingar og [Lagerbirgðir](../../../../supply-chain/inventory/tasks/check-availability-stock.md). Upplýsingarnar innihalda þetta magn:

- **Magn á lager**
- **Frátekið magn á lager**
- **Tiltækt magn á lager**
- **Pöntunarmagn**
- **Magn í pöntun**
- **Frátekið pantað magn**
- **Heildarmagn tiltækt**

## <a name="atp-information"></a>ATP-upplýsingar

Í vörulínum skjámyndanna **Tilboð**, **Pantanir** eða **Reikningar** í Dynamics 365 Sales er nýjum hnapp **ATP-upplýsingar** bætt við. Þegar smellt er á hnappinn birtist svargluggi og hægt er að tilgreina fyrirtækið, afurðina, birgðasvæðið, birgðavöruhúsið og pöntunarmagn. Hann skilar **ATP-upplýsingar** frá Supply Chain Management og birtir stillingar sem útskýrðar eru í [Pöntun lofað](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations). Upplýsingarnar innihalda **ATP-magn**, **Innhreyfingarmagn**, **Úthreyfingarmagn** og **Magn lagerbirgða**.
