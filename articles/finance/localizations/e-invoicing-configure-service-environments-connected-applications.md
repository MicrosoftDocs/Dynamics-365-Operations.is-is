---
title: Skilgreina þjónustuumhverfi og tengd forrit
description: Þessi grein veitir upplýsingar um hvernig á að stilla þjónustuumhverfi og tengd forrit.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 8ede98cfad685992bad3fb643ea46d6adcb08487
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269532"
---
# <a name="configure-service-environments-and-connected-applications"></a>Skilgreina þjónustuumhverfi og tengd forrit

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um hvernig á að stilla þjónustuumhverfi og tengd forrit. Þrjú skref eru að þessu ferli. Skref 1 er skylda og skref 2 og 3 eru valfrjáls.

## <a name="step-1-create-a-service-environment"></a>Skref 1: Stofna þjónustuumhverfi

Þegar þú býrð til þjónustuumhverfið þitt skaltu skilgreina listann yfir notendur sem geta sett hnattræna eiginleika í það. Fyrir sumar þessar aðstæður er valfrjást að skilgreina listann yfir ytri forrit sem geta haft samskipti við rafrænu reikningsfærsluþjónustuna. Settu upp númeraraðir ef þú notar þær við aðstæður.

Til að ljúka þessu skrefi, sjá [Þjónustuumhverfi](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>2. skref: Bættu við vottorðum og leynilyklum

Bættu tilvísun við Microsoft Azure lyklageymsluna og leynilyklana til að nota þá í aðstæðunum þínum. Þetta skref er áskilið ef aðgerðir í vinnslukeðjum nota vottorð og leynilykla fyrir stafræna undirskrift eða í samskiptum við ytri vefþjónustur.

Til að ljúka þessu skrefi skaltu skoða [Vottorð og leynilyklar viðskiptavina](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>Skref 3: Stilla tengd forrit

Til að setja upp samskipti milli Dynamics 365 Finance eða Dynamics 365 Supply Chain Management forrita og rafrænnar reikningsfærslu þarf að skilgreina Finance og Supply Chain Management til að búa til kallið í rafræna reikningsfærsluþjónustu og undirbúa viðskiptagögn í sameinuðu skipulagi sem hægt er að umbreyta í nauðsynlegt rafrænt snið. Forritin verða einnig að vinna rétt úr svörum frá þjónustunni. Hægt er að ljúka þessar skilgreiningu beint í umhverfi Finance eða Supply Chain Management eða þú getur lokið henni í Regulatory Configuration Service (RCS). Ef þú lýkur skilgreiningunni í RCS er hægt að setja hana upp í umhverfi Finance eða Supply Chain Management. Í þessu skrefi skráir þú tengda forritið fyrir uppsetningu færirbreytu.

Til að ljúka þessu skrefi skal skoða [Tengd forrit](e-invoicing-connected-applications.md).
