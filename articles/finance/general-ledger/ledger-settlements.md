---
title: Fjárhagsjafnanir
description: Þetta efnisatriði útskýrir hvernig á að nota síðu fjárhagsjafnana til að jafna fjárhagsfærslur og bakfærslur.
author: kweekley
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 6ba50321ea5e1cfb727f20bdb598f0c4e3236994
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753997"
---
# <a name="ledger-settlements"></a>Fjárhagsjafnanir

[!include [banner](../includes/banner.md)]

Fjárhagsjafnanir gerir þér kleift að samsvara debet- og kreditfærslur í fjárhagnum og merkja þau sem jöfnuð. Þannig geturðu tryggt að tengdar færslur hafi verið hreinsaðar. Þú getur einnig bakfært ef þær voru gerðar fyrir mistök.

## <a name="enable-advanced-ledger-settlements"></a>Virkja ítarleg fjárhagsuppgjör

Síða ítarlegs fjárhagsuppgjörs veitir frekari getu til að sía og velja færslur. Til að virkja síðu ítarlegs fjárhagsuppgjörs skaltu fylgja þessum skrefum.

1. Veldu **Fjárhagur** \> **Fjárhagsuppsetning** \> **Færibreytur fyrir fjárhag**. 
2. Á **Fjárhagsuppgjörs** flipanum skaltu stilla **Ítarlegt fjárhagsuppgjör** á **Já** til að kveikja á virkni ítarlega fjárhagsuppgjörsins. Ítarlega **Fjárhagsuppgjör** síðu verður notaður þegar þú velur **Fjárhagsuppgjör** í **Reglubundin verkefni**. 
3. Þú verður að slá inn lista yfir reikninga til að nota fyrir fjárhagsuppgjör fyrir hvern bókhaldslykil. Þessi listi er notaður til að sía lista yfir færslur sem birtast á **Fjárhagsuppgjör** síðu. Í **Listi yfir reikninga** skaltu velja bókhaldslykil og velja síðan **Nýr** til að bæta við nýjum reikningum á listann.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Settu upp færslur með því að nota síðu ítarlega fjárhagsuppgjörsins

Til að jafn fjárhagsfærslur skaltu fylgja þessum skrefum.

1. Veldu **Fjárhagur** \> **Reglubundin verkefni** \> **Fjárhagsuppgjör**.
2. Stilltu síurnar efst á síðunni:

    - Veldu dagsetningarbil, eða veldu **Kóða dagsetningarbils** til að fylla sjálfkrafa inn tímabilið.
    - Breyttu bókunarlaginu eins og þú þarfnast.
    - Til að birta fjárhagslykil og víddir sér skaltu velja fjárhagsvíddarsamstæðu.

3. Veldu **Birta færslur** til að sýna allar færslur sem samsvara síunum sem þú stillir og lista yfir reikninga sem þú tilgreindir þegar þú settir upp bókhaldslykilinn í fyrri hlutanum. Ef þú breytir einhverjum síum eða víddarsamstæðum þarftu að velja **Birta færslur** aftur.
4. Veldu eina eða fleiri línur sem þú ert að íhuga fyrir jöfnun. Virði **Valin upphæð** reitinn efst á síðunni eykst eða lækkar með heildarupphæðinni á línum sem þú valdir.
5. Þegar þú hefur lokið við að velja færslur skaltu velja **Merkja sem valið**. Gátmerki birtist í **Merkta** dálknum fyrir hverja færslu sem þú valdir. Auk þess eykst gildið **Valin upphæð** svæðisins fyrir ofan hnitanetið eða lækkar með heildarupphæðinni á línunum sem þú merktir.
6. Þegar **Valin upphæð** gildi er **0** (núll) skaltu velja **Jafna valdar færslur**. Staða valinna færslna er uppfært í **Jafnað**.

## <a name="make-transactions-easier-to-find"></a>Gera það auðveldara að finna færslur

**Fjárhagsuppgjör** síðan inniheldur aðgerðir sem auðveldar að sjá færslurnar sem þarf að jafna.

- **Fjarlægja val** hnappinn hreinsar **Valið** reitinn fyrir allar línur sem eru valdir.
- **Valið** sían gerir þér kleift að sía færslur miðað við hvort **Valið** reitinn fyrir þá sé valinn eða hreinsaður.
- **Staða** sía gerir þér kleift að sía færslur eftir því hvort staða þeirra er **Jöfnuð** eða **Ekki jöfnuð**.
- Með **Raða eftir algildri upphæð** hnappur er hægt að raða upphæðunum eftir algildri upphæð, þannig að þú getur sameinað debet og kredit að sömu upphæð.

## <a name="reverse-a-settlement"></a>Bakfæra jöfnun

Þú getur bakfært jöfnun sem var gerð fyrir mistök.

1. Fylgdu skrefum 1 til 3 í „Jafna færslur með því að nota síðu fyrir ítarleg fjárhagsuppgjör“ til að sýna færslurnar sem þú ert að leita að.
2. Í **Staða** síu, veldu **Jöfnuð**.
3. Veldu eina eða fleiri línur sem þú ert að íhuga að bakfæra. Virði **Valin upphæð** reitinn efst á síðunni eykst eða lækkar með heildarupphæðinni á línum sem þú valdir.
4. Þegar þú hefur lokið við að velja færslur skaltu velja **Merkja sem valið**. Gátmerki birtist í **Merkta** dálknum fyrir hverja færslu sem þú valdir. Þar að auki virði **Valin upphæð** reitinn efst á síðunni eykst eða lækkar með heildarupphæðinni á línum sem þú valdir.
5. Þegar **Valin upphæð** gildi er **0** (núll) skaltu velja **Bakfæra valdar færslur**. Staða merktra færslna er uppfært í **Ekki uppgert**.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>Uppfærðu lista yfir reikninga sem eru í listanum yfir færslur

Veldu **Lyklar fjárhagsuppgjörs** til að opna svarglugga þar sem þú getur breytt reikningum sem eru innifalin í listanum yfir færslur. Veldu **Nýr** til að bæta við nýjum reikningum á listann. Þessi listi er notaður til að sía lista yfir færslur sem birtast á **Fjárhagsuppgjör** síðu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
