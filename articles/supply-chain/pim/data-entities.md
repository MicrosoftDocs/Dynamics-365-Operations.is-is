---
title: Afurðagagnaeiningar
description: Þetta efni veitir upplýsingar um mismunandi aðila sem hægt er að nota til að flytja inn og flytja út afurðagögn.
author: cvocph
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: 340cb33537c7ba07555e1f0b6437fa4a3458a11a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208617"
---
# <a name="product-data-entities"></a>Afurðagagnaeiningar

[!include [banner](../includes/banner.md)]

Til að flytja afurðagögn inn og út verður að nota gagnaeiningar. Eftirfarandi tafla veitir upplýsingar um afurðatengdar gagnaeiningar og lýsir tilgangi hverrar þeirrar.

| Eining | Heiti hugbúnaðarhlutatrés (AOT) (gerð) | Athugasemdir |
|--------|-------------------------------------------|-------|
| Afurðir V2 | EcoResProductV2Entity | Þessi eining er notuð til að flytja inn og flytja út sameiginlegar afurðir-einkvæmar afurðir og afurðarsniðmát. Hún gerir ráð fyrir uppfærslum. Hún styður ekki samstöðubyggðar SQL-aðgerðir. Hún er virkjuð fyrir Open Data Protocol (OData). |
| Útgefnar afurðir V2 | EcoResReleasedProductV2Entity | Þessi eining er notuð til að flytja inn og flytja út losaðar afurðir-einkvæmar afurðir og afurðarsniðmát. Hún gerir ráð fyrir uppfærslum. Hún krefst þess að hluti afurðarinnar hafi þegar verið búinn til. Þegar ný útgefin afurð er flutt inn á sér stað útgáfa af samnýttu afurðinni. Það eru líka aðskildar einingar sem hægt er að nota til að flytja inn og flytja út losuð afurðarsniðmát og losuð einkvæm afbrigði. Þessi eining styður ekki samstöðubyggðar SQL-aðgerðir né eyðir aðgerðum. Hún er virkjuð fyrir OData. |
| Útgefin stofnun afurðar V2 | EcoResReleasedProductCreationV2Entity | Þessi eining er notuð til að flytja inn samnýttar afurðir og útgefnar vörur í einu skrefi. Þó að hún styðji útflutning er ekki mælt með þeirri notkun, vegna þess að tilgangur einingarinnar er vöruframleiðsla. Hún styður ekki uppfærslur. Hún styður takmarkað mengi reita (reitir sem eru fáanlegir í valmynd vörusköpunar). Hún styður ekki samstöðubyggðar SQL-aðgerðir. Hún er ekki birt í gegnum OData. |
| Afurðarafbrigði | EcoResProductVariantEntity | Þessi eining er notuð til að flytja inn og flytja út afbrigði af samnýttum vörum. Hún gerir ráð fyrir uppfærslum. Hún krefst þess að víddargildi hafi þegar verið búin til. Sameiningartakkinn er afurðarsniðmátið og afurðarvíddirnar. Þessi eining styður ekki samstöðubyggðar SQL-aðgerðir. Hún er virkjuð fyrir OData. Hún styður aðgerðir til að eyða. Ekki er hægt að framlengja hana með því að bæta við nýjum afurðavíddum. |
| Afurðarafbrigði eftir kenni afurðarnúmers | EcoResProductNumberIdentifiedProductVariantEntity | Þessi eining er notuð til að flytja inn og flytja út afbrigði af samnýttum vörum. Hún gerir ráð fyrir uppfærslum. Hún krefst þess að víddargildi hafi þegar verið búin til. Samþættingarlykillinn er vörunúmerið (en samþættingarlykill fyrir eininguna **Afurðarafbrigði** er afurðarsniðmátið og afurðarvíddirnar). |
| Útgefin afurðarafbrigði | EcoResReleasedProductVariantEntity | Þessi eining er notuð til að flytja inn og flytja út afbrigði af útgefnum vörum. Hún gerir ráð fyrir uppfærslum. Hún krefst þess að hluti afurðarfbrigðanna hafi þegar verið búinn til. Þegar nýtt útgefið afurðarafbrigði er flutt inn á sér stað útgáfa af samnýtta afurðarafbrigðinu. Þessi eining styður ekki samstöðubyggðar SQL-aðgerðir. Hún er virkjuð fyrir OData. Þó að það styðji aðgerðir til að eyða, þá veldur sú notkun eins og stendur spillingu í gögnum vegna villu á núverandi verkvangi. Ekki er hægt að framlengja þessa einingu með því að bæta við nýjum afurðavíddum. |
| Útgefin afurðarafbrigði eftir kenni afurðarnúmers | EcoResProductNumberIdentifiedReleasedProductVariantEntity | Þessi eining er lík einingunni **Útgefin afurðarafbrigði** en samþættingarlykillinn er afurðarnúmerið í staðinn fyrir afurðarsniðmátið og afurðarvíddirnar. Hægt er að framlengja hana með því að bæta við nýjum afurðavíddum. |
| Seljanlegar útgefnar afurðir | EcoResSellableReleasedProductEntity | Þessi eining er notuð til að flytja aðeins út seljanlegar vörur. Seljanlegar vörur eru vörur sem hafa þær upplýsingar sem þær þurfa til að vera notaðar í sölupöntun. Sama regla gildir þegar vara er villuleituð með því að nota **Villuleita** virknina á síðunni **Útgefnar afurðir**. |
| Útgefnar einkvæmar afurðir V2 | EcoResDistinctProductV2Entity | Þessi eining er notuð til að flytja út einkvæmar afurðir. Þessar einkvæmu afurðir geta verið afurðir, undirafurðir og afurðaafbrigði. |
| Útgefin afurðarsniðmát V2 | EcoResProductMasterV2Entity | Þessi eining er notuð til að flytja inn og flytja út afurðarsniðmát. Hún er ekki virkjuð fyrir gagnastjórnun. |
| Vara - strikamerki | EcoResProductBarcodeEntity | Þessi eining er notuð til að flytja út afurðir og strikamerki. |
| Lífferilsstaða afurðar | EcoResProductLifecycleSateEntity | Þessi eining er notuð til að flytja inn og flytja út mismunandi líftímastöður afurðar sem hægt er að úthluta afurð. |

> [!NOTE]
> Aðeins er hægt að nota gagnaeininguna **Útgefnar afurðir V2** til að flytja afurðir inn í kerfið ef samnýtta afurðin hefur þegar verið búin til. Að öðrum kosti, til að flytja vörur inn í kerfið verður að nota gagnaeininguna **Afurðasköpun**.
