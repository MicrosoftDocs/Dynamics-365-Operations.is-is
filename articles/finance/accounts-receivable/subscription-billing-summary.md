---
title: Yfirlit yfir áskriftargreiðslur
description: Þetta efni lýsir innheimtu áskriftar í Microsoft Dynamics 365 Fjármál.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 9d46492cca3cc435048fa497f6b1f3a28b77140a
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644528"
---
# <a name="subscription-billing-overview"></a>Yfirlit yfir áskriftargreiðslur

[!include [banner](../includes/banner.md)]

Innheimta áskriftar gerir fyrirtækjum kleift að stjórna áskriftartekjum og endurteknum innheimtu í gegnum innheimtuáætlanir. Auðvelt er að stjórna flóknum verðlagningar- og innheimtulíkönum og tekjuúthlutun og þau eru innheimt og viðurkennd á línustigi. Fjölþátta tekjuúthlutun gerir ráðstöfun tekna kleift að uppfylla alþjóðlega reikningsskilastaðla (International Financial Reporting Standard 15\[ IFRS 15\]) og almennt viðurkenndar reikningsskilareglur (US GAAP) staðla (reikningsskilastaðla Codification Topic 606\[ ASC 606\]).

Lausnin hefur þrjár einingar sem hægt er að nota sjálfstætt. Að öðrum kosti er hægt að nota allar þrjár einingarnar saman.

- **Endurtekinn samningsreikningur** – Þessi eining gerir endurtekna innheimtu og verðstýringu kleift að veita stjórn á verðlagningu og innheimtubreytum, endurnýjun samnings og samstæðureikninga.
- **Frestun tekna og gjalda** – Þessi eining útilokar handvirka ferla og ósjálfstæði á ytri kerfum með því að stjórna tekjum og gera rauntíma innsýn í mánaðarlegar endurteknar tekjur.
- **Fjölþátta tekjuúthlutun** – Þessi eining hjálpar til við að fara eftir tekjum með því að meðhöndla verðlagningu og tekjuúthlutun yfir marga hluti.

Fyrir frekari upplýsingar um innheimtu áskriftar, sjá [Innheimta áskriftar Power BI efni](sub-bill-power-bi.md).

Innheimta áskriftar er virkjuð í gegnum **Eiginleikastjórnun**. Hins vegar er ekki hægt að nota það með **Tekjufærsla** eiginleiki. Þess vegna verður þú að slökkva á þeim eiginleika áður en þú virkjar innheimtu áskriftar.

1. Í **Eiginleikastjórnun** vinnusvæði, á **Allt** flipi, slá inn **Tekjufærsla** í síunni og veldu síðan eiginleikaheitið sem síu.
2. Veldu **Tekjufærsla** eiginleiki og veldu síðan **Slökkva**.
3. Í **Eiginleikaheiti** sía, slá inn **Innheimta áskriftar**, og veldu síðan mátsíuna.
4. Veldu **Innheimta áskriftar** eiginleiki og veldu síðan **Virkja**.
5. Veldu eina af þremur einingum af fyrri listanum og veldu síðan **Virkja**. Endurtaktu þetta skref fyrir hverja af hinum tveimur einingunum.

    > [!IMPORTANT]
    > The **Innheimta áskriftar** eiginleikann verður að vera virkur áður en þú getur virkjað einhverja af þessum þremur einingum.
