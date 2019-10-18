---
title: Samþætting nærrirauntímagagna á milli Finance and Operations og Common Data Service.
description: Þetta efni veitir yfirlit yfir samþættingu á milli Finance and Operations og Common Data Service.
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
ms.openlocfilehash: b7d9e6be6fb2fef85bcf1182f89b8e370abea3d6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184486"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Samþætting gagna í næstum rauntíma við Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Í núverandi stafrænum heimi nota vistkerfi fyrirtækja Microsoft Dynamics 365 forritin sem heild. Vegna þess að gögn frá fólki, viðskiptavinum, aðgerðum og Internet of Things (IoT) tækjum streyma inn í eina uppsprettu er tækifæri fyrir stafrænar endurgjafarlykkjur. Til að ná þessari reynslu er samþætting á milli forrita Finance and Operations og annarra forrita Dynamics 365 nauðsynleg. Sum forrit eru byggð ofan á Common Data Service. Sameining gagna á milli forrita Finance and Operations við Common Data Service gerir öðrum forritum kleift að eiga samræmd og lipur samskipti við Finance and Operations.

Forrit Finance and Operations og Common Data Service bjóða upp á samstillingu gagna í rauntíma milli forrita Finance and Operations og annarra forrita Dynamics 365 með tvískiptum ramma. Umfjöllunin er breið og spannar 28 yfirborðssvið í forritinu. Markmiðið er að bjóða upp á „One Dynamics 365“ notendaupplifun með óaðfinnanlegu gagnastreymi sem tengir viðskiptaferla milli forrita.

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

Fylgdu þessum skrefum til að setja upp samþættingu á milli forritum Finance and Operations og Common Data Service.
    
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
