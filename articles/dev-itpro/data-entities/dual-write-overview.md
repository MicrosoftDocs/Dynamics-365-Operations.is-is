---
title: Samþætting nærrirauntímagagna á milli Finance and Operations og Common Data Service.
description: Þetta efnisatriði veitir yfirlit yfir samþættingu á milli Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797229"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Samþætting nærrirauntímagagna á milli Finance and Operations og Common Data Service.

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Í núverandi stafræna heimi nota vistkerfi fyrirtækja Microsoft Dynamics 365 pakkann sem heild. Vegna þess að gögn frá fólki, viðskiptavinum, aðgerðum og Internet of Things (IoT) tækjum streyma inn í eina uppsprettu er tækifæri fyrir stafrænar endurgjafarlykkjur. Til að ná þessari reynslu er samþætting á milli Dynamics 365 for Finance and Operations og Dynamics 365 fyrir forritið Customer Engagement nauðsynleg. Forrit Customer Engagement eru byggð ofan á Common Data Service. Sameining gagna Finance and Operations við Common Data Service gerir forritum Customer Engagement kleift að eiga samræmd og lipur samskipti við Finance and Operations.

Finance and Operations og Common Data Service bjóða upp á samstillingu gagna í rauntíma milli forritanna Finance and Operations og Customer Engagement með tvískiptum ramma. Umfjöllunin er breið og spannar 28 yfirborðssvið Finance and Operations. Markmiðið er að bjóða upp á „One Dynamics 365“ notendaupplifun með óaðfinnanlegu gagnastreymi sem tengir viðskiptaferla milli forrita.

![Yfirlitsmynd arkitektúrs](media/dual-write-overview.jpg)

Eftirfarandi gildistillögur eru í boði fyrir viðskiptavini:

+ [Stigveldi fyrirtækis í Common Data Service](dual-write-organization.md)
+ [Fyrirtækishugtak í Common Data Service](dual-write-company.md)
+ [Samþættur aðalviðskiptavinur](dual-write-customer.md)
+ [Samþættur aðallánardrottinn](dual-write-vendor.md)
+ Sameinað afurðarsniðmát

## <a name="system-requirements"></a>Kerfiskröfur

Samstillt, tvíátta, nær rauntíma gagnaflæði krefst eftirfarandi útgáfa:

+ Microsoft Dynamics 365 for Finance and Operations útgáfa 10.0.4 (júlí 2019) með verkvangsuppfærslu 28 eða hærra
+ Microsoft Dynamics 365 for Customer Engagement útgáfa 9.1. (4.2) eða nýrri

## <a name="setup-instructions"></a>Leiðbeiningar um uppsetningu

Fylgdu þessum skrefum til að setja upp samþættingu á milli Finance and Operations og Common Data Service.
    
1. Upplýsingar um uppsetningu tvískiptakerfisins er að finna í [skref-fyrir-skref leiðbeiningar](https://aka.ms/dualwrite-docs) um tilkynningu forskoðunar á tvöföldum skrifum.
2. Sæktu og settu upp lausnina úr [Finance and Operations, Common Data Service og samþættingu Customer Engagement](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer hópur. Pakkinn inniheldur fimm lausnir:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Fylgdu framkvæmdarskipuninni fyrir [samstilla fyrstu tilvísunargögn](dual-write-initial.md).
4. Ef þú lendir í tvískiptum samstillingarvandamálum skaltu skoða [Úrræðaleiðbeiningar fyrir samþættingu gagna](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Þú getur ekki keyrt tvískipt skrif og [Viðfang til sjóðsstreymis](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) hlið við hlið. Ef þú ert að keyra lausnina Viðfang til sjóðsstreymis verður þú að fjarlægja hana. Þú verður einnig að slökkva á tvöföldum skrifasniðmátum viðskiptavinar og lánardrottins sem eru hluti af lausninni Viðfang til sjóðsstreymis.
