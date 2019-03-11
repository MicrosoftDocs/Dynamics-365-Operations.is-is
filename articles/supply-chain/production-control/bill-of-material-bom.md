---
title: Uppskriftir og formúlur
description: Þetta efnisatriði veitir upplýsingar um uppskriftir (BOM) og formúlur, sem eru miðpunktur í skilgreiningu á afurðum og afurðaafbrigðum.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0833143722df5402a17e4f8f456a923792c478a5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "317109"
---
# <a name="bills-of-materials-and-formulas"></a>Uppskriftir og formúlur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um uppskriftir (BOM) og formúlur, sem eru miðpunktur í skilgreiningu á afurðum og afurðaafbrigðum. Uppskriftir og formúlur tilgreina áskilið hráefni eða innihaldsefni fyrir tilgreinda afurð. Formúlur tilgreina einnig aukaafurðir og hliðarafurðir sem eru mótteknar í tilgreindu framleiðslusamhengi. 

<a name="bills-of-materials"></a>Uppskriftir
------------------

Uppskrift (BOM) skilgreinir þá íhluti sem þarf til að framleiða vöru. Íhluti geta verið hráefni, næstum tilbúinar afurðir eða innihaldsefni. Í sumum tilvikum, má vísað í þjónustu í Uppskrift. Hins vegar lýsa Uppskriftir yfirleitt á *efnistilföng* sem krafist er.  

Þegar hún er sameinað við leið eða framleiðsluflæði sem lýsir aðgerðir og tilföng sem eru nauðsynleg til að byggja afurð, myndar Uppskrift grundvöll fyrir útreikninga á áætluðum kostnaði vöru.  

Uppskrift er einstök eining sem lýst er með eftirfarandi upplýsingum:

-   BOM-kenni
-   Uppskriftarnafn
-   Uppskriftarlínur sem lýsa íhluti og innihaldsefni
-   Uppskriftaútgáfur sem skilgreina tímabil og afurð sem hægt er að nota Uppskriftina fyrir

Einstaka uppskrift lýsir einu stigi sem er auðkennt af einkvæmu kenni. Íhlutir gætu haft sínar eigin Uppskriftir sem er vísað í af uppskriftaútgáfur. Hægt er að birta og breyta lokið stigveldi fyrir Uppskriftir fyrir tiltekna vöru í uppskriftarhönnuði.

### <a name="formulas-co-products-and-by-products"></a>Formúlur, aukaafurðir, hliðarafurðir

Formúla er undirgerðin Uppskriftar sem er yfirleitt notað fyrir framleiðsluferli. Að auki íhluta og innihaldsefnis, lýsir Formúla aukaafurðir og hliðarafurðir. Í raunútgáfu krefst skilgreiningar á aukaafurðir og hliðarafurðir fyrir formúlu formúluútgáfu. Formúla er yfirleitt tilgreind fyrir eina tiltekna lokna afurð (formúla eða áætlunarvara) sem er skilgreint í formúluútgáfan.

### <a name="boms-in-the-product-lifecycle"></a>Uppskriftir í lífsferli afurðar

Í lífsferli afurðar, gætu verið stofnaðar margar gerðir Uppskrift af ýmsum ástæðum:

-   **Uppkast/drög að uppskrift** – þessi uppskrift gefur drög að áætlun fyrir efni sem þörf er á í fyrstu stigum hönnunarfasa og hjálpar þér að gera grófa áætlun á kostnaði og áætluðum afurðareigindum. Þessi Uppskrift er yfirleitt ekki notuð í bókhalds- og áætlunarkerfi (ERP).
-   **Verkfræðileg Uppskrift** – Þetta Uppskrift er vanalega notuð þegar afurðir eru hannaðar sem eru byggð á fyrirliggjandi afurðarskjalamöppum. Verkfræðilegar Uppskriftir eru byggðar upp til að einfalda hönnunarferlið og flokka flóknar afurðir í verkfræðilegar kerfiseiningar. Fyrir Einföld afurð gæti verið mögulegt að hanna verkfræðilega Uppskriftir fyrir raunverulegt framleiðsluferli. Hins vegar, fyrir aðrar afurðir, þarf að umbreyta verkfræðilegri Uppskrift raunverulegrar framleiðsluuppskrift. Verkfræðilegar Uppskriftir eru yfirleitt táknuð með skuggum í stigveldi Uppskriftar. Þótt hægt er að nota verkfræðilegar Uppskriftir fyrir áætlanagerð og keyrslu framleiðslu aðgerða, getur þessa nálgun leitt til óhagkvæmni, sérstaklega í endurtekna aðgerðum þar sem margar pantanir eru stofnaðar.
-   **Áætlunaruppskrift** – Þetta Uppskrift er notuð til að gera áætlun fyrir kröfur um efni. Eftirspurn fyrir íhluta og innihaldsefni er reiknuð á grundvelli eftirspurnar eftir fullunninna vara. Eins og kostnaðaruppskrift, gætu áætlunaruppskriftir tákna tiltekna blöndu efnis sem er notaður á tímabili.
-   **Framleiðsluuppskrift** – er raunverulega Uppskriftar sem er notað fyrir tiltekna framleiðslu. Framleiðsluuppskrift verður að taka mið af raunverulegu tilföng sem eru notaðar til að framleiða vöruna. Þegar framleiðslupöntun, runupöntun eða kanban er stofnuð, eru hin mörgu stigu Uppskriftir sem eru sýndir með skuggum dregin saman í eitt stig og dreift yfir aðgerðir fyrir pöntunina.
-   **Kostnaðaruppskrift** - þessi uppskrift er notað til að reikna áætlaðan kostnað afurðar. Til dæmis er hægt að nota kostnaðaruppskrift þegar staðalkostnaður er notaður eða áætlaðan kostnað tiltekinnar vöru er reiknaður. Kostnaðaruppskrift geta vísa í tiltekna blöndu af efni og tilföng sem áætlað er að nota. Þess vegna er hægt að nota kostnaðaruppskrift til að stofna dæmigerðan áætlaðan kostnað fyrir tímabilinu og hjálpa við að koma í veg fyrir frávik yfir tímabil.

Gerðir Uppskrifta sem eru raunverulega notaðar eru háðar innleiðingu, og einnig viðskiptaaðstæður og þarfir. Í einfaldri framkvæmd, er hægt að móta áætlunaruppskrift, framleiðsluuppskrift og kostnaðaruppskrift sem eina Uppskrift. Í umhverfi þar sem eru tíðar verkfræðilegar breytingar og margar leiðir sem velja má um er stærri safn Uppskriftagerða sennilega þarft.

### <a name="approval-of-boms-and-formulas"></a>Samþykki fyrir Uppskriftir og formúlur

Hver Uppskrift og formúla geta verið sérstaklega samþykkt eða ósamþykkt. Venjulega er samþykkt Uppskriftar eða formúlu gerð þegar fyrsta viðeigandi uppskriftaútgáfa er samþykkt. Hins vegar í sumum viðskiptaaðstæður gæti þessi samþykki verið mismunandi skref í ferlinu og gæti falið í sér mismunandi eigendur ferlis.  

Athugið að, ef Uppskrift er ósamþykkt, eru öllum tengdum uppskriftaútgáfur einnig ósamþykktar.

## <a name="bom-and-formula-versions"></a>Uppskriftarútgáfur og formúluútgáfur
Til að tengja ákveðna Uppskrift eða formúla við afurðarafbrigði sem hægt er að framleiða, verður að stofna uppskriftarútgáfan eða formúluútgáfan. Hægt að takmarka gildistíma uppskriftarútgáfa og formúluútgáfa eftir tímabili, magn, svæði, tiltekinn afurðavíddir og öðrum skilyrðum. Formúluútgáfur hafa aðrar mikilvægar eiginleika, eins og framlegð, skilgreiningar hliðarafurð og aukaafurða og leiðbeiningar fyrir dreifingu kostnaðar fyrir formúluna.

### <a name="approval-of-bom-and-formula-versions"></a>Samþykki fyrir uppskrift og formúluútgáfa

Áður en hægt er að nota uppskriftarútgáfu í áætlun eða framleiðsluferli, það verður að vera samþykkt. Þegar uppskriftarútgáfa er samþykkt, er einnig hægt að samþykka tengda Uppskrift, eftir vali notanda og sannvottunarréttindi . Athugið að hægt er að samþykkja uppskriftaútgáfu eingöngu ef sjálf tengda Uppskriftin er samþykkt.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Virkjun á sjálfgefinni Uppskrift eða formúluútgáfur

Til að stilla tiltekna Uppskrift eða formúlu sem sjálfgefna uppskriftarútgáfan eða formúluútgáfan sem verður notað með aðaláætlanagerð eða til að stofna framleiðslupantana, verður að virkja útgáfu. Þegar útgáfa er virkjuð, er einkvæmni útgáfu fyrir tilteknar skorður (til dæmis, tímabil, svæði eða magn) staðfest. Villuskilaboð berast ef útgáfan sem verið er að reyna að virkja rekst á við útgáfu sem er þegar virk. Þú verður annaðhvort á óvirkja útgáfa sem rekist er á eða breyta skorður útgáfu (yfirleitt tímabils) til að koma í veg fyrir tvíræðrar virkjun.

### <a name="product-change-with-case-management"></a>Vörubreyting með málastjórnun

Afurðarbreytingamál fyrir samþykkt og virkjun nýrra uppskrifta eða breytta uppskrifta og uppskriftarútgáfa veitir auðveld leið til að sjá yfirlit yfir skorður uppskriftarútgáfu. Einnig er hægt að samþykkja og virkja allar Uppskriftir og formúlur sem tengjast ákveðnum breytingum fyrir eina virkjunardagsetning.

### <a name="alternative-bom-versions"></a>Aðrar uppskriftaútgáfur

Stundum ætti virka uppskriftarútgáfan eða formúluútgáfan ekki að vera notuð í spár, sölu eða yfirafurð. Í þessu tilfelli er hægt að velja ákveðna samþykktri Uppskrift sem hluti af þarfir (spárlínu, sölulínu eða uppskriftarlína) ef er samþykkt uppskriftarútgáfan eða formúluútgáfan er nú þegar til fyrir aðra Uppskriftar eða formúlu.  

Þegar áætlaðar pantanir, framleiðslupöntunum eða kanbön eru stofnaðar, geta skipuleggjandi eða yfirmaður í vinnusal nota hvaða samþykktri uppskriftarútgáfu sem er gild á umbeðinni tímabili fyrir áætluð pöntun til að áætla eða framleiða tiltekið vöru. Uppskriftarútgáfan sem er notuð þarf ekki að vera virkjuð sem sjálfgefin uppskriftarútgáfa.

## <a name="bom-and-formula-lines"></a>Uppskriftarlínur og formúlulínur
Uppskriftarlínu er stofnuð fyrir hverja efni, þjónustu eða innihaldsefni. Lína skilgreinir áætlaða notkun tilgreinds afurðarafbrigðis og skilgreinir einnig ýmsar eigindir sem eru tengdar við áætlaða notkun.  

Uppskriftarlínur geta haft eftirtöldum línugerðum: **Vöru**, **Skugga**, **fest framboð**, **Lánardrottins**.

### <a name="item"></a>Vara

Velja skal **Vöru** línugerð fyrir efni eða þjónustu sem eru notaðar beint og sem ekki þurfa frekari niðurbrot eða fest framboð.

### <a name="phantom"></a>Skugga

Veljið **skugga** línugerð þegar ætlunin er að brjóta niður lægri stig af uppskriftarvörum sem eru í uppskriftarlínunni. Í Aðalröðun, útreikning áætlaðs kostnaðar eða í mat á framleiðslupöntun sem notar uppskriftarlínur af gerðinni **Skuggi** , er yfir uppskriftarlína sem vísar til afurðarafbrigði sem hefur skuggauppskrift skipt út fyrir hluta vöru sem eru skráðir sem uppskriftarlínur í þeirri Uppskrift, eins og ákvarðað er af viðeigandi virka uppskriftaútgáfan þess afurðarafbrigðis. Ef afurðarafbrigðis er með viðeigandi virka leið, eru aðgerðir á leiðinni sameinaðar í yfir leið..  

Athugið að skuggar eru vanalega notaðir til að einfalda verkfræðileg ferli. Yfirgripsmikil notkun skuggauppskrifta í mörgum stigum hefur áhrif á afköst, sérstaklega í mjög endurtektarsömum framleiðsluaðstæðum. Til að bæta afköst ætti að forðast djúp stigveldi fyrir skugga. Í stað þess skal nota fyrirfram niðurbrotið framleiðsluuppskriftir og leiðir.

### <a name="pegged-supply"></a>Þarfaraktar birgðir

Velja **Fest framboð** línugerð þegar óskað er að stofna undirframleiðslu, tilvikskanban uppskriftarlínu eða beina innkaupapöntun fyrir einhver afurðarafbrigði sem uppskriftarlínan vísar til. Undirframleiðslan, tilvikskanban eða innkaupapöntun er stofnuð þegar metin er framleiðslupöntun. Nauðsynlegt magn af vöru er tekið frá sjálfkrafa fyrir framleiðslupöntunina sem mun nota það..

### <a name="vendor"></a>Lánardrottinn

Veljið **lánardrottinn** línugerð ef framleiðsluferlið notar undirverktaka og ætlunin er að stofna sjálfkrafa undirframleiðslu eða innkaupapöntun fyrir undirverktakann.  

**Athugasemd um úthýst verj í Uppskrift:** þjónustan eða vinnan sem undirverktaka framkvæmir verður að vera stofnuð sem þjónustuvara sem er rakin í birgðir. Tengja verður þjónustuvöru við yfirvöruna sem uppskriftarlínu. Leiðin verður að innihalda aðgerð sem er úthlutað til rekstrartilföng undirverktakans.



