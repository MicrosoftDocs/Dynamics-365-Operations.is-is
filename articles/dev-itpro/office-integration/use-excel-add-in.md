---
title: "Nota Excel innbót"
description: "Í þessu efnisatriði er útskýrt hvernig opna skal einingagögn í Microsoft Excel og síðan skoða, uppfæra og breyta gögnum með því að nota Microsoft Dynamics Office-innbót fyrir Excel."
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 06fc9f8dda83fddea9ae331bb82c8874b15d76b9
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="use-the-excel-add-in"></a>Nota Excel innbót

[!include[banner](../includes/banner.md)]


Í þessu efnisatriði er útskýrt hvernig opna skal einingagögn í Microsoft Excel og síðan skoða, uppfæra og breyta gögnum með því að nota Microsoft Dynamics Office-innbót fyrir Excel. Til að opna einingagögn er hægt að hefja úr Excel eða Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

Í þessu efnisatriði er útskýrt hvernig opna á einingagögn í Microsoft Excel og skoða, uppfæra og breyta gögnum með því að nota Microsoft Dynamics Office-innbót fyrir Excel. Þessi innbót krefst Microsoft Excel 2016. **Athugasemd:** Ef notanda Microsoft Azure Active Directory (Azure AD) leigjanda er skilgreindur til að nota Active Directory Federation Services (AD FS), þarf að tryggja að uppfærsla frá maí 2016 hafið verið notuð, þannig að í Excel-innbót geti skráð þig rétt inn.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-finance-and-operations"></a>Opna einingagögn í Excel þegar byrjað er í Dynamics 365 for Finance and Operations
1.  Á síðu í Microsoft Dynamics 365 for Finance and Operations, smellið á **Opna í Microsoft Office**. Ef rótargagnagjafi (tafla) fyrir listasíðu er sá sami og rótargagnagjafi fyrir allar einingar eru sjálfgefnir valkostir **Opna í Excel** myndaðir fyrir síðuna. Valkostina **Opna í Excel** má finna á algengum síðum, eins og **Allir lánardrottnar** og **Allir viðskiptavinir**.
2.  Smellið á valkostinn **Opna í Excel** og opnið vinnubókina sem er mynduð. Þessi vinnubók hefur bindingarupplýsingar fyrir einingu, bendilinn í umhverfinu og bendilinn í Excel-innbót.
3.  Í Excel, smellið á **Virkja breytingar** til að virkja Excel-innbót til að keyra. Í Excel-innbót keyrir í rúða hægra megin í Excel-glugga.
4.  Ef verið er að keyra í Excel-innbót í fyrsta sinn, er smellt á **Treysta þessari innbót**.
5.  Ef beðið er um að skrá sig inn skal smella á **Innskráningu**, og síðan skrá sig inn með því að nota sömu skilríki og er notuð til að skrá sig inn í Dynamics 365 Finance and for Operations. Excel-innbót mun nota samhengi fyrri innskráningar úr Internet Explorer og skrá þig sjálfkrafa inn, ef það er hægt. Þess vegna þarf að staðfesta notandanafn í efra hægri horninu í Excel-innbót.

Excel-innbót les sjálfkrafa gögn fyrir eininguna sem er valin. Athugið að það verða engin gögn í vinnubókinni fyrr en Excel-innbót les þau inn.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Opna einingagögn í Excel þegar hefja úr Excel
1.  Í Excel, á flipanum **Setja** í **innbætur** flokk er smellt á **Verslun** til að opna Office-Verslun.
2.  Office-Verslun er leitað með í leitað með lykilorð "Dynamics", og smellið á **Bæta við** við hliðina á **Microsoft Dynamics Officel-innbót** (í Excel-innbót).
3.  Ef verið er að keyra í Excel-innbót í fyrsta sinn, er smellt á **Treysta þessari innbót**. Í Excel-innbót keyrir í rúða hægra megin í Excel-glugga.
4.  Smellið á **Bæta þjónsupplýsingar** til að opna rúðuna **Valkostir**.
5.  Afrita skal vafraslóð úr markmiði tilviki Dynamics 365 for Finance and Operations, líma hana inn í svæðið **Vefþjónsslóð** og eyða síðan öllu eftir heiti hýsilsins. Meðfylgjandi Vefslóð ætti að hafa bara hýsilheiti.
Ef slóðin er t.d. https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage, skal eyða öllu nema **https://xxx.dynamics.com**.
6.  Smellt er á **Í lagi** og **Já** til að staðfesta breytinguna. Excel-innbót endurræsist og hleður lýsigögnum. Hnappurinn **Hönnun** er tiltækur. Ef Excel-innbót er með hnappinn **Hlaða smáforrit** ertu sennilega ekki skráð/ur inn sem réttur notandi. Nánari upplýsingar eru í "Hleðslu smáforrit hnappur birtist" í hlutanum „Úrræðaleit" í þessu efnisatriði.
7.  Smellið á **Hönnun**. Excel-innbót sækir lýsigögn einingar.
8.  Smelltu á **Bæta við töflu**. Listi yfir einingar birtist. Einingar eru taldar upp á sniðinu "Heiti – Merki".
9.  Veljið einingu á listanum, eins og **Viðskiptavinar - Viðskiptavinir**, og smellið síðan á **Næsta**.
10. Til að bæta við svæði af listanum **Tiltæk svæði** yfir á listann **Valið svæði** skal smella á svæðið og smellið síðan á **Bæta við**. Einnig er hægt að tvísmella á svæðið.
11. Eftir að svæðum hefur verið bætt við á listann **Valin svæði** þarf að passa að bendillinn sé á réttum stað í vinnublaðinu (t.d. hólf A1) og smella síðan á **Lokið**. Smellið síðan á **Gert** til að fara úr hönnuði.
12. Smellið á **Endurnýja** til að sækja gagnamengi.

## <a name="view-and-update-entity-data-in-excel"></a>Skoða og uppfæra einingagögn í Excel
Eftir að Excel-innbót les gögn um einingar inn í vinnubókina, er hægt að uppfæra gögnin hvenær sem er með því að smella á **Endurnýja** í Excel-innbót.

## <a name="edit-entity-data-in-excel"></a>Breyta einingagögnum í Excel
Hægt er að breyta gögnum um einingar eftir þörfum og birta þau aftur með því að smella á **Birta** í Excel-innbót. Til að breyta færslu, skal velja hólf í vinnublaðinu og breyta síðan gildi hólfsins. Til að bæta við nýrri færslu, skal fylgja einu af eftirfarandi skrefum:

-   Smellið einhvers staðar í gagnagjafatöflunni, og smellið síðan á **Nýtt** í Excel-innbót.
-   Smella í síðustu línu í gagnagjafatöflunni og ýttu síðan á flipalykil þar til að bendillinn fer út úr síðasta dálki þeirrar línu og ný lína er stofnuð.
-   Smelltu í línuna beint undir gagnagjafatöflunni og byrjaðu að færa gögn í hólf. Þegar áhersla er flutt út úr því hólfi útvíkkast gagnagjafataflan til að hafa nýja línu.
-   Smellið á eitt af svæðunum fyrir svæðisbindings hausfærslna, og smellið síðan á **Nýtt** í Excel innbót.

Athugið að aðeins hægt er að stofna nýja færslu ef öll helstu áskildu svæðin eru bundinn í vinnublaðinu eða ef sjálfgildi voru fyllt út með því að nota skilyrði síunnar.
Til að eyða færslu, skal fylgja einu af eftirfarandi skrefum:

-   Hægri-smella á línunúmer við hlið vinnublaðslínunnar sem á að eyða og smella síðan á **Eyða**.
-   Hægri-smella í vinnublaðslínuna sem á að eyða og smella síðan á **Eyða** &gt; **Töflulínur**.
Ef upprunagögnum hefur verið bætt við sem tengdum, er haus gefinn út fyrir línur. Ef tengsl eru á milli annarra gagnagjafa, gæti þurft að breyta sjálfgefnu útgáfuröðinni. Til að breyta útgáfuröðinni í Excel-innbótinni, smellið á **Valkostir** hnappinn (tannhjólstákn). Á flýtiflipanum **Gagnatengi** skal svo smella á **Grunnstilla birtingarröð**.

## <a name="add-or-remove-columns"></a>Bæta við eða fjarlægja dálka
Hægt er að nota hönnuðinn til að leiðrétta dálka sem er sjálfkrafa bætt við vinnublaðið.

1.  Hefja hönnuð upprunagagna í Excel-innbót með því að smella á **Valkosti** hnappinn (tannhjólstákn) og velja síðan **Virkja hönnun** gátreitinn.
2.  Smellið á **Hönnun** í Excel-viðbót. Allir gagnagjafar eru taldir upp.
3.  Við hlið gagnagjafa, smellið á **Breyta** hnappinn (blýantstákn).
4.  Leiðréttu listann í listanum **Valinn svæði** eftir því sem með þarf:
    -   Til að bæta við svæði af listanum **Tiltæk svæði** yfir á listann **Valið svæði** skal smella á svæðið og smellið síðan á **Bæta við**. Einnig er hægt að tvísmella á svæðið.
    -   Svæði er fjarlægt af listanum **Valin svæði** með því að hægrismella á það og smella því næst á **fjarlægja**. Einnig er hægt að tvísmella á svæðið.
    -   Til að breyta röð svæða, skal smella á svæðið í **Valið svæði** listanum, smella á reit og svo á **Upp** eða **Niður**.

5. Til að nota breytingarnar gagnagjafa skal smella á **Uppfæra**. Smellið síðan á **Gert** til að fara úr hönnuði. 
6. Ef svæði (dálk) var bætt við, smellið á **Endurnýja** til að sækja uppfærð gagnamengi.

## <a name="troubleshooting"></a>Úrræðaleit
Það eru nokkur vandamál sem hægt er að leysa með nokkrum auðveldum skrefum.

-   **Hnappurinn Hlaða smáforrit er sýndur.** Ef Excel-innbót er með hnappinn **Hlaða smáforrit** ertu sennilega ekki skráð/ur inn sem réttur notandi. Til að leysa þetta vandamál stað staðfesta að rétt notandanafn birtist í efra hægri horninu í Excel-innbót. Ef rangt notandaheiti birtist, smella á það, útskráning og síðan innskráningu aftur.
-   **Þú færð „bönnuð“ skilaboð.** Ef þér berast „bönnuð“ skilaboð á meðan Excel-innbót er að hlaða lýsigögnum, er lykillinn sem er innskráður í Excel-innbót ekki með heimild til að nota markað þjónustu tilvik eða gagnagrunninum. Til að leysa þetta vandamál stað staðfesta að rétt notandanafn birtist í efra hægri horninu í Excel-innbót. Ef rangt notandaheiti birtist, smella á það, útskráning og síðan innskráningu aftur.
-   **Auð vefsíða sýnd yfir í Excel.** Ef auð vefsíða opnast við innskráningarvinnslu, krefst lykillinn AD FS en útgáfa Excel sem keyrir á innbótinni er ekki nógu nýleg til að hlaða svarglugga innskráningar. Uppfæra útgáfu Excel sem verið er að nota til að leysa þetta vandamál. Til að uppfæra útgáfu Excel þegar þú ert í stóru fyrirtæki sem eru á frestaðri rás skal nota [Office uppsetningarverkfæri](https://technet.microsoft.com/library/jj219422.aspx) til að [fara úr frestaður rásar yfir í núverandi rás](https://technet.microsoft.com/library/mt455210.aspx).





