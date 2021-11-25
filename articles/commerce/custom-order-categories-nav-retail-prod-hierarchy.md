---
title: Breyta röðun fyrir smásölueiningar
description: Þetta efni útskýrir hugtök sem tengjast stjórnun birtingarraðar fyrir ýmsar smásölueiningar í Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 444f1ebd99cf8443181a51d93a48b6b4d1addf4d
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779543"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Breyta röðun fyrir smásölueiningar


[!Include [banner](includes/banner.md)]

Smásalar líta á vöruuppgötvun sem aðalverkfæri til að hafa samskipti við viðskiptavini á öllum rásum. Ýmis virkni geta hjálpað viðskiptavinum að uppgötva vörur á auðveldan hátt. Til dæmis geta þeir skoðað flokka, leitað og síað.

Þetta efni útskýrir hugtök sem tengjast stjórnun birtingarraðar fyrir ýmsar smásölueiningar. Það útskýrir einnig hvernig á að breyta röðuninni.

## <a name="overview"></a>Yfirlit

Stuðningur við röðun ýmissa smásöluaðila hefur verið aukinn. Þessi stuðningur er nú betur í takt við núverandi viðskiptavinasviðsmyndir sem áður kröfðust viðbóta frá framkvæmdaraðilum.

Í útgáfum af Retail sem eru eldri en útgáfa 10.0.5 var röðunin fyrir flokka í yfirlitsstigveldinu í stafrófsröð. Nýja sérsniðna röðunaraðgerðin gerir kleift vörustjórum smásölu að stilla röðunina fyrir ýmsar smásölueiningar á milli allra viðskiptavina. Þessir viðskiptavinir eru með höfuðstöðvar (HQ) og símaver.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Skilgreindu birtingarröð fyrir flokka í afurðastigveldi

Áður en þú getur klárað þetta ferli verður að setja upp kynningargögn í umhverfi þínu.

1. Farðu í **Retail og Commerce \> Afurðir og tegundir \> Afurðastigveldi Commerce**.
2. Smelltu á **Breyta tegundastigveldi**.
3. Smellið á **Breyta**.
4. Í trénu stækkarðu **ALL \> Action Sports**.
5. Í trénu stækkarðu **ALL \> Hópíþróttir**.
6. Í reitinn **Sýna röðun** skal slá inn númer. (Talan getur verið neikvæð.)
7. Endurtaktu skref 4 til 6 fyrir fleiri flokka sem þú vilt breyta röðinni á.

Skjápöntunin fyrir yfirlitsstigveldi rásar mun endurspeglast í aðalstöðvum fyrir stigveldi afurðar netverslunar og losaðar afurðir eftir flokkum.

![Afurðarstigveldi raðað með neikvæðum gildum.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Losaðar afurðir eftir flokki raðað út frá afurðastigveldinu.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Skilgreindu birtingarröð fyrir flokka í yfirlitsstigveldi rásar

Áður en þú getur klárað þetta ferli verður að setja upp kynningargögn í umhverfi þínu.

1. Farðu í **Retail og Commerce \> Afurðir og flokkar \> Yfirlitsflokkar rásar**.
2. Af listanum velurðu stigveldið **Tískuyfirlit**.
3. Smelltu á **Breyta tegundastigveldi**.
4. Smellið á **Breyta**.
5. Í trénu velurðu **Tíska \> Kvenfatnaður \> Dömuskór**.
6. Í reitinn **Sýna röðun** skal slá inn númer.
7. Í trénu velurðu **Tíska \> Kvenfatnaður \> Toppar**.

    Sömuleiðis er hægt að skilgreina röðun fyrir undirflokka.

8. Í trénu velurðu **Tíska \> Herrafatnaður \> Óformlegar skyrtur**.
9. Í reitinn **Sýna röðun** skal slá inn númer.
10. Í trénu velurðu **Tíska \> Herrafatnaður \> Frakkar og jakkar**.
11. Í reitinn **Sýna röðun** skal slá inn númer.
12. Endurtaktu fyrir fleiri flokka sem þú vilt breyta röðinni á.

Birtingarröð fyrir yfirlitsstigveldi rásarinnar endurspeglast í aðalstöðvum, vörulista og rásum.

![Sérstillt röðun á yfirlitsstigveldi rásar.](./media/ChannelNavCustomSorted.png)

![Sérstillt röðun á yfirlitsstigveldi vörulista samkvæmt yfirlitsstigveldi rásar.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Sölustaður með sérstillta röðun flokka.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Sjálfgefið er að slökkt sé á sérröðunarstillingunni. Til að læra hvernig á að kveikja á þessum eiginleika og öðrum eiginleikum skal sjá [Eiginleikastjórnun](/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]