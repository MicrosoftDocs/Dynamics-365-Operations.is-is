---
title: Stofna runuvinnslu
description: Runuvinnsla er flokkur verka sem er sendur til AOS-tilviksins (hugbúnaðarhlutarþjónstilviks) í sjálfvirka vinnslu.
author: matapg007
ms.date: 11/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
ms.openlocfilehash: 06fb9a18e70c316be97645ba76f9462cd3ccc729
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292451"
---
# <a name="create-a-batch-job"></a>Stofna runuvinnslu

[!include [banner](../../includes/banner.md)]

Runuvinnsla er flokkur verka sem er sendur til AOS-tilviksins (hugbúnaðarhlutarþjónstilviks) í sjálfvirka vinnslu. Runuvinnslur er keyrðar með því að nota öryggis- og notendaheimildir þess notanda sem stofnaði verkið. Fylgið eftirfarandi ferli ef stofna á runuvinnslu. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-the-batch-job"></a>Stofna runuvinnslu
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Fyrirspurnir > Runuvinnslur**.
2. Veljið **Nýtt**.
3. Í reitinn **Verklýsing** er færð stutt lýsing á runuvinnslunni.
4. Í reitinn **Áætluð upphafsdagsetning/-tími** skal færa inn dagsetningu og tíma þegar runuvinnslan á að vera keyrð.
5. Veldu **Vista**.

## <a name="create-a-recurrence"></a>Stofna endurtekningu
1. Veldu **Runuvinnsla** á aðgerðasvæðinu.
2. Veljið **Endurtekning**. Notið þessa valkosti til að færa inn afmörkun og mynstur fyrir endurtekninguna.  
3. Veldu **Í lagi**.

## <a name="add-alerts"></a>Bæta við viðvaranir
1. Veldu **Runuvinnsla** á aðgerðasvæðinu.
2. Veljið **Viðvaranir**. Tilgreina hvort óskað sé eftir að viðvörunarboðin birtist þegar runuvinnsla lýkur, villa er til staðar eða hætt er við. Tilgreinið síðan ef óskað er eftir að viðvaranir birtist sem sprettigluggar.   
3. Veldu **Í lagi**.

## <a name="add-a-task-to-a-batch-job"></a>Verki bætt við runuvinnslu
1.  Á síðunni **Runuvinnslur** skaltu velja **Skoða verkefni**.
2.  Veldu **Ctrl+N** til að búa til verkefni.
3.  Færðu inn lýsingu á runuverkinu.
4.  Í reitnum **Fyrirtækjareikningar** skal velja þann fyrirtækjagagnagrunninn sem á að keyra verkefnið í.
5.  Í svæðinu **Klasaheiti**, veljið það ferli sem verkið á að keyra. 
6.  Eftir því sem við á, veljið runuflokk fyrir verkið.

    Biðlaraverkefnum verður að úthluta í runuflokk. Þeim er sjálfkrafa úthlutað til sjálfgefins runuflokks (einnig þekktur sem tómur runuflokkur).

7.  Veljið **Ctrl + S** til að vista verkið.
8.  Til að gera valið verk háð öðru verki í vinnslunni, veljið **Hefur skilyrði** og fylgið síðan eftirfarandi skrefum fyrir hvert skilyrði sem þið viljið skilgreina:

    1. Veldu **Ctrl+N** til að búa til skilyrði.
    2. Veljið auðkenni verks sem tilheyrir yfirverkinu.
    3. Veljið stöðuna sem yfirverkið verður að ná áður en hægt er að keyra hið tengda undirverk.
    4. Veljið **Ctrl + S** til að vista skilyrðið.

    Ef fleiri en eitt skilyrði hafa verið skilgreind og ef mæta verður *öllum* skilyrðum áður en hægt er að keyra tengda verkið, veljið tegund skilyrðis sem **Allt**. Ef hægt er að keyra tengda verkið eftir að *einhverju* skilyrðanna hefur verið fullnægt, veljið skilyrðistegund **Eitthvað**.

9.  Veljið hvernig brugðist skuli við misheppnuðum verkum. Til að hunsa þegar tiltekið verk mistekst, á flipanum **Almennt** skal velja valkostinn **Hunsa verkefnismistök** fyrir það verk. Ef þessi valkostur er valinn mun misfella í verki ekki valda því að verkefnið mistakist. Einnig er hægt að nota reitinn **Hámark tilrauna** til að tilgreina þann fjölda tilrauna sem gera skal til að framkvæma verkefni áður en það telst hafa mistekist. Þess vegna mælum við með því að stilla gildið fyrir reitinn **Hámark tilrauna** ekki á hærra gildi en **5**.

    Frekari upplýsingar um endurteknum runum eru í [Gera runutilraunir virkar](../retryable-batch.md).

## <a name="adjust-batch-job-status"></a>Stilla stöðu runuvinnslu
1. Farðu í **Kerfisstjórnun > Fyrirspurnir> Runuvinnslur**.
2. Veldu viðeigandi runuvinnslu.
3. Veldu **Runuvinnsla > >Virkni > Breyta stöðu** á aðgerðasvæðinu.
4. Veldu viðeigandi stöðu:
    - **Halda eftir**: Stilla runuvinnsluna sem **halda eftir** svo að henni er haldið eftir í verkraðara runuvinnslu. Jafngildir *stöðva*.
    - **Bið**: Stilla runuvinnsluna sem **bið** svo að hún bíður þess að verkraðari runuvinnslu taki hana til. Jafngildir *ræsa*.
5. Veldu **Í lagi**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
