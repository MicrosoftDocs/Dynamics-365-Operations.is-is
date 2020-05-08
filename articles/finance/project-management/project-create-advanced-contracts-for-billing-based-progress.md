---
title: Stofna ítarlega samninga fyrir greiðslur sem miðast við framvindu
description: Þetta efnisatriði útskýrir hvernig á að búa til verksamninga svo að þú getir búið til reikninga fyrir viðskiptavini, miðað við prósentuhlutfall lokinna verka.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282831"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Stofna ítarlega samninga fyrir greiðslur sem miðast við framvindu
[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að búa til verksamninga svo að þú getir stofnað reikninga fyrir viðskiptavini, miðað við prósentuhlutfall lokinna verka. Reikningsupphæðir eru sjálfkrafa reiknaðar út fyrir tegundir fjárhagsáætlunar vinnu sem er sett upp fyrir verk. Tímasetning reikningsins er stillt þegar samið er um verksamninginn við viðskiptavininn.

Notið aðferðirnar í þessu efnisatriði til þess að setja upp samning, tengt verk, og reikningsreglur sem nota á við útreikning reikningsupphæða fyrir tegundir fjárhagsáætlunar vinnu sem er sett upp fyrir verkið.

Þegar þú hefur stofnað samninginn og verkið, er hægt að setja upp upplýsingarnar um verkið. Til dæmis er hægt að skilgreina aðgerðir og úthluta starfsmönnum til verksins.

## <a name="example"></a>Dæmi

Fyrirtæki notanda er fyrirtæki í hugbúnaðarþróun. Þú samþykkir að þróa launabókhaldspakka fyrir viðskiptavin vegna heildargjalda sem nema 20.000 bandaríkjadölum (USD). Fyrirtækið samþykkir að senda reikning til viðskiptavinarins samhliða því að það lýkur tilteknu hlutfalli verksins. Þú setur upp eftirfarandi verkflokka fyrir verkið, þannig að þú getir notað þá í reikningagerð:

- Ráðgjöf
- Hönnun
- Uppsetning

Þú setur einnig upp reglur sem reikna sjálfkrafa upphæð reiknings fyrir hlutfall vinnu við verk sem er lokið í hverjum flokki fyrir sig.

Stjórnandi fjárhagsáætlunar stofnar fjárhagsáætlun fyrir verkflokkana. Upphæð lokinnar vinnu er sjálfkrafa reiknað sem hlutfall raunvinnu samanborið við upphæðir fjárhagsáætlunarinnar.

## <a name="prerequisites"></a>Forkröfur

Áður en þú stofnar verk sem notar reikningsreglur verður þú að setja upp númeraröð fyrir reikningsreglur og þóknunarbók sem er notuð til að bóka útskriftir samkvæmt framvindu.

1. Opnaðu **Verkefnastjórnun og bókhald** \> **Uppsetning** \> **Færibreytur verkefnastjórnunar og bókhalds**.
2. Á síðunni **Verkefnastjórnun og bókhaldsfæribreytur** á flipanum **Númeraraðir** setur þú upp númeraröðina sem skal nota þegar reikningsreglur eru stofnaðar.
3. Opnaðu **Verkefnastjórnun og bókhald** \> **Færslubækur** \> **Gjald**.
4. Á síðunni **Gjaldabók** velurðu **Nýtt** og slærð inn heiti færslubókarinnar.

## <a name="create-a-contract-for-progress-billings"></a>Stofna samning fyrir framvinduútskriftir

Notið þessa aðferð til þess að stofna verksamning fyrir fastverðsverk. Stofnaður er verkreikningur þegar vinnan sem lokið er fyrir verkið nær tilteknu hlutfalli.

1. Opnaðu **Verkefnastjórnun og bókhald** \> **Verk** \> **Verksamningar**.
2. Veldu **Nýtt** á síðunni **Verksamningar**.
3. Stillið eftirfarandi svæði í svarglugganum **Nýr verksamningur**:

    - **Nafn**
    - **Gerð fjármögnunar**
    - **Fjármögnunaraðili**
    - **Sölugjaldmiðill** Sjálfgefið er að þessi gjaldmiðill sé notaður fyrir reikninga viðskiptavina sem tengjast verksamningnum. Hins vegar er hægt að breyta sölugjaldmiðlinum á tilteknum reikningi viðskiptavinar.

4. Veljið **Í lagi**. Upplýsingarnar eru afritaðar í haus síðunnar **Verksamningar**.
5. Á síðunni **Verksamningar** skal ljúka við að fylla út í nauðsynlegar upplýsingar fyrir verkið.

## <a name="create-a-project-for-progress-billings"></a>Stofna verk fyrir framvinduútskriftir

Fylgdu eftirfarandi skrefum til að stofna verk og undirverk af hvaða toga sem tengjast verksamningi.

1. Opnaðu **Verkefnastjórnun og bókhald** \> **Verk** \> **Öll verk**.
2. Á síðunni **Öll verk** velurðu **Nýtt**.
3. Í svarglugganum **Nýtt verk** í svæðinu **Gerð verk** velurðu **Tími og efni**.
4. Veljið verkflokk. Verkflokkur skilgreinir bókunarupplýsingar verka sem eru tengd við flokkinn.
5. Velja **Stofna verk**.
6. Eftir að búið er að stofna verkið, skal stilla verkstigið á **Í vinnslu**.

## <a name="create-a-budget-for-a-project"></a>Stofna áætlun fyrir verk

Tegundir fjárhagsáætlunar eru notaðar til að reikna sjálfkrafa út reikningsupphæðir fyrir hlutfall þeirrar vinnu sem er lokið fyrir hverja flokka. Fylgdu þessum skrefum til að stofna fjárhagsáætlunarflokka fyrir áætlaðan kostnað.

1. Opnaðu **Verkefnastjórnun og bókhald** \> **Verk** \> **Öll verk**.
2. Á síðunni **Öll verk** velurðu og opnar verkið sem óskað er eftir.
3. Á síðunni **Verk** á Aðgerðasvæðinu á flipanum **Áætlun** í hópnum **Fjárhagsáætlun** velurðu **Fjárhagsáætlun verks**.
4. Á síðunni **Fjárhagsáætlun verks** skaltu færa inn áætlaðan kostnað fyrir hvern flokk í verkinu.

## <a name="create-billing-rules-for-progress-billings"></a>Stofna reikningsreglur fyrir framvinduútskriftir

1. Opnaðu **Verkefnastjórnun og bókhald** \> **Verk** \> **Verksamningar**.
2. Veldu og opnaðu verksamning á síðunni **Verksamningar**.
3. Á síðu verksamningsins á flýtiflipanum **Reikningsreglur** velurðu **Bæta við**.
4. Á síðunni **Reikningsregla** á svæðinu **Línugerð** velurðu **Framvinda**.
5. Á flýtiflipanum **Upplýsingar um reikningsreglulínu** á svæðinu **Samningsvirði** slærðu inn heildarvirði samningsins.
6. Á svæðinu **Flokkur** skal velja flokkinn til að bóka þóknunarfærsluna í.
7. Á svæðinu **Verk** er valið verk sem notar þessa reikningsreglu.
8. Valfrjálst: Hægt er að úthluta reikningsreglunni til annarra verka. Á flýtiflipanum **Verk** í hlutanum **Tiltæk verk** velurðu verk og síðan hægri örvarhnappinn til að bæta verkinu við hlutan **Valin verk**.
9. Valfrjálst: Reikna út hlutfall upphæðar sem viðskiptavinurinn heldur eftir af greiðslum á reikningi. Á flýtiflipanum **Varðveisluskilmála greiðslu** skal velja uppruna fjármögnunar og síðan færa varðveisluprósentuna inn á svæðinu **Varðveisluprósenta**.
10. Þessi skref eru endurtekin til að stofna fleiri reikningsreglur fyrir verksamninginn.
