---
title: "Tímasetja álagsnýtingu"
description: "Í þessu efnisatriði er útskýrt hvernig á að setja upp og tímasetja álag fyrir vöruhús."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d52ad452c615a61739582431fcd100a7efa3d93a
ms.openlocfilehash: 350666cee8f2643c53e9eed8ee73299bbea1e757
ms.contentlocale: is-is
ms.lasthandoff: 04/26/2018

---

# <a name="schedule-load-utilization"></a>Tímasetja álagsnýtingu

[!include[banner](../includes/banner.md)]

Þú getur tímasett álagsnýtingu fyrir valdar gerðir staðsetninga og þú getur einnig gert ráð fyrir núverandi og framtíðarálagsnýtingu. Þú getur áætlað álagið fyrir eitt eða fleiri svæði, fyrir álagseiningarnar (svæði eða vöruhús) eða fyrir samsetningu af svæði og vöruhúsi.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>Raða og skoða álag fyrir vöruhús eða staðsetningu

Til að raða álaginu fyrir svæði, vöruhús, eða staði er búin til uppsetning plássnotkunar og hún tengd aðaláætlun.

Í uppsetningu plássnotkunar notarðu gerðir staðsetninga, t.d. **Magnstaðsetning** og **Tínslustaður** til að tilgreina hvernig eigi að áætla plássnotkun. Þú tilgreinir einnig geymsluálagsstillingu, eins og **Svæði**.

Vörpun framvirkrar plássnotkunar er grundvöllum á upplýsingum sem eru reiknaðar samkvæmt tengdri aðaláætlun. Aðaláætlanir spá fyrir forðaáætlun fyrir pantanir á innleið og útleið fyrir framleiðslu og aðgerðir. Vörpun tiltæks pláss er grundvölluð á sambandinu á milli uppsetningar plássnotkunar og valinnar aðaláætlunar.

Með því að nota geymsluálagsstillinguna sem þú valdir í uppsetningu plássnotkunar, getur þú tilgreint hvort álagið skuli áætlað fyrir hvert vöruhús eða svæði, eða hvort áætlanirnar ætti að innihalda upplýsingar um bæði vöruhús og svæði. Þú tilgreinir einnig hvort staðsetningar sem lokað hefur verið á verði ekki teknar með í útreikningi á álagsnýtingu.

Þú getur spáð fyrir um plássnotkun með því að búa til skýrsluna **Álagsnýting í vöruhúsi**. Þegar þú býrð til þessa skýrslu er hægt að tilgreina hvort álagsnýtingin eigi að vera áætluð fyrir hvert svæði eða fyrir valda álagseiningu, t.d. svæði eða vöruhús.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Búa til uppsetningu plássnotkunar fyrir vöruhús

1. Veldu **Birgðastjórnun** \> **Uppsetning** \> **Vöktun vöruhúss** \> **Plássnotkun**.
2. Veldu **Nýtt** til að búa til uppsetningu plássnotkunar. Tilgreindu auðkenni og heiti fyrir nýju uppsetninguna.
3. Í reitnum **Geymsluálagsstilling** skal velja hvort yfirlit plássnotkunar eigi að sýna upplýsingar eftir vöruhúsi, svæði eða vöruhúsi og svæði.
4. Stilltu valkostinn **Ekki taka með útilokaðar staðsetningar** á **Já** til að taka birgðastaðsetningar sem hefur verið lokað á ekki með í útreikninginn á tiltæku plássi. Þú getur lokað á birgðastaðsetningu fyrir inntak og úttak með því að tilgreina ástæðu útilokunar fyrir staðsetninguna í reitunum **Inntak útilokað** eða **Úttak útilokað** á flýtiflipanum **Annað** á síðunni **Birgðastaðsetningar**.
5. Á flýtiflipanum **Gerð staðsetningar** skaltu velja gerðir staðsetninga sem eru teknar með í útreikningi á plássnotkun. Velja verður í það minnsta eina staðsetningargerð fyrir spána.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Tengja uppsetningu plássnotkunar við aðaláætlun

1. Veldu **Birgðastjórnun** \> **Reglubundin verkefni** \> **Tímasetja álagsnýtingu**.
2. Í reitnum **Aðaláætlun** skal velja aðaláætlun.
3. Í reitnum **Fjöldi daga** skal tilgreina fjölda daga sem á að hafa með í áætlun á núverandi og framtíðarvinnuálagi.
4. Í reitnum **Plássnotkun** skal velja uppsetningu plássnotkunar til að nota fyrir áætlun á núverandi og framtíðarvinnuálagi.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>Tilgreina spá fyrir álagsnýtingu og skoða upplýsingar

1. Veldu **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Efnislegar birgðarskýrslur** \> **Álagsnýting í vöruhúsi**.
2. Í reitnum **Sýna eftir** skaltu velja stig áætlunar á plássnotkun:

    - **Svæði** - Spá fyrir um plássnotkun fyrir hvert svæði. Þessi spá er gagnleg, til dæmis ef skoða á öll vöruhús fyrir svæði þannig að hægt sé að jafna plássnotkun á milli vöruhúsa.
    - **Álagseining** - Spá fyrir um plássnotkun fyrir svæði eða vöruhús. Laust pláss er síðan áætlað í samræmi við gildið sem þú valdir í reitnum **Geymsluálagsstilling** á síðunni **Plássnotkun** þegar þú bjóst til uppsetningu plássnotkunar.

3. Fylgdu einu af þessum skrefum, fer eftir gildinu sem þú valdir í fyrra skrefi:

    - Ef þú hefur valið **Svæði** í reitnum **Sýna eftir** er reiturinn **Svæði** tiltækur. Veldu eitt eða fleiri svæði til að hafa með í spánni.
    - Ef þú valdir **Álagseining** í reitnum **Sýna eftir** er reiturinn **Álagseining** tiltækur. Veldu álagseininguna.

4. Í reitnum **Álagsgerð** skaltu velja **Rúmmál** eða **Þyngd** til að tilgreina rekstrareiningu vöruhússins fyrir áætlun á plássi.
5. Í reitnum **Uppsetning plássnotkunar** skal velja uppsetningu plássnotkunar sem spáin á að byggjast á.

