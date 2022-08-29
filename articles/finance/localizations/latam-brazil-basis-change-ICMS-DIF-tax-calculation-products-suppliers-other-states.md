---
title: Breyting á grunni í ICMS-DIF skattaútreikningum fyrir afurðir frá birgjum í öðrum ríkjum
description: Þessi grein lýsir uppsetningu fyrir útreikninga á skattategundinni ICMS-DIF þegar skattskjal er móttekið í Brasilíska fylkinu Rio Grande do Sul (RS) eða São Paulo (SP).
author: Kai-Cloud
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218650"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Grunnbreyting (tvöfaldur grunnur) í ICMS-DIF skattaútreikningum fyrir vörur frá birgjum í öðrum ríkjum

Þessi grein lýsir uppsetningu fyrir útreikninga á **ICMS-DIF** skattategund þegar skattskjal er móttekið í brasilíska fylkinu Rio Grande do Sul (RS) eða São Paulo (SP).

Samkvæmt skilgreiningunni í ríkislögunum verður Imposto sobre Circulação de Mercadorias e Serviços (ICMS) sem safnað er að fylgja þessari reglu:

*ICMS til að safna* = ([(*Aðgerðarupphæð* –*ICMS frá uppruna*) ÷ (1 –*ICMS % innri*)] ×*ICMS % innri*) -*ICMS upphæð frá uppruna*

## <a name="example"></a>Dæmi

Brasilískt fyrirtæki í RS-ríkinu fær fjárhagsskjal fyrir kaup frá söluaðila í SP-ríkinu. Fyrirtækið verður að innheimta prósentumismun ICMS milli RS-ríkis (18 prósent) og SP-ríkis (12 prósent). Hins vegar ber að reikna grunninn samkvæmt fyrri reglu.

- **Aðgerðarupphæð:** 1.000,00 brasilískir raunir (1.000,00 R$)
- **ICMS milliríki:** R$ 120,00
- **ICMS hlutfall í RS ríkinu:** 18 prósent
- **ICMS til að safna í RS ríkinu:** (\[ (1.000 – 120) ÷ (1 – 0,18)\] × 0,18) – 120 = R$ 73,17 

## <a name="resolution"></a>Upplausn

Til að reikna út mismunadrifið ICMS (ICMS-DIF) samkvæmt reglum RS-ríkisins verður þú að setja upp VSK-kóða og VSK-flokk á eftirfarandi hátt:

1. Búðu til söluskattskóða til að fá 12 prósenta ICMS (fyrir hitt ríkið). Þessi kóði er notaður til að skrá skattkröfur frá seljanda.
2. Búðu til söluskattskóða til að safna ICMS-DIF. Þessi söluskattskóði ætti að hafa prósentuupphæðina 18 prósent (fyrir þitt eigið ríki) til að skilgreina muninn á milli 18 prósent og 12 prósent. Stilltu skatttegundina á **ICMS-DIF**. Þessi virðisaukaskattskóði verður að vera skilgreindur á eftirfarandi hátt í útreikningsbreytum:

    - Í **Uppruni** reit, veldu **Hlutfall af brúttófjárhæð**.
    - Í **Jaðargrunnur** reit, veldu **Nettóupphæð á línu**.
    - Skilgreindu skattlagningarkóðann þannig að hann hafi fjárhagslegt gildi sem **3**. Á þennan hátt verður leiðréttingarfærslan sjálfkrafa búin til þegar **Fjárhagsbækur** eining er virkjuð.
    - Í uppsetningu söluskattshópsins skaltu velja **Notaðu skatt** valkostur fyrir **ICMS-DIF** söluskattskóða.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Notaðu deltaskattshlutfallið í uppsetningu tvíþættra ICMS-DIF söluskattskóða

Þegar áður lýstar stillingar eru notaðar, er **ICMS-DIF** söluskattskóði verður reiknaður út í tvíþættri grunnreglu. Hins vegar verður nafnskattshlutfallið 18 prósent, sem er frábrugðið 6 prósenta hlutfallinu í einföldu grunnreglunni. Þessi munur veldur ósamræmi í fjárhagsskjali og skattskýrslugerð. Frá Microsoft Dynamics 365 Finance útgáfa 10.0.29, þú getur virkjað **(Brasilía) Stilltu delta skatthlutfallið í ICMS-DIF skattkóða fyrir tvöfalt grunnfall** lögun í **Eiginleikastjórnun** til að eyða ósamræminu.

- Auk þess að klára skrefin í fyrri hlutanum skaltu velja **ICMS 12** söluskattskóða í **Söluskattur af söluskatti** sviði.
- Stilltu skatthlutfallið **ICMS-DIF** söluskattskóða í 18 prósent. The **Hlutfall/upphæð** reit mun sýna nafnskattshlutfallið sem 6 prósent.

> [!NOTE]
> The **ICMS-DIF** og **ICMS 12** VSK-kóðum verður að úthluta í sama VSK-flokki.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Grunnbreyting (tvöfaldur grunnur) í ICMS-DIF skattaútreikningum fyrir vörur til neytenda sem ekki eru skattgreiðendur (DIFAL) í öðrum ríkjum

Virkjaðu **(Brasilía) Tvískiptur grunnútreikningur fyrir ICMS-DIFAL í söluviðskiptum** lögun í **Eiginleikastjórnun** til að styðja við grunnbreytinguna ICMS-DIF um viðskipti við neytendur sem ekki eru skattgreiðendur frá öðru ríki. Dæmi um ICMS-DIF söluskattskóðinn verður virkur í sölupöntunum og reikningsfærslum með frjálsum texta.

Virkjaðu **(Brasilía) Tvöfaldur grunnútreikningur fyrir ICMS-DIFAL fyrir IPI tilvik** lögun í **Eiginleikastjórnun** til að styðja við aðstæður þar sem viðskipti við neytendur sem ekki eru skattgreiðendur frá öðru ríki bera einnig ábyrgð á Imposto sobre Produtos Industrializados (IPI). Skattfjárhæð IPI söluskattskóða verður viðurkennd og notuð í ICMS-DIFAL skattstofni.

- Á haus sölupöntunar eða ókeypis textareiknings, á **Upplýsingar um ríkisfjármál** Flýtiflipi, the **Endanleg notandi** valkostur verður að vera stilltur á **Já**.
- Á haus innkaupapöntunar eða reiknings lánardrottins, á **Upplýsingar um ríkisfjármál** Flýtiflipi, the **Notkun og neysla** valkostur verður að vera stilltur á **Já**.
