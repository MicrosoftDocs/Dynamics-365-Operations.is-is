---
title: Bókun innkaupapöntunar
description: Þessi grein lýsir flipanum Innkaupapöntun á síðunni Birgðafærslusnið.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 0793c58b07d2c0a133e1a5bc0607483f22206b95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849932"
---
# <a name="purchase-order-posting"></a>Bókun innkaupapöntunar

The **Pöntun** flipann á **Skráningarsnið** síða er notuð til að stjórna því hvernig innkaupapantanir verða bókaðar í fjárhag. Tvær meginaðgerðir bóka í aðalbók fyrir innkaupapöntun: 

- Innhreyfingarskjal afurða
- Reikningur

Til þess að efnisleg færsla (vörukvittun) geti bókað í fjárhag á innkaupapöntun, verður að velja eftirfarandi gátreit:

- The **Bókaðu innhreyfingu vöru í höfuðbók** gátreitinn á **Birgða- og vöruhúsastjórnunarfæribreytur** síðu.
- The **Bókaðu efnislegar birgðir** og **Áfallast ábyrgð við móttöku vöru** gátreitir á **Vörulíkanaflokkar** síðu.

Helstu reikningar verða að vera tilgreindir í **Birgðafærslusnið** síðu fyrir eftirfarandi birtingargerðir:

- Kostnaður við innkaupaefni móttekið
- Kaupkostnaður, óreikningsfærður
- Innkaup, uppsöfnun

Til þess að fjárhagsfærsla (reikningur) geti bókað í fjárhag á innkaupapöntun, þarf að uppfylla eftirfarandi skilyrði:

- The **Bókaðu fjárhagsskrá** gátreitinn verður að vera valinn í **Vörulíkanaflokkar** síðu fyrir vöruna sem valin er í innkaupapöntunarlínunni.
- Helstu reikningar verða að vera tilgreindir í **Birgðafærslusnið** síðu fyrir eftirfarandi birtingargerðir:
  - Kostnaður vegna keypts reikningsfærðs efnis
  - Innkaupaútgjöld afurðar
  - Innkaupaútgjöld kostnaðar
  - Afsláttur (valfrjálst)

## <a name="fixed-receipt-price-posting"></a>Föst kvittun verðbókun

Þú getur notað fast kvittunarverð sem staðalkostnað fyrir vöru sem valkost við að velja **Staðalkostnaður** valmöguleika í **Birgðalíkan** sviði á **Vörulíkanaflokkar** síðu fyrir hlut. Aðalmunurinn er sá að hvenær **Fast kvittunarverð** er notað verður núverandi kostnaðarverð notað fyrir vöruna þegar birgðakvittun er bókuð. Það er ekkert kostnaðarendurmatsferli fyrir **Fast kvittunarverð** ; þegar fjárhagsuppfærsla er bókuð er núverandi kostnaðarverð notað við bókun. Ef munur er á kostnaðarverði sem notað er við móttöku og reikning, mun frávikið bóka á rekstrarreikninga fyrir fasta innhreyfingarverð.

Til að nota fast kvittunarverð fyrir vöru verður þú að stilla eftirfarandi:

- Á **Vörulíkanaflokkar** síðu, veldu **Bókaðu efnislegar birgðir** og **Fast kvittunarverð** gátreitir. 
- Á **Birgða- og vöruhúsastjórnunarfæribreytur** síðu, veldu **Bókaðu fylgiseðil í höfuðbók** gátreit.
- Á **Birgðafærslusnið** síðu, tilgreindu aðalreikninga fyrir eftirfarandi færslugerðir:
  - Hagnaður á föstu verði innhreyfingar
  - Tap á föstu verði innhreyfingar
  - Mótbókun fasts innhreyfingarverðs

Fyrir frekari upplýsingar, farðu á [Fast kvittunarverð](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="purchase-charges-and-stock-variation-posting"></a>Innkaupagjöld og lagerafbrigði

Ef þú ætlar að gera grein fyrir innkaupagjöldum og lagerafbrigðum skaltu gera eftirfarandi:

- Á **Færibreytur viðskiptaskulda** síðu á **Reikningur** flipann, veldu **Bókaðu á gjaldfærslureikning í höfuðbók** gátreit.
- Á **Vörulíkanaflokkar** síðu fyrir vöruna sem valin er í innkaupapöntunarlínunni, veldu **Bókaðu efnislegar birgðir**, **fjárhagsskrá**, og **Áfallast ábyrgð við móttöku vöru** gátreitir.
- Á **Innkaupa- og innkaupafæribreytur** síðu, veldu **Búðu til gjöld á vörukvittun** gátreit.
- Á **Birgða- og vöruhúsastjórnunarfæribreytur** síðu, veldu **Bókaðu fylgiseðil í höfuðbók** gátreit.

Á **Birgðafærslusnið** síðu, verður þú að tilgreina aðalreikninga fyrir eftirfarandi færslugerðir:

- Kaupkostnaður, óreikningsfærður
- Innkaupaútgjöld afurðar
- Birgðaafbrigði

> [!NOTE]
> The **Hleðsla** færslugerð er ekki notuð þegar **Bókaðu á gjaldfærslureikning í höfuðbók** færibreytan er valin.

Fyrir frekari upplýsingar, farðu á [Bóka til gjaldfærslu reikningsreikningsreglu](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md).

## <a name="sample-posting-profile-configuration"></a>Dæmi um stillingar fyrir færslusnið

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðalreikningum og lýsingum:

- The **Hreinsunarreikningur** dálkurinn gefur til kynna að bókunartegundin sé jöfnunarreikningur. Upphæðin sem er bókuð á þessum reikningi er sjálfkrafa bakfærð þegar síðari færsla er bókuð. 
- The **P/F** dálkur gefur til kynna **P** fyrir líkamlega færslu og **F** fyrir fjárhagslega færslu. 
- The **Fylgja** dálkur gefur til kynna hvort aðalreikningur tiltekinnar færslutegundar sé venjulega sá sami og annarri færslutegund. Gildið í dálknum gefur til kynna færslugerðina sem venjulega er notuð.

> [!NOTE]
> Aðalreikningar og nöfn aðalreikninga eru aðeins tillögur. Við mælum með<!--note from editor: Via Writing Style Guide.--> Að þú vinnur með endurskoðanda þínum til að ákvarða bestu uppsetninguna fyrir fyrirtækisþarfir þínar.


| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Kostnaður vegna keypts efnis sem er móttekið | 140100</br>140101 | Efnisskrá</br>Efni sent ekki reikningsfært | Eign | Debet | Já | P | Kostnaður vegna keypts reikningsfærðs efnis | Notað þegar innkaupapöntun vörukvittun er bókuð. Jöfnun á reikninginn er innkaupakostnaður, óreikningsfærður. Upphæðin á þessum reikningi er bakfærð þegar innkaupapöntunarreikningur er bókaður. |
| Kaupkostnaður, óreikningsfærður | 600180 | Efniskvittanir | Kostnaður | Debet | Já | P | |Notað þegar innkaupapöntun vörukvittun er bókuð. Tvö fylgiskjöl eru búin til fyrir kvittunina til að rekja frávik innkaupaverðs þegar staðallkostnaður er notaður. Jöfnun á reikninginn á fyrsta fylgiskjali er innkaupauppsöfnun. Jöfnun á öðru fylgiskjali er summan af kostnaði við móttekið efni og innkaupaverðsfráviksreikningum. Upphæðir sem eru bókaðar á þessum reikningi eru bakfærðar þegar innkaupapöntunarreikningur er bókaður. |
| Kostnaður vegna keypts reikningsfærðs efnis | 140100 | Efnisskrá | Eign | Debet | Nr. | F  |Kostnaður vegna keypts efnis sem er móttekið | Notað þegar innkaupapöntunarreikningur er bókaður. Mótið á þennan reikning er innkaupaútgjöld fyrir vöru. Þessi reikningur táknar birgðir á efnahagsreikningi þínum. Reikningurinn sem notaður er er venjulega sami reikningurinn og notaður fyrir kostnað af afhentum einingum og kostnað eininga sem reikningsfærðar eru fyrir sölupöntun. |
| Innkaupaútgjöld afurðar | 600180 | Efniskvittun | Kostnaður | Kredit | Nr. | F  | |Notað þegar innkaupapöntunarreikningur er bókaður. Jöfnun á þennan reikning er kostnaður við keypt efni. Þessi reikningur táknar birgðir á efnahagsreikningi þínum. |
| Verðhagnaður fasta innhreyfinga (Kaup, hagnaður af fastri innhreyfingu*) | 510310 | Frávik innkaupaverðs | Kostnaður | Kredit | Nr. | F | Tap á föstu verði innhreyfingar | Notað þegar innkaupapöntunarreikningur er bókaður og munur er á reikningsfærðu verði og sjálfgefna kostnaði vörunnar. Þessi reikningur er notaður þegar munurinn er meiri. Mótið á þennan reikning er fast móttökuverðsjöfnun. |
| Fast verðtap kvittunar (Kaup, fast kvittunartap*) | 510310 | Frávik innkaupaverðs | Kostnaður | Debet | Nr. | F | Hagnaður á föstu verði innhreyfingar | Notað þegar innkaupapöntunarreikningur er bókaður og munur er á reikningsfærðu verði og sjálfgefna kostnaði vörunnar. Þessi reikningur er notaður þegar mismunurinn er minni. Mótið á þennan reikning er fast móttökuverðsjöfnun. |
| Föst kvittun verðjöfnun (Kaup, föst kvittun verðjöfnun*) | 140900 | Birgðaafbrigði | Eign | Bæði | Nr. | F  | |Notað þegar innkaupapöntunarreikningur er bókaður og munur er á reikningsfærðu verði og sjálfgefna kostnaði vörunnar. Þessi reikningur er mótvægið við Föst innhreyfingarverð rekstrarreikninga. |
| Gjald | NA | NA | NA | NA | NA | NA | NA | Þessi reikningur er ekki lengur notaður. Notaðu lagerafbrigðið í staðinn. |
| Birgðaafbrigði | 600170 | Birgðaafbrigði | Kostnaður | Kredit | Nr. | Bæði | | Þessi reikningur er notaður þegar: <ul><li>Það er munur á einingarverði milli vörukvittunar og reiknings.</li><li>Gjöld eru færð á hlutinn.</li><li>Óbeinn kostnaður hefur verið<!--note from editor: Edit okay?--> Bætt við keyptar vörur. </li><li>Jöfnun á þennan reikning er innkaupaútgjöld, óreikningsfærður reikningur.</li></ul> |
| Innkaup, uppsöfnun | 200140 | Uppsöfnuð kaup | Bótaábyrgð | Kredit | Y | P | |Notað þegar innkaupapöntun vörukvittun er bókuð og valkosturinn til að safna innkaupaupphæðum er virkur. |
| Áfallinn virðisaukaskattur á innhreyfingu | 250500 | Áfallinn söluskattur | Bótaábyrgð | Kredit | Y | Bæði  | |Þessi reikningur er notaður þegar þú velur **Bókaðu líkamlegan skatt** valmöguleika á **Birgða- og vöruhúsastjórnunarfæribreytur** og þú ert með innkaupapöntun með skatti. Upphæðin er bókuð þegar þú uppfærir innkaupapöntunina líkamlega (vörukvittun) og bakfærð þegar þú bókar innkaupapöntunina fjárhagslega (reikningur). |
| Fasteignakvittun (fasteignaskuld*) | 180100 | Varanlegir fastafjármunir | Eign | Debet | N | Bæði | Bæði | Þessi reikningur er notaður þegar þú velur valkostinn á innkaupapöntunarlínunni fyrir fastafjármuni. Samþætting innkaupapöntunar hefur verið stillt til að eignast eignina við móttöku vöru eða reikning. Fyrir frekari upplýsingar um samþættingu innkaupapöntunar fastafjármuna, farðu á [Afla eigna með innkaupum](/fixed-assets/acquire-assets-procurement). |
| Innkaupaútgjöld kostnaðar | 618900 | Ýmis kostnaður | Kostnaður | Debet | N | Bæði | |Notað þegar þú bókar vörukvittun eða reikning fyrir innkaupapöntun þar sem vörurnar eru ekki á lager eða innkaupaflokkur er notaður. |
| Fyrirframgreiðsla | 132190 | Fyrirframgreiddur kostnaður | Eign | Debet | N | Bæði | | Notað þegar unnið er með fyrirframgreiðslureikning á innkaupapöntun. |


\* Gildi sem sýnd eru innan sviga tákna gildið sem er notað í **Tegund færslu** sviði á **Viðskipti með skírteini** síðu. Þú getur skoðað **Tegund færslu** á **Viðskipti með skírteini** síðu á **Almennt** flipa.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Bókun eigna með innkaupapöntunum

Ef þú notar **Fastafjármunir** mát og ætlar að kaupa fastafjármuni í gegnum innkaupapantanir, verður þú að stilla **Kvittun eigna** birtingartegund á **Pöntun** flipi á **Birgðafærslusnið** síðu. Fyrir frekari upplýsingar, farðu á [Samþætting fastafjármuna](/fixed-assets/fixed-asset-integration.md) og [Búðu til og eignast eignir frá viðskiptaskulda](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Fyrirframgreiðsla innkaupapöntunar reikningsbókun

Ef þú ætlar að nota **Fyrirframgreiðsla reikningur** eiginleiki fyrir innkaupapantanir, the **Fyrirframgreiðsla** færslugerð verður að vera valin á **Pöntun** flipann á **Birgðafærslusnið** síðu. Fyrir frekari upplýsingar, farðu á [Fyrirframgreiðslureikningar vs fyrirframgreiðslur](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Innkaupabeiðni og innkaupapöntun staðfestingarbókun

Einnig er hægt að stilla innkaupabeiðnir og innkaupapöntunarstaðfestingar til að bóka forkvaðir og kvaðir í fjárhag. Þessum færslum er stjórnað af færsluskilgreiningu. Fyrir frekari upplýsingar, farðu á [Um kvaðir á innkaupapöntunum](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Innkaupaflokksfærsla

Í stað þess að setja upp birgðabókun fyrir allar vörur, vöruflokk eða eina vöru, er hægt að setja upp flokka og stjórna fjárhagsbókun eftir innkaupaflokkum. Fyrir frekari upplýsingar um uppsetningu flokka og úthluta þeim á vörur, farðu á [Dæmi um stillingar fyrir færslusnið](#sample-posting-profile-configuration) fyrr í þessari grein.

Þegar flokkar eru notaðir með innkaupapantunum eða reikningum lánardrottins þarf að úthluta flokkastigveldinu til **Stigveldi innkaupaflokka** sláðu inn á **Hlutverkaúthlutun flokkastigveldis** síðu.

### <a name="vendor-invoices-with-procurement-categories"></a>Seljendareikningar með innkaupaflokkum

Ef fyrirtækið þitt notar innkaupapantanir fyrir sum innkaup en ekki fyrir önnur, geturðu unnið reikninga sem ekki tengjast innkaupapöntun á margvíslegan hátt. Þetta felur í sér að nota tímarit í **Viðskiptaskuldir** eða af **Reikningar seljanda í bið** síðu sem er notuð til að búa til reikninga fyrir innkaupapantanir. Þegar reikningar eru búnir til fyrir reikninga sem ekki tengjast innkaupapöntun, þarftu að búa til innkaupaflokka fyrir hverja tegund kostnaðar. Þú þarft að kortleggja flokkinn á réttan kostnaðarreikning á **Skráningarsnið** síðu.

Nákvæmur fjöldi flokka er mismunandi eftir fjölda kostnaðarreikninga sem þú notar til að bóka reikninga þína. Þú þarft að minnsta kosti einn innkaupaflokk fyrir hvern aðalreikning sem þú kostar reikninga sem ekki eru innkaupapöntun á. Hægt er að nota marga flokka fyrir einn aðalreikning. Þetta getur verið gagnlegt fyrir notagildi, leitarmöguleika og skýrslugerð hvers konar útgjalda þú notar.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Kostir þess að nota innkaupaflokka fyrir reikninga lánardrottins

Sumir kostir þess að nota innkaupaflokka fyrir reikninga lánardrottna eru:

- Stöðug notendaupplifun: Þegar þú stillir innkaupaflokka fyrir allan kostnað sem ekki tengist innkaupapöntun er hægt að þjálfa notendur í einu ferli fyrir reikningagerð með því að nota **Reikningar seljanda í bið** síðu.
- Bætt skýrslugerðarupplifun: Þegar þú stillir innkaupaflokka fyrir allar vörur og allan kostnað sem ekki tengist innkaupapöntun mun innkaupaútgjaldaskýrslan greina eyðsluna eftir lánardrottni, flokkum og fleiru.
- Stöðugt vinnuflæði: Þegar þú notar **Reikningar seljanda í bið** til að vinna alla reikninga er hægt að búa til samræmt verkflæði og samþykkisferli með því að nota eitt verkflæði.

## <a name="consignment-inventory-posting"></a>Birgðafærsla vörusendinga

Sendingarbirgðir notar sömu fjárhagsbókun og aðrar keyptar vörur. Lykilmunurinn er sá að þegar birgðin er móttekin eru engar fjárhagsfærslur skráðar. Að flytja eignarhald til stofnunarinnar þegar an **Breyting á birgðaeign** færslubók er bókuð, fylgiskjal er myndað til að skrá kostnað vörunnar. Fyrir frekari upplýsingar, farðu á [Settu upp sendingu](/supply-chain/inventory/consignment.md).
