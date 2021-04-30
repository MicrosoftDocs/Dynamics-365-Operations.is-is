---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (25. febrúar 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 25. febrúar 2020.
author: andreabichsel
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e0ff8fa382ea186426b6f6ceff6044dc35496373
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893377"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (25. febrúar 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.2927. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Kveiktu á stjórnun mála vegna málastjórnunar og gagnaumsýslu (DMF) (414754)

Þessi forskoðunaraðgerð gerir kleift að fletta í málum í málastjórnun. Þú getur gert þennan forskoðunareiginleika virkan í vinnusvæðinu **Stjórnun eiginleika**. Þessi valmyndaratriði birtast í vinnusvæðinu **Fylgni** í Dynamics 365 Human Resources. Með þessari breytingu geta Human Resources nálgast:

- Öll mál
- Málin mín
- Opnu málin mín
- Mál mín í vanskilum
- Mál sem notanda hefur verið úthlutað í verkflæðinu

Ásamt þessum nýju sjónarmiðum í málum, **Málatilvik** DMF eining er einnig fáanleg.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Virkja skilgreiningar á venslum í altækri aðsetursbók (414762)

Vensl eru nú virk í altækri aðsetursbók. Fyrir útgáfu vikunnar sýndi upplýsingakassinn **Vensl** sýndi öll kerfisskilgreind vensl. Nú er hægt að skilgreina þessi tengsl á síðunni altæk aðsetursbók.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>Hægt er að fjarlægja stöðu þegar virkar bótaskrár eru til fyrir stöðuna (414568)

Með þessari breytingu birtist viðvörun þegar þú reynir að eyða stöðu og starfsmaður hefur virkan bótaskrá fyrir sömu stöðu. Þegar þetta gerist verður þú að uppfæra starfsmannaskrána með föstum bótum áður en þú fjarlægir starfið.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>Verkferill vegna árangursskoðunar bætir stundum við afskráningum frá fólki sem er ekki hluti af ferlinu (414171)

Þessi breyting leiðréttir vandamál þar sem fleiri þátttakendur vegna afskráningar bætast við frammistöðumatið.

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>Verkalýðsverkefni ekki búið til í Dataverse þegar valið er í New Worker valmyndinni (413479)

Þessi breyting leiðréttir mál þegar ráðinn er nýr starfsmaður og framselja nýja ráðninguna í stöðu í gegnum **Nýr starfsmaður** samtal. Nú endurspeglast stöðuúthlutunin Dataverse.

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

Á næstu vikum verða þessar einingarbreytingar tiltækar í öllu umhverfi. Til að setja upp það nýjasta handvirkt Dataverse lausn fyrir Human Resources:

1.  Farðu í [Power Platform Stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).

2.  Veldu **Umhverfi**.

3.  Finndu umhverfið sem þú vilt uppfæra. Það ætti að samsvara **Heiti umhverfisins** í **Common Data Service upplýsingar** kafla í glugganum **Um** í Human Resources.

4.  Veldu umhverfið til að skoða upplýsingar um umhverfið.

5.  Í aðgerðastikunni efst velurðu **Stýra lausnum**. Nýr vafragluggi opnast og fer í **Stjórnunarmiðstöð Dynamics 365** í samhengi við umhverfi þitt.

6.  Í listanum **Lausn** velurðu **Dynamics 365 Human Resources Akkeri**.

7.  Veldu **Uppfæra** til að beita nýjustu lausninni.

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi forskoðunaraðgerðir urðu fáanlegar 3. febrúar 2020:

- **Forskoðunareiginleikar Leyfis og fjarvista** - Frekari upplýsingar um stjórnun leyfa og fjarvista er að finna í [Forskoðunareiginleikar leyfis og fjarvista](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forskoðunareiginleiki fríðindastjórnunar** - Sjá frekari upplýsingar, þ.mt þekkt mál [Yfirlit yfir ávinning stjórnenda](hr-benefits-management-overview.md).

## <a name="see-also"></a>Sjá einnig

[Nýjungar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]