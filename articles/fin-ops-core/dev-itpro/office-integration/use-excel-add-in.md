---
title: Skoða og uppfæra einingagögn með Excel
description: Í þessu efnisatriði er útskýrt hvernig opna skal einingagögn í Microsoft Excel og síðan skoða, uppfæra og breyta gögnum með því að nota Microsoft Dynamics Excel-innbót.
author: jasongre
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1593206e8e22aed518ebca9bee0772c6620bec9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068793"
---
# <a name="view-and-update-entity-data-with-excel"></a>Skoða og uppfæra einingagögn með Excel 

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]


Í þessu efnisatriði er útskýrt hvernig opna skal einingagögn í Microsoft Excel og síðan skoða, uppfæra og breyta gögnum með því að nota Microsoft Dynamics Excel-innbót. Til að opna einingargögn geturðu byrjað annað hvort í Excel eða Finance and Operations forritum.

Með því að opna einingagögn í Excel er hægt að skoða og breyta gögnum með því að nota innbót fyrir Excel. Þessi innbót þarf Microsoft Excel 2016 eða nýrra.

> [!NOTE]
> Ef Microsoft Azure Active Directory (Azure AD) leigjandi er skilgreindur til að nota Active Directory Federation Services (AD FS), þarf að tryggja að uppfærsla frá maí 2016 fyrir Office hafi verið notuð, þannig að í Excel-innbót geti skráð þig rétt inn.

Til að fá frekari upplýsingar um hvernig á að nota Excel-innbótina skal horfa á stutt myndband: [Stofna Excel-sniðmát fyrir haus- og línumynstur](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-a-finance-and-operations-app"></a>Opnaðu einingargögn í Excel þegar þú byrjar úr Finance and Operations app
1. Veldu á síðu í Finance and Operations app **Opið í Microsoft Office**.

    Ef rótargagnagjafi (tafla) fyrir listasíðu er sá sami og rótargagnagjafi fyrir allar einingar eru sjálfgefnir valkostir **Opna í Excel** myndaðir fyrir síðuna. Valkostina **Opna í Excel** má finna á algengum síðum, eins og **Allir lánardrottnar** og **Allir viðskiptavinir**.
 
2. Veljið **Opna í Excel** og opnið vinnubókina sem er mynduð. Þessi vinnubók hefur bindingarupplýsingar fyrir einingu, bendilinn í umhverfinu og bendilinn í Excel-innbót.
3. Í Excel, veljið **Virkja breytingar** til að virkja Excel-innbót til að keyra. Í Excel-innbót keyrir í rúða hægra megin í Excel-glugga.
4. Ef verið er að keyra í Excel-innbót í fyrsta sinn, er valið **Treysta þessari innbót**.
5. Ef þú ert beðinn um að skrá þig inn skaltu velja **skrá inn**, og skráðu þig síðan inn með því að nota sömu skilríki og þú notaðir til að skrá þig inn á Finance and Operations appið. Excel-innbót mun nota samhengi fyrri innskráningar úr vafra og skrá þig sjálfkrafa inn, ef það er hægt. (Upplýsingar um vafrann sem notaður er samkvæmt stýrikerfinu er að finna í [Vafrar sem Office-innbætur nota](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins.) Til að ganga úr skugga um að innskráning hafi tekist skal staðfesta notandanafnið efst í hægra horni Excel-innbótarinnar. 

Excel-innbót les sjálfkrafa gögn fyrir eininguna sem er valin. Athugið að það verða engin gögn í vinnubókinni fyrr en Excel-innbót les þau inn.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Opna einingagögn í Excel þegar hefja úr Excel
1. Í Excel, á flipanum **Setja** í **innbætur** flokk er valið **Verslun** til að opna Office-Verslun.
2. Í Office-Verslun er leitað með í leitað með lykilorðinu **Dynamics** og svo valið **Bæta við** við hliðina á **Microsoft Dynamics Office-innbót** (Excel innbótin).
3. Ef verið er að keyra í Excel-innbót í fyrsta sinn, er valið **Treysta þessari innbót**. Í Excel-innbót keyrir í rúða hægra megin í Excel-glugga.
4. Veljið **Bæta þjónsupplýsingar** til að opna rúðuna **Valkostir**.
5. Í vafranum þínum skaltu afrita vefslóðina á tilvikinu þínu fyrir Finance and Operations appið þitt, límdu það inn í **Vefslóð netþjóns** reit og eyddu síðan öllu á eftir hýsilnafninu. Meðfylgjandi Vefslóð ætti aðeins að hafa bara hýsilheiti.

    Ef slóðin er t.d. `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage` skal eyða öllu nema `https://xxx.dynamics.com`.

6. Veljið **Í lagi** og svo **Já** til að staðfesta breytinguna. Excel-innbót endurræsist og hleður lýsigögnum.

    Hnappurinn **Hönnun** er tiltækur. Ef Excel-innbótin er með tengilinn **Hlaða smáforritum** ertu sennilega ekki skráð/ur inn sem réttur notandi. Frekari upplýsingar um hvernig skuli bregðast við þessu vandamáli er að finna í úrræðaleitarfærslunni [Hlaða smáforritum](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane).

7. Smellið á **Hönnun**. Excel-innbót sækir lýsigögn einingar.
8. Velja **Bæta við töflu**. Listi yfir einingar birtist. Einingar eru taldar upp á sniðinu "Heiti – Merki".
9. Veljið einingu á listanum, eins og **Viðskiptavinar - Viðskiptavinir**, og veljið svo **Næsta**.
10. Til að bæta við svæði af listanum **Tiltæk svæði** yfir á listann **Valið svæði** skal velja svæðið og svo **Bæta við**. Einnig er hægt að tvísmella á svæðið í **Tiltækir reitir** listanum.
11. Eftir að svæðum hefur verið bætt við á listann **Valin svæði** þarf að passa að bendillinn sé á réttum stað í vinnublaðinu (t.d. hólf A1) og veja svo **Lokið**. Svo skal velja **Lokið** til að fara úr hönnuði.
12. Veljið **Endurnýja** til að sækja gagnamengi.

## <a name="view-and-update-entity-data-in-excel"></a>Skoða og uppfæra einingagögn í Excel
Eftir að Excel-innbót les gögn um einingar inn í vinnubókina, er hægt að uppfæra gögnin hvenær sem er með því að velja **Endurnýja** í Excel-innbót.

## <a name="edit-entity-data-in-excel"></a>Breyta einingagögnum í Excel
Þú getur breytt einingargögnum eftir þörfum og birt þau síðan aftur í Finance and Operations forrit með því að velja **Birta** í Excel viðbótinni. Til að breyta færslu, skal velja hólf í vinnublaðinu og breyta síðan gildi hólfsins. Til að bæta við nýrri færslu, skal fylgja einu af eftirfarandi skrefum:

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

## <a name="change-the-publish-batch-size"></a>Breyta runustærð birtingar
Þegar notendur birta breytingar á gagnafærslum með því að nota Excel-innbótina eru uppfærslurnar sendar inn í runur. Sjálfgefin runustærðarstærð útgáfu er 100 línur. Í útgáfu 10.0.17 og nýrri mun eiginleikinn **Leyfa skilgreiningu á runustærð birtingar í Excel innbótinni** veita sveigjanlegri stjórnun á runustærð birtingar.

Kerfisstjórar geta tilgreint takmörk fyrir allt kerfið í runustærð birtingar fyrir „Opna í Excel“ vinnubækur með því að stilla reitinn **Takmörk runubirtingar** í hlutanum **Færibreytur forrits** á síðunni **Færibreytur Office-forrits**.

Einnig er hægt að breyta runustærð birtingar fyrir staka vinnubók með því að nota Excel-innbótina.

1. Opnið vinnubókina í Excel.
2. Veljið hnappinn (tannhjólið) **Valkostur** uppi hægra megin í Excel-innbótinni.
3. Stillið reitinn **Runustærð birtingar** eftir þörfum. Gildið sem stillt er verður að vera minna en takmörk runubirtingar yfir allt kerfið.
4. Veljið **Í lagi**.
5. Vistið vinnubókina. Ef vinnubókin er ekki vistuð þegar breytingar hafa verið gerðar á stillingum innbótar munu þessar breytingar ekki halda sér þegar vinnubókin er opnuð aftur.

Sniðmátshöfundar Excel-vinnubókar geta notað sömu aðferð til að stilla runustærð birtingar fyrir sniðmát áður en þeir hlaða þeim upp í kerfið.

## <a name="copy-environment-data"></a>Afrita umhverfisgögn

Gögnin sem eru lesin inn í vinnubókina úr einu umhverfi er hægt að afrita í annað umhverfi. Hins vegar er ekki hægt að breyta tengislóðinni vegna þess að gagnaskyndiminni í vinnubókinni mun halda áfram að meðhöndla gögnin sem fyrirliggjandi gögn. Þess í stað verður þú að nota virknina Afrita umhverfisgögn til að birta gögnin í nýju umhverfi sem ný gögn.

1. Veljið **Valkostir** hnappinn (tannhjólstáknið), og svo **Gagnatengi** flipann **Afrita umhverfisgögn**. 
2. Gefa þarf upp vefslóð þjóns fyrir nýja umhverfið. 
3. Veljið **Í lagi** og svo **Já** til að staðfesta aðgerðina. Excel-innbót endurræsist og tengist við nýja umhverfið. Öll gögn sem eru í vinnubókinni eru meðhöndluð sem ný gögn.

    Eftir að Excel viðbótin er endurræst birtist skilaboðareitur um að vinnubókin sé í Umhverfisafritun.

4. Til að afrita gögnin í nýja umhverfið sem ný gögn skal velja **Birta**. Til að hætta við að umhverfisafritun og skoða núverandi gögn í nýju umhverfi skaltu velja **Uppfæra**.

## <a name="troubleshooting"></a>Úrræðaleit
Það eru nokkur vandamál sem hægt er að leysa með nokkrum auðveldum skrefum.

- **Tengillinn „Hlaða smáforritum“ er sýndur** – Frekari upplýsingar um þetta vandamál er að finna í úrræðaleitarfærslunni [Hlaða smáforritum](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane). 
- **Ef þér berast „bönnuð“ skilaboð** - Ef þér berast „bönnuð“ skilaboð á meðan Excel-innbót er að hlaða lýsigögnum, er lykillinn sem er innskráður í Excel-innbót ekki með heimild til að nota markað þjónustu tilvik eða gagnagrunninum. Til að leysa þetta vandamál stað staðfesta að rétt notandanafn birtist í efra hægri horninu í Excel-innbót. Ef rangt notandaheiti birtist skal velja það, útskráningu og síðan innskráningu aftur.
- **Auð vefsíða sýnd yfir í Excel** - Ef auð vefsíða opnast við innskráningarvinnslu, krefst lykillinn AD FS en útgáfa Excel sem keyrir á innbótinni er ekki nógu nýleg til að hlaða svarglugga innskráningar. Uppfæra útgáfu Excel sem verið er að nota til að leysa þetta vandamál. Til að uppfæra útgáfu Excel þegar þú ert í stóru fyrirtæki sem eru á frestaðri rás skal nota [Office uppsetningarverkfæri](/deployoffice/overview-office-deployment-tool) til að [fara úr frestaður rásar yfir í núverandi rás](/deployoffice/overview-update-channels).
- **Þú færð tímalok á meðan þú ert að gefa út gagnabreytingar** – Ef upp koma skilaboð um tímalok á meðan reynt er að gefa út gagnabreytingar á einingu skal huga að því að draga úr runustærð birtingar fyrir vinnubókina sem um ræðir. Einingar sem ræsa mikið magn af rökum fyrir skráarbreytingar gætu þurft að uppfærslur verði sendar í smærri runum til að koma í veg fyrir tímalokanir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
