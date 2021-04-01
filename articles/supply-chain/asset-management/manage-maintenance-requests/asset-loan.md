---
title: Eignarlán
description: Þetta efni lýsir því hvernig á að skrá lán á eignir í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d76d8e9b735adc1fa796cff5e0ef7d049d109144
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253447"
---
# <a name="asset-loans"></a>Eignarlán

[!include [banner](../../includes/banner.md)]

 

Ef fyrirtæki þitt fær eignir til viðgerðar- eða viðhaldsstarfa frá annaðhvort innri staðsetningu eða viðskiptavinum og ef þú lánar eignir tímabundið til þessara staða eða viðskiptavina getur eignastýring rakið eignalánin.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Skráðu eignarlán á viðhaldsbeiðni

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.
2. Veldu viðhaldsbeiðni til að skrá eignarlán í og veldu síðan **Breyta**.
3. Á síðunni **Beiðni** velurðu **Senda lánseign**.
4. Veldu eignina og sláðu inn áætlaðan skiladag.
5. Veljið **Í lagi**.

> [!NOTE]
> - Þú getur aðeins sent lánaeign ef eign af sömu eignategund er tiltæk.
> - Eignin sem þú lánar verður að vera með eignalíftímastöðu sem gerir kleift að hún sé notuð sem lánaeign, svo sem **InStorage**. Þegar eignalánið er skráð, er líftímastaða eignarinnar sjálfkrafa uppfærð í t.d. **OnLoan**.

Til að skoða lista yfir allar eignir sem þú hefur lánað til annarra staða eða viðskiptavina skaltu velja **Eignastýring** \> **Sameiginlegt** \> **Eignalán** \> **Öll eignalán**. Ef gátreiturinn **Klárað** er valinn fyrir eign hefur eignin verið skráð sem skilað til fyrirtækisins.

![Vinna með viðhaldsbeiðnir](media/06-manage-maintenance-requests.png)

Á síðunni **Virk eignalán** geturðu skoðað lista yfir allar lánaeignir sem hefur ekki enn verið skilað til fyrirtækisins.

## <a name="register-loan-assets-as-returned"></a>Skráðu lánaeignir sem skilað er

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignalán** \> **Virk eignalán**.
2. Veldu eignalánið sem á að skrá sem skilað og veldu síðan **Skila eignaláni**.
3. Í reitnum **Skilað** skaltu slá inn dagsetningu og tíma.
4. Veljið **Í lagi**.
5. Endurnærðu **Virk eignalán** listasíðu og taktu eftir því að eignalánið birtist ekki lengur á listanum.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]