---
title: Gerðir virkra staðsetninga
description: Þetta efni lýsir hvernig á að stofna gerðir virkra staðsetninga í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb758f9ef205c06cbb9d18b498a5cd7c36012714
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783358"
---
# <a name="functional-location-types"></a>Gerðir virkra staðsetninga

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Þetta efni lýsir hvernig á að stofna gerðir virkra staðsetninga í eignastjórnun. Gerðir virkra staðsetninga eru notaðar til að stjórna kröfum um virkar staðsetningar, þar með talið hvernig eignir eru settar upp á virkri staðsetningu. Þú getur sett upp eignategundir, viðhaldsáætlanir, eigindi virkrar staðsetninga og eignaeigindakröfur til að nota á virkri staðsetningu sem notar sérstaka gerð virkrar staðsetningar. Þegar þú býrð til virka staðsetningu er gerð virkrar staðsetningar lögboðin.

>[!NOTE] 
>Til að vinna með virkar staðsetningar verður þú að búa til sjálfgefna virka staðsetningu sem eingöngu er notuð í þeim tilgangi að búa til nýjar eignir. Fyrir þá sjálfgefnu virku staðsetningu sem þú notar ættir þú að búa til sjálfgefna gerð virkrar staðsetningar sem er mjög einföld og gerir kleift að setja upp margar eignir á sjálfgefna virka staðsetningu. Sjá [Stofna virkar staðsetningar](../functional-locations/create-functional-locations.md) fyrir frekari upplýsingar um hvernig á að setja upp virkar staðsetningar.

## <a name="create-a-default-functional-location-type"></a>Stofna sjálfgefna gerð virkrar staðsetningar

Þessi aðferð sýnir hvernig á að búa til sjálfgefna gerð virkrar staðsetningar sem á að nota fyrir sjálfgefna virka staðsetningu.

1. Veldu **Eignastýring** > **Uppsetning** > **Virkar staðsetningar** > **Gerðir virka staðsetninga**.
2. Veldu **Nýr** til að stofna nýja gerð virkrar staðsetningar.
3. Settu kenni virkrar staðsetningar inn í reitinn **Gerð virkrar staðsetningar**, til dæmis „Sjálfgefið“, og heiti í reitinn **Heiti**.
4. Veldu líftímalíkan í reitnum **Líftímalíkan virkrar staðsetningar**.
5. Veldu „Já“ á skiptihnappnum **Margar eignir** til að leyfa fleiri eignum að vera settar upp á virkri staðsetningu (sjálfgefinn virk staðsetning) með því að nota þessa gerð.

Núna hefur sjálfgefin gerð virkrar staðsetningar sem aðeins á að nota fyrir sjálfgefna virka staðsetningu verið stofnuð. Þú ættir ekki að bæta við fleiri kröfum eða takmörkunum við þessa sjálfgefnu gerð virkrar staðsetningar.


## <a name="create-functional-location-types"></a>Stofna gerðir virkar staðsetningar

1. Veldu **Eignastýring** > **Uppsetning** > **Virkar staðsetningar** > **Gerðir virka staðsetninga**.
2. Veldu **Nýr** til að stofna nýja gerð virkrar staðsetningar.
3. Settu kenni virkrar staðsetningar inn í reitinn **Gerð virkrar staðsetningar** og heiti í reitinn **Heiti**.
4. Veldu líftímalíkan í reitnum **Líftímalíkan virkrar staðsetningar**. Sjá [Líftímastöður virkrar staðsetningar](../setup-for-functional-locations/functional-location-stages.md) til að fá frekari upplýsingar um líftímastöður virkra staðsetninga og líftímalíkön.
5. Veldu „Já“ á skiptihnappnum **Margar eignir** ef það á að vera hægt að setja upp margar eignir upp á virkri staðsetningu með því að nota þessa gerð virkrar staðsetningar. Ef þú velur „Nei“ geturðu aðeins sett upp *eina* eign á virkri staðsetningu með því að nota þessa gerð virkrar staðsetningar.
6. Veldu „Já“ á skiptihnappnum **Uppfæra eignavídd** ef þú vilt að eignir séu settar upp á virkri staðsetningu af þessari gerð til að nota sjálfkrafa fjárhagsvíddir sem tengjast virkri staðsetningu. Þetta þýðir að ef þú breytir fjárhagslegum stærðum í forminu [Virk staðsetning](../functional-locations/create-functional-locations.md) og virka staðsetningin notar gerð virkrar staðsetningar með þessum skiptihnappi sem er stillt á „Já“ eru fjárhagvíddir eru sjálfkrafa uppfærðar á öllum eignum sem settar eru upp á þeirri virku staðsetningu.
7. Reiturinn **Gerð eigna** er notaður ef þú vilt búa til sjálfkrafa *eina* eign fyrir virka staðsetningu með sama kenni og heiti og virka staðsetningin sem þú ert að búa til. Til dæmis getur þetta skipt máli ef þú býrð til kyrrstæða virka staðsetningu, svo sem byggingu eða leiðslu. Í því tilfelli skaltu velja eignategundina sem þú vilt nota fyrir sjálfvirkt stofnaða eignina. Mundu að ef þú gerir val á þessu sviði, þá verður skiptihnappurinn **Margar eignir** að vera stilltur á „Nei“.
8. Á flýtiflipanum **Gerðir eigna** veldu þá eignategund sem á að tengjast gerð virku staðsetningarinnar. Veldu **Bæta við línu** og veldu eignagerðirnar. Ef þú bætir við eignategundum hér er aðeins hægt að setja upp eignir sem nota þessar eignategundir á virkri staðsetningu með því að nota þessa gerð virkrar staðsetningar. Ef engar eignategundir eru valdar á flýtiflipanum **Gerðir eigna** kunna allar eignategundir að vera settar upp.
9. Á flýtiflipanum **Viðhaldsáætlanir** veldu viðhaldsáætlanir sem sjálfkrafa ætti að setja upp á nýjum virkum staðsetningum með því að nota þessa gerð virkrar staðsetningar. Veldu **Bæta við línu** og veldu viðhaldsáætlanir. Ef þú bætir við viðhaldsáætlunum hér, er aðeins hægt að nota þessar áætlanir á virkri staðsetningu með því að nota þessa gerð virkrar staðsetningar.
10. Á flýtiflipanum **Kröfur eignaeiginda** seturðu upp eignaeigindi sem sjálfkrafa ætti að setja upp á nýjum virkum staðsetningum með því að nota þessa gerð virkrar staðsetningar. Veldu **Bæta við línu** og veldu eigindina. Þessar eigindakröfur virka sem leiðbeiningar. Þær eru ekki staðfestir á móti eigindum sem settir eru upp á eign (**Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir** > veldu eign á listasíðunni > flipanum **Almennt** > hnappnum **Eigindir**). Eigindkröfurnar eru sýndar þegar þú setur upp eignir á virkum stöðum.
11. Á flýtiflipanum **Leyfðar gerðir** veldu gerðir virkrar staðsetningar sem ættu að gilda fyrir gerðir virkra undirstaðsetninga sem tengjast gerð virkrar yfirstaðsetningar sem notar valda gerð virkrar staðsetningar.
12. Á flýtiflipanum **Eigindir** veldu eigindir virkrar staðsetningar sem sjálfkrafa ætti að setja upp á nýjum virkum staðsetningum með því að nota þessa gerð virkrar staðsetningar. Veldu **Bæta við línu** og veldu eigindina.


>[!NOTE] 
>Á flýtiflipanum **Almennt** geturðu fengið yfirlit yfir fjölda eignagerða, viðhaldsáætlanir, eignaeigindakröfur, leyfðar gerðir, eigindi og virkar staðsetningar sem settar eru upp á gerð virkrar staðsetningar. Reiturinn **Virkar staðsetningar** sýnir fjölda virkra staðsetninga sem nota gerð virkrar staðsetningar. Þú getur notað hnappinn **Afrita** til að afrita stillingar frá gerð virkrar staðsetningar yfir í valda gerð virkrar staðsetningar.
