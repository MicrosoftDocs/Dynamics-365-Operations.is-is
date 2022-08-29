---
title: Ljúka við, birta og setja upp altækan eiginleika
description: Þessi grein veitir upplýsingar um líftíma hnattvæðingareiginleika.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 11378991a24e1a5f5e213d64f0f414db2e5c2573
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279901"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Ljúka við, birta og setja upp altækan eiginleika

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Útgáfur fyrir eiginleika rafrænna reikninga

Aðgerðir rafrænna reikninga eru útfærðar. Þegar ný útgáfa er búin til hækkar útgáfunúmerið sjálfkrafa.

Eiginleikaútgáfur rafrænnar reikningsfærslu fylgja stuðningstíma sem er með allt að þrjár stöður:

- **Drög** – Þegar eiginleikaútgáfa hefur þessa stöðu geturðu breytt stillingareiginleikum hennar og gripum (til dæmis stillingum skráarsniðs).
- **Heill** – Þessi staða gefur til kynna að þú hafir lokið við að breyta eiginleika útgáfunni og ætlar ekki að gera fleiri uppfærslur á henni. Þegar eiginleikaútgáfa hefur þessa stöðu geturðu ekki lengur breytt henni eða einhverjum af íhlutum hennar.
- **Birt** – Þessi staða gefur til kynna að eiginleikaútgáfan hafi verið birt í alþjóðlegu geymslunni sem tengist fyrirtækinu þínu. Þegar eiginleikaútgáfa hefur þessa stöðu geturðu ekki lengur breytt henni eða einhverjum af íhlutum hennar.

Þú getur tilgreint an **Gildir frá** dagsetningu fyrir nýja útgáfu af eiginleikum rafrænna reikninga. Á þennan hátt er hægt að skilgreina sjálfgefna útgáfu sem hægt er að nota, eða sem hægt er að skrifa yfir þegar eiginleikinn er settur í þjónustuumhverfið.

Fylgdu þessum skrefum til að breyta stöðu eiginleika útgáfu rafrænna reikninga.

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Vinstra megin við **Eiginleikar rafrænna reikninga** síðu, veldu rafræna reikningseiginleikann.
4. Á **Útgáfur** flipann hægra megin á síðunni, veldu útgáfuna.
5. Veldu **Breyta stöðu**, og veldu síðan **Heill** (ef núverandi staða er **Drög**) eða **Birt** (ef núverandi staða er **Heill**).
6. Veldu í skilaboðareitnum **Já** til að staðfesta beiðnina.

Handbók breyting frá **Heill** stöðu til **Birt** staða er valkvæð. Útgáfur rafrænna reikningaeiginleika eru sjálfkrafa uppfærðar í **Birt** stöðu þegar þeim er dreift í þjónustuumhverfið.

Þú getur fylgst með stöðunni í **Staða eiginleika útgáfu** dálki á **Útgáfur** flipa.

## <a name="deploy-feature-versions"></a>Settu upp eiginleikaútgáfur

Í RCS notarðu **Dreifa** skipun til að birta eiginleika útgáfu rafrænna reikninga í markþjónustuumhverfið eða tengda forritið.

1. Vinstra megin við **Eiginleikar rafrænna reikninga** síðu, veldu rafræna reikningseiginleikann.
2. Á **Útgáfur** flipann hægra megin á síðunni, veldu útgáfu rafrænna reikningaeiginleika sem þú vilt nota í þjónustuumhverfið eða tengda forritið. Valin útgáfa verður að hafa stöðuna **Heill** eða **Birt**.
3. Veldu **Dreifa**, og veldu síðan einn eða báða eftirfarandi valkosta til að skilgreina markmið dreifingarinnar:

    - **Tengt forrit** – Stillingin sem fylgir uppsetningu forritsins er skrifuð í tilviki af Microsoft Dynamics 365 Fjármál eða Dynamics 365 Supply Chain Management sem áður var tengdur því.
    - **Þjónustuumhverfi** – Útgáfa rafrænna innheimtuaðgerða er notuð í þjónustuumhverfið. Rafrænn reikningur er þá tilbúinn til að taka á móti og vinna úr rafrænum skjölum sem fjármála- eða birgðakeðjustjórnun sendir.

> [!NOTE]
> Venjulega muntu breyta færibreytum rafrænnar skýrslugerðar (ER) eiginleikans sem þarf að nota í þjónustuumhverfið. Breytingar á tengdu forriti verða sjaldgæfar. Þú ættir aðeins að dreifa nýjum útgáfum á tengda forritið þegar þú breytir samsvarandi breytum forritsins þíns.

Til að ákvarða hvort tiltekin útgáfa af eiginleikum rafrænna reikninga sé notuð í tiltekið umhverfi, skoðaðu upplýsingarnar á **Umhverfi** flipa.

## <a name="remove-feature-versions"></a>Fjarlægðu eiginleika útgáfur

Í RCS geturðu valið **Hætta við** að fjarlægja tiltekna útgáfu rafrænna reikningaeiginleika úr þjónustuumhverfi, ef hún var notuð þar.

> [!IMPORTANT]
> The **Hætta við** hnappur virkar aðeins fyrir þjónustuumhverfi. Það fjarlægir ekkert úr tengdu forritinu fyrir núverandi rafræna reikningseiginleika.

## <a name="rebase-electronic-invoicing-features"></a>Endurbæta eiginleika rafrænna reikninga

Þegar einn eiginleiki rafrænna reikninga er fenginn frá öðrum geturðu valið **Endurbasa** að uppfæra afleidda eiginleikann með þeim breytingum sem hafa verið gerðar á upprunalega (foreldri) eiginleikanum.

Til að endurbæta afleidda útgáfu af eiginleika sem þú bjóst til skaltu fylgja þessum skrefum.

1. Fáðu nýjustu útgáfuna af eiginleikanum með því að flytja hann inn úr alþjóðlegu geymslunni. Fyrir frekari upplýsingar, sjá [Flytja inn eiginleiki frá alþjóðlegri geymslu](e-invoicing-import-feature-global-repository.md).
2. Í listanum yfir eiginleika skal velja eiginleikann sem á að endurreikna grunn fyrir.
3. Á **Útgáfur** flipa, veldu **Nýtt** til að búa til drög að útgáfu.
4. Veldu **Endurreikna grunn**.
5. Í **Endurbasa** valmynd, veldu útgáfu eiginleikans sem þú vilt endurbyggja á.
6. Veldu **Í lagi**.
7. Farið yfir íhluti eiginleikans og gerið allar nauðsynlegar breytingar.
8. Veljið **Breyta stöðu** til að ljúka við eiginleika með endurreiknaðan grunn. Þegar endurreikning grunns er lokið er hægt að framkvæma fleiri aðgerðir.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Fáðu sérstaka útgáfu af eiginleikum rafrænna reikninga

Þegar þú býrð til nýja útgáfu af eiginleikum rafrænna reikninga, býr kerfið til afrit af nýjustu eiginleikaútgáfunni. Til að nota eldri útgáfu af eiginleikanum sem grunn fyrir nýja útgáfu skaltu velja útgáfuna og svo **Fáðu þessa útgáfu skipun**. Ný drög að útgáfu eiginleikans eru búin til sem er afrit af völdu útgáfunni.
