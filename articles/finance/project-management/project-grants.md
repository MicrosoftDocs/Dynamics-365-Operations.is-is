---
title: Verkefnisstyrkir
description: Í þessu efnisatriði er útskýrt hvernig á að stofna eða breyta styrk.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
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
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282832"
---
# <a name="project-grants"></a>Verkefnisstyrkir

[!include [banner](../includes/banner.md)]

Styrkur er peningagjöf vegna ákveðins tilgangs eða verks. Yfirleitt eru hömlur á hvernig er hægt að nota styrk. Í Verkefnastjórnun og bókhald er hægt að færa inn og rekja styrki og skilgreina vensl þeirra við verk og verksamninga. Til dæmis er hægt að framkvæma eftirfarandi verk:

- Tengja styrki við verkefni og fjármögnunaraðila í gegnum tengla á síðurnar **Verk** og **Upplýsingar um verksamning**.
- Færa inn og rekja breytingar á styrk í því sem hann færist úr einni stöðu í aðra.
- Færa inn og rekja kostnað, umbeðnar upphæðir, og veittar upphæðir.
- Stofna styrkssniðmát og tengja undirstyrki við þau.

Hægt er að búa til styrk með því að færa inn allar upplýsingar í nýja færslu eða með því að afrita þær úr eldri styrk og síðan uppfæra þær.

## <a name="create-a-new-grant"></a>Stofna nýjan styrk

1. Opnaðu **Verkefnastjórnun og bókhald** \> **Styrkir** \> **Styrkir**.
2. Veldu **Nýr** \> **Styrkur**.
3. Á upplýsingasíðu styrks, í flýtiflipanum **Almennt**, í reitnum **Kenni styrks**, skaltu slá inn auðkenni styrksins í tölu- eða bókstöfum.
4. Í reitnum **Heiti styrks** skaltu slá inn heiti styrksins.
5. Í reitnum **Lýsing** skaltu bæta við upplýsingum um nýja styrkinn.

    Flestir hinna reitanna á síðunni eru valfrjálsir og hægt er að færa inn eins litlar eða eins miklar upplýsingar og þurfa þykir.

    Eftirfarandi listi lýsir upplýsingum sem eru tilgreindar á hverjum flýtiflipa á upplýsingasíðu styrksins:

    - **Almennt** - Sláðu inn heiti styrks, stöðu, lýsingu, tilgang og upphæð.
    - **Tengiliðaupplýsingar** - Færðu inn upplýsingar um starfsmenn og þá deild sem mun hafa umsjón með styrknum og viðskiptavin styrksins eða fyrirtækið sem er styrktaraðili. Einnig er hægt að tákna hvort fyrirtæki áframsendingareining sem fær styrk og lætur hann síðan í hendur annars viðtakanda. Smellið á **Bæta við** til að bæta við tengslaupplýsingum eins og símanúmerum og tölvupóstum fyrir fyrirtækið sem veitir styrkinn.
    - **Dagsetningar og skiladagar** – Færa inn dagsetningar sem tengjast styrknum og styrkumsókninni. Sem dæmi má nefna gjalddaga umsóknar, skiladagur og dagsetning þegar styrkurinn er samþykktur eða honum hafnað.
    - **Tengd verk og verksamningar** - Þú getur aðeins fært inn upplýsingar á þessum flýtiflipa ef reiturinn **Staða styrks** í flýtiflipanum **Almennt** er stilltur á **Virkur** eða **Veittur**. Veldu úr eftirfarandi valkostum til að ljúka við tengda verkið:

        - **Bæta við fjármögnunaraðila** – Bæta við nýjum fjármögnunaraðila fyrir styrkinn. Hægt er að færa inn allar upplýsingar nú eða nota sjálfgefnu upplýsingarnar og uppfæra síðar.
        - **Bæta við verksamningi** – Bæta við eða uppfæra samningsupplýsingar verks.
        - **Bæta við verki** – Bæta við eða uppfæra verkupplýsingar.

    - **Uppsetning** - Færðu inn upplýsingar um samsvarandi sjóði ef þessar upplýsingar eru nauðsynlegar. Mörg fyrirtæki sem veita styrki krefjast að viðtakandi eyði visst mikið af eigin fjármagni eða forða til að jafna út það sem veitt er í styrk. Í reitnum **Staðbundið verk eða rakningarkenni** geturðu fært inn kennimerki sem er ólíkt verkkenninu.

        > [!NOTE]
        > Ef hluti styrksins verður veittur til annars fyrirtækis skal stilla valkostinn **Undirstyrktaraðili** á **Já**. Fyrir styrki sem eru veittir í Bandaríkjunum er hægt að tilgreina hvort styrkur verður veittur samkvæmt ríkis- eða alríkistilskipun.

    - **Upplýsingar um niðurfærslu** - Bæta við eða uppfæra upplýsingar um hversu oft má taka út fjármagn styrks, rukka fyrir það eða eyða.

## <a name="create-a-new-grant-from-a-copy"></a>Stofna nýjan styrk úr afriti

1. Opnaðu **Verkefnastjórnun og bókhald** \> **Styrkir** \> **Styrkir**.
2. Veljið **Ný** \> **Afrita úr styrki**.
3. Færa inn auðkenni í tölu - eða bókstöfum og heiti fyrir nýjan styrk og síðan valið **Í lagi**.
4. Á upplýsingasíðu styrks skal fara yfir upplýsingar afritaðs styrks og gera nauðsynlegar breytingar. Flestir reitir á síðunni eru valfrjálsir.

## <a name="view-or-modify-grant-details"></a>Skoða eða breyta styrkupplýsingum

1. Opnaðu **Verkefnastjórnun og bókhald** \> **Styrkir** \> **Styrkir**.
2. Veljið réttinn til að breyta.
3. Á aðgerðasvæðinu, í flipanum **Styrkur**, í flokknum **Viðhalda**, skal velja **Breyta**.
4. Farðu yfir styrkupplýsingarnar og gerðu allar nauðsynlegar breytingar.
