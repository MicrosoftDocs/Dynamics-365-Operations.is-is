---
title: Setja upp kostnaðargerðir
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp kostnaðargerðir í Eignarleigu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1538826f140393eec59be9ff4df5242d5ced9d8f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249750"
---
# <a name="set-up-expense-types"></a>Setja upp kostnaðargerðir

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp kostnaðargerðir í Eignarleigu. Kostnaður sem er ekki sýndur í greiðsluáætlun er þekktur sem *útgjaldakostnaður*. Dæmi um slíkan kostnað eru m.a. fasteignaskattar, viðhaldskostnaður sameiginlegs svæðis og tryggingagjöld.

## <a name="add-an-administrative-expense-type"></a>Nota gerð stjórnunarkostnaðar

1. Opnið **Eignarleiga \> Uppsetning \> Kostnaðargerðir**.
2. Veljið **Nýtt**.
3. Í viðeigandi svæði skal færa inn nýja kostnaðargerð og lýsingu.

## <a name="assign-accounts-to-administrative-costs"></a>Úthluta lyklum á stjórnunarkostnað

Næst ætti að tengja lykla við kostnaðargerðirnar. Þessir lyklar verða debetfærðir þegar kostnaðaráætlunarfærslur eru bókaðar. Mótlykill er tilgreindur á **Greiðsluáætlunarlínum rekstrarkostnaðar** fyrir hvern leigusamning fyrir sig.

1. Opnið **Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**.
2. Á flipanum **Lyklar** á flýtiflipanum **Rekstrarkostnaður** í svæðinu **Kostnaðargerð** er kostnaðargerðin valin.
3. Veljið **Bæta við**.
4. Í reitnum **Bókargerð** skal velja gerð bókarinnar sem á að tengja við stjórnunarkostnaðinn.

    > [!NOTE]
    > Hægt er að tengja margar bókargerðir við sama kostnaðarlykil.

5. Í svæðinu **Lykilkóði** skal tilgreina leigusamningana sem nota skal bókina fyrir:

    - **Allt** – Nota bók fyrir allar leigur.
    - **Flokkur** -Notið bókina á tiltekinn flokk leigusamninga.
    - **Tafla** – Nota bókina fyrir tiltekna leigusamninga.

6. Ef þú valdir **Flokk** eða **Tafla** í svæðinu **Lykilkóði** skaltu velja lykilnúmer eða flokksnúmer á svæðinu **Lykil-/flokksnúmer**.
7. Í viðeigandi svæðum skal velja aðallykill fjármögnunarleigusamnings og aðallykil rekstrarleigusamnings.

Þegar þessum skrefum er lokið er hægt að bæta kostnaði við **Greiðsluáætlunarlínur rekstrarkostnaðar** á síðunni **Upplýsingar um leigusamning** fyrir valinn leigusamning. Að öðrum kosti er hægt að bæta við kostnaði þegar ný leiga er stofnuð.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]