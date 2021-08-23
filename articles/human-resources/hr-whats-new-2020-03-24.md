---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (24. mars 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 24. mars 2020.
author: andreabichsel
ms.date: 03/24/2020
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
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64abc088ec1ec9bdf4d6f5ba175e420e495e770535c321b4dd9d266e1864d58e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751195"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (24. mars 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3073. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Lifecycle Services (LCS) vegna tilvísunar.

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Umhverfismörk Human Resources eru nú byggð á uppfærðu leyfi (394595)

Takmörkun á fjölda umhverfis á hvert verk í Lifecycle Services (LCS) hefur breyst. Fyrri mörkin voru tvö umhverfi. Takmörkunin á fjölda framleiðslu- og sandkassaumhverfis sem þú getur búið til fyrir Human Resources í LCS er nú byggð á uppfærðu leyfi. Þú getur nú búið til eins mörg umhverfi og þörf er á fyrir hvert LCS verk, háð fjölda leyfa sem keypt er. Nýja leyfið, uppfært 1. febrúar 2020, gerir viðskiptavinum kleift að kaupa viðbótarumhverfi. Nánari upplýsingar um leyfiskröfur fyrir viðbótarumhverfi, sjá [Leyfishandbók fyrir Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="platform-changes"></a>Verkvangsbreytingar

- Forrit á heila síðu (Preview) - Þessi forskoðunareiginleiki, sem krefst þess að þú gerðir vistað skjáaðgerð, gerir það kleift Power Apps og forrit frá þriðja aðila til að bæta við sem heilsíðunarupplifun í stjórnborðinu.

- Vistaðar skoðanir (forsýning) - Þessi forskoðunaraðgerð gerir kleift að vista skoðanir, sem er veruleg aukning á undirkerfi sérsniðs. Þessi aðgerð gerir notendum kleift að hafa mörg nefnd sérsnið á hverja síðu. Þú getur einnig birt skoðanir í öryggishlutverkum.

- Fínstilling “er eitt af„ síunarupplifun - Þessi aðgerð gerir kleift að hagræða “er ein af„ síunarupplifun sem gerir það auðveldara að slá inn mörg síugildi, hefur einfaldara fyrirkomulag til að fjarlægja einstök eða öll síu gildi og hafa meira samningur og leiðandi sjón á gildi síunnar.

- Mælt með reitum - Notendur þurfa oft að bæta reitum við töflu eða síðu. Þetta getur verið erfitt með svo marga reiti sem eru tiltækir. Í stað þess að þurfa að leita í stórum lista gerir þessi aðgerð kerfinu kleift að yfirborð setja af ráðlögðum reitum út frá því sem aðrir notendur bæta oftast við í svipuðum aðstæðum.

- Sticky sjálfgefnar aðgerðir í ristum - Þessi aðgerð tryggir að sjálfgefna aðgerðin í ristinni er tengd ákveðnum dálki í ristinni, óháð því hvort sá dálkur er færður eða falinn.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a>Ekki tókst að leiðrétta orlofsstöðu fyrir áætlun með enga uppsöfnun sem var stofnuð með kveikt á eiginleikanum „margar leyfisgerðir” (419635)

Með þessari breytingu geturðu leiðrétt stöður fyrir leyfisáætlanir sem voru stofnaðar með (forskoðunar)eiginleikann Margar leyfisgerðir virkjaðan í eiginleikastjórnun.

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi forskoðunaraðgerðir urðu fáanlegar 3. febrúar 2020:

- **Forskoðunareiginleikar Leyfis og fjarvista** - Frekari upplýsingar um stjórnun leyfa og fjarvista er að finna í [Forskoðunareiginleikar leyfis og fjarvista](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forskoðunareiginleiki fríðindastjórnunar** - Sjá frekari upplýsingar, þ.mt þekkt mál [Yfirlit yfir ávinning stjórnenda](hr-benefits-management-overview.md).

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse lausn er nú fáanleg með eftirfarandi breytingum:

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
| Einingin nýr **Titill** | <ul><li>**Titli** bætt við</li></ul>Nýja einingin **Titill** er innifalin í Dataverse en er ekki tilvísuð úr einigunum **Staða starfs** eða **Starf** á þessum tíma. |

> [!NOTE]
> Fjárhagsvíddir fyrir bæði störf og atvinnu veita einnar áttar samþættingu fyrir uppfærslur úr Human Resources í Dataverse. Uppfærslur fjárhagsvídda samstillast ekki eins og stendur úr Dataverse í Human Resources.

Á næstu vikum verða þessar einingarbreytingar tiltækar í öllu umhverfi. Til að setja upp það nýjasta handvirkt Dataverse lausn fyrir Human Resources:

1.  Farðu í [Power Platform Stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).

2.  Veldu **Umhverfi**.

3.  Finndu umhverfið sem þú vilt uppfæra. Umhverfið ætti að samsvara **Heiti umhverfisins** í **Common Data Service upplýsingar** kafla í glugganum **Um** í Human Resources.

4.  Veldu umhverfið til að skoða upplýsingar um umhverfið.

5.  Í aðgerðastikunni efst velurðu **Stýra lausnum**. Nýr vafragluggi opnast og fer í **Stjórnunarmiðstöð Dynamics 365** í samhengi við umhverfi þitt.

6.  Í listanum **Lausn** velurðu **Dynamics 365 Human Resources Akkeri**.

7.  Veldu **Uppfæra** til að beita nýjustu lausninni.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint forsýning virkar ekki í sumum umhverfum

Ef forskoðun skjals fyrir skjöl sem eru vistuð í SharePoint virkar ekki, prófaðu eftirfarandi aðferð:

1. Staðfestu að notandareikningur stjórnanda sé með tölvupóst sem tengist notendaskránni. Þessar upplýsingar er hægt að skoða á síðunni **Notandi**. Ef tölvupóstur er ekki settur upp þarftu að bæta við tölvupóstinum og veitunni með OData Excel viðbótinni. Sjálfgefið er að netfangið er ekki til í Excel-hönnuninni. Þú þarft að breyta Excel hönnuninni, bæta við öllum reitum, beita og endurnýja. Þegar þú hefur lokið þessum skrefum geturðu uppfært stjórnandareikninginn.

2. Þegar stjórnandareikningurinn er með tilheyrandi tölvupóstreikning skaltu skrá þig inn á Human Resources með stjórnandaskilríkjum.

3. Opnaðu viðhengi í SharePoint til að hefja forskoðun skjalsins.

4. Skráðu þig inn með öðrum notendareikningi sem hefur aðgang að viðhengjum og sannreyndu að forsýningin virkar eins og búist var við.

## <a name="coming-soon"></a>Væntanlegt

## <a name="new-production-release-cadence"></a>Ný tíðni framleiðsluútgáfu

Frá og með apríl mun losunarferlið fyrir Human Resources breytast úr vikulegri uppfærslu í hálfsmánaðar uppfærslu. Til að tryggja samræmingu við örugga notkun á vettvangi og viðhalda háum stöðlum um stöðugleika og áreiðanleika í þjónustunni verður ferlið við að dreifa þjónustuuppfærslum á öllum svæðum í hálfsmánaðar útgáfu. Viðbótarprófanir og skjáir verða uppsettir til að staðfesta árangursríka dreifingu á hverju stigi ferlisins. Nánari upplýsingar um losunarrýmið, sjá [Uppfæra ferli](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Þekkt vandamál

## <a name="employment-detail-entity"></a>Atvinnuupplýsingaeining

Einingin **Atvinnuupplýsingar** hefur verið uppfærð með eftirfarandi reitum: **Launatíðni**, **Kenni starfsgreinar**, **Starfsheiti**, **Kenni starfsheitis** og **Fríðindastaða starfs**. Uppsetningargögnin fyrir þessa reiti treysta á að fríðindastjórnun sé virkjuð í Eiginleikastjórnun. Þessa reitir ætti ekki að fylla út eða uppfæra í einingunni **Starfsupplýsingar** vegna þess að það mun valda villum við innflutning.

## <a name="see-also"></a>Sjá einnig

[Nýjungar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]