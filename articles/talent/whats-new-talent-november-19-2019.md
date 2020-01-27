---
title: Nýjungar eða breytingar í Dynamics 365 Talent (19. nóvember 2019)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 88ed678cdd37b4bd3d1a7ae92b505b2cfdea4fc8
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896728"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (19. nóvember 2019)

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2621. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Verkvangsuppfærsla 31 fyrir forrit Finance and Operations

Sjá frekari upplýsingar [Forskoða eiginleika í uppfærslu pallsins 31 fyrir forrit Finance and Operations (janúar 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31).

### <a name="feature-management-workspace-383856"></a>Vinnusvæði eiginleikastjórnunar (383856)

Vinnusvæðið **Stjórnun eiginleika** býður upp á lista yfir eiginleika sem eru afhentir í hverri útgáfu. Sjálfgefið er að slökkt sé á nýjum eiginleikum. Hægt er að nota vinnusvæðið til að kveikja á þeim og skoða fylgiskjölin fyrir þá. Nánari upplýsingar um stjórnun eiginleika er að finna í [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Allar nýju aðgerðirnar eru áfram í forskoðun í að minnsta kosti 30 daga og venjulega 30-60 daga. Helstu eiginleikar eru venjulega fáanlegir í október og apríl ár hvert í kjölfar forskoðunartímabilsins. Um leið og þú sérð nýja möguleika í vinnusvæðinu **Stjórnun eiginleika** er hægt að kveikja á þeim. Sumar aðgerðir kunna að vera sjálfkrafa á.
 
Stundum er sambyggður eiginleiki virkur og ekki er hægt að slökkva á honum (til dæmis vinnusvæðinu **Stjórnun eiginleika**).
 
Þegar eiginleiki er almennt tiltækur kann að vera kveikt eða slökkt á honum í framleiðsluumhverfi. Vinnusvæðið **Stjórnun eiginleika** gefur til kynna hvenær forsýningareiginleiki verður nauðsynlegur. Þessi dagsetning er venjulega 1. október eða 1. apríl til að samræma hálfsársáætlun um losun. Ekki er hægt að slökkva á skyldueiginleikum. Þar til það verður skylda geturðu kveikt og slökkt á eiginleikum í öllu umhverfi.

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>Skilaboð birtast þegar afturkölluð aðgerð er til fyrir stöðu (382887)

Eftirfarandi skilaboð birtast ekki lengur þegar þú velur ákveðna stöðu og aflýst aðgerð er allt sem er tiltækt fyrir stöðuna: **Ófullkomin aðgerð er í vinnslu vegna stöðu xxxxxx**.

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>Við nám í greiningu sýna námskeiðsgerð og staða röng gögn (381151)

Útgáfa vikunnar uppfærð fræðigreining til að sýna rétt **Námskeiðsgerð** og **Staða**.

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>Starfsmannanúmer ætti að birtast á borða nýs starfsmanns (383832)

Í glugganum **Nýr starfskraftur** birtist **Númer starfsmanns** nú á borða fyrir fljótlega tilvísun.

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>Upphafsdagsetning staðsetningar ákvarðar starfsskrána sem á að nota þegar sótt er bótastig við ráðningu (350361)

Í þessari útgáfu segir m.a. **Upphafsdagsetning bóta** ákvarðar stig sem úthlutað er í nýju vinnsluna.

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>Sérsniðnir tiltektarlistareitir í töflunni Staða eru ekki samstilltir við Common Data Service (387503)

Með þessari útgáfu eru vörur á tiltektarlista núna samstilltir við Common Data Service.

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>Heimilisfang starfsmanns er ekki samstillt við Common Data Service við innflutning nýrra gagna (349673)

Í þessari útgáfu vikunnar samstillast heimilisfangsgögn nú við Common Data Service við innflutning á nýjum gögnum.

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="print-performance-reviews"></a>Prenta árangursumsagnir

Sjá [Prenta árangursumsagnir](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) í Dynamics 365: 2019 útgáfu bylgjuáætlun 2.
