---
title: Nýjungar eða breytingar í Dynamics 365 Talent (21. janúar 2020)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528123"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Nýjungar eða breytingar í Dynamics 365 Talent (21. janúar 2020)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract. Við höfum bætt virkni við Attract til að styðja nýlega tilkynningu okkar, [Að byggja upp farsælla vinnuafl með Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).

### <a name="download-environment-data"></a>Sækja umhverfisgögn

Stjórnendur geta sótt umhverfisgögn. Gögnin eru flutt út á venjulegu JSON sniði með öll störf, frambjóðendur og stillingar fluttar út í zip skrá. Frekari upplýsingar eru í [Flytja gögn út úr Attract og Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Takmarka aðgang að umhverfi fyrir notendur sem ekki eru stjórnendur

Stjórnendur geta nú takmarkað aðgang að umhverfinu fyrir notendur sem ekki eru stjórnendur. Ekki er hægt að afturkalla þessa aðgerð. Frekari upplýsingar eru í [Takmörkun aðgangs að Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

### <a name="exporting-onboarding-guides"></a>Útflutningur móttökukynningum

Notendur geta nú flutt út allar leiðbeiningar um borð og sniðmát um borð á Word skjalasniði. Frekari upplýsingar eru í [Flytja gögn út úr Attract og Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2726. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Nýjasta árlega bótasviðið í Staðfesta atvinnuform er ekki í samræmi (392092)

Þessi útgáfa felur í sér breytingu sem stöðugt mun sýna nýjasta gjaldmiðilinn byggðan á fyrirtækjavalinu á eyðublaðinu **Staðfesta starf**.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Þekktur sem reitur bætt við leit að endurgjöf viðtakenda (407789)

Þegar leitað var eftir árangri veitti leitin að starfsmönnum ekki nægar upplýsingar til að ákvarða hvort endurgjöfin færi til rétts aðila. Við bættum við dálknum **Þekktur sem** til að hjálpa til við að bera kennsl á einkvæmt nafn starfsmanns.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>HcmWorkerPayrollInfo færsla er búin til án tengsla við starfsmann (394526)

Þessi útgáfa felur í sér breytingu á að skrifa ekki HCMWorkerPayrollInfo færslur án tilvísunar til starfsmanns.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Fær um að breyta deild þegar flett er úr stöðuveldi (341001)

Þegar öryggi hefur verið sett upp til að hafna aðgangi að breytingardeildum er breyting afvirkjuð þegar farið er í eyðublaðið **Deildir** í öllum atburðarásum.

## <a name="coming-soon"></a>Væntanlegt

Nýtt Common Data Service lausn mun liggja fyrir fljótlega með eftirfarandi breytingum:

| Lýsing | Skiptimynt |
| --- | --- |
| **Vinna/staða** einingabreytingar | <ul><li>**Launasvæði** bætt við</li><li>**Fjárhagsvíddum** bætt við</li></ul> |
| **Verkamaður** eining breytist | <ul><li>**Nafnaröð** bætt við</li><li>**Vinnur að heiman** bætt við</li><li>**Tungumáli** bætt við</li><li>**Starfsaldursdagsetningu** bætt við</li><li>**Dagsetning starfsafmælis** bætt við</li><li>**Upprunalegri ráðningardagsetningu** bætt við</li></ul> |
| **Starf** einingu breytt | <ul><li>**Fjárhagsvíddum** bætt við</li><li>**Ástæða starfsloka** bætt við</li><li>**Uppsagnadagur** endurnefnt frá **Dagsetning breytinga**</li><li>**Dagsetningu reynslutíma** bætt við</li></ul> |
| **Heimilisfang starfskrafts** eining breytist | <ul><li>**Götu** bætt við</li><li>**Heimilisfang 1**, **Heimilisfang lína 2** og **Heimilisfangslína 3** merkt fyrir afskriftir</li></ul> |
| Nýir uppsetningaraðilar breytilegra bóta | <ul><li>**Fyrirkomulagsgerð breytilegra uppbóta**</li><li>**Fyrirkomulag breytilegra uppbóta**</li><li>**Veitireglur**</li><li>**Fyrirkomulagsstig breytilegra uppbóta**</li></ul> |
| Nýtt **Starfsmaður dagatal atvinnu** eining | <ul><li>**Vinnudagatalseining** bætt við</li></ul> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]