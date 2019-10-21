---
title: Setja upp vöruhús með því að nota skilgreiningarsniðmát vöruhúss
description: Þetta efnisatriði útskýrir hvernig skal setja upp vöruhús með því að nota skilgreiningarsniðmát vöruhúss.
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 3a6645bc55dfd4f03ce9872ff5017f1659b1f11c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017598"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Setja upp vöruhús með því að nota skilgreiningarsniðmát vöruhúss

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig skal setja upp vöruhús með því að nota skilgreiningarsniðmát vöruhúss. Til eru nokkrar forskilgreind skilgreiningarsniðmát sem hægt er að nota. Fyrir upplýsingar um hvernig á að nota þessi sniðmát, sjá [Sniðmát fyrir skilgreiningargögn](../../dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Atburðarás þar sem skilgreiningarsniðmát geta reynst hjálpleg

Skilgreiningarsniðmát geta reynst hjálpleg í margskonar atburðarás. Hér eru nokkur dæmi:

- Þú hefur lokið og prófað skilgreiningaruppsetningu í prófunarumhverfi og þú vilt nú afrita uppsetninguna yfir í framleiðslu umhverfi.
- Þú vilt velta vöruhúsauppsetningu út til nokkurra lögaðila eða búa til nýtt vöruhús í sama lögaðila.
- Þú vilt undirbúa þig skjótt fyrir kynningu á vöruhúsvirkninni.
- Þú vilt að núverandi vörur og vöruhús noti virknina í Vöruhúsastýringu í staðinn fyrir virknina í Birgðastýringu.

Í þessu efnisatriði er lögð áherslu á fyrstu atburðarásina. Það sýnir hvernig þú getur notað skilgreiningarsniðmát til að afrita skilgreiningu á uppsetningu frá próf umhverfi yfir í framleiðslu umhverfi.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Afrita skilgreiningu á uppsetningu frá próf umhverfi yfir í framleiðslu umhverfi

Fyrir þessa atburðarás eru skilgreining á uppsetningu fyrir vöruhús og sum færsluferli nú þegar til í próf umhverfi. Þú vilt nú afrita skilgreininguna á uppsetningu fyrir vöruhús frá prófunarumhverfi yfir í framleiðslu umhverfis.

> [!NOTE]
> Það er mikilvægt að þú takir með önnur tengd uppsetningargögn þegar þú afritar skilgreiningu á uppsetningu. Til dæmis viltu setja upp vörur með því að afrita uppsetninguna úr prófunarumhverfi. Hins vegar getur þú ekki sett upp fasta tiltektarstaðsetningu fyrir vöru áður en sú vara er búin til. Þó að einstakar skilgreiningarsniðmát styðji ekki þessa tegund af ákvæðum, þá eru til sjálfgefin gagnasniðmát sem styðja hana. Þú getur auðveldlega haft þessar sjálfgefna gagnasniðmát með í skilgreiningarferli.

### <a name="export-a-default-warehouse-template"></a>Flytja út sjálfgefið vöruhúsasniðmát 

1. Opnaðu vinnusvæðið **Gagnastjórnun**.

    > [!NOTE]
    > Ef þú er að notar þetta vinnusvæði í fyrsta skipti verður þú að hlaða öllum gagnaeiningar áður en þú heldur áfram.

2. Velja **Sniðmátið** reitinn og síðan **Hlaða sjálfgefin sniðmát** til að hlaða sjálfgefnu sniðmátin.

    > [!NOTE]
    > **Hlaða sjálfgefna sniðmát** er aðeins í boði í **Aukið** yfirlit. Smellið á **Rammafæribreytur** og síðan í reitnum **Skoða sjálfgildi** skal velja **Aukið yfirlit**.

3. Eftir að sjálfgefin sniðmát eru hlaðin geturðu breytt þeim svo að þær uppfylli kröfur fyrirtækisins.

    > [!NOTE]
    > Til að hlaða sjálfgefnum sniðmátum og flytja inn sniðmát þarftu að hafa aðgang kerfisstjóra. Þessi krafa hjálpar til við að tryggja að allir einingar séu rétt hlaðnir inn í sniðmátið.

4. Vertu viss um að vera inni í lögaðilanum sem þú vilt flytja gögn tengd fyrirtækinu frá.
5. Í vinnusvæði, veldu **Flytja út**.
6. Stofna nýtt útflutningsverk.
7. Veldu **+ Bæta við sniðmáti**, og finndu **400 - WMS** sjálfgefið vöruhúsasniðmát. Þetta sniðmát bætir við gagnaeiningum fyrir vöruhúsaskilgreiningu.

    > [!NOTE]
    > Ef gögnin sem þú ert að flytja út þarf að sía (til dæmis, þú vilt aðeins flytja út gögnin sem tengjast tilteknu vöruhúsi), þú verður að meta hverja gagnaeiningu og bæta við síun í gegnum fyrirspurn. Einnig er hægt að flytja út öll gögn og eyða þeim færslum sem ekki er krafist í áfangastaðaskránum.

8. Velja **Flytja út**. Gögn sem tengjast öllum gagnaeiningum í verkinu er flutt út.

Þú getur sótt zip-skrá fyrir gagnapakkann. Þessi skrá inniheldur öll gögnin á völdu sniðinu (til dæmis Excel snið). Eins og áður hefur komið fram gæti verið að sumar færslur í gagnapakkaskránum þyrftu uppfærslu áður en hægt er að flytja þær inn í framleiðslu umhverfið. Ef þú uppfærir færslu skaltu ganga úr skugga um að þú breytir ekki skráarnafninu.

### <a name="import-a-warehouse-configuration-setup"></a>Flytja inn skilgreiningu á uppsetningu vöruhúss

1. Í áfangastaður umhverfi skaltu vera viss um að þú sért í fyrirtækið sem flytja á vöruhúsagögnin inn í.

    > [!NOTE]
    > Áður en þú framkvæmir innflutninginn ættir þú að bera kennsl á öll ákvæði milli gagna. Til dæmis inniheldur sniðmátið **Vöruhúsastýring** gagnaeiningu sem heitir **Ráðstöfunarkóðar vöruhúss**. Þessi eining inniheldur gögn sem tengjast uppsetningarsíðu **Ráðstöfunarkóðar** (**Vöruhúsastýring** > **Uppsetning** > **Fartæki** > **Ráðstöfunarkóðar**). Ef núverandi uppsetning meðhöndlar nú þegar skilaferlið fyrir sölupantanir, inniheldur reiturinn **Skilaráðstöfunarkóði** gildi. Ráðstöfunarkóðinn í þessum reit er tengdur við gagnaeiningu **Ráðstöfunarkóði**, sem er hluti af **Sölu- og markaðs** sniðmátinu. Ef gögnin úr gagnaeiningu **Ráðstöfunarkóði** eru ekki flutt inn á undan gögnin úr reitnum **Ráðstöfunarkóðar vöruhúss** mun innflutningurinn mistakast.

2. Á vinnusvæðið **Gagnastjórnun** skal velja **Innflutningur**.
3. Stofna nýtt innflutningsverk.
4. Veldu **+ Bæta við skrá** og hlaða upp zip-skránni fyrir gagnapakkann.
5. Velja **Innflutningur**. Í **Aukið** yfirlit geturðu notað **Sía** valkost til að fá snögglega yfirlit yfir vandamál sem kunna að eiga sér stað við innflutning.

**Yfirlit aðgerða** skráin veitir nákvæmar upplýsingar um hverja gagnaeiningu sem er flutt inn. Þú getur notað sviðsetningargögn yfirlitið til að komast á skömmum tíma að markgögnunum. Þannig geturðu séð hvernig innfluttu gögnin líta út á tengdum síðum í forritinu. Þegar þú notar sjálfgefin gagnasniðmát, virkar innflutningsröðin fyrir hverja gagnaeiningu á fyrirfram ákveðinni hátt, til að tryggja að öll háð gögn séu flutt inn fyrst. Ef sérsniðin gagnaeiningar eru hluti af verkinu, verður þú að ganga úr skugga um að rétta röðin sé skilgreind. Nánari upplýsingar, sjá [Gagnasniðmát skilgreiningar](../../dev-itpro/data-entities/configuration-data-templates.md).

Til að fræðast betur um hvernig á að nota sniðmát vöruhúss til að afrita skilgreiningar vöruhúss frá einu fyrirtæki til nýs fyrirtækis innan sama tilviks er hægt að horfa á þetta þriggja mínútna myndband á YouTube um [hvernig nota skuli sniðmát vöruhúss til að afrita skilgreininguna í Finance and Operations](https://www.youtube.com/watch?v=K2WIfFlqJYs).

## <a name="related-topic"></a>Tengt efni

[Sniðmát skilgreiningargagna](../../dev-itpro/data-entities/configuration-data-templates.md)
