---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (12. febrúar 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 12. febrúar 2020.
author: andreabichsel
ms.date: 02/07/2020
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
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6cae0d3f59b1b0d01f3b2f6cf3469520e35d2f91
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051213"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (12. febrúar 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.2867. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Fyrirliggjandi einingarnar CompFixedEmpls og HcmPersonImage ættu að vera aðgengilegar úr OData (414178)

Með útgáfu þessarar viku eru einingarnar **CompFixedEmpls** og **HcmPersonImage** núna almennar og tiltækar í gegnum ODAta.

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a>Eyða atvinnu úr Dataverse virkar ekki þegar atvinnuupplýsingar eru ekki virkar (403193)

Þessi breyting gerir nú kleift að eyða störfum í gegnum Dataverse þegar engar virkar atvinnuupplýsingar eru fyrir hendi.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>Verkflæði námskeiðsskráningar breytir stöðu til að ljúka og villur eftir annað samþykki (409749)

Verkflæði námskeiðsskráningar hefur verið uppfært til að leyfa marga samþykktaraðila.

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi forskoðunaraðgerðir eru í boði 3. febrúar 2020:

- **Forskoðunareiginleikar Leyfis og fjarvista** - Frekari upplýsingar um stjórnun leyfa og fjarvista er að finna í [Forskoðunareiginleikar leyfis og fjarvista](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forskoðunareiginleiki fríðindastjórnunar** - Sjá frekari upplýsingar, þ.mt þekkt mál [Yfirlit yfir ávinning stjórnenda](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Væntanlegt

### <a name="platform-update-32"></a>Update 32 fyrir verkvang 

Uppfærsla pallsins 32 verður tiltæk innan tíðar. [Fáðu frekari upplýsingar um uppfærslu pallsins 32 hér](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

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