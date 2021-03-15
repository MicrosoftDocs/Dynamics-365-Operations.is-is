---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (7. febrúar 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 7. febrúar 2020.
author: andreabichsel
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a45eed4e094cedb9d6d8ed0cb2bdc81eb31b76e
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128114"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (7. febrúar 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.2835. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>Að læra greinandi sýnir ekki námskeiðið ef kennslustofan er tóm (388289)

Námsgreiningarsíðan sýnir nú námskeiðið ef kennslustofan er tóm.

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>Stöðuleit tekur ekki tillit til tímabeltisins (405344)

Leit að opnum stöðum tekur nú mið af tímabeltinu þegar verið er að staðfesta hvort staða er opin.

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>Yfirlit yfir núverandi jafnvægisuppfærslu uppfærist ekki með réttu núverandi orlofshlutfalli eftir að hafa sent inn beiðnir um frí (409756)

Núverandi staða nær nú yfir sendar beiðnir um tíma.

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi forskoðunaraðgerðir eru í boði 3. febrúar 2020:

- **Forskoðunareiginleikar Leyfis og fjarvista** - Frekari upplýsingar um stjórnun leyfa og fjarvista er að finna í [Forskoðunareiginleikar leyfis og fjarvista](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forskoðunareiginleiki fríðindastjórnunar** - Frekari upplýsingar, þ.m.t. þekkt vandamál, er að finna í [Yfirlit yfir ávinning stjórnenda](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Væntanlegt

### <a name="platform-update-32"></a>Update 32 fyrir verkvang 

Uppfærsla pallsins 32 verður tiltæk innan tíðar. [Fáðu frekari upplýsingar um uppfærslu pallsins 32 hér](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

### <a name="updated-dataverse-solution"></a>Uppfærð Dataverse-lausn

Nýtt Dataverse lausn mun liggja fyrir fljótlega með eftirfarandi breytingum:

| Lýsing | Skiptimynt |
| ----------------------------------------- | --- |
| **Vinna/staða** einingabreytingar | **Launasvæði** bætt við</br>**Fjárhagsvíddum** bætt við |
| **Verkamaður** eining breytist | **Nafnaröð** bætt við</br>**Vinnur að heiman** bætt við</br>**Tungumáli** bætt við</br>**Starfsaldursdagsetningu** bætt við</br>**Dagsetning starfsafmælis** bætt við</br>**Upprunalegri ráðningardagsetningu** bætt við |
| **Starf** einingu breytt | **Fjárhagsvíddum** bætt við</br>**Ástæða starfsloka** bætt við</br>**Uppsagnadagur** endurnefnt frá **Dagsetning breytinga**</br>**Dagsetningu reynslutíma** bætt við |
| **Heimilisfang starfskrafts** eining breytist | **Götu** bætt við</br>**Heimilisfang 1**, **Heimilisfang lína 2** og **Heimilisfangslína 3** merkt fyrir afskriftir |
| Nýir uppsetningaraðilar breytilegra bóta | **Fyrirkomulagsgerð breytilegra uppbóta**</br>**Fyrirkomulag breytilegra uppbóta**</br>**Veitireglur**</br>**Fyrirkomulagsstig breytilegra uppbóta** |
| Nýtt **Starfsmaður dagatal atvinnu** eining | **Vinnudagatalseining** bætt við |
| Ný eining **Upplýsinga um launastöðu** | **Upplýsingar um launastöðu** bætt við |
| Einingin nýr **Titill** | **Titill** bætt við. Nýja einingin **Titill** verður með í samstillingarferlinu milli Human Resources og Dataverse. Ekki verður upphaflega vísað í hana úr einingunum **Staða starfs** eða **Starf**. |

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]