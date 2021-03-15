---
title: Skilgreina vildarkerfi
description: Þessi verklýsing sýnir hvernig á að setja upp vildarkerfi með tveimur vildarlög.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a853287c0795057b09c429ea1c9ad5231e39a33
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972306"
---
# <a name="define-loyalty-programs"></a>Skilgreina vildarkerfi

[!include [banner](../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp vildarkerfi með tveimur vildarlög. Þessi aðferð notar USRT sýnigögn fyrirtækisins.

1. Fara í Retail og Commerce > .. > Vildarkerfi.
2. Smellið á Nýtt.
3. Í reitinn Heiti skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Smella á bæta Við línu.
6. Í reitinn Stig skal slá inn númer.
7. Færið inn heiti fyrir í vildarlag í svæðinu Lag.
8. Í reitinn Lýsing skal slá inn gildi.
9. Í reitnum dagsetningabil skal smella á fellilistahnappinn til að opna leitina.
    * dagsetningabili ætti að ná inn í framtíðina. Til dæmis, ef dagsetningabil sem er valið fyrir fulllag er eins árs tímabil, getur hvaða viðskiptavinur sem uppfyllir skilyrði fyrir gulllag getur fengið umbun sem eru úthluta í the gulllag fyrir eitt ár. Ef viðskiptavinurinn verður aftur hæfur fyrir gull stig lags meðan þær eru í því lagi, verður dagsetningin þegar lagið þeirra rennur út framlengt um annað ár, frá þeim degi þegar þeir verða aftur hæfir.  
10. Í listanum skal smella á tengilinn í valinni línu.
11. Smellið á „Bæta við línu“.
12. Í reitinn Stig skal slá inn númer.
13. Færið inn heiti fyrir í vildarlag í svæðinu Lag.
14. Í reitinn Lýsing skal slá inn gildi.
15. Í reitnum dagsetningabil skal smella á fellilistahnappinn til að opna leitina.
16. Í listanum skal smella á tengilinn í valinni línu.
17. Smellið á „Vista“.
18. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Reglur vildarlags skilgreina lágmarksfjöldi sem þarf að vera unnið inn á tímabili til að geta fengið vildarpunktur lags.  
19. Víxla útvíkkun á liðnum reglur lags.
20. Smellið á „Nýtt“.
    * Hægt er að hafa fleiri en eitt lag reglu hvert lag. Til dæmis gæti verið þrjár skilyrði til að laga; aukakort eftir eyðsluþök $500 í einn mánuð með eyðsluþök einu ári á 1000 usd og hafi 20 færslur í einu ári á eftir. Ef Þetta er gert yrði þarf að stofna þrjá vildarlags.  
21. Í reitnum vildarpunktar skal smella á fellilistahnappinn til að opna leitina.
    * Þetta ætti að vera ekki innleysanlegur vildarpunktur.  
22. Í listanum skal smella á tengilinn í valinni línu.
23. Færið inn tölu í svæðinu Lágmarksfjöldi útgefinna punkta.
    * Fyrir lægsta stig lags ef allir viðskiptavinir eru gildir einfaldlega með því að taka þátt í áætluninni, færa inn '0'.  
24. Í reitnum Dagsetningabil endurmats skal smella á fellilistahnappinn til að opna leitina.
    * Þessu dagsetningabili ætti að ná inn í fortíðina. Aðeins stig sem fengin á þessu dagsetningabili einungis verða talin upp gildið fyrir lágmarks útgefnir punktar .  
25. Í listanum skal smella á tengilinn í valinni línu.
26. Smellið á „Vista“.
27. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
28. Smellt er á Nýtt.
29. Í reitnum vildarpunktar skal smella á fellilistahnappinn til að opna leitina.
30. Í listanum skal smella á tengilinn í valinni línu.
31. Færið inn tölu í svæðinu Lágmarksfjöldi útgefinna punkta.
32. Í reitnum Dagsetningabil endurmats skal smella á fellilistahnappinn til að opna leitina.
    * Þessu dagsetningabili ætti að ná inn í fortíðina.  
33. Í listanum skal smella á tengilinn í valinni línu.
34. Smellið á „Vista“.
35. Smellt er á verðflokkur.
    * Ef óskað er að veita vildarviðskiptavini afslætti . Þú þarft að úthluta eina eða fleiri verðflokkum fyrir vildarkerfi og úthluta verðflokkum á afslætti. Góðir starfshættir eru að blanda ekki verðflokkum yfir mismunandi gerðir af afsláttareiningum.  Til dæmis ekki nota sömu verðflokk fyrir afslátt vildarkorts og afslátt rásar.  
36. Í reitnum verðflokkur skal smella á fellilistahnappinn til að opna leitina.
    * Verðflokkatengill flokka efst á síðunni er fyrir vildarkerfi. Verðflokkatengillinn í lögum forrits hjá flýtiflipanum er aðeins fyrir tiltekið vildarlag.  
37. Í listanum skal smella á tengilinn í valinni línu.
38. Smellið á „Vista“.
39. Lokið síðunni.
40. Smellið á „Vista“.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]