---
title: Uppsetning eigna
description: Þetta efnisatriði veitir yfirlit yfir uppsetningu á einingunni Eignir.
author: moaamer
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f624ddc2e7b8f59a2ba002d757ce68ee222a7223
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216587"
---
# <a name="set-up-fixed-assets"></a>Uppsetning eigna

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir uppsetningu á einingunni **Eignir**. 

Færibreytur stjórna almennri hegðun innan eignar. Eignaflokkar leyfa þér að flokka eignunum og tilgreina sjálfgefnar eigindir fyrir hverja eign sem er úthlutað á flokk. Bókum er úthlutað á eignaflokka. Bækur rekja fjárhagslegu virði eignar yfir tíma með því að nota skilgreiningu afskriftir sem tilgreind er í afskriftareglu.

Eignir eru úthlutaðar flokki þar sem þær eru stofnaðar. Að sjálfgefnu eru bækur úthlutað eignaflokki sem er svo úthlutað á eign. Bækur sem eru skilgreind til að bóka í fjárhaginn tengjast bókunarreglu. Fjárhagslyklar eru skilgreindir fyrir hverja bók í bókunarreglu og eru notaðir þegar eignafærslur eru bókaðir.

![Eignahlutar](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Afskriftarreglur

Þú ættir fyrst að setja upp afskriftarreglur. Í Afskriftaregla er skilgreint hvernig virði eignar er afskrifað með tímanum. Þú þarft að skilgreina aðferð við afskrift, afskriftarár (almanaksár eða fjárhagsár) og tíðni afskrifta. Fyrir frekari upplýsingar, sjá [Setja upp og stofna afskriftarreglur](tasks/set-up-depreciation-profiles.md).

## <a name="books"></a>Bækur

Eftir að setja upp afskriftareglur, verður að stofna nauðsynleg bækur fyrir eignunum. Hver bók rekur óháð fjárhagslegan lífsferil eigna. Hægt er að skilgreina bækur til að bóka tengdar færslur í fjárhag. Þessi skilgreining er sjálfgefna stillingin, þar sem það er yfirleitt notuð við fjárhagsskýrslugerð fyrirtækis. Bækur sem bóka ekki í fjárhag bóka aðeins í undirbókar eignar og yfirleitt notuð fyrir skattskýrslugerð.

Aðalafskriftaregla er úthlutað á hvert bók. Bækur hafa einnig afskriftareglu umskipta, ef þessa gerð forstillingar á við. Til að láta hafa eignabók sjálfkrafa með í keyrslum afskrifta, þarf að virkja á **Reikna afskrift** valkostur. Ef þessi valkostur er ekki virkur fyrir eign sleppir afskriftartillagan eigninni.

Einnig hægt að setja upp afleiddar bækur. Tilgreindar afleiddar færslur eru bókaðar á móti afleiddu bókunum sem nákvæm afrit af aðalfærslunni. Þar af leiðandi eru afleiddra færslna yfirleitt settir upp fyrir kaup og losanir, en ekki fyrir afskriftarfærslur. Nánari upplýsingar um það eru í [Setja upp virðislíkön](tasks/set-up-value-models.md).

Valkostur á síðunni **Færibreytur eigna** gerir kleift að kveikja eða slökkva á læsingaraðgerðinni. Þessi eiginleiki er virkjaður á **Vinnusvæði eiginleikastjórnunar**.

## <a name="fixed-asset-posting-profiles"></a>Bókunarreglur eigna

Eftir að þú setur upp bækur, geturðu stofnað bókunarreglur. Bókunarreglu verður að skilgreina með bók, en einnig er hægt að skilgreina það á ítarlegri stigi. Til dæmis er hægt að skilgreina bókunarreglu fyrir samsetningu bókar og eignaflokks eða jafnvel fyrir einstaka eignabók. Að sjálfgefnu eru fjárhagslykla sem eru skilgreindar notaðir fyrir eignafærslur.

Skilgreina verður fjárhagslykla sem notaðar eru við losunarferli, bæði sölulosun og rýrnunarlosun. Á losunartíma eru áður bókaðar eignafærslur bakfærðar úr upprunalegum lyklum. Nettóupphæðin er síðan færð á viðeigandi lykil fyrir hagnað og tap fyrir eignalosun. Til að hjálpa til við að tryggja að fræslur séu bakfærðar á réttan hátt, verður að setja upp lyklana fyrir hverri gerð færslunnar sem notað er í fyrirtækinu. Aðallykilinn ætti að vera upprunalegi lykillinn sem stilltur var í bókunarreglu fyrir viðkomandi gerð færslu og mótlykill ætti að vera þinn hagnaður og tap fyrir losunarreikninginn. Undantekningin er bókað nettóvirði. Í þessu tilfelli ætti að stilla bæði aðallykilinn og mótlykil á hagnað og tap fyrir losunarreikninginn. Nánari upplýsingar er að finna í [Setja upp bókunarreglur eigna](tasks/set-up-fixed-asset-posting-profiles.md).

## <a name="fixed-asset-groups"></a>Eignaflokkar

Svæðið **Eignaflokkur** er eini áskilda svæðið þegar eign er stofnuð. Gildið í þessu svæði ákveður sjálfgildi nokkurra upplýsingasvæða fyrir eignina. Bækur eru settar upp þannig að sjálfgefna bókin er úthlutað á hverja eign í flokki. Þannig geta eigindin sem þú setur fyrir bækurnar verið sérstakar fyrir eignahóp. Þessi eigindi fela í sér líftíma og afskriftarreglu.

Einnig er hægt að skilgreina sérstakar heimildir til afskrifta eða viðbótarafskriftir, fyrir tiltekna samsetningu eignaflokks og bókar. Úthluta verður forgangur á sérstök heimild til afskriftar til að tilgreina röðina sem heimildir eru reiknaðar í þegar margar heimildir eru úthlutaðar á bók. Nánari upplýsingar er að finna í [Setja upp eignaflokka](tasks/set-up-fixed-asset-groups.md).

## <a name="journal-names"></a>Færslubókanöfn

Á síðunni **Heiti færslubókar** verður þú að stofna heiti færslubókanna sem á að nota með færslubók eignar. Þú verður að stilla svæðið **Færslubókargerð** á **Bóka eignir**. Stilltu svæðið **Fylgiskjalarunur** þannig að heiti færslubóka séu notuð fyrir færslubók eignar. Færslubækur eigna skulu ekki nota stillinguna **Eingöngu númer fylgiskjals** vegna þess að nokkrir sjálfvirkir ferlar, eins og gagnaflutningar og skipti, krefjast sérnúmers á fylgiskjali.

## <a name="fixed-asset-parameters"></a>Eignafæribreyta

Síðasta skrefið er að uppfæra færibreytur eigna.

**Fjármögnunarþröskuldi** svæði ákvarðar eignir sem eru afskrifaðar. Ef innkaupalína er valin sem föst eign, en hún uppfyllir ekki tilgreindum fjármögnunarþröskuldi, er eign enn stofnaðar eða uppfærðar, en **Reikna afskrift** valkostur er stilltur á **Nei**. Þess vegna verður eignin ekki afskrifuð sjálfkrafa sem hluti af afskriftartillögunum.

Einn mikilvægur valkostur er nefndur **Stofna sjálfvirkt leiðrétta afskriftaupphæðir með losun**. Þegar þessi valkostur er stilltur á **Já** er afskrift eignar sjálfvirkt leiðrétt, byggt á afskriftirnar afskriftar við losun eignar. Annar valkostur gerir þér kleift að draga staðgreiðsluafslátt frá kaupupphæðinni þegar þú kaupir eign með því að reikning lánardrottins.

Færibreytan **Læsa eignabókum í afskriftabók** gerir kleift að læsa eignabókum í afskriftabók. Þegar afskriftarfærslur eru bókaðar mun kerfið ganga úr skugga um að sömu eignabókinni hafi ekki verið bætt við fleiri en eina afskriftabók. Ef svo er verður eignabókinni læst og bókunin stöðvuð. Ef auðkenni eignabókar er í læstri færslubók verður hún aflæst sjálfkrafa þegar bókun lýkur fyrir upprunalegu færslubókina. Einnig er hægt að læsa færslubókinni handvirkt. 

Í flýtiflipi **Innkaupapantanir** er hægt er skilgreina hvernig eignir eigi að vera stofnaðar sem hluti af innkaupaferli. Fyrsti valkostur er nefndur **Leyfa eignakaup frá innkaupum**. Ef þessu valkostur er stilltur á **Já**, eiga eignakaup á sér stað þegar reikningur er bókaður. Ef þessi valkostur er stilltur á **Nei** er enn hægt að setja eign á innkaupapöntunina (IP) og reikning, en kaupin verða ekki bókuð. Bókun verður að framkvæma sem sérstakt skref úr færslubók eignar. Valkosturinn **Stofna eign við bókun innhreyfingarskjals afurða eða reiknings** gerir þér kleift að stofna nýja eign "fyrirvaralaust" við bókun. Þess vegna þarf eignin ekki að vera uppsett sem eign fyrir færsluna. Síðasta valkostinum **Gá að stofnun eigna við innfærslu lína**, á einungis við innkaupabeiðnir.

Hægt er að skilgreina ástæðukóða svo þeirra sé krafist fyrir breytingar á eign eða fyrir tiltekna eignafærslur.

Loks í flipanum **Númeraraðir** skilgreinir þú númeraraðir fyrir eignir. Hægt er að hnekkja númeraröð **Eignar** með númeraröð **Eignaflokks** ef hún hefur verið tilgreind.

Nánari upplýsingar sjá [Stofna eign](tasks/create-fixed-asset.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
