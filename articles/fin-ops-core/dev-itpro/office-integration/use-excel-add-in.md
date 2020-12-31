---
title: Opna einingagögn í Excel og uppfæra þau með Excel-innbót
description: Í þessu efnisatriði er útskýrt hvernig opna skal einingagögn í Microsoft Excel og síðan skoða, uppfæra og breyta gögnum með því að nota Microsoft Dynamics Office-innbót fyrir Excel.
author: ChrisGarty
manager: AnnBe
ms.date: 04/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26d5f165648c1553745e3061cc89bcba42f9636a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688468"
---
# <a name="open-entity-data-in-excel-and-update-it-by-using-the-excel-add-in"></a>Opna einingagögn í Excel og uppfæra þau með Excel-innbót

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig opna skal einingagögn í Microsoft Excel og síðan skoða, uppfæra og breyta gögnum með því að nota Microsoft Dynamics Office-innbót fyrir Excel. Til að opna einingagögn geturðu byrjað annaðhvort í Excel eða Finance and Operations.

Með því að opna einingagögn í Excel er hægt að skoða og breyta gögnum með því að nota innbót fyrir Excel. Þessi innbót þarf Microsoft Excel 2016.

> [!NOTE]
> Ef Microsoft Azure Active Directory (Azure AD) leigjandi er skilgreindur til að nota Active Directory Federation Services (AD FS), þarf að tryggja að uppfærsla frá maí 2016 fyrir Office hafi verið notuð, þannig að í Excel-innbót geti skráð þig rétt inn.

Til að fræðast meira um notkun á Excel-innbótinni skaltu horfa á þetta stutta myndband [Stofna Excel-sniðmát fyrir haus- og línumynstur í Dynamics 365 for Finance and Operations](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-finance-and-operations"></a>Opna einingagögn í Excel þegar byrjað er í Finance and Operations
1. Á síðu í Finance and Operations skal velja **Opna í Microsoft Office**.

    Ef rótargagnagjafi (tafla) fyrir listasíðu er sá sami og rótargagnagjafi fyrir allar einingar eru sjálfgefnir valkostir **Opna í Excel** myndaðir fyrir síðuna. Valkostina **Opna í Excel** má finna á algengum síðum, eins og **Allir lánardrottnar** og **Allir viðskiptavinir**.
 
2. Veljið **Opna í Excel** og opnið vinnubókina sem er mynduð. Þessi vinnubók hefur bindingarupplýsingar fyrir einingu, bendilinn í umhverfinu og bendilinn í Excel-innbót.
3. Í Excel, veljið **Virkja breytingar** til að virkja Excel-innbót til að keyra. Í Excel-innbót keyrir í rúða hægra megin í Excel-glugga.
4. Ef verið er að keyra í Excel-innbót í fyrsta sinn, er valið **Treysta þessari innbót**.
5. Ef beðið er um að skrá sig inn skal velja **Innskráningu**, og síðan skrá sig inn með því að nota sömu innskráningarupplýsingar og eru notuð til að skrá sig inn í Finance and Operations. Excel-innbót mun nota samhengi fyrri innskráningar úr Internet Explorer og skrá þig sjálfkrafa inn, ef það er hægt. Þess vegna þarf að staðfesta notandanafn í efra hægri horninu í Excel-innbót.

Excel-innbót les sjálfkrafa gögn fyrir eininguna sem er valin. Athugið að það verða engin gögn í vinnubókinni fyrr en Excel-innbót les þau inn.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Opna einingagögn í Excel þegar hefja úr Excel
1. Í Excel, á flipanum **Setja** í **innbætur** flokk er valið **Verslun** til að opna Office-Verslun.
2. Í Office-Verslun er leitað með í leitað með lykilorðinu **Dynamics** og svo valið **Bæta við** við hliðina á **Microsoft Dynamics Office-innbót** (Excel innbótin).
3. Ef verið er að keyra í Excel-innbót í fyrsta sinn, er valið **Treysta þessari innbót**. Í Excel-innbót keyrir í rúða hægra megin í Excel-glugga.
4. Veljið **Bæta þjónsupplýsingar** til að opna rúðuna **Valkostir**.
5. Í vafranum skal afrita vefslóð úr marktilviki Finance and Operations, líma hana inn í svæðið **Vefþjónsslóð** og eyða síðan öllu eftir heiti hýsilsins. Meðfylgjandi Vefslóð ætti aðeins að hafa bara hýsilheiti.

    Ef slóðin er t.d. `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage` skal eyða öllu nema `https://xxx.dynamics.com`.

6. Veljið **Í lagi** og svo **Já** til að staðfesta breytinguna. Excel-innbót endurræsist og hleður lýsigögnum.

    Hnappurinn **Hönnun** er tiltækur. Ef Excel-innbót er með hnappinn **Hlaða smáforrit** ertu sennilega ekki skráð/ur inn sem réttur notandi. Nánari upplýsingar eru í "Hleðslu smáforrit hnappur birtist" í hlutanum [Úrræðaleit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#troubleshooting) í þessu efnisatriði.

7. Veljið **Hönnun**. Excel-innbót sækir lýsigögn einingar.
8. Velja **Bæta við töflu**. Listi yfir einingar birtist. Einingar eru taldar upp á sniðinu "Heiti – Merki".
9. Veljið einingu á listanum, eins og **Viðskiptavinar - Viðskiptavinir**, og veljið svo **Næsta**.
10. Til að bæta við svæði af listanum **Tiltæk svæði** yfir á listann **Valið svæði** skal velja svæðið og svo **Bæta við**. Einnig er hægt að tvísmella á svæðið í **Tiltækir reitir** listanum.
11. Eftir að svæðum hefur verið bætt við á listann **Valin svæði** þarf að passa að bendillinn sé á réttum stað í vinnublaðinu (t.d. hólf A1) og veja svo **Lokið**. Svo skal velja **Lokið** til að fara úr hönnuði.
12. Veljið **Endurnýja** til að sækja gagnamengi.

## <a name="view-and-update-entity-data-in-excel"></a>Skoða og uppfæra einingagögn í Excel
Eftir að Excel-innbót les gögn um einingar inn í vinnubókina, er hægt að uppfæra gögnin hvenær sem er með því að velja **Endurnýja** í Excel-innbót.

## <a name="edit-entity-data-in-excel"></a>Breyta einingagögnum í Excel
Hægt er að breyta gögnum um einingar eftir þörfum og birta þau aftur með því að velja **Birta** í Excel-innbót. Til að breyta færslu, skal velja hólf í vinnublaðinu og breyta síðan gildi hólfsins. Til að bæta við nýrri færslu, skal fylgja einu af eftirfarandi skrefum:

- Smellið einhvers staðar í gagnagjafatöflunni, og velja svo **Nýtt** í Excel-innbót.
- Smellið hvar sem er í síðustu línu í gagnagjafatöflunni og ýttu síðan á flipalykil þar til að bendillinn fer út úr síðasta dálki þeirrar línu og ný lína er stofnuð.
- Smellið hvar sem er í línunni beint undir gagnagjafatöflunni og byrjaðu að færa gögn í hólf. Þegar áhersla er flutt út úr því hólfi útvíkkast gagnagjafataflan til að hafa nýja línu.
- Valið er eitt af svæðunum fyrir svæðisbindings hausfærslna, og svo **Nýtt** í Excel innbót.

Athugið að aðeins hægt er að stofna nýja færslu ef öll helstu áskildu svæðin eru bundinn í vinnublaðinu eða ef sjálfgildi voru fyllt út með því að nota skilyrði síunnar.

Til að eyða færslu, skal fylgja einu af eftirfarandi skrefum:

- Hægrismellið á línunúmer við hlið vinnublaðslínunnar sem á að eyða og veljið svo **Eyða**.
- Hægrismellið hvar sem er á línunúmer við hlið vinnublaðslínunnar sem á að eyða og veljið svo **Eyða** &gt; **Töflulínur**.

Ef upprunagögnum hefur verið bætt við sem tengdu gagnaveitu, er haus gefinn út fyrir línur. Ef tengsl eru á milli annarra gagnagjafa, gæti þurft að breyta sjálfgefnu útgáfuröðinni. Til að breyta birtingarröðinni, í Excel innbótinni skal velja **Valkostir** hnappinn (tannhjólstáknið), og svo á **Gagnatengi** flipanum **Grunnstilla birta pöntun**.

## <a name="add-or-remove-columns"></a>Bæta við eða fjarlægja dálka
Hægt er að nota hönnuðinn til að leiðrétta dálka sem er sjálfkrafa bætt við vinnublaðið.

> [!NOTE]
> Ef hnappurinn **Hönnun** birtist ekki undir hnappinum **Sía** í Excel-viðbótinni þarftu að virkja hönnuð upprunagagna. Veljið **Valkostir** hnappinn (tannhjólstáknið) og svo **Kveikja á hönnun** gátreitinn.

1. Í Excel-innbótinnni skal velja **Hönnun**. Allir gagnagjafar eru taldir upp.
2. Við hlið gagnagjafa, veljið **Breyta** hnappinn (blýantstákn).
3. Í **Valið svæði** skal stilla lista reita eftir því sem með þarf:

    - Til að bæta við svæði af listanum **Tiltæk svæði** yfir á listann **Valið svæði** skal velja svæðið og svo **Bæta við**. Einnig er hægt að tvísmella á svæðið í **Tiltækir reitir** listanum.
    - Svæði er fjarlægt af listanum **Valin svæði** með því að hægrismella á það og velja **Fjarlægja**. Einnig er hægt að tvísmella á svæðið.
    - Til að breyta röð svæða, skal velja **Valið svæði** listann, velja reit og svo á **Upp** eða **Niður**.

4. Til að nota breytingarnar gagnagjafa skal velja **Uppfæra**. Svo skal velja **Lokið** til að fara úr hönnuði.
5. Ef svæði (dálk) var bætt við, veljið **Endurnýja** til að sækja uppfærð gagnamengi.

## <a name="copy-environment-data"></a>Afrita umhverfisgögn

Gögnin sem eru lesin inn í vinnubókina úr einu umhverfi er hægt að afrita í annað umhverfi. Hins vegar er ekki hægt að breyta tengislóðinni vegna þess að gagnaskyndiminni í vinnubókinni mun halda áfram að meðhöndla gögnin sem fyrirliggjandi gögn. Þess í stað verður þú að nota virknina Afrita umhverfisgögn til að birta gögnin í nýju umhverfi sem ný gögn.

1. Veljið **Valkostir** hnappinn (tannhjólstáknið), og svo **Gagnatengi** flipann **Afrita umhverfisgögn**. 
2. Gefa þarf upp vefslóð þjóns fyrir nýja umhverfið. 
3. Veljið **Í lagi** og svo **Já** til að staðfesta aðgerðina. Excel-innbót endurræsist og tengist við nýja umhverfið. Öll gögn sem eru í vinnubókinni eru meðhöndluð sem ný gögn.

    Eftir að Excel viðbótin er endurræst birtist skilaboðareitur um að vinnubókin sé í Umhverfisafritun.

4. Til að afrita gögnin í nýja umhverfið sem ný gögn skal velja **Birta**. Til að hætta við að umhverfisafritun og skoða núverandi gögn í nýju umhverfi skaltu velja **Uppfæra**.

## <a name="troubleshooting"></a>Úrræðaleit
Það eru nokkur vandamál sem hægt er að leysa með nokkrum auðveldum skrefum.

- **Hnappurinn Hlaða smáforrit er sýndur** - Ef Excel-innbót er með hnappinn **Hlaða smáforrit** ertu sennilega ekki skráð/ur inn sem réttur notandi. Til að leysa þetta vandamál stað staðfesta að rétt notandanafn birtist í efra hægri horninu í Excel-innbót. Ef rangt notandaheiti birtist skal velja það, útskráningu og síðan innskráningu aftur.
- **Ef þér berast „bönnuð“ skilaboð** - Ef þér berast „bönnuð“ skilaboð á meðan Excel-innbót er að hlaða lýsigögnum, er lykillinn sem er innskráður í Excel-innbót ekki með heimild til að nota markað þjónustu tilvik eða gagnagrunninum. Til að leysa þetta vandamál stað staðfesta að rétt notandanafn birtist í efra hægri horninu í Excel-innbót. Ef rangt notandaheiti birtist skal velja það, útskráningu og síðan innskráningu aftur.
- **Auð vefsíða sýnd yfir í Excel** - Ef auð vefsíða opnast við innskráningarvinnslu, krefst lykillinn AD FS en útgáfa Excel sem keyrir á innbótinni er ekki nógu nýleg til að hlaða svarglugga innskráningar. Uppfæra útgáfu Excel sem verið er að nota til að leysa þetta vandamál. Til að uppfæra útgáfu Excel þegar þú ert í stóru fyrirtæki sem eru á frestaðri rás skal nota [Office uppsetningarverkfæri](https://technet.microsoft.com/library/jj219422.aspx) til að [fara úr frestaður rásar yfir í núverandi rás](https://technet.microsoft.com/library/mt455210.aspx).
