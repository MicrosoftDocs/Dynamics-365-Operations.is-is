---
title: Afþakka söfnun aðgerðatilvika á vef
description: Þessi grein útskýrir hvernig þú getur látið gesti á vefsíðunni þinni afþakka söfnun vefvirkniviðburða í Microsoft Dynamics 365 Commerce.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78d3f795820eb36d1a81fb28875456e7471f8971
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878400"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Afþakka söfnun aðgerðatilvika á vef
[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig þú getur látið viðskiptavini afþakka söfnun vefvirkniviðburða í Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce gerir stjórnendum vefsvæða kleift að greina vefnotkun notenda þeirra á vefsvæðum rafrænna viðskipta. Á þann hátt er hægt að skilja hvernig vefsvæði þeirra eru notuð og þeir geta fínstillt vefsvæðin til að veita bætta notendaupplifun og uppfylla markmið fyrirtækis.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Leiðir fyrir stjórnendur til að innleiða afþökkunarupplifun

Stjórnendur hafa þrjár leiðir til að innleiða afþökkunarupplifun.

### <a name="opt-out-on-behalf-of-users"></a>Afþakka fyrir hönd notenda

Í reikningsstjórnun í Commerce Headquarters (HQ) geta stjórnendur afþakkað fyrir hönd notenda.

1. Í HQ-biðlaranum, á síðunni **Allir viðskiptavinir**, skal leita að og velja viðskiptavin.
1. Á upplýsingasíðu viðskiptavinar, á **Retail** flýtiflipa, í **Persónuvernd**-hluta skal stilla **Ekki rekja vefnotkun** á **Já**.

    ![Persónuverndarstillingar.](media/Disablepersonalizationpart2.png)

1. Veljið **Vista** og lokið síðan skjámyndinni.

### <a name="module-based-opt-out-experience"></a>Eining byggð á afþakkunarreynslu

Stjórnendur geta leyft sannvottuðum notendum að afþakka söfnun vefnotkunar sjálfir. Til að bjóða upp á þessa afþakkunarupplifun skaltu bæta við afþakkunareiningunni fyrir notendur á prófílsíðum viðskiptavinarreiknings.

### <a name="custom-extensions"></a>Sérsniðnar viðbætur

Stjórnendur geta búið til sínar eigin viðbætur til að stjórna afþökkunarupplifuninni fyrir notendur. Fyrir frekari upplýsingar, sjá [Hringdu í smáforritaskil smásölumiðlara](e-commerce-extensibility/call-retail-server-apis.md) og [Stækkanleiki á netinu](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
