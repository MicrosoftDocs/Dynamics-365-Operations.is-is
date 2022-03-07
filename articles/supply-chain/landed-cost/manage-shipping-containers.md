---
title: Stjórna gámum
description: Þetta efnisatriði útskýrir hvernig á að vinna með gáma. Gámar eru notaðir til að flokka saman vörur sem eru efnislega flokkaðar saman. Þeir eru einnig notaðir í tilvikum þar sem aðeins er hægt að deila kostnaði niður á þessar vörur, yfirleitt vegna þess að þær eru efnislega saman.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: d3a47aa2ae36cd36a7e92aa2503252021e03f739
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573778"
---
# <a name="manage-shipping-containers"></a>Stjórna gámum

[!include [banner](../../includes/banner.md)]

Gámar eru notaðir til að flokka saman vörur sem eru efnislega flokkaðar saman. Þeir eru einnig notaðir í tilvikum þar sem aðeins er hægt að deila kostnaði niður á þessar vörur, yfirleitt vegna þess að þær eru efnislega saman.

Til að skoða og vinna úr vörum í gegnum gámasíðuna skal fara í **Heildarkostnaður \> Gámar \> Allir gámar**. Síðan **Allir gámar** sýnir lista yfir alla tiltæka gáma. Hægt er að nota hnappana á aðgerðasvæðinu til að stofna, eyða eða vinna með gáma. Veljið einhvern gám af listanum til að skoða upplýsingar um hann á síðunni **Gámar**.

Efri hlutinn á upplýsingasíðu gámsins sýnir upplýsingar um gám og kostnaðarútreikning. Hlutinn **Línur** sýnir fólíó, vörur og innkaupapantanir eða flutningspantanir sem eru hengdar við gáminn.

## <a name="action-pane"></a>Aðgerðasvæði

Aðgerðasvæðið á síðunum **Allir gámar** og **Gámar** býður upp á hnappa sem gera kleift að vinna með valinn gám. Hver hnappur framkvæmir eina aðgerð. Aðgerðarsvæðið inniheldur líka flipa sem hver um sig býður upp á sett af svipuðum hnöppum. Nema þar sem annað er tekið fram, er öllum hnöppum og flipum sem lýst er í eftirfarandi undirhlutum tiltækir bæði á listayfirlitinu (þ.e. á síðunni **Allir gámar**) og í ítarlega yfirlitinu (þ.e. á síðunni **Gámar**).

### <a name="buttons-on-the-manage-tab"></a>Hnappar á stjórnunarflipanum

Eftirfarandi tafla lýsir hnöppunum sem eru í boði í flipanum **Stjórna** á aðgerðasvæðinu.

| Hnappur | Lýsingar |
|---|---|
| Bóka innhreyfingalista | Bókið innhreyfingaskjal eða skoðið innhreyfingarskjöl afurða fyrir allar innkaupapöntunarlínur í gámnum. Ef sendingar margra fyrirtækja eru notaðar opnast nýr svargluggi fyrir bókun innhreyfingaskjals fyrir hvert fyrirtæki. |
| Bóka innhreyfingarskjal afurða | Bóka innhreyfingarskjal fyrir allar innkaupapantanalínur í gáminum. |
| Bóka reikning | Bókið reikning fyrir allar innkaupapöntunarlínur í gámnum. Ef sendir margra fyrirtækja eru notaðar opnast nýr svargluggi fyrir bókun reiknings fyrir hvert fyrirtæki. |
| Senda flutningspöntun | Bókið sendingu flutningspöntunar fyrir allar flutningspöntunarlínur gámsins. Aðeins þær línur í gámnum sem eru af gerð flutningspöntunar birtast í svarglugganum. |
| Taka á móti flutningspöntun | Bókið móttöku flutningspöntunar fyrir allar flutningspöntunarlínur gámsins. Svargluggi móttökunnar er einfaldasta leiðin til að taka á móti vörum í gámi eða ferð og er einn af þremur mögulegum leiðum. Einnig er hægt að taka á móti í gegnum komubækur eða úrvinnslu fartækis. |
| Stofna komubók | Hægt er að mynda komubók fyrir fyrirtæki með því að nota ítarlega vöruhúsaeiginleika. Valkostirnir eru _Frumstilla magn_ (ráðlagt) og annaðhvort _Stofna úr vörum í flutningi_ eða _Stofna úr innkaupapöntunum_. Síðustu tveir valkostirnir eru háðir því hvort verið er að nota vörur í flutningi. |
| Endurnefna | Opnið svarglugga þar sem hægt er að endurnefna valdan gám. |
| Breyta sniðmáti ferðar | Breyta ferðasniðmáti. Þegar ferðasniðmátinu hefur verið breytt gæti þurft að velja **Leita að sjálfvirkum kostnaði** eða bæta kostnaði við aftur handvirkt vegna þess að sendingarkostnaðinum verður eytt. |
| Breyta í leigu | Breytið völdum gámi í leigugám. |

### <a name="buttons-on-the-general-tab"></a>Hnappar á flipanum Almennt

Eftirfarandi tafla lýsir hnöppunum sem eru í boði í flipanum **Almennt** á aðgerðasvæðinu.

| Hnappur | Lýsingar |
|---|---|
| Komulisti | Bókið innhreyfingaskjal fyrir allar innkaupapöntunarlínur gáminum. Ef ferðir margra fyrirtækja eru notaðar opnast nýr svargluggi fyrir bókun innhreyfingaskjals fyrir hvert fyrirtæki. |
| Innhreyfingarskjal afurða | Skoðið færslu innhreyfingarskjals afurðar ef það er notað. Ferli innhreyfingarskjals verður aðeins notað ef vörurnar nota ekki virkni vöruflutninga. |
| Vörumóttaka | Skoðið komubók vörunnar fyrir gáminn ef sú færslubók er notuð. |
| Leggir | Leggir eru notaðir til að auðkenna aðskilda hluta ferðar. Hægt er að tengja afhendingartíma við hvern legg til að aðstoða við rakningu sendingar. Frekari upplýsingar er að finna í [Uppsetning ferðar með mörgum leggjum](multi-leg-journey-setup.md). |
| Rakning | Skoða eða uppfæra sendingarakningu. |
| Vöruflutningspantanir | Hægt er að opna síðuna **Vörur í flutningi** beint úr gámnum. Sú síða sýnir aðeins færslur fyrir vörur í flutningi fyrir valinn gám. |

## <a name="header-view"></a>Hausyfirlit

Til að opna yfirlitið **Haus** skal opna gám og síðan velja flipann **Haus** uppi hægra megin í síðuhaus gáms.

### <a name="settings-on-the-general-fasttab"></a>Stillingar á flýtiflipanum Almennt

Eftirfarandi tafla lýsir stillingunum sem eru í boði í flýtiflipanum **Almennt** í yfirlitinu **Haus** fyrir gám.

| Svæði | lýsing |
|---|---|
| Gámur | Heiti gáms. |
| Ferð | Ferðin sem tengist gámnum. |
| Gámagerð | Slá inn gámagerð sendingar. Stilla verður reitinn. Hægt er að nota hann til að ákvarða kostnað fyrir farm, til dæmis með því að velja sjálfvirkan kostnað sem tengist gámagerðinni. |
| Skip | Færa inn eða velja skip. Ef skipið er ekki gefið upp sem gildi er hægt að færa inn auðkenni skipsins sem frjálsan texta. Í því tilfelli er aðaltaflan ekki uppfærð þannig að hægt er að velja auðkenni skipsins seinna í þessum reit. Frekari upplýsingar er að finna í [Skip](shipping-information-setup.md#vessels). |
| Einingargerð | Einingargerðir eru notaðar sem viðbót við flokkun og auðkenningu gáma. Þær eru sýndar og valdar á gámasíðunni. Frekari upplýsingar er að finna í [Setja upp einingagerðir](shipping-container-setup.md#unit-types). |
| Gerð kælingar | Kæligerðir eru notaðar sem viðbót við flokkun og auðkenningu gáma, yfirleitt kæligáma. Þær eru sýndar og valdar á gámasíðunni. Frekari upplýsingar er að finna í [Setja upp kæligerðir](shipping-container-setup.md#refrigeration-types). |
| Mæling | Þessi reitur gerir notendum kleift að tilgreina mælingu í einingunni **Heildarkostnaður**. Mælingar eru oft notaðar af fyrirtækjum sem vita ekki rúmmál eða þyngd á hverri vöru fyrir sig, en þurfa nákvæmari skiptingu en upphæðin eða magnið gefur til kynna. Flutningsmiðlarinn gefur upp þyngd í kílógrömmum eða rúmmálsmælieiningu og hægt er að setja hana inn á annaðhvort stigi vöru eða innkaupapöntunar. Hægt er að uppfæra hana sjálfkrafa ef færibreytan er valin eða færa hana inn handvirkt. |
| Mælieining | Mælieiningin sem gildir um númerið í reitnum **Mæling**. |
| Raunþyngd | Hægt er að skrá raunþyngd kassans eða gámsins. Hægt er að nota þetta gildi fyrir staðfestingu á móti hámarksþyngd sem leyfð er í uppsetningu gáms. |
| Fjöldi kassa | Fjöldi kassa er sjálfkrafa uppfærður ef færibreytan er valin. |
| Lýsing á vörum | Hægt er að velja lýsingu á vörum í haus gáms eða fólíós. Hún er notuð til að hjálpa til við að auðkenna vörur í ferð, gámi eða fólíó. Frekari upplýsingar er að finna í [Lýsing á vörum](shipping-information-setup.md#description-of-goods). |
| Grunnflugfarmbréf/farmbréf | Hægt er að tilgreina grunnflugfarmbréf eða farmbréf fyrir gáminn. |
| Athugasemdir | Frekari upplýsingar sem tengjast gámnum. |
| Hægt að skila | Gildi sem segir til um hvort hægt er að skila gámnum eftir ferðina. |
| Staða ferðar | Staða ferðarinnar sem tengist gámnum. |
| Staða innkaupapöntunar | Staða innkaupapöntunarinnar sem tengist gámnum. |

### <a name="settings-on-the-delivery-fasttab"></a>Stillingar á flýtiflipanum Afhending

Eftirfarandi tafla lýsir stillingunum sem eru í boði í flýtiflipanum **Afhending** í yfirlitinu **Haus** fyrir gám.

| Svæði | lýsing |
|---|---|
| Tími og dagsetning stofnunar | Dagsetning og tími þegar gámurinn var stofnaður. |
| Dagsetning útflutningsverksmiðju | Þessi dagsetning er yfirleitt gefin upp til verksmiðju/lánardrottins til að gefa til kynna hvenær áætlað er að vörurnar yfirgefi svæðið. Þegar unnið er með verksmiðju í Asíu er þessi dagsetning oft nauðsynleg í stað dagsetningarinnar sem búist er við að fá vörurnar. (Fyrir afhendingu í nágrenninu er aftur á móti krafist dagsetningar fyrir hvenær búist er við að fá vörurnar.) Hægt er að fylla í þennan reit úr innkaupapöntunarlínum í gámalistanum. Einnig er hægt að færa það inn handvirkt hér. |
| Sendingardagsetning | Hægt er að prenta þessa dagsetningu á skjal innkaupapöntunar. Hún upplýsir venjulega verksmiðju/lánardrottin um dagsetninguna þegar afhenda á vörurnar á höfnina. Þetta svæði er eingöngu ætlað til upplýsinga. Hún er ekki notuð til að áætla væntanlegan afhendingardag varanna í gámnum. Hægt er að stilla þennan reit þannig að sé sjálfkrafa uppfærður þegar síða rakningarstýringar er uppfærð. |
| Dagsetning inn í verslun | Fyrsta dagsetning þegar vörur úr innkaupapöntunum sem eru tengdar við ferðina verða tiltækar fyrir sölu.|
| Áætluð afhendingardagsetning | Yfirleitt dagsetningin þegar vörurnar eiga að koma í vöruhúsið. Þetta svæði er eingöngu ætlað til upplýsinga. Hann er ekki notaður til að reikna út aðaláætlanagerð í innkaupapöntunarlínunum í gámnum. Væntanleg afhendingardagsetning í innkaupapöntunarlínunum er uppfærð með rakningarstjórn. Hægt er að setja upp þennan reit þannig að hann sé uppfærður þegar síða rakningarstjórnunar er uppfærð. |
| Brottfarartími | Vanalega dagsetningin þegar flugvél eða skip leggur af stað. |
| Áætlaður komutími til afhendingarhafnar | Áætlaður komudagur í áfangahöfn („til“ höfn). |
| Upprunaleg skjöl móttekin | Valfrjálst: Uppfærið dagsetninguna þegar upprunaleg skjöl voru móttekin. |
| Ráðlegging miðlara | Valfrjálst: Uppfærið dagsetninguna þegar miðlari var spurður álits. |
| Upprunalegt farmbréf sent | Valfrjálst: Uppfærið dagsetninguna þegar upprunalegt farmbréf var sent. |
| Vörur losaðar | Valfrjálst: Uppfærið dagsetninguna þegar vörurnar voru losaðar. |
| Fundur viðskiptavinar | Valfrjálst: Uppfærið fundardagsetningu viðskiptavinar. |
| Afhent í vöruhúsi | Valfrjálst: Uppfærið dagsetninguna þegar vörurnar voru afhentar í vöruhúsinu. |
| Staðfestingardagsetning | Valfrjálst: Uppfæra staðfestingardagsetninguna. |
| Leiðbeiningar um afhendingu | Valfrjálst: Uppfærið dagsetningu á leiðbeiningum afhendingar. |
| Frá höfn | Höfnin sem vörurnar verða sendar frá. |
| Til hafnar | Höfnin sem vörurnar verða sendar til. |
| Staðbundinn miðlari | Þetta svæði er eingöngu ætlað til upplýsinga. Staðbundinn miðlara á að vera hægt að velja úr töflu lánardrottins. |
| Dagsetning staðbundins flutnings | Sláið inn dagsetningu sem staðbundinn flutningur er bókaður fyrir. Þessi reitur getur hjálpað vöruhúsinu að gera áætlanagerð. |
| Staðbundinn flutningstími | Færið inn tímahólf. Þessi reitur getur hjálpað vöruhúsinu að gera áætlanagerð. |
| Sniðmát ferðar | Ferðasniðmátið sem er tilgreint fyrir ferðina. Sniðmát ferðarinnar veitir upplýsingar um „til“ og „frá“ hafnir og afhendingartíma sem tengjast rakningarstjórnun gámsins. |

### <a name="settings-on-the-other-fasttab"></a>Stillingar á flýtiflipanum Annað

Eftirfarandi tafla lýsir stillingunum sem eru í boði í flýtiflipanum **Annað** í yfirlitinu **Haus** fyrir gám.

| Svæði | lýsing |
|---|---|
| Leiga | Gildi sem segir til um hvort gámurinn sé leigugámur. Leigukostnaður gæti átti við um leigugáma. |
| Breytt í leigu | Gildi sem segir til um hvort gámnum hafi verið breytt í leigugám. Leigukostnaður gæti átti við um leigugáma. |
| Upprunaleg ferð | Ef gámurinn var færður yfir á nýja ferð, upprunalega ferð. |
| Notað | Notið þetta til að skrá hvort gámurinn hafi verið notaður. Því er aðeins ætlað að veita upplýsingar. |
| Væntanleg hleðsludagsetning | Dagsetningin þegar áætlað er að gámurinn verði hlaðinn af vörum. |
| Raðnúmer okkar | Sláið inn raðnúmerið sem fyrirtækið notar innanhúss fyrir gáminn. |
| Raðnúmer flutningsfyrirtækis | Færið inn raðnúmerið sem flutningsfyrirtækið eða umboðsaðilinn gaf upp fyrir gáminn. |
| Upphafsdagsetning gerðarprófunarvottorðs | Dagsetningin þegar beðið var um skoðun á gámnum. |
| Móttökudagsetning gerðarprófunarvottorðs | Dagsetningin þegar skoðunarvottorð var móttekið. |
| Lokadagsetning gerðarprófunarvottorðs | Dagsetningin þegar skoðunarvottorðið rennur út. |
| Númer gerðarprófunarvottorðs | Númer vottorðs sem var gefið út eftir skoðun. |

## <a name="lines-view"></a>Línuyfirlit

Til að opna yfirlitið **Línur** skal opna ferð og síðan velja flipann **Línur** uppi hægra megin í síðuhaus gáms.

### <a name="information-on-the-shipping-container-fasttab"></a>Flýtiflipi gámaupplýsinga

Flýtiflipinn **Gámur** í yfirlitinu **Línur** sýnir upplýsingar um fólíóið. Flestar þessara upplýsinga birtast einnig í yfirlitinu **Haus** eins og lýst er hér á undan í þessu efnisatriði.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Upplýsingar og hnappar í flýtiflipanum fyrir línur

Flýtiflipinn **Línur** í yfirlitinu **Línur** sýnir upplýsingar um hverja fulla eða hluta til innkaupapöntunarlínur sem eru hafðar með í núverandi gámi.

Eftirfarandi tafla lýsir hnöppunum sem eru á í boði í flýtiflipanum **Línur** í yfirlitinu **Línur**.

| Hnappur | lýsing |
|---|---|
| Fjarl. | Fjarlægið valda innkaupapöntunarlínu úr ferðinni. |
| Birgðafærslur \> | Skoðið birgðafærslur fyrir valda innkaupapöntunarlínu. Athugið að ef notaðar eru vörur í flutningi eru einnig upprunaleg pöntun og vöruflutningspantanir sýndar. |
| Birtar víddir \> birgða | Opnið svarglugga þar sem hægt er að velja birgðavíddirnar sem eru sýndar fyrir færslurnar sem eru skoðaðar. |
| Uppfæra | Uppfærið upplýsingar sem tengjast línuupphæð, þyngd eða magni valinnar innkaupapöntunarlínu. |

### <a name="information-on-the-lines-details-fasttab"></a>Upplýsingar á flýtiflipanum Línur

Flýtiflipinn **Upplýsingar um línu** í yfirlitinu **Línur** veitir upplýsingar um innkaupapöntunarlínuna sem er valin í flýtiflipanum **Línur**.
