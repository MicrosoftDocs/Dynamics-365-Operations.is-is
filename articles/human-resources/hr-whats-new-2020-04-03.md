---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (3. apríl 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 3. apríl 2020.
author: Darinkramer
manager: AnnBe
ms.date: 04/03/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8f5d7ab996e0d27f763cd4c3c51e9a2c923d909b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526787"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (3. apríl 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3111. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Lifecycle Services (LCS) vegna tilvísunar.

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>Aðgerðir sem eru almennt í boði vikuna 6. apríl

- **Eiginleikar leyfis og fjarvista** - Nánari upplýsingar er að finna í [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md).

- **Eiginleikar fríðindastjórnunar** - Nánari upplýsingar er að finna í [Yfirlit yfir fríðindastjórnun](hr-benefits-management-overview.md).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Umhverfismörk Human Resources eru nú byggð á uppfærðu leyfi (394595)

Takmörkun á fjölda umhverfis á hvert verk í LCS hefur breyst. Fyrri mörkin voru tvö umhverfi. Takmörkunin á fjölda framleiðslu- og sandkassaumhverfis sem þú getur búið til fyrir Human Resources í LCS er nú byggð á uppfærðu leyfi. Þú getur nú búið til eins mörg umhverfi og þörf er á fyrir hvert LCS verk, háð fjölda leyfa sem keypt er. Nýja leyfið, uppfært 1. febrúar 2020, gerir viðskiptavinum kleift að kaupa viðbótarumhverfi. Nánari upplýsingar um leyfiskröfur fyrir viðbótarumhverfi, sjá [Leyfishandbók fyrir Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Villa við að reyna að eyða spurningalista (428603)

Uppfærsla þessarar viku leiðréttir vandamál þar sem eftirfarandi villa birtist þegar reynt er að eyða spurningalista:

Óstemmandi X++ TTSBEGIN/TTSCOMMIT par hefur fundist.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Öryggisatriði vegna frammistöðubókar og fagvottorða (428499)

Þessi breyting takmarkar sýnileika bæði frammistöðubóka og fagvottorða miðað við fyrirtækin sem þau hafa aðgang að. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>Skammstöfunin fyrir Quebec og Manitoba (387510)

Upphafsgögn hafa verið uppfærð til að endurspegla rétta skammstöfun fyrir Manitoba og Quebec.

## <a name="new-entities-available-in-data-management-framework"></a>Nýjar einingar í boði í gagnastjórnunarramma

Eftirfarandi einingar eru nú tiltækar. Ef þú sérð þessar einingar ekki skráðar á einingalistanum notarðu valkostinn **Uppfæra einingar** í **Rammafæribreytur > Einingastillingar > Uppfæra skrá yfir einingar**.

 - Bankafærsla yfir leyfi og fjarvistir V2
 - Skráning leyfis og fjarvista V2
 - Áætlunarskil leyfis og fjarvista V2
 - Áætlun leyfis og fjarvista V2

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service lausn er nú fáanleg með eftirfarandi breytingum:

| lýsing | Skiptimynt |
| --- | --- |
| **Vinna/staða** einingabreytingar | <ul><li>**Launasvæði** bætt við</li>|
| Einingunni **Vídd stöðu starfs** bætt við | <ul><li>**Fjárhagsvíddum** bætt við</li>
| **Verkamaður** eining breytist | <ul><li>**Nafnaröð** bætt við</li><li>**Vinnur að heiman** bætt við</li><li>**Tungumáli** bætt við</li><li>**Starfsaldursdagsetningu** bætt við</li><li>**Dagsetning starfsafmælis** bætt við</li><li>**Upprunalegri ráðningardagsetningu** bætt við</li></ul> |
| **Starf** einingu breytt | <ul><li>**Fjárhagsvíddum** bætt við</li><li>**Ástæða starfsloka** bætt við</li><li>**Uppsagnadagur** endurnefnt frá **Dagsetning breytinga**</li><li>**Dagsetningu reynslutíma** bætt við</li></ul> |
| **Heimilisfang starfskrafts** eining breytist | <ul><li>**Götu** bætt við</li><li>**Heimilisfang 1**, **Heimilisfang lína 2** og **Heimilisfangslína 3** merkt fyrir afskriftir</li></ul> |
| Nýir uppsetningaraðilar breytilegra bóta | <ul><li>**Fyrirkomulagsgerð breytilegra uppbóta**</li><li>**Fyrirkomulag breytilegra uppbóta**</li><li>**Veitireglur**</li><li>**Fyrirkomulagsstig breytilegra uppbóta**</li></ul> |
| Nýtt **Starfsmaður dagatal atvinnu** eining | <ul><li>**Vinnudagatalseining** bætt við</li></ul> |
| Ný eining **Upplýsinga um launastöðu** | <ul><li>**Upplýsingar um launastöðu** bætt við</li></ul> |
| Einingin nýr **Titill** | <ul><li>**Titli** bætt við</li></ul>Nýja einingin **Titill** er innifalin í Common Data Service en er ekki tilvísuð úr einigunum **Staða starfs** eða **Starf** á þessum tíma. |

> [!NOTE]
> Fjárhagsvíddir fyrir bæði störf og atvinnu veita einnar áttar samþættingu fyrir uppfærslur úr Human Resources í Common Data Service. Uppfærslur fjárhagsvídda samstillast ekki eins og stendur úr Common Data Service í Human Resources.

Á næstu vikum verða þessar einingarbreytingar tiltækar í öllu umhverfi. Til að setja upp það nýjasta handvirkt Common Data Service lausn fyrir Human Resources:

1.  Farðu í [Power Platform Stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).

2.  Veldu **Umhverfi**.

3.  Finndu umhverfið sem þú vilt uppfæra. Umhverfið ætti að samsvara **Heiti umhverfisins** í **Common Data Service upplýsingar** kafla í glugganum **Um** í Human Resources.

4.  Veldu umhverfið til að skoða upplýsingar um umhverfið.

5.  Í aðgerðastikunni efst velurðu **Stýra lausnum**. Nýr vafragluggi opnast og fer í **Stjórnunarmiðstöð Dynamics 365** í samhengi við umhverfi þitt.

6.  Í listanum **Lausn** velurðu **Dynamics 365 Human Resources Akkeri**.

7.  Veldu **Uppfæra** til að beita nýjustu lausninni.

## <a name="in-preview"></a>Í kynningarútgáfu

## <a name="leave-suspension"></a>Frestun leyfis

Þú getur frestað leyfi og fjarvistum í Human Resources fyrir starfsmann. Frestun leyfis stöðvar leyfisuppsöfnun fyrir valdar leyfisgerðir. Ef frestunin á sér stað eftir að uppsöfnun hefur verið unnin mun frestun leyfis skapa hlutfallslega leiðréttingu á leyfisstöðu starfsmanns. Frekari upplýsingar eru í [Fresta leyfi](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Yfirfærslureglur

Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar. Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga. Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).

## <a name="coming-soon"></a>Væntanlegt

## <a name="new-production-release-cadence"></a>Ný tíðni framleiðsluútgáfu

Frá og með apríl mun losunarferlið fyrir Human Resources breytast úr vikulegri uppfærslu í hálfsmánaðar uppfærslu. Til að tryggja samræmingu við örugga notkun á vettvangi og viðhalda háum stöðlum um stöðugleika og áreiðanleika í þjónustunni verður ferlið við að dreifa þjónustuuppfærslum á öllum svæðum í hálfsmánaðar útgáfu. Viðbótarprófanir og skjáir verða uppsettir til að staðfesta árangursríka dreifingu á hverju stigi ferlisins. Nánari upplýsingar um losunarrýmið, sjá [Uppfæra ferli](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Þekkt vandamál

## <a name="employment-detail-entity"></a>Atvinnuupplýsingaeining

Einingin **Atvinnuupplýsingar** hefur verið uppfærð með eftirfarandi reitum: **Launatíðni**, **Kenni starfsgreinar**, **Starfsheiti**, **Kenni starfsheitis** og **Fríðindastaða starfs**. Uppsetningargögnin fyrir þessa reiti treysta á að fríðindastjórnun sé virkjuð í Eiginleikastjórnun. Þessa reitir ætti ekki að fylla út eða uppfæra í einingunni **Starfsupplýsingar** vegna þess að það mun valda villum við innflutning.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint forsýning virkar ekki í sumum umhverfum

Ef forskoðun skjals fyrir skjöl sem eru vistuð í SharePoint virkar ekki, prófaðu eftirfarandi aðferð:

1. Staðfestu að notandareikningur stjórnanda sé með tölvupóst sem tengist notendaskránni. Þessar upplýsingar er hægt að skoða á síðunni **Notandi**. Ef tölvupóstur er ekki settur upp þarftu að bæta við tölvupóstinum og veitunni með OData Excel viðbótinni. Sjálfgefið er að netfangið er ekki til í Excel-hönnuninni. Þú þarft að breyta Excel hönnuninni, bæta við öllum reitum, beita og endurnýja. Þegar þú hefur lokið þessum skrefum geturðu uppfært stjórnandareikninginn.

2. Þegar stjórnandareikningurinn er með tilheyrandi tölvupóstreikning skaltu skrá þig inn á Human Resources með stjórnandaskilríkjum.

3. Opnaðu viðhengi í SharePoint til að hefja forskoðun skjalsins.

4. Skráðu þig inn með öðrum notendareikningi sem hefur aðgang að viðhengjum og sannreyndu að forsýningin virkar eins og búist var við.

## <a name="see-also"></a>Sjá einnig

[Nýjungar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)