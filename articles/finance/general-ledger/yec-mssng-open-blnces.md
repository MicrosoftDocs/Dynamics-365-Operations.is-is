---
title: Opnar innistæður vantar í árslokalokun
description: Þetta efnisatriði útskýrir hvers vegna opna stöður kann að vanta þegar þú lokar ári og hvernig á að endurbyggja þær stöður ef þær vantar.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4bebf35a8959d4f72d46d4b40e5487f499b2756d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356653"
---
# <a name="year-end-close-missing-opening-balances"></a>Opnar innistæður vantar í árslokalokun

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvers vegna opna stöður kann að vanta þegar þú lokar ári og hvernig á að endurbyggja þær stöður ef þær vantar.

### <a name="symptom"></a>Einkenni

Hvers vegna eru engar upphafsstöður eftir keyrslu árslokalokun í Fjárhag? 

### <a name="resolution"></a>Lausn

Hér eru nokkur atriði sem skal athuga ef þú hefur lokað ári í Fjárhag og síðan myndað prófjöfnuð sem sýnir ekki opnunarstöður fyrir næsta fjárhagsár.

Ef reiturinn **Afturkalla fyrri lokun** er stilltur á **Já** er verið að afturkalla fyrri árslokalokun fyrir sama fjárhagsár. Þegar keyra á ferli til að bakfæra árslokalokun verður öllum færslum fyrir bæði lokunar- og opnunarstöður eytt rétt eins og árinu hafi aldrei verið lokað. Fylgiskjölunum er einnig eytt. Ferlið fyrir lokun í árslok verður ekki keyrt aftur sjálfkrafa. Hefja þarf ferlið aftur og í þetta skipti uppfæra **Afturkalla fyrri lokun** valkostinn í **Nei**.

Fjallað er um þessar aðstæður í algengum spurningum um árslokalokun. Frekari upplýsingar eru í [Algengar spurningar um verkþætti árslokunar](faq-year-end-activities.md).

### <a name="symptom"></a>Einkenni

Ég keyrði árslokalokun með valkostinn **Afturkalla fyrri lokun** stilltan á **Nei** en er samt sem áður ekki með opnunarstöður fyrir fjárhagsárið mitt.

### <a name="resolution"></a>Lausn

Athugaðu fyrst stöðu runuvinnslunnar. Að loka ári felur í sér fjölda ótengdra verka, en mikilvægasta skrefið er runuverkið með verklýsinguna **Skref 5.0.0**. Opnunarfærslur, og valfrjálsar lokunarfærslur, eru bókaðar í Fjárhag í þessu skrefi. 

[![Sögulisti runu.](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Ef þér tókst að ljúka þessu skrefi en sérð ekki opnunarstöðurnar á síðunni **Fyrirspurn prófjöfnuðar** (**Fjárhagur > Fyrirspurnir og skýrslur > Prófjöfnuður**) skaltu fara yfir niðurstöður runuvinnslu árslokalokunar til að komast að því hvort tekist hafi að ljúka skrefinu Endurbyggja stöður.

[![Niðurstöður runuvinnslu árslokalokunar.](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Ef þetta skref tókst ekki af einhverjum ástæðum, tókst líklega að bóka opnunarfærslurnar (og lokunarfærslurnar ef það var gert). Þú getur gengið úr skugga um að tekist hafi að bóka færslurnar í Fjárhag með því að nota síðuna **Fyrirspurn um fylgiskjalsfærslur** með því að gefa upp fylgiskjalsnúmerið og dagsetninguna sem gefið er upp í svarglugga árslokalokunar fyrir árið sem þú lokaðir (**Fjárhagur > Fyrirspurnir og skýrslur > Færslur fylgiskjals**).

[![Fyrirspurn um fylgiskjalsfærslu.](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Ef fylgiskjöl opnunar (og valfrjálst lokunar) eru til staðar þarftu ekki að keyra árslokalokun á nýjan leik. Í staðinn er vísað í næsta kafla til að fá upplýsingar um hvernig haldið er áfram.

### <a name="symptom"></a>Einkenni

Skrefið „Endurbyggja stöður“ í árslokalokun tókst ekki, þarft ég að keyra allt ferli árslokalokunar aftur?

### <a name="resolution"></a>Lausn

Skrefið Endurbyggja stöður uppfærir stöður í Fjárhag sem eru notaðar þegar fyrirspurn um prófjöfnuð er búin til.  Þetta er lokaskrefið í árslokalokun.  Ef þetta skref er eina skrefið sem mistókst hafa færslur í Fjárhag verið bókaðar.  Þú þarft ekki að loka árinu aftur. Þú getur keyrt ferlið til að endurbyggja stöðurnar á handvirkan hátt með því að nota síðuna **Fjárhagsvíddasamstæður** (**Fjárhagur > Bókhaldslykill > Víddir > Fjárhagsvíddasamstæður**).

[![Hnappurinn Endurbyggja stöður á síðunni Fjárhagsvíddasamstæður.](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Ef það tekur langan tíma að vinna úr þessu skrefi mælum við með því að farið verði yfir bestu starfsvenjur fyrir fjárhagsvíddasamstæður eins og lýst er í [Bestu starfsvenjur fyrir uppfærslu á fjárhagsvíddasamstæðum](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets). 

