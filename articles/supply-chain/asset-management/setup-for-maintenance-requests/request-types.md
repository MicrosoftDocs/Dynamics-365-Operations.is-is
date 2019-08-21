---
title: Gerðir viðhaldsbeiðna
description: Þetta efni útskýrir hvernig á að setja upp gerðir viðhaldsbeiðna í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790505"
---
# <a name="maintenance-request-types"></a>Gerðir viðhaldsbeiðna

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Gerðir viðhaldsbeiðna eru notaðar til að flokka viðhaldsbeiðnir. Til dæmis gætir þú verið með tegundir viðhaldsbeiðna sem tengjast fyrirbyggjandi viðhaldi og leiðréttandi viðhaldi. Eða þú gætir haft sérstaka tegund viðhaldsbeiðni sem er notuð til að stjórna viðgerðum á eignum (viðgerð á geymslu).

Gerð viðhaldsbeiðni skilgreinir tengsl við líftímastöðuhóp fyrir viðhaldsbeiðni (viðhaldslíftímalíkan). Líftímalíkön viðhaldsbeiðni skilgreina líftímastöður sem hægt er að stilla fyrir viðhaldsbeiðni. (Dæmi um lífshringrásarstig viðhalds eru **Stofnað**, **Virkur**, og **Klárað**.)

1. Veldu **Eignastýring** \> **Uppsetning** \> **Viðhaldsbeiðnir** \> **Gerðir viðhaldsbeiðna**.
2. Veldu **Nýtt** til að búa til gerð viðhaldsbeiðni.
3. Í reitnum **Gerð viðhaldsbeiðni**, sláðu inn auðkenni fyrir gerð viðhaldsbeiðni.
4. Færið inn lýsandi nafn í reitinn **Heiti**.
5. Á flýtiflipanum **Almennt**, í **Líftímalíkan viðhaldsbeiðni**, veldu líkan um líftíma viðhaldsbeiðni.
6. Í reitnum **Verkbeiðni** velurðu gerð verkbeiðni. Þegar viðhaldsbeiðni er breytt í verkbeiðni fær verkbeiðnin sjálfkrafa þá gerð verkbeiðni sem tengist gerð viðhaldsbeiðninnar.

Eftirfarandi mynd sýnir dæmi um síðuna **Gerðir viðhaldsbeiðna**.

![Mynd 1](media/07-setup-for-requests.png)
