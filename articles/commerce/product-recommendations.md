---
title: Yfirlit yfir afurðarráðleggingar
description: Þetta efnisatriði veitir almennar upplýsingar um afurðatillögur. Afurðatillögur auðvelda viðskiptavinum að finna vörur sem þeir vilja á fljótlegan hátt og jafnvel vörur sem þeir ætluðu ekki upphaflega að kaupa.
author: Moonma
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 667c26a8ab7665f9eb1e2cc91217338fc0eb00d6c9c21ba7b4a7e5a203e41410
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763765"
---
# <a name="product-recommendations-overview"></a>Yfirlit yfir afurðarráðleggingar

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce má nota til að sýna afurðartillögur á rafrænu vefsvæði og tæki sölustaðar. Afurðatillögur eru vörur sem viðskiptavinur gæti haft áhuga á. Ráðleggingarnar eru byggðar á kaupþróun annarra viðskiptavina í verslunum á netinu og verslunum sjálfum.

Afurðatillögur gera viðskiptavinum kleift að finna auðveldlega og fljótt vörur sem þeir vilja á meðan þeir hafa reynslu sem þjónar þeim vel. Krosssölu og uppsölu er jafnvel hægt að nota til að hjálpa viðskiptavinum að finna fleiri vörur en þeir ætluðu upphaflega ekki að kaupa. Þegar ráðleggingar eru notaðar til að auka uppgötvun vöru skapa þau fleiri viðskiptatækifæri, hjálpað til við að auka sölutekjur og jafnvel aukið ánægju viðskiptavina og varðveisla.

Í Commerce eru afurðatillögur knúnar af vélanámstækni Microsoft tilmæla í stórum stíl.

Þessi þjónusta er viðbót við Dynamics 365 Commerce. Sæktu nýjustu [Microsoft Dynamics 365 leyfishandbókina](https://go.microsoft.com/fwlink/?LinkId=866544) fyrir frekari upplýsingar.


## <a name="recommendation-service"></a>Tillöguþjónusta

Vöru ráðleggingarþjónustan notar tækni til gervigreindar og vélanáms (AI-ML) á eftirfarandi hátt:

- Gögn á sniðinu sem ráðleggingarþjónustan þarf eru dregin út úr virknigagnagrunni Commerce og send til Azure Data Lake Storage eða einingaverslunar.
- Tilmælaþjónustan notar vistuð gögnin til að þjálfa tillögulíkön fyrir listana **Fólki líkar einnig**, **Oft keypt saman**, **Nýtt**, **Mest selt** og **Vinsælt**.

## <a name="scenarios"></a>Sviðsmyndir

Afurðatillögur eru í boði fyrir eftirfarandi aðstæður:

- **Á hvaða verslunarsíðu sem er til að vafra eða áfangasíðu í netverslun:** Ef viðskiptavinir eða starfsfólk verslunarinnar heimsækja verslunarsíðu getur meðmælavélin lagt til vörur í listunum **Nýtt**, **Mest selt** og **Vinsælt**.
- **Á síðu vöruupplýsinga:** Ef viðskiptavinir eða starfsfólk verslunar fer á síðuna **Upplýsingar um vöru** mælir tillöguvélin með viðbótarvörum sem einnig er líklegt að verði keyptar. Þessar vörur birtast á listanum **Fólki líkar einnig**.
- **Á færslusíðunni eða greiðslusíðunni:** Tillöguvélin leggur til vörur, byggðar á öllum listanum yfir vörur í körfunni. Þessir vörur birtast á listanum **Oft keypt saman**.
- **Sérsniðnar ráðleggingar:** Vörur geta veitt innskráðum viðskiptavinum persónulega **velur fyrir þig** lista, auk nýrrar virkni sem gerir kleift að sérsníða fyrirliggjandi listasviðsmyndir út frá þeim viðskiptavini. Til að læra meira, sjál [Kveikja á sérsniðnum tillögum.](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>Gerðir afurðarráðlegginga

Eftirfarandi tafla lýsir ýmsum gerðum sjálfvirkra vöruábendinga sem eru í boði fyrir smásala til að útfæra í þeirra Dynamics 365 Commerce lausn í gegnum [vörusöfnunareining](product-collection-module-overview.md). Smásalar geta einnig sýnt sérsniðnar niðurstöður fyrir innritaðan notanda ef vefhöfundur velur þann valkost.

| Afurðasafnseining  | Gerð | lýsing |
|----------------------------|------|-------------|
| Nýjar                        | Reiknirit | Þessi eining sýnir lista yfir nýjustu afurðirnar sem hafa nýlega verið flokkaðar í rásir og vörulista. |
| Mest selt               | Reiknirit | Þessi eining sýnir lista yfir vörur sem eru metnar með mesta sölu. |
| Vinsælt                   | Reiknirit | Þessi eining sýnir lista yfir vörur sem skila mestum árangri á tilteknu tímabili, raðað eftir mesta sölufjölda.  |
| Oft keypt saman | AI-ML | Þessi eining mælir með lista yfir vörur sem oftast eru keyptar ásamt innihaldi núverandi körfu neytenda. |
| Fólki líkar einnig við           | AI-ML | Þessi eining mælir með vörum fyrir tiltekna grunnafurð byggða á kaupmynstri neytenda. |
| Tillögur fyrir þig              | AI-ML | Þessi eining mælir með persónulega lista yfir vörur byggðar á innkaupamynstri innritaðs notanda. Fyrir gestanotanda verður þessi listi felldur saman. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Bæta við afurðatillögum á sölustað](product.md)

[Bæta tillögum við færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
