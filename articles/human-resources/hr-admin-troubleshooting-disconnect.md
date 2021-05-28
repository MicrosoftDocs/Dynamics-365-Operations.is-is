---
title: Biðlari rýfur tengingu
description: Þessi útskýrir hvað eigi að gera ef viðskiptamaður aftengist umhverfi sínu og veit ekki hvers vegna.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db0e8efec1a5a6f01c9b7c4d9334a959fc42886b
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027988"
---
# <a name="client-disconnects"></a>Biðlari rýfur tengingu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Umhverfisupplýsingar** 

Þetta vandamál getur komið upp í öllum umhverfum.
 
**Einkenni** 

Viðskiptamaður aftengist umhverfi sínu og veit ekki hvers vegna. Viðskiptamaður fær eitt af eftirfarandi villuboðum:

- Tengingin hefur rofnað. Smellið á „Loka“ til að halda áfram vinnu.
- Tenging virðist hafa rofnað við netkerfi, smellið á „Reyna aftur“ til að reyna aftur.

**Rautt flagg**

Þetta vandamál kemur oft upp þegar notendur eru á innleiðingarstiginu, þegar þeir eru að bera saman upplýsingar þvert yfir framleiðslu og prófunarumhverfi, og gleyma því að þeir eru flakka frá einni lotu til annarrar. Ef notendur eru á þessu stigi eru mestar líkur á þessu vandamáli.

**Úthreyfing** 

**Tegundir vafra:** Google Chrome, Internet Explorer og Microsoft Edge

Microsoft Dynamics 365 Human Resources aftengir notendur þegar tvær mismunandi lotur eru opnar á sama tíma fyrir sama notanda í sömu tegund af vafra. (Til dæmis er notandi A að skoða bæði umhverfi 1 og umhverfi 2 í Chrome.) Það skiptir ekki máli hvort notendur opni aðra vafraglugga eða aðra flipa. Human Resources aftengir eina af lotunum ef sömu notandaskilríki eru notuð til að skrá sig inn í bæði umhverfi 1 og umhverfi 2 á sama tíma og í sömu tegund af vafra.

**Lausn**

Gangið úr skugga um að aðeins eitt umhverfi í einu sé opið fyrir tiltekna tegund vafra. Notendur geta opnað margar lotur í sama umhverfinu (sem sagt marga flipa í sama vafranum).

Notendur sem vilja hoppa á milli tveggja umhverfa á sama tíma ættu að opna umhverfin í ólíkum tegundum vafra. (Til dæmis getur notandi A skoðað umhverfi 1 í Chrome og umhverfi 2 í Microsoft Edge.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]