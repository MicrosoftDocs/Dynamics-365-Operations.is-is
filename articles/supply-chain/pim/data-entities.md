---
title: Afurðagagnaeiningar
description: Þessi grein veitir upplýsingar um mismunandi aðila sem hægt er að nota til að flytja inn og flytja út afurðagögn.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: e37e0928d8633a81d3a736527f2545cd61055a78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859199"
---
# <a name="product-data-entities"></a>Afurðagagnaeiningar

[!include [banner](../includes/banner.md)]

Til að flytja afurðagögn inn og út verður að nota gagnaeiningar. Eftirfarandi tafla veitir upplýsingar um afurðatengdar gagnaeiningar og lýsir tilgangi hverrar þeirrar.

| Eining | Heiti hugbúnaðarhlutatrés (AOT) (gerð) | Athugasemdir |
|--------|-------------------------------------------|-------|
| Afurðir V2 | `EcoResProductV2Entity` | Þessi eining er notuð til að flytja inn og flytja út sameiginlegar afurðir-einkvæmar afurðir og afurðarsniðmát. Hún gerir ráð fyrir uppfærslum. Hún styður ekki samstöðubyggðar SQL-aðgerðir. Hún er virkjuð fyrir Open Data Protocol (OData). |
| Útgefnar afurðir V2 | `EcoResReleasedProductV2Entity` | Þessi eining er notuð til að flytja inn og flytja út losaðar afurðir-einkvæmar afurðir og afurðarsniðmát. Hún gerir ráð fyrir uppfærslum. Hún krefst þess að hluti afurðarinnar hafi þegar verið búinn til. Þegar ný útgefin afurð er flutt inn á sér stað útgáfa af samnýttu afurðinni. Það eru líka aðskildar einingar sem hægt er að nota til að flytja inn og flytja út losuð afurðarsniðmát og losuð einkvæm afbrigði. Þessi eining styður ekki samstöðubyggðar SQL-aðgerðir né eyðir aðgerðum. Hún er virkjuð fyrir OData. |
| Útgefin stofnun afurðar V2 | `EcoResReleasedProductCreationV2Entity` | Þessi eining er notuð til að flytja inn samnýttar afurðir og útgefnar vörur í einu skrefi. Þó að hún styðji útflutning er ekki mælt með þeirri notkun, vegna þess að tilgangur einingarinnar er vöruframleiðsla. Hún styður ekki uppfærslur. Hún styður takmarkað mengi reita (reitir sem eru fáanlegir í valmynd vörusköpunar). Hún styður ekki samstöðubyggðar SQL-aðgerðir. Hún er ekki birt í gegnum OData. |
| Afurðarafbrigði | `EcoResProductVariantEntity` | Þessi eining er notuð til að flytja inn og flytja út afbrigði af samnýttum vörum. Hún gerir ráð fyrir uppfærslum. Hún krefst þess að víddargildi hafi þegar verið búin til. Sameiningartakkinn er afurðarsniðmátið og afurðarvíddirnar. Þessi eining styður ekki samstöðubyggðar SQL-aðgerðir. Hún er virkjuð fyrir OData. Hún styður aðgerðir til að eyða. Ekki er hægt að framlengja hana með því að bæta við nýjum afurðavíddum. |
| Afurðarafbrigði eftir kenni afurðarnúmers | `EcoResProductNumberIdentifiedProductVariantEntity` | Þessi eining er notuð til að flytja inn og flytja út afbrigði af samnýttum vörum. Hún gerir ráð fyrir uppfærslum. Hún krefst þess að víddargildi hafi þegar verið búin til. Samþættingarlykillinn er vörunúmerið (en samþættingarlykill fyrir eininguna **Afurðarafbrigði** er afurðarsniðmátið og afurðarvíddirnar). |
| Útgefin afurðarafbrigði | `EcoResReleasedProductVariantEntity` | Þessi eining er notuð til að flytja inn og flytja út afbrigði af útgefnum vörum. Hún gerir ráð fyrir uppfærslum. Hún krefst þess að hluti afurðarfbrigðanna hafi þegar verið búinn til. Þegar nýtt útgefið afurðarafbrigði er flutt inn á sér stað útgáfa af samnýtta afurðarafbrigðinu. Þessi eining styður ekki samstöðubyggðar SQL-aðgerðir. Hún er virkjuð fyrir OData. Þó að það styðji aðgerðir til að eyða, þá veldur sú notkun eins og stendur spillingu í gögnum vegna villu á núverandi verkvangi. Ekki er hægt að framlengja þessa einingu með því að bæta við nýjum afurðavíddum. |
| Útgefin afurðarafbrigði eftir kenni afurðarnúmers | `EcoResProductNumberIdentifiedReleasedProductVariantEntity` | Þessi eining er lík einingunni **Útgefin afurðarafbrigði** en samþættingarlykillinn er afurðarnúmerið í staðinn fyrir afurðarsniðmátið og afurðarvíddirnar. Hægt er að framlengja hana með því að bæta við nýjum afurðavíddum. |
| Seljanlegar útgefnar afurðir | `EcoResSellableReleasedProductEntity` | Þessi eining er notuð til að flytja aðeins út seljanlegar vörur. Seljanlegar vörur eru vörur sem hafa þær upplýsingar sem þær þurfa til að vera notaðar í sölupöntun. Sama regla gildir þegar vara er villuleituð með því að nota **Villuleita** virknina á síðunni **Útgefnar afurðir**. |
| Útgefnar einkvæmar afurðir V2 | `EcoResDistinctProductV2Entity` | Þessi eining er notuð til að flytja út einkvæmar afurðir. Þessar einkvæmu afurðir geta verið afurðir, undirafurðir og afurðaafbrigði. |
| Útgefin afurðarsniðmát V2 | `EcoResProductMasterV2Entity` | Þessi eining er notuð til að flytja inn og flytja út afurðarsniðmát. Hún er ekki virkjuð fyrir gagnastjórnun. |
| Atriði - strikamerki | `EcoResProductBarcodeEntityV3` | Þessi eining er notuð til að flytja út afurðir og strikamerki. Þessi eining leyfir ekki breytingarakningu, uppfærslur eða eyðingu. Til að nota breytingarakningu, uppfærslur eða eyðingu á strikamerkjum skal nota eininguna **Atriði - Strikamerkjatengsl**. |
| Atriði - strikamerkjatengsl | `EcoResProductBarcodeAssociationEntity` | Þessi eining er notuð til að flytja út afurðir og strikamerki. Þar er hægt að breyta rakningu, uppfærslum og eyðingu. Til að nota eininguna verður að virkja eiginleikann *Atriði - endurbætur strikamerkis* í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Einingarlykill hennar er `AssociationID` sem myndar tengslin milli strikamerkis og afurðar. Til að bæta við stuðningi fyrir þennan hnapp verður taflan `InventitemBarcodeAssociation` fyllt út fyrir fyrirliggjandi strikamerkjagögn vöru þegar kveikt er á eiginleikanum. Taflan er fyllt út með runuvinnslu og ef strikamerkjataflan er með mikið magn af færslum gæti það tekið nokkurn tíma að keyra runuvinnsluna. Þess vegna mælum við með því að eiginleikinn verði virkjaður (og þar af leiðandi runuvinnslan) á hentugum tíma. |
| Lífferilsstaða afurðar | `EcoResProductLifecycleSateEntity` | Þessi eining er notuð til að flytja inn og flytja út mismunandi líftímastöður afurðar sem hægt er að úthluta afurð. |

> [!NOTE]
> Aðeins er hægt að nota gagnaeininguna **Útgefnar afurðir V2** til að flytja afurðir inn í kerfið ef samnýtta afurðin hefur þegar verið búin til. Að öðrum kosti, til að flytja vörur inn í kerfið verður að nota gagnaeininguna **Afurðasköpun**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]