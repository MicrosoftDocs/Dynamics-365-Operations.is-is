---
title: Kaupa og selja leyfisdaga
description: Þessi grein lýsir því hvernig á að senda inn beiðnir um að kaupa og selja leyfi í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a6d38a69a73ce14f099beb6b6b560bf6c5686b0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875714"
---
# <a name="buy-and-sell-leave"></a>Kaupa og selja leyfisdaga


>[!Important]
>Virknin sem getið er um í þessari grein er eins og er í boði fyrir viðskiptavini á sjálfstætt Dynamics 365 Human Resources. Sum eða öll virknin verður í boði sem hluti af síðari útgáfu í tölvukerfi Finance eftir útgáfu 10.0.26 af Finance.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í Dynamics 365 Human Resources er hægt að leggja fram beiðnir um að kaupa og selja leyfi samkvæmt reglum um kaup og sölur leyfa sem fyrirtækið hefur sett upp.  

## <a name="request-to-buy-leave"></a>Biðja um að kaupa leyfi

1. Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns** skal velja **Beiðni um kaup á leyfisdögum** í reitnum **Frídagastaða**. 

2. Bætið við **Leyfisgerð** og sláið inn **Upphæð** fyrir leyfisupphæð sem á að kaupa. 

3. Veldu **Sendu inn** þegar þú ert tilbúinn að leggja fram beiðni þína. 

Stöðurnar verða annaðhvort uppfærðar sjálfkrafa eða fara í gegnum samþykktarferli áður en uppfærsla fer fram. Þetta veltur á því hvernig kaupreglan hefur verið skilgreind.

## <a name="request-to-sell-leave"></a>Beiðni um að selja leyfi

1. Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns** skal velja **Beiðni um að selja leyfisdaga** í reitnum **Frídagastaða**. 

2. Bætið við **Leyfisgerð** og sláið inn **Upphæð** fyrir leyfisupphæð sem á að selja. 

3. Veldu **Sendu inn** þegar þú ert tilbúinn að leggja fram beiðni þína.

Stöðurnar verða annaðhvort uppfærðar sjálfkrafa eða fara í gegnum samþykktarferli áður en uppfærsla fer fram. Þetta veltur á því hvernig kaupreglan hefur verið skilgreind.


## <a name="troubleshooting"></a>Úrræðaleit 

Ef ósk um kaup eða sölu á leyfi mistekst munu notendur með réttindin **EssLeaveBuySellRequestApprover** geta farið yfir skilaboðakladdann fyrir allar óskir um kaup og sölu á leyfum. Þetta er gert með því að fara í **Leyfi og fjarvistir > Tenglar > Beiðnir um kaup og sölu á leyfi > Skilaboðakladdi** (efst til vinstri). **Skilaboðakladdinn** sýnir notendum hvernig unnið var úr færslunum og tengdri verkflæðissögu.


## <a name="see-also"></a>Sjá einnig

[Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)</br>
[Stjórna reglum fyrir kaup og sölu á leyfisdögum](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
