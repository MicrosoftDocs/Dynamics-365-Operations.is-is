---
title: Flettingaleit
description: Flettingaleit - Þetta efnisatriði útskýrir hvernig skuli nota leitarvirknina til að fara inn á síður í Microsoft Dynamics 365 for Finance and Operations.
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c05098815c6b330cbb9c7f5ce886779927c6804
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "353012"
---
# <a name="navigation-search"></a>Flettingaleit

[!include [banner](../includes/banner.md)]

Flettingaleit - Þetta efnisatriði útskýrir hvernig skuli nota leitarvirknina til að fara inn á síður í Microsoft Dynamics 365 for Finance and Operations.

Finance and Operations veitir eiginleika fyrir breitt svið iðnaðar og framleiðslu. Forritið felur í sér fjölda svæða og síður til að hjálpa þér að framkvæma ýmis verk. Til að finna fljótt þær síður sem þú þarft til að ljúka verkefnum þínum skaltu nota eiginleikann flettingaleit.

Til að Nota þessa aðgerð þarf að smella á í **Leit** teiknið til að birta **Leit** gátreiturinn. Síðan er hægt að slá eitt eða fleiri orð í reitnum. Kerfið leitar strax að viðeigandi síðum í forritinu sem passa orð sem þú slóst inn. Til dæmis gætir þú slegið inn „reikningur lánardrottins“ sem inntak, og þá birtir kerfið niðurstöður sem passa við inntakið.

> [!NOTE]
> Reiturinn **Leit** hjálpar til við að leita og fletta að síðum. Það ekki gagnast við að finna ákveðna gögn eða aðgerðir.

[![leitargluggi](media/navigation-search.png "Leitargluggi")

## <a name="quickly-navigate-to-a-particular-page"></a>Að fara á ákveðna síðu á fljótlegan hátt

Flettingaleitareiginleikinn þjónar einnig sem frábær leið fyrir þig til að fletta fljótt á ákveðna síðu. Ef þú ert til dæmis starfsmaður viðskiptaskulda sem oft notar síðuna **Greiðslubók**, gætirðu slegið inn "greiðslubók" í reitinn **Leit**. Þar sem inntak er nákvæm samsvörun fyrir blaðsíðutitil, er síðan skráð á toppi af leitarniðurstöðum, og þú getur fljótt flett á það.

Leitarniðurstöðulistinn sýnir síðutitilinn auk flettingarleiðar. Þetta sýnir staðsetningu síðunnar í forritinu. Það hjálpar einnig til að aðgreina á milli tveggja eða fleiri svipuð síður í niðurstöðum.

Þegar þú leitar að síðu, er inntak þitt er borin saman við síðutitli, auk flettingarleiðar. Ef til dæmis er fært inn „kröfur“ í reitinn **Leita** sjást niðurstöður fyrir síður sem eru tiltækar á svæðinu fyrir viðskiptakröfur – jafnvel þótt síðutitillinn innihaldi ekki orðið „kröfur“.

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Flettið fljótt að síðu á grundvelli heitis tæknisniðs

Flettingaleitarvirkni er einnig með mikið umbeðna aðgerð fyrir lengra komna: getu til fljótt fletta á síðu á grundvelli heitis á tæknilegri skjámynd. Margir notendur eru svo kunnugir kerfinu, að þeir vita nákvæmlega nöfn skjámyndar sem þeir vinna með. Ef þú ert einn af þessum notendum má færa inn **skjámynd: (form:)** og í kjölfarið kemur heiti skjámyndarinnar sem er leitað eftir. Til dæmis, ef fært er inn **form: vendinvoice**,sýna leitarniðurstöður allar síður þar sem heiti skjámyndar byrjar **vendinvoice**.

## <a name="administration-and-security"></a>Stjórnun og öryggi

Vegna stjórnunar og öryggissjónarmiða sýnir flettingaleitareiginleikinn aðeins tvær gerðir niðurstaðna:

- Síður sem eru virkjaðir í gildandi skilgreiningu (með skilgreiningarlykla).
- Síður sem notandi hefur aðgang að byggt á hlutverki notanda.

Lista yfir leitarniðurstöður takmarkast við 10 vörur. Ef þú finnur ekki það sem þú ert að leita að í niðurstöðum, ættir þú að reyna fínstillingu eða uppfæra inntak.

## <a name="development"></a>Þróunarvalmynd

Frá þróunarsjónarhóli er flettingaleitarvirkni auðvelt að til að finna jafnvægi, þar er nánast engin töf milli uppsetningar valmyndaratriða og getu þeirra til að birtast í leitarniðurstöðum. Svo lengi sem tengt er í valmyndaratriðin annað hvort úr skoðunarrúðunni eða á yfirlitinu, verða þær sjálfkrafa finnanlegar.
