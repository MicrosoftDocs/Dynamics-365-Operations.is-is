---
title: Yfirlit yfir líftímastöðu afurðar
description: Lífferilsstaða afurðar skráir lífferilsstöðu útgefinnar vöru eða vöruafbrigðis.
author: cvocph
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 1def67750fe6328087fe6bf7eeb22105232390fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820203"
---
# <a name="product-lifecycle-state-overview"></a>Yfirlit yfir líftímastöðu afurðar

[!include [banner](../includes/banner.md)]

Lífferilsstaða afurðar skráir lífferilsstöðu útgefinnar vöru eða vöruafbrigðis. Lífferilsstöður afurða eru skilgreind af notanda, yfirleitt framleiðslustjóra eða vara aðalgagna-framleiðslustjóra. Tilteknir viðskiptaferlar, svo sem aðaláætlanagerð, geta orðið fyrir áhrifum af tiltekinni lífferilsstöðu.

Útgefin vara eða varaafbrigði getur tengst lífferilsstöðu afurðar sem skráir í hvaða lífferilsstöðu tiltekin afurð eða afbrigði er nú. Þú getur skilgreint hvaða fjölda lífferilsstöðu afurða sem er, með því að úthluta heiti og lýsingu á stöðunni. Þú getur valið eina lífferilsstöðu sem sjálfgefið stöðu fyrir nýjar útgefnar afurðir. Útgefin afurðaafbrigði erfa sína lífferilsstöðu afurðar frá útgefnu afurðasniðmáti þeirra við sköpun. Þegar þú breytir lífferilsstöðu á útgefnu afurðasniðmáti, getur þú valið að uppfæra öll núverandi afbrigði sem hafa sama upprunalega stöðuna.  

## <a name="create-a-new-product-lifecycle-state"></a>Stofna nýja líftímastöðu afurðar

- Til að búa til nýja lífferilsstöðu afurðar, sjá [Búðu til nýja lífferilsstöðu afurðar](tasks/new-product-lifecycle-state.md).

- Til að búa til sjálfgefið lífferilsstaða afurðar, sjá [Búa til sjálfgefið lífferilsstaða afurðar](tasks/default-product-lifecycle-state.md).

## <a name="associate-product-lifecycle-states-to-released-products"></a>Tengja lífferilsstöðu afurðar við útgefnar afurðir  

Það eru margar leiðir til að tengja lífferilsstöðu afurðar við útgefnar afurðir eða afurðaafbrigði.

- Við stofnun nýrrar útgefinnar afurðar er sjálfgefin **Lífferilsstaða afurðar** úthlutað sjálfkrafa.
- Við útgáfu afurðar til lögaðila, er sjálfgefin **Lífferilsstaða afurðar** úthlutað sjálfkrafa.
- Við útgáfu afurðaafbrigða til lögaðila, er **Lífferilsstaða afurðar** sem tengd er við útgefið afurðasniðmát í þessum lögaðila, sjálfkrafa úthlutað til nýja afbrigðisins.

Hægt er að uppfæra lífferilsstöðu afurðar handvirkt með því að nota:

- Listasíða **Útgefnar afurðir** eða **Upplýsingar yfirlit**.
- Listasíða **Útgefin afurðaafbrigði** lista síðu eða **Upplýsingar yfirlit**.
- Finndu úreltar afurðir eða afurðaafbrigði sem byggist á eftirspurn og tengdu við það lífferilsstöðu.  

Frekari upplýsingar:

- Til að tengja lífferilsstöðu afurðar við útgefinn afurðasniðmát sjá [Úthlutaðu lífferilsstöðu afurðar til útgefins afurðasniðmáts](tasks/product-lifecycle-state-released-product-master.md).

- Til að tengja lífferilsstöðu afurðar við útgefna afurð s´já [Úthlutaðu lífferilsstöðu afurðar til útgefinnar afurðar](tasks/product-lifecycle-state-released-product.md).

## <a name="impact-on-master-planning"></a>Áhrif á aðaláætlanagerð

Lífferilsstaða afurðar hefur aðeins eina stýringarmerki: **Er virkt fyrir áætlanagerð**. Sjálfgefið er þetta stillt á **Já** fyrir allar tilbúnar lífferilsstöðu afurðar, en það er hægt að breyta í **Nei**. Þegar stillt er á **Nei**, eru tengdir útgefnar afurðir eða útgefin afurðaafbrigði:

- Útilokuð frá aðaláætlanagerð.
- Útilokuð frá útreikningi á BOM-stigi.

Nánari upplýsingar um hvernig á að nota lífferilsstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð og útreikningum á BOM-stigi, sjá [Búðu til lífferilsstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð](tasks/exclude-products-master-planning.md).

> [!NOTE]
> Af ástæðum tengdum afköstum, er mjög mælt með því að tengja allar úreltar afurðir eða afurðaafbrigði, sérstaklega þegar unnið er með óendurnotanleg grunnstillingaafbrigði afurða, við lífferilsstöðu afurðar sem er óvirkt fyrir aðaláætlanagerð.  

## <a name="default-migration-import-and-export"></a>Sjálfgefinn flutningur, innflutningur, og útflutningur

Líftímastöður afurðar eru ekki studdar af gagnaeiningum og líftímastöðu er hægt að stilla í breytilega stöðu gegnum annaðhvort gagnaeiningu útgefinnar afurðar eða gagnaeiningu útgefins afbrigðis.

## <a name="find-obsolete-products-and-products-variants"></a>Finna úreltar afurðir og afurðarafbrigði

Þú getur keyrt hermigreiningu til að finna úreltar afurðir eða afurðaafbrigði og síðan uppfæra lífferilsstaða afurðar þeirra. Til að finna úreldar afurðir, sjá [Finna úrelt afurðaafbrigði og úthluta lífferilsstöðu afurðar](tasks/obsolete-product-variants.md). Þetta efni sýnir hvernig á að finna úreltar afurðir eða afurðaafbrigði og hvernig á að tengja lífferilsstöðu afurðar við úreltar afurðir. Það sýnir einnig hvernig skal skoða herminiðurstöðurnar og meta hversu margar afurðir og afurðaafbrigði verða tengd nýjum lífferilsstaða afurðar þegar keyrð er uppfærslan án hermunar.  

Með því að keyra greininguna í hermistillingu, birtist afurðir og afurðaafbrigði sem eru úreltar á tilteknu formi, þar sem hægt er að endurskoða þær auðveldlega. Greiningin leitar að færslum og tilteknum aðalgögnum til að bera kennsl á afurðir sem hafa enga eftirspurn innan breytilegs tímabils og engar aðalgögn sem geta leitt til eftirspurnar. Nýjar afurðir sem gefnar eru út innan breytilegs tíma má útiloka frá greiningunni. Þegar hermigreiningin skilar áætluðum niðurstöðum getur notandinn keyrt greininguna og sett nýtt lífferilsstaða afurðar til allra afurða sem auðkenndar eru úreltar með greiningunni.  

> [!NOTE]
> Athugaðu að allar greiningar og uppfærslur verða að vera gerðar innan sama lögaðila.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Viðmiðanir til að velja og uppfæra útgefnar afurðir eða afurðaafbrigði

Notaðu eftirfarandi viðmiðanir til að velja og uppfæra útgefnar afurðir eða afurðaafbrigði:

- Lífferilsstaða afurðar eða afurðarafbrigðis verður að vera frábrugðin nýju, áformuðu ástandi.
- Afurðin eða afurðarafbrigðið var búið til fyrir nokkrum dögum síðan miðað við fjölda daga sem þú slærð inn í svargluggann fyrir val.
- Það eru engar opnar framleiðslupantanir (= staða < lokið) fyrir afurð eða afurðaafbrigði.
- Það eru engar opnar birgðafærslur (= staða útgáfa ReservPhysical til QuotationIssue eða staða innhreyfingar Skráð í QuotationReceipt) fyrir afurð eða afurðaafbrigði.
- Engin birgðafærslur eiga sér stað á síðustu dögum fyrir afurð eða afurðaafbrigði.
- Það er engin framtíðareftirspurn eða framboðspá fyrir afurð eða afurðaafbrigði.  
- Engin lágmarks birgðir hefur verið stillt í vöruþekju fyrir afurð eða afurðaafbrigði.
- Engin föst kanban-regla virk fyrir afurð eða afurðaafbrigði.  
- Engar þjónustupöntunarlínur fyrir afurð eða afurðaafbrigði.
- Engar virkar eða framtíðar sölu- eða innkaupsamningslínur fyrir afurð eða afurðaafbrigði.
- Afurð eða afurðaafbrigði er ekki notuð í BOM sem tengist samþykktri BOM útgáfu sem ekki er útrunnin fyrir afurð eða afbrigði sem er virk fyrir áætlunargerð.

## <a name="related-topics"></a>Tengd efnisatriði

- [Stofna nýja líftímastöðu afurðar](tasks/new-product-lifecycle-state.md)
- [Stofna sjálfgefna líftímastöðu afurðar](tasks/default-product-lifecycle-state.md)
- [Úthluta líftímastöðu afurðar til útgefins afurðarsniðmáts](tasks/product-lifecycle-state-released-product-master.md)
- [Úthluta líftímastöðu afurðar til útgefinnar afurðar](tasks/product-lifecycle-state-released-product.md)
- [Finna úrelt afurðaafbrigði og úthluta lífferilsstöðu afurðar](tasks/obsolete-product-variants.md)
- [Búa til lífferlisstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð](tasks/exclude-products-master-planning.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]