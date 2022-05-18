---
title: Bæta við gagnareitum í skattaskilgreiningum
description: Þetta efnisatriði útskýrir hvernig á að sérsníða skattaskilgreiningar með því að bæta við gagnasvæðum.
author: Kai-Cloud
ms.date: 10/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: deb19c8ddf20b416864ed8c3f816f92e43309f71
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694094"
---
# <a name="add-data-fields-in-tax-configurations"></a>Bæta við gagnareitum í skattaskilgreiningum

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að sérstilla skattaskilgreiningar [gagnareiti sem er bætt við í skattasamþættingu](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Sérstilla skattgagnalíkan

1. Í Microsoft Dynamics 365 Fjármál, farðu til **Rafræn skýrslugerð** > **Skattstillingar**.
2. Í skilgreiningartrénu skal velja **Gagnalíkan skattaútreiknings**. Í aðgerðasvæðinu velurðu svo **Stofna skilgreiningu**. 

  > [!NOTE] 
  > Ef engin skilgreiningarveita er tiltæk skal búa til eina og virkja hana fyrir skattaskilgreininguna. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
  
3. Í fellilistanum velurðu **Skattskylt skjallíkan afleitt af nafni: Skattútreikningsgagnalíkan, Microsoft** valkostinn, slærð inn heiti fyrir nýja skattgagnalíkanið og velur **Stofna skilgreiningu**.
4. Veljið skattgagnalíkan sem nýverið var stofnuð, og síðan, á Aðgerðarúðu, smellið á **Hönnuður**.
5. Víkkið tré gagnalíkans, veljið **Línur** og svo **Ný**.
6. Í svarglugganum **Stofna hnút** skaltu slá inn nafn, tilgreina gerð atriðis og velja svo **Bæta við**.
7. Bæta skal við öllum áskildum dálkum.
8. Á aðgerðasvæðinu skal velja **Vista** og síðan **Ljúka**.
9. Lokaðu síðunni og skoðaðu lokaútgáfu af skattgagnalíkani þínu.

## <a name="customize-the-tax-configuration"></a>Sérstilla skattaskilgreiningu

1. Í Finance er farið í **Rafræn skýrslugerð** > **Skattaskilgreiningar**.
2. Í skilgreiningartrénu skal velja **Skilgreining skattaútreiknings**. Í aðgerðasvæðinu velurðu svo **Stofna skilgreiningu**.
3. Í fellilistanum velurðu **Skilgreining skattþjónustu afleidd af nafni: Skattareikningsskilgreining, Microsoft**, slærð inn heiti fyrir nýju skattaskilgreininguna og velur **Stofna skilgreiningu**.
4. Veljið skattaskilgreiningu sem nýverið var stofnuð, og síðan, á Aðgerðarúðu, smellið á **Hönnuður**.
5. Í hlutanum **Eiginleikar** í **Gagnalíkan** skal velja sérstillta skattgagnalíkanið sem var búið til áður.
6. Í reitnum **Útgáfa gagnalíkans** er lokið við að velja útgáfu af gerð skattagagnalíkansins.
7. Veljið **Bæta við** og bætið við nauðsynlegum skattalegum ráðstöfunum.
8. Á aðgerðasvæðinu skal velja **Vista** og síðan **Ljúka**.
9. Lokaðu síðunni og skoðaðu lokaútgáfu af skattskilgreiningunni þinni.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Innleiða skattaeiginleika í sérsniðinni skattaskilgreiningu

1. Í Regulatory Configuration Service (RCS) skal fara í **Altækir eiginleikar** > **Skattur**.
2. Veljið **Bæta við**, sláið inn upplýsingar um nýja eiginleikann og veljið svo **Búa til eiginleika**.
3. Á flipanum **Útgáfur** skal velja eiginleikann og svo **Breyta**.
4. Á flipanum **Almennt** í reitnum **Útgáfa skilgreiningar** skal velja sérstillta skattaskilgreiningu og útgáfu.
5. Í svarglugganum **Stjórna dálkum** skal velja haus og línudálka sem á að hafa með á sérstilltri skattaráðstöfun og velja svo rétta örvatakkann til að bæta þeim á listann **Valdir dálkar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
