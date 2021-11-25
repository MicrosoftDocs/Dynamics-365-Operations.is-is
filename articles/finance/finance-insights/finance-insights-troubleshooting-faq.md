---
title: Úrræðaleit fyrir vandamál varðandi uppsetningu fjármálainnsýnar
description: Í þessu efnisatriði eru talin upp vandamál sem geta komið upp þegar möguleikar fjármálainnsýnar eru notaðir. Þar er einnig útskýrt hvernig á að laga þessi vandamál.
author: panolte
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: f3cac30a66ff3a74a7f67c11dd9fa14af79d10af
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752618"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Úrræðaleit fyrir vandamál varðandi uppsetningu fjármálainnsýnar

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessu efnisatriði eru talin upp vandamál sem geta komið upp þegar möguleikar fjármálainnsýnar eru notaðir. Þar er einnig útskýrt hvernig á að laga þessi vandamál.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Einkenni: Hvers vegna get ég ekki varpað viðtökudálki fyrir sniðmát gagnasamþættingar greiðsluinnsýnar viðskiptavinar?

### <a name="resolution"></a>Upplausn

Þú gætir verið að nota sniðmát fyrir eldri útgáfu. Áður en útgáfa 10.0.17 er gefin út, hafa viðskiptavinir forskoðað og stillt sniðmát gagnasamþættingar (DI) **Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops)** með því að nota eininguna **Niðurstaða greiðsluspár (forskoðun)**. Eftir uppfærslu í 10.0.17 og síðar ættir þú að nota DI-sniðmátið fyrir **Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops útgáfu 10.0.17 og síðar)** til að ljúka vörpuninni. Ekki er víst að þú getir varpað viðtökudálki DI-sniðmáts fyrr en einingalisti gagnastjórnunar er uppfærður og einingin **Niðurstaða greiðsluspár** birtist þar. Til að uppfæra einingalistann og sýna niðurstöðu greiðsluspár lýkurðu við skref í bæði Microsoft Dynamics 365 Finance og Dataverse (áður þekkt sem Common Data Service \[ CDS\] stjórnendagátt).

### <a name="in-finance"></a>Í Finance

Fylgdu þessum skrefum í Finance eftir uppfærslu.

1. Opnaðu **Kerfisstjórnun \> Vinnusvæði \> Gagnastjórnun**.
2. Á vinnusvæðinu **Gagnastjórnun** skal velja reitinn **Færibreytur ramma**.
3. Á síðunni **Færibreytur ramma fyrir inn- og útflutning gagna** skal velja **Einingastillingar** og síðan velja **Uppfæra einingalista**.
4. Lokaðu síðunni **Færibreytur ramma fyrir inn- og útflutning gagna**.
5. Á vinnusvæðinu **Gagnastjórnun** skal velja reitinn **Gagnaeiningar**.
6. Leitaðu að „Niðurstaða greiðsluspár“. Staðfestu að einingin **Niðurstaða greiðsluspár** sé ekki forútgáfan. Heiti forútgáfunnar endar á „(forskoðun)“. Ef þú sérð aðeins forútgáfu einingarinnar skaltu hafa samband við notendaþjónustu Microsoft.

### <a name="in-dataverse"></a>Í Dataverse

Fylgdu eftirfarandi skrefum í [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com/environments) til að uppfæra gagnasamþættingarverkin þín.

1. Ef þú ert að nota forútgáfu fjármálainnsýnar skaltu fjarlægja DI-verkið sem er tengt við sniðmátið **Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops)**.
2. Fylgdu skrefunum í [Stofna gagnasamþættingarverk](create-data-integrate-project.md). Notaðu sniðmátið **Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops 10.0.17 og síðar)**.

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Einkenni: Þegar ég reyni að opna AI Builder með því að nota tenglana á uppsetningarsíðunni fyrir greiðsluspá viðskiptavina, hvers vegna fæ ég eftirfarandi villuboð: „Því miður, það hefur verið sambandsleysi“?

### <a name="resolution"></a>Upplausn

Dynamics 365 Finance notendur verða að hafa a Microsoft Power Apps notandareikningur fyrir umhverfið, og sá notendareikningur verður að hafa hlutverk sérsniðnar kerfis. The Microsoft Power Apps kerfisstjóri getur búið til notendareikninginn og úthlutað hlutverkinu. Þú getur þá farið á<https://make.preview.powerapps.com/>, skráðu þig inn með því að nota þann notandareikning og reyndu aftur tenglana.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Einkenni: Hvers vegna sýnir flipi reiðufjárspár á vinnusvæði sjóðsstreymisspáar ekki nein gögn?

### <a name="resolution"></a>Upplausn

Virkni sjóðsstreymisspár í reiðufjár- og bankastjórnun og eiginleika sjóðsstreymisspáar í fjármálainnsýn verður að vera sett upp og virkjuð til að sýna gögn á réttan hátt á vinnusvæðinu **Sjóðstreymisspá**.

Fyrst skal setja upp og virkja sjóðsstreymisspá og greiðslugetulykla. Frekari upplýsingar er að finna í [Sjóðstreymisspá](../cash-bank-management/cash-flow-forecasting.md). Ef þessari uppsetningu er lokið en þú sérð ekki niðurstöðurnar sem þú býst við skaltu skoða [Úrræðaleit vegna uppsetningar sjóðstreymisspár](../cash-bank-management/cash-flow-forecasting-tsg.md) til að fá frekari upplýsingar.

Næst skal staðfesta að eiginleiki sjóðsstreymisspár í fjármálainnsýn (**Reiðufjár- og bankastjórnun \> Uppsetning \> Fjármálainnsýn \> Sjóðstreymisspár**) hafi verið virkjaður og að þjálfun gervigreindarlíkansins sé lokið. Ef þjálfuninni er ekki lokið skaltu velja **Spá núna** til að hefja þjálfunarferli líkansins.
