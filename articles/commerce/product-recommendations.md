---
title: Yfirlit yfir afurðarráðleggingar
description: Þetta efnisatriði veitir almennar upplýsingar um afurðatillögur. Afurðatillögur auðvelda viðskiptavinum að finna vörur sem þeir vilja á fljótlegan hátt og jafnvel vörur sem þeir ætluðu ekki upphaflega að kaupa.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770048"
---
# <a name="product-recommendations-overview"></a>Yfirlit yfir afurðarráðleggingar

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce má nota til að sýna afurðatillögur á vefsíðu netverslunar og sölustað (POS) tækinu. Afurðatillögur eru vörur sem viðskiptavinur gæti haft áhuga á. Ráðleggingarnar eru byggðar á kaupþróun annarra viðskiptavina í verslunum á netinu og verslunum sjálfum.

Afurðatillögur gera viðskiptavinum auðveldlega og fljótt að finna vörur sem þeir vilja á meðan þeir hafa reynslu sem þjónar þeim vel. Krosssölu og uppsölu er jafnvel hægt að nota til að hjálpa viðskiptavinum að finna fleiri vörur en þeir ætluðu upphaflega ekki að kaupa. Þegar ráðleggingar eru notaðar til að hjálpa við uppgötvun vöru geta þau skapað fleiri viðskiptatækifæri, hjálpað til við að auka sölutekjur og jafnvel hjálpað til við að auka ánægju viðskiptavina og varðveisla.

Í Commerce eru afurðatillögur knúnar af vélanámstækni Microsoft tilmæla í stórum stíl.


## <a name="scenarios"></a>Sviðsmyndir

Afurðatillögur eru í boði fyrir eftirfarandi aðstæður:

- **Á hvaða verslunarsíðu sem er til að vafra eða áfangasíðu í netverslun:** Ef viðskiptavinir eða starfsfólk verslunarinnar heimsækja verslunarsíðu getur meðmælavélin lagt til vörur í listunum **Nýtt**, **Mest selt** og **Vinsælt**.
- **Á síðu vöruupplýsinga:** Ef viðskiptavinir eða starfsfólk verslunar fer á síðuna **Upplýsingar um vöru** mælir tillöguvélin með viðbótarvörum sem einnig er líklegt að verði keyptar. Þessar vörur birtast á listanum **Fólki líkar einnig**.
- **Á færslusíðunni eða greiðslusíðunni:** Tillöguvélin leggur til vörur, byggðar á öllum listanum yfir vörur í körfunni. Þessir vörur birtast á listanum **Oft keypt saman**.

## <a name="recommendation-service"></a>Tillöguþjónusta

Afurðatillögur nota námstækni tilmælavélanna á eftirfarandi hátt:

- Gögn á sniðinu sem tillöguþjónustan krefst eru fengin úr virknigagnagrunni Commerce og send í einingaverslunina.
- Tilmælaþjónustan notar gögnin til að þjálfa tillögulíkön fyrir listana **Fólki líkar einnig**, **Oft keypt saman**, **Nýtt**, **Mest selt** og **Vinsælt**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Búa til lista með sérvöldum afurðartillögum](create-editorial-recommendation-lists.md)

[Stjórna niðurstöðum afurðartillagna sem byggjast á AI-ML](modify-product-recommendation-results.md)

[Bæta við listum með afurðartillögum við síður](add-reco-list-to-page.md)
