---
title: algengar spurningar um Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði veitir svör við algengum spurningum um Microsoft Dynamics 365 Commerce matsumhverfi.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b8d7d7364087dacf3b4479ab008609ecffeaacb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000976"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>algengar spurningar um Dynamics 365 Commerce matsumhverfi

[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir svör við algengum spurningum um Microsoft Dynamics 365 Commerce matsumhverfi.

**Er hægt að nota Commerce-matsumhverfi sem netverslun rafrænna viðskipta fyrir viðskiptavini sem innleiða smásölu eins og er?**

Nei. Commerce-matsumhverfi er aðeins fyrir mat. Ef þú þarft umhverfi fyrir viðskiptavini sem útfærir Retail skaltu hafa samband við Microsoft.

**Er hægt að nota Commerce-matsumhverfi til að úthluta eiginleikum rafrænna viðskipta ásamt fyrirliggjandi forriti/umhverfi sem innleiðir smásölu?**

Nei (aðallega). Íhlutir Commerce-mats eru aðeins í boði fyrir umhverfi sem samsvarar skilgreiningum sem eru tilgreindar í skilyrðum og úthlutunarleiðbeiningum. Þar að auki verða nauðsynleg grunnsýnigögn ekki tiltæk í umhverfum sem voru sett upp með upphaflegri útgáfu sem er eldri en 10.0.8. 

**Hvaða kostnaður fylgir því að setja upp Commerce-matsumhverfi á Microsoft Azure í gegnum Microsoft Dynamics Lifecycle Services?**

Hefðbundið Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce sýniútgáfuumhverfi höfuðstöðva (sýndarvél \[SV\]) verður hýst í Azure-áskriftinni þinni. Þú getur notað [Reiknivél fyrir verðlagningu í Azure](https://azure.microsoft.com/pricing/calculator/) að áætla þennan kostnað.

Aðrir þættir, svo sem Commerce Scale Unit, Commerce-vefsmiður og rafræna viðskiptasvæðið þitt verða í boði sem SaaS-þjónusta og hýst af Microsoft.

**Hvaða löng og svæði Azure eru studd eins og er fyrir Commerce-matsumhverfið?**

Aðeins er hægt að nota Commerce-matsumhverfið á svæðum Norður-Ameríku.

**Er til niðurhalanlegur sýndardiskur (VHD) sem hefur fullkominn OneBox sýndarvél (VM) valkost?**

Dynamics 365 Commerce og Commerce Scale Unit eru SaaS-þjónusta og verða að vera hýst í skýinu.

**Hversu lengi er hægt að nota matsumhverfi í Commerce?**

Commerce-matsumhverfið er með 30 daga gildistíma frá þeim degi þegar SaaS-íhlutir á borð við Commerce Scale Unit, Commerce-vefsmiður og rafrænt viðskiptasvæðið þitt er úthlutað.

**Get ég framlengt tímamörkunum fyrir matsumhverfið mitt í Commerce?**

Framlenging á tímamörkum er undantekning sem þarf að skoða sérstaklega fyrir hvert mál. Þú ættir að hafa samband við Microsoft samstarfsaðila þinn til að fá aðstoð.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi](cpe-overview.md)

[Úthluta Dynamics 365 Commerce matsumhverfi](provisioning-guide.md)

[Stilla Dynamics 365 Commerce matsumhverfi](cpe-post-provisioning.md)

[Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi](cpe-bopis.md)

[Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]