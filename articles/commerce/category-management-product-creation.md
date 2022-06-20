---
title: Stjórna afurðaflokkum og afurðum
description: Þessi grein lýsir því hvernig sölustjórar geta notað vöruflokka til að stjórna tengslum milli vörustigveldis viðskipta og útgefnar vöruupplýsingar.
author: ashishmsft
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0871475e0910e0a46544c56083b505ff647fd6a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878571"
---
# <a name="manage-product-categories-and-products"></a>Stjórna afurðaflokkum og afurðum

[!include [banner](./includes/banner.md)]

Þessi grein lýsir endurbættri leið til að stjórna vöruflokkum og vörum í Dynamics 365 Commerce. Viðbæturnar gera vörustjórum kleift að skoða byggingu á eiginleikum afurðar sem er deilt milli stigveldis afurðar og upplýsinga um losaðar afurðir.

Til að læra meira um stjórnun á flokkum afurða í vinnusvæðinu **Flokka- og afurðastjórnun** skal velja reitinn **Afurðastigveldi Commerce**.

Takið eftir aukinni uppbyggingu á síðunni **Afurðastigveldi Commerce** sem birtist. Í fyrri útgáfum forritsins var eiginleikum afurða skipt niður í *grunneiginleika afurðar* og *eiginleika smásöluafurðar* byggt á notkunareiginleikum þeirra. Eiginleikar smásöluafurðar eru *altækir* í notkunareiginleikum þeirra. M.ö.o., fyrir hvern eiginleika afurðar er sama gildi deilt með öllum lögaðilum. Hins vegar eru grunneiginleikar afurðar *sértækir fyrir hvern lögaðila*. Með öðrum orðum, fyrir tiltekinn grunneiginleika afurðar getur gildið verið mismunandi milli lögaðila, fer allt eftir einstökum viðskiptakröfum hvers lögaðila.

Með aukinni byggingu á flokkum afurðar eru eiginleikar afurða röklega greindir í sundur eftir notkunareiginleikum þeirra innan hóps til að endurspegla byggingu skjámyndar fyrir upplýsingar um losaðar afurðir.

![Svæði flokkuð á grundvelli notkunareiginleika.](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Hægt er að skipta á milli þess að stjórna sértækum eiginleikum lögaðila yfir alla lögaðila og stjórna þeim fyrir tiltekinn lögaðila.

Til að stjórna eiginleikum yfir alla lögaðila skal velja **Skoða fyrir alla lögaðila** (eða **Breyta fyrir alla lögaðila**).

![Skoða/breyta fyrir alla lögaðila.](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Til að stjórna eiginleikum fyrir tiltekinn lögaðila skal velja **Skoða fyrir tiltekinn lögaðila** (eða **Breyta fyrir tiltekinn lögaðila**).

![Skoða/breyta fyrir tiltekinn lögaðila.](media/ToggleToEditForAllLegalEntities.PNG)

Auk þess getur vörustjóri í betrumbættu byggingunni á flokkum afurðar nú einnig skilgreint sjálfgildi fyrir viðbótarsett af eiginleikum afurðar á stigi einstakra flokka. Þegar afurðir eru síðan búnar til öðlast þær sjálfgefið gildi fyrir afurðaeiginleika þeirra sem byggist á tengslum þessara eiginleika við einstakan flokk í stigveldi smásöluafurðar. Þessir erfðu eiginleikar afurðar er einnig hægt að breyta fyrir hverja afurð til að uppfylla einstakar viðskiptakröfur.

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a>Val á eiginleikum til að uppfæra afurðir á síðunni Afurðastigveldi Commerce

Hægt er að nota nýju betrumbættu bygginguna fyrir eiginleika afurðar til að velja hvaða uppfærðu eiginleikar afurðar á að flytja til tengdra afurða. Á síðunni **Afurðastigveldi Commerce**, skal velja á aðgerðasvæðinu **Flokkur** og síðan velja **Uppfæra afurðir** til að opna svargluggann **Uppfæra afurðir**.

![Uppfæra svarglugga afurða.](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]