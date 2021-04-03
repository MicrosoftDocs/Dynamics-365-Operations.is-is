---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (3. mars 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 3. mars 2020.
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 695ae11278a270a44c1ade51964aa396d2fafc60
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463743"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (3. mars 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.2955. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse lausn er nú fáanleg með eftirfarandi breytingum:

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

Á næstu vikum verða þessar einingarbreytingar tiltækar í öllu umhverfi. Til að setja upp það nýjasta handvirkt Dataverse lausn fyrir Human Resources:

1.  Farðu í [Power Platform Stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).

2.  Veldu **Umhverfi**.

3.  Finndu umhverfið sem þú vilt uppfæra. Umhverfið ætti að samsvara **Heiti umhverfisins** í **Common Data Service upplýsingar** kafla í glugganum **Um** í Human Resources.

4.  Veldu umhverfið til að skoða upplýsingar um umhverfið.

5.  Í aðgerðastikunni efst velurðu **Stýra lausnum**. Nýr vafragluggi opnast og fer í **Stjórnunarmiðstöð Dynamics 365** í samhengi við umhverfi þitt.

6.  Í listanum **Lausn** velurðu **Dynamics 365 Human Resources Akkeri**.

7.  Veldu **Uppfæra** til að beita nýjustu lausninni.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Flytja inn vandamál með leyfisskráningargagnaeininguna (406082)

Þú getur nú skráð starfsmann í nýja leyfisáætlun af sömu gerð, svo framarlega sem nýi skráningardagurinn er seinna en útrunninn skráningardagur fyrri áætlunar.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Útgáfa með útflutningsframlagshlutfall í 401k payrollWorkerEnrolledBenefitDetail einingu í DMF (420700)

Þessi breyting leiðréttir útflutningsvirkni fyrir **payrollWorkerEnrolledBenefitDetail** eining til að endurspegla núverandi gildi fyrir framlag vinnuveitenda.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Leit í straumlínulagaðri starfsmannaformi veldur skilaboðum þar sem sagt er að fylla þarf út reitinn (402525)

Þegar þú leitar að starfsmanni færðu ekki lengur skilaboð um að þú verður að fylla út reitinn **Einstaklingur**.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Gildi athugasemdarsviðs er ekki birt á Bæta við fleiri færniformum (380134)

Þessi breyting leiðréttir mál þegar þú sérsníður gluggann **Bæta við meiri færni** í sjálfsafgreiðslu starfsmanna.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Margfeldi fastra launaáætlana rennur ekki út við flutning starfsmanna (389466)

Með þessari breytingu falla úr gildi allar virkar fastar launaskrár vegna gömlu stöðunnar á aðlögunardegi.

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi forskoðunaraðgerðir urðu fáanlegar 3. febrúar 2020:

- **Forskoðunareiginleikar Leyfis og fjarvista** - Frekari upplýsingar um stjórnun leyfa og fjarvista er að finna í [Forskoðunareiginleikar leyfis og fjarvista](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forskoðunareiginleiki fríðindastjórnunar** - Sjá frekari upplýsingar, þ.mt þekkt mál [Yfirlit yfir ávinning stjórnenda](hr-benefits-management-overview.md).

## <a name="see-also"></a>Sjá einnig

[Nýjungar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]