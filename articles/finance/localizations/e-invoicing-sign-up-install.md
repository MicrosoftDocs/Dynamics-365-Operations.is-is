---
title: Skráðu þig fyrir og settu upp þjónustu fyrir rafræna reikninga
description: Í þessari grein er að finna upplýsingar um hvernig á að skrá sig fyrir og setja upp rafræna reikningsfærsluþjónustu.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283958"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Skráðu þig fyrir og settu upp þjónustu fyrir rafræna reikninga

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna upplýsingar um hvernig á að skrá sig fyrir og setja upp rafræna reikningsfærsluþjónustu. Það eru fjögur skref í þessu ferli. Skref 1 til 3 eru nauðsynleg og skref 4 er valfrjálst.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>1. Skref: Skráðu þig í Regulatory Configuration Service

Regulatory Configuration Service (RCS) veitir þá stillingar- og hönnunarupplifun sem er notuð til að stilla Rafræna reikninga. Tilföng eins og umhverfi og eiginleikar rafrænnar reikningsfærslu eru búin til, unnið með og stjórnað í RCS. Þegar tilföngin eru tilbúin eru þau birt í rafrænni reikningsfærsluþjónustu.

Frekari upplýsingar um RCS er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md)

Til að skrá þig í RCS skaltu fara [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) síðuna.

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Skref 2: Setja upp innbótina fyrir örþjónusta í Microsoft Dynamics Lifecycle Services

Þjónusta fyrir rafræna reikninga er örþjónusta sem er hýst í gagnaverum Microsoft. Sjálfgefið er að viðskiptavinir Dynamics 365 Finance og Dynamics 365 Supply Chain Management hafi ekki aðgang að Rafræn reikningsfærsluþjónusta. Þú verður að setja það upp sem viðbót í Microsoft Dynamics Lifecycle Services (LCS). Þegar þú setur upp innbótina er Finance eða Supply Chain Management skráð í skrá yfir forrit sem hafa leyfi til að tengjast rafrænum reikningum.

Til að ljúka þessu skrefi skal skoða [Setja upp innbótina fyrir microservices í Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>3. skref: Setja upp RCS

Setja verður upp samþættingu milli RCS og rafrænnar reikningsfærsluþjónustu. Einnig þarf að setja upp aðalíhluti.

Til að ljúka þessu skrefi, sjá [Settu upp Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Skref 4: Microsoft Power Platform-tilvísun stjórnanda fyrir viðbót

Sumar aðstæður krefjast samþættingar við Dataverse innan Microsoft Power Platform.

Eins og er er skylt að nota þessa uppsetningu ef nota á rafrænar reikningslausnir fyrir indónesískar rafrænar reikningsaðstæður. Hins vegar er það valfrjálst fyrir sádi-arabískar rafrænar reikningsaðstæður. Frekari upplýsingar eru í [Framboð á eiginleikum rafrænnar reikningsfærslu eftir landi eða svæði](e-invoicing-country-specific-availability.md).

Til að ljúka þessu skrefi skal skoða [Microsoft Power Platform-tilvísun stjórnanda fyrir viðbót](e-invoicing-power-platform-plug-in.md).
