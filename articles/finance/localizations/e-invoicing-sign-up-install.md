---
title: Skráðu þig í og settu upp rafræna reikningaþjónustu
description: Þessi grein veitir upplýsingar um hvernig á að skrá sig í og setja upp rafræna reikningaþjónustu.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 57314058883e60599bc51d91a65b0daeae724bb7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865527"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Skráðu þig í og settu upp rafræna reikningaþjónustu

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um hvernig á að skrá sig í og setja upp rafræna reikningaþjónustu. Það eru fjögur skref í þessu ferli. Skref 1 til 3 eru nauðsynleg og skref 4 er valfrjálst.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>Skref 1: Skráðu þig í Regulatory Configuration Service

Regulatory Configuration Service (RCS) veitir uppsetningu og hönnunarupplifun sem er notuð til að stilla rafræna reikningagerð. Tilföng eins og umhverfi og eiginleikar rafrænna reikninga eru búnar til, viðhaldið og stjórnað í RCS. Þegar tilföngin eru tilbúin eru þau birt til rafrænna reikningaþjónustunnar.

Fyrir frekari upplýsingar um RCS, sjá [Regulatory Configuration Services (RCS) - Hnattvæðingareiginleikar](rcs-globalization-feature.md).

Til að skrá þig í RCS skaltu fara á [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) síðu.

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Skref 2: Settu upp viðbótina fyrir örþjónustur í Microsoft Dynamics Lífsferilsþjónusta

Rafræn reikningaþjónusta er safn örþjónustu sem er hýst í gagnaverum Microsoft. Sjálfgefið er að viðskiptavinir Dynamics 365 Finance og Dynamics 365 Supply Chain Management hafa ekki aðgang að rafrænum reikningaþjónustu. Þú verður að setja það upp sem viðbót Microsoft Dynamics Lífsferilsþjónusta (LCS). Þegar þú setur upp viðbótina er fjármála- eða framboðskeðjuumhverfi þitt skráð í skrá yfir forrit sem hafa leyfi til að tengjast rafrænum reikningaþjónustu.

Til að ljúka þessu skrefi, sjá [Settu upp viðbótina fyrir örþjónustur í Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>Skref 3: Settu upp RCS

Þú verður að setja upp samþættingu RCS og rafrænna reikningaþjónustunnar. Þú verður líka að setja upp helstu þætti.

Til að ljúka þessu skrefi, sjá [Settu upp reglustillingarþjónustu (RCS)](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Skref 4:Microsoft Power Platform admin tilvísun í viðbót

Sumar aðstæður krefjast samþættingar við Dataverse í umfangi Microsoft Power Platform.

Eins og er, er þessi uppsetning skylda ef þú notar rafrænar reikningslausnir fyrir indónesískar rafrænar reikningsfærslur. Hins vegar er það valfrjálst fyrir rafræna reikninga í Sádi-Arabíu. Fyrir frekari upplýsingar, sjá [Aðgengi að eiginleikum rafrænna reikninga eftir löndum eða svæðum](e-invoicing-country-specific-availability.md).

Til að ljúka þessu skrefi, sjá [Microsoft Power Platform admin tilvísun í viðbót](e-invoicing-power-platform-plug-in.md).
