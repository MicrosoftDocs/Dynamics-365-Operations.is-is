---
title: Bæta við gagnareitum í skattaskilgreiningum
description: Þetta efnisatriði útskýrir hvernig á að sérsníða skattaskilgreiningar með því að bæta við gagnasvæðum.
author: kailiang
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9d9fce81151ad70d57c69e389e238a6f9137d56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819425"
---
# <a name="add-data-fields-in-tax-configurations"></a>Bæta við gagnareitum í skattaskilgreiningum

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hvernig á að sérstilla skattaskilgreiningar [gagnareiti sem er bætt við í skattasamþættingu](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Sérstilla skattgagnalíkan

1. Í Microsoft Dynamics 365 Finance skaltu fara í **Rafræn skýrslugerð** \> **Skattaskilgreiningar**.
2. Í skilgreiningartrénu velurðu **Skattgaganlíkan - Evrópa**. Í aðgerðasvæðinu velurðu svo **Stofna skilgreiningu**.
3. Í fellilistanum velurðu **Skattskylt skjallíkan afleitt af nafni: Skattgagnalíkan -- Evrópa, Microsoft** valkostinn, slærð inn heiti fyrir nýja skattgagnalíkanið og velur **Stofna skilgreiningu**.
4. Veljið skattgagnalíkan sem nýverið var stofnuð, og síðan, á Aðgerðarúðu, smellið á **Hönnuður**.
5. Víkkið tré gagnalíkans, veljið **Línur** og svo **Ný**.
6. Í svarglugganum **Stofna hnút** skaltu slá inn nafn, tilgreina gerð atriðis og velja svo **Bæta við**.
7. Bæta skal við öllum áskildum dálkum.
8. Á aðgerðasvæðinu skal velja **Vista** og síðan **Ljúka**.
9. Lokaðu síðunni og skoðaðu lokaútgáfu af skattgagnalíkani þínu.

## <a name="customize-the-tax-configuration"></a>Sérstilla skattaskilgreiningu

1. Í Finance er farið í **Rafræn skýrslugerð** \> **Skattaskilgreiningar**.
2. Í skilgreiningartrénu velurðu **Skattaskilgreining - Evrópa**. Í aðgerðasvæðinu velurðu svo **Stofna skilgreiningu**.
3. Í fellilistanum velurðu **Skilgreining skattþjónustu afleidd af nafni: Skattaskilgreining -- Evrópa, Microsoft** valkostinn, slærð inn heiti fyrir nýju skattaskilgreininguna og velur **Stofna skilgreiningu**.
4. Veljið skattaskilgreiningu sem nýverið var stofnuð, og síðan, á Aðgerðarúðu, smellið á **Hönnuður**.
5. Í hlutanum **Eiginleikar** í **Gagnalíkan** skal velja sérstillta skattgagnalíkanið sem var búið til áður.
6. Í reitnum **Útgáfa gagnalíkans** er lokið við að velja útgáfu af gerð skattagagnalíkansins.
7. Veljið **Bæta við** og bætið við nauðsynlegum skattalegum ráðstöfunum.
8. Á aðgerðasvæðinu skal velja **Vista** og síðan **Ljúka**.
9. Lokið síðunni og skoðið lokaútgáfu af skattgagnalíkaninu.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Innleiða skattaeiginleika í sérsniðinni skattaskilgreiningu

1. Í Regulatory Configuration Service (RCS) skal fara í **Altækir eiginleikar** \> **Skattur**.
2. Veljið **Bæta við**, sláið inn upplýsingar um nýja eiginleikann og veljið svo **Búa til eiginleika**.
3. Á flipanum **Útgáfur** skal velja eiginleikann og svo **Breyta**.
4. Á flipanum **Almennt** í reitnum **Útgáfa skilgreiningar** skal velja sérstillta skattaskilgreiningu og útgáfu.
5. Í svarglugganum **Stjórna dálkum** skal velja haus og línudálka sem á að hafa með á sérstilltri skattaráðstöfun og velja svo rétta örvatakkann til að bæta þeim á listann **Valdir dálkar**.
