---
title: Nýjungar eða breytingar í Dynamics 365 Talent (5. nóvember 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4068cf81782d2f9559179b91da31e049c006059
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527121"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (5. nóvember 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2598. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="copy-a-core-hr-instance"></a>Afritaðu Core HR tilvik

Í útgáfu vikunnar geturðu notað Microsoft Dynamics Lifecycle Services (LCS) til að afrita Microsoft Dynamics 365 Talent: Core HR gagnagrunn í sandkassaumhverfi. Ef þú ert með annað sandkassaumhverfi geturðu einnig afritað gagnagrunninn úr því umhverfi yfir í markviss sandkassaumhverfi. Frekari upplýsingar má finna á

- [Víðtækari umhverfisstjórnun](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) í Dynamics 365: 2019 útgáfu Wave 2 áætlun

- [Afritaðu Core HR tilvik](hr-copy-instance.md) í Talent fylgiskjölum

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Common Data Service runuvinnslur samþættingar eru ekki búnar til þegar Common Data Service samþætting er virk (388030)

Þessi breyting mun skapa runuvinnslur fyrir Common Data Service samþættingu þegar hún er virk.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity breytir ekki myndastærð einstaklings þegar henni er hlaðið upp (369469)

Útgáfa þessarar viku breytir því hvernig myndastærð er breytt fyrir betri afköst þegar þær eru fluttar inn með gagnastjórnun.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>Staða er tiltæk fyrir úthlutunardag getur verið fyrr en virkjunardagsetningin (340103)

Með þessari breytingu birtist viðvörun ef þú velur **Tiltæk fyrir úthlutunardag** sem er á undan **Virkjunardagsetningu** stöðunnar.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Get ekki búið til beiðni um breytingu á bótum í sjálfsafgreiðslu starfsmanna vegna skrefatengdra áætlana (376872)

Þessi útgáfa leiðréttir mál þegar beðið er um bótabreytingar í gegnum sjálfsafgreiðslu starfsmanna vegna skrefabundinna áætlana. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Ástæðukóði er ekki samstillt við Common Data Service ef lýsingin er lengri en 30 stafir leyfir Core HR 60 (352682)

Með þessari breytingu verða ástæðukóðar með meira en 30 stöfum uppfærðir í Common Data Service. Breytingar gerðar í Common Data Service munu einnig endurspeglast aftur í Talent.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Vinna með samþættingar úr Talent í Finance and Operations (351961)

Þessi útgáfa lagar vandamál þar sem vefföng sem voru uppfærð í Talent voru ekki uppfærð í Finance and Operations. Breytingar á heimilisfangablokkum verða nú uppfærðar.

## <a name="coming-soon"></a>Væntanlegt

### <a name="print-performance-reviews"></a>Prenta árangursumsagnir

Sjá [Prenta árangursumsagnir](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) í Dynamics 365: 2019 útgáfu bylgjuáætlun 2.

### <a name="feature-management-workspace"></a>Vinnusvæði eiginleikastjórnunar

Eiginleikum er bætt við og þeir uppfærðir í hverri útgáfu. Upplifun eiginleikastjórnunar veitir vinnusvæði þar sem hægt er að skoða lista yfir eiginleika sem hafa verið gefnir út í hverri útgáfu. Sjálfgefið er að slökkt sé á nýjum eiginleikum. Hægt er að nota vinnusvæðið til að kveikja á þeim og skoða fylgiskjölin fyrir þá.

Til að læra meira um breytingarnar sem fylgja eiginleikastjórnun, sjá [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
