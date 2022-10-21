---
title: Settu upp Invoice capture lausnina
description: Þessi grein veitir upplýsingar um hvernig á að setja upp reikningsupptökulausnina og samþætta hana Microsoft Dynamics 365 Fjármál.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690995"
---
# <a name="install-the-invoice-capture-solution"></a>Settu upp Invoice capture lausnina

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Ef þú settir upp lausnina í einkaforskoðun verður þú að fjarlægja gömlu lausnina áður en þú heldur áfram.

## <a name="prerequisites"></a>Forkröfur

Áður en þú getur sett upp reikningsupptökulausnina þarftu að uppfylla eftirfarandi skilyrði:

1. Skráðu forrit og bættu leyndarmáli viðskiptavinar við Microsoft Azure Active Directory (Azure AD) undir Azure áskriftinni þinni. Fyrir frekari upplýsingar, sjá [Skráðu vefforrit hjá AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Taktu eftir **Auðkenni umsóknar (viðskiptavinar).**, **viðskiptavinar**, og **Auðkenni leigjanda** gildi, því þú munt þurfa á þeim að halda síðar.

2. Skráðu Azure forritið í Dynamics 365 Finance umhverfi. Fyrir frekari upplýsingar, sjá [Skráðu ytri umsókn þína](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Settu upp og settu upp lausnina

Til að setja upp Invoice capture lausnina skaltu fara á AppSource, og veldu hlekkinn fyrir forskoðunarútgáfuna af [Dynamics 365 Invoice handtaka](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). Eftir að uppsetningunni er lokið muntu sjá lausnina uppsetta í völdu umhverfi í Power Apps.

Til að ljúka uppsetningunni skaltu fylgja þessum skrefum.

1. Sækja [aðstoðarlausn](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) til að setja upp eftirfarandi upplýsingar:

    - Samskiptin milli Microsoft Power Platform og fjármálaumhverfi
    - Tengingartilvísunin fyrir Dataverse og Office 365 Outlook sem verður notað af rásinni

2. Í Power Apps, farðu í umhverfið þitt og veldu **Innflutningslausn**.
3. Veldu **Skoðaðu**, veldu aðstoðarlausnarpakkann sem þú sóttir niður og veldu síðan **Næst**.
4. Veljið **Næst**.
5. Úthlutaðu núverandi tengingu eða búðu til nýja með því að velja **Nýtt samband**.
6. Eftir að pakkinn hefur verið fluttur inn skaltu opna **Dynamics 365 Invoice capture – Uppsetningarverkfæri**.
7. Keyrðu skýjaflæðið til að setja upp tenginguna milli reikningsfangalausnarinnar í Microsoft Power Platform og Fjármál.
8. Veldu **Hlaupa**, og tilgreindu eftirfarandi færibreytur:

    - **Dynamics 365 Finance URL** – Vefslóð fjármálaumhverfisins sem þú vilt samþætta við.
    - **Auðkenni leigjanda** – Auðkenni leigjanda fyrir fjármálaumhverfið.
    - **Auðkenni viðskiptavinar** – Azure forritauðkennið sem var skráð.
    - **Leyndarmál viðskiptavinar** – Biðlaraleyndarmálið sem var búið til fyrir Azure forritið.
