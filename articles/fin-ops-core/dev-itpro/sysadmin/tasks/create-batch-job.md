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
ms.translationtype: MT
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
3. Í **Starfslýsing** reit, sláðu inn lýsingu á runuvinnunni.
4. Í **Áætlaður upphafsdagur/tími** reit, sláðu inn dagsetningu og tíma þegar runuvinnan á að keyra.
5. Veldu **Vista**.

## <a name="create-a-recurrence"></a>Stofna endurtekningu
1. Á aðgerðarrúðunni velurðu **Lotuvinna**.
2. Veljið **Endurtekning**. Notið þessa valkosti til að færa inn afmörkun og mynstur fyrir endurtekninguna.  
3. Veldu **Í lagi**.

## <a name="add-alerts"></a>Bæta við viðvaranir
1. Á aðgerðarrúðunni velurðu **Lotuvinna**.
2. Veldu **Viðvaranir**. Tilgreina hvort óskað sé eftir að viðvörunarboðin birtist þegar runuvinnsla lýkur, villa er til staðar eða hætt er við. Tilgreinið síðan ef óskað er eftir að viðvaranir birtist sem sprettigluggar.   
3. Veldu **Í lagi**.

## <a name="add-a-task-to-a-batch-job"></a>Verki bætt við runuvinnslu
1.  Á **Lotustörf** síðu, veldu **Skoða verkefni**.
2.  Veldu **Ctrl+N** að búa til verkefni.
3.  Færið inn lýsingu á lotuverkefninu.
4.  Í **Reikningar fyrirtækja** reit, veldu fyrirtækjagagnagrunninn sem verkefnið á að keyra í.
5.  Í **Nafn bekkjar** reit, veldu ferlið sem verkefnið á að keyra. 
6.  Eftir því sem við á skaltu velja runuhóp fyrir verkefnið.

    Verkefni viðskiptavina verða að vera úthlutað til runuhóps. Þeim er sjálfkrafa úthlutað í sjálfgefna runuhópinn (einnig þekktur sem tómur runuhópurinn).

7.  Veldu **Ctrl+S** til að vista verkefnið.
8.  Til að gera valið verkefni háð öðru verki í verkinu skaltu velja **Hefur skilyrði** rist, og fylgdu síðan þessum skrefum fyrir hvert skilyrði sem þú vilt skilgreina:

    1. Veldu **Ctrl+N** að skapa skilyrði.
    2. Veldu verkefnakenni móðurverkefnisins.
    3. Veldu stöðuna sem yfirverkefnið verður að ná áður en háða verkið getur keyrt.
    4. Veldu **Ctrl+S** til að bjarga ástandinu.

    Ef þú skilgreinir fleiri en eitt skilyrði, og ef *allt* skilyrðin verða að vera uppfyllt áður en háða verkefnið getur keyrt, veldu skilyrðistegund af **Allt**. Ef háð verkefni getur keyrt eftir *Einhver* af skilyrðunum hefur verið uppfyllt, veldu skilyrðistegund af **Einhver**.

9.  Veldu hvernig verkefnabilanir á að meðhöndla. Til að hunsa bilun tiltekins verkefnis, á **Almennt** flipann, veldu **Hunsa verkefnabilun** valmöguleika fyrir það verkefni. Ef þessi valkostur er valinn mun bilun í verkinu ekki valda því að verkið mistekst. Þú getur líka notað **Hámarkstilraunir** reit til að tilgreina fjölda skipta sem endurtaka ætti verkefni áður en það er talið hafa mistekist. Sem besta starfsvenjan mælum við með að þú stillir ekki **Hámarkstilraunir** reit að gildi sem er meira en **5**.

    Fyrir frekari upplýsingar um endurtekningarlotu, sjá [Virkjaðu endurtekna hóptilraunir](../retryable-batch.md).

## <a name="adjust-batch-job-status"></a>Stilla stöðu runuvinnslu
1. Farðu í **Kerfisstjórnun > Fyrirspurnir> Runuvinnslur**.
2. Veldu viðeigandi runuvinnslu.
3. Á aðgerðarrúðunni velurðu **Lotuvinna > Aðgerðir > Breyta stöðu**.
4. Veldu viðeigandi stöðu:
    - **Halda eftir**: Stilla runuvinnsluna sem **halda eftir** svo að henni er haldið eftir í verkraðara runuvinnslu. Jafngildir *stöðva*.
    - **Bið**: Stilla runuvinnsluna sem **bið** svo að hún bíður þess að verkraðari runuvinnslu taki hana til. Jafngildir *ræsa*.
5. Veldu **Í lagi**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
