---
title: "Hlaða niður Grunnstillingar fyrir rafræna skýrslugerð úr Lifecycle Services"
description: "Í þessu efnisatriði er útskýrt hvernig á að sækja Rafræna skýrslugerð skilgreiningar (ER) úr Microsoft Dynamics Lifecycle Services (LCS)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Hlaða niður Grunnstillingar fyrir rafræna skýrslugerð úr Lifecycle Services

Í þessu efnisatriði er útskýrt hvernig á að sækja Rafræna skýrslugerð skilgreiningar (ER) úr Microsoft Dynamics Lifecycle Services (LCS).

Þetta kennsluefni leiðbeinir þér við ferli til að sækja nýjustu útgáfu forstillinga Rafræna skýrslugerð (ER) úr Microsoft Dynamics Lifecycle Services (LCS).

1.  Skráðu þig inn á Dynamics 365 for Operations með því að nota eitt af eftirfarandi hlutverkum:
    -   Þróunaraðili rafrænnar skýrslulausnar
    -   Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    -   Kerfisstjóri

2.  Fara í **fyrirtækisstjórnun**&gt;**Rafræna skýrslugerð**.
3.  Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Microsoft**
4.  Á **Microsoft** gluggareit, er smellt á **gagnasöfn**. [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  Á **gagnasöfn skilgreininga ** síðu í hnitanetinu skal velja fyrirliggjandi gagnasafn af gerðinni **LCS** . Ef þessi gagnasafn birtist ekki í hnitanetinu skal fylgja þessum skrefum:
    1.  Smelltu á **Bæta við ** til að bæta við nýju gagnasafni.
    2.  Veljið **LCS ** sem gerð gagnasafns.
    3.  Smellið á **Stofna gagnasafn**.
    4.  Færa skal inn heiti og lýsingu fyrir gagnasafn.
    5.  Smellið á **í lagi** til að staðfesta nýja færslu gagnasafns.
    6.  Í hnitanetinu, veljið nýtt gagnasafn af gerðinni **LCS** .

6.  Smellið á **Opna** til að skoða lista yfir skilgreiningar rafrænnar skýrslugerðar (ER) fyrir valda gagnasafn. [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Í skilgreiningatrénu í vinstri rúðunni er valið skilgreining ER sem þig vantar.
8.  Á flýtiflipanum **Útgáfur** skal velja nauðsynlega útgáfu skilgreiningar rafrænnar skýrslugerðar.
9.  Smellið á **Innflutning** til að sækja valda útgáfu úr LCS í núverandi tilvik Dynamics 365 for Operations. **Athugasemd:** **Innflutnings** hnappurinn er ekki tiltækur fyrir útgáfur skilgreininga rafrænnar skýrslugerðar sem þegar eru til staðar í gildandi tilvik Dynamics 365 for Operations. [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Athugasemd:** eftir stillingum rafrænnar skýurslugerðar, eru skilgreiningar villuleituð eftir að þau eru flutt inn. Notandi gæti verið látinn vita um vandamál ósamræmi sem fundust. Leysa þarf úr vandamálunum áður en hægt er að nota innflutta útgáfu skilgreiningu. Nánari upplýsingar, sjá lista yfir tengdar greinum fyrir þetta viðfangsefni.

<a name="see-also"></a>Sjá einnig
--------

[Yfirlit yfir Rafræna skýrslugerð](general-electronic-reporting.md)


