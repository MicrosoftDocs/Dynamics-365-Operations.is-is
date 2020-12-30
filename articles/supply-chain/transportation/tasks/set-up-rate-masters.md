---
title: Setja upp sniðmát fyrir taxta
description: Þessi verklýsing sýnir hvernig á að setja upp taxtasniðmát.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cca9fd47a5d8c81d7b8a913d0a467bc113b584
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/29/2020
ms.locfileid: "4430795"
---
# <a name="set-up-rate-masters"></a>Setja upp sniðmát fyrir taxta

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp taxtasniðmát. stjórnandi vörustjórnunar setur yfirleitt upp taxtasniðmát, allt eftir samningum sem voru undirritað með í flutningsaðila. Í þessu tilfelli verður að setja upp taxtasniðmát fyrir flutningsaðila í lofti. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.

## <a name="set-up-break-master"></a>Setja upp sniðmát hlés

1. Fara í **Flutningsstjórnun > Uppsetning >Einkunn > Sniðmát hlés**. Sniðmát hlés eru notuð til að skilgreina uppbyggingu verðlagningar og rofstaði hennar. Uppbygging verðlagningar notar lagskipt verðlagningu sem byggir á efnislegum víddum.  
1. Veljið **Nýtt**.
1. Í reitinn **Sniðmát hlés** skal slá inn gildi.
1. Í reitinn **Heiti** skal slá inn gildi.
1. Veljið gagnagerðina í reitnum **Gagnagerð**.
1. Í svæðinu **Samanburður** skal færa inn tegund samanburðar sem beðið er um (með virknitáknum).
1. Í reitinn **Skipta einingu** skal færa inn skiptieiningu.
1. Í hlutanum **Upplýsingar** skal stofna eins mörg hlé og þörf er á vegna verðlagsuppbyggingar.
1. Veljið **Vista**.

## <a name="set-up-rate-master"></a>Setja upp taxtasniðmát

1. Fara í **Flutningsstjórnun > Uppsetning >Einkunn > Taxtasniðmát**.
1. Veljið **Nýtt**.
1. Í reitinn **Taxtasniðmát** skal færa inn gildi.
1. Í reitinn **Heiti** skal slá inn gildi.
1. Í reitnum **Lýsigagnakenni fyrir taxta** skal velja á fellilistahnappinn til að opna leitina. Lýsigagnakenni fyrir taxta ákvarða gögn sem þarf fyrir taxtasniðmátið, þar sem það skilgreinir lýsigögn sem flutningsstjórnunarvél býst við með þessu taxtasniðmát.  
1. Í þessu dæmi skal velja valkostinn P2P. Þetta er þegar skilgreint í sýnigögnunum.
1. Í listanum skal velja tengilinn í valinni línu.
1. Veljið **Vista**.

## <a name="set-up-rate-base"></a>Setja upp taxtagrunn

1. Veljið **Taxtagrunnur**.
    * Taxtagrunn ákvarðar gengi farmflytjanda og hægt er að nota til að setja upp uppbyggingu taxta þar sem það byggir upp taxta á rofstöðum sem skilgreint í aðalgögnum skila.  
2. Veljið **Nýtt**.
3. Í reitnum **Taxtagrunnur** skal færa inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitnum **Sniðmát hlés** skal velja á fellilistahnappinn til að opna leitina.
    * Sniðmát hlés eru notuð til að skilgreina uppbyggingu verðlagningar og rofstaði hennar. Uppbygging verðlagningar notar lagskipt verðlagningu sem byggir á efnislegum víddum.  
6. Í þessu dæmi notarðu þyngd. Þetta er þegar skilgreint í sýnigögnunum.
7. Í listanum skal velja tengilinn í auðkenndu línunni.
8. Útvíkka hlutann **Upplýsingar**.
9. Veljið **Nýtt**.
10. Í reitnum **Póstnúmer affermingar** frá skal slá inn ‚30301‘.
11. Í reitnum **Póstnúmer affermingar** til skal slá inn ‚30318‘.
12. Í reitnum **Landsvæði affermingar** skal slá inn ‚USA‘.
13. Í reitnum **<1,00** pund ritið '100'.
    * Setja inn taxtann fyrir hvert pund ef heildarþyngd hleðslu er minna en 1 pund.  
14. Í reitnum **<5,00 pund** ritið '300'.
    * Setja inn taxtann fyrir hvert pund ef heildarþyngd hleðslu er minna en 5 pund.  
15. Í reitnum **<20,00** pund ritið '500'.
    * Setja inn taxtann fyrir hvert pund ef heildarþyngd hleðslu er minna en 20 pund.  
16. Í reitnum **<100,00** pund ritið ‚1.000'.
    * Setja inn taxtann fyrir hvert pund ef heildarþyngd hleðslu er minna en 100 pund.  
17. Í reitnum **<1.000,00** pund ritið '3000'.
    * Setja inn taxtann fyrir hvert pund ef heildarþyngd hleðslu er minni en 1.000 pund.  
18. Veljið **Vista**.
19. Lokið síðunni.

## <a name="assign-rate-base"></a>Úthluta taxtagrunn

1. Víkka eða draga saman hlutann **Úthlutanir taxtagrunns**.
2. Veljið **Nýtt**.
    * Hægt er að hafa nokkrar úthlutanir taxtagrunns fyrir hverja taxtasniðmát. Þetta gerir mögulegt að stofna nokkra mismunandi verðpunkta fyrir hvern farmflytjanda eftir áfangastaði, þjónustu eða mismunandi taxtagrunnum. Í þessu ferli verður aðeins að stofna eina úthlutun taxtagrunns.  
3. Í reitinn **Heiti** skal slá inn gildi.
4. Í reitnum **Taxtagrunnur** skal velja á fellilistahnappinn til að opna leitina.
5. Í listanum skal velja tengilinn í auðkenndu línunni.
6. Í reitnum **Þjónusta** skal velja á fellilistahnappinn til að opna leitina.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
8. Í listanum skal velja tengilinn í auðkenndu línunni.
9. Í Svæðið **Póstnúmer** þar sem sótt er, skal færa inn '98052'.
    * Tilgreina hvaða póstnúmer þessa úthlutun taxtagrunns á að gilda frá.
10. Í reitnum **Landsvæði** þar sem sótt er, skal slá inn ‚USA‘.
11. Veljið **Vista**.
