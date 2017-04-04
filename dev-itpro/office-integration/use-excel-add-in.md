---
title: "Nota í Excel-viðbótar"
description: "Í þessu efnisatriði er útskýrt hvernig opna einingagögn í Microsoft Excel og að skoða, uppfæra og breyta gögnum með því að nota í Microsoft Dynamics Office-viðbótar Excel. Til að opna einingagögn á er hægt að hefja úr Excel eða Microsoft Dynamics 365 aðgerða."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Nota í Excel-viðbótar

Í þessu efnisatriði er útskýrt hvernig opna einingagögn í Microsoft Excel og að skoða, uppfæra og breyta gögnum með því að nota í Microsoft Dynamics Office-viðbótar Excel. Til að opna einingagögn á er hægt að hefja úr Excel eða Microsoft Dynamics 365 aðgerða.

Með því að opna einingagögn í Microsoft Excel, hægt fljótlegt og auðvelt að skoða og breyta gögnum með því að nota í Microsoft Dynamics Office-viðbótar Excel. Þessi innbót krefst Microsoft Excel 2016. **Athugasemd:** Ef notanda Microsoft Azure Active Directory (Azure AD) leigjanda er skilgreindur til að nota Active Directory Samsteypuþjónusta (AD FS), þarf að tryggja sem uppfæra 2016 Getur verið notuð, þannig að í Excel-viðbótar getur rétt skráð er.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Opna einingagögn í Excel þegar frá Dynamics 365 fyrir Aðgerðir
1.  Á síðu í Microsoft Dynamics 365 fyrir Aðgerðir, smellið á **Opna í Microsoft Office**. Ef rótargagnagjafi (tafla) fyrir listasíðu er sú sama og rótargagnagjafi fyrir allar einingar sjálfgefin **Opna í Excel** valkostir eru búnar til síðan. **Opna í Excel** valkostina má finna á algengum síðum, eins og **Allir lánardrottnar** og **Allir viðskiptavinir**.
2.  Smellið á **Opna í Excel** valkosturinn og til að opna vinnubókina sem er mynduð. Þessi vinnubók hefur bindingarupplýsingar fyrir einingu, bendilinn í umhverfinu og bendilinn til í Excel-viðbótar.
3.  Í Excel, smellið á **Virkja verður breytingar** til að virkja í Excel viðbót til að keyra. Í Excel-viðbótar keyrir í rúða hægra megin í Excel-glugga.
4.  Ef verið er að keyra í Excel-viðbótar í fyrsta sinn, er smellt á **Traust þessa innbótin**.
5.  Ef afskriftareglur eru beðið til að skrá inn, smella á **innskráning**, og síðan skrá sig inn með því að nota sömu skilríki sem er notað til að skrá sig Dynamics 365 fyrir Aðgerðir. Í Excel-viðbótar verður notuð í fyrri formerki í samhengi í Internet Explorer og sjálfkrafa skrá er í, ef það er hægt. Þess vegna er staðfesta notandanafn í efra hægri horninu í Excel-viðbótar.

Í Excel-viðbótar sjálfkrafa les gögn fyrir eininguna sem er valin. Athugið að það verður engin gögn í vinnubókinni fyrr en í Excel-viðbótar les í.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Opna einingagögn í Excel þegar hefja úr Excel
1.  Í Excel, á við **Setja** flipanum, á **innbætur** flokk er smellt á **Verslun** til að opna Office-Verslun.
2.  Office-Verslun í leita á lykilorð "Dynamics", og smellið á **Bæta** hliðina á í **Microsoft Dynamics Office-viðbótar** (í Excel-viðbótar).
3.  Ef verið er að keyra í Excel-viðbótar í fyrsta sinn, er smellt á **Traust þessa innbótin** til að virkja í Excel viðbót til að keyra. Í Excel-viðbótar keyrir í rúða hægra megin í Excel-glugga.
4.  Smellið á **Bæta þjónsupplýsingar** til að opna í **Valkosti** rúðunni.
5.  Afrita skal markmiði Dynamics 365 fyrir tilvik Aðgerðir vafra Vefslóð, líma þau inn í **Vefþjónsslóð** svæðinu og eyða allt eftir heiti hýsilsins (t.d. eyða **/? cmp = usmf & mi = CustTableListPage**). Meðfylgjandi Vefslóð ætti að hafa bara hýsilheiti (t.d. **https://xxx.dynamics.com**).
6.  Smellið á **í lagi**, og smellið síðan á **Já** til að staðfesta breytinguna. Í Excel bæta restarts og hleður lýsigögnum. Í **Hönnun** hnappinn er nú tiltækt. Hafi í Excel-viðbótar í **Hlaða smáforrit** hnappinn sennilega sem ekki eru kostnaðarjafnaðar að skráður sem rétt notanda. Nánari upplýsingar eru í "Hleðslu smáforrit hnappur birtist" í hlutanum "Troubleshooting" í þessu efnisatriði.
7.  Smellið á **Hönnun**. Sækir lýsigögn einingar í Excel-viðbótar.
8.  Smellið á **töfluna Bæta**. Listi yfir einingar sem birtist. Einingar sem eru talin upp í sniðið "Heiti Merkis –".
9.  Veljið einingu á listanum, eins og **Viðskiptavinar - Viðskiptavinir**, og smellið síðan á **Næsta**.
10. Til að bæta við svæði úr á **Tiltæk svæði** listanum yfir á **Valið svæði** listanum, smella á svæðið og smellið síðan á **Bæta**. Einnig er tvísmellt á svæðið.
11. Eftir að hefur verið bætt við þau svæði sem á við **Valin svæði** listanum bendillinn sé á réttum stað í vinnublaðinu (t.d. hólf A1) og smellið síðan á **Gert**. Smellið síðan á **Gert** til að hætta við hönnuður.
12. Smellið á **Endurnýja** til að sækja gögn í.

## <a name="view-and-update-entity-data-in-excel"></a>Skoða og uppfæra gögn um einingar í Excel
Eftir í Excel-viðbótar les gögn um einingar í vinnubókinni, er hægt að uppfæra gögn í einu með því að smella **Endurnýja** í í Excel-viðbótar.

## <a name="edit-entity-data-in-excel"></a>Breyta einingu gögn í Excel
Hægt er að breyta gögn um einingar sem krefjast og birta hann aftur með því að smella á **Birta** í í Excel-viðbótar. Breyta færslu, veljið í hólf í vinnublaðinu og breyttu síðan hólf gildi. Til að bæta nýrri færslu, skal fylgja eitt af eftirfarandi skrefum:

-   Smellið einhvers staðar í vinnublaðinu, og smellið síðan á **Nýtt** í í Excel-viðbótar.
-   Smella á síðustu línuna vinnublaðs og styðja á Tab lykils þar til bendillinn fer af dálki sem línu og ný lína er stofnuð.
-   Smellt er á í línunni strax undir vinnublaðið og byrja að færa gögn í í flokk. Þegar færa aðdráttinn utan sem hólf expands vinnublaðið til að hafa nýja línu.

Til að eyða færslu, skal fylgja eitt af eftirfarandi skrefum:

-   Hægrismella línunúmer við vinnublaðið línu til að eyða og smellið síðan á **Eyða**.
-   Hægrismellið í vinnublaðinu línu til að eyða og smellið síðan á **Eyða**&gt;**Töfluna Línur**.

## <a name="add-or-remove-columns"></a>Bæta við eða fjarlægja dálka
Hægt er að nota hönnuðurinn til að leiðrétta dálka sem eru sjálfkrafa bætt við í vinnublaðinu.

1.  Hefja uppruna hönnuður gögnin yfir í Excel-viðbótar með því að smella á **Valkosti** hnappinn (gear tákn) og því næst á **Virkja hönnun** gátreitinn.
2.  Smellið á **Hönnun** í í Excel-viðbótar. Alla gagnagjafa eru talin upp.
3.  Við gagnagjafa, smellið á **Breyta** hnappinn (pencil tákn).
4.  Leiðrétta í listanum í **Valinn svæði** listanum sem er krafist:
    -   Til að bæta við svæði úr á **Tiltæk svæði** listanum yfir á **Valið svæði** listanum, smella á svæðið og smellið síðan á **Bæta**. Einnig er tvísmellt á svæðið.
    -   Til að fjarlægja svæðið úr í **Valinn svæði** listanum, smella á svæðið og smellið síðan á **Fjarlægja**. Einnig er tvísmellt á svæðið.
    -   Ef breyta á röð svæða, smella á svæðið á **Valið svæði** listanum og smellið síðan á **Upp** eða **Niður**.

5.  Nota breytingarnar gagnagjafa með því að smella **Uppfærslu**. Smellið síðan á **Gert** til að hætta við hönnuður. Ef svæði (dálk), smellið á **Endurnýja** til að sækja í uppfærð gögn.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
Það eru nokkrar úthreyfingar sem hægt er að leysa gegnum sumar auðveld.

-   **Hnappurinn smáforrit Hleðslu er sýnd.** Hafi í Excel-viðbótar í **Hlaða smáforrit** hnappinn eftir í, sem hafa ekki eru kostnaðarjafnaðar skráður sem rétt notanda. Staðfestið að leysa þetta vandamál rétt notandanafn birtist í efra hægri horninu í Excel-viðbótar. Ef rangt notanda heiti birtist, smella á það útskráning og síðan innskráningu aftur.
-   **Boð "Forbidden".** Ef berast "Forbidden" meðan í Excel-viðbótar er hleður lýsigögnum, er lykillinn sem er innskráður í Excel-viðbótar hefur ekki heimild til að nota markað þjónustu tilvik eða gagnagrunninum. Staðfestið að leysa þetta vandamál rétt notandanafn birtist í efra hægri horninu í Excel-viðbótar. Ef rangt notanda heiti birtist, smella á það útskráning og síðan innskráningu aftur.
-   **Autt vefsíða sýnd yfir í Excel.** Ef autt vefsíða opnar við formerki í vinnslu, lykill krefst AD FS en útgáfu Excel sem keyrir á innbótin ekki nógu nýlegar að hlaða formerki í svarglugganum. Uppfæra útgáfu Excel sem verið er að nota til að leysa þetta vandamál. Til að uppfæra útgáfu Excel þegar verið í sannvotta sem er í frestaður rásar, í [Office virkjun verkfæri](https://technet.microsoft.com/library/jj219422.aspx) til [fara úr frestaður rásar núverandi rás](https://technet.microsoft.com/library/mt455210.aspx).



