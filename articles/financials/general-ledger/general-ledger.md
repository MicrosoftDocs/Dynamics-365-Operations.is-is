---
title: "Fjárhagur og Fjárhagsleg skýrslugerð heimasíða"
description: "Fjárhagur er notaður til að skilgreina og stjórna fjárhagslegum færslum í lögaðila."
author: twheeloc
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2177110dc16528de7eddedb0667faae553a36b12
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

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

### <a name="whats-new-and-in-development"></a>Nýjungar og eiginleikar á þróunarstigi

Á [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) eru upplýsingar um nýja eiginleika og eiginleika sem eru á þróunarstigi. 

### <a name="blogs"></a>Blogg

Á [Microsoft Dynamics 365-blogginu](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) er að finna umfjöllun, fréttir og aðrar upplýsingar um Viðskiptaskuldir og aðrar hugbúnaðarlausnir.

Hægt er að finna margar færslur um fjárhag á [bloggi afurðarteymis Microsoft Dynamics AX](https://blogs.msdn.microsoft.com/dax/). Þó svo sumar þessara færslna voru skrifaðar um eldri útgáfu fjárhagsins eiga sömu hugtök eiga enn við og ferlin eru svipuð í nýjustu útgáfunni.

[Blogg Microsoft Dynamics Operations-samstarfsaðila](https://community.dynamics.com/partner/b/operationspartnercommunityblog) veitir Microsoft Dynamics-samstarfsaðilum aðgang að tæmandi upplýsingum um nýjungar og vinsæla eiginleika MBS Operations á einum stað.

### <a name="task-guides"></a>Verkleiðbeiningar
Frekari hjálp er í boði sem verkleiðbeiningar í Finance and Operations. Smellið á hnappinn Hjálp á hvaða síðu sem er til að fá aðgang að verkleiðbeiningum.

### <a name="videos"></a>Myndbönd

Kynntu þér kennslumyndbönd sem eru aðgengileg á [YouuTube-rás Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).


