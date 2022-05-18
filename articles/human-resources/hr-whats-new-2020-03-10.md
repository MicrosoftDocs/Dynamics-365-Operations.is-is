---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (10. mars 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 10. mars 2020.
author: andreabichsel
ms.date: 03/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 831f66ef944dbe61c4dbb7833d6ec24d34aa80a3
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688434"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (10. mars 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.2985. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Get ekki fengið aðgang að greiningarskýrslu færnihátta (394460)

Þessi skýrsla er ekki studd í Dynamics 365 Human Resources. Valmyndaratriðið til að prenta SSRS skýrsluna er fjarlægt.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Röng skilaboð um upphafssíðuna (417950)

Með þessari breytingu leynir öryggi þessum valmyndaratriðum ef þú hefur ekki aðgang að glugganum.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Straumlínulagað viðhaldsverkefni fyrir starfsmenn (380538)

Viðhaldsgluggi starfskraftaverka skráir yfir öll verk fyrir starfsmann í nýliðum, starfslokum, umbreytingum og viðskiptaferlum. Þú getur eytt, endurúthlutað eða uppfært stöðu verka.

Dæmi: Benjamin Martin er fríðindastjórnandi. Við nýliðun starfsmanna eru verkefni búin til fyrir Benjamin til að endurskoða fríðindaval nýrra starfsmanns. Benjamin er með fyrri verkefni sem hann hefur lokið og framtíðarverkefni sem hann þarf að klára. Benjamin ákveður að hætta hjá fyrirtækinu og því þarf annaðhvort að úthluta verkefnum hans eða fjarlægja þau. Viðhaldsgluggi verks (í aðgerðarrúðunni í glugganum **Starfskraftur**) gerir kleift að úthluta öllum verkum Benjamíns til annars starfsmanns eða fjarlægja þau.  

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
| Einingin nýr **Titill** | <ul><li>**Titli** bætt við</li></ul> Nýja einingin **Titill** er innifalin í Dataverse en er ekki tilvísuð úr einigunum **Staða starfs** eða **Starf** á þessum tíma. |

> [!NOTE]
> Fjárhagsvíddir fyrir bæði störf og atvinnu veita einnar áttar samþættingu fyrir uppfærslur úr Human Resources í Dataverse. Uppfærslur fjárhagsvídda samstillast ekki eins og stendur úr Dataverse í Human Resources.

Á næstu vikum verða þessar einingarbreytingar tiltækar í öllu umhverfi. Til að setja upp það nýjasta handvirkt Dataverse lausn fyrir Human Resources:

1.  Farðu í [Power Platform Stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).

2.  Veldu **Umhverfi**.

3.  Finndu umhverfið sem þú vilt uppfæra. Umhverfið ætti að samsvara **Heiti umhverfisins** í **Dataverse upplýsingar** kafla í glugganum **Um** í Human Resources.

4.  Veldu umhverfið til að skoða upplýsingar um umhverfið.

5.  Í aðgerðastikunni efst velurðu **Stýra lausnum**. Nýr vafragluggi opnast og fer í **Stjórnunarmiðstöð Dynamics 365** í samhengi við umhverfi þitt.

6.  Í listanum **Lausn** velurðu **Dynamics 365 Human Resources Akkeri**.

7.  Veldu **Uppfæra** til að beita nýjustu lausninni.

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi forskoðunaraðgerðir eru í boði 3. febrúar 2020:

- **Forskoðunareiginleikar Leyfis og fjarvista** - Frekari upplýsingar um stjórnun leyfa og fjarvista er að finna í [Forskoðunareiginleikar leyfis og fjarvista](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forskoðunareiginleiki fríðindastjórnunar** - Sjá frekari upplýsingar, þ.mt þekkt mál [Yfirlit yfir ávinning stjórnenda](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Væntanlegt

### <a name="platform-update-33"></a>Update 33 fyrir verkvang

- Forrit á heila síðu (Preview) - Þessi forskoðunareiginleiki, sem krefst þess að þú gerðir vistað skjáaðgerð, gerir það kleift Power Apps og forrit frá þriðja aðila til að bæta við sem heilsíðunarupplifun í stjórnborðinu.

- Vistaðar skoðanir (forsýning) - Þessi forskoðunaraðgerð gerir kleift að vista skoðanir, sem er veruleg aukning á undirkerfi sérsniðinnar. Þessi aðgerð gerir notendum kleift að hafa mörg nefnd sérsnið á hverja síðu. Þú getur einnig birt skoðanir í öryggishlutverkum.

- Fínstilling “er eitt af„ síunarupplifun - Þessi aðgerð gerir kleift að hagræða “er ein af„ síunarupplifun sem gerir það auðveldara að slá inn mörg síugildi, hefur einfaldara fyrirkomulag til að fjarlægja einstök eða öll síu gildi og hafa meira samningur og leiðandi sjón á gildi síunnar.

- Mælt með reitum - Notendur þurfa oft að bæta reitum við töflu eða síðu. Þetta getur verið erfitt með svo marga reiti sem eru tiltækir. Í stað þess að þurfa að leita í stórum lista gerir þessi aðgerð kerfinu kleift að yfirborð setja af ráðlögðum reitum út frá því sem aðrir notendur bæta oftast við í svipuðum aðstæðum.

- Sticky sjálfgefnar aðgerðir í ristum - Þessi aðgerð tryggir að sjálfgefna aðgerðin í ristinni er tengd ákveðnum dálki í ristinni, óháð því hvort sá dálkur er færður eða falinn.

## <a name="see-also"></a>Sjá einnig

[Nýjungar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]