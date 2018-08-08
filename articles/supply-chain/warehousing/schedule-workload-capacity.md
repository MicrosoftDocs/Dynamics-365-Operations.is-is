---
title: "Tímasetja afkastagetu vinnuálags"
description: "Í þessu efnisatriði er útskýrt hvernig á að setja upp og raða vinnuálagsgetu starfsfólks í vöruhúsi eða fyrir heilt vöruhús."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69b9c5590e6f9311696bbbed2e63a6eeba2a90bf
ms.openlocfilehash: 1b93cfaf098b4cff3e72ee9bb599eadfdac2a9b9
ms.contentlocale: is-is
ms.lasthandoff: 05/03/2018

---

# <a name="schedule-workload-capacity"></a>Tímasetja afkastagetu vinnuálags

[!include[banner](../includes/banner.md)]

Hægt er að spá fyrir um vinnuálagsgetu fyrir vöruhús og einnig er hægt að spá fyrir um núverandi og framtíðarvinnuálag fyrir starfsfólkið í einstökum vöruhúsum. Hægt er að spá fyrir um vinnuálag fyrir allt vöruhúsið eða spá fyrir um vinnuálagið aðskilið fyrir vinnuálag bæði á innleið og útleið.

Til að spá fyrir um vinnuálagsframleiðslu fyrir valin vöruhús, verða gögn aðalröðunar að vera tiltæk fyrir þessi vöruhús. Fyrir frekari upplýsingar, sjá [Aðaláætlanir](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Raða og skoða vinnuálag fyrir vöruhús

Til að raða vinnuálagsgetu fyrir vöruhús er stofnuð uppsetning vinnuálags fyrir eitt eða fleiri vöruhús og uppsetningin svo tengd við aðaláætlunina. Í uppsetningu vinnuálagsgetu geturðu skilgreint mörk fyrir þyngd eða rúmmál fyrir færslur á inn- og útleið. Þú getur einnig búið til fleiri en eina uppsetningu fyrir hvert vöruhús og síðan tengt uppsetninguna við einstakar aðaláætlanir. Til dæmis gætirðu notað þessa aðferð til að mæta árstíðabundnum breytingum á vinnuafli.

Ef starfsfólk í vöruhúsi vinnur með færslur fyrir vinnuálag bæði á inn- og útleið getur þú stillt uppsetningu á afkastagetu vöruhúss þannig að vinnuálaginu er varpað í sameiginlegt yfirlit.

Til að tímasetja og skoða vinnuálag fyrir vöruhús verður þú að ljúka eftirfarandi verkum:

1. Stofna uppsetningu á afkastagetu vinnuálags og skilgreina mörk afkastagetu vinnuálags fyrir eitt eða fleiri vöruhús.
2. Tengja uppsetningu á afkastagetu vinnuálags við aðaláætlun til að búa til áætlun vinnuálags og tilgreina hversu lengi þessar áætlanir eiga við.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Búa til uppsetningu á afkastagetu vinnuálags fyrir vöruhús

1. Veldu **Birgðastjórnun** \> **Uppsetning** \> **Vöktun vöruhúss** \> **Afkastageta vinnuálags**.
2. Í aðgerðarglugganum skal velja **Nýtt** til að búa til uppsetningu á afkastagetu vinnuálags.
3. Á flýtiflipanum **Vöruhús** skal velja **Nýtt** og slá síðan inn gildi á línunni til að tengja vöruhúsi uppsetningu á afkastagetu vinnuálags.
4. Veldu gátreitinn **Sameinað vinnuálag fyrir inn- og útleið** ef skýrslan **Afkastageta vinnuálags** skyldi sýna heildarvinnuálag fyrir færslur á inn- og útleið í einu yfirliti.
5. Á flýtiflipanum **Færslugerðir** skal velja gerðir af færslum á inn- og útleið sem mörk vinnuálags eiga við um.

    > [!NOTE]
    > Þú verður að velja að minnsta kosti eina færslugerð fyrir bæði vinnuálag á inn- og útleið.

#### <a name="define-limits-for-volume-or-weight"></a>Skilgreina mörk fyrir rúmmál eða þyngd

Þú getur sett upp mörk fyrir rúmmál eða þyngd, fer eftir takmörkuninni sem á við um mannafla vöruhússins. Mörkin sem þú tilgreinir eru tekin með í áætlun á afkastagetu vinnuálags sem hægt er að skoða í skýrslunni **Afkastageta vinnuálags**.

Til að spá fyrir um upplýsingar varðandi rúmmál og þyngd á vörum, verður að tilgreina staðalrúmmál og þyngd á einni birgðavöru fyrir allar afurðir. Nauðsynlegir reitir eru í boði í eftirfarandi reitaflokkum á flýtiflipanum **Stjórna birgðum** á síðunni **Upplýsingar um losaðar afurðir**:

- Afgreiðsla
- Efnislegar víddir
- Vægi mælinga

Ef þessar upplýsingar eru ekki tilgreindar á réttan hátt, færðu skilaboð þegar þú býrð til skýrsluna **Afkastageta vinnuálags**. Frá skýrslunni er hægt að bora niður til að bera kennsl á upplýsingar sem vantar sem þarf til að geta spáð fyrir um framtíðarvinnuálag.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Tengja uppsetningu á afkastagetu vinnuálags við aðaláætlun

1. Veldu **Birgðastjórnun** \> **Reglubundin** \> **Raða vinnuálagi**.
2. Í reitnum **Aðaláætlun** skal velja aðaláætlun til að nota fyrir áætlanir um vinnuálag.
3. Í reitnum **Fjöldi daga** skal tilgreina fjölda daga sem áætlun vinnuálags nær yfir.
4. Í reitnum **Vinnuálag** skal velja uppsetningu vinnuálags sem tengja á við aðaláætlun.

### <a name="view-workload-capacity"></a>Skoða afkastagetu vinnuálags

1. Veldu **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Efnislegar birgðarskýrslur** \> **Afkastageta vinnuálags**.
2. Í reitnum **Fjöldi dálka** skal tilgreina fjölda dálka sem birta á í skýrslunni.
3. Í reitnum **Gerð pöntunar** skal velja **Áætlað og staðfest**, **Áætlað** eða **Staðfest** til að tilgreina gerð pantana sem á að spá fyrir í skýrslunni.
4. Í reitnum **Álagsgerðir** skal velja álagsgerð til að tilgreina hvort spá ætti fyrir um afkastagetu vinnuálags fyrir rúmmál og þyngd.
5. Í reitnum **Afkastageta vinnuálags** skal velja uppsetningu á afkastagetu vinnuálags.

