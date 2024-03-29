---
title: Viðburðir vöruhúsaforrits
description: Þessi grein lýsir úrvinnslu á viðburðum vöruhúsaforrits sem notaðir eru til að vinna úr skilaboðum um viðburð vöruhúsaforrits sem hluti af runuvinnslu.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2dc24fed1ec71432d9e2a3e1cb5b366267c2938b
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218743"
---
# <a name="warehouse-app-event-processing"></a>Vinnsla viðburða í vöruhúsaforriti

[!include [banner](../includes/banner.md)]

Runuvinnslur sem keyra í Supply Chain Management geta notað gögn úr þessari biðröð til að vinna úr viðburðum sem farsímaforrit vöruhúsakerfis gefur út til að bregðast við tilkynntum viðburðum eftir því sem þörf krefur. Þessi eiginleiki bætir viðeigandi viðburðum við biðröðina sem svar við tilteknum gerðum aðgerða sem starfsmenn sem nota forritið grípa til. Dæmi er þegar verið er að nota eiginleikann *Stofna og vinna úr flutningspöntunum úr vöruhúsaforriti*, verða haus og línur flutningspöntunar stofnaðar og uppfærðar í bakvinnslunni þegar kerfið keyrir runuvinnsluna **Vinna úr viðburðum vöruhúsaforrits**.

## <a name="turn-the-process-warehouse-app-events-feature-on-or-off"></a>Kveikja eða slökkva á eiginleikanum „Vinna úr viðburðum vöruhúsaforrits“

Sem hluti af Supply Chain Management, útgáfa 10.0.25, er sjálfgefið kveikt á þessum eiginleika. Sem hluti af Supply Chain Management, útgáfa 10.0.29, er þessi eiginleiki áskilinn. Því er sjálfgefið að kveikt sé á henni og ekki er hægt að slökkva á henni aftur. Ef þú ert að keyra útgáfu sem er eldri en 10.0.29 geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Vinna úr viðburðum vöruhúsaforrits* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Setja upp runuvinnslu til að vinna úr viðburðum vöruhúsaforrits

### <a name="process-warehouse-app-events"></a>Vinna úr viðburðum vöruhúsaforrits

Setjið upp áætlaða runuvinnslu til að vinna úr viðburðum í vöruhúsaforriti fyrir stofnun flutningspöntunar og línuuppfærslur.

1. Farið í **Vöruhúsakerfi \> Reglubundin verk \> Vinna úr viðburðum vöruhúsaforrits**.
1. Svarglugginn fyrir „Vinna úr viðburðum vöruhúsaforrits“ opnast. Stækkið flýtiflipann **Keyra í bakgrunni** og stillið **Runuvinnsla** á **Já**.
1. Í flýtiflipanum **Keyra í bakgrunni** skal velja **Endurtekning**.
1. Svarglugginn **Skilgreina endurtekningu** opnast. Stillið keyrslu áætlunar eftir þörfum fyrir fyrirtækið.
1. Veljið **Í lagi** til að fara aftur í svargluggann **Vinna úr viðburðum vöruhúsaforrits**.
1. Veljið **Í lagi** í svarglugganum **Vinna úr viðburðum vöruhúsaforrits** til að bæta runuvinnslunni við runuröðina.

## <a name="query-warehouse-app-events"></a>Fyrirspurn um viðburði vöruhúsaforrits

Hægt er að skoða viðburðaröðina og viðburðaskilaboðin sem farsímaforrit vöruhúsakerfis býr til með því að fara í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Kladdar fartækis \> Viðburðir vöruhúsaforrits**.

## <a name="the-standard-event-queue-process"></a>Hefðbundin vinnsla á viðburðaröð

Viðburðaröð vöruhúsaforrits er yfirleitt notuð með eftirfarandi tegundum flæðis:

1. Viðburði verður bætt við biðröðina með skilaboði fyrir viðburðinn. Nýju skilaboðin eru upphaflega með viðburðarstöðuna á **Í bið**, sem þýðir að runuvinnslan **Vinna úr viðburðum vöruhúsaforrits** nær ekki í og vinnur úr þessum skilaboðum.
1. Um leið og staða viðburðar er uppfærð í **Í biðröð**, mun runuvinnsla viðburða **Vinna úr viðburðum vöruhúsaforrits** sækja og vinna úr viðburði.
1. Runuvinnslan uppfærir stöðu viðburðarins í annaðhvort **Lokið** eða **Tókst ekki**, fer eftir því hvort umbeðin vinnsla var möguleg.
1. Þegar öllum tengdum skilaboðum viðburðar er **Lokið**, er viðburðinum eytt úr biðröðinni.

 Til að sjá ítarlegt dæmi skal fara í [Stofna flutningspöntun úr vinnslu vöruhúsaforrits](create-transfer-order-from-warehouse-app.md).

## <a name="handle-event-errors"></a>Meðhöndla villur í atburðum

Sem hluti af úrvinnslu viðburða vöruhúss, getur verið að umbeðin aðgerð skilaboðanna fái ekki úrvinnslu frá runuvinnslunni. Í þessu tilfelli breytist skilaboð viðburðarins í **Tókst ekki**. Hægt er að nota upplýsingarnar **Runukladdi** til að komast að ástæðunni og grípa til nauðsynlegra aðgerða til að leysa vandamálið.

Til að sjá ítarlegt dæmi skal fara í [Stofna flutningspöntun úr vöruhúsaforriti](create-transfer-order-from-warehouse-app.md).

Til að endurstilla mislukkuð viðburðarskilaboð vöruhúsaforrits:

1. Farið í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Kladdar fartækis \> Viðburðir vöruhúsaforrits**.
1. Í flýtiflipanum **Viðburðarskilaboð vöruhúsaforrits** skal finna og velja viðeigandi viðburð sem sýnir **Tókst ekki** í dálknum **Staða viðburðar**.
1. Veljið **Endurstilla** í tækjastikunni **Viðburðarskilaboð vöruhúsaforrits**.
1. Vinnið áfram þar til öll viðeigandi skilaboð eru endurstillt.

Einnig er hægt að fjarlægja **tókst ekki** viðburðarskilaboð með því að nota **Eyða** valkostinn í tækjastikunni **Viðburðarskilaboð vöruhúsaforrits**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
