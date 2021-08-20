---
title: Vinna með fólíó
description: Þetta efnisatriði útskýrir hvernig á að vinna með fólíó. Fólíó inniheldur yfirleitt eina vöru lánardrottins fyrir eina einingu eða fyrirtæki á hverja sendingu. Vörur í fólíói geta verið í einum gámi eða dreift á marga gáma.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 813065b32df8388ef2e86841267e499691b528e16d5bb9ef3072b3ce811ffaa0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713007"
---
# <a name="manage-folios"></a>Vinna með fólíó

[!include [banner](../../includes/banner.md)]

Fólíó er oft ákvarðað samkvæmt tollreglugerðum. Það getur innihaldið eina vöru lánardrottins fyrir eina einingu eða fyrirtæki fyrir hverja sendingu. Vörur í fólíói geta verið í einum gámi eða dreift á marga gáma.

Til að opna síðun **Öll fólíó** skal fara á **Heildarkostnaður \> Fólíó \> Öll fólíó**. Þessi síða sýnir lista yfir öll núgildandi fólíó. Hægt er að nota hnappana á aðgerðasvæðinu til að stofna, eyða eða vinna með fólíó. Veljið hvaða fólíó sem er á listanum til að skoða upplýsingar á síðunni **Fólíó**.

## <a name="action-pane"></a>Aðgerðasvæði

Á aðgerðasvæðinu á síðunum **Öll fólíó** og **Fólíó** eru hnappar sem gera kleift að vinna með valið fólíó. Hver hnappur framkvæmir eina aðgerð. Aðgerðarsvæðið inniheldur líka flipa sem hver um sig býður upp á sett af svipuðum hnöppum. Nema þar sem annað er tekið fram, er öllum hnöppum og flipum sem lýst er í eftirfarandi undirhlutum tiltækir bæði á listayfirlitinu (þ.e. á síðunni **Öll fólíó**) og í ítarlega yfirlitinu (þ.e. á síðunni **Fólíó**).

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Hnappar sem birtast á aðgerðasvæðinu

Eftirfarandi tafla lýsir hnöppunum sem eru í boði á aðgerðasvæðinu.

| Hnappur | lýsing |
|---|---|
| Nýjar | Búa til fólíó. |
| Eyða | Eyða opnu eða völdu fólíói. |
| Kostnaður ferðar | Opnið síðuna **Kostnaður ferðar** þar sem hægt er að skoða og bæta kostnaði á stigi fólíós við allar vörur í ferðinni. Þegar kostnaði fólíós er bætt handvirkt við ferðina er honum sjálfkrafa bætt við síðuna fyrirspurn um kostnað og skipt niður á hverja vöru samkvæmt aðferðinni sem er tilgreind á síðunni **Kostnaður ferðar**. |

### <a name="buttons-on-the-manage-tab"></a>Hnappar á stjórnunarflipanum

Eftirfarandi tafla lýsir hnöppunum sem eru í boði í flipanum **Stjórna** á aðgerðasvæðinu.

| Hnappur | lýsing |
|---|---|
| Bóka innhreyfingalista | Bókið innhreyfingaskjal fyrir allar innkaupapöntunarlínur í fólíói. Ef sendingar margra fyrirtækja eru notaðar opnast nýr svargluggi fyrir bókun innhreyfingaskjals fyrir hvert fyrirtæki. |
| Bóka innhreyfingarskjal afurða | Bókið innhreyfingarskjal afurðar fyrir allar innkaupapöntunarlínur í fólíói. Ef ferðir margra fyrirtækja eru notaðar opnast nýr svargluggi fyrir bókun innhreyfingarskjals fyrir hvert fyrirtæki. |
| Bóka reikning | Bókið reikning fyrir allar innkaupapöntunarlínur í fólíói. Ef ferðir margra fyrirtækja eru notaðar opnast nýr svargluggi fyrir bókun reiknings fyrir hvert fyrirtæki. |
| Senda flutningspöntun | Bókið flutningspöntun fyrir allar flutningspöntunarlínur sem tengjast núverandi fólíói í tengdri sendingu. |
| Taka á móti flutningspöntun | Bókið móttöku flutningspöntunar fyrir allar flutningspöntunarlínur sem tengjast núverandi fólíói í tengdri sendingu. |
| Taka á móti vörum í flutningi | Takið á móti öllum pöntunarlínum sem eru í flutningi í fólíói. |
| Skjöl móttekin | Uppfæra skal stillingu á valkostinum **Skjöl móttekin** á *Já*. Hægt er að nota þennan hnapp til að læsa vöru-og/eða innkaupalínu til að ekki sé hægt að uppfæra hana meira. |
| Leita að sjálfvirkum kostnaði | Finna tengdan kostnað ferðar. Ef þessi kostnaður hefur þegar verið fundinn eða uppfærður birtast eftirfarandi skilaboð: „Óreikningsfærðar kostnaðarlínur eru til staðar. Á að skrifa yfir þetta? Athugið að ekki verður skrifað yfir kostnað ferðar sem er hengdur við fólíó og hefur verið reikningsfærður. |
| Stofna komubók | Mynda komubók fyrir fyrirtæki með því að nota ítarlega vöruhúsaeiginleika. Hægt er að velja **Frumstilla magn** (ráðlagt), **Stofna úr vörum í flutningi** og/eða **Stofna úr innkaupapöntunum**. Síðasti valkostur velturinn á því hvort verið er að nota vörur í flutningi. |
| Uppsafnaður kostnaður | Safna upp kostnaði þar sem kostnaðargerð er með fjárhagslykilinn tilgreindan fyrir debet. Þessi hnappur er vanalega notaður þegar birgðir eru í flutningi eða þegar vörur hafa verið mótteknar og reikningsfærðar. |

### <a name="buttons-on-the-general-tab"></a>Hnappar á flipanum Almennt

Eftirfarandi tafla lýsir hnöppunum sem eru í boði í flipanum **Almennt** á aðgerðasvæðinu.

| Hnappur | lýsing |
|---|---|
| Komulisti | Bókið innhreyfingaskjal fyrir allar innkaupapöntunarlínur í fólíói. Ef ferðir margra fyrirtækja eru notaðar opnast nýr svargluggi fyrir bókun innhreyfingaskjals fyrir hvert fyrirtæki. |
| Innhreyfingarskjal afurða | Skoðið færslu innhreyfingarskjals afurðar ef það er notað. |
| Vörumóttaka | Skoðið komubók vörunnar ef hún er notuð. |
| Fyrirspurn um kostnað | Opnið síðu kostnaðarfyrirspurnar til að skoða allan kostnað ferðar, þ.m.t. gám, fólíó og innkaupapöntun. Hægt er að breyta yfirliti síðunnar með því að nota yfirlitsaðgerðina. Á síðu kostnaðarfyrirspurnar er hægt að skoða öll svæðin ásamt vörunni og kóða kostnaðargerðar. Með því að fjarlægja þessi atriði er hægt að breyta síðunni með því að flokka saman kostnað. Þessi eiginleiki getur komið sér vel ef þú ert að nota stærðir og liti. Hægt er að breyta víddunum sem sýndar eru á síðunni. Síðan **Kostnaður** sýnir aðeins kóða kostnaðargerðar þar sem færslan **Dr** í flipanum **Bókun** er stillt á *Vara*. |

## <a name="header-view"></a>Hausyfirlit

Til að opna yfirlitið **Haus** skal opna ferð og síða velja flipann **Haus** uppi hægra megin í síðuhaus fólíós.

### <a name="settings-on-the-general-fasttab"></a>Stillingar á flýtiflipanum Almennt

Eftirfarandi tafla lýsir reitunum sem eru í boði í flýtiflipanum **Almennt** í yfirlitinu **Haus** fyrir fólíó.

| Svæði | lýsing |
|---|---|
| Fólíó | Heiti fólíós. Þetta heiti er sjálfkrafa myndað þegar fólíóið er stofnað.|
| Ferð | Ferðin sem tengist fólíóinu. |
| Tollmiðlari | Veljið tollmiðlara fyrir fólíóíð. Tollmiðlarar eru skilgreindir í lánardrottni. Þeir gera kleift að ákvarða stofnaðan kostnað sjálfkrafa. |
| Grunnflugfarmbréf/farmbréf | Tilgreinið grunnflugfarmbréf eða farmbréf sem á við um fólíóið. |
| Fyrirt.   | Lögaðilinn (fyrirtækið) sem tengist fólíóinu. |
| Eftirlitsnúmer farms | Þessi reitur er notaður af tolladeildinni í sumum löndum og svæðum. |
| Mæling | Þessi reitur gerir notendum kleift að tilgreina mælingu í einingunni **Heildarkostnaður**. Mælingar eru oft notaðar af fyrirtækjum sem vita ekki rúmmál eða þyngd á hverri vöru fyrir sig, en þurfa nákvæmari skiptingu en upphæðin eða magnið gefur til kynna. Flutningsmiðlarinn gefur upp þyngd eða rúmmálsmælieiningu og hægt er að setja hana inn á annaðhvort stigi vöru eða innkaupapöntunar. Hægt er að uppfæra hana sjálfkrafa ef færibreytan er valin eða færð inn handvirkt. |
| Mælieining | Einingin sem á við tilgreinda mælingu. |
| Fjöldi kassa | Fjöldi kassa í fólíói. Hægt er að uppfæra þennan reit sjálfkrafa, allt eftir því hvaða færibreyta hefur verið valin. |
| Lykill lánardrottins | Veljið lánardrottin sem tengist fólíóinu. Þetta svæði er eingöngu ætlað til upplýsinga. Það hefur ekki áhrif á neina virkni. |
| Nafn | Nafn á völdum lánardrottnalykli. |
| Athugasemdir | Færið inn allar viðbótarupplýsingar sem tengjast fólíói. |
| Lýsing á vörum | Veljið lýsingu vöru til að auðvelda að auðkenna fólíóið. Frekari upplýsingar er að finna í [Lýsing á vörum](shipping-information-setup.md#description-of-goods). |
| Dagsetning mats | Þessi reitur tengist tollfærslusíðunni. Einingin **Heildarkostnaður** mun nota tollgengið fyrir dagsetninguna sem stillt er hér. Sjálfgefið gildi er dagsetningin á tollfærslusíðunni. |
| Tollkenni | Færið inn tollkennið. Tolldeildirnar í löndum eða svæðum útvega þetta kenni. |
| Kóði tollflokks | Sláið inn kóða tollflokks sem tengist fólíóinu. Yfirleitt er krafist þessa kóða (og hann skilgreindur) eftir landinu eða svæðinu sem senda á til. |

### <a name="settings-on-the-delivery-fasttab"></a>Stillingar á flýtiflipanum Afhending

Eftirfarandi tafla lýsir stillingunum sem eru í boði í flýtiflipanum **Afhending** í yfirlitinu **Haus** fyrir fólíó.

| Svæði | lýsing |
|---|---|
| Dagsetning fólíós | Veljið dagsetningu til að tengja við fólíóið. Sjálfgefið gildi er stofndagur ferðarinnar. |
| Áætlaður komutími til afhendingarhafnar | Áætlaður komutími á afhendingarhöfn („til“ höfn). |
| Áætluð afhendingardagsetning | Yfirleitt dagsetningin þegar vörurnar eiga að koma í vöruhúsið. Þessi reitur er notaður þegar áætlaður afhendingardagur er reiknaður. (Áætlaður afhendingardagur rakningarstjórnunar er notaður í staðinn.) Til að stilla þennan reit þannig að gildið passi við áætlaðan afhendingardag rakningarstjórnunar skal nota [Stjórnstöð rakningar](delivery-information-setup.md#tracking-control-center). |
| Upprunaleg skjöl móttekin | Dagsetningin þegar upprunaleg skjöl voru móttekin. |
| Ráðlegging miðlara | Dagsetningin þegar miðlari var spurður álits. |
| Upprunalegt farmbréf sent | Dagsetningin þegar upprunalegt farmbréf var sent. |
| Vörur losaðar | Dagsetningin þegar vörur voru losaðar. |
| Fundur viðskiptavinar | Fundardagsetning viðskiptavinar. |
| Afhent í vöruhúsi | Dagsetningin þegar vörur voru afhentar í vöruhúsinu. |
| Staðfestingardagsetning | Staðfestingardagsetningin. |
| Leiðbeiningar um afhendingu | Dagsetningin þegar leiðbeiningar um afhendingu voru mótteknar. |
| Frá höfn | Höfnin sem ferðin fer frá. |
| Til hafnar | Höfnin sem ferðin fer til. Gámurinn gæti verið með mismunandi höfn vegna þess að skipið gæti haft viðdvöl í mörgum höfnum. |

### <a name="settings-on-the-export-fasttab"></a>Stillingar á flýtiflipanum Flytja útflutningur

Eftirfarandi tafla lýsir stilllingunum sem eru í boði í flýtiflipanum **Útflutningur** í yfirlitinu **Haus** fyrir fólíó.

| Svæði | lýsing |
|---|---|
| Útflutningsaðili | Hægt er að vista útflutningsaðilann í fólíóinu. Í alþjóðlegum viðskiptum gæti innkaupapöntun verið send á eitt fyrirtæki, en vörurnar fengnar frá öðru fyrirtæki. Tollayfirvöld krefjast rakningar og fylgigagna. Hægt er að vista heiti og aðsetur útflutningsaðila hér. |
| Nafn | Nafn valinns útflytjanda. |

## <a name="lines-view"></a>Línuyfirlit

Til að opna yfirlitið **Línur** skal opna ferð og síða velja flipann **Línur** uppi hægra megin í síðuhaus fólíós.

### <a name="information-on-the-folio-fasttab"></a>Upplýsingar á flýtiflipanum Fólíó

Flýtiflipinn **Fólíó** í yfirlitinu **Línur** sýnir upplýsingar um fólíóið. Flestar þessara upplýsinga birtast einnig í yfirlitinu **Haus** eins og lýst er hér á undan í þessu efnisatriði.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Upplýsingar og hnappar í flýtiflipanum fyrir línur

Flýtiflipinn **Línur** í yfirlitinu **Línur** sýnir upplýsingar um hverja fulla eða hluta til fulla innkaupapöntunarlínu sem er höfð með í núverandi fólíó.

Eftirfarandi tafla lýsir hnöppunum sem eru á í boði í flýtiflipanum **Línur** í yfirlitinu **Línur**.

| Hnappur | lýsing |
|---|---|
| Fjarl. | Fjarlægið valda innkaupapöntunarlínu úr ferðinni. |
| Birgðafærslur \> | Skoðið birgðafærslur fyrir valda innkaupapöntunarlínu. Athugið að ef notaðar eru vörur í flutningi eru einnig upprunaleg pöntun og vöruflutningspantanir sýndar. |
| Birtar víddir \> birgða | Opnið svarglugga þar sem hægt er að velja birgðavíddirnar sem eru sýndar fyrir færslurnar sem eru skoðaðar. |
| Uppfæra | Uppfærið upplýsingar sem tengjast línuupphæð, þyngd eða magni valinnar innkaupapöntunarlínu. |

### <a name="information-on-the-lines-details-fasttab"></a>Upplýsingar á flýtiflipanum Línur

Flýtiflipinn **Upplýsingar um línu** í yfirlitinu **Línur** veitir upplýsingar um innkaupapöntunarlínuna sem er valin í flýtiflipanum **Línur**.
