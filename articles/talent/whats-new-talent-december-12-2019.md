---
title: Nýjungar eða breytingar í Dynamics 365 Talent (10. desember 2019)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528172"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (10. desember 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2660. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Vinnusvæði eiginleikastjórnunar

Vinnusvæðið **Stjórnun eiginleika** býður upp á lista yfir eiginleika sem eru afhentir í hverri útgáfu. Sjálfgefið er að slökkt sé á nýjum eiginleikum. Hægt er að nota vinnusvæðið til að kveikja á þeim og skoða fylgiskjölin fyrir þá. Nánari upplýsingar um stjórnun eiginleika er að finna í [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Allar nýju aðgerðirnar eru áfram í forskoðun í að minnsta kosti 30 daga og venjulega 30-60 daga. Helstu eiginleikar eru venjulega fáanlegir í október og apríl ár hvert í kjölfar forskoðunartímabilsins. Um leið og þú sérð nýja möguleika í vinnusvæðinu **Stjórnun eiginleika** er hægt að kveikja á þeim. Sumar aðgerðir kunna að vera sjálfkrafa á.
 
Stundum er sambyggður eiginleiki virkur og ekki er hægt að slökkva á honum (til dæmis vinnusvæðinu **Stjórnun eiginleika**).
 
Þegar eiginleiki er almennt tiltækur kann að vera kveikt eða slökkt á honum í framleiðsluumhverfi. Vinnusvæðið **Stjórnun eiginleika** gefur til kynna hvenær forsýningareiginleiki verður nauðsynlegur. Þessi dagsetning er venjulega 1. október eða 1. apríl til að samræma hálfsársáætlun um losun. Ekki er hægt að slökkva á skyldueiginleikum. Þar til það verður skylda geturðu kveikt og slökkt á eiginleikum í öllu umhverfi.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Straumlínulagað starfsmannaform hefur verið fært yfir í vinnusvæðið Stjórnun eiginleika (390583)

Með þessari breytingu er nú hægt að gera straumlínulagað starfsmannaform virkt á vinnusvæðinu **Stjórnun eiginleika**. Þessi eiginleiki hefur verið fluttur úr forminu **Kerfisfæribreytur** í **Kerfisstjórnun**.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Koma í veg fyrir að HcmWorkerPayrollInfo-skrár séu skrifaðar án starfskraftagildis (394526)

Með þessari útgáfu eru **HcmWorkerPayrollInfo**-skrár eru ekki lengur búnar til án tilvísunar starfskrafta í þessari atburðarás. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Skilaboðaskrá sem er tengd aðgerðinni er ekki byggð þegar aðgerðinni tekst ekki að ljúka (374007)

Þessi útgáfa felur í sér breytingu á að útfyllingu aðgerðarskilaboðaskráar þegar aðgerð tekst ekki í vissum atburðarásum. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Samþætting Common Data Service við stofnun runuvinnslu (388030)

Með þessari breytingu eru runuvinnslur fyrir samþættingu Common Data Service stofnaðar þegar þjónustan er virkjuð.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Viðbótartínslulisti gilda í sérsniðnum reitum endurspeglast ekki í Common Data Service þegar smellt hefur verið á Nota í eyðublaðsreitnum Sérsnið (379599)

Með þessari breytingu eru ný tínslulistagildi sem eru færð inn í Talent núna samstillt við Common Data Service þegar þú beitir breytingunum.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Uppfæra í Common Data Service fyrir þá fer orlofsbankafærslueiningu að innskot á Talent hlið (352938)

Þessi breyting leiðréttir mál þar sem uppfærsla á orlofsbankafærslu býr til nýja skrá í Talent.

## <a name="in-preview"></a>Í kynningarútgáfu

Forskoðunareiginleikar eru aðeins í boði í umhverfi **sandkassa**.

### <a name="print-performance-reviews"></a>Prenta árangursumsagnir

Sjá [Prenta árangursumsagnir](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) í Dynamics 365: 2019 útgáfu bylgjuáætlun 2.



[!INCLUDE[footer-include](../includes/footer-banner.md)]