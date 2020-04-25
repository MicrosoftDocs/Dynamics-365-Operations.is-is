---
title: 'Skilgreina reglulega talningu '
description: Reglulega talningu er vöruhúsið ferli sem hægt er að nota til að endurskoða vörur á lager.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d10904414b8c35960e421caeb7cae838edd312dd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217058"
---
# <a name="define-cycle-counting"></a>Skilgreina reglulega talningu  

[!include [banner](../../includes/banner.md)]

Reglulega talningu er vöruhúsið ferli sem hægt er að nota til að endurskoða vörur á lager. Þetta verk sýnir hvernig á að: setja upp sjálfgefinn verkforgang talningar; virkja valmyndaratriði fartækis til að keyra bæði tínslu- og talningaraðgerðir; virkja kveikju þröskulds talningar þegar staðsetning tæmist; virkja áætlun um reglulega talningu fyrir tiltekna vöru innan tiltekins vöruhúss. Þessi verk eru yfirleitt unnin af stjórnanda vöruhúss. Hægt er að fara í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða þín eigin gögn.


## <a name="set-the-priority-of-counting-work"></a>Stilla forgang talningar
1. Í **Skoðunarrúðunni** ferðu í **Kerfi > Vöruhúsakerfi > Uppsetning > Vöruhús > Færibreytur vöruhúsakerfis**.
2. Smelltu á flipann **Regluleg talning**.
3. Í reitinn **Sjálfgefinn forgangur verkforgangs reglulegrar talningar** skal færa inn tölu. Þetta skref mun breyta forgangi reglulegrar talningarvinnu samanborið við aðrar gerðir vinnu í vöruhúsi. Ef þú setur inn lægri tölu fyrir reglulega talningu en fyrir aðrar gerðir vinnu hækkar það forgang vinnu reglulegrar talningar.  
4. Smellt er á **Vista**.
5. Lokið síðunni.

## <a name="enable-the-mobile-device"></a>Virkja fartækið
1. Í **Skoðunarrúðunni** ferðu í **Einingar > Vöruhúsakerfi > Uppsetning > Fartæki > Valmyndaratriði fartækis**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Heiti valmyndaratriðis** skal færa inn gildi.
4. Í reitinn **Titill** skal slá inn gildi.
5. Í reitnum **Stilling** velurðu „Vinna“.
6. Stilltu valkostinn **Nota fyrirliggjandi vinnu** á Já. Þegar þessi valkostur er settur á Já leitar kerfið að fyrirliggjandi vinnu þegar valmyndaratriði fartækis er notað.  
7. Í reitnum **Stýrt af** velurðu 'Stýrt af Kerfi'. Þegar „Stýrt af kerfi“ er valið, verður vöruhúsastarfsmanni stýrt í átt að opinni vinnu sem er í skilgreindum vinnuklösum. (Við munum stofna þessa vinnuklasa næst.)  
8. Útvíkkaðu flýtiflipann **Vinnuklasar**. Næst munum við stofna tvo vinnuklasa sem verða notaðir með þessu valmyndaratriði fartækis. Þegar valmyndaratriðið er notað, verður sett fram fyrirspurn um þessa vinnuklasa, og vinnan sem er efst í forgangsröðinni verður sýnd notandanum.  
9. Smellt er á **Nýtt**.
10. Í reitnum **Kenni vinnuklasa** skal velja gildi.
11. Smellt er á **Nýtt**.
12. Í reitnum **Kenni vinnuklasa** skal velja gildi.
13. Í **Aðgerðasvæðinu** smellirðu á **Vista**.
14. Lokið síðunni.
15. Í **Skoðunarrúðunni** ferðu í **Einingar > Vöruhúsakerfi > Uppsetning > Fartæki > Valmyndaratriði fartækis**.
16. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
17. Í trénu, skal velja þau valmyndaratriði sem þú varst að stofna.
18. Smellið á **Breyta**.
19. Smellt er á örina til að bæta við valmyndaratriði við valmyndina.
20. Smellt er á **Vista**.

## <a name="create-a-counting-threshold"></a>Stofna þröskuld fyrir talningu
1. Í **Skoðunarrúðunni** ferði í **Einingar > Vöruhúsakerfi > Uppsetning > Regluleg talning > Þröskuldar fyrir reglulega talningu**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Auðkenni þröskulds fyrir reglulega talningu** skal færa inn gildi.
4. Stilltu valkostinn **Vinna reglulegrar talningar strax** á Já.
5. Í reitinn **Lýsing** skal slá inn gildi.
6. Smellt er á **Vista**.
7. Smelltu á **Velja staðsetningar**.
8. Í listanum skal merkja valda línu.
9. Veldu gildi í reitnum **Skilyrði**.
10. Smellt er á **OK**.
11. Lokið síðunni.

## <a name="create-a-cycle-count-plan"></a>Stofna áætlun um reglulega talningu
1. Í **Skoðunarrúðunni** ferðu í **Einingar > Vöruhúsakerfi > Uppsetning > Regluleg talning > Áætlanir um reglulega talningu**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Auðkenni fyrir áætlun um reglulega talningu** skal færa inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitnum **Hámarksfjöldi reglulegrar talningar** skal færa inn tölu.
6. Smellt er á **Vista**.
7. Smelltu á **Velja staðsetningar**.
8. Í listanum skal merkja valda línu.
9. Veldu gildi í reitnum **Skilyrði**.
10. Smellt er á **OK**.
11. Í reitinn **Dagar á milli reglulegrar talninga** skal færa inn tölu. Til dæmis ef gildið sem er skilgreint í **Dagar á milli reglulegrar talninga** er 5 verður vinna reglulegrar talningar stofnuð á fimm daga fresti. Hins vegar ef unnið er úr vinnu reglulegrar talningar á degi Þrír mun næsta reglulega talning stofnast fimm dögum eftir að síðasta reglulega talning var unnin, á degi 8.  
12. Smellt er á **Vista**.
13. Smellt er á **Nýtt**.
14. Í reitinn **Raðnúmer** skal slá inn númer. Röðunin er frá lægsta númerinu til hæsta númersins. Gildið verður að vera meira en 0 (núll).  
15. Í listanum skal merkja valda línu.
16. Í reitinn **Lýsing** skal slá inn gildi.
17. Smellt er á **Vista**.
18. Smelltu á fyrirspurnina **Skilgreina afurð**.
19. Í listanum skal merkja valda línu.
20. Í reitinn **Skilyrði** skal slá inn eða velja gildi.
21. Smellt er á **OK**.
22. Lokið síðunni.

