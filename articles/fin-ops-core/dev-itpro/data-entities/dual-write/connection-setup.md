---
title: Studdar atburðarás fyrir tvískipt skrifun
description: Þetta efni lýsir atburðarásum sem eru studdar fyrir tvískipt skrifun.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b4f69e7933bc5a50cccad6911c99cf08d2768578
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818597"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Studdar atburðarás fyrir tvískipt skrifun

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Þú getur sett upp tvískipt samband milli Finance and Operations umhverfis og Common Data Service umhverfis.

+ **Finance and Operations umhverfi** býður upp á undirliggjandi verkvanginn fyrir **Finance and Operations forrit** (til dæmis Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Retail).
+ **Common Data Service-umhverfi** veitir undirliggjandi verkvang fyrir **líkanadrifin forrit í Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Mannauður í Finance and Operations styður tengingu tvískiptra skrifa, en Dynamics 365 Human Resources-forritið gerir það ekki.

Skipulagið er mismunandi eftir áskrift og umhverfi.

+ Fyrir ný tilvik af forrit Finance and Operations hefst uppsetningin á tvískiptri tengingu í Microsoft Dynamics Lifecycle Services (LCS). Ef þú ert með leyfi fyrir Power Platform geturðu fengið nýtt umhverfi Common Data Service ef leigjandi þinn hefur ekki slíkt.
+ Fyrir núverandi tilvik forrita Finance and Operations hefst uppsetning tvískiptrar tengingar í umhverfi Finance and Operations.

Eftirfarandi uppsetningaraðstæður eru studdar:

+ [Nýtt forritstilvik Finance and Operations og nýtt líkanadrifið forritstilvik](#new-new)
+ [Nýtt forritstilvik Finance and Operations og fyrirliggjandi líkanadrifið forritstilvik](#new-existing)
+ [Nýtt forritstilvik Finance and Operations sem er með sýnigögn og nýtt líkanadrifið forritstilvik](#new-demo-new)
+ [Nýtt forritstilvik Finance and Operations sem er með sýnigögn og fyrirliggjandi líkanadrifið forritstilvik](#new-demo-existing)
+ [Fyrirliggjandi forritstilvik Finance and Operations og nýtt eða fyrirliggjandi líkanadrifið forritstilvik](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>Nýtt forritstilvik Finance and Operations og nýtt líkanadrifið forritstilvik

Til að koma á tvískiptri tengingu milli nýs dæmi um forrit Finance and Operations sem hefur engin gögn og nýtt tilvik af líkanadrifnu forriti í Dynamics 365 fylgirðu skrefunum í [Tvískipt uppsetning úr Lifecycle Services](lcs-setup.md). Þegar uppsetningu tengingarinnar er lokið fara eftirfarandi aðgerðir sjálfkrafa fram:

- Nýtt, tómt umhverfi Finance and Operations er veitt.
- Nýtt, tómt tilvik af líkanadrifnu forriti er útbúið þar sem CRM frumlausnin er sett upp.
- Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.
- Einingakort eru virk fyrir samstillingu í beinni.

Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>Nýtt forritstilvik Finance and Operations og fyrirliggjandi líkanadrifið forritstilvik

Til að koma á tvískiptri tengingu milli nýs dæmi um forrit Finance and Operations sem hefur engin gögn og fyrirliggjandi tilvik af líkanadrifnu forriti í Dynamics 365 fylgirðu skrefunum í [Tvískipt uppsetning úr Lifecycle Services](lcs-setup.md). Þegar uppsetningu tengingarinnar er lokið fara eftirfarandi aðgerðir sjálfkrafa fram:

- Nýtt, tómt umhverfi Finance and Operations er veitt.
- Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.
- Einingakort eru virk fyrir samstillingu í beinni.

Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.

Til að samstilla fyrirliggjandi gögn Common Data Service við forrit Finance and Operations fylgirðu þessum skrefum.

1. Stofnaðu nýtt fyrirtæki í forriti Finance and Operations.
2. Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.
3. [Ræstu](bootstrap-company-data.md) Common Data Service-gögnin með því að nota þriggja stafa fyrirtækjakóða Alþjóðlegu staðlastofnunarinnar (ISO).

Þar sem tvískipt skrifun er í samstillingarstillingu í beinni fara gögnin úr Common Data Service sjálfkrafa að flæða í forrit Finance and Operations.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>Nýtt forritstilvik Finance and Operations sem er með sýnigögn og nýtt líkanadrifið forritstilvik

Til að koma á tvískiptri tengingu milli nýs dæmi um forrit Finance and Operations sem er með kynningargögn og nýtt tilvik líkanadrifins forrits í Dynamics 365 fylgirðu skrefunum í hlutanum [Nýtt forritstilvik Finance and Operations og nýtt tilvik líkanadrifins forrits](#new-new) fyrr í þessu efni. Þegar uppsetningu á tengingunni er lokið, ef þú vilt samstilla kynningargögnin við líkanadrifna forritið, fylgdu þessum skrefum.

1. Opnaðu forritið Finance and Operations af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.
2. Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>Nýtt forritstilvik Finance and Operations sem er með sýnigögn og fyrirliggjandi líkanadrifið forritstilvik

Til að koma á tvískiptri tengingu milli nýs dæmi um forrit Finance and Operations sem er með kynningargögn og fyrirliggjandi tilvik líkanadrifins forrits í Dynamics 365 fylgirðu skrefunum í hlutanum [Nýtt forritstilvik Finance and Operations og fyrirliggjandi tilvik líkanadrifins forrits](#new-existing) fyrr í þessu efni. Þegar uppsetningu á tengingunni er lokið, ef þú vilt samstilla kynningargögnin við líkanadrifna forritið, fylgdu þessum skrefum.

1. Opnaðu forritið Finance and Operations af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.
2. Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.

Til að samstilla fyrirliggjandi gögn Common Data Service við forrit Finance and Operations fylgirðu þessum skrefum.

1. Stofnaðu nýtt fyrirtæki í forriti Finance and Operations.
2. Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.
3. [Ræstu](bootstrap-company-data.md) Common Data Service-gögnin með því að nota þriggja stafa fyrirtækjakóða ISO.

Þar sem tvískipt skrifun er í samstillingarstillingu í beinni fara gögnin úr Common Data Service sjálfkrafa að flæða í forrit Finance and Operations.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>Fyrirliggjandi forritstilvik Finance and Operations og nýtt eða fyrirliggjandi líkanadrifið forritstilvik

Skipulag á tvískiptri tengingu milli núverandi dæmi um forrit Finance and Operations og nýtt eða núverandi dæmi um líkanadrifið forrit í Dynamics 365 á sér stað í umhverfi Finance and Operations.

1. Settu upp tenginguna úr forriti Finance and Operations.
2. Til að samstilla núverandi Common Data Service-gögn við forrit Finance and Operations, [skaltu ræsa](bootstrap-company-data.md) Common Data Service-gögnin með þriggja stafa ISO fyrirtækjakóða.

Þar sem tvískipt skrifun er í samstillingarstillingu í beinni fara gögnin úr Common Data Service sjálfkrafa að flæða í forrit Finance and Operations.
