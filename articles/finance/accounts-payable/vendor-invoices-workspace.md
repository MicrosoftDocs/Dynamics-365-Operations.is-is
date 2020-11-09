---
title: Vinnusvæði reikningsfærslu lánardrottins
description: Þetta efnisatriði útskýrir hvernig á að setja upp vinnusvæðið sem tengist reikningum lánardrottna og sýnir upplýsingarnar sem eru í boði í gegnum Microsoft Power BI.
author: abruer
manager: AnnBe
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a4ba676d9b6df69cf0a91862bcc4d2837b7cb69e
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000796"
---
# <a name="vendor-invoice-entry-workspace"></a>Vinnusvæði reikningsfærslu lánardrottins

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp vinnusvæðið sem tengist reikningum lánardrottna og sýnir upplýsingarnar sem eru í boði í gegnum Microsoft Power BI. Upplýsingar um reikning lánardrottins á þessu vinnusvæði eru afmarkaðar fyrir tiltekna notendur og eru sýndar á myndrænu sniði.

## <a name="overview"></a>Yfirlit

**Reikningsfærsla lánardrottins** vinnusvæðið sýnir upplýsingar sem tengjast meðhöndlun reikninga lánardrottins. Þar er að finna yfirlitið **Mín vinna** og síðuna **Greiningar - Öll fyrirtæki**. Í **Mínar vinnu** skoða sýnir samantekt tiles hnitanet færslu lánardrottins og tengdar lánardrottnaupplýsingum. Síðan **Greiningar - Öll fyrirtæki** notar möguleika Power BI til að sýna myndefni sem tengjast reikningum lánardrottna.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Setja upp vinnusvæði til að sýna Power BI efni

Ljúka verður við þessa uppsetningu áður en hægt er að sýna gögn í myndrænni framsetningu Power BI á vinnusvæðinu **Reikningsfærsla lánardrottins**.

1. Á vinnusvæðinu **Eiginleikastjórnun** skal sía listann til að finna eiginleikann **Sjálfvirkni reiknings lánardrottins**.
3. Veldu **Virkja núna**.
4. Til að tryggja að hægt sé að vinna úr reikningum frá upphafi til enda án þess að þurfa handvirk afskipti skal setja upp verkflæði lánardrottnareiknings. Til að setja upp verkflæði skal fara í **Viðskiptaskuldir \> Uppsetning \> Verkflæði viðskiptaskulda**.
5. Farið í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda** og veljið flipann **Sjálfvirkni lánardrottnareiknings**. Frekari upplýsingar er að finna í [Uppsetningarvalkostir fyrir sjálfvirkni lánardrottnareiknings](vnd-invoice-set-up-options.md).
6. Stillið valkostinn **Senda innflutta reikninga sjálfkrafa í verkflæði** á **Já**.
7. Ef innhreyfingarskjöl afurða eiga að vera sjálfkrafa jöfnuð skal stilla valkostinn **Sjálfkrafa jafna innhreyfingarskjöl afurða við reikninga** á **Já**.
8. Yfirfarið eftirstandandi valfrjálsar stillingar og skilgreinið þær samkvæmt kröfum fyrirtækisins.
9. Farið í **Kerfisstjórnun \> Uppsetning \> Kerfisfæribreytur** og stillið reitina **Gjaldmiðill kerfis** og **Gengi kerfis**.
10. Farið í **Almennur fjárhagur \> Uppsetning \> Fjárhagur** og stillið reitina **Bókhaldsgjaldmiðill** og **Gerð gengis**.
11. Farið í **Fjárhagur \> Gjaldmiðlar \> Gengi gjaldmiðla** og færið inn gengið milli færslugjaldmiðils og bókhaldsgjaldmiðils og milli bókhaldsgjaldmiðils og kerfisgjaldmiðils.
12. Farið í **Kerfisstjórnun \> Uppsetning \> Einingaverslun** og leitið að **Sjálfvirk mæling lánardrottnareiknings**. Veldu **Endurnýja**.

Til að skoða upplýsingarnar sem birtast á vinnusvæðinu þarf að vera með öryggishlutverk fyrir stjórnanda eða starfsmann viðskiptaskulda.

## <a name="my-work-view"></a>Skoða Mína vinnu

### <a name="company-selection"></a>Val fyrirtækis

Þegar kveikt er á eiginleikanum **Gera reikninga lánardrottna sjálfvirka** birtist reiturinn **Fyrirtæki** efst á vinnusvæðinu. Valið í reitnum **Fyrirtæki** hefur áhrif á allar upplýsingar sem sýndar eru á vinnusvæðinu. Yfirlit sýnir sjálfgefið upplýsingar fyrir fyrirtækið sem þú skráðir þig inn í. Með því að velja annað fyrirtæki í reitnum **Fyrirtæki** geturðu sýnt upplýsingar fyrir það fyrirtæki á vinnusvæðinu. Síðan er hægt að velja reit á vinnusvæðinu til að fara á tengda síðu í völdu fyrirtæki.

### <a name="summary-tiles"></a>Samantektarreitir

Reitirnir í hlutanum **Samantekt yfir reikninga í bið** í yfirlitinu **Mín vinna** gefur yfirlit yfir stöðu lánardrottnareikninganna. Hægt er að sjá færslubækur sem eru ekki enn bókaðar og reikninga sem eru í bið. Að auki eru það reitirnir fjórir sem tengjast sjálfvirknieiginleika lánardrottnareiknings:

- Handvirka jöfnun innhreyfingar vantar
- Villuleit jöfnunar tókst ekki
- Reikningar ekki sendir í verkflæði
- Reikningar ekki fluttir inn

(Þessir fjórir reitir krefjast þess að kveikt sé á sjálfvirknieiginleiki lánardrottnareiknings í eiginleikastjórnun.)

Til að nota reitinn **Endurheimta reikninga lánardrottna** verður að vera kveikt á eiginleikanum í færibreytum viðskiptaskulda. Farið í **Viðskiptaskuldir \> Færibreytur viðskiptaskulda** og síðan, í flipanum **Reikningur** , skal stilla valkostinn **Leyfa endurheimt á reikningum lánardrottna** á **Já**.

Þegar kveikt er á eiginleikanum sjást einnig þrír reitir saman á vinnusvæðinu í hluta sem kallast **Færslubækur**. Reitirnir kallast **Færslubækur** , **Færslubækur – Úthlutað til þín** og **Reikningasafn**. 

Upplýsingarnar í hlutanum **Samantekt yfir reikninga í bið** eru fyrir fyrirtækið sem er stillt sem sjálfgefið fyrirtæki fyrir innskráninguna þína.

### <a name="creating-new-records"></a>Nýjar færslur stofnaðar

Til að stofna nýja reikningsfærslu skal velja **Ný** og síðan velja eina af eftirfarandi færslugerðum úr listanum:

- Reikningur frá lánardrottni
- Reikningabók
- Altæk reikningabók
- Skráningabók reikninga
- Reikningssamþykki

Athugið að færslan sem er stofnuð byggir á fyrirtækissíunni, ekki fyrirtækinu sem þú ert skráður inn í. Til dæmis er þú skráð(ur) inn í **UMSF** fyrirtækið en sía fyrirtækisins er stillt á **GBSI**. Í þessu tilfelli, þegar þú velur **Ný** og velur síðan færslugerð úr listanum, er færslan stofnuð í GBSI-fyrirtækinu.

### <a name="documents-not-invoiced-grids"></a>Hnitanet fyrir ekki reikningsfærð skjöl

Hlutinn **Skjöl ekki reikningsfærð** inniheldur hnitanet sem sýnir skjöl sem bíða eftir lánardrottnareikningum.

Hnitanetið **Opna innkaupapantanir** sýnir allar innkaupapantanir sem eru ekki enn að fullu reikningsfærðar. Hægt er að nota hnappinn **Reikningur núna** til að stofna reikning lánardrottins fyrir innkaupapöntun. Hægt er að nota hnappinn **Fyrirframgreiðslureikningur núna** til að stofna fyrirframgreiðslureikning fyrir innkaupapöntun.

Hnitanetið **Innhreyfingarskjöl afurða** sýnir innhreyfingarfærslur innkaupa sem ekki er búið að reikningsfæra að fullu. Hægt er að nota hnappinn **Reikningur núna** til að stofna reikning lánardrottins fyrir innkaupapöntun.

Hnitanetið **Reikningar frá lánardrottni í bið** sýnir alla lánardrottnareikninga sem hafa ekki verið sendir inn í verkflæðiskerfið. Hægt er að nota reitinn **Leita** og/eða fyrirtækissíuna til að leita að tilteknum reikningi lánardrottins. Hægt er að nota hnappinn **Breyta** til að breyta færslu sem birtist í hnitanetinu.

Í hnitanetinu **Finna innkaupapöntun** er hægt að nota reitinn **Leita** til að leita að tiltekinni innkaupapöntun.

### <a name="related-information"></a>Tengdar upplýsingar

Hægt er að skoða upplýsingar um bókaða reikninga með því að nota tenglana hægra megin á vinnusvæðinu. Þessir tenglar innihalda **Opnir lánardrottnareikningar** , **Reikningabækur** og **Reikningssaga og samsvarandi upplýsingar**. Í hlutanum **Lánardrottnar** er hægt að opna síaðan lista sem sýnir alla lánardrottna sem eru í bið eða hægt er að nota tengilinn **Allir lánardrottnar**. Tenglarnir **Allar innkaupapantanir** og **Opnar fyrirframgreiðslur** eru einnig í boði.

### <a name="analytics--all-companies-page"></a>Greiningar - síðan fyrir öll fyrirtæki

Þegar valkosturinn **Senda innflutta reikninga sjálfkrafa í verkflæði** er stilltur á **Já** á síðunni **Færibreytur viðskiptaskulda** er hægt að skoða greiningar sjálfvirkni. Síðan **Greiningar - öll fyrirtæki** býður upp á mikilvægar mælingar á borð við lánardrottnareikninga sem eru í samþykkisferli samþykktaraðila og fyrirtækis. Þessi síða inniheldur fimm skýrslusíður. Á einni síðu er að finna yfirlit og hinar síðurnar gefa upp upplýsingar um mælingar á sjálfvirkni viðskiptaskulda.

Eftirfarandi tafla sýnir sýnigögn sem eru tiltæk á hverri skýrslusíðu.

| Skýrslusíða                    | Myndbirtingar |
|--------------------------------|----------------|
| Yfirlit lánardrottnareikninga        | <ul><li>Reikningar frá lánardrottni í bið í sjálfvirkni í kerfisgjaldmiðli</li><li>Reikningar sem ekki tókst að flytja inn</li><li>Reikningar í verkflæði</li><li>Snertilausir reikningar síðustu 30 daga</li><li>Samtals sjálfvirkir reikningar síðustu 30 daga</li><li>Staða opinna reikninga í kerfisgjaldmiðli</li><li>Ástæður fyrir bilunum síðustu 30 daga</li><li>Prósenta bókaðra reikninga sem voru unnir sjálfkrafa</li><li>Dagar til að vinna úr reikningi</ul></li> |
| Staða sjálfvirkni              | <ul><li>Snertilausir reikningar síðustu 30 daga</li><li>Snertilausir reikningar síðustu 30 daga eftir fyrirtæki</li><li>Snertilausir reikningar síðustu 30 daga eftir lánardrottnaflokki</li><li>Prósenta bókaðra reikninga sem voru unnir sjálfkrafa</li><li>Dagar til að vinna úr reikningi</li></ul> |
| Reikningar sem ekki tókst að flytja inn | <ul><li>Reikningar sem ekki tókst að flytja inn</li><li>Reikningar sem ekki tókst að flytja inn eftir fyrirtæki</li></ul> |
| Ástæður fyrir bilun sjálfvirkni | <ul><li>Reikningar mistókust</li><li>Reikningar mistókust eftir fyrirtæki</li><li>Reikningar mistókust eftir lánardrottnaflokki</li></ul> |
| Staða verkflæðis                | <ul><li>Reikningar í verkflæði</li><li>Verkflæðitilvik lánardrottnareiknings</li><li>Úthlutun á hvern samþykkjanda</li><li>Verkflæði lánardrottnareiknings eftir fyrirtæki</li><li>Meðaltal daga í verkflæði eftir samþykkjanda</li></ul> |
