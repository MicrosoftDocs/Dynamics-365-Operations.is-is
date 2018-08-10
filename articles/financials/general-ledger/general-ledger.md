---
title: "Fjárhagur og Fjárhagsleg skýrslugerð heimasíða"
description: "Fjárhagur er notaður til að skilgreina og stjórna fjárhagslegum færslum í lögaðila."
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 03bab1d03be71c0e23a6ea93f542d6a52a212a1f
ms.openlocfilehash: 9ee3f73cd11b38ed2237ea3fe08db18000e55f07
ms.contentlocale: is-is
ms.lasthandoff: 06/25/2018

---

# <a name="general-ledger"></a>Fjárhagur 

[!include [banner](../includes/banner.md)]

Fjárhagur er notaður til að skilgreina og stjórna fjárhagslegum færslum í lögaðila. Í fjárhag er skrá fyrir debet og kredit færslur. Þessar færslur eru flokkaðar með lyklarnir sem taldir eru upp í línuriti yfir lykla. 

 - [Yfirlit yfir bókhaldslykil](plan-chart-of-accounts.md)
 - [Aðallykilgerðir](main-account-types.md)

Hægt er að úthluta eða dreifa peningarupphæðum  á einn eða fleiri reikninga eða reikning og samsetningar reikningsvídda byggt á úthlutunarreglum. Til eru tvær gerðir úthlutunar: föst og breytileg. Einnig er hægt að jafna færslur á milli fjárhagslykla og endurmeta upphæðir gjaldmiðla. Við lok fjárhagsársins þarf að undirbúa lyklana fyrir næsta fjárhagsár og loka núverandi fjárhagsárunum. Hægt er að nota sameiningaraðgerðin til að sameina fjárhagsniðurstöður nokkurra dótturfyrirtækja lögaðila í niðurstöðum eina, sameinað fyrirtæki. Dótturfyrirtækin geta verið í sama Microsoft Dynamics 365 for Finance and Operations gagnagrunni eða aðskildum gagnagrunnum.

- [Yfirlit yfir samstæðu og niðurfellingu](../budgeting/consolidation-elimination-overview.md)
- [Fjárhagslykilstöður](general-ledger-account-balances.md)
- [Fjárhagsvíddir](financial-dimensions.md)

[![Viðskiptaferli](./media/GL-process.PNG)](./media/GL-process.PNG)

## <a name="sales-tax"></a>Virðisaukaskattur
Hvert fyrirtæki innheimtir og greiðir skatta til ýmissa skattyfirvalda. Reglur og taxtar eru mismunandi eftir landi/svæði, fylki, sýslu og borg.
Þar að auki þarf að uppfæra reglur reglulega þegar kröfur skattyfirvalda breytast. Í VSK-kóða eru grunnupplýsingar um hversu mikið er innheimt og greitt til yfirvalda. Þegar settur er upp vsk-kóði, skilgreinirðu upphæðirnar og prósentur sem þarf að innheimta. Einnig skilgreinirðu ýmsar aðferðir sem notaðar eru þegar þessum upphæðum eða prósentum er beitt á færsluupphæðir. Efnisatriðin í þessum hluta veita upplýsingar um hvernig setja á upp VSK-kóða fyrir aðferðirnar og taxtana sem skattyfirvöld krefjast.

 - [Yfirlit virðisaukaskatts](indirect-taxes-overview.md)
 - [Virðisaukaskattur byggður á jaðargrunns- og útreikningsaðferðum](marginal-base-field.md)
 - [VSK-greiðslur og sléttunarreglur](round-sales-tax-payments.md)


## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="whats-new"></a>Nýjungar

Farðu í [Útgáfuupplýsingar](https://docs.microsoft.com/en-us/business-applications-release-notes/) til að sjá hvaða nýju eiginleikar hafa verið gefnar út. 

### <a name="videos"></a>Myndbönd

Kynntu þér kennslumyndbönd sem eru aðgengileg á [YouuTube-rás Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).

### <a name="blogs"></a>Blogg

Á [Microsoft Dynamics 365-blogginu](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) er að finna umfjöllun, fréttir og aðrar upplýsingar um Viðskiptaskuldir og aðrar hugbúnaðarlausnir.

Hægt er að finna margar færslur um fjárhag á [bloggi afurðarteymis Microsoft Dynamics AX](https://blogs.msdn.microsoft.com/dax/). Þó svo sumar þessara færslna voru skrifaðar um eldri útgáfu fjárhagsins eiga sömu hugtök eiga enn við og ferlin eru svipuð í nýjustu útgáfunni.

[Blogg Microsoft Dynamics Operations-samstarfsaðila](https://community.dynamics.com/partner/b/operationspartnercommunityblog) veitir Microsoft Dynamics-samstarfsaðilum aðgang að tæmandi upplýsingum um nýjungar og vinsæla eiginleika MBS Operations á einum stað.

#### <a name="community-blogs"></a>Samfélagsblogg

- [Það sem þú ættir að vita um fjárhag í Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)


