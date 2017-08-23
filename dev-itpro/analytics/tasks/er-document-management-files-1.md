--- 
title: "Undirbúa gagnalíkan til að nota skjalastjórnunarskrár fyrir snið frálags í rafrænni skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cc0909f99be9aad1b6bec22d4ed10381e0484a41
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Undirbúa gagnalíkan til að nota skjalastjórnunarskrár fyrir snið frálags í rafrænni skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Fá aðgang að lista yfir skilgreiningar sem Microsoft veitir
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Gakktu úr skugga um að „Litware, Inc.“ veitandi sé tiltæk og merkt Virk.  
2. Velja Litware, Inc. veita.
3. Smella á Geymslur.
    * Sleppa önnur þrep í núverandi undirverki ef gagnasafn af gerð 'Rekstrartilföngum' er þegar til.  
4. Smelltu á Bæta við til að opna felligluggann.
5. Í reitnum gerð gagnasafns fyrir skilgreiningar, færðu inn "rekstrartilföng".
6. Smellið á Stofna gagnasafn.
7. Smellið á „Í lagi“.

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Sækja Líkan Reiknings viðskiptavinar-skilgreiningar sem Microsoft veitir
1. Smellt er á Sýna síur.
2. Nota eftirfarandi síur: færið Inn gildi síu "Rekstrartilföngum" síu á svæðið "Heiti" með því að nota í "byrjar á" virknitákn síu; Færa inn gildi síu "" á reitnum "Lýsing" með því að nota "byrjar á" virknitákn síu.
3. Smellt er á Sýna síur.
4. Smellt er á Opin.
5. Í trénu, veljið 'Customer invoice model'.
    * Velja skilgreiningu líkans 'líkan reiknings viðskiptavinar' til að flytja það inn.  
6. Smelltu á Flytja inn.
    * Smelltu á innflutning fyrir útgáfu 1 fyrir valda skilgreiningu.  
7. Smella á Já.
8. Lokið síðunni.
9. Lokið síðunni.
10. Smelltu á Grunnstillingar skýrslugerðar
11. Í trénu, veljið 'Customer invoice model'.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Stofna afleitt líkan til að styðja aðgang að skrám Skjalastjórnunar.
    * Þú munt stofna okkar eigin skilgreiningu á líkani reiknings viðskiptavinar og fá það úr skilgreiningu sem Microsoft veitir. Þú munt nota þessa skilgreiningu til að innleiða aðgang að skrám Skjalastjórnunar og gera þau tiltæk fyrir rafræn skjöl sem þú munt stofna á grundvelli þessa líkans.  
1. Smellt er á stofna skilgreiningu til að opna fellilistanum.
2. Í svæðinu Nýtt, veljið 'Leiða af nafni: líkan reiknings viðskiptavinar, Microsoft'.
3. Í svæðið Heiti, Færðu inn 'líkan reiknings viðskiptavinar (sérstillt)'.
    * Líkan Reiknings viðskiptavinar (sérstillt)  
4. Smelltu á Stofna skilgreiningu.


