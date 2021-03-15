---
title: Yfirlit yfir framleiðsluferli
description: Þetta efnisatriði veitir yfirlit yfir framleiðsluferlið. Hún lýsir mismunandi stigum framleiðslupantana, runupantana og kanbana, frá stofnun pöntunar til lokunar fjárhagstímabilsins.
author: cvocph
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, OpResLifecycleManagementWorkspace, ProdParmCostEstimation, ProdParmRelease, ProdSchedule, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19832
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a376510e76bdc9687f7fa9af5921ae7c50d1fc59
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998926"
---
# <a name="production-process-overview"></a>Yfirlit yfir framleiðsluferli

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir framleiðsluferlið. Hún lýsir mismunandi stigum framleiðslupantana, runupantana og kanbana, frá stofnun pöntunar til lokunar fjárhagstímabilsins. 

Framleiðsla á vörum, ferli sem er einnig þekkt sem líftími framleiðslu, fylgir ákveðnum skrefum sem þarf að ljúka við framleiðslu á vöru. Líftími hefst með stofnun framleiðslupöntunar, runupöntun eða kanban. Líftíma lýkur með lokinni, framleiddri vöru sem er tilbúin fyrir annaðhvort viðskiptavininn eða annan áfanga framleiðslu. Hvert skref í líftíma krefst mismunandi gerða upplýsinga til að ljúka ferlinu. Þegar hverju skrefi er lokið sýnir framleiðslupöntun, runupöntun eða kanban breytingu á framleiðslustöðu. Mismunandi gerðir afurða krefjast mismunandi framleiðsluferla.  

Kerfiseiningin **Framleiðslustýring** er tengd við aðrar kerfiseiningar, eins og **Upplýsingar um afurðastjórnun**, **Birgðastjórnun**, **Fjárhagur**, **Vöruhúsakerfi**, **Verkbókhald** og **Fyrirtækisstjórnun**. Þessi samþætting styður upplýsingaflæðið sem er krafist til að klára framleiðslu afurðar.  

Framleiðsluferlið verður vanalega fyrir áhrifum af kostnaðarbókhalds- og birgðamatsaðferðum sem eru valdar fyrir tiltekið framleiðsluferli. Supply Chain Management styður bæði raunkostnað (fyrst inn, fyrst út \[FIFO\]; síðast inn, fyrst út \[LIFO\]; hlaupandi meðaltal og reglubundið vegið meðaltal) og aðferðir staðalkostnaðar. Lean-framleiðsla er innleidd byggt á reglu bakfærslukostnaðaraðgerðarar.  

Val á kostnaðarmatsaðferðunum skilgreinir einnig kröfur um skýrslugerð um efni og tilfanganotkun meðan á framleiðsluferlinu stendur. Yfirleitt krefjast raunkostnaður aðferðir nákvæmra skýrslna á vinnslustigi en reglubundnar kostnaðarútreikningsaðferðir leyfa minna grófa skýrslugerð um efni og tilföng.

## <a name="mixed-mode-manufacturing"></a>Blönduð framleiðsla
Mismunandi afurðir og grannfræði framleiðslu krefjast beitingar á mismunandi pöntunargerðum. Supply Chain Management getur notað ýmsar gerðir pantana í blönduðum ham. Með öðrum orðum geta allar gerðir pantana átt sér stað á meðan vinnslum frá upphafi til enda í framleiðslu einnar endanlegrar afurðar.

-   **Framleiðslupöntun** – Þetta er hefðbundin gerð pöntunar til að framleiða tiltekna afurð eða afurðarafbrigði í ákveðnu magni á tiltekinni dagsetningu. Framleiðslupantanir eru byggðar á uppskriftum (BOMs) og leiðum.
-   **Runupöntun** – Þessi gerð pöntunar er notuð fyrir iðnaðarferli og aðskilin ferli þar sem umreikningur framleiðslu er byggður á formúlu, eða þar sem aukaafurðir og hliðarafurðir geta verið lokaafurðir viðbótar eða í stað aðallykil. Runupantanir nota **Formúlu** gerð uppskrifta og leiða.
-   **Kanban** – Kanban eru notaðar til að gefa merki um endurtekin ferli lean-framleiðslu sem byggja á framleiðsluflæðum, kanban-reglum og uppskriftum.
-   **Verk** – Framleiðsluverk sameinar afurðir og þjónustu við tiltekna greiðsluáætlun og fjárhagsáætlun. Hægt er að afhenda framleiðsluhluti verks í gegnum hvaða aðra gerð pöntunar sem er.

## <a name="manufacturing-principles"></a>Framleiðslureglur
Til að velja framleiðslureglu sem best á við um tiltekna vöru og tengdan markað verður að hugleiða þarfir framleiðslu og vörustjórnunar og einnig væntingar viðskiptavina um biðtíma afhendingar.

-   **Gera á lager** – Þetta er hefðbundin framleiðsluregla, þar sem vörur eru framleiddar fyrir birgðir, samkvæmt spá eða lágmarks áfyllingarmagni birgðatalningar (hið síðara er yfirleitt reiknað samkvæmt spá eða eldri notkun).
-   **Eftir pöntun** – Staðlaðar afurðir eru gerðar eftir pöntun eða lokið við pöntun. Þótt forframleiðsla gæti verið gerð með því að nota regluna Gera á lager eru dýr skref keðjugilda, eða skref sem búa til afbrigði, ræst með sölupöntun eða flutningspöntun.
-   **Skilgreina fyrir pöntun** – Eins og til fyrir regluna Fyrir pöntun eru endanlegar aðgerðir birgðakeðjustjórnunar gerðar eftir pöntun. Raunveruleg afurðarafbrigði sem er framleitt er ekki forskilgreint en er stofnað á um leið og pöntunarfærslan, byggt á afbrigðalíkani söluafurðarinnar. Reglan Skilgreina fyrir pöntun krefst ákveðins stigs ferlasameiningar fyrir afurð á tiltekna línu.
-   **Skipulagt eftir pöntun** – Ferli sem skipulögð eru eftir pöntun eru yfirleitt meðhöndluð eftir verki og hefjast venjulega með skipulagningaráfanga. Á meðan skipulagningaráfanganum stendur eru raunverulegar afurðir sem eru nauðsynlegar til að uppfylla pöntunina hannaðar og þeim lýst. Síðan er hægt að stofna framleiðslupantanir, runupantanir eða kanban til að framleiða afurðir.

## <a name="overview-of-the-production-life-cycle"></a>Yfirlit yfir framleiðsluferlið
Eftirfarandi skref í líftíma framleiðslu geta átt sér stað fyrir allar gerðir pöntunar í blönduðum framleiðsluham. Hins vegar eru þau ekki öll sýnd sem yfirlýst pöntunarstaða.

1.  **Stofnað** – Hægt er að stofna framleiðslupöntun, runupöntun eða kanban handvirkt, eða hægt er að stilla kerfið til að mynda þau samkvæmt mismunandi eftirspurnarmerkjum. Áætlanagerð stofnar framleiðslupantanir, runupantanir eða kanban með því að staðfesta áætlaðar pantanir. Önnur eftirspurnarmerki eru sölupantanir eða fest framboðsmerki frá öðrum framleiðslupöntunum eða kanban. Fyrir kanban með föstu magni eru eftirspurnarmerki mynduð þegar kanban eru skráð sem tóm.
2.  **Áætlað** - Hægt er að reikna áætlað efni og tilfanganotkun. Áætlunin myndar birgðafærslur fyrir hráefni sem hafa stöðuna **Í pöntun**. Kvittanir fyrir aðalafurðir, aukaafurðir og hliðarafurðir eru myndaðar þegar framleiðslupantanir eða runupantanir eru áætlaðar. Ef Uppskrift inniheldur línur af gerðinni **Fest framboð** eru innkaupapantanir fyrir efni eða úthýst virkniþjónusta myndaðar og festar við framleiðslupöntun eða runupöntun. Vörur eða pantanir eru teknar frá samkvæmt frátektarstefnu framleiðslupöntunar og verð fullbúnu vörunnar reiknað út á grundvelli stillinga færibreyta.
3.  **Tímasett** - Hægt er að gera áætlanir um framleiðslu byggðar á aðgerðum, einstökum vinnslum eða hvoru tveggja.
    -   **Aðgerðarröðun** – Þessi röðunaraðferð býður upp á grófa langtímaáætlun. Með þessari aðferð er hægt að gefa framleiðslupöntunum upphafs- og lokadagsetningar. Ef framleiðslupantanir eru tengdar við leiðaraðgerðir er hægt að úthluta þeim á flokka kostnaðarstaða.
    -   **Vinnsluröðun** – Þessi röðunaraðferð býður upp á nákvæma áætlun. Hver virkni er brotin niður í stakar vinnslur sem hafa tilteknar dagsetningar, tíma og úthlutuð rekstrartilföng. Ef takmörkuð afkastageta er notuð eru vinnslur úthlutaðar á frátekna afkastaveitu eftir því hvað er tiltækt. Hægt er að skoða og breyta röðuninni í Gantt-riti.
    -   **Kanban-áætlun** – Kanban-vinnslum er raðað í áætlunartöflu kanbans eða raðað sjálfkrafa samkvæmt skilgreiningu sjálfvirkrar fjárhagsáætlunargerðar kanban-reglna.

4.  **Losað** -Hægt er að losa framleiðslupöntun eða runupöntun þegar röðuninni er lokið og efni er tiltækt til að taka til eða undirbúið. Ráðstöfunarathugun efnis hjálpar yfirmanni vinnusalarstjórnunar að meta hversu mikið efni er til ráðstöfunar fyrir framleiðslupantanir eða runupantanir. Einnig er hægt að prenta framleiðslupöntunarskjöl, eins og tiltektarlista, vinnsluspjald, leiðarspjald og leiðarvinnslu. Þegar framleiðslupöntunin hefur verið losuð breytist staða pöntunarinnar og gefur til kynna að framleiðslan geti hafist. Ef vöruhúsakerfi er notað losar losun framleiðslupöntunar eða runupöntunar framleiðslu uppskriftarlína til vöruhúsakerfis. Síðan eru vöruhúsabylgjur og vöruhúsavinna myndaðar samkvæmt uppsetningu vöruhússins.
5.  **Undirbúið**/**Tekið til** – Þegar efni og tilföng hafa verið sett í bið á staðsetningu framleiðslu, eru línur í framleiðsluuppskrift eða kanban-línur eru uppfærðar í stöðuna **Tekið til**. Föstum birgðapöntunum og tengdri vöruhúsavinnu er yfirleitt lokið á þessu stigi. Kanban-spjöldum eða vinnsluspjöldum sem nauðsynleg eru fyrir skýrslu framleiðslugangur ætti að vera úthlutað og prentað.
6.  **Hafið** – Þegar framleiðslupöntun, runupöntun eða kanban er hafin, er hægt að skrá efni og tilfanganotkun á móti pöntuninni. Hægt er að stilla kerfið til að meta sjálfkrafa efni og tilfanganotkun sem er úthlutað í pöntun þegar pöntun er hafin. Þessi úthlutun kallast forlosun, framvirk birgðaskráning eða sjálfsnotkun. Hægt er að úthluta efni handvirkt á framleiðslupantanir eða runupantanir með því að stofna viðbótar færslubækur tiltektarlista. Einnig er hægt handvirkt að úthluta vinnu og öðrum leiðarkostnaði í pöntun. Ef verið er að nota aðgerðaröðun er hægt að úthluta þessum kostnaði með því að stofna færslubók leiðarspjalds. Ef verið er að nota vinnsluröðun er hægt að úthluta þessum kostnaði með því að stofna færslubók vinnsluspjalds. Hægt er að hefja framleiðslu- eða runupantanir í runum endanlega umbeðins magns. Innan framleiðslupöntunar, runupöntunar eða kanbans, er hægt að hefja vinnslurnar sem eru stofnaðar og tilkynna aðskilið gegnum færslubækur, framkvæmd framleiðslu afgreiðslustöðvar (MES afgreiðslustöðvar) eða kanban-borð.
7.  Sýna framvindu /**Lokið** vinnslur – Notið MES Afgreiðslustöð, framleiðslubækur, kanban-borð eða skönnunargetu fartækis til að tilkynna framleiðslugangur með vinnslu eða tilföng. Notkun efnis og tilfanga verður bókuð og staða tengdra kanbana, framleiðslupantana og runupantana gæti verið uppfærð í **Móttekið** eða **Tilbúið**. Frágangsvinna fyrir vöruhúsið gæti verið að stofnuð, eftir skilgreiningu vöruhúss.
8.  **Tilbúið** (innhreyfingarskjal afurða) – Þegar framleiðslupöntun eða runupöntun er skráð sem lokið, er magn fullbúinna vara sem var lokið uppfært í birgðum. Þetta magn inniheldur magn viðeigandi aukaafurða og hliðarafurða. Ef verið er að nota bókhald fyrir verk í gangi (VÍV), er færslubók fjárhags mynduð til að minnka vív-lyklar og auka birgðir fullbúnar vörur. Þegar kostnaður framleiðslupöntunar er reiknað út raunkostnað framleiðslu er bókuð. Ef kostnaði efnis- og vinnu sem er tengdur við framleiðslu er ekki þegar úthlutað í færslubók eða með forlosun, er hægt að úthluta þeim sjálfkrafa með bakalosun. Úthlutun með bakalosun felur í sér frádrátt eftirá á ferlum birgðafærslu. Ef framleiðslupöntun er lokið skal velja gátreitinn **Ljúka vinnslu** til að breyta eftirstandandi stöðu í **Lokið**. Annars er svæðið skilið eftir autt til að leyfa skráningu aukamagn sem eru framleiddar.
9.  **Gæðaprófun** – Innhreyfingarskjal afurða getur virkjað stofnun gæðapantana eftir skilgreiningu á prófunarferli og gæðareglum sem eru tilbúnar fyrir tilteknar vörur. Vegna þess að gæðapöntun getur uppfært birgðastöðu eða runueigindir prófaðra afurða er gæðaprófun skylduferli í mörgum atvinnugreinum.
10. **Frágangur** og **Senda í pöntun** – Eftir innhreyfingarskjal afurða og gæðaprófun beinir valfrjáls frágangsvinna mótteknum afurðum á næsta viðtökustað notkunar, vöruhús fullunninna vara eða sendingasvæði ef fyrirliggjandi eru sendingarpantanir.
11. **Lokið** - Áður er framleiðslu er lokið er raunkostnaður reiknaður fyrir magnið sem var framleitt. Allur áætlaður kostnaður fyrir efni, vinnu og rekstrarkostnaði er bakfærður og skipt út fyrir raunkostnað. Ef þú velur **Ljúka vinnslu** gátreitur þegar þú keyrir kostnaðarútreikningur, breytist staða framleiðslupöntunar í **Lokið**. Þessi staða kemur í veg fyrir að aukalegur kostnaður sé bókaður á lokna framleiðslupöntun.
12. **Tímabilslokuin** – Sumar kostnaðarbókhaldsreglur, eins og reglubundið meðaltal, til baka kostnaðarútreikningur, FIFO eða LIFO krefjast reglubundnar aðgerðir til að loka birgðum eða fjárhagstímabil. Yfirleitt, reynir kerfið að skrá allt efni og tilfanganotkun og einnig leiðréttingar á birgðum og rýrnun, áður en tímabili er lokað. Þessi skýrsla er yfirleitt gerð með því að nota birgðahreyfingabækur eða færslubækur birgðaleiðréttinga. Markmiðið er að meta fjárhagslega frammistöðu rekstrareininga á hverju tímabili. Í sumum tilfellum, þegar langtíma framleiðslupantanir eru notaðar sem ná yfir fjárhagsskýrslutímabil, eru framleiðslubækur notaðar til að tilkynna framvindu framleiðslu og tilfanganotkun í lok tímabils.


<a name="additional-resources"></a>Frekari upplýsingar
--------

[Endurgjöf um framleiðslu](production-feedback.md)

[Yfirlit afbrigðalíkön afurðar](../pim/product-configuration-models.md)

[Yfirlit yfir lean-framleiðslu](lean-manufacturing-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]