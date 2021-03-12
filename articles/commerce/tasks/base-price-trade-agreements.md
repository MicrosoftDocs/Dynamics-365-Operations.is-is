---
title: Grunnverð og verðsamningar
description: Þetta ferli fer í gegnum stofnun söluverð bundnum við rás viðskiptasamninga.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db3a91807c0cfb51426c03eeaf7785168e6ad0de
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006059"
---
# <a name="base-price-and-trade-agreements"></a>Grunnverð og verðsamningar

[!include [banner](../includes/banner.md)]

Þetta ferli fer í gegnum stofnun söluverð bundnum við rás viðskiptasamninga. Þessi aðferð notar USRT sýnigögn fyrirtækisins.

1. Í **Skoðunarrúðu** ferðu í **Einingar > Retail og Commerce > Verðlagning og afsláttarstjórnun > Verðflokkar > Allir verðflokkar**. Verðflokkar eru hvernig verðsamninga er úthlutað á tiltekinn rásir. Notkun verðflokka til að tengja viðskiptasamninga við rás gerir virkjar verðlagningu eftir rásum.  
2. Smellt er á **Nýtt**.
3. Í reitinn **Verðflokkar** skal slá inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Smellt er á **Vista**.
6. Lokið síðunni.
7. Í **Skoðunarrúðunni** ferðu í **Einingar > Retail og Commerce > Rásir > Verslanir > Allar smásöluverslanir**.
8. Á listanum, veljið 'New York'
9. Í aðgerðasvæðinu er smellt á **Verslun**.
10. Smelltu á **Verðflokka**.
11. Smellt er á **Nýtt**.
12. Í reitnum **Verðflokkar** skal smella á fellilistahnappinn til að opna leitina.
13. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
14. Smellt er á **Vista**.
15. Lokið síðunni.
16. Lokið síðunni.
17. Í **Skoðunarrúðunni** ferðu í **Einingar > Retail og Commerce > Afurðir og flokkar > Losaðar afurðir eftir flokki**.
18. Í listanum skal smella á tengilinn í valinni línu.
19. Smellið á **Breyta**.
20. Útvíkkaðu flýtiflipann **Selja**.
21. Í reitinn **Verð** skal slá inn tölu. Þetta verð er notaður ef engin viðeigandi verðsamningar fundust.  
22. Smellt er á **Vista**.
23. Í **Aðgerðasvæðinu** smellirðu á **Selja**.
24. Smelltu á **Stofna verðsamninga**.
25. Smellt er á **Nýtt**.
26. Í reitnum **Heiti** skal smella á fellilistahnappinn til að opna leitina.
27. Í listanum skal **Commerce**. Færslubókarheitið **Commerce** er notað í sýnigögnum sem sjálfgefin tengsl við **Verð (sala)**. Þetta þýðir að allar nýjar línur sem stofnaðar eru verða sjálfgefnar fyrir söluverð viðskiptasamninga.  
28. Í **Aðgerðasvæðinu**, smellirðu á **Línur**.
29. Í reitnum **Gerð aðilakóða** er valinn „Flokkur“.
30. Í reitnum **Val á lykli** skal smella á fellilistahnappinn til að opna uppflettinguna.
31. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Þetta Ljúka við tengil úr Rásar til vöruverðs til viðskiptasamningi.  
32. Í reitinn **Vöruvensl** skal slá inn gildi.
33. Í reitnum **Upphæð í gjaldmiðli** skal færa inn tölu.
34. Á flýtiflipanum **Upplýsingar** skaltu haka eða afhaka við gátreitinn **Finna næstu**. Þegar **Finna næsta** hefur verið stillt á 'Já' mun verðlagningarvélin halda áfram að leita að viðeigandi verðsamningum með lægra söluverði. Þegar **Finna næsta** hefur verið stillt á 'Nei' stöðvar verðvélin leit og notar verðsamninginn.  
35. Smelltu á **bóka.**
36. Smellt er á **OK**.
37. Lokið síðunni.
38. Í **Aðgerðasvæðinu** smellirðu á Selja.
39. Smelltu á **Söluverð**.

