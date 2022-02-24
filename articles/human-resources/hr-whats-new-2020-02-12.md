---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (12. febrúar 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 12. febrúar 2020.
author: Darinkramer
manager: AnnBe
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
ms.author: dkrame
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b89e022441f69825d9c9c56ecdbca2e09e461b9e
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526889"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (12. febrúar 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.2867. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Fyrirliggjandi einingarnar CompFixedEmpls og HcmPersonImage ættu að vera aðgengilegar úr OData (414178)

Með útgáfu þessarar viku eru einingarnar **CompFixedEmpls** og **HcmPersonImage** núna almennar og tiltækar í gegnum ODAta.

## <a name="delete-employment-from-common-data-service-doesnt-work-when-employment-details-arent-active-403193"></a>Eyða atvinnu úr Common Data Service virkar ekki þegar atvinnuupplýsingar eru ekki virkar (403193)

Þessi breyting gerir nú kleift að eyða störfum í gegnum Common Data Service þegar engar virkar atvinnuupplýsingar eru fyrir hendi.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>Verkflæði námskeiðsskráningar breytir stöðu til að ljúka og villur eftir annað samþykki (409749)

Verkflæði námskeiðsskráningar hefur verið uppfært til að leyfa marga samþykktaraðila.

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi forskoðunaraðgerðir eru í boði 3. febrúar 2020:

- **Forskoðunareiginleikar Leyfis og fjarvista** - Frekari upplýsingar um stjórnun leyfa og fjarvista er að finna í [Forskoðunareiginleikar leyfis og fjarvista](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forskoðunareiginleiki fríðindastjórnunar** - Sjá frekari upplýsingar, þ.mt þekkt mál [Yfirlit yfir ávinning stjórnenda](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Væntanlegt

### <a name="platform-update-32"></a>Update 32 fyrir verkvang 

Uppfærsla pallsins 32 verður tiltæk innan tíðar. [Fáðu frekari upplýsingar um uppfærslu pallsins 32 hér](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

### <a name="updated-common-data-service-solution"></a>Uppfærð Common Data Service-lausn

Nýtt Common Data Service lausn mun liggja fyrir fljótlega með eftirfarandi breytingum:

| Lýsing | Skiptimynt |
| ----------------------------------------- | --- |
| **Vinna/staða** einingabreytingar | **Launasvæði** bætt við</br>**Fjárhagsvíddum** bætt við |
| **Verkamaður** eining breytist | **Nafnaröð** bætt við</br>**Vinnur að heiman** bætt við</br>**Tungumáli** bætt við</br>**Starfsaldursdagsetningu** bætt við</br>**Dagsetning starfsafmælis** bætt við</br>**Upprunalegri ráðningardagsetningu** bætt við |
| **Starf** einingu breytt | **Fjárhagsvíddum** bætt við</br>**Ástæða starfsloka** bætt við</br>**Uppsagnadagur** endurnefnt frá **Dagsetning breytinga**</br>**Dagsetningu reynslutíma** bætt við |
| **Heimilisfang starfskrafts** eining breytist | **Götu** bætt við</br>**Heimilisfang 1**, **Heimilisfang lína 2** og **Heimilisfangslína 3** merkt fyrir afskriftir |
| Nýir uppsetningaraðilar breytilegra bóta | **Fyrirkomulagsgerð breytilegra uppbóta**</br>**Fyrirkomulag breytilegra uppbóta**</br>**Veitireglur**</br>**Fyrirkomulagsstig breytilegra uppbóta** |
| Nýtt **Starfsmaður dagatal atvinnu** eining | **Vinnudagatalseining** bætt við |
| Ný eining **Upplýsinga um launastöðu** | **Upplýsingar um launastöðu** bætt við |
| Einingin nýr **Titill** | **Titill** bætt við. Nýja einingin **Titill** verður með í samstillingarferlinu milli Human Resources og Common Data Service. Ekki verður upphaflega vísað í hana úr einingunum **Staða starfs** eða **Starf**. |

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)