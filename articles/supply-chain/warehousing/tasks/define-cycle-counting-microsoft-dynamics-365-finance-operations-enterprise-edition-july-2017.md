---
title: 'Skilgreina reglulega talningu '
description: Reglulega talningu er vöruhúsið ferli sem hægt er að nota til að endurskoða vörur á lager.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2832547f81b0153d42ac4664184f18bd66f1acdd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "337303"
---
# <a name="define-cycle-counting"></a>Skilgreina reglulega talningu  

[!include [task guide banner](../../includes/task-guide-banner.md)]

Reglulega talningu er vöruhúsið ferli sem hægt er að nota til að endurskoða vörur á lager. Þetta verk sýnir hvernig á að: setja upp sjálfgefinn verkforgang talningar; virkja valmyndaratriði fartækis til að keyra bæði tínslu- og talningaraðgerðir; virkja kveikju þröskulds talningar þegar staðsetning tæmist; virkja áætlun um reglulega talningu fyrir tiltekna vöru innan tiltekins vöruhúss. Þessi verk eru yfirleitt unnin af stjórnanda vöruhúss. Hægt er að fara í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða þín eigin gögn.


## <a name="set-the-priority-of-counting-work"></a>Stilla forgang talningar
1. Fara í vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis.
2. Smellt er á flipann Regluleg talningu.
3. Í reitnum Sjálfgefinn forgangur verkforgangs reglulegrar talningar skal færa inn tölu.
    * Þetta skref mun breyta forgangi reglulegrar talningarvinnu samanborið við aðrar gerðir vinnu í vöruhúsi. Ef þú setur inn lægri tölu fyrir reglulega talningu en fyrir aðrar gerðir vinnu hækkar það forgang vinnu reglulegrar talningar.  
4. Smellið á „Vista“.
5. Lokið síðunni.

## <a name="enable-the-mobile-device"></a>Virkja fartækið
1. Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmyndaratriði fartækis
2. Smellið á „Nýtt“.
3. Í svæðið heiti valmyndaratriðis, færa inn gildi.
4. Í reitinn Titill skal slá inn gildi.
5. Í reitnum Stilling velurðu „Vinna“.
6. Stilltu valkostinn Nota fyrirliggjandi verk á Já.
    * Þegar þessi valkostur er settur á Já leitar kerfið að fyrirliggjandi vinnu þegar valmyndaratriði fartækis er notað.  
7. Í reitnum Stýrt af velurðu 'Stýrt af Kerfi'.
    * Þegar „Stýrt af kerfi“ er valið, verður vöruhúsastarfsmanni stýrt í átt að opinni vinnu sem er í skilgreindum vinnuklösum. (Við munum stofna þessa vinnuklasa næst.)  
8. Stækka eða fella saman hlutann vinnuklasar.
    * Næst munum við stofna tvo vinnuklasa sem verða notaðir með þessu valmyndaratriði fartækis. Þegar valmyndaratriðið er notað, verður sett fram fyrirspurn um þessa vinnuklasa, og vinnan sem er efst í forgangsröðinni verður sýnd notandanum.  
9. Smellið á „Nýtt“.
10. Í reitnum Kenni vinnuklasa skal velja gildi.
11. Smellið á „Nýtt“.
12. Í reitnum Kenni vinnuklasa skal velja gildi.
13. Smellið á „Vista“.
14. Lokið síðunni.
15. Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmynd fartækis
16. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
17. Í trénu, skal velja þau valmyndaratriði sem þú varst að stofna.
18. Smellið á „Breyta“.
19. Smellt er á örina til að bæta við valmyndaratriði við valmyndina.
20. Smellið á „Vista“.

## <a name="create-a-counting-threshold"></a>Stofna þröskuld fyrir talningu
1. Fara í vöruhúsakerfi > Uppsetning >Reglulega talningu > Þröskulda fyrir reglulega talningu.
2. Smellið á „Nýtt“.
3. Í reitnum Auðkenni þröskulds fyrir reglulega talningu skal færa inn gildi.
4. Stilltu valkostinn Vinna reglulegrar talningar strax á Já.
5. Sláið inn gildi í reitnum „Lýsing“.
6. Smelltu á Vista.
7. Smellt er á Velja staðsetningar.
8. Í listanum skal merkja valda línu.
9. Veljið gildi í reitnum Skilyrði.
10. Smellið á „Í lagi“.
11. Lokið síðunni.

## <a name="create-a-cycle-count-plan"></a>Stofna áætlun um reglulega talningu
1. Fara í vöruhúsakerfi > Uppsetning > Reglulega talningu > Áætlanir um reglulega talningu.
2. Smellið á „Nýtt“.
3. Í reitnum Auðkenni fyrir áætlun um reglulega talningu skal færa inn gildi.
4. Í reitinn Lýsing skal slá inn gildi.
5. Í reitnum Hámarksfjöldi reglulegrar talningar skal færa inn tölu.
6. Smelltu á Vista.
7. Smellt er á Velja staðsetningar.
8. Í listanum skal merkja valda línu.
9. Veljið gildi í reitnum Skilyrði.
10. Smellið á „Í lagi“.
11. Færið inn númer í reitinn Dagar á milli reglulegrar talninga.
    * Til dæmis ef gildið sem er skilgreint í Dagar á milli reglulegrar talninga er 5 verður vinna reglulegrar talningar stofnuð á fimm daga fresti. Hins vegar ef unnið er úr vinnu reglulegrar talningar á degi Þrír mun næsta reglulega talning stofnast fimm dögum eftir að síðasta reglulega talning var unnin, á degi 8.  
12. Smellið á „Vista“.
13. Smellið á „Nýtt“.
14. Í reitinn raðnúmer skal slá inn númer.
    * Röðunin er frá lægsta númerinu til hæsta númersins. Gildið verður að vera meira en 0 (núll).  
15. Í listanum skal merkja valda línu.
16. Sláið inn gildi í reitnum „Lýsing“.
17. Smelltu á Vista.
18. Smella á Skilgreina fyrirspurn um afurð
19. Í listanum skal merkja valda línu.
20. Í reitinn Skilyrði skal slá inn eða veldu gildi.
21. Smellið á „Í lagi“.
22. Lokið síðunni.

