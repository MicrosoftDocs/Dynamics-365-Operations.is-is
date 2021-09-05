---
title: algengar spurningar um Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði veitir svör við algengum spurningum um Microsoft Dynamics 365 Commerce matsumhverfi.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e8a3e760353b351d42aff82c0d372d2aca350cd2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343559"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce algengar spurningar um matsumhverfi

[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir svör við algengum spurningum um Microsoft Dynamics 365 Commerce matsumhverfi.

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>Er hægt að nota Commerce-matsumhverfi sem netverslun rafrænna viðskipta fyrir viðskiptavini sem innleiða smásölu eins og er?

Nei. Commerce-matsumhverfi er aðeins fyrir mat. Ef þú þarft umhverfi fyrir viðskiptavini sem útfærir Retail skaltu hafa samband við Microsoft.

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>Er hægt að nota Commerce-matsumhverfi til að úthluta eiginleikum rafrænna viðskipta ásamt fyrirliggjandi forriti/umhverfi sem innleiðir smásölu?

Nei (aðallega). Íhlutir Commerce-mats eru aðeins í boði fyrir umhverfi sem samsvarar skilgreiningum sem eru tilgreindar í skilyrðum og úthlutunarleiðbeiningum. Þar að auki verða nauðsynleg grunnsýnigögn ekki tiltæk í umhverfum sem voru sett upp með upphaflegri útgáfu sem er eldri en 10.0.8. 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>Hvaða kostnaður fylgir því að setja upp Commerce-matsumhverfi á Microsoft Azure í gegnum Microsoft Dynamics Lifecycle Services?

Hefðbundið Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce sýniútgáfuumhverfi höfuðstöðva (sýndarvél \[SV\]) verður hýst í Azure-áskriftinni þinni. Þú getur notað [Reiknivél fyrir verðlagningu í Azure](https://azure.microsoft.com/pricing/calculator/) að áætla þennan kostnað.

Aðrir þættir, svo sem Commerce Scale Unit, Commerce-vefsmiður og rafræna viðskiptasvæðið þitt verða í boði sem SaaS-þjónusta og hýst af Microsoft.

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>Hvaða löng og svæði Azure eru studd eins og er fyrir Commerce-matsumhverfið?

Aðeins er hægt að nota Commerce-matsumhverfið á svæðum Norður-Ameríku.

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>Er til niðurhalanlegur sýndardiskur (VHD) sem hefur fullkominn OneBox sýndarvél (VM) valkost?

Dynamics 365 Commerce og Commerce Scale Unit eru SaaS-þjónusta og verða að vera hýst í skýinu.

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>Hversu lengi er hægt að nota matsumhverfi í Commerce?

Commerce-matsumhverfið er með 30 daga gildistíma frá þeim degi þegar SaaS-íhlutir á borð við Commerce Scale Unit, Commerce-vefsmiður og rafrænt viðskiptasvæðið þitt er úthlutað.

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>Get ég framlengt tímamörkunum fyrir matsumhverfið mitt í Commerce?

Framlenging á tímamörkum er undantekning sem þarf að skoða sérstaklega fyrir hvert mál. Þú ættir að hafa samband við Microsoft samstarfsaðila þinn til að fá aðstoð.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi](cpe-overview.md)

[Úthluta Dynamics 365 Commerce matsumhverfi](provisioning-guide.md)

[Stilla Dynamics 365 Commerce matsumhverfi](cpe-post-provisioning.md)

[Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi](cpe-bopis.md)

[Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
