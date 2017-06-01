---
title: "Grunnstilla hliðstæður verkþátt í verkflæði"
description: "Til að skilgreina samhliða verkþátt, Ljúka eftirfarandi aðgerðum í verkflæðisritill."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4c2f98803164d5c761d2089152c077cfb9e83c43
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Grunnstilla hliðstæður verkþátt í verkflæði

[!include[banner](../includes/banner.md)]


Til að skilgreina samhliða verkþátt, Ljúka eftirfarandi aðgerðum í verkflæðisritill.

Samhliða verkþáttur samanstendur úr verkflæðisgreinar sem eru keyrðar á sama tíma.

## <a name="name-a-parallel-activity"></a>Nefna Hliðstæður verkþáttur
Fylgið þessum skrefum til að færa inn heiti á samhliða aðgerð.
1.  Hægrismellt á hliðstæður verkþáttur og smellið síðan á **Eiginleika** til að opna í **Eiginleika** skjámynd.
2.  Í vinstri glugganum, smelltu á **grunnstillingar**.
3.  Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir hliðstæður verkþáttur
4.  Smellið á **Loka**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Skilgreina greinar Hliðstæður verkþáttur
Fylgdu eftirfarandi skrefum til að bæta við og skilgreina greinar þessa hliðstæður verkþáttur.
1.  Tvísmellið á samhliða verkþáttar til að birta greinar hins samhliða verkþáttar.
2.  Til að bæta við grein, dragið á **Grein** einingu úr á **verkflæðiseiningar** svæði á innskotsstaður í striga. Eftirfarandi tala sýnir innskotsstaði. ![innskotsstaður](./media/workflow_insertionpoint.gif)
    | **Ábending**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Röðun greina er ekki mikilvæg þar sem allar greinar samhliða verkþáttar keyra á sama tíma. |

3.  Til þess að skilgreina hver grein, sjá [Skilgreina samhliða grein](configure-parallel-branch-workflow.md).






