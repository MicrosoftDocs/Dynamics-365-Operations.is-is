---
title: "Verkþátturinn er byggður á undirverktaka"
description: "Þetta efnisatriði lýsir, í smáatriðum, hvernig á að nota úthýsta verkþætti í framleiðsluflæði fyrir lean manufacturing."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Verkþátturinn er byggður á undirverktaka

Þetta efnisatriði lýsir, í smáatriðum, hvernig á að nota úthýsta verkþætti í framleiðsluflæði fyrir lean manufacturing.

Í Microsoft Dynamics 365 aðgerða, eru tvær nálganir fyrir undirverktaka: framleiðslupantanir og lean manufacturing. Í lean manufacturing nálgunin subcontracting vinnu er gera líkan af sem þjónusta sem tengjast verkþætti framleiðsluflæðis. Sérstök gerð gerð kostnaðarflokks sem er með heitinu **Beina útvistun** hefur verið innleiddur og subcontracting þjónustur eru ekki lengur hluti af uppskrift (BOM). Kostnaðarbókhald undirverktaka er fyllilega samþætt í kostnaðarútgáfunni lausn fyrir lean manufacturing.

## <a name="production-flows-that-involve-subcontractors"></a>Framleiðsluflæði sem snerta undirverktaka
Einföld regla framleiðsluflæðis ekki breyta þegar aðgerðir eru úthýstur. Efni streymir enn milli staðsetningar vinnsluverkþætti umbreyta efni afurðir og flutningsverkþætti færa efni eða vörur úr einum stað yfir á aðra. Model staðsetningar og vinnuflokkar sem lánardrottinn stýrt með því að tengja lykil lánardrottins í vöruhús eða tilföngum á tilfangaflokk.  

Á grundvelli þessara getu, fyrirferðarlitla ekki krefjast hvaða tilteknar aðgerðir til að styðja á efni og afurðir. Allar mögulegar aðstæður sem fela í sér lánardrottna sem veitur af framleiðslu- eða flutning þjónustu er miðuð samkvæmt högun framleiðsluflæði og verkþætti.  

Til dæmis undirverktaki vinnur úr geymslusvæði sem er staðsett í undirverktaka. Þegar efnismeðhöndlunareiningar eru tæmt á undirverktaka, kanban-spjöld skilað í samsetningu hólf með næsta sendinguna. Síðan er endurnýjaðar geymslusvæði í undirverktaka. Færslur til og frá undirverktaka er miðuð sem yfirlýst flutningsverkþætti til að styðja við tiltekt og sendingu vinnslu. Ef yfirlýst skráningu er ekki krafist til að styðja efnislegt flutning, hægt flytja verkþætti sleppt.  

Hægt er að nota undirverktaki til að álagsjafna heildaruppsetningu afkastagetu framleiðsluflæði. Til dæmis framleiðsluflæðis er gera líkan af með því að nota áætlað kanban-reglur. Í vinnuáætlanagerð notar kanban-röðunar spjald til að raða og hlaða stig bæði vinnuflokkana eftir þörfum. Í vinnuáætlanagerð einnig fylgist með því sameinaða birgðaáætlun geymslusvæði sem á við **birgðaáætlun** síðu. Margar undirverktaka er miðuð eina eða margar framleiðsluflæði og gæti verið margar kanban-reglur sem nota má til að útvega á sömu afurð á sömu staðsetningu gegnum mismunandi verkþætti. Planner er hægt að umbreyta kanbönum í annarri kanban-reglu til að endurraða kanban sem upphaflega var stofnuð fyrir innri framleiðslunnar við önnur ferli. Í fact úthýsta eðli vinnuflokkur hefur engin áhrif á framleiðsluflæði. Sama reglan vinnutíma gildir fyrir tvær vinnuflokkana á samhliða innri eða tvær úthýsta reitum.   

Eins og öllum öðrum verkþátt í framleiðsluflæði, úthýsta verkþætti hægt að nota og birgðir búið er að skrá, ekki-búið er að skrá (vinna í vinnslu \[VÍV\]), og hálfkláraðar efni og afurðir. Í öllum tilvikum vinnslur fyrir röðun og framkvæmd úthýsta verkþætti eru þær sömu. Þar að auki er þar að vinna eins og ferli fyrir innri verk.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Ferli innkaupapantana fyrir úthýsta verkþætti (þjónusta)
Innkaupaferlinu fyrir úthýsta verkþætti á grundvelli efnislegra efni flæði sem er skráð með kanban-vinnslu ferlis, til dæmis, Hefja eða Ljúka. Fjárhagsleg flæði, til dæmis kostnaði undirverktaka, er auka flæði sem fylgir efnislegt framleiðsluflæðis. Á sama tíma er innkaupaferlinu óháð ferli sem leyfir leiðrétting handvirkum innkaupaskjölum við hvert skref. Hér er innkaupaferlinu fyrir úthýsta verkþætti:

1.  Stofna innkaupasamning. Innkaupasamnings stofnað fyrir þjónustuna og tengdur við verkþátt í framleiðsluflæðinu.
2.  Stofna innkaupapöntun. Hægt er að stofna úttektarpöntun innkaupa fyrir þjónustu samkvæmt áætlað kanban-vinnslurnar. Vinnslur fyrir sama þjónustu er hægt að flokka á innkaupapöntunarlínur eftir degi, viku eða mánuð. Hægt er að stofna innkaupapöntunarlínur hvenær sem er eftir að kanban-vinnslur eru stofnaðar. Enn er hægt að stofna innkaupapöntunarlínur eftir að hver einstök. Þessi valkostur er yfirleitt valið ef undirverktaki býður upp á þjónustu fyrirvaralaust viðbótar, byggt á kanbön eða kanban-spjöld sem tekur við undirverktaka. Í þessu tilfelli er hægt að lágmörkuð frávik milli innkaupapöntunarinnar og reikningsins.
3.  Búa til kanban-spjöld, efni og tiltektarlistann til að senda undirverktaka til að undirbúa fyrir vinnslu. Grundvelli nákvæmar líkanabreytu í framleiðsluflæðinu undirbúningi eru gerðar á kanban-spjaldið fyrir ferlisverkþætti með því að nota í tiltektarlistanum og undirbúning aðgerð. Einnig er undirbúningi eru gerðar á kanban-spjald fyrir flutningsvinnslur með því að nota í tiltektarlistanum og upphafs- eða lokið. Búið er að skrá efni fyrir bæði ferlin getur verið styður Vöruhúsakerfis Tiltekt og Sendingu vinnslu. Hægt er að stofna farmbréf eftir þörfum.
4.  Mynda efnismeðhöndlunareiningar kanban og spjöld. Eftir vinnslu, spjöld skilað úr undirverktaka. Vanalega er kort með fylgiseðils sem tilgreinir efnislega efni sem hefur verið sent. Tilvísun veitt þjónusta er ekki krafist. Komu efni eða afurð við viðskiptavinar er skráð á kanban-spjald eftir kanban-spjöld. (Kanban-spjaldið fyrir ferlisverkþætti eða kanban-spjald fyrir flutningsvinnslur er notaður eftir líkani verkþætti.).
5.  Stofna kvittun advisory. Advisory innhreyfingu er hægt að nota til að skipta út fylgiseðli skjal fylgiseðils fyrir móttekið þjónustu. Hægt er að mynda innhreyfingu advisories samkvæmt lokið kanban-vinnslur fyrir subcontracting verkþátt fyrir valin tímabil. Fyrir hverja innhreyfingu vinnslu advisories eru stofnaðar fyrir tengdri innkaupapöntunarlínu. Kvittun advisory getur prentaðar og sendar til undirverktaka sem staðfestingu á innhreyfingu.
6.  Mynda reikning.

Ferlið hefst þegar undirverktaka er reikningsfærð fyrir tímabil. Jöfnun reiknings er gert gagnvart advisories innhreyfingar sem eru stofnaðar. Þar sem innhreyfing advisories tákna nákvæma efnislegu efnis, þríhliða jöfnun prentaraforskrifta einfaldara.

## <a name="configuring-activities-for-subcontracting"></a>Skilgreining verkþætti fyrir undirverktaka
Eftirfarandi kaflar lýsa því hvernig skilgreina á verkþætti fyrir undirverktaka.

### <a name="subcontracted-services"></a>Úthýsta þjónustu

Við greiðslu sem er notað í undirverktaka verkþátturinn er byggður verður afurðar sem hefur eftirfarandi eiginleika:

-   **Gerð afurðar:** Þjónustu
-   **Birgðalíkanaflokkur:** Ekki í birgðum

Krafan um þetta setur notkun fyrst inn, fyrst út (FIFO) birgðalíkan. **Athugasemd:** kostnaðarútreikning afurðanna krefst staðalkostnaðar þjónustu að skilgreina. Innkaupasamningur með lánardrottins er nauðsynlegt. Annars er ekki hægt að nota þjónustuna fyrir undirverktaka byggt á verkþættinum.

### <a name="subcontracted-process-activities"></a>Ferli fyrir úthýsta verkþætti

Fylgið eftirfarandi skrefum til að skilgreina ferli verkþáttar sem úthýsta verkþætti.

1.  Skilgreina úthýsta vinnuflokkur. Til að skilgreina vinnuflokks sem úthýstur, verður að stofna tilföngum yfir á **Lánardrottins** gerð og tengja hana við vinnuflokkur (tilfangaflokkur). Kostnaðartegund keyrslutíma yfir í **Beina útvistun** kostnaðarflokksgerð ætti að úthluta vinnuflokki. Kostnaðartegundir fyrir uppsetningu og magn sem ekki eru kostnaðarjafnaðar krafist.
2.  Eftir að ferli verkþáttar er stofnuð og tengd við úthýsta vinnuflokkur, þarf að skilgreina þjónustunnar fyrir verkþátt áður en hægt er að virkja útgáfu framleiðsluflæðis. Ljúka þessu skrefi á í **Verkþáttar****upplýsingar** síðu. Fyrir verkþætti sem eru tengdar við úthýsta vinnuflokkur á **Þjónustu skilmála** FastTab er sýnd. Á Flýtiflipanum, bæta við sjálfgefna þjónustu sem gildir fyrir allar vörur út. Ef tiltekinn úttaksatriði krefjast mismunandi útreikninga þjónustufæribreytur (til dæmis á mismunandi þjónustuhlutfall) eða mismunandi þjónustu, hægt að bæta önnur þjónusta verkþáttarins.

## <a name="subcontracted-transfer-activities"></a>Flytja úthýsta verkþætti
Flytja verkþátt er skilgreindur sem úthýsta verkþætti, allt eftir í **Flutt með** stillingu flutning verkþáttar. Eftirtaldir valkostir eru í boði:

-   **Farmsendanda** – verkþátturinn er úthýstur ef flutnings frá vöruhúsi er stjórnað af lánardrottni (eins og skilgreint er með eiginleikann vöruhúsinu). Allar valdar innkaupasamninga fyrir þjónustu verður að hafa sama Kenni lánardrottins sem vöruhús.
-   **Viðtakandi** -verkþáttur er úthýstur ef flutningur í vöruhús er stjórnað af lánardrottni (eins og skilgreint er með eiginleikann vöruhúsinu). Allar valdar innkaupasamninga fyrir þjónustu verður að hafa sama Kenni lánardrottins sem vöruhús.
-   **Flutningsaðili** -verkþáttur er úthýstur til allra lánardrottna sem veitir þjónustu. Á að gilda flutningsaðila verður að vera stofnuð fyrir vöruhúsakerfi og verður að hafa lykil úthlutaður lánardrottinn.

Og vinnsluverkþætti, þarf að skilgreina sjálfgefna þjónustu fyrir úthýsta flutningsverkþætti á í **Þjónustu skilmála** FastTab yfir í **Verkþáttar****upplýsingar** síðu.

## <a name="service-quantity-calculation"></a>Útreikningur þjónustumagns
Allt innkaupaferlinu á grundvelli til tilvísun fyrir þjónustu. Þessi tilvísun er mæld í mælieining fyrir þjónustu. Þjónustur eru yfirleitt mæld í fjölda þjónustu (einingar) eða í tíma. Til að reikna út magn þjónustu, byggt á skráðum lokið kanban-vinnslum, er hægt að nota eftirfarandi aðferðum:

-   **Útreikning sem er byggt á fjölda vinnslur** – Einn kanban-vinnslu jafngildir *n* einingar þjónustu, óháð því magni sem er. Í lean manufacturing einni vinnslu samsvarar einni afgreiðslueiningu. Þessi útreikningsaðferð við öll þjónusta sem hafa fast verð á hverja meðhöndlunareiningu. Þar af leiðandi hefur þessi aðferð vanalega við flutningsverkþátta. Hins vegar það getur líka átt við um verkþætti í ferli sem vinna allt efnismeðhöndlunareiningar.
-   **Útreikningur á grundvelli afurðarmagnið** – þjónustumagnið er miðað við magn sem er raðað/uppgefið. Þegar uppgefin afurðarmagnið er reiknað villumagn hægt er að annað hvort tekin með eða útiloka. Þessi útreikningsaðferð við öll tilvik þar sem þjónusta verð á einingu af unnum afurðar er umsamin.
-   **Útreikningur á grundvelli tími verkþáttar** -fræðilegt verkþáttartímar eru reiknaðir út frá vinnslutíma fyrir verkþáttinn, samtals vinna magn og afkastahlutfall unnar afurðar. Þessi útreikningsaðferð við þjónustu sem greidd eru á klukkustund og hafa frávik í tími á hverja afurð unnar.

## <a name="cost-accounting-of-subcontracted-services"></a>Kostnaðarbókhaldi úthýsta þjónustu
Þegar móttöku advisory eða lánardrottins á innkaupapöntun sem var stofnuð fyrir framleiðsluflæði (með öðrum orðum innkaupapöntun sem var mynduð á grundvelli kanban-vinnslur fyrir úthýsta verkþætti) fylgiseðill er bókaður sem gildi innhreyfinga gjaldfært í VÍV lykla í framleiðsluflæðinu. Frávik reikninga eru einnig kostnaðarfært í framleiðsluflæði. Hefur verið kynnt kostnaðartegund fyrir undirverktaka. Þessi kostnaðartegund virkja gagnsæ rakningu á gildi undirverktaka sem er úthlutað á VÍV- og notkun á hvert tímabil.  

Bakfærslukostnaðaraðgerðar fyrir lean manufacturing við lok tímabils kostnaðarútgáfu reiknar raunverulega frávik afurða sem framleidd eru úr framleiðsluflæði kostnaðarútreiknings tímabili.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Flytur líkanabreytu sem úthýsta verkþætti
Fólk íhuga oft framleiðslulausum flutning og leikur sem bætir ekkert gildi. Hins vegar þegar kostnaður undirverktaka er borið saman við kostnað framleiðslu innri kostnaðar verkþátta viðbótar flutningur verður að athuga. Framleiðsluflæðið sem nær yfir marga staðsetningar og flutning þjónustu krefst ætti líkan flutningur kostnaðar sem hluta af kostnaði útvega afurðir til viðskiptavinar. 

Undirverktaka verkþátturinn er byggður á fyrirferðarlitla gerir kleift að samþætta flutningsaðila og flytja lánardrottna sem flytja efni og afurða milli staðsetninga framleiðsluflæðis. Með líkanabreytur flutning verkþátt, hægt er að úthluta flutningsaðila eða lánardrottins. Verkþætti/flutningsstarf byggist á þjónustu og innkaupasamninga, og hægt er að stofna innkaupapantanir og móttöku advisories, byggð á raunverulegum flutningsvinnslur. Þessi aðgerð er sú sama og virkni fyrir ferli fyrir úthýsta verkþætti.  

Þess vegna Dynamics 365 aðgerða nú styður uppskriftarútreikning sem felur í sér flutning þjónustu, stofnun tengdar innkaupapantanir, samþætt innhreyfingu skráningu og samþættingu flutningur þjónustu kostnað í framleiðslu flæði kostnaðarútreikning.


