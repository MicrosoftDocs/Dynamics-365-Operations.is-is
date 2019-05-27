---
title: Talent-biðlari aftengist
description: Þetta efnisatriði útskýrir hvað eigi að gera ef viðskiptamaður aftengist umhverfi sínu og veit ekki hvers vegna.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 885e2d743cd2b01588546327840508f6f7e95958
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518235"
---
# <a name="talent-client-disconnects"></a>Talent-biðlari aftengist

[!include [banner](includes/banner.md)]

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

Verkvangur Microsoft Dynamics 365 for Talent aftengir notendur þegar tvær mismunandi lotur eru opnar á sama tíma fyrir sama notanda í sömu tegund af vafra. (Til dæmis er notandi A að skoða bæði umhverfi 1 og umhverfi 2 í Chrome.) Það skiptir ekki máli hvort notendur opni aðra vafraglugga eða aðra flipa. Talent aftengir eina af lotunum ef sömu notandaskilríki eru notuð til að skrá sig inn í bæði umhverfi 1 og umhverfi 2 á sama tíma og í sömu tegund af vafra.

**Lausn**

Gangið úr skugga um að aðeins eitt umhverfi í einu sé opið fyrir tiltekna tegund vafra. Notendur geta opnað margar lotur í sama umhverfinu (sem sagt marga flipa í sama vafranum).

Notendur sem vilja hoppa á milli tveggja umhverfa á sama tíma ættu að opna umhverfin í ólíkum tegundum vafra. (Til dæmis getur notandi A skoðað umhverfi 1 í Chrome og umhverfi 2 í Microsoft Edge.)
