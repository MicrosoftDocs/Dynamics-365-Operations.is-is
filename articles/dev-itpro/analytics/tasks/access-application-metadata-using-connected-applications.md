---
title: Aðgangur að lýsigögnum forrits með tengdum forritum
description: Skrefin í þessu efni útskýra hvernig notandi Regulatory Configuration Service (RCS) getur sett upp nýja líkanavörpun rafrænnar skýrslugerðar með notkun á lýsigögnunum í Finance and Operations
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d3581f6ae2d91b9648da3ba69e6b1d36cd08196
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727053"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Aðgangur að lýsigögnum forrits með tengdum forritum

[!include [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi Regulatory Configuration Service í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur sett upp nýja líkanavörpun rafrænnar skýrslugerðar með því að nota lýsigögnin í Dynamics 365 for Finance and Operations. Lýsigögn hugbúnaðar verða skoðuð á netinu með því að nota RCS -tengda forritið. Dæmi um líkanavörpun rafrænnar skýrslugerðar verður skilgreint til að fá aðgang að utanríkisviðskiptafærslum. Til að ljúka þessum skrefum verður fyrst að ljúka skrefunum í efninu [Stofna skilgreiningaveitu og merkja hana sem virka](er-configuration-provider-mark-it-active-2016-11.md) í RCS. Ef þú hefur ekki lokið við skrefin í efninu [Fáðu aðgang að lýsigögnum hugbúnaðar með notkun á grunnstillingum rafrænnar skýrslugerðar](access-application-metadata-er-configuration.md), skaltu fara í [Síðu með dæmum um rafræna skýrslugerð](https://go.microsoft.com/fwlink/?linkid=862266) til að sækja og vista eftirfarandi skilgreiningar rafrænnar skýrslugerðar: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, og ljúka síðan við skrefin í ferlinu.

## <a name="prerequisites"></a>Forkröfur
1. Farðu í **Öll vinnusvæði** > **Rafræn skýrslugerð**. 
2. Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**. Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitu og merkja hana sem virka](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="get-required-er-configurations"></a>Sækja umbeðnar ER-skilgreiningar
1. Smellið á **Skilgreiningar skýrslugerðar**. 
2. Ef þú hefur þegar lokið við skrefin í ferlinu [(RCS) Fá aðgang að lýsigögnum hugbúnaðar með notkun á grunnstillingum rafrænnar skýrslugerðar](access-application-metadata-er-configuration.md) hefurðu nú þegar allar nauðsynlegar skilgreiningar rafrænnar skýrslugerðar (skilgreiningar lýsigagna utanríkisviðskipta, líkans og vörpunar) í gildandi RCS-tilviki. Þú getur sleppt öllum eftirstandandi skrefum í þessu undirverkefni. 
3. Smelltu á **Skipta út**. 
4. Smelltu á **Hlaða úr XML-skrá**. 
5. Smelltu á **Skoða** og veldu skrána **Foreign trade metadata.xml**. 
6. Smellt er á **OK**. 
7. Smelltu á **Skipta út**. 
8. Smelltu á **Hlaða úr XML-skrá**. 
9. Smelltu á **Skoða** og veldu skrána **Foreign trade model.xml**. 
10. Smellt er á **OK**. 
11. Smelltu á **Skipta út**. 
12. Smelltu á **Hlaða úr XML-skrá**. 
13. Smelltu á **Skoða** og veldu skrána **Foreign trade mapping.xml**. 
14. Smellt er á **OK**. 

## <a name="register-connected-dynamics-365-for-finance-and-operations-application"></a>Skráðu tengdan hugbúnað Dynamics 365 for Finance and Operations
1. Lokið síðunni. 
2. Lokið síðunni. 
3. Farðu í **Öll vinnusvæði** > **Rafræn skýrslugerð**. 
4. Smelltu á **Tengd forrit**. 
5. Gakktu úr skugga um að skilgreint forrit sé byggt á Azura og aðgengilegt fyrir núverandi notanda RCS. Þess er einnig krafist að núverandi notandi RCS hafi aðgang að völdu forriti og hafi verið skráður sem notandi þessara forrits, sem gegnir hlutverki í að gefa honum réttindi til að fá aðgang að lýsigögnum forritsins. 
6. Smellt er á **Nýtt**. 
7. Í reitinn **Heiti** slærðu inn „MyConnectedApp“. 
8. Í reitinn **Forrit** slærðu inn „https:// mycompany.operations.dynamics.com“. 
9. Í reitinn **Leigjandi** „slærðu inn mycompany.onmicrosoft.com“. 
10. Smellt er á **Vista**. 
11. Þegar þú skoðar tengingu við skilgreint forrit skaltu á síðunni **Tengja við ytra forrit** smella á tengilinn **Smellta hér til að tengja við valið ytra forrit**. 
12. Smelltu á **Athuga tengingu**. 
13. Smellið á **Loka**. 
14. Þegar tengingarvottun hefur tekist verða upplýsingar um útgáfu og leigjendur uppfærðar fyrir skilgreind forrit í núverandi hnitaneti. 

## <a name="review-existing-model-mapping-configuration"></a>Yfirfara fyrirliggjandi skilgreiningu fyrir líkanavörpun
1. Lokið síðunni. 
2. Smellið á **Skilgreiningar skýrslugerðar**. 
3. Í trénu útvíkkarðu **Líkan utanríkisverslunar**. 
4. Í trénu skaltu velja **Líkan utanríkisviðskipta\Vörpun utanríkisviðskipta**. 
5. Stækkaðu hlutann **Skilyrði**. 

> [!NOTE]
> Eins og er vísar þessi vörpun í skilgreiningu lýsigagna. Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan verið er að setja þessa líkanavörpun upp. 

6. Smellið á **Hönnuður**. 
7. Smellið á **Hönnuður**. 
8. Í trénu velurðu **Dynamics 365 for Operations\Töflufærslur**. 
9. Smelltu á **Bæta rót við**. 
10. Sláið inn eða veldu gildi í reitnum **Tafla**. 

> [!NOTE]
> Eins og er vísar þessi vörpun í skilgreiningu lýsigagna. Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan verið er að setja þessa líkanavörpun upp. 

11. Smelltu á **Hætta við**. 
12. Lokið síðunni. 
13. Lokið síðunni. 

## <a name="assign-connected-application-to-model-mapping"></a>Úthluta tengdu forriti á líkanavörpun 
1. Smellið á **Breyta**. 
2. Veldu forritið **MyConnectedApp**. 

> [!NOTE]
> Eins og er, vísar þessi vörpun í lýsigögn valins tengds forrits. Þegar sama vöpun vísar í lýsigagnaskilgreiningu um leið og tengt forrit verða lýsigögn tengds forrits notuð. 

3. Smellið á **Hönnuður**. 
4. Smellið á **Hönnuður**. 
5. Í trénu velurðu **Dynamics 365 for Operations\Töflufærslur**. 
6. Smelltu á **Bæta rót við**. 
7. Sláið inn eða veldu gildi í reitnum **Tafla**. 

> [!NOTE]
> Fleiri en tvær forritstöflur voru boðnar núna þar sem þessi vörpun notar öll lýsigögn tengds forrits sem hefur verið úthlutað fyrir það. 

8. Smelltu á **Hætta við**. 
9. Smelltu á **Villuleita**. 

> [!NOTE]
> Okkur tókst að binda þætti gagnalíkans við atriði gagnagjafa sem er lýst með því að nota upplýsingar um lýsigögn forrits úr tengdu forriti sem hefue verið úthlutað fyrir þessa vörpun. 

10. Lokið síðunni. 
11. Lokið síðunni. 

Þegar þú þarft að meta þessa líkanavörpun með því að nota lýsigögn annarrar útgáfu forrits skaltu skrá annað tengt forrit, úthluta því á þessara líkanavörpun og sannprófa það gegn nýjum lýsigögnum.