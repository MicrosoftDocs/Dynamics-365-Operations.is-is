---
title: Virkja drög að fjárhagsáætlun (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að virkja eiginleikann Drög að fjárhagsáætlun í Fjármálainnsýn.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: cc7b06ee40553a254a939babc30e6f5c99f85507c1a3db4e916f480560cf8835
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768940"
---
# <a name="enable-budget-proposals-preview"></a>Virkja drög að fjárhagsáætlun (forskoðun)

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að virkja eiginleikann Drög að fjárhagsáætlun í Fjármálainnsýn.

1. Notaðu upplýsingar úr umhverfissíðunni í Microsoft Dynamics Lifecycle Services (LCS) til að tengjast aðaltilviki Azure SQL fyrir þetta umhverfi. Keyrið eftirfarandi Transact-SQL (T-SQL) skipun til að kveikja á flugi fyrir sandkassaumhverfa. (Hugsanlega þarf að kveikja á aðgangi að IP-tölu notanda í LCS áður en hægt er að fjartengjast við AOS \[Application Object Server\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Sleppið þessu skrefi ef notuð er útgáfa 10.0.20 eða nýrri eða ef notuð er uppsetning Service Fabric. Fjármögnunarteymið ætti nú þegar að hafa kveikt á forútgáfunni fyrir þig. Ef þú sérð ekki eiginleikann á vinnusvæðinu **Eiginleikastjórnun** eða ef vandamál koma upp þegar reynt er að kveikja á honum skal hafa samband við <fiap@microsoft.com>.

2. Opnið vinnusvæðið **Eiginleikastjórnun** og fylgið eftirfarandi skrefum:

    1. Veldu **Leita að uppfærslum**.
    2. Leitið að **Drög að fjárhagsáætlun** og kveikið á þessum eiginleika.

3. Farið í **Fjárhagsáætlanir \> Uppsetning \> grunnáætlanagerð \> Drög að fjárhagsáætlun (forskoðun)** og veljið **Virkja eiginleika**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
