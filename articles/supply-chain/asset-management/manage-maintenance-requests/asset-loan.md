---
title: Eignarlán
description: Þessi grein lýsir því hvernig á að skrá lánaeignir í eignastýringu.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f70b29ef69b80160f108e6f53edda12b86c2c9db
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015755"
---
# <a name="asset-loans"></a>Eignarlán

[!include [banner](../../includes/banner.md)]

 

Ef fyrirtæki þitt fær eignir til viðgerðar- eða viðhaldsstarfa frá annaðhvort innri staðsetningu eða viðskiptavinum og ef þú lánar eignir tímabundið til þessara staða eða viðskiptavina getur eignastýring rakið eignalánin.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Skráðu eignarlán á viðhaldsbeiðni

1. Veldu **Eignastýring** \> **Viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.
2. Veldu viðhaldsbeiðni til að skrá eignarlán í og veldu síðan **Breyta**.
3. Á síðunni **Beiðni** velurðu **Senda lánseign**.
4. Veldu eignina og sláðu inn áætlaðan skiladag.
5. Veljið **Í lagi**.

> [!NOTE]
> - Þú getur aðeins sent lánaeign ef eign af sömu eignategund er tiltæk.
> - Eignin sem þú lánar verður að vera með eignalíftímastöðu sem gerir kleift að hún sé notuð sem lánaeign, svo sem **InStorage**. Þegar eignalánið er skráð, er líftímastaða eignarinnar sjálfkrafa uppfærð í t.d. **OnLoan**.

Til að skoða lista yfir allar eignir sem þú hefur lánað öðrum stöðum eða viðskiptavinum skaltu velja **Eignastýring** \> **Eignalán** \> **Öll eignalán**. Ef gátreiturinn **Klárað** er valinn fyrir eign hefur eignin verið skráð sem skilað til fyrirtækisins.

![Vinna með viðhaldsbeiðnir.](media/06-manage-maintenance-requests.png)

Á síðunni **Virk eignalán** geturðu skoðað lista yfir allar lánaeignir sem hefur ekki enn verið skilað til fyrirtækisins.

## <a name="register-loan-assets-as-returned"></a>Skráðu lánaeignir sem skilað er

1. Veldu **Eignastýring** \> **Eignalán** \> **Virk eignalán**.
2. Veldu eignalánið sem á að skrá sem skilað og veldu síðan **Skila eignaláni**.
3. Í reitnum **Skilað** skaltu slá inn dagsetningu og tíma.
4. Veljið **Í lagi**.
5. Endurnærðu **Virk eignalán** listasíðu og taktu eftir því að eignalánið birtist ekki lengur á listanum.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]