---
title: "Skilgreina hliðstæða verkþætti í verkflæði"
description: "Til að skilgreina samhliða verkþátt, Ljúka eftirfarandi aðgerðum í verkflæðisritill."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 64cd387f8a6ab693d159cd659fca51fa6568ee39
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="configure-parallel-activities-in-a-workflow"></a>Skilgreina hliðstæða verkþætti í verkflæði

[!include [banner](../includes/banner.md)]

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
1. Tvísmellið á samhliða verkþáttar til að birta greinar hins samhliða verkþáttar.
2. Til að bæta við grein, dragið á **Grein** einingu úr á **verkflæðiseiningar** svæði á innskotsstaður í striga. Eftirfarandi tala sýnir innskotsstaði. ![innskotsstaður](./media/workflow_insertionpoint.gif)

   |                                              <strong>Ábending</strong>                                               |
   |------------------------------------------------------------------------------------------------------------------|
   | Röðun greina er ekki mikilvæg þar sem allar greinar samhliða verkþáttar keyra á sama tíma. |


3. Til þess að skilgreina hver grein, sjá [Skilgreina samhliða grein](configure-parallel-branch-workflow.md).






