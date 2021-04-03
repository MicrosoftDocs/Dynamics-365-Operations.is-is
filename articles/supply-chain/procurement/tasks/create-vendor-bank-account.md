---
title: Stofna bankareikning lánardrottins
description: Þessi verklýsing sýnir hvernig á að stofna bankareikning fyrir lánardrottinn.
author: RichardLuan
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 425cce178c96097c8aa0a28345d4a9094b7970d9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262190"
---
# <a name="create-a-vendor-bank-account"></a>Stofna bankareikning lánardrottins

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna bankareikning fyrir lánardrottinn. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.

1. Farði í **Skoðunarrúðuna > Kerfiseiningar > Innkaup og aðföng > Lánardrottnar > Allir lánardrottnar**.
2. Veljið lánardrottinn sem á að stofna bankareikning fyrir, og smellið síðan á tengil í reitnum **Kenni lánardrottnalykils**.
3. Á **Aðgerðasvæði** er smellt á **Lánardrottinn**.
4. Smelltu á **Bankareikninga**.
5. Í **aðgerðasvæðinu** er smellt á **Nýtt**.
6. Í reitinn **Bankareikningar** skal slá inn gildi. Þetta Kenni verður notuð til að auðkenna bankareikninginn á lánardrottinsfærslu.  
7. Í reitinn **Heiti** skal slá inn gildi.
8. Í reitnum **Bankaflokkur** skal rita eða velja gildi.
9. Í reitnum **Gerð leiðarnúmer** skal velja valkost. Þetta er gerð leiðarnúmers sem er notuð fyrir alþjóðlegar greiðslur.  
10. Í reitinn **Bankareikningsnúmer** skal slá inn gildi.
11. Í reitinn **SWIFT-kóði** skal rita gildi.
12. Í reitinn **IBAN** skal slá inn gildi.
    - Iban-númeri verður að vera á réttu sniði. Til dæmis er hægt að nota DE89370400440532013000.  
    - Staða bankareikningsins er Virkur ef Virkri dagsetningu hefur verið náð og lokadagur er ekki liðinn. Hún er einnig virk ef reitirnir Virk dagsetning og Gildistími eru auðir. Ef dagsetningarnar í svæðunum Virk dagsetning og Lokadagur eru báðar í framtíðinni er ekki hægt að gera rafrænar greiðslur. Aðrar greiðslugerðir eru mögulegar og bankareikningurinn er virkur.  
13. Útvíkkaðu kaflann **Uppsetning**.
14. Í reitinn **Textakóði** skal rita gildi. Þetta svæði tilgreinir kóða sem mun birtast á bankayfirliti viðtakanda.  
15. Í reitinn **Skilaboð til banka** skal slá inn gildi.
16. Í reitinn **Gengistilvísun** skal rita gildi. Þetta er Tilvísunarnúmer fyrir hvers kyns framvirkt eða fast gengi.
17. Í reitinn **Gjaldmiðill** skal slá inn eða velja gildi. Þegar fyrirframkvittanir eru gefin út, gefur þessa kafla yfirlit yfir stöðu þeirra (í bið eða samþykkt).  
18. Útvíkkaðu kaflann **Aðsetur**.
19. Útvíkkaðu kaflann **Fyrirframkvittanir**.
20. Útvíkkaðu kaflann **Tengslaupplýsingar**.
21. Í reitinn **Símanúmer** skal slá inn gildi.
22. Lokið síðunni.
23. Smellið á **Breyta**.
24. Útvíkkaðu kaflann **Greiðslur**.
25. Í reitnum **Bankareikningur** skal velja lykil sem var nýlega stofnaður.
26. Smellt er á **Vista**. Aðsetrið má erfa frá bankaflokki, ef slíkt er tilgreint, eða hægt er að bæta honum við hér.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]