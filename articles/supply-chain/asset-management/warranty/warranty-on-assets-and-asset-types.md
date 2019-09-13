---
title: Ábyrgðir á eignum og eignagerðum
description: Þetta efni útskýrir hvernig á að setja upp ábyrgðir á eignum og eignagerðum í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b13f8aba7e1d2448495f97a4772eb573e08c025
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874602"
---
# <a name="warranty-on-assets-and-asset-types"></a>Ábyrgð á eignum og eignagerðum

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Þetta efni útskýrir hvernig á að setja upp ábyrgðir á eignum og eignagerðum í eignastjórnun.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Settu upp ábyrgð á eignagerð

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignagerðir** \> **Eignagerðir**.
2. Í vinstri glugganum velurðu eignategundina sem á að festa ábyrgðarsamning lánardrottins við og velur síðan **Sjálfgefin tegund eigna**.
3. Á flýtiflipanum **Almennt**, í reitnum **Ábyrgð lánardrottins** velurðu samninginn.

## <a name="set-up-a-warranty-on-an-asset"></a>Settu upp ábyrgð á eign

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir**.
2. Veldu eignina og veldu síðan **Breyta**.
3. Á flýtflipanum **Lánardrottinn** í hlutanum **Ábyrgð lánardrottins** í reitnum **Ábyrgð** velurðu ábyrgðarsamninginn.
4. Í reitunum **Upphafð ábyrgðar** og **Lok ábyrgðar** velurðu upphafs- og lokadagsetningar.

    > [!IMPORTANT]
    > Ef dagsetning er valin í reitnum **Upphaf ábyrgðar** í verkbeiðni gildir ábyrgðin fyrir verkbeiðnina á þeim degi. Þegar þú býrð til verkbeiðni er reiturinn **Upphaf ábyrgðar** sjálfvirkt stilltur á dagsetningu stofnunar. Hins vegar er hægt að breyta dagsetningunni þannig að hún samsvari til dæmis upphafsdagsetningu ábyrgðarsamnings.
    >
    > ![Mynd 1](media/02-warranty.png)

> [!NOTE]
> Þegar þú býrð til verkbeiðni fyrir eign sem fellur undir ábyrgð lánardrottins, ef verkbeiðnin er með áætlaðan upphafsdag á ábyrgðartímabilinu, færðu tilkynningu um ábyrgðarsamninginn. Þú getur síðan sagt upp verkbeiðninni eins og þú þarft.
