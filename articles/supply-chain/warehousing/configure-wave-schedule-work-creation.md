---
title: Áætla stofnun vinnu í bylgju
description: Þetta efnisatriði lýsir því hvernig á að setja upp og nota vinnsluaðferð bylgju fyrir áætla stofnun vinnu.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078272"
---
# <a name="schedule-work-creation-during-wave"></a>Áætla stofnun vinnu í bylgju

[!include [banner](../includes/banner.md)]

Notið eiginleikann *Áætla stofnun vinnu* sem hluta af bylgjuferlinu til að auka gegnumstreymi bylgjuvinnslu með því að láta kerfið stofna vinnu með samhliða vinnslu.

Þegar aðgerðin er virkjuð verður áætluð vinna stofnuð sjálfkrafa sem kerfið mun að lokum vinna úr til að stofna raunverulega vinnu. Ef fjöldi hleðslulína bylgju nær fyrirframskilgreindum þröskuldi mun kerfið stofna raunverulega vinnu á fljótlegri hátt með því að nota samhliða, ósamstillta vinnslu.

## <a name="enable-the-schedule-work-creation-feature"></a>Virkja eiginleikann Áætlun stofnun vinnu

### <a name="enable-the-feature-in-feature-management"></a>Virkjun eiginleika í eiginleikastjórnun

Áður en hægt er að nota eiginleikann *Áætla stofnun vinnu* verður að vera kveikt á honum í kerfinu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Áætla stofnun vinnu*

> [!NOTE]
> Eiginleikinn *Vinnulokun fyrir allt fyrirtækið* verður að vera virkur áður en hægt er að virkja *Áætla stofnun vinnu*.

### <a name="manually-enable-batch-processing-of-waves"></a>Virkja handvirkt runuvinnslur fyrir bylgjur

Til að nýta sér samhliða ósamstillta aðferð til að stofna vöruhúsavinnu verður bylgjuferlið að vera keyrt í runu. Til að setja þetta upp:

1. Farðu í  **Vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.

1. Í flipanum **Almennt** skal stilla **Vinna bylgjur í runu** á *Já*. Einnig er hægt að velja sérstakan **Runuflokk bylgjuvinnslu** til að koma í veg fyrir að úrvinnsla runubiðraðar verði keyrð á sama tíma og önnur ferli.

1. Stillið **Biðtími læsingar (ms)** sem verður notaður þegar kerfið vinnur úr nokkrum bylgjum samtímis. Fyrir flest stærri bylgjuferli er mælt með gildinu *60000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Virkja nýja bylgjuskrefsaðferð handvirkt fyrir fyrirliggjandi bylgjusniðmát

Byrjið á því að stofna nýja bylgjuskrefsaðferð og virkið hana fyrir ósamstillta verkvinnslu.

1. Farið í  **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.

1. Veljið  **Endurgera aðferð** og athugið að *WHSScheduleWorkCreationWaveStepMethod* hefur verið bætt við listann yfir aðferðir bylgjuferlis sem hægt er að nota í bylgjusniðmátum sendingar.

1. Veljið færsluna með **Heiti aðferðar** *WHSScheduleWorkCreationWaveStepMethod* og veljið **Verkskilgreiningu**.

1. Til að bæta nýrri línu við hnitanetið skal velja **Ný** á aðgerðasvæðinu og nota eftirfarandi stillingar:

    - **Vöruhús** - Veljið vöruhúsið sem nota á til að tímasetja vinnslu á stofnun vinnu.

    - **Hámarksfjöldi runuverka** - Tilgreinið hámarksfjölda runuverka. Í flestum tilfellum ætti þetta gildi að vera á bilinu 8-16, hins vegar mælum við með því að þið prófið ykkur áfram til að finna út bestu stillinguna fyrir ykkar aðstæður.

    - **Runuflokkur bylgjuvinnslu** - Veljið sérstakan runuflokk bylgjuvinnslu til að fínstilla vinnslu runubiðraðar.

Nú er hægt að uppfæra fyrirliggjandi bylgjusniðmát (eða búa til nýtt) til að nota bylgjuvinnsluaðferðina *Áætla stofnun vinnu*.

1. Fara í  **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.

1. Á aðgerðarúðunni skal velja **Breyta**.

1. Á listasvæðinu skal velja bylgjusniðmátið sem á að uppfæra (ef verið er að prófa með sýnigögnum, þá er hægt að nota *24 Sjálfgefin sending*).

1. Stækkið flýtiflipann **Aðferðir** og veljið línuna með **Heitinu** *Áætla stofnun vinnu* í hnitanetinu **Eftirstandandi aðferðir**.

1. Veljið örina sem vísar í **Valdar aðferðir** til að fara valda línu í þeim dálki. (Aðeins er hægt að hafa eina valda aðferð í einu sem notar annaðhvort *WHSScheduleWorkCreationWaveStepMethod* eða *createWork* þannig að fyrirliggjandi lína með **Heiti aðferðar** *createWork* færist sjálfkrafa í hnitanetið **Eftirstandandi aðferðir**.)

## <a name="set-wave-task-processing-threshold-data"></a>Stilla þröskuldsgögn fyrir úrvinnslu bylgjuverks

Kerfið stofnar sjálfgefin þröskuldsgögn fyrir úrvinnslu bylgjuverks í fyrsta skipti sem bylgjuferli er keyrt með því að nota einhverja verktengda vinnslu. Gögnin eru notuð til að stjórna því hvenær bylgjuvinnsla mun keyra ósamstillt og vera tengd verki, sem gerir henni kleift að vinna úr og stofna vinnu samhliða.

Sjálfgefin gögn munu í upphafi nota þröskuldsgildið 15 fyrir lágmarksfjölda hleðslulína (MINIMUMWAVELOADLINES). Þetta þýðir að þegar kerfið vinnur úr bylgju með fleiri en 15 hleðslulínum notar það ósamstæða verkvinnslu. Hægt er að setja inn/uppfæra þessi gögn handvirkt í töflunni **WHSWaveTaskProcessingThresholdParameters** í prófunarumhverfinu, en ef breyta þarf þessari stillingu í vinnsluumhverfi verður að hafa samskipti við notendaþjónustu Microsoft til að óska eftir uppfærslunni.

## <a name="work-with-the-feature"></a>Unnið með eiginleikann

Þegar aðgerðin *Áætla stofnun vinnu* er virkjuð mun bylgjuvinnsla stofna áætlaða vinnu sem verður á endanum notuð af nýju stofnferli vinnu. Við stofnun vinnu verður lokað fyrir vinnu með því að nota eiginleikann *Vinnulokun fyrir allt fyrirtækið*.

Eftirfarandi flæðirit sýnir hvernig áætluð vinna er stofnuð við bylgjuvinnslu.

![Áætla stofnun vinnu](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>áætluð vinna

Síðan **Upplýsingar um áætlaða vinnu** (**Vöruhúsakerfi \> Vinna \> Upplýsingar um áætlaða vinnu**) sýnir upplýsingar um áætlaða vinnu sem er upphaflega stofnuð í bylgjuvinnslu. Eftirtalin **Staða ferlis** gildi eru tiltæk:

- **Í biðröð** - Áætluð vinna bíður þess að vera notuð til að stofna vinnu.
- **Lokið** – Áætluð vinna hefur verið notuð til að stofna vinnu.
- **Mistókst** – Ekki tókst að vinna bylgjuna. Athugið að áætluð vinna getur verið í stöðu sem **Mistókst** með eða án tengdrar raunvinnu. Þegar stofnferli raunverulegrar vinnu tekst ekki helst raunveruleg vinna í stöðunni *Hætt við*.

### <a name="batch-job-for-the-work-creation-process"></a>Runuvinnsla fyrir stofnferli vinnu

Til að skoða runuvinnslur fyrir vinnslubylgjur skal velja **Runuvinnslur** á aðgerðasvæðinu á **Allar bylgjur** síðunni.

Héðan er hægt að skoða allar upplýsingar um runuverk fyrir hvert runuvinnslukenni.
