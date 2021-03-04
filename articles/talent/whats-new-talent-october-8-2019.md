---
title: Nýjungar eða breytingar í Dynamics 365 Talent (8. október 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40898ca7f54089337180def964b8942e8653663b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529481"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (8. október 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingunum sem er lýst í þessum hluta eiga við um smíðarnúmer 8.1.2542. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Fjarlæging bóta opnar skráningu úr almennri forskoðun

Í tengslum við tilkynningu okkar í bloggfærslunni [Strategískar fjárfestingar í kjarnastarfsemi HR keyra gæðarekstur](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/), Microsoft er að fjarlægja ávinninginn fyrir opnun skráningar úr forsýningu almennings 18. október 2019. Í staðinn verður nýr virkni gefinn út í framtíðinni. Framleiðslunotkun kostanna opnar skráningaraðgerð sem nú er í forskoðun almennings verður ekki studd. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Common Data Service samþætting hefur verið sjálfvirkt slökkt vegna nýrra ákvæða (343675)
 
Þegar nýtt umhverfi er útbúið hefur nú verið slökkt á samþættingu Common Data Service. Nánari upplýsingar er að finna í [Skilgreina Common Data Service samþættingu](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Einfaldaður innsláttur og skoðun starfsmanns

Virkni fyrir starfsmannafærslur og leiðsögn er nú fáanleg í öllum umhverfum. Til að kveikja á þessum eiginleika ferðu í **Kerfisstjórnun \> Tenglar \> Uppsetning \> Kerfisfæribreytur \> Forskoða eiginleika** og velur **Bætt skjámynd starfskrafta og yfirlit**. Síðan er kveikt á eiginleikanum fyrir alla notendur. Þú getur slökkt á þessum möguleika hvenær sem er.

Sjá frekari upplýsingar [Einfaldaður gagnainnsláttur starfsmanns](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) í Dynamics 365: 2019 útgáfu bylgjuáætlun 2.

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Attract og Onboard stofna óvirka starfsmenn í Core HR (380517)

Útgáfa þessarar viku leiðréttir mál þar sem Attract og Onboard búa til óvirka starfsmenn í Core HR.

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Vinnuflæðið tekst ekki þegar stjórnandinn er skráður inn í annað fyrirtæki meðan hann segir upp starfsmanni (346852)

Verkflæðið bregst ekki lengur út frá lögaðilanum sem stjórnandinn er skráður inn á.

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>Upplýsingar vantar um HcmOnboardingWorkerChecklistTaskEntity (349591)

Þessi útgáfa inniheldur viðbótarupplýsingar um **HcmOnboardingWorkerChecklistTaskEntity**. Hér eru nokkur dæmi:

- **Heiti hóps** þegar úthlutuð gerð er **hópur**
- **Heiti starfsmanns** þegar úthlutuð gerð er **starfsmaður**
- **Heiti stjórnanda** þegar úthlutuð gerð er **stjórnandi**

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Einingar eru ekki skráðar í stafrófsröð í Common Data Service Aministration (377414)

Einingar eru núna skráðar í stafrófsröð í á síðunni **CDS Administration**.

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Að breyta starfstegundinni með framtíðardegi leyfir ekki stöðuverkefni (339958)

Þessi breyting gerir ráð fyrir stöðuverkefnum þegar gerðum starfsmanna er breytt (til dæmis frá starfsmanni til verktaka).

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Uppfærsla á Common Data Service Eining orlofsbankafærslu stofnar nýja skrá í Talent (352938)

Orlofsfærslan er nú uppfærð þegar uppfærsla er gerð á Common Data Service vegna orlofsbankafærslna.

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Titill viðhengja fyrir athugasemdir sem sýnir endurgjöf sýnir athugasemdir viðbrögð (343765)

Athugasemdalýsingin birtist ekki lengur í viðhengistitlinum.

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Vinnuflæði fyrir bætur Athugasemdareit sýnir rangt efni (339297)

Þessi breyting sýnir innihald reitsins **% HcmActionState.HcmWorkerActionComment.Comments%**.

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity og WorkCalendarDayEntity koma ekki í gegnum OData (376329)

Í þessari útgáfu segir m.a. **VinnaCalendarEntity** og **VinnaCalendarDayEntity** eru nú fáanlegar í gegnum Open Data Protocol (OData).

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>HCMWorkerEntity er hægt þegar OData er notað (375221)

Breytingar bæta árangur **HCMWorkerEntity** þegar Microsoft Excel vinnubókaruppsetning er notuð.

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Færsla dagbókar um frammistöðu stjórnanda sýnir villu eftir að eyðingu dagbókar var gerð og ný (336061)

Þessi útgáfa leiðréttir mál sem kemur upp eftir að einni frammistöðubók er eytt og ný stofnuð strax eftir það. Þessi leiðrétting breytir hegðun í sjálfsafgreiðslu stjórnenda.

## <a name="coming-soon"></a>Væntanlegt

### <a name="print-performance-reviews"></a>Prenta árangursumsagnir

Sjá [Prenta árangursumsagnir](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) í Dynamics 365: 2019 útgáfu bylgjuáætlun 2.


[!INCLUDE[footer-include](../includes/footer-banner.md)]