---
title: Stofna gerðir áætlana
description: Áætlunargerð í Microsoft Dynamics 365 Human Resources er há stigi flokkun á tilteknum tegundum af fríðindum. Hver áætlunartegund hefur kóða gerð áætlunar sem ákvarðar reglur fyrir gerð áætlunarinnar.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb4746425c2faa3c0b1bd3940bf2e03cf7f9595c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057863"
---
# <a name="create-plan-types"></a>Stofna gerðir áætlana

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Áætlunargerð í Microsoft Dynamics 365 Human Resources er há stigi flokkun á tilteknum tegundum af fríðindum. Hver áætlunartegund hefur kóða gerð áætlunar sem ákvarðar reglur fyrir gerð áætlunarinnar. Til dæmis, áætlunartegund Grunnlífsins myndi hafa tegundar kóðans Líf vegna þess að hún er eins konar líftryggingaráætlun og verður að vera í samræmi við reglur sem settar voru fyrir gerð kóða lífsins. Önnur áætlunartegund gæti verið viðbótarlíf, einnig með tegundar kóða kóða Líf.

Hver áætlunartegund gefur til kynna hvort starfsmaður geti skráð sig í eina áætlun af sinni gerð eða margfeldi. Til dæmis væri starfsmaður líklega fær um að skrá sig í bæði grunnlífið og viðbótarlífsstefnurnar af áætluninni Líf. Starfsmanni væri líklega leyft að skrá sig í eina stefnu af gerðinni Medical.

Ef áætlunartegundir fela í sér tengiliði, sýnir áætlunartegundin hvort tengiliðir séu styrkþegar eða á framfæri. Til dæmis, grunnlífsáætlunartegund myndi hafa rétthafa, en grunnlæknisfræðileg áætlunartæki væru á framfæri. Í sumum tilvikum er ekki víst að nein persónuleg tengsl séu í áætlun. Til dæmis sveigjanlegur útgjaldareikningur eða bílastæðagreiðsla.

Áætlunartegundir geta skilgreint valkosti umfjöllunar. Valkostir umfjöllunar eru skilgreindir í formi umfjöllunarvalkostar. Með umfjöllunarvalkosti er hægt að tilgreina fjárhæð bóta eða þá tengiliði sem eiga kost á áætlunartegundinni. Til dæmis, ef samskiptategundin er bótaþegi, ætti umfjöllunarvalkosturinn að skilgreina skilmála þess sem styrkþeginn er hæfur til að fá þegar fríðindin eru nýtt. Ef tengiliðategundin er háð, ætti umfjöllunarvalkosturinn að skilgreina samband milli háðs og starfsmanns. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Áætlunargerðir**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Gerð áætlunar** | Einstakt nafn sem auðkennir gerð áætlunarinnar. |
   | **Lýsing** | Lýsing á áætlunargerð. |
   | **Gerð kóða áætlunargerðar** | Veljið áætlunargerðarkóða úr í fellilistagildunum. Númeralisti áætlunartegundarinnar sýnir allar áætlunartegundir sem eru studdar í núverandi útgáfu. |
   | **Samhliða skráning** | Tilgreinir hvort starfsmaður geti skráð sig í margvíslegar fríðindaáætlanir af sömu áætlunartegund eða eingöngu einni fríðindaáætlun á hverja áætlunartegund. |
   | **Gerð tengiliðar** | Tilgreinir hlutverk persónulegs tengiliðar. Gildin eru auð, háð og rétthafi. Þú getur haft **Tengiliðagerð** auðan ef áætlunartegund þeirra þarfnast ekki háðs eða rétthafa miðað við tryggingarvalkostinn. |

4. Veldu til að stilla valkosti fyrir lífatburði **Aðgerðir** og veldu síðan **Valkostir fyrir viðburði**. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Gerð áætlunar** | Gerð áætlunarinnar til að stilla valkosti viðburða fyrir. |
   | **Auðkenni gerðar viðburðar** | Auðkenni tegundar atburðar í lífinu. |
   | **Leyfa að hætta við** | Tilgreinir hvort starfsmaður geti sagt upp bótaáætlun meðan á lífstímabilinu stendur. |
   | **Breyta tryggingarvalkosti** | Tilgreinir hvort starfsmaður geti sagt upp breytt tryggingakostum meðan á viðburði stendur. |
   | **Breyta í nýja áætlun** | Tilgreinir hvort starfsmaður geti sagt upp breytt áætlunum meðan á viðburði stendur. |
   | **Hætta sjálfkrafa við áætlun** | Tilgreinir hvort hætta eigi við áætlunina sjálfkrafa meðan á atburðinum stendur. |
   | **Opna sjálfkrafa aftur hæfnisathugun** | Tilgreinir hvort opna eigi sjálfkrafa aftur hæfnisathugun fríðindaskráningar á meðan viðburðinum stendur. |
   | **Tilkynningargluggi** | Tilgreinir tilkynningarglugga viðburðar í dögum. **Athugið**: Ef þú slærð ekki inn upphæð gerir kerfið ráð fyrir að skýrsluglugginn sé núll og afgreiði ekki viðburðinn. |

5. Veljið **Vista**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]