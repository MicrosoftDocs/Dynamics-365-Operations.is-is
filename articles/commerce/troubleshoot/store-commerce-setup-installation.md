---
title: Leysa uppsetningar- og uppsetningarvandamál í Store Commerce
description: Þessi grein útskýrir hvernig eigi að leysa uppsetningar- og uppsetningarvandamál í Microsoft Dynamics 365 Commerce Store Commerce app.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 92d4a9d78485b681b4e802f695d54f44ecd7c5de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870467"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Leysa uppsetningar- og uppsetningarvandamál í Store Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Þessi grein útskýrir hvernig eigi að leysa uppsetningar- og uppsetningarvandamál í Microsoft Dynamics 365 Commerce Store Commerce app.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Ég get ekki virkjað appið og ég fæ villuboð um tengingu

Eftir að þú slærð inn gilda slóð á skýjasölustað (CPOS) gætirðu fengið villuboð um tengingu sem líkist eftirfarandi dæmi:

> Tengingarvilla kom upp og tækið þitt getur ekki tengst CPOS. Vefslóð CPOS sem slegin er inn gæti verið vandamál.

Í þessu tilviki skaltu skoða vefslóðina fyrir prentvillur eða ákvarða hvort ekki sé hægt að ná í CPOS vegna þess að það er ótengdur.

Að auki, staðfestu að Cloud Scale Unit (CSU) útgáfan sé 10.0.25 (9.35.\* .\*) eða seinna. CPOS útgáfa 10.0.25 eða nýrri er nauðsynleg til að nota Store Commerce appið.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Ég get ekki sett upp appið vegna þess að Modern POS er þegar uppsett

Við uppsetningu gætirðu fengið villuboð eins og eftirfarandi dæmi:

> Útgáfa (9.\* .\* .\*) þessarar vöru (Modern POS) hefur áður verið sett upp í gegnum eldri uppsetningarforritið.

Til að laga villuna verður þú að fjarlægja Modern Point of Sale (MPOS) appið fyrir alla notendur vélarinnar og reyna síðan aftur. Þú getur staðfest hvort MPOS hafi verið fjarlægt fyrir alla notendur með því að keyra eftirfarandi PowerShell skipun.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Ég get ekki virkjað appið vegna ógildrar vefslóðar eða villuástands

Ef CPOS vefslóðin sem þú slóst inn er ekki gild og þú vilt breyta henni, eða ef Store Commerce appið er í villuástandi við virkjun, geturðu endurræst ferlið með því að endurstilla appið. Store Commerce appið mun aðeins vista gilda CPOS vefslóð.

Til að endurstilla Store Commerce appið skaltu fylgja þessum skrefum.

1. Á Windows **Byrjaðu** valmynd, veldu og haltu inni (eða hægrismelltu) á forritið og veldu síðan **Meira \> App stillingar**.
2. Skrunaðu niður stillingasíðuna þar til þú finnur **Endurstilla** takki.
3. Veldu **Endurstilla**. Síðan, þegar þú ert beðinn um það skaltu staðfesta að þú viljir endurstilla forritið.
