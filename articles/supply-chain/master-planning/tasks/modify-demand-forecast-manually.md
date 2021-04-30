---
title: Breyta eftirspurnarspá handvirkt
description: Í þessu efnisatriði er útskýrt hvernig á að breyta spá fyrir vöru
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889025"
---
# <a name="modify-a-demand-forecast-manually"></a>Breyta eftirspurnarspá handvirkt

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að breyta spá fyrir vöru. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætluð fyrir framleiðslustjóri

## <a name="modify-the-forecast-for-a-selected-item"></a>Breyta spá fyrir valda vöru

Til að breyta spá fyrir valið atriði:

1. Farið í **Einingar \> Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Velja vöruna sem ætlunin er að breyta spánni.
1. Á aðgerðasvæðinu skal opna flipann **Áætlun** og velja **Eftirspurnarspá**.
1. Í listanum velurðu línu. Ef það eru engar spárlínur skal stofna nýja línu með því að velja **Ný** á aðgerðasvæðinu.  
1. Í reitnum **Sölumagn** skal slá inn jákvæða tölu. Þetta númer stendur fyrir spáð magn vörunnar. Villa birtist ef neikvæð tala er færð inn.
1. Fyllið út í önnur svæði eftir þörfum.
1. Í aðgerðaglugganum velurðu **Vista**.

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a>Breyta spá fyrir eina eða fleiri vörur Microsoft Excel

Til að breyta spá fyrir eina eða fleiri vörur Microsoft Excel:

1. Gerið eitt af eftirfarandi:
    - Farið á síðuna **Eftirspurnarspá** fyrir einhverja vöru (skiptir ekki máli hvaða vöru) eins og lýst er í fyrri hlutanum.
    - Farið í **Aðaláætlanagerð \> Spá \> Handvirk spárfærsla \> Eftirspurnarspárlínur**.
1. Á aðgerðasvæðinu skal velja **Opna í Microsoft Office \> Eftirspurnarspáfærslur**.
1. Veljið niðurhalsstað, vistið og opnið síðan sótta skrá í Excel.
1. Ef viðvörun kemur upp skal velja **Virkja breytingar**.
1. Í Excel skal skrá sig inn í Supply Chain Management með því að nota Microsoft Dynamics verksvæðið. Nauðsynlegt er að skrá sig inn með valkostinn **Halda mér innskráðum** virkan og treysta verður á gagnatengingarforritið.
1. Excel-töflureiknirinn sýnir nú allar núverandi eftirspurnarspárlínur fyrir fyrirtækið.  Bætið við, eyðið og breytið eftirspurnarspárlínum eftir þörfum.
1. Veljið **Birta** á Microsoft Dynamics verksvæðinu til að hlaða breytingunum aftur upp í Supply Chain Management.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
