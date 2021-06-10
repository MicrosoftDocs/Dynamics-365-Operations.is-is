---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (18. febrúar 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 18. febrúar 2020.
author: andreabichsel
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 62b5890f02b6b9598ba5a87e25745fa7633df769
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051234"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (18. febrúar 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.2903. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="platform-update-32"></a>Update 32 fyrir verkvang 

Verkvangsuppfærsla 32 er nú fáanleg. Sjá frekari upplýsingar [Hvað er nýtt eða breytt í uppfærslu verkvangs 32 fyrir Finance and Operations (febrúar 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Leitargildi eru minnst þegar skipt er um skjámöguleika í straumlínulagaðri starfsmannaformi (383833)

Nýi glugginn **Starfskraftur** man nú eftir leitargildum þegar þú breytir skjávalkostunum og beitir breytingum.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Samantektarreitir á launastjórnun í forsýningareiginleikum endurbeina á röng eyðublöð (401861)

Fastir og breytilegir reitir fyrir launastjórnun sýna nú réttar skrár í nýja eyðublaðinu **Starfskraftur**. Gildir aðeins um straumlínulagaða forskoðunareiginleika starfsmanna. Þú getur gert þennan forskoðunareiginleika virkan í **Stjórnun eiginleika**. Frekari upplýsingar eru í [Stjórna eiginleikum](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a>Tómur stöðureitur fyrir sumar skráningar vegna leyfisbeiðna í Dataverse (414915)

Þessi breyting leiðréttir mál í Dataverse þegar reiturinn **Staða** í leyfisbeiðni er stilltur á **Endurskoðun**. Dataverse endurspeglar nú stöðuna.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Hæfnigreining aðeins möguleg fyrir úthlutað starf (411390)

Þú getur nú gert hæfnigreiningar í hverju starfi sem skilgreint er í Human Resources.

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a>Kerfisgjaldmiðill er ekki samstillt úr Dataverse í Human Resources í nýju umhverfi (418011)

Kerfisgjaldmiðill í Dataverse getur núna samstillt sig við Human Resources.

## <a name="in-preview"></a>Í kynningarútgáfu

- [Forskoðunareiginleikar leyfis og fjarveru](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Forskoðunareiginleikar fríðindastjórnunar](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Væntanlegt

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
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]