---
title: Breyting á grunni í ICMS-DIF skattaútreikningum fyrir afurðir frá birgjum í öðrum ríkjum
description: Þessi grein lýsir uppsetningu útreikninga á ICMS-DIF skatttegundinni þegar tekið er á móti fjárhagsskjali í brasilíska ríkinu Rio Grande do Sul (RS) eða São Paulo (SP).
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218650"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Breyting á grunni (tvöfaldur grunnur) í ICMS-DIF skattaútreikningum fyrir vörur frá birgjum í öðrum ríkjum

Þessi grein lýsir uppsetningu útreikninga á **ICMS-DIF** skatttegundinni þegar tekið er á móti fjárhagsskjali í brasilíska ríkinu Rio Grande do Sul (RS) eða São Paulo (SP).

Samkvæmt skilgreiningu í lögum ríkisins verður Imposto sobre Circulação de Mercadorias e Serviços (ICMS) sem innheimt er að fylgja þessari reglu:

*ICMS til að safna* = ([(*Rekstrarfjárhæð* – *ICMS frá uppruna*) ÷ (1 – *ICMS % innri*)] × *ICMS % innri*) – *ICMS upphæð frá uppruna*

## <a name="example"></a>Dæmi

Brasilískt fyrirtæki í RS-ríkinu fær fjárhagsskjal fyrir kaup frá lánardrottni í SP-ríkinu. Fyrirtækið verður að innheimta prósentumun ICMS milli RS-ríkis (18 prósent) og SP-ríkis (12 prósent). Grunninn verður þó að reikna eftir framangreindri reglu.

- **Rekstrarfjárhæð: 1.000,00** brasilískir real (R$ 1.000,00)
- **ICMS milli ríkja:** R$ 120,00
- **ICMS-prósenta í RS-ástandi:** 18 prósent
- **ICMS til að safna í RS-ríki:** (\[(1.000 – 120) ÷ (1 – 0,18)\] × 0,18 ) – 120 = R$ 73,17 

## <a name="resolution"></a>Upplausn

Til að reikna út mismunandi ICMS (ICMS-DIF) samkvæmt reglum RS-ríkisins verður að setja upp söluskattkóða og söluskattflokk á eftirfarandi hátt:

1. Stofna söluskattkóða til að fá 12 prósent ICMS (fyrir hitt ríkið). Þessi kóði er notaður til að skrá upphæð innskatts frá lánardrottni.
2. Stofna VSK-kóða til að innheimta ICMS-DIF. Söluskattkóðinn ætti að vera 18 prósent (fyrir eigið ríki) til að skilgreina muninn á 18 prósentum og 12 prósentum. Stilltu skattgerðina á **ICMS-DIF**. Skilgreina þarf þennan söluskattkóða á eftirfarandi hátt í reiknibreytum:

    - Í reitnum **Uppruni** er valið **Prósenta af brúttóupphæð**.
    - Í reitnum **Jaðargrunnur** skaltu velja **Nettóupphæð á línu**.
    - Skilgreindu skattkóðann þannig að hann hafi fjárhagsgildi **3**. Á þennan hátt verða leiðréttingarfærslurnar sjálfkrafa búnar til þegar **Skattabækur** einingin er virk.
    - Í uppsetningu söluskattflokksins, veldu valkostinn **Neysluskattur** fyrir **ICMS-DIF** söluskattskóðann.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Notaðu delta skatthlutfallið í stillingu á tvöföldum grunni ICMS-DIF söluskattakóða

Þegar áður lýstar stillingar eru notaðar er **ICMS-DIF** söluskattskóðinn reiknaður út í tvískiptri grunnreglu. Nafnskatthlutfallið verður hins vegar 18 prósent, sem er annað en 6 prósent skatthlutfallið í einföldu grunnreglunni. Þessi munur veldur ósamræmi í fjárhagsskjali og skattskilum. Frá og með Microsoft Dynamics 365 Finance útgáfa 10.0.29, getur þú **(Brasilía) Grunnstillið deltaskatthlutfallið í skattkóða ICMS-DIF fyrir tvöfaldan grunn** eiginleiki í **Eiginleikastjórnun** til að fjarlægja ósamræmið.

- Auk þess að ljúka skrefunum í fyrri hlutanum skaltu velja **ICMS 12** VSK-kóðann í reitnum **VSK á VSK**.
- Stilltu skatthlutfall **ICMS-DIF** söluskattskóðans í 18 prósent. Reiturinn fyrir **Prósenta/upphæð** sýnir nafnskattshlutfallið sem 6 prósent.

> [!NOTE]
> **ICMS-DIF** og **ICMS 12** söluskattskóðarnir verða að vera úthlutað á sama söluskattsflokk.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Breyting á grunni (tvöfaldur grunnur) í ICMS-DIF skattaútreikningum fyrir vörur til þeirra sem ekki greiða skatt (DIFAL) í öðrum ríkjum

Virkjaðu **(Brasilía) Tvöfaldur grunnútreikningur fyrir ICMS-DIFAL í sölufærslum** eiginleikann í **Eiginleikastjórnun** til að styðja grundvallarbreytingu ICMS-DIF á viðskiptum við neytendur sem ekki eru skattskyldir frá öðru ríki. Söluskattskóði ICMS-DIF dæmisins verður virkur í sölupöntun og reikningyn með frjálsum texta.

Virkjaðu **(Brasilía) Tvöfaldur grunnútreikningur fyrir ICMS-DIFAL fyrir IPI-tilvik** eiginleikann í **Eiginleikastjórnun** til að styðja aðstæður þar sem viðskipti við neytendur sem ekki eru skattskyldir frá öðru ríki eru einnig ábyrgir fyrir Imposto sobre Produtos Industrializados (IPI). Skattfjárhæð IPI söluskattakóðans verður tekjufærð og notuð á ICMS-DIFAL skattstofninn.

- Á haus sölupöntunar eða reiknings með frjálsum texta, á **Fjárhagsupplýsingar** flýtiflipanum þarf valkosturinn **Endanlegur notandi** að vera stilltur á **Já**.
- Á haus innkaupapöntunar eða reiknings lánardrottins, á **Fjárhagsupplýsingar** flýtiflipanum þarf valkosturinn **Notkun og neysla** að vera stilltur á **Já**.
