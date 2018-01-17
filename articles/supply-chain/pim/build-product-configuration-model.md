---
title: "Bygging afbrigðalíkans afurðar"
description: "Þörf á að skilgreina vörur í sérstökum kröfum er verði reglan frekar en undantekning í fyrirtæki til fyrirtækis og viðskiptaferli í consumer vensl."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b096f366f13406a4c80d7eccfa8f27d8f8f712e4
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="build-a-product-configuration-model"></a>Bygging afbrigðalíkans afurðar

[!include[banner](../includes/banner.md)]


Þörf á að skilgreina vörur í sérstökum kröfum er verði reglan frekar en undantekning í fyrirtæki til fyrirtækis og viðskiptaferli í consumer vensl.

Framleiðandi sem styður aðstæður sem snúast um að grunnstilla fyrir pöntun hefur tækifæri við huga betur að þörfum viðskiptavina. Þar að auki, með því að geyma hálfkláraðar vörur á formi almennra íhluta í stað tilbúinna afurða, getur framleiðandi dregið úr því fé sem er bundið í birgðum.  

Árangursríkur flutningur úr uppsetningu framleiðslu til birgða til uppsetningar á grunnstilla fyrir pöntun krefst vandlegrar greiningar á uppbyggingu afurða, auðkenningu afurðasafna og íhlutum Til að draga úr fjölda hluta og lágmarka fjölda vara sem eru í vinnslu, er mjög mikilvægt að skilja viðmót afurðar og að hannað er til endurnýtingu.  

Til eru nokkrar líkanareglur afurðagrunnstillingar, eins og reglumiðuð, víddabyggð og skorðubyggð líkön. Kannanir sýna að aðferð sem byggir á skorðum getur dregið úr fjölda kóðalína í líkön um 50 prósent miðað við aðrar reglur líkanabreytu. Þar af leiðandi getur þessi aðferð lækkað heildarkostnað eignarhalds (TCO). Með því að færast frá reglumiðuðu líkani sem byggir á X ++ kóða yfir í líkan sem byggir á skorðum þarf ekki lengur að krefjast leyfis forritara til að vinna með vörulíkön.

## <a name="product-configuration"></a>Afurðarafbrigði
Iðnvæðingartímabilið hefur leitt til mikils árangurs við framleiðslu hágæða afurða með mörgum eiginleikum, á viðráðanlegu verði. Stærðarhagkvæmni hefur gert það mögulegt fyrir flest fólk í hinum iðnvædda hluta heimsins að kaupa bíla, sjónvörp, heimilistæki og aðrar vörur sem flest okkar telja nauðsynlegan hluta af daglegu lífi okkar.  

Þar sem margar afurðir hafa orðið verslunarvörur hefur komið upp þörf til að aðgreina þær. Bein svörun framleiðenda við þessari áskorun hefur verið til að skapa afbrigði af hverri vöru, svo að viðskiptavinir hafi um fleira að velja. Þessi stefna hefur leitt til aukinna spáráskorana og einnig aukningar á birgðakostnaði og óseldum afurðum sem verða úreltar.  

Með því að taka upp aðferðafræði grunnstillingar fyrir pöntun hafa framleiðendur tækifæri til að uppfylla eftirspurn viðskiptavina eftir einstökum afurðum en draga um leið úr eða sleppa úreltum birgðavörum. Þegar framleiðslu á lager framleiðsluaðferðarfræði er skipt yfir í aðferðafræði grunnstillinga fyrir pöntun er ein fyrsta áskorunin sem rís að þörfina á stuttum afhendingartíma verður að jafna við lágt birgðastig.  

Lykillinn að árangri hér er að greina afurðasafnið vandlega og leita að mynstrum í bæði aðgerðum og ferlum afurðar. Markmiðið er að tilgreina almenna íhluti sem hægt er að framleiða með sama búnað og notaður er í öllum afbrigðunum.  

Í nýja eiginleikum Afurðar skilgreiningu inniheldur í notendaviðmótinu (UI) sem gefur yfirlit visual líkanaskipanina skilgreiningu, og einnig málskipan declarative skorðu sem hefur ekki á að þýða. Þess vegna eiga fyrirtæki sem vilja styðja skilgreiningavenju auðveldar með að hefja rekstur. Eins og eftirfarandi kaflar útskýra krefst vöruhönnuður ekki lengur stuðnings forritara til að byggja afbrigðalíkan afurðar, prófa það og losa þær sölufyrirtæki.

## <a name="building-a-product-configuration-model"></a>Uppbygging afbrigðalíkans afurðar
Það eru nokkrar nálganir sem notandi getur tekið til að byggja afbrigðalíkan afurðar. Einn valkostur er að fylgja raðstreymi með því að stofna fyrst öll tilvísunargögn, eins og afurðarsniðmát, einkvæmar afurðair og rekstrartilföng og hafa þau síðan með sem íhluti, uppskriftarlínur, leiðaraðgerðir og aðrar einingar afbrigðalíkans afurðar. Einnig er hægt að velja nálgun sem er endurtekin með því að stofna fyrst líkanið og bæta síðan tilvísunargögnum eftir því sem þörf krefur.

### <a name="components"></a>Íhlutir

Afbrigðalíkan afurðar samanstendur af einum eða fleiri íhlutum sem eru tengdir saman með undirþáttagerð vensl. Íhlutir eru skilgreindir einu sinni og hægt að nota oft í einni eða fleiri afbrigðalíkönum afurðar. Þættirnir eru aðal grunneiningar afbrigðalíkans afurðar og næstum allar upplýsingar um líkanið er tengt þeim.

### <a name="attributes"></a>Eigindir

Hver hluti hefur eina eða fleiri eigindir sem auðkenna eiginleikum hans. Eigindir eru það sem notendur verða að velja meðan á skilgreiningu stendur. Eigindir stjórna bæði milli venslum íhluta og innan íhluta til að hafa með í skorðum eða útreikningum. Gegnum skilyrði sem eiga við uppskriftalínur er hægt að nota eigindir til að ákvarða hvaða efnislegt hlutum skilgreindu vöra samanstanda af. Þar að auki getur eigind stjórnað eiginleika uppskriftarlínu með vörpunarferli. Svipuð virkni er til fyrir leiðaraðgerðir varðandi meðtalningu og eiginleika stillingar.

### <a name="expression-constraints"></a>Segðarskorður

Notið afbrigðalíkans afurðar sem byggir á skorðum gefur sumar takmarkanir til þegar notandi velur gildi fyrir ýmsar eigindir. Hægt er að innleika slíkar takmarkanir sem segðarskorður með því að nota í Fínstilling Líkanabreytur Tungumál (auðkenni OML). Einnig er hægt að innleiða hömlu í töfluskorðu.

### <a name="table-constraints"></a>Töfluskorður

Töfluskorður geta verið notandaskilgreindar eða kerfisskilgreindar.  

Notandaskilgreind töfluskorða er byggð á notanda. Notandi velur samsetningu eigindagerðir dálka í töflunni stendur og færir gildi úr lénum valinna eigindagerða til að mynda línur í töfluskorðunni.  

Kerfisskilgreind töfluskorða er skilgreind með því að velja hvaða töflu í Microsoft Dynamics 365 for Finance and Operations á að nota sem tilvísun og velja svo svæði úr þessari töflu til að mynda dálka í skorðunni. Línur töfluskorðunnar eru línurnar í Finance and Operations töflu sem eru til staðar við skilgreiningu.  

Töfluskorða er innifalin í afbrigðalíkani afurðar með því að vísa í skilgreiningu töfluskorðu og vörpun viðeigandi eiginda í líkanið í dálkum í töfluskorðunni.

### <a name="calculations"></a>Útreikningar

Útreikningar tákna ferli til að framkvæma reikniaðgerðir á afbrigðalíkani. Útreikningur getur til dæmis ákvarðað lengd tiltekins hráefnis eða vinnslutíma polishing aðgerð. Útreikningar eru grundvallaratriði og setja gildi í markmiðseigind eftir öllum eigindargildin sem eru innifaldar í útreikningssegð verða tiltækar.

### <a name="subcomponents"></a>Undiríhlutir

Undiríhlutir endurspegla hnúta í afbrigðalíkani afurðar. Fyrir hver vensl undirþáttagerð verður að tilgreina tilvísun í afurðarsniðmát sem er með tækni til skilgreiningar afbrigða stillt á skorðuskilgreiningu.

### <a name="user-requirements"></a>Notendakröfur

Þörf notanda hefur constituents yfir í undirþáttagerð. Eini munurinn er að þörf notanda er ekki bundin afurðarsniðmáti. Framkvæmd áhrif þessa munurinn er að allar uppskriftalínur eða leiðaraðgerð sem eru skilgreindar í samhengi við notanda þarfir eru dregin saman í yfirstig skipulag Uppskrift eða leið. Þessi hegðun er svipuð hegðun skugga uppskriftar.

### <a name="bom-lines"></a>Uppskriftarlínur

Uppskriftarlínur eru hafðar með til að auðkenna framleiðslufyrirtæki Uppskriftinni fyrir hvern íhlut. Í uppskriftalínu verður að vísa á vöru og alla eiginleika vöru er hægt að stilla á fast gildi eða varpað á eigind.

### <a name="route-operations"></a>Leiðaraðgerðir

Leiðaraðgerðir hafðar með til að auðkenna framleiðsluleiðina. Leiðaaðgerð verður að vísa skilgreinda aðgerð og öllum eiginleikum aðgerð er hægt að setja að föstu gildi. Hægt er að varpa alla eiginleika nema tilfangaþarfir eigind í staðinn fyrir gildið.

## <a name="validating-and-testing-a-product-configuration-model"></a>Villuleita og prófa afbrigðalíkan afurðar
Villuleit afbrigðalíkan afurðar getur átt sér stað á nokkrum stigum í líkaninu og því hægt að ná yfir mismunandi sviðum. Lægsta stig er fyrir staka segðarskorðu. Í þessu tilfelli villuleit eru yfirleitt framkvæmd af vöruhönnuður til að sannreyna málskipan segðar sé rétt.  

Á svipaðan hátt, er hægt að staðfesta skilyrðið fyrir uppskriftarlínu eða inn leiðaraðgerð í skyndimyndar.  

Einnig er hægt að framkvæma villuleit fyrir sem notandi skilgreinir skilgreiningu töfluskorðu. Í þessu tilfelli getur notandinn staðfest gildi sem eru færð inn fyrir hvert svæði sem eru innan léns samsvarandi gerða eiginda.  

Loks er hægt að framkvæma villuleit fyrir lokið afbrigðalíkan afurðar til að sannreyna málskipan lokið sé rétt og að allar nafngiftar- og líkanabreytum reglur hafi verið virtar.

### <a name="testing"></a>Prófun

Prófun á líkani svipar til þess að keyra raunverulega skilgreiningu setu. Notandinn getur gilda gegnum skilgreiningu síður og staðfesta skipulag líkan styður skilgreiningarferlið. Notandinn getur staðfest að eigindargildi séu rétt og lýsingar eigind leiðbeina notandanum að velja rétta gildi. Loks þegar prófun setu lýkur kerfið reynir að stofna Uppskrift og leið sem samsvarar til valda eigindagildi og birtir villuskilaboð ef eitthvað skyldi fara úrskeiðis.

### <a name="the-configuration-page"></a>Síðan Skilgreiningar

Smellið til að fletta á milli þátta, **Næsta**, eða þáttur í vörulíkanstré skilgreiningu til að setja áherslu á því að smella á.

## <a name="finalizing-a-model-for-configuration"></a>Ljúka líkan fyrir skilgreiningu
Þegar afbrigðalíkan afurðar er tilbúið til notkunar í aðstæðum skilgreina pöntun, verður að stofna útgáfu. Hins vegar eru nokkrir valkostir sem er hægt að auka upplifunina við líkanatréð.

### <a name="user-interface"></a>Notandaviðmót

Hægt er að breyta skilgreiningum notandaviðmóts með því að nota milliflokka eigindaflokka í einni eða fleiri undiríhlutir. Slík flokkun getur merkt vensl milli sérstakra eiginleika og auðveldað skilgreiningu notanda auðkenna svæði afurða sem er í víddaráherslu.

### <a name="templates"></a>Sniðmát

Hægt er að stofna eitt eða fleiri sniðmát skilgreiningar til að flýta skilgreiningarferlinu. Einnig er hægt að stofna sniðmát á skýrsluþjónsgreining ákveðna eigindin samsetningar, t.d. þegar sölupöntun herferð áherslu á ákveðin eiginleika afurðar.

### <a name="translations"></a>Þýðingar

Ef selja verður afurðina í mismunandi löndum/svæðum, hægt að stofna þýðingar fyrir allan texta sem birtist í Notandaviðmót skilgreiningar. Þessi texti inniheldur ekki einungis heiti og lýsing svæði, heldur einnig eigindagildi texta.

### <a name="versions"></a>Útgáfur

Síðasta og mikilvægustu skrefi í frágangsferlinu er að stofna útgáfu fyrir afbrigðalíkan afurðar. Útgáfa stendur fyrir vensl á milli afurðarsniðmáts sem hægt er að velja fyrir skilgreiningu á pöntun eða tilboðslínu og afbrigðalíkan afurðar. Útgáfa verður að vera samþykkt áður en hægt er að hefja hana og nota.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Útvíkka afbrigðalíkan afurðar gegnum API
Hefur verið útfærð í sérnýttu forritið forritun viðmót (API) svo að viðskiptaaðila og önnur sem hafa leyfi forritara er að útvíkka getu afbrigðalíkans afurðar. Aðal markmið hefur verið að stofna ferli sem gerir kleift að samstarfsaðila og viðskiptavina sem nota fyrirliggjandi Vörusamsetningu flytja kóði sem er felldur inn í Vörusamsetningu líkön sem á að API. Á þennan hátt er þær hægt flytja þeirra líkön úr vörusamsetningu í afbrigði vöru. Hins vegar getur það einnig gagnast nýjum viðskiptaaðilum og viðskiptavinum að nota API til að lengja nýja afbrigðalíkönum afurðar.

### <a name="pcadaptor-class"></a>PCAdaptor klasa

API er virkur með því að nota safn **PCAdaptor** klasar sem sýna gögn skipan afbrigðalíkönum afurðar. Tilvik í **PCAdaptor** klasa verður stofnuð fyrir hvert virðislíkan sem verður veitt. Eftir skilgreinarlotu er lokið kerfið athugar fyrir tilvik þennan klasa og keyrir hún ef slíkt finnst.  

Í eftirfarandi skýringarmynd útskýrir ferlið.  

[![Flæðisskýringarmynd](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

API-flæðisskýringarmynd afurðarafbrigða

## <a name="product-configuration"></a>Afurðarafbrigði
Hægt er að framkvæma skilgreiningu afurðar frá eftirfarandi stöðum:

-   Sölupöntunarlína
-   Sölutilboðslína
-   Innkaupapöntunarlína
-   Framleiðslupöntunarlína
-   Vöruþarfalína (verk)

Tilgangur skilgreiningarinnar er að stofna vöruvíddasamsetning einkvæmrar vöru sem uppfyllir kröfur viðskiptavinar. Einkvæmt skilgreiningarkenni er stofnað fyrir hverja nýja skilgreiningu. Þetta kenni gerir kleift að rekja í gegnum birgðir.

### <a name="multiple-sites-and-intercompany"></a>Mörg svæði og innan samstæðu

Ef afbrigði verður að framkvæma á svæði, eða jafnvel fyrirtæki, sem er önnur en svæði eða fyrirtækið þar sem framleiðslan mun eiga sér stað, Uppskrift og leið stofnuð fyrir og setja starfsstöð birgi supplying fyrirtæki. Afurðarafbrigðið verða losaðar fyrirtækja sem taka þátt í birgðakeðjunni.




