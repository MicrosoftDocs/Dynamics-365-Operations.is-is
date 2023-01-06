---
title: Setja upp lausn Invoice capture
description: Þessi grein veitir upplýsingar um hvernig á að setja upp Invoice capture-lausn og samþætta hana við Microsoft Dynamics 365 Finance.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690995"
---
# <a name="install-the-invoice-capture-solution"></a>Setja upp lausn Invoice capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Ef þú settir lausnina upp í einkaforskoðun verður þú að fjarlægja gömlu lausnina áður en þú heldur áfram.

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að setja upp Invoice capture-lausn þarf að ljúka eftirfarandi skilyrðum:

1. Skráðu forrit og bættu leyniorði biðlara við Microsoft Azure Active Directory (Azure AD) undir Azure-áskriftinni þinni. Frekari upplýsingar er að finna í [Skrá vefforrit með AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Skráðu hjá þér gildin fyrir **Kenni forrits (biðlara)**, **Leyniorð biðlara** og **Kenni leigjanda** því þú þarft á þeim halda síðar.

2. Skráðu Azure forritið í Dynamics 365 Finance umhverfi. Frekari upplýsingar er að finna í [Skrá ytra forritið](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Uppsetning lausnarinnar

Til að setja upp lausn Invoice capture skal fara í AppSource og velja tengilinn fyrir forútgáfuna af [Dynamics 365 Invoice capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). Eftir að uppsetningunni er lokið sérðu lausnina uppsetta í völdu umhverfi í Power Apps.

Fylgdu eftirfarandi skrefum til að ljúka þessari uppsetningu.

1. Sæktu [stuðningslausnina](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) til að setja upp eftirfarandi upplýsingar:

    - Samskiptin milli Microsoft Power Platform og Finance-umhverfis
    - Tilvísunin er fyrir tengingu Dataverse og Office 365 Outlook sem verður notuð af rásinni.

2. Í Power Apps skal fara í umhverfið og velja **Flytja inn lausn**.
3. Veldu **Fletta**, veldu stuðningslausnapakka sem var sóttur og veldu síðan **Næsta**.
4. Veljið **Næst**.
5. Úthlutaðu núverandi tengingu eða stofnaðu nýja með því að velja **Ný tenging**.
6. Eftir að pakkinn hefur verið fluttur inn skaltu opna **Dynamics 365 Invoice capture – Uppsetningarverkfæri**.
7. Keyrðu skýjaflæðið til að setja upp tenginguna milli Invoice capture í Microsoft Power Platform og Finance.
8. Veljið **Keyra Run** og tilgreinið eftirfarandi færibreytur:

    - **Vefslóð Dynamics 365 Finance** – Vefslóð Finance-umhverfisins sem á að samþætta við.
    - **Leigjandakenni** – Auðkenni leigjanda fyrir Finance-umhverfið.
    - **Biðlarakenni** – Azure-forritskennið sem var skráð.
    - **Leyniorð biðlara** – Leynilykill biðlara sem var búið til fyrir Azure-forritið.
