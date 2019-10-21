---
title: Breyta röðun fyrir smásölueiningar
description: Þetta efni útskýrir hugtök sem tengjast stjórnun birtingarraðar fyrir ýmsar smásölueiningar í Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c159ff869d6c504fdebbef1fa68115a410c81d85
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019417"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Breyta röðun fyrir smásölueiningar


[!include [banner](includes/banner.md)]

Smásalar líta á vöruuppgötvun sem aðalverkfæri til að hafa samskipti við viðskiptavini á öllum smásölurásum. Ýmis virkni geta hjálpað viðskiptavinum að uppgötva vörur á auðveldan hátt. Til dæmis geta þeir skoðað flokka, leitað og síað.

Þetta efni útskýrir hugtök sem tengjast stjórnun birtingarraðar fyrir ýmsar smásölueiningar. Það útskýrir einnig hvernig á að breyta röðuninni.

## <a name="overview"></a>Yfirlit

Stuðningur við röðun ýmissa smásöluaðila hefur verið aukinn. Þessi stuðningur er nú betur í takt við núverandi viðskiptavinasviðsmyndir sem áður kröfðust viðbóta frá framkvæmdaraðilum.

Í útgáfum af Retail sem eru eldri en útgáfa 10.0.5 var röðunin fyrir flokka í yfirlitsstigveldinu í stafrófsröð. Nýja sérsniðna röðunaraðgerðin gerir kleift vörustjórum smásölu að stilla röðunina fyrir ýmsar smásölueiningar á milli allra viðskiptavina. Þessir viðskiptavinir eru með höfuðstöðvar (HQ) og símaver.

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a>Skilgreindu birtingarröð fyrir flokka í stigveldi smásöluafurðar

Áður en þú getur klárað þetta ferli verður að setja upp kynningargögn í umhverfi þínu.

1. Farðu í **Smásala \> Afurðir og flokkar \> Stigveldi smásöluafurða**.
2. Smelltu á **Breyta tegundastigveldi**.
3. Smellið á **Breyta**.
4. Í trénu stækkarðu **ALL \> Action Sports**.
5. Í trénu stækkarðu **ALL \> Hópíþróttir**.
6. Í reitinn **Sýna röðun** skal slá inn númer. (Talan getur verið neikvæð.)
7. Endurtaktu skref 4 til 6 fyrir fleiri flokka sem þú vilt breyta röðinni á.

Skjápöntunin fyrir yfirlitsstigveldi rásar mun endurspeglast í aðalstöðvum fyrir stigveldi smásöluafurðar og losaðar afurðir eftir flokkum.

![Sérsniðin stigveldi smásöluafurða flokkuð með neikvæðum gildum](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Losaðar afurðir eftir flokkum sérraðað eftir stigveldi smásöluafurðar](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Skilgreindu birtingarröð fyrir flokka í yfirlitsstigveldi rásar

Áður en þú getur klárað þetta ferli verður að setja upp kynningargögn í umhverfi þínu.

1. Farðu í **Smásala \> Afurðir og flokkar \> Yfirlitsflokkar rásar**.
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

Birtingarröð fyrir yfirlitsstigveldi rásarinnar endurspeglast í aðalstöðvum, vörulista og smásölurásum.

![Sérröðun yfirlitsstigveldis rásar](./media/ChannelNavCustomSorted.png)

![Yfirlitsstigveldi vörulista sérflokkuð eftir yfirlitsstigveldi rásarinnar](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Sölustaður með sérsniðnum flokkum](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Sjálfgefið er að slökkt sé á sérröðunarstillingunni. Til að læra hvernig á að kveikja á þessum eiginleika og öðrum eiginleikum skal sjá [Eiginleikastjórnun](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).
