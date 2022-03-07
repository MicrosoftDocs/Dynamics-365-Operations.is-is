---
title: Eignir á innleið og útleið
description: Þetta efni útskýrir hvernig á að eignir á innleið og útleið í eignastýringu.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0bd3127df1b583acc6841c3e115d3beceabcab2756098e567b2269c1dcc94004
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759624"
---
# <a name="inbound-and-outbound-assets"></a>Eignir á innleið og útleið

[!include [banner](../../includes/banner.md)]

 

Ef fyrirtæki þitt sinnir viðgerðarstörfum eða viðhaldsstörfum á eignum sem eru mótteknar frá öðrum stöðum eða viðskiptavinum, þá getur eignastýring rakið bæði eignir á innleið sem eru á leið til þíns fyrirtækis og eignir á útleið sem er skilað.

> [!NOTE]
> Ef þú vilt nota líftímastöður á innleið og útleið til að stjórna eignum sem eru að koma inn og verða skilað, verður þú að setja upp viðhaldsbeiðni um líftímastöður og líftímalíkön til að styðja þessar aðgerðir. Nánari upplýsingar er að finna í [Viðhaldsbeiðnir](../setup-for-maintenance-requests/requests.md).

Uppsetning eignastýringar ákvarðar hvort þú getur unnið eignir á innleið og útleið.

## <a name="register-assets-as-inbound"></a>Skráðu eignir sem á innleið

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Virkar viðhaldsbeiðnir**.
2. Veljið viðhaldsbeiðnina.
3. Veldu **Uppfæra stöðu viðhaldsbeiðni**.
4. Veldu **Á innleið** (eða aðra líftímastöðu sem þú hefur búið til fyrir eignir á innleið) og veldu síðan **Í lagi**.

![Skrá eignir sem á innleið.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Skrá eignir á innleið sem mótteknar

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Innleið/útleið** \> **Eignir á innleið**.
2. Veljið eignina eða viðhaldsbeiðnina.
3. Veldu **Taka á móti eignum**.
4. Í reitnum **Móttekið** skaltu slá inn dagsetningu og tíma. Veljið síðan **Í lagi**. Gögnin eru tekin af listasíðunni **Eignir á innleið**.

![Skrá eignir á innleið sem mótteknar.](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Skráðu eignir sem á útleið

Þegar þú hefur lokið viðhalds- eða viðgerðarstörfum geturðu skráð eignina sem skilað.

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Virkar viðhaldsbeiðnir**.
2. Veljið viðhaldsbeiðnina.
3. Veldu **Uppfæra stöðu viðhaldsbeiðni**.
4. Veldu **Á útleið** (eða aðra líftímastöðu sem þú hefur búið til fyrir eignir á útleið) og veldu síðan **Í lagi**.

## <a name="register-outbound-assets-as-delivered"></a>Skráðu eignir á útleið sem afhentar

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Innleið/útleið** \> **Eignir á útleið**.
2. Veljið eignina eða viðhaldsbeiðnina.
3. Veldu **Skila eignum**.
4. Í reitnum **Afhent** skaltu slá inn dagsetningu og tíma. Veljið síðan **Í lagi**. Gögnin eru tekin af listasíðunni **Eignir á útleið**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]