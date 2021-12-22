---
title: Flokkar samstæðulykla og viðbótar samstæðulyklar
description: Þetta efnisatriði veitir upplýsingar um samstæðureikningaflokka og viðbótarsamstæðureikninga og útskýrir hvernig þeir eru notaðir.
author: panolte
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 489f5417b6044e02d4711a03a17d6c19031cc2ee
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883388"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Hópar samstæðulykla og samstæðulyklar til viðbótar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um samstæðureikningaflokka og viðbótarsamstæðureikninga og útskýrir hvernig þeir eru notaðir.

## <a name="consolidation-account-groups"></a>Flokkar samstæðulykla

Flokkar samstæðulykla gera þér kleift að stofna flokk þeirra lykla sem þú vilt nota til að sameina gögn. Venjulega táknar samstæðureikningahópur ríkisreikningaskrá. Samstæðureikningahópur getur einnig varpað reikningum við hóp sem er skilgreindur af höfuðstöðvum fyrirtækisins. Hægt er að finna flokka samstæðulykla í svæðinu **Setja upp** í einingunni **Samstæður**. Þegar þú bætir við nýjum hópi slærðu inn einstakt auðkenni fyrir reikningshópinn, auk nafns.

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
