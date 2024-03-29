---
title: Búa til verkefnalista og bæta við verkum
description: Þessi grein lýsir því hvernig á að búa til verkefnalista og bæta verkefnum við þá í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: b81f27f79362516f8a25766c1f663a7691ebb42a
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746160"
---
# <a name="create-task-lists-and-add-tasks"></a>Búa til verkefnalista og bæta við verkum

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til verkefnalista og bæta verkefnum við þá í Microsoft Dynamics 365 Commerce.

*Verk* skilgreinir tiltekið verk eða aðgerð sem einhver verður að ljúka á eða fyrir tiltekinn gjalddaga. Í Dynamics 365 Commerce getur verk innihaldið nákvæmar leiðbeiningar og upplýsingar um tengilið. Það getur einnig falið í sér hlekki á bakvinnsluaðgerðir, sölustaði (POS) eða vefsíður til að bæta framleiðni og veita það samhengi sem eigandi verkefna þarf til að ljúka verkinu á skilvirkan hátt.

*Verkefnalisti* er safn verkefna sem þarf að ljúka sem hluta af viðskiptaferli. Til dæmis gæti verið til verkefnalisti sem nýr starfsmaður verður að fylla út í nýliðaþjálfun, verkefnalista fyrir gjaldkera sem vinna kvöldvaktir eða verkefnalista sem verður að ljúka til að undirbúa verslunina fyrir komandi frídaga. Í Commerce er hægt að úthluta öllum verkefnalistum sem eru með dagsetningu til hvaða fjölda verslana eða starfsmanna sem er og hægt er að stilla það svo að það endurtaki sig.

Bæði stjórnendur og starfsmenn geta búið til verkefnalista í bakvinnslu Commerce og síðan úthlutað þeim í safn verslana.

## <a name="create-a-task-list"></a>Búa til verklista

Áður en þú byrjar ferlið við að búa til verkefnalista skaltu ganga úr skugga um að þú hafir lokið stillingum í [Stilla verkefnastjórnun](task-mgmt-configure.md) grein. Til að stofna verklista skal fylgja þessum skrefum.

1. Farðu í **Retail og Commerce \> Verkefnisstjórn \> Stjórnun verkefnisstjórnunar**.
1. Veldu **Nýtt** og sláðu síðan inn gildi í reitunum **Nafn**, **Lýsing** og **Eigandi**.
1. Veljið **Vista**.

## <a name="add-tasks-to-a-task-list"></a>Bættu verkefnum við verkefnalista

Til að bæta verki við verklista skaltu fylgja þessum skrefum.
 
1. Á flýtiflipanum **Verk** í fyrirliggjandi verkefnalista velurðu **Nýtt** til að bæta við verki.
1. Í valmyndinni **Stofna nýtt verk** í reitnum **Heiti** er fært inn einkvæmt heiti fyrir verkið.
1. Í reitinn **Mótfærsla gjalddaga frá markdegi** slærðu inn jákvætt eða neikvætt heiltölugildi. Til dæmis, sláðu inn **-2** ef verkefni ætti að vera lokið tveimur dögum fyrir gjalddaga verkefnalistans.
1. Í reitinn **Athugasemdir** slærðu inn nákvæmar leiðbeiningar.
1. Í reitinn **Tengiliður** slærðu inn heiti efnissérfræðings sem verkefnaeigandinn getur haft samband ef hann þarfnast hjálpar.
1. Í reitinn **Verktengill** slærðu inn tengil, samkvæmt á eðli verksins.

> [!TIP]
> Þó að þú getir notað reitinn **Úthlutað á** til að úthluta verkum á einhvers meðan þú ert að búa til verkefnalista, mælum við með að þú forðist að úthluta verkefnum meðan verkefnalistinn er búinn til. Í staðinn skaltu úthluta verkefnum þegar listinn hefur verið eintekinn fyrir stakar verslanir.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Notaðu verkefnatengla til að bæta framleiðni starfsmanna

Commerce gerir þér kleift að tengja verk við sérstakar POS-aðgerðir, eins og að keyra söluskýrslu, skoða þjálfunarmyndband á netinu fyrir nýja stefnu starfsmanna eða framkvæma bakvinnsluaðgerð. Þessi aðgerð hjálpar eigendum verkefna að fá þær upplýsingar sem þeir þurfa til að klára verkefni á skilvirkan hátt.

Fylgdu þessum skrefum til að bæta við verkefnatenglum meðan þú býrð til verkefni.

1. Á flýtiflipanum **Verk** í fyrirliggjandi verkefnalista velurðu **Breyta**.
1. Í glugganum **Breyta verki** í reitnum **Verkefnatengill** velurðu einn eða fleiri af eftirfarandi valkostum:

    - Veldu **Valmyndaratriði** til að stilla bakvinnslu, eins og „Vörusett”.
    - Veldu **POS aðgerð** til að stilla POS aðgerð, eins og „Söluskýrslur”.
    - Veldu **Vefslóð** til að stilla fasta slóð.

Eftirfarandi mynd sýnir val á verkstenglum í valmyndinni **Breyta verki**.

![Val á verktenglum í glugganum Breyta verkefni.](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>Stilltu POS-aðgerð svo hægt sé að tengja hana við verk

Til að stilla POS-aðgerð svo hægt sé að tengja hana við verk fylgirðu þessum skrefum.

1. Farðu í **Retail og Commerce \> Uppsetningu rásar \> Uppsetning POS \> POS \> POS-aðgerðir**.
1. Veldu **Breyta**, finndu POS-aðgerðina og veldu síðan gátreitinn **Virkja verkefnisstjórnun** fyrir hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit verkefnastjórnunar](task-mgmt-overview.md)

[Skilgreina verkstýringu](task-mgmt-configure.md)

[Úthluta verkefnalistum til verslana eða starfsmanna](task-mgmt-assign-lists.md)

[Verkstjórnun á sölustað](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
