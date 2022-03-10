---
title: Stilltu þjónustuumhverfi og tengd forrit
description: Þetta efni veitir upplýsingar um hvernig á að stilla þjónustuumhverfi og tengd forrit.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c3366e75b4a6d3f33a1aac9e444236d9ae57c829
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371916"
---
# <a name="configure-service-environments-and-connected-applications"></a>Stilltu þjónustuumhverfi og tengd forrit

[!include [banner](../includes/banner.md)]

Þetta efni veitir upplýsingar um hvernig á að stilla þjónustuumhverfi og tengd forrit. Það eru þrjú skref í þessu ferli. Skref 1 er skylda og skref 2 og 3 eru valfrjáls.

## <a name="step-1-create-a-service-environment"></a>Skref 1: Búðu til þjónustuumhverfi

Þegar þú býrð til þjónustuumhverfi þitt skaltu tilgreina listann yfir notendur sem geta innleitt hnattvæðingareiginleika á það. Valfrjálst, fyrir sumar tilvikanna, skilgreinið lista yfir ytri forrit sem geta átt samskipti við rafræna reikningsþjónustu. Settu upp númeraraðir ef þú ætlar að nota þær í aðstæðum þínum.

Til að ljúka þessu skrefi, sjá [Þjónustuumhverfi](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>Skref 2: Bættu við vottorðum og leyndarmálum

Bættu við tilvísun í Microsoft Azure lykilhólf og leyndarmál til að nota þau í aðstæðum þínum. Þetta skref er skylt ef aðgerðir í vinnsluleiðslum nota vottorð og leyndarmál fyrir stafræna undirskrift eða samskipti við utanaðkomandi vefþjónustur.

Til að ljúka þessu skrefi, sjá [Viðskiptavinavottorð og leyndarmál](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>Skref 3: Stilltu tengd forrit

Til að setja upp samskipti á milli Dynamics 365 Finance eða Dynamics 365 Supply Chain Management forritum og rafrænum reikningum, verður þú að stilla fjármála- eða birgðakeðjustjórnun til að búa til símtalið til rafrænna reikningaþjónustunnar og undirbúa viðskiptagögn í sameinuðu skipulagi sem hægt er að breyta í tilskilið rafrænt snið. Umsóknir þurfa einnig að vinna rétt úr svörum frá þjónustunni. Þú getur klárað þessa stillingu beint í fjármála- eða framboðskeðjuumhverfi þínu, eða þú getur klárað hana í Regulatory Configuration Service (RCS). Ef þú lýkur uppsetningunni í RCS geturðu síðan sett hana í fjármála- eða framboðskeðjuumhverfið þitt. Í þessu skrefi muntu skrá tengda forritið fyrir uppsetningu á færibreytum.

Til að ljúka þessu skrefi, sjá [Tengd forrit](e-invoicing-connected-applications.md).
