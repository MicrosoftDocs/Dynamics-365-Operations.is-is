---
title: Ljúka við, birta og setja upp altækan eiginleika
description: Í þessari grein er að finna upplýsingar um stuðningstíma altækra eiginleika.
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
ms.openlocfilehash: 9d4a408f2169b220fefd9ab7e9f3b37217fb3cfe
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710836"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Ljúka við, birta og setja upp altækan eiginleika

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Eiginleikaútgáfur rafrænnar reikningsfærslu

Eiginleikar rafrænnar reikningsfærslu fá úthlutað útgáfu. Þegar ný útgáfa er búin til hækkar útgáfunúmerið sjálfkrafa.

Eiginleikaútgáfur rafrænnar reikningsfærslu fylgja stuðningstíma sem er með allt að þrjár stöður:

- **Drög** – Þegar útgáfa eiginleika hefur þessa stöðu er hægt að breyta skilgreiningareigindum og gervingum hennar (til dæmis skilgreiningum skráarsniðs).
- **Lokið** – Þessi staða gefur til kynna að þú hafir lokið við að breyta útgáfu eiginleikans og ætlar ekki að gera fleiri uppfærslur á honum. Þegar eiginleikaútgáfa hefur þessa stöðu er ekki lengur hægt að breyta henni eða neinum þáttum hennar.
- **Birt** – Þessi staða gefur til kynna að útgáfa eiginleika hafi verið birt í altækri geymslu sem tengist fyrirtækinu. Þegar eiginleikaútgáfa hefur þessa stöðu er ekki lengur hægt að breyta henni eða neinum þáttum hennar.

Hægt er að tilgreina dagsetningu í **Gildir frá** fyrir nýja útgáfu eiginleika fyrir rafræna reikningsgerð. Þannig getur þú skilgreint sjálfgefna útgáfu sem hægt er að nota eða sem hægt er að skrifa yfir þegar eiginleikinn er settur upp í þjónustuumhverfið.

Til að breyta stöðu eiginleikaútgáfu rafrænnar reikningagerðar skal fylgja þessum skrefum.

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Vinstra megin við síðuna **Eiginleikar rafrænnar reikningsfærslu** skal velja eiginleika rafrænnar reikningsfærslu.
4. Veljið flipann **Útgáfur** hægra megin á síðunni, veljið útgáfu.
5. Veldu **Breyta stöðu** og veldu síðan **Ljúka** (ef núverandi staða er **Drög**) eða **Birt** (ef núverandi stöðu er **Lokið**).
6. Veljið **Já** í skilaboðaglugganum til að staðfesta beiðnina.

Handvirk breyting úr **Ljúka** stöðu í **Birt** stöðu. Útgáfur eiginleika rafrænnar reikningagerðar eru sjálfkrafa uppfærðar **Birt** þegar þær eru settar upp í þjónustuumhverfið.

Hægt er að fylgjast með stöðunni í dálkinum **Staða útgáfu eiginleika** á flipanum **Útgáfur**.

## <a name="deploy-feature-versions"></a>Eiginleikaútgáfur notaðar

Í RCS er skipunin **Nota** notuð til að birta eiginleikaútgáfu rafrænnar reikningsfærslu í markþjónustuumhverfinu eða tengdu forriti

1. Vinstra megin við síðuna **Eiginleikar rafrænnar reikningsfærslu** skal velja eiginleika rafrænnar reikningsfærslu.
2. Á flipanum **Útgáfur** hægra megin á síðunni velurðu útgáfu rafræns reikningagerðareiginleika sem þú vilt nota í þjónustuumhverfið eða tengt forrit. Valin útgáfa verður að hafa stöðuna **Lokið** eða **Birt**.
3. Veljið **Nota** og veljið síðan einn eða báða af eftirfarandi valkosta til að skilgreina markmið uppsetningarinnar:

    - **Tengt forrit** – Þetta er valfrjálst, en verður að nota ef þú vilt að skilgreining sem fylgja uppsetningu forritsins séu skrifaðar í tilfelli Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management sem áður voru tengdar við það. Sleppa þessari tegund af útfærslu krefst handvirkrar skilgreiningar á færibreytum sem skilgreindar eru í uppsetningu forrits Finance eða Supply Chain Management.
    - **Þjónustuumhverfi** - þetta setur upp eiginleika rafrænnar reikningsfærslu í þjónustuumhverfi Rafræn reikningsfærsla er þá tilbúin til að taka við og vinna úr rafrænum skjölum sem Finance eða Supply Chain Management sendir.

> [!NOTE]
> Venjulega breytir þú færibreytum eiginleika rafrænnar skýrslugerðar sem verður að setja inn í þjónustuumhverfið. Breytingar á tengdu forriti eru sjaldgæfar. Þú ættir aðeins að setja inn nýjar útgáfur í tengda forritið þegar þú breytir samsvarandi færibreytum í forritinu þínu.

Til að ákvarða hvort tiltekin útgáfa af eiginleika rafrænnar reikningagerðar sé notuð í tilteknu umhverfi skaltu fara yfir upplýsingarnar á flipanum **Umhverfi**.

## <a name="remove-feature-versions"></a>Fjarlægja eiginleikaútgáfur

Í RCS er hægt að velja **Hætta við** til að fjarlægja tiltekna eiginleikaútgáfu rafrænnar reikningsfærslu úr þjónustuumhverfi, ef hún var notuð þar.

> [!IMPORTANT]
> Hnappurinn **Hætta við** virkar aðeins fyrir þjónustuumhverfi. Þetta fjarlægir ekki neitt úr tengdu forriti fyrir núverandi rafræna reikningagerð.

## <a name="rebase-electronic-invoicing-features"></a>Eiginleikar endurreikningur grunns rafrænnar reikningsfærslu

Þegar einn eiginleiki rafrænnar reikningsfærslu er tekinn frá öðrum, er hægt að velja **Endurreikna grunn** til að uppfæra afleiddan eiginleika með breytingunum sem hafa verið gerðar á upprunalega (yfir) eiginleikanum.

Til að endurreikna grunn afleiddrar útgáfu af eiginleika sem þú bjóst til skaltu fylgja þessum skrefum.

1. Sækið nýjustu útgáfuna eiginleikans með því að flytja hana inn úr altæku geymslunni. Frekari upplýsingar er að finna í [Flytja inn eiginleika úr altækri geymslu](e-invoicing-import-feature-global-repository.md).
2. Í listanum yfir eiginleika skal velja eiginleikann sem á að endurreikna grunn fyrir.
3. Í flipanum **Útgáfur** skal velja **Ný** til að búa til drög að útgáfu.
4. Veldu **Endurreikna grunn**.
5. Í svarglugganum **Endurreikna grunn** skal velja útgáfu eiginleikans til að endurreikna til.
6. Veldu **Í lagi**.
7. Farið yfir íhluti eiginleikans og gerið allar nauðsynlegar breytingar.
8. Veljið **Breyta stöðu** til að ljúka við eiginleika með endurreiknaðan grunn. Þegar endurreikning grunns er lokið er hægt að framkvæma fleiri aðgerðir.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Fáðu tiltekna útgáfu af eiginleikum rafrænnar reikningagerðar

Þegar ný útgáfa af eiginleika rafrænnar reikningargerðar er búin til býr kerfið til afrit af nýjustu útgáfu eiginleikans. Til að nota eldri útgáfu af eiginleikanum sem grunn fyrir nýja útgáfu skaltu velja útgáfuna og velja svo **Sækja þessa útgáfuskipun**. Ný uppkastsútgáfa af eiginleikanum er búin til sem er afrit af valda útgáfunni.
