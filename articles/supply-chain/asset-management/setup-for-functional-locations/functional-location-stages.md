---
title: Líftímastöður virkra staðsetninga
description: Þessi grein lýsir því hvernig á að setja upp virka staðsetningarstöðu og líftímalíkön í eignastýringu.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae56c2b734339343b134be95abe0ce40b70c8a0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934730"
---
# <a name="functional-location-lifecycle-states"></a>Líftímastöður virkra staðsetninga

[!include [banner](../../includes/banner.md)]

 

Þessi grein lýsir því hvernig á að setja upp virka staðsetningarlífferilsstöðu og lífferilslíkön í eignastýringu. Líftímastöður virkra staðsetninga skilgreina þau ríki sem hagnýtur staðsetning getur farið í gegnum, til dæmis búið til, virkan og endað. Þú getur skoðað allar virkar staðsetningar, óháð líftímastöðu þeirra, á listasíðunni **Allar virkar staðsetningar**. Þú getur breytt stöðu virkrar staðsetningar með því að velja hana á listasíðunni **Allar virkar staðsetningar** og velja **Uppfæra stöðu virkar staðsetningar**.

## <a name="set-up-functional-location-lifecycle-states"></a>Setja upp líftímastöður virkra staðsetninga

1. Veldu **Eignastýring** > **Uppsetning** > **Virkar staðsetningar** > **Líftímastöður**.
2. Veldu **Nýr** til að stofna nýja virk staðsetning.
3. Settu stöðukennið inn í reitinn **Líftímastaða** og heiti á stöðu virkrar staðsetningar í reitnum **Heiti**. Í reitnum **Líftímalíkön** er hægt að sjá fjölda virkra líftímalíkana virkrar staðsetningar sem nota stöðu virkrar staðsetningar.
4. Á flýtiflipanum **Almennt** velurðu „Já“ á skiptihnappnum **Virkur** ef virk staðsetning ætti að vera virk í þessari stöðu.
5. Veldu „Já“ á skiptihnappnum **Stofna eignir** ef það ætti að vera mögulegt að búa sjálfkrafa til eign með sama nafni og virka staðsetningin og setja hana upp á virkri staðsetningu í þessari stöðu.  
>[!NOTE]
>Þessi skiptihnappur tengist reitnum **Gerð eigna** á flýtiflipanum **Almennt** í forminu **Gerðir virkra staðsetninga** (**Eignastýring** > **Uppsetning** > **Virkar staðsetningar** > **Gerðir virkra staðsetninga**).

6. Veldu „Já“ á skiptihnappnum **Endurnefna staðsetningu** ef það ætti að vera mögulegt að breyta heiti á virkni staðsetningunni í þessari stöðu.
7. Veldu „Já“ á skiptihnappnum **Nýjar undirstaðsetningar** ef það ætti að vera mögulegt að bæta nýjum undirstaðsetningum við virku staðsetninguna í þessari stöðu.
8. Veldu „Já“ á skiptihnappnum **Setja upp eignir** ef það ætti að vera mögulegt að setja upp eignir á virku staðsetningunni í þessari stöðu.
9. Veldu „Já“ á skiptihnappnum **Eyða virkri staðsetningu** ef það ætti að vera mögulegt að eyða virkri staðsetningu í þessari stöðu.
10. Veldu eignarstöðu í reitnum **Líftímastaða** ef þú vilt að líftímastaða eignar fyrir allar eignir sem settar eru upp á virkri staðsetningu verði uppfærðar sjálfkrafa í þessari stöðu. Dæmi: Ef þú lokar virkri staðsetningu og stillir líftímastöðu virkrar staðsetningar á „Lokið“, gætirðu viljað breyta sjálfkrafa líftímastöðu eigna sem eru settar upp á þeirri virku staðsetningu í „Ekki í notkun“.


>[!NOTE]
>Líftímastaða virkrar staðsetningar, líftímalíkön og gerðir eru tengdar og notaðar á sama hátt og líftímastöður verkbeiðni, líftímalíkön verkbeiðni og gerðir verkbeiðni. 

## <a name="set-up-functional-location-lifecycle-models"></a>Setja upp Líftímalíkön virkra staðsetninga

Þegar þú hefur búið til líftímastöður sem krafist er fyrir virkar staðsetningar þínar, þeim er hægt að skipta í hópa. Þetta er gert til að búa til flæði líftímalíkansins sem hægt er að nota fyrir mismunandi gerðir af virkum stöðum. Að lágmarki ætti að búa til eitt staðlað líftímalíkan fyrir virka staðsetningu.

1. Veldu **Eignastýring** > **Uppsetning** > **Virkar staðsetningar** > **Líftímalíkön**.
2. Veldu **Nýr** til að stofna nýtt líftímalíkan.
3. Settu líftímalíkanið inn í reitinn **Líftímalíkan** og heiti á líftímalíkaninu í reitnum **Heiti**. Í reitunum **Gerðir virkra staðsetninga** og **Líftímastöður** geturðu séð fjölda virka staðsetninga sem nota líftímalíkanið og fjölda valinna staða í líftímalíkaninu.
4. Á flýtiflipanum **Líftímastöður** velurðu þær stöður sem ætti að vera með í líkaninu. Þetta er gert með því að smella á stöðu í hlutanum **Eftirstandandi líftímastaða** og smella á ![ör áfram.](media/02-setup-for-functional-locations.png) hnappur.
5. Ef velja á allar tiltækar stöður fyrir líkan skal smella á ![velja öll tiltæk stig.](media/03-setup-for-functional-locations.png) hnappur. Allar stöður eru fluttar í hlutann **Valdar líftímastöður**.
6. Ef þú vilt fjarlægja valda stöðu úr líkaninu skal velja stöðuna í hlutanum **Líftímastöður valdar** og síðan velja ![ör til baka.](media/04-setup-for-functional-locations.png) hnappur.
7. Veldu **Uppfærslur á líftímastöðu** til að skilgreina hvaða líftímastaða getur fylgt valinni stöðu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
