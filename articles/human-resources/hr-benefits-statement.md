---
title: Yfirlit yfir fríðindi
description: Skýrslan um bótayfirlit útskýrir fríðindin sem starfsmaður er skráður í.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 602e4f9459aac8fdbea5f2752e51cc2c1b71360c
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358244"
---
# <a name="benefit-statement"></a>Yfirlit yfir fríðindi


[!INCLUDE [PEAP](../includes/peap-2.md)]

Skýrslan **Yfirlit yfir fríðindi** gefur upp yfirlit yfir fríðindi sem starfsmaður er skráður í. Starfsmaður getur sjálfur nálgast skýrsluna eða í gegnum fríðindastjórnanda. **Yfirlit yfir fríðindi** gefur upp lista yfir skráð fríðindi starfsmanns, tryggingarvalkosti, kostnað og skráða aðstandendur eða rétthafa. Yfirlitið er hægt að prenta fyrir einn starfsmann eða marga starfsmenn.

> [!NOTE]
Eiginleikinn **Yfirlit yfir fríðindi** verður að vera virkjaður á vinnusvæðinu **Eiginleikastjórnun**. Til þess að gera þetta þarf að vera kveikt á eiginleikanum **Stjórnun fríðinda** í eiginleikastjórnun. 


## <a name="importing-the-benefit-statement"></a>Yfirlit yfir fríðindi flutt inn 

Þú verður að flytja inn **Yfirlit yfir fríðindi** með skýrsluskilgreiningu áður en **Yfirlit yfir fríðindi** verður gert aðgengilegt. Til að gera þetta þarf að ljúka eftirfarandi skrefum:

1.  Opnaðu vinnusvæði **Kerfisstjórnunar**.

2.  Veldu reitinn **Rafræn skýrslugerð**.

3.  Opnaðu **Skilgreiningarveitur** og veldu **Gagnageymslur**.

  ![Val á gagnageymslum.](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  Veldu **Tilföng mannauðs** úr listanum og veldu svo **Opna**.

    ![Gagnasöfn skilgreiningar.](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  Veldu **Líkan fríðindayfirlits** vinstra megin og stækkaðu það þannig að **Snið fríðindayfirlits** sjáist.

6.  Veldu **Snið fríðindayfirlits** vinstra megin.

7.  Hægra megin á skjánum mun sjást flýtiflipinn **Útgáfur**. Velja **Innflutningur**.

    ![Flýtiflipi útgáfa.](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Búa til fríðindayfirlit sem PDF-skrá

**Yfirlit yfir fríðindi** verður sjálfgefið prentað sem Microsoft Word-skjal. Til að prenta á PDF-sniði þarftu að stilla PDF-valkostinn í **Viðtökustaður rafrænnar skýrslugerðar**. 

1. Til að gera þetta skaltu fara í **Vinnusvæði kerfisstjórnunar** > **Rafræn skýrslugerð** > **Tengdir tenglar** > **Viðtökustaður rafrænnar skýrslugerðar**.

1.  Veljið **Nýtt**.

2.  Í reitnum **Tilvísun** skal velja **Snið fríðindayfirlits**.

3.  Í flýtiflipanum **Viðtökustaður skráar** skal velja **Nýr**.

4.  Í reitinn **Heiti** skal færa inn **PDF-skjal fríðindayfirlits**.

5.  Í reitnum **Heiti skráaríhlutar** skal velja **Yfirlit yfir fríðindi**.

6.  Veldu gátreitinn **Umbreyta í PDF-skjal**.

7.  Veldu **Stillingar** úr valmyndaratriðinu. 

    ![Viðtökustaður skráar.](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  Veldu flýtiflipann **Skrá** og veldu svo **Virkjað**.

9.  Veldu **Í lagi**.
   
> [!NOTE]
> Eiginleiki fríðindastjórnunar er í stöðu forútgáfu. Þekkt vandamál er til staðar þegar stilling á viðtökustað tölvupósts er notuð í skýrslunni **Viðtökustaður rafrænnar skýrslugerðar**. Þú gætir fengið villuboð og ekki verður hægt að senda tölvupóstinn.

**Yfirlit yfir fríðindi** er hægt að búa til á eftirfarandi síðum:

-   **Vinnusvæði fríðindastjórnunar** > **Tenglar** > **Skýrslur** > **Yfirlit yfir fríðindi**

-   **Starfsmenn (eldri skjámynd)** > **Flipi persónuupplýsinga** > **Fríðindayfirlit**

-   **Einfölduð starfsmannafærsla** > **Skýrsla um fríðindi** > **Fríðindayfirlit**

-   **Sjálfsafgreiðsla starfsmanns** > **Fríðindi** > **Skoða fríðindayfirlit**

> [!NOTE]
>  Aðgangi að **Yfirlit yfir fríðindi** í **Sjálfsafgreiðslu starfsmanns** er stýrt af réttindunum **Skoða yfirlit yfir fríðindi**. Þetta er undir aðgangsheimildinni **Fríðindi sjálfsafgreiðslu starfsmanna**. Starfsmönnum er sjálfkrafa veitt þessi réttindi.

## <a name="report-contents"></a>Innihald skýrslu

**Yfirlit yfir fríðindi** mun prenta út staðfest áætlunarval starfsmanns, þ.m.t. niðurfelldar áætlanir. Eftirfarandi mynd sýnir dæmi um þessa skýrslu. 

![Skýrsla fríðindayfirlits.](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

Í skýrslunni birtist **Áætlun**, **Tryggingarvalkostur**, **Kostnaður starfsmanns** og **Kostnaður vinnuveitanda**. Í skýrslunni verða einnig tryggðir aðstandendur taldir upp. Ef áætlunin er með rétthafa tengda henni verða rétthafar og forgangur úthlutunar og prósenta hennar einnig sýnd.

Hægt er að prenta út skýrslu **Fríðindayfirlits** fyrir marga starfsmenn samtímis með því að nota flýtiflipann **Færslur til að taka með** á síðunni **Yfirlit yfir fríðindi**.
