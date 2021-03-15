---
title: Virkja drög að fjárhagsáætlun (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að virkja eiginleikann Drög að fjárhagsáætlun í Fjármálainnsýn.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995141"
---
# <a name="enable-budget-proposals-preview"></a>Virkja drög að fjárhagsáætlun (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hvernig á að virkja eiginleikann Drög að fjárhagsáætlun í Fjármálainnsýn.

1. Notaðu upplýsingar úr umhverfissíðunni í Microsoft Dynamics Lifecycle Services (LCS) til að tengjast aðaltilviki Azure SQL fyrir þetta umhverfi. Keyrið eftirfarandi Transact-SQL (T-SQL) skipun til að kveikja á flugi fyrir sandkassaumhverfa. (Hugsanlega þarf að kveikja á aðgangi að IP-tölu notanda í LCS áður en hægt er að fjartengjast við AOS \[Application Object Server\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Ef verið er að setja upp Microsoft Dynamics 365 Finance sem Service Fabric-uppsetningu er hægt að sleppa þessu skrefi. Fjármögnunarteymið ætti nú þegar að hafa kveikt á forútgáfunni fyrir þig. Ef eiginleikinn er ekki sýnilegur í vinnusvæðinu **Eiginleikastjórnun** eða ef vandamál kemur upp þegar reynt er að kveikja á honum skal senda tölvupóst á [Teymi forskoðinar forritsins Fjárhagsinnsýnar](mailto:fiap@microsoft.com).

2. Opnið vinnusvæðið **Eiginleikastjórnun** og fylgið eftirfarandi skrefum:

    1. Veldu **Leita að uppfærslum**.
    2. Leitið að **Drög að fjárhagsáætlun** og kveikið á þessum eiginleika.

3. Farið í **Fjárhagsáætlanir \> Uppsetning \> grunnáætlanagerð \> Drög að fjárhagsáætlun (forskoðun)** og veljið **Virkja eiginleika**.

#### <a name="privacy-notice"></a>Tilkynning um persónuvernd
Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]