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
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 07472188051aea7084142cc417c6d725462cf4f9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205254"
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
