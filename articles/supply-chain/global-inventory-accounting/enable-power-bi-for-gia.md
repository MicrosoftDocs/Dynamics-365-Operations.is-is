---
title: Virkja Power BI fyrir altækt birgðabókhald
description: Þetta efnisatriði lýsir hvernig á að virkja Microsoft Power BI fyrir altækt birgðabókhald.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0b00de29a4f12719e469c063861b52e0fc20c5f1
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641112"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Virkja Power BI fyrir altækt birgðabókhald

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Hægt er að festa reiti, yfirlit og skýrslur af reikningnum þínum á [PowerBI.com](https://powerbi.com/) á vinnusvæðið þitt hjá Microsoft Dynamics 365 forritum.

## <a name="prerequisites"></a>Forkröfur

Eftirfarandi skilyrði verða að vera til staðar áður en hægt er að virkja Power BI skýrslugjöf:

- Þú verður að vera kerfisstjóri í Dynamics 365-forritinu.
- Nauðsynlegt er að vera með reikning hjá [PowerBI.com](https://powerbi.com/).
- Nauðsynlegt er að vera með a.m.k. eitt yfirlit og eina skýrslu á Power BI-reikningnum.
- Nauðsynlegt er að vera stjórnandi fyrir Azure Active Directory (Azure AD) reikninginn.
- Lénið Azure AD verður að vera sama lénið og þú notaðir fyrir [PowerBI.com](https://powerbi.com/) reikninginn.

## <a name="setup"></a>Setja upp

Fylgið þessum skrefum til að setja upp Power BI-samþættingu.

1. Skráðu þig inn í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Farið í **Samnýtt eignasafn**, veljið **Power BI skýrslulíkan** sem eignagerðina og sækið pakkann **Altækt birgðabókhald**. 
1. Skráið ykkur inn á [PowerBI.com](https://app.powerbi.com/) og hlaðið upp **Altæku birgðabókhaldi** Power BI skýrsluskrá með því að fylgja þessum skrefum:

    1. Veljið **Nýtt**.
    1. Veljið **Hlaða upp skrá**.
    1. Veljið **Altækt birgðabókhald** Power BI skýrsluskrá.

1. Stillið **Altækt birgðabókhald** Power BI skýrslu með því að fylgja þessum skrefum:

    1. Farið á **Vinnusvæðið mitt**, finnið gagnasafnið fyrir altækt birgðabókhald og síðan í valmyndinni **Valkostir** skal velja **Stillingar**.
    1. Í **Stillingar fyrir altækt birgðabókhald** skal víkka út **Færibreytur** og uppfæra allar færibreytur eftir þörfum. Einkum skal gæta þess að skoða eftirfarandi stillingar:
        1. Skrifa yfir sjálfgefin **Dataverse vefslóð** og **umhverfisauðkenni** með því að nota gildin sem finna má á **umhverfisupplýsingasíðu** í LCS (í **Power Platform samþættingarhlutanum**).
        1. Veldu tengilinn **Breyta skilríkjum** við hliðina á **Cds**-merkinu í hlutanum **Skilríki gagnagjafa**. Skráðu þig síðan inn á Dataverse reikninginn þinn með **OAuth2** sannvottunaraðferðinni.
    1. Staðfestu að Power BI skýrslurnar á **vinnusvæðinu mínu \> Skýrslur \> altækt birgðabókhald** virki nú rétt og sýni efni úr kerfinu.

1. Skrá forritið eins og lýst er í [Stilla PowerBI.com samþættingu](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).
1. Samþættið **Altækt birgðabókhald** Power BI skýrsluskrá við Dynamics 365 Supply Chain Management með því að fylgja þessum skrefum:

    1. Farið í **Kerfisstjórnun \> Uppsetning \> Skilgreining PowerBI.com**.
    1. Veljið **Breyta**.
    1. Veldu **Gera PowerBI.com-samþættingu virka**.
    1. Í reitinn **Kenni forrits** skal slá inn kenni forrits.
    1. Í reitinn **Forritslykill** skal slá inn lykil forrits.
    1. Veldu **Vista**.

1. Endurhlaðið síðunni þannig að innskráningargluggi Power BI birtist.
1. Í flipanum **Valkostir** skal velja **Opna skýrslulista** og síðan velja **Altækt birgðabókhald** Power BI skýrsluskrá sem var hlaðin upp hér áður.
1. Endurhlaðið síðuna. Þú ættir að sjá að skýrslunni hefur verið bætt við.
1. Undir **Power BI skýrslur** skal velja tengilinn **Altækt birgðabókhald**.

Frekari upplýsingar er að finna í [Skilgreina samþættingu PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
