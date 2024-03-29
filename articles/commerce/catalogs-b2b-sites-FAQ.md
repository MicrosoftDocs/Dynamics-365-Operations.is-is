---
title: Algengar spurningar um Commerce-vörulista fyrir B2B
description: Þessi grein veitir svör við algengum spurningum um Microsoft Dynamics 365 Commerce vörulista.
author: ashishmsft
ms.date: 07/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 68c648c5caf2667f413b236dc437fc2c74c40d07
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168986"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>Algengar spurningar um Commerce-vörulista fyrir B2B

[!include [banner](includes/banner.md)]

Þessi grein veitir svör við algengum spurningum um Microsoft Dynamics 365 Commerce [vörulistar frá fyrirtæki til fyrirtækja (B2B)](catalogs-b2b-sites.md).

### <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Hvers vegna get ég ekki stillt vörulistasérhæft leiðsögustigveldi eða séð möguleika á að tengja stigveldi viðskiptavina?

Gakktu úr skugga um að **Virkjaðu notkun margra vörulista á smásölurásum** eiginleiki er virkur í höfuðstöðvum Commerce **Eiginleikastjórnun** vinnusvæði og að umhverfi þitt sé Commerce útgáfa 10.0.27 eða nýrri útgáfu. Gakktu úr skugga um að þú hafir valið **B2B** undir **Tegund vörulista**.

### <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Get ég skoðað vörulistasértæka stigveldið og auðgað flokkasíður í Commerce site builder?

Já, notendur viðskiptasíðugerðar sem hafa aðgang að **Vörur** síða í vefsmiði getur valið vörulista og skoðað vörulistasértæka stigveldið. Frá **Vörur** síðu geta notendur einnig auðgað flokkasíðu fyrir ákveðinn flokk í vörulistanum. Sjá frekari upplýsingar [Bæta lendingarsíðu flokks](enrich-category-page.md). Ef þú vilt hafa auðgun sem er sértæk fyrir vörulista mælum við með því að þú hafir sérstakt og einstakt leiðsögustigveldi fyrir þann vörulista.

### <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Getur B2B kaupandi keypt úr mörgum vörulistum í einni afgreiðslu?

Já, kaup úr mörgum vörulistum í einni afgreiðslu eru leyfð. B2B kaupendur geta notað vörulistavísirinn í körfuskjánum til að ákvarða hvaða hlutum var bætt við úr hvaða vörulista.

### <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Ef B2B kaupandi kaupir sömu vöru úr mismunandi vörulistum, hver er þá hegðun sem búist er við?

Þrátt fyrir að tiltekinn notandi gæti haft aðgang að mörgum vörulistum á tilteknum tíma, er búist við því að vörur í þessum vörulistum útiloki hvor aðra. Með öðrum orðum, helst ætti sama vara ekki að vera hluti af fleiri en einum vörulista fyrir tiltekinn notanda.

Hins vegar, ef aðstæður koma upp þar sem sama varan tilheyrir mörgum vörulistum, mun kerfið viðhalda mörgum körfulínum fyrir þá vöru. Það verður sérstök lína fyrir hvern vörulista. Sama vara úr tveimur mismunandi vörulistum verður ekki sameinuð við kassa.

### <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Þegar B2B kaupandi er að versla, er einhver staðfesting á framboði vörulista?

Já. B2B kaupandi mun aðeins fá að halda áfram að stöðva ef allir hlutir í körfunni eru úr gildum vörulistum. Ef einhverjar vörur í körfu eru úr útrunnum eða dregnum vörulistum verða þeir fjarlægðir og notandinn látinn vita.

### <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Á meðan á innkaupaupplifun stendur, eru leit og vöruuppgötvun (þar á meðal tengd og mælt vörusöfn) vörulistasértæk?

Já. Um leið og notandi velur tiltekinn vörulista verður allt verslunarferðin vörulistasértæk. Þetta ferðalag felur í sér upplifun vöruuppgötvunar eins og leitartillögur, leitarniðurstöður, flokkaniðurstöður, hreinsunarefni, verðlagningu, eiginleika og ráðlagðar vörur (svo sem nýjar, mest seldar, vinsælar, oft keyptar saman og tengdar vörur).

### <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Getur B2B kaupandi keypt úr sjálfgefna úrvalinu (catalogID=0)?

Nei, B2B kaupandi hefur ekki leyfi til að kaupa úr sjálfgefna úrvalinu. Það úrval er aðeins ætlað til nafnlausrar vafra. Ef B2B kaupandi vantar vörulistaúthlutun (uppfærslur í bið frá umsýslu þeirra) munu þeir ekki geta séð neina vörulista sem þeir geta valið úr og ekkert flokkastigveldi verður sýnilegt.

### <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Er hægt að útbúa markaðsefni fyrir vöru sem er sérstök fyrir vörulista?

Eins og er er vöruauðgun aðeins studd á vefsvæði og rásarstigi. Með öðrum orðum, ef vara er auðguð og henni er deilt á milli margra vörulista, verður samsvarandi auðgað vöruupplýsingasíða (PDP) fyrir þá vöru birt á sama hátt í öllum vörulistum fyrir tiltekna síðu. 

### <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Er vörulistastuðningur í boði fyrir bæði B2B og fyrirtæki til neytenda (B2C) netrásir?

Eins og er er viðskiptaskrám ætlað að vinna með B2B netrásum eingöngu.

### <a name="a-new-customer-was-added-to-the-customer-hierarchy-or-a-new-hierarchy-was-associated-with-the-catalog-but-the-catalog-is-not-available-to-the-user-why"></a>Nýr viðskiptavinur var bætt við stigveldi viðskiptavina eða nýtt stigveldi var tengt við vörulistann, en vörulistinn er ekki tiltækur fyrir notandann. Af hverju?

Gakktu úr skugga um að þú hafir hlaupið **1010** störf eftir að þú tengdir nýja viðskiptamanninn við núverandi stigveldi viðskiptavina og þegar þú stofnaðir nýja viðskiptamannastigveldið. Vörurnar sem tengjast stigveldi viðskiptavina verða aðeins sýnilegar eftir að **1010** verki er lokið með góðum árangri. Ef vörulistinn er líka nýr skaltu ganga úr skugga um að þú hafir keyrt **1150** (verslun) starf sem og **1010** störf. Eins og með alla nýja vörulista, gefðu þér tíma fyrir gögnin að samstilla við rásina og leitarvísitöluna. Ef starf hefur stöðuna „Beitt“ þýðir það að verið er að samstilla gögnin við rásargagnagrunn, en viðbótartími þarf til að gögnin samstillist við leitarvísitöluna. 

### <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Getum við sett upp vörulistasértæka uppsölu/krosssöluvöru?

Eins og er er aðeins virkni tengdra vara studd. Hins vegar eru uppsölu- og krosssölustillingar í boði fyrir símaver.

Eftirfarandi eiginleikar eru einnig aðeins studdir fyrir símaver:

- Heimildarkóðar vörulista
- Notkun upprunaauðkenna til að fylgjast með kostnaði og svarhlutfalli
- Vörulistasértæk pöntunar- og vöruforskrift
- Greining vörulistasíðu
- Vörulistabeiðnir
- Greiðsluáætlanir
- Ókeypis vörur byggðar á frumkóðum

### <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Getum við notað frumkóða vörulista fyrir B2B pantanir í gegnum netverslunargáttina?

Nr. Kóðar vörulista eru aðeins studdir fyrir rásir símavera.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna Commerce-vörulista fyrir B2B-svæði](catalogs-b2b-sites.md)

[Vörulistavalseining](catalog-picker.md)

[Stækkunarhæfniáhrif Commerce-vörulista fyrir B2B-sérstillingar](catalogs-b2b-sites-dev.md)
