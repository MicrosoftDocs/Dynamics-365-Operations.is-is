---
title: "Flokkar samstæðulykla og viðbótar samstæðulyklar"
description: "Þetta efnisatriði veitir upplýsingar um flokka samstæðulykla og viðbótarsamstæðulykla og útskýrir hvernig þeir eru notaðir í Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 3c08e48b22f964c3f643c5ddc4ecd687502d7fda
ms.contentlocale: is-is
ms.lasthandoff: 08/01/2017

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Flokkar samstæðulykla og viðbótar samstæðulyklar

[!include[banner](../includes/banner.md)]


Þetta efnisatriði veitir upplýsingar um flokka samstæðulykla og viðbótarsamstæðulykla og útskýrir hvernig þeir eru notaðir í Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu.

<a name="consolidation-account-groups"></a>Flokkar samstæðulykla
----------------------------

Flokkar samstæðulykla gera þér kleift að stofna flokk þeirra lykla sem þú vilt nota til að sameina gögn. Oftast stendur flokkur samstæðulykla fyrir stjórnvaldatilskipaðan bókhaldslykil eða varpar lyklum á flokka sem eru skilgreindir eftir höfuðstöðvum fyrirtækisins. Hægt er að finna flokka samstæðulykla í svæðinu **Setja upp** í einingunni **Samstæður**. Þegar nýjum flokki er bætt við skal færa inn einkvæmt kenni fyrir lyklaflokkinn og heiti.

## <a name="additional-consolidation-accounts"></a>Fleiri samstæðulyklar
Fleiri samstæðulyklar gera þér kleift að úthluta lykli úr fyrirliggjandi bókhaldslykill til samstæðulykill flokkur. Síðan er hægt að tilgreina samstæðulykill gildi og heiti. 

Hægt er að finna viðbótar samstæðulykla í svæðinu **Setja upp** í einingunni **Samstæður**. Þegar nýr samstæðulykill er stofnaður verður að tilgreina gerð eftirfarandi upplýsingar:

-   **Aðallykill** – Þessi reitur er uppfletting sem sýnir alla aðallykla sem eru á grunni bókhaldslykill sem var valinn á síðunni. Þegar þú velur lykil er heiti hans sjálfvirkt skráð í svæðið **Heiti reiknings**.
-   **Flokkur samstæðulykla** – Notaðu þetta svæði til að tilgreina flokk til að úthluta lykill í. Ef þú sameinar á tvo mismunandi vegu verður að bæta við sama lykli í alla fjóra flokka samstæðulykla.
-   **Samstæðulykill** – Skráðu gildi samstæðulykilsins. Þetta gildi þarf ekki að vera lykill úr bókhaldslykill. Það getur verið hvaða gildi sem þú vilt.
-   **Heiti samstæðulykils** – Skráðu heiti reikningsins eins og það á að birtast á fyrirspurnum og skýrslum.
-   **SAT stig** – Þessi reitur er notaður til að tilkynna lyklayfirlit til mexíkanskra skattayfirvalda. 

Þegar þú hefur lokið stofnun á flokkum samstæðulykla og viðbótar samstæðulykla er hægt að velja flokkinn í ferlinu Sameina á netinu.


Nánari upplýsingar er að finna í [Stofna samstæðuhópa og fleiri samstæðulykla](../general-ledger/tasks/create-consolidation-groups.md) 




