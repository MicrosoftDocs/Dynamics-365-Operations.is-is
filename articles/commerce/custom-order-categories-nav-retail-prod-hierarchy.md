---
title: Breyta röðun fyrir smásölueiningar
description: Þessi grein útskýrir hugtökin sem tengjast því að stjórna birtingarpöntun fyrir ýmsar sölutengdar einingar í Dynamics 365 Commerce.
author: josaw1
ms.date: 08/11/2022
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
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265837"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Breyta röðun fyrir smásölueiningar


[!Include [banner](includes/banner.md)]

Smásalar líta á vöruuppgötvun sem aðalverkfæri til að hafa samskipti við viðskiptavini á öllum rásum. Það eru nokkrir eiginleikar sem geta hjálpað viðskiptavinum að finna vörur auðveldlega. Til dæmis geta viðskiptavinir skoðað flokka, leitað og síað.

Þessi grein útskýrir hugtökin sem tengjast því að stjórna birtingarpöntun fyrir ýmsar sölutengdar einingar. Það útskýrir einnig hvernig á að breyta röðuninni.

## <a name="overview"></a>Yfirlit

Í Commerce er flokkun ýmissa vörutengdra eininga í takt við núverandi aðstæður viðskiptavina og krefst ekki lengur framlengingar frá innleiðingaraðilum.

Í Commerce útgáfum 10.0.5 og eldri var röðun flokka í leiðsögustigveldinu stafrófsröð. Núverandi sérsniðin röðunaraðgerð gerir sölustjórum kleift að stilla flokkunarröðina fyrir ýmsar sölutengdar einingar á öllum notendaviðskiptavinum. Þessir viðskiptavinir eru með höfuðstöðvar (HQ) og símaver.

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
5. Í trénu, veldu **Tíska \> Kvennaföt \> Kvennaskór**.
6. Í reitinn **Sýna röðun** skal slá inn númer.
7. Í trénu velurðu **Tíska \> Kvenfatnaður \> Toppar**.

Sömuleiðis er hægt að skilgreina flokkunarröð fyrir undirflokkana.

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
> Sjálfgefið er **Virkja birtingarpöntun fyrir sölueiningar** slökkt er á eiginleikanum. Notaðu [Eiginleikastjórnun](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) að kveikja á því. Eftir að þú hefur kveikt á eiginleikanum skaltu keyra **Alþjóðleg stilling -1110** CDX starf úr dreifingaráætlun.
> Ef flokkapöntunin þín í POS er ekki uppfærð skaltu endurvirkja tækið. Upplýsingar um flokk eru sóttar þegar virkjun tækis á sér stað, þannig að tækið gæti þurft að sækja flokkaupplýsingarnar aftur með uppfærðum skjápöntunum. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
