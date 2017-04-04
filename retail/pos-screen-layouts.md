---
title: "Skilgreina skjá útlit fyrir Sölustað"
description: "Þetta efni veitir upplýsingar um afgreiðsluskjás fyrir Microsoft Dynamics 365 aðgerða - stað Retail reynslu sölu (POS)."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Skilgreina skjá útlit fyrir Sölustað

Þetta efni veitir upplýsingar um afgreiðsluskjás fyrir Microsoft Dynamics 365 aðgerða - stað Retail reynslu sölu (POS).

Hægt er að skilgreina Microsoft Dynamics 365 aðgerða - stað Retail notendaviðmótinu sölu (POS) með samsetningu sjónrænar reglur og útlit afgreiðsluskjás, úthlutað á verslanir, afgreiðslukassar, og/eða notendur.

## <a name="visual-profile"></a>Sjónræn regla
Sjónrænar reglur er úthlutað á afgreiðslukassa og eru notaðir til að tilgreina visual einingar sem eru sérstaklega afgreiðslukassa og samnýtta yfir notendur. Notendur sem skráir sig inn á afgreiðslukassa hefur sama þema, liti og myndir. **Reglunúmer** -forstilling er einkvæmt auðkenni fyrir Sjónræna reglu. **Lýsing** -lýsing gerir kleift að tilgreina auðskilið nafn hjálpar til við að auðkenna rétt forstillingunni hverju tilviki. **Þema** -Notendur hægt er að velja milli Light eða Dökkra forritsþemu. Þessar stillingar áhrif letursliti og bakgrunnsliti liti í gegnum forritið. **Litur áherslulitar** -áherslulitur Sem er notuð alls staðar á Sölustaðnum til að aðgreina eða merkið tilteknar einingar visual reitir, skipunarhnappa eða tengla. Þessar einingar eru yfirleitt hluta. **Litur haus** -litur haus leyfir notandanum að skilgreina lit blaðsíðuhaus til að uppfylla branding á retailer. Þessi eiginleiki er aðeins tiltækur í Dynamics 365 fyrir útgáfu Aðgerðir 1611. **Innskráning backgrounds** -Notendur er hægt að tilgreina bakgrunnsmynd fyrir innskráningu skjánum. Skrá stærð bakgrunnur myndir á að halda sem lítið sem hægt er og geymslu og hlaða stórar skrár geta haft áhrif á virkni forritsins og afköst. **Forritið-bakgrunnur** -POS Er einnig hægt að nota mynd sem bakgrunnur gjörvallt kerfið stað solid þema lit. Með innskráningu backgrounds, það er látinn vita að geyma stærð lágmarksréttindi eins og mögulegt.

## <a name="screen-layouts"></a>Útlit afgreiðsluskjás
Skilgreining útlit afgreiðsluskjás ákvarðar aðgerðir, efni og staðsetning UI stýrir í skjánum Sölustaður Velkomin(n) og færsluskjár. ** Upphafsskjár **-í flestum tilvikum í upphafsskjár er síðan notendur sjá þegar þeir fyrst skrá inn á Sölustað. Upphafsskjár sem getur verið samsett branding mynd og hnappahnit sem veita aðgang að aðgerðir Sölustaðar. Aðgerðir sem eiga sérstaklega við gildandi færslu eru yfirleitt settar hér. **Færsluskjár** -í færsluskjár er aðal skjánum Sölustaður í fyrir vinnslu sölufærslur og pantanir. Hægt er að skilgreina skjánum Færslan með útlitshönnuður afgreiðsluskjás. **Sjálfgefin ræsa skjánum** -Sumar smásala stilltu sem gjaldkeri fara beint í færsluskjár eftir innskráningu. Sjálfgefin ræsing skjánum stilling gerir notendum kleift að setja þetta fyrir hvern útlit afgreiðsluskjás.

### <a name="assignment"></a>Verkefni

Hægt er að úthluta útlit afgreiðsluskjás á verslun, afgreiðslukassa eða notandi stigi. Úthlutun notanda hnekkir afgreiðslukassa og geyma úthlutun og skrá úthlutun hnekkingar úthlutun verslun. Í einfalt dæmi þar sem allir notendur notað sama útlit, afgreiðslukassa eða hlutverk, skjásins má setja aðeins í verslun. Í tilfellum þar sem tilteknar afgreiðslukassa eða notendur þurfa specialized útlit hægt er að úthluta þeim hæfilega.

### <a name="layout-sizes"></a>Útlitsstærðir

Þessi eiginleiki aðeins við Dynamics 365 Aðgerðir útgáfu 1611. Vegna þess að í mörgum tilvikum afgreiðsluskjás hægt er að nota skjánum stærðir og úrlausnir notendur hægt er að skilgreina þeirra snið og innihald fyrir hverja. POS forritið mun sjálfkrafa velja næst er afhendingardegi útlit stærð fyrir tækið við ræsingu. Útlit skjás getur einnig innihaldið skilgreiningar fyrir bæði fullu og compact tæki. Þessi skilgreining leyfir notanda sem á að úthluta á einn skjásins sem verður að vinna í mismunandi stærðum og stuðla skjámynd innan verslunarinnar. **Modern POS - Full** -Fullt útlit yfirleitt best notaðar fyrir stærri birtir PC monitors eða tablets. Notendur er hægt að velja hvaða einingar UI til að taka ákvarða stærðar- og staðsetning þeirra og skilgreina ítarlega eiginleika þeirra. Full útlit styðja sjónrænni og lárétt skilgreiningar. **Modern POS - Compact** -Compact útlit yfirleitt best notaðar fyrir símar eða lítil tablets. Hönnun möguleika takmarkast fyrir compact tæki. Notendur geta skilgreina dálka og svæði fyrir móttöku og rúður.

### <a name="screen-layout-designer"></a>Útlitshönnuður afgreiðsluskjás

Verður að skilgreina hverja útlit stærð innan útlit skjás með útlitshönnuður afgreiðsluskjás. Hönnuðurinn gerir notendum kleift að tilgreina og skilgreina UI einingar á skjánum Færslu. Útlitshönnuður afgreiðsluskjás notar ClickOnce til að sækja, setja upp og ræsa nýjustu útgáfu forritsins í hvert sinn sem notandi tengist henni. Gætið þess að villuleita kröfur fyrir vafra til að nota ClickOnce — sumar vöfrum Króm, svo sem krefjast viðauka. **Talnaborð** -í talnaborð er aðal notendainnsetningar í færsluskjár Sölustaðar. Hægt er að skilgreina það til að sýna öll on-screen takkaborð sem er tilvalið fyrir touchscreens, eða aðeins inntakssvæði, sem hægt er að nota með efnisleg lyklaborði. Númer stillingar takkaborðinu eru tiltækar í fullt útlit aðeins. Í Dynamics 365 Aðgerðir útgáfu 1611 compact útlit alltaf með í full talnaborð tiltæk skjánum Færslu. **Samtölugluggi** - hægt er að skilgreina á samtölugluggi í annaðhvort einn eða tvo dálka til þess að sýna svæði eins og lína talningu, afsláttarupphæð, gjöld, millisamtala og skatts. Í Dynamics 365 Aðgerðir útgáfu 1611 compact útlit styður eingöngu samtölur einn dálkur. **Kvittun** -** ** panel afurða inniheldur sölulínur, línur greiðslu og afhendingarupplýsingar fyrir afurðir og þjónustu sem vinna á sölustað. Notendur geta tilgreina dálka widths og staðsetning. Í compact í Dynamics 365 Aðgerðir útgáfu 1611, einnig hægt að skilgreina viðbótarupplýsingar sem mun birtast á línunni undir aðaltöflu línu. **Viðskiptavinakortið** - kort sýnir upplýsingar um viðskiptavin tilheyrir viðskiptavinar sem tengist færslunni. Hægt er að skilgreina viðskiptavinakortið til að fela eða sýna viðbótarupplýsingar. **Stjórna flipanum** - flipanum stýringu geta verið staðsettir á skjásins og aðrar stýringar borð við númer takkaborð viðskiptavinakortið, eða hnappahnit má setja inn á flipanum. Flipastýring sem er geymir sem hjálpar notendum að passa fleiri efni í skjánum. Flipastýring sem er aðeins tiltækur fyrir fulla útlit. ** Mynd **-mynd stýringin er hægt að nota til að sýna merki verslun eða öðrum branding mynd á skjánum færslu. Stjórna mynd er aðeins tiltækur fyrir fulla útlit. **Mælt er með afurðir** - Ef þetta er skilgreint fyrir það umhverfi ráðlögð afurðir fjárhagsáætlunarstýringar mun sýna afurð tillögur byggðar á vél nám. Afurðir sem mælt er með stýringu er aðeins tiltækur fyrir fulla útlit í Dynamics 365 fyrir útgáfu Aðgerðir 1611. ** Sérstillt stýring **-sérstillt stýring þjónar sem frátakara innan skjásins sem gerir notendum kleift að taka frá pláss fyrir sérsniðna efni. Sérstillt stýring er aðeins tiltækur fyrir alla útlit.

<a name="see-also"></a>Sjá einnig
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)


