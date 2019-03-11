---
title: Innsýn í greiðslu viðskiptavinar (forútgáfa)
description: Þetta efnisatriði fjallar um það hvernig innsýn í greiðslu viðskiptavinar getur auðveldað að spá fyrir um hvenær reikningur verður greiddur og auðveldað fyrirtækjum að búa til fínstilltar aðferðir sem auka líkurnar á því að greitt sé á réttum tíma.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "344663"
---
# <a name="customer-payment-insights-preview"></a>Innsýn í greiðslu viðskiptavinar (forútgáfa)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Þessi eiginleiki er hluti af markútgáfu og er aðeins í boði fyrir notendur sem hafa valið að taka þátt í einkaforútgáfu. Þessi eiginleiki verður innifalinn í almennri útgáfu sem er væntanleg.

# <a name="overview"></a>Yfirlit

Fyrirtækjum finnst oft krefjandi að spá fyrir um hvenær viðskiptavinur greiðir reikninga sína. Þessi skortur á innsýn getur leitt til ónákvæmra sjóðstreymisspáa, óhagkvæmra innheimtuferla og möguleika á því að pantanir verði afgreiddar viðskiptavinum sem kunna að fela í sér lánsáhættu. Innsýn í greiðslu viðskiptavinar (forútgáfa) notar vélnám til að spá fyrir um hvenær reikningur verður greiddur. Hún veitir einnig fínstilltar aðferðir sem hægt er að stilla til að hámarka líkurnar á því að viðskiptavinir greiði á réttum tíma.

## <a name="predictions"></a>Spár

Greiðsluspár leyfa fyrirtækjum að bæta viðskiptaferla sína með því að auðvelda það að:

-   Bera auðveldlega kennsl á reikninga sem spáð er að verði greiddir seint.
-   Gera viðeigandi ráðstafanir til að bæta líkurnar á að fá greitt á réttum tíma.

Innsýn í greiðslu viðskiptavinar (forútgáfa) notar vélnám til að spá fyrir um hvenær reikningur verður greiddur. Innsýnin notar eldri gögn reikninga, greiðslna og viðskiptavina til að búa til vélnámslíkan sem er notað til að spá fyrir um hvenær reikningur verður greiddur.

Fyrir hvern opinn reikning spáir innsýn í greiðslu viðskiptavinar (forútgáfa) fyrir um þrjá greiðslumöguleika:

-  Líkur á að greiðsla sé á réttum tíma (innan gjalddaga reiknings).
-  Líkur á að greiðsla sé greidd innan 30 daga frá gjalddaga reiknings.
-  Líkur á að greiðsla sé greidd seinna en 30 dögum frá gjalddaga reiknings.

Líkurnar á greiðslu er hægt er að skoða í spáhlutanum.

[![Greiðsluspár](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Hverjum reikningi er einnig úthlutað bestu líkum á greiðslu með því að nota eina af atburðarásunum þremur um greiðsluspárlíkur skilgreindar hér að ofan. Atburðarásin með hæstu líkum á greiðslu er atburðarás sem stendur upp úr.


Gefum okkur sem dæmi að spá fyrir reikning gefur 71% líkur á að hann verði greiddur á réttum tíma, 13% líkur á að hann verði greiddur innan 30 daga frá gjalddaga og 16% líkur á að hann verði greiddur seinna en 30 dögum frá gjalddaga. Bestu líkurnar sýna að reikningurinn verði í atburðarás fyrir greiðslu á réttum tíma, þannig að reikningurinn verði merktur með líkum á því að hann verði greiddur á réttum tíma.

[![Greiðsluspár](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Fínstillingaraðferðir

Ásamt greiðsluspám getur innsýn í greiðslu viðskiptavinar (forútgáfa) notað fínstillingaraðferðir til að bæta líkurnar á því að fá greitt á réttum tíma. Þetta gerir fyrirtækjum kleift að gera „Hvað ef“ greiningu með því að leyfa notendum að stilla færibreytur reikninga og viðskiptavina og svo bera saman samsvarandi áhrif á líkurnar á því að fá greiðslu á reikningum á réttum tíma.

Fyrirtæki gæti til dæmis viljað meta áhrifin sem uppfærsla á staðgreiðsluafslætti á reikningum hefur á líkurnar á því að fá greiðsluna á réttum tíma. Þegar reikningar eru fínstilltir til að nota nýja afsláttinn, geta notendur farið yfir áhrifin við að nota afslættina hefur á líkurnar á því að fá greiðslur fyrir þessa reikninga á réttum tíma. Ef kostnaðurinn við að nota afsláttinn er hverfandi í samanburði við ávinning þess að innheimta greiðsluna á réttum tíma, kann fyrirtækið að velja að nota valinn afslátt fyrir allar opnar pantanir í framtíðinni.

> [!NOTE] 
> Eins og staðan er nú er afsláttur aðeins í boði sem fínstillingaraðferð fyrir innsýn í greiðslu viðskiptavinar (forútgáfa).

[![Fínstilltar spár](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Hvernig skal nálgast innsýn í greiðslu viðskiptavinar (forútgáfa)

Ef þú hefur áhuga á að prófa innsýn í greiðslu viðskiptavinar (forútgáfa) skaltu senda tölvupóst til [Hópur forútgáfu á fjármálainnsýn](mailto:fiap@microsoft.com). 

## <a name="privacy-statement"></a>Yfirlýsing um persónuvernd

Forútgáfur geyma gögn viðskiptavinar í Bandaríkjunum. Að auki, forútgáfur (1) geta mögulega notað eki eins miklar persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 for Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.
