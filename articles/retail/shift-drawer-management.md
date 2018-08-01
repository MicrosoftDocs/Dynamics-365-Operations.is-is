---
title: "Vakta- og peningaskúffustjórnun"
description: "Þetta efnisatriði útskýrir hvernig á að setja upp og nota vaktir á sölustað (POS)."
author: jblucher
manager: AnnBe
ms.date: 05/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: da5519eb0746347905e3b3d3d81161850c429f57
ms.openlocfilehash: f0856a3a36ff97773c0fadbe94fe680762c5206b
ms.contentlocale: is-is
ms.lasthandoff: 06/22/2018

---

# <a name="shift-and-cash-drawer-management"></a>Vakta- og peningaskúffustjórnun

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp og nota vaktir á sölustað (POS). 

Í Microsoft Dynamics 365 for Retail, lýsir hugtakið *vakt* söfnun POS færslugagna og aðgerða á milli tveggja tímapunkta. Fyrir hverja vakt er fjárhæðin sem búist er við borin saman við upphæðina sem var talin og gefin upp.

Venjulega eru vaktir opnaðar í byrjun vinnudags. Á þeim tímapunkti gefur notandi upp byrjunarupphæðina sem peningaskúffan inniheldur. Sölufærslur eru síðan framkvæmdar yfir daginn. Að lokum, í lok dagsins, er skúffan talin og lokaupphæðin er gefin upp. Vaktinni er lokað og Z skýrsla er búin til. Z skýrslan sýnir hvort upphæðin er of há eða of lág.

## <a name="typical-shift-scenarios"></a>Dæmigerð atburðarás á vakt
Retail býður upp á nokkra valkosti fyrir grunnstillingar og POS-aðgerðir til að styðja við fjölda viðskiptaferla sem keyrðir eru í lok dags fyrir POS. Þessi hluti lýsir nokkrum dæmigerðum atburðarásum á vakt.

### <a name="fixed-till"></a>Föst skúffa
Þessi atburðarás hefur oftast verið notuð. Hún er enn mikið notuð. Á „föst skúffa“ vakt, er vaktin og skúffan tengd við ákveðinn afgreiðslukassa. Þau eru ekki flutt frá einum afgreiðslukassa til annars. „Föst skúffa“ vakt er hægt að nota af einum notanda eða deilt meðal margra notenda. „Föst skúffa“ vaktir þurfa ekki neina sérstaka grunnstillingu.

### <a name="floating-till"></a>Fljótandi skúffa
Á „Fljótandi skúffa“ vakt er hægt að færa vakt og peningaskúffu frá einum afgreiðslukassa til annars. Þó að afgreiðslukassi megi aðeins hafa eina virka vakt á hverja peningaskúffu, er hægt að fresta vöktum og síðan halda áfram síðar eða á öðrum afgreiðslukassa.

Til dæmis hefur verslun tvo afgreiðslukassa. Hvert afgreiðslukassi er opnað í byrjun dags þegar gjaldkeri opnar nýjan vakt og gefur upp byrjunarupphæðina. Þegar einn gjaldkeri er tilbúinn til að taka hlé, frestar þessi gjaldkeri vaktinni sinni og fjarlægir skúffuna úr peningaskúffunni. Þessi afgreiðslukassi verður þá tiltækur fyrir aðra gjaldkera. Annar gjaldkeri getur skráð sig inn og opnað vaktina sína á afgreiðslukassanum. Eftir að vinnuhléi fyrsta gjaldkeri er lokið, getur sá gjaldkeri haldið áfram vaktinni sinni þegar einhver af hinum afgreiðslukassi verður tiltækur. „Fljótandi skúffa“ vaktir þurfa ekki sérstaka grunnstillingu eða heimild.

### <a name="single-user"></a>Einn notandi
Margir smásalar kjósa að leyfa aðeins einn notanda á hverja vakt, til að tryggja hæsta stigs ábyrgð fyrir reiðufénu í peningaskúffunni. Ef aðeins einn notandi er heimilt að nota skúffuna sem tengist vaktinni, getur þessi notandi verið einvörðungu ábyrgur fyrir misræmi. Ef fleiri en einn notandi nota vaktina, er erfitt að ákvarða hver gerði villu eða hver gæti verið að reyna að stela úr skúffunni.

### <a name="multiple-users"></a>Margir notendur
Sumir smásalar eru reiðubúnir að fórna þeirri hæsta stigs ábyrgð sem vaktir fyrir einn notanda veita og leyfa fleiri en einn notanda á hverja vakt. Þessi aðferð er dæmigerð þegar notendur eru fleiri en tiltækir afgreiðslukassar, og þörfin fyrir sveigjanleika og hraða vegur þyngra en hugsanlegt tap. Það er líka dæmigerð þegar verslunarstjórnendur eru ekki með sínar eigin vaktir en geta, eftir því sem þörf krefur, notað vaktir einhverra gjaldkeri þeirra. Til að skrá þig inn á og nota vakt sem opnað var af öðrum notanda, verður notandi að hafa **Heimila fjölinnskráningu á vakt** POS leyfið.

### <a name="shared-shift"></a>Samnýtt vakt
„Samnýtt vakt“ grunnstilling gerir smásala kleift að vera með eina vakt sem nær yfir margar afgreiðslukassa, peningaskúffur og notendur. Samnýtt vakt hefur eina byrjunarupphæð og einn lokaupphæð sem er tekin saman úr öllum peningaskúffum. Samnýttar vaktir eru mest dæmigerðar þegar fartæki eru notaðar. Í þessari atburðarás er ekki sérstakt peningaskúffa frátekið fyrir hvert afgreiðslukassa. Í staðinn geta allir afgreiðslukassar deilt einni peningaskúffu.

Ef nota á samnýttar vaktir í verslun, verður peningaskúffan að vera grunnstillt sem „samnýtt vakt skúffa“ í **Smásala \> Uppsetning rásar \> POS uppsetning \> POS forstillingar \> Vélbúnaðar snið \> Skúffa**. Að auki þurfa notendur að hafa einn eða báðar heimildir fyrir sameiginlegri vakt (Leyfa stjórnun á samnýtt vakt og Leyfa notkun á samnýtt vakt).

> [!NOTE]
> Aðeins einn samnýtt vakt getur verið opin í einu í hverri verslun. Hægt er að nota samnýtta vaktir og sjálfstæðar vaktir í sama verslunarinnar.

## <a name="shift-and-drawer-operations"></a>Vakta- og skúffuaðgerðir
Ýmsar aðgerðir er hægt að framkvæma til að breyta stöðu vaktar, eða til að auka eða minnka peningamagn í peningaskúffunni. Þessi kafli lýsir þessum vaktaaðgerðum fyrir Microsoft Dynamics 365 for Retail Modern POS og Cloud POS.

### <a name="open-shift"></a>Opna vakt
POS krefst þess að notendur hafi virka, opna vakt til að geta framkvæmt allar þær aðgerðir sem hafa í för með sér fjárhagsfærslu, eins og t.d. sala, skil eða pöntun viðskiptavinar.

Þegar notandi skráir sig í POS, staðfestir kerfið fyrst hvort virkt vakt sé í boði fyrir þann notanda á fyrirliggjandi afgreiðslukassa. Ef virk vakt er ekki tiltæk, getur notandinn opnað nýjan vakt, halda áfram með núverandi vakt eða skráð sig inn í „engin-skúffa“ stillingu, allt eftir grunnstillingu kerfis og heimildum notandans.

### <a name="declare-start-amount"></a>Skilgreina upphafsupphæð
Þessi aðgerð er oft fyrsta aðgerðin sem er gerð fyrir nýlega opnað vakt. Fyrir þessa aðgerð, tilgreina notendur byrjunarupphæð reiðufjár í peningaskúffunni fyrir vaktina. Þessi aðgerð er mikilvægt vegna þess að útreikningur á ofgreiðslu/ávöntun sem á sér stað þegar vakt er lokað tekur mið af byrjunarupphæðina.

### <a name="float-entry"></a>Skiptimyntarfærsla
*Skiptimyntafærslur* eru ekki-sölufærslur sem eru gerðar á virkri vakt til að auka reiðufjármagn í peningaskúffunni. Einkennandi dæmi um skiptimyntafærslu er færsla til að bæta við viðbótar skiptimynt í skúffuna þegar hún er í lágmarki.

### <a name="tender-removal"></a>Skiptimynt fjarlægð
*Skiptimynt fjarlægð* eru ekki-sölufærslur sem eru gerðar á virkri vakt til að draga úr reiðufjármagni í peningaskúffu. Þessi aðgerð er oftast notuð í tengslum við skiptimyntarfærsluaðgerð á annarri vakt. Til dæmis, vegna þess að skiptimynt í afgreiðslukassi 1 er í lágmarki, framkvæmir notandinn á afgreiðslukassa 2 aðgerðina skiptimynt fjarlægð til að draga úr upphæðinni í peningaskúffu sinni. Notandinn á afgreiðslukassa 1 framkvæmir þá skiptimyntarfærslu til að auka upphæðina í peningaskúffu sinni.

### <a name="suspend-shift"></a>Ljúka vakt
Notendur geta frestað virkri vakt sinni til að losa um núverandi afgreiðslukassa fyrir annan notanda eða færa vaktina sína í annað afgreiðslukassa (í þessu tilviki er vaktin oft nefndur „fljótandi skúffa“ vakt).

Frestun vaktar kemur í veg fyrir nýjar færslur eða breytingar á vaktinni þar til hún er hafin aftur.

### <a name="resume-shift"></a>Halda vakt áfram
Þessi aðgerð gerir notendum kleift að halda áfram frestuðum vöktum á öllum afgreiðslukössum sem er ekki þegar með virkan vakt.

### <a name="tender-declaration"></a>Talning skiptimyntar
Þessi aðgerð er framkvæmd til að tilgreina fyrirliggjandi heildarfjárhæð í peningaskúffunni. Notendur framkvæma oftast þessa aðgerð áður en þeir loka vakt. Tilgreind upphæð er borin saman við vaktaupphæð sem búist var við til að reikna upphæð ofgreiðslu/ávöntunar.

### <a name="safe-drop"></a>Peningaflutningur í öryggisskáp
Hægt er að framkvæma peningaflutning í öryggisskáp hvenær sem er á virkri vakt. Þessi aðgerð fjarlægir peninga úr peningaskúffunni þannig að hægt sé að flytja hann á öruggari stað eins og peningaskáp í bakherbergi. Heildarupphæðin sem er skráð fyrir peningaflutning í öryggisskáp er innifalin í samtölu vaktar, en þarf ekki að teljast sem hluti af talning skiptimyntar.

### <a name="bank-drop"></a>Peningaflutningur í banka
Eins og peningaflutningur í öryggisskáp, er peningaflutningur í banka einnig framkvæmdur á virkri vakt. Þessi aðgerð fjarlægir peninga af vaktinni til að undirbúa fyrir innlögn í banka.

### <a name="blind-close-shift"></a>Loka vakt blindandi
*Vaktir sem lokað er blint* eru ekki lengur virkir en hefur ekki verið lokað að fullu. Ólíkt vöktum í bið, er vaktir sem lokað er blint ekki hægt að opna aftur. Hins vegar, aðgerðir eins og gefa upp byrjunarupphæð og talning skiptimyntar er hægt að framkvæma á þeim seinna eða frá öðrum afgreiðslukassa.

Vaktir sem lokað er blint eru oft notaðar til að losa um afgreiðslukassa fyrir nýjan notanda eða vakt án þess að þurfa fyrst að fullu telja, afstemma og loka vaktinni.

### <a name="close-shift"></a>Loka vakt
Þessi aðgerð reiknar samtölu vaktar og ofgreiðslu/ávöntun fjárhæðir, og lýkur síðan virkri vakt eða vakt sem er lokað blint. Z-skýrsla er einnig prentuð fyrir vaktina, en það fer eftir heimildum notandans. Ekki er hægt að halda áfram með eða breyta lokaðar vaktir.

### <a name="print-x"></a>Prenta X
Þessi aðgerð býr til og prentar X-skýrslu fyrir núverandi virka vakt.

### <a name="reprint-z"></a>Endurprenta Z
Þessi aðgerð endurprentar síðustu Z skýrsluna sem kerfið bjó til þegar vakt var lokað.

### <a name="manage-shifts"></a>Stjórna vöktum
Þessi aðgerð gerir notendum kleift að skoða allar vaktir sem eru virkar, frestaðar og sem hefur verið lokað blint fyrir verslunina. Notendur geta framkvæmt lokunarferli sín, svo sem Talning skiptimyntar og Loka vakt aðgerðir fyrir vaktir sem er lokað blint, en það fer eftir heimildum þeirra. Þessi aðgerð leyfir einnig notendum að skoða og eyða ógildum vöktum, þá sjaldan að skilið er við vakt í slæmu ástandi eftir að skipt hefur verið á milli stillinga með og án nettengingar. Þessar ógildar vaktir innihalda ekki neinar fjárhagsupplýsingar eða færslugögn sem þarf til afstemmingar.

## <a name="shift-and-drawer-permissions"></a>Vakta- og skúffuheimildir
Eftirfarandi POS heimildir hafa áhrif á það sem notandi getur og getur ekki gert í ýmsum tilfellum:

- **Leyfa blinda lokun**
- **Leyfa prentun X-skýrslu**
- **Leyfa prentun á Z-skýrslu**
- **Leyfa talningu skiptimyntar**
- **Leyfa skilgreiningu skiptimyntar**
- **Opna skúffu án sölu**
- **Leyfa fjölinnskráningu á vakt** - Þessi heimild leyfir notandanum að skrá sig inn og nota vakt sem annar notandi opnaði. Notendur sem ekki hafa þessa heimild geta skráð sig inn og notað aðeins vaktir sem þeir hafa opnað.
- **Leyfa stjórnun samnýttar vaktar** - Notendur verða að hafa þetta leyfi til að opna eða loka samnýttri vakt.
- **Leyfa notkun samnýttrar vaktar** - Notendur verða að hafa þetta leyfi til að skrá sig inn og nota samnýtta vakt.

## <a name="back-office-end-of-day-considerations"></a>Umhugsunarefni í bakvinnslu að degi loknum
Það hvernig vaktir og afstemming peningaskúffur er notuð í POS er frábrugðið því hvernig færslugögn eru tekin saman við útreikning uppgjörs. Það er mikilvægt að þú skiljir þessa mismun. Vaktargögnin í POS (Z skýrslunni) og reiknuð uppgjör í bakvinnslu geta gefið þér mismunandi niðurstöður, allt eftir grunnstillingum þínum og viðskiptaferlum. Þessi munur þýðir ekki endilega að annað hvort vaktargögnin eða reiknuð uppgjör sé rangt eða að það sé vandamál með gögnin. Það þýðir bara að færibreyturnar sem eru veittar gætu falið í sér viðbótarfærslu eða færri færslur, eða að færslurnar hafi verið tekin saman á mismunandi hátt.

Þótt sérhver smásali hafi mismunandi viðskiptaskilyrði mælum við með því að þú setjir upp kerfið þitt á eftirfarandi hátt til að forðast aðstæður þar sem mismunur af þessu tagi kemur fram:

Farðu í **Smásala \> Rásir \> Smásöluverslanir \> Allar smásöluverslanir \> Uppgjör/lokun**, og fyrir hverja verslun skal stilla bæði **Uppgjörsaðferð** reitinn og **Lokunaraðferð** reitinn á **Vakt**.

Þessi uppsetning hjálpar til við að tryggja að bakvinnsluuppgjör innihaldi sömu færslur og vaktir í POS, og að gögnin séu tekin saman af þeirri vakt.

Frekari upplýsingar um uppgjör og lokunaraðferðir, sjá [Grunnstillingar verslunar fyrir smásöluuppgjör](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).

