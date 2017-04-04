---
title: "Notið uppflettingu til að finna upplýsingar"
description: "Mörg svæði hafa uppflettingar getur hjálpað við að finna auðveldlega rétt eða viðeigandi gildi í Microsoft Dynamics 365 fyrir Aðgerðir. Nokkrar viðbætur hefur verið bætt við uppflettingar sem gera þessar stýringar fleiri nothæf og notendur gera á fleiri framleiðinna. Í þessu efnisatriði er mun læra um þessar aðgerðir nýja leit og fær sumar góð ráð til að fá ákjósanlegar notkun úr uppflettingum í kerfinu."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Notið uppflettingu til að finna upplýsingar

Mörg svæði hafa uppflettingar getur hjálpað við að finna auðveldlega rétt eða viðeigandi gildi í Microsoft Dynamics 365 fyrir Aðgerðir. Nokkrar viðbætur hefur verið bætt við uppflettingar sem gera þessar stýringar fleiri nothæf og notendur gera á fleiri framleiðinna. Í þessu efnisatriði er mun læra um þessar aðgerðir nýja leit og fær sumar góð ráð til að fá ákjósanlegar notkun úr uppflettingum í kerfinu.  

<a name="responsive-lookups"></a>Responsive uppflettingar
------------------

Í fyrri útgáfum Dynamics 365 fyrir Aðgerð þegar gefur með uppflettingu eftirlit, myndi notandi með taki yfirlýst aðgerð til að opna í fellilista. Þetta gæti hafa verið með því að færa inn stjörnu (\*) í stýringu til að sía uppfletting byggt á núverandi gildi stýringarinnar, því að smella á hnappinn fellilistanum eða með því að nota í **Alt**+**Niður ör** flýtilykli. Uppfletting stýrir hefur verið breytt á eftirfarandi hátt betur framleiðslupöntunarmagns gildandi vefnum venjum:

-   Uppfletting valmyndunum fellilistanum nú opnast sjálfkrafa eftir slight hlé á því að slá, með fellilistinn innihaldi fyrir valmyndinni síuð eftir gildi uppfletting fjárhagsáætlunarstýringar.
    -   Athugið að gamla hegðun sjálfvirka opnun á dropdown eftir því að færa inn stjörnu (\*) hefur verið hafnað.
-   Eftir að uppfletting fellilista hefur opnað eftirfarandi á sér stað:
    -   Bendillinn áfram í stýringu uppfletting (en ekki flutt inn í fellilista áherslu) svo hægt er að halda áfram að gera breytingar á gildi stýringarinnar. Hins vegar notandinn enn hægt að nota í **Upp ör** og **Niður ör** til að breyta línum í á fellilista og færa inn til að velja núgildandi línu í fyrir fellilista.
    -   Innihald í fellilista verður að leiðrétta eftir hvaða breytingar eru gerðar stýringu uppfletting gildi.

Til dæmis, íhugið í uppflettisvæðinu kallað **Borg**. 

Þegar áhersla er á **Borg** er hægt að hefja leitað borg sem óskað er með því að slá nokkrar stafi, eins og "col."  Eftir því að slá að stöðva uppfletting opnast sjálfkrafa síuð til að þær borgir sem byrja á "col". 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

Á þessum tímapunkti, er bendillinn enn í uppflettisvæðinu. Ef haldið er áfram því að slá svo gildið "colum" er uppfletting innihaldi leiðrétta sjálfkrafa til að endurspegla er síðasta gildi stýringarinnar. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Jafnvel þótt áhersla er enn uppfletting stýringu er einnig hægt að nota í **Upp ör** eða **Niður ör** lykla til að merkja línuna sem á að velja. Ef smellt er á **Færið** auðkenndu línuna verða valdar úr leitinni og gildi stýringarinnar verða uppfærðar. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Því að slá í meira en Kennum
Þegar gögnum er færð inn er raunlykils fyrir notendur tilraun til að auðkenna aðila, eins og viðskiptavin eða lánardrottinn með heiti en ekki kenni fyrir eininguna. Í þessari útgáfu af Dynamics 365 aðgerða nú leyfir vefumhverfi gagnainnfærslu uppflettingar margar (en ekki öll). Þessi eiginleiki öflug leyfir notandanum að færa Kenni eða nafn samsvarandi í stýringu uppflettingu. 

Til dæmis, íhugið á **viðskiptavinalykil** þegar sölupöntun er stofnuð. Þetta svæði sýnir á **Kenni Þjónustureikningsins** til viðskiptavinarins, en notandi væri yfirleitt æskilegt að færa inn í **lykilheiti** í stað er **Kenni Þjónustureikningsins** fyrir þetta svæði þegar sölupöntun er stofnuð, eins og "Skóginum Hafa Wholesales" en "US-003."

Ef notandinn byrjað að færa inn **Kenni Þjónustureikningsins** í stýringu uppflettingu í fellilista myndi sjálfkrafa opna eins og lýst er í fyrri hluta og myndi sjá uppfletting eins og sýnt er hér að neðan.

[![Vefumhverfi uppfletting þegar færður er inn Kenni fyrir reikning viðskiptavinar](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Hins vegar notanda einnig nú má færa inn upphaf í **lykilheiti** einnig. Ef það er, svo sem mun notandinn sjá eftirfarandi uppflettingu. Tilkynning hvernig **Heiti** dálkur flutt að vera í fyrsta dálki uppfletting og hvernig uppfletting raðað og síuð samkvæmt á **Heiti** dálk.

[![Vefumhverfi uppfletting þegar færð er inn nafn viðskiptavinar](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Með hnitaneti haus dálks til ítarlegri síunar og röðunar
Uppfletting endurbætur sem fjallað er um í tvo kafla fyrri mjög auka notanda kleift að fara í línur í "byrja" leit á grundvelli uppfletting í **Kenni** eða **Heiti** í uppflettisvæðinu. Hins vegar eru aðstæður sem ítarlegri síun (eða röðun) þarf til að finna í réttri röð. Í þessum aðstæðum þarf notandann til að nota síunarskilyrði og raða valkosti í hnitanetinu haus dálks í uppflettisvæðinu. Til dæmis, íhugið starfsmanns við sölupöntunarlínu sem þarf að staðsetja hægri "köplum" sem afurðar. Því að slá "köplum" í á **Vörunúmer** stýringin er ekki hjálplegt, eins og það eru engar nöfn afurða sem byrja á "köplum." 

![emptyitemlookup](./media/emptyitemlookup.png) 

Þess í stað sem notandi þarf að hreinsa gildi stýringarinnar uppfletting opna uppfletting fellilista og sía fellilista með dálkfyrirsögn hnitanets, eins og sýnt er hér að neðan. Mús (eða snertingu nákvæmlega) notandinn getur einfaldlega smellið (eða snertiskjár) hvaða dálkhaus að komast í valkosti síunar og röðunar fyrir dálk sem. Lyklaborð notanda, notandinn einfaldlega þarf að ýta á **Alt**+**Niður****ör** seinni tíma til að fara inn í fellilista, eftir sem notandinn getur flipanum í dálkinn rétt og styðjið síðan **Ctrl**+**G** til að opna í hnitanetinu dálkur haus fellilista. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Eftir hefur verið notuð í síu (sjá myndinni hér fyrir neðan), getur notandinn finna og velja línuna eins og venjulega. 

![filtereditemlookup](./media/filtereditemlookup.png)


