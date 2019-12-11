---
title: Afurðasafnseiningar
description: Þetta efni veitir yfirlit yfir afurðasafnseiningar í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785468"
---
# <a name="product-collection-modules"></a>Afurðasafnseiningar  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni veitir yfirlit yfir afurðasafnseiningar í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Vöruuppgötvun er aðalverkfærið sem smásalar nota til að eiga samskipti við viðskiptavini sína á vefsíðu netverslunar. Afurðasafnseiningar hjálpa smásöluaðilum að byggja upp sannfærandi verslunarupplifun með því að bjóða upp á leiðandi sjónviðmót sem hægt er að nota til að skrifa afurðasöfn á fljótlegan hátt.

Afurðasafnseiningar tákna efnislegar vörur og þjónustu á vefsíðunni. Afurðasafnseining er venjulega tengd við upplýsingasíðu þar sem viðskiptavinir geta keypt vöru eða þjónustu, eða kynnt sér það meira. 

Heimildir fyrir afurðasafni geta verið listar af þremur gerðum:

- Ristjórnartlistar yfir afurðir sem eru skilgreindar handvirkt í Dynamics 365 Retail sem skyldar afurðir fyrir afurð, eða afurðalista
- Reikniritlistar, svo sem listar yfir nýjar, mest seldu eða vinsælar afurðir
- Tilmælalistar sem eru byggðir á vélanámi

Eftirfarandi mynd sýnir mismunandi gerðir af afurðasöfnum sem notaðar eru á netverslunarsíðu.

![Dæmi um mismunandi tegundir afurðasafna á netverslunarsíðu](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Notaðu ávallt afurðasafnseiningar til að sýna hóp af afurðum af svipaðri gerð eða þema.

## <a name="product-collection-modules-and-types"></a>Afurðasafnseiningar og gerðir

Eftirfarandi tafla lýsir ýmsum gerðum af afurðasafnseiningum í Dynamics 365 Commerce.

| Afurðasafnseining  | Gerð | Lýsing |
|----------------------------|------|-------------|
| Flett í tegund            | Ritill | Þessi gerð af afurðasafnseiningunni notar tegundastigveldi yfirlitsflokks sem smásalinn bjó til fyrir smásölurás til að sýna flettiflæði fyrir afurðir sem eru í boði í tilteknum vefflokki. |
| Leitarniðurstöður             | Leitarfyrirspurn | Þessi gerð afurðasafnseininga sýnir lista yfir vörur sem passa best við leitarfyrirspurnina sem viðskiptavinurinn sló inn. |
| Tengdar afurðir           | Ritill | Þessi gerð af afurðasafnseiningum sýnir lista yfir afurðir sem verslunarstjóri hefur stillt sem tengdar afurðir í Retail, fyrir þá tengslagerð sem höfundur valdi. |
| Sérvaldir afurðalistar      | Ritill | Þessi gerð afurðasafnseininga sýnir sérsniðna lista sem söluaðilar og ritstjórar hafa búið til í Retail. |
| Nýjar                        | Reiknirit | Þessi gerð af afurðasafnseiningum sýnir lista yfir nýjustu vörurnar sem hafa verið settar á rásir og vörulista. |
| Mest selt               | Reiknirit | Þessi gerð af afurðasafnseiningum sýnir lista yfir vörur sem raðað er eftir mestum fjölda sölu. |
| Vinsælt                   | Reiknirit | Þessi gerð afurðasafnseininga sýnir lista yfir vörur sem skila mestum árangri á tilteknu tímabili. |
| Oft keypt saman | Gervigreind/Vélanám | Þessi gerð af afurðasafnseiningunni notar vélnám til að greina kaupmynstur neytenda og mæla með skyldum vörum sem eru oft keyptar ásamt tiltekinni afurð. |
| Fólki líkar einnig við           | Gervigreind/Vélanám | Þessi gerð af afurðasafnseiningunni notar vélnám til að greina kaupmynstur neytenda og mæla með vörum sem eru skyldar tiltekinni afurð. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Bæta afurðasafnseiningu við flokksíðu

Til að bæta afurðasafnseiningu við flokksíðu skaltu fylgja þessum skrefum.

1. Í Dynamics 365 Commerce ferðu á vefsvæðið og býrð til síðu sem notar sama sniðmát og sjálfgefna flokkasíðan þín.
1. Í síðuútlínunum velurðu hólfið **Undirsíðufótur**, velur úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.
1. Í svarglugganum **Bæta við einingu** skal velja **Gám** og síðan smella á **Í lagi**.
1. Í gámaeiningunni skaltu velja úrfellingarhnappinn og veldu síðan **Bæta við einingu**.
1. Í svarglugganum **Bæta við einingu** skal velja **Afurðasafn** og síðan smella á **Í lagi**.
1. Stilltu stillingar með því að velja viðeigandi gagnagjafa og inntak fyrir afurðasafnið.
1. Í eiginleikaglugganum fyrir afurðasafnseininguna velurðu **Bæta við afurðalista**.
1. Í valmyndinni **Velja stillingu afurðalista** velurðu gerð listans, slærð inn fjölda vara og veldu hvaða valkosti sem eru tiltækir fyrir listategundina. Nánari upplýsingar um listagerðir er að sjá í töflunni sem fylgir. 
1. Veljið **Í lagi**.
1. Vistaðu síðuna og skráðu hana inn.

Eftirfarandi tafla sýnir listagerðirnar sem hægt er að velja í valmyndinni **Velja stillingu afurðalista**.
   
| Gerð                       | Lýsing | Almenn venja | Samhengi sem hægt er að fá út frá samhengi síðunnar | Samhengi sem höfundur getur hnekkt síðusamhengi með |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Afurðir eftir flokki       | Listi yfir afurðir sem tilheyra tilteknum flokki. Þessi flokkur er ákvörðaður út frá annaðhvort síðasamhengi eða samhengi sem höfundur býður upp á. | Auðgaðu flokksíðu, heimasíðuna, kassa- og körfusíður og vörusíður | Tegund | Flokkur ákveðinn af höfundi |
| Tengdar afurðir           | Listi yfir afurðir sem verslunarstjóri hefur stillt sem tengdar vörur í Retail fyrir tengslagerð. | Afurðasíður, kassa- og körfusíður, óskalistasíða og síður viðskiptavinareikninga | Afurð, tengslagerð (skylda)  | Afurðar, tengslagerð |
| Sérvalið                    | Sérsniðinn listi sem söluaðilar og ritstjórar hafa búið til í Retail. | Auðgaðu flokksíðu, heimasíðuna, kassa- og körfusíður og vörusíður | Á ekki við | Listatiltekt |
| Reiknirit                | <ul><li>**Nýtt** - Listi yfir nýjustu afurðirnar sem hafa verið flokkaðar í rásir og vörulista.</li><li>**Mest selt** - Listi yfir vörur sem eru metnar með mesta sölu.</li><li>**Vinsælt** - Listi yfir vörur sem skila mestum árangri á tilteknu tímabili.</li></ul> | Heimasíða, auðguð flokkasíða og kassa- og körfusíður | Tegund | Flokkur ákveðinn af höfundi |
| Oft keypt saman | Listi sem notar vélnám til að greina kaupmynstur neytenda og mæla með skyldum vörum sem eru oft keyptar ásamt tiltekinni afurð. | Afurðasíður og kassa- og körfusíður | Afurð, karfa | Hafa körfu með |
| Fólki líkar einnig við           | Listi sem notar vélnám til að greina kaupmynstur neytenda og mæla með vörum sem tengjast tiltekinni afurð. | Afurðasíður og kassa- og körfusíður | Afurð, karfa | Á ekki við |

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Myndaræmueining](add-carousel.md)

[Eining með fjölbreyttu efni](add-content-rich-block.md)

[Eining staðsetningar efnis](add-content-placement-modules.md)

[Hólfeining](add-container-module.md)

[Kaupgluggaeining](add-buy-box.md)

