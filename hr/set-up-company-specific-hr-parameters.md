---
title: "Setja upp færibreytur mannauðs bundnar tilteknu fyrirtæki"
description: "Stillingar fyrir sumar færibreytur Mannauðs (HR) eru eins milli fyrirtækja, á meðan stillingar annara færibreyta eru bundnar tilteknu fyrirtæki. Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs sem eru bundnar tilteknu fyrirtæki."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: f83bc127f7bf3cdceb39a79c1e69f4f7e96f6462
ms.openlocfilehash: ef84ad6e90e7c58ea921930e23b67228d393bc7e
ms.contentlocale: is-is
ms.lasthandoff: 06/19/2017


---

# <a name="set-up-company-specific-hr-parameters"></a>Setja upp færibreytur mannauðs bundnar tilteknu fyrirtæki

[!include[banner](includes/banner.md)]


Stillingar fyrir sumar færibreytur Mannauðs (HR) eru eins milli fyrirtækja, á meðan stillingar annara færibreyta eru bundnar tilteknu fyrirtæki. Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs sem eru bundnar tilteknu fyrirtæki.

Tvær síður eru notaðar til að setja upp færibreytur mannauðs (HR). Fyrir Færibreytur sem fyrirtæki samnýta, notarðu **samnýttar færibreytur fyrir mannauð** síðu. Fyrir færibreytur sem eru bundin tilteknu fyrirtæki (með öðrum orðum, stillingar eiga við um eitt fyrirtæki), notarðu **færibreytum mannauðs** síðu. Á **færibreytur Mannauðs** síða, er stillingum deild á sex flipa:

-   Almennt
-   Ráðningar - þetta er ekki teki' með í Dynamics 365 for Talent
-   Laun
-   Númeraraðir
-   Family and Medical Leave Act (lög um leyfi vegna fjölskyldu eða veikinda)
-   Sjálfsafgreiðsla starfsmanna

Hver flipi inniheldur upplýsingar sem tengjast einu fyrirtæki. Stillingar á í **Almennt** flipanum skilgreina útlit hvers upplýsinga um fjarvistir, meiðsla og veikinda og nýráðningar. Stillingar á þessum flipa skilgreina einnig sumar sjálfgefnar færslur sem birtast meðfram vinnu. Þessi flipi leyfir þér nákvæmlega að velja lit til að hafa á opnum fjarvistarfærslum, stílblað til að nota fyrir skýrslur, virkja á samþættinguna á milli þjálfunarnámskeiða og fjarvistarskráningar og veljið fjarvistarkóðann sem á að nota til að stýra þessari samþættingu. Einnig er hægt að tilgreina hversu lengi atvikum meiðsla og veikindamála á að halda og tilgreina sjálfgefið auðkennisnúmer sem er sýnt þegar nýr starfsmaður er ráðinn. 

Stillingar á **Ráðningarverk** flipa er að skilgreina gerðir skjala sem eru notaðar fyrir samskipti sem er sjálfkrafa sent umsækjendum og ráðningarverkið sem er notað fyrir óumbeðnar umsóknir (umsóknir sem ekki eru fyrir tiltekið ráðningarverk). Tímabilið sem er skilgreint fyrir aldursgreiningu ráðningarverks ákvarðar ráðningarverk sem eru innifalin á **aldursgreiningarverk** reitnum í **umsjón með ráðningum** vinnusvæði. Tímabilið sem er skilgreint fyrir viðvörun lokafrests umsóknar er notað til að birta ráðningarverk sem eru að nálgast skilafrest sinn á í **skilafrestur umsóknar nálgast** reit í **Ráðningarverk** vinnusvæði. 

Stillingar á **Laun** flipanum skilgreina hvort notendur verða staðfesta að þeir vilji að vista upplýsingar fyrir fast eða breytilegt launafyrirkomulag. Ef gátreiturinn **Virkja villuleit vistunar** er valinn fá notendur skilaboð þegar þeir loka síðu sem tengist launum þar sem spurt er hvort þeir vilji vista færsluna. Sumar síður í lausnastjórnun leyfa ekki notendum að eyða upplýsingum. Þess vegna, með því að senda kvaðningu til notenda til að staðfesta að þeir vilja að vista upplýsingar, gætirðu takmarkað magn upplýsinga sem er vistað en ekki er hægt að eyða síðar. Ef **Virkja villuleit vistunar** gátreiturinn er hreinsaður eru færslur alltaf vistaðar strax, mögulega áður en notandinn er tilbúinn. Ef þú er ekki að nota frammistöðustjórnun er leyfir **Launa** flipinn þér einnig að velja einkunnalíkan til að nota í staðinn fyrir líkanið sem er úthlutað á launafyrirkomulag þegar verið er að gefa frammistöðu einkunn. 

### <a name="previously-released-functionality"></a>Áður losaðar virkni
Stillingarnar á flipanum **númeraröð** ákvarða raðir sem verða notuð til að úthluta sjálfkrafa auðkenni á liði í mannauði, svo sem umsókn, fjarvistarskráningar, viðburðir, niðurstöður launavinnsla, málsnúmer, námskeið og námskeiðsdagskrá. Til að vinna með tilvísanir númeraraða og kóða í **Númeraraðir** listasíðu (smellt er á **Fyrirtækisstjórnun** &gt; **Númeraraðir** &gt; **Númeraraðir**).

### <a name="if-youre-using-dynamics-365-for-talent"></a>Ef verið er að nota Dynamics 365 til Talent
Stillingarnar á flipanum **númeraröð** ákvarða raðir sem verða notuð til að úthluta sjálfkrafa auðkenni á liði í mannauði, svo sem umsókn, fjarvistarskráningar, viðburðir, niðurstöður launavinnsla, málsnúmer, námskeið og námskeiðsdagskrá. Til að vinna með tilvísanir númeraraða og kóða skal nota listasíðuna **Númeraraðir** (smellt er á **Kerfisstjórnun** &gt; **Tenglaflipi** &gt; **Númeraraðir** &gt; **Númeraraðir**). 

Stillingar á í **FMLA** flipa skilgreina hversu margar stundir starfsmaður verður að vinna til að tækur fyrir FMLA fríðindi, tíma í starfi sem er krafist fyrir hæfni, og upphafsdagsetningu ráðningar sem er notuð til að ákvarða lengd ráðningar. stillingar Skilgreina einnig fjölda stunda FMLA stunda sem starfsmenn eiga rétt á og FMLA leyfisdagatal sem er notuð til að reikna út hversu margir FMLA klukkustundir starfsmenn hafa notað. **FMLA** flipi er einungis tiltækt fyrir fyrirtæki í Bandaríkjunum. 

**Ábending:** fjölda stunda sem er unnið má ekki fara yfir 1,250 og lengd ráðningar má ekki fara yfir 12 mánuði. Þessi hámarksgildi eru samkvæmt alríkislögum í Bandaríkjunum. Að lokum, stillingar á í **sjálfsafgreiðslu Starfsmanns** flipanum ákvarða upplýsingar sem stjórnandi getur fært inn fyrir hönd starfsmanns hans eða hennar.

<a name="see-also"></a>Sjá einnig
--------

[Setja upp færibreytur mannauðs (HR) á milli lögaðila](set-up-hr-parameters-across-legal-entities.md)




