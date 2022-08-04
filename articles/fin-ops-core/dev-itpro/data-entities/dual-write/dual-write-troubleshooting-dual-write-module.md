---
title: Lestu vandamál með tvískrift í fjármála- og rekstrarforritum
description: Þessi grein veitir upplýsingar um bilanaleit sem geta hjálpað þér að laga vandamál með Dual-write eininguna í fjármála- og rekstrarforritum.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2743b99538b332af7cc6ad8d951eede562c14235
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111171"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Lestu vandamál með tvískrift í fjármála- og rekstrarforritum

[!include [banner](../../includes/banner.md)]



Þessi grein veitir upplýsingar um bilanaleit fyrir samþættingu tvískrifa milli fjármála- og rekstrarforrita og Dataverse. Nánar tiltekið veitir það upplýsingar sem geta hjálpað þér að laga vandamál með **Tvöfalt skrifa** mát í fjármála- og rekstraröppum.

> [!IMPORTANT]
> Sum vandamálin sem þessi grein fjallar um gætu þurft annað hvort kerfisstjórahlutverkið eða Microsoft Azure Active Directory (Azure AD) leigjanda stjórnanda skilríki. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Þú getur ekki hlaðið tvískriftareiningunni í fjármála- og rekstrarforrit

Ef þú getur ekki opnað síðuna **Tvöfalt skrif** með því að velja reitinn **Tvöfalt skrif** á vinnusvæðinu **Gagnastjórnun** liggur gagnasamstillingarónustan líklega niðri. Búðu til stuðningseðil til að biðja um endurræsingu gagnasamstillingarþjónustunnar.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Villa þegar reynt er að búa til nýtt töflukort

**Nauðsynlegar innskráningarupplýsingar til að laga vandann:** Sami notandi og setti upp tvískipt skrif.

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stilla nýja töflu fyrir tvískipt skrif. Eini notandinn sem getur búið til vörpun er notandinn sem setti upp tengingu tvískiptrar skrifa.

*Kóði svörunarstöðu bendir ekki til árangurs: 401 (Óheimilt)*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Villa þegar þú opnar tvískipt notendaviðmót

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að komast í tvískipt skrif úr vinnusvæðinu **Gagnastjórnun**:

*login.microsoftonline.com neitaði að tengjast.*

Til að laga málið, skráðu þig inn með því að nota InPrivate glugga í Microsoft Edge, huliðsglugga í Chromium, eða huliðsglugga í Google Chrome. Þú verður einnig að opna eða hreinsa smákökur frá þriðja aðila.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Villa þegar tengt er við umhverfi fyrir tvöfalda skráningu eða nýrri töfluvörpun er bætt við

**Áskilið hlutverk til að laga málið:** Kerfisstjóri bæði í fjármála- og rekstraröppum og Dataverse.

Þú gætir lent í eftirfarandi villu þegar þú tengir eða býrð til kort:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

Þessi villa getur komið fram ef þú hefur ekki nægar heimildir til að tengja tvöfalt skrif eða búa til kort. Þessi villa getur einnig komið upp ef Dataverse-umhverfið var endurstillt án þess að aftengja tvískipt skrif. Allir notendur með hlutverk kerfisstjóra í bæði fjármála- og rekstrarforritum og Dataverse getur tengt umhverfið. Eingöngu notandinn sem setti upp tengingu tvöfaldrar skráningar getur bætt við nýjum töfluvörpunum. Eftir uppsetningu getur allir notendur með hlutverk kerfisstjóra fylgst með stöðunni og breytt vörpununum.

## <a name="error-when-you-stop-the-table-mapping"></a>Villa þegar töfluvörpun er stöðvuð

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stöðva töfluvörpunina:

*\[Forbidden\], \[{"staða":403,"uppruni":"","skilaboð":"Villa úr táknskiptum: Notanda er ekki heimild að fara í tengingu dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*

Þessi villa kemur upp þegar tengt umhverfi Dataverse er ekki í boði.

Til að laga málið, stofnaðu miða fyrir Data Integration teymið. Festu netsporið svo að gagnasamstillingarteymið geti merkt kortin sem **Ekki í gangi** í bakvinnslunni.

## <a name="enable-parallel-processing-in-finance-and-operations-apps-to-improve-performance"></a>Virkjaðu samhliða vinnslu í fjármála- og rekstrarforritum til að bæta árangur

Með því að virkja samhliða vinnslu getur það dregið úr þeim tíma sem þarf til að flytja inn gögn úr Dynamics 365 forritum fyrir þátttöku viðskiptavina og Microsoft Dataverse að fjármögnunar- og rekstraröppum. 

Til að virkja samhliða vinnslu í fjármála- og rekstrarforritum skaltu ljúka eftirfarandi skrefum.

1. Skráðu þig inn í þitt fjármála- og rekstrarumhverfi.
2. Fara til **Gagnastjórnun > Framework færibreytur**.
3. Veldu **Einingastillingar** og veldu **Stilla framkvæmdarfæribreytur eininga**.
4. Bættu við breytum fyrir samhliða vinnslu:
    - **Fjöldi innflutningsþröskulda** – Fjöldi skráa sem þarf að uppfylla áður en samhliða vinnsla er virkjuð.
    - **Innflutningsfjöldi verkefna** – Fjöldi þráða (verkefna) sem á að keyra samhliða.
5. Veldu **Vista**.


## <a name="errors-while-trying-to-start-a-table-mapping"></a>Villur við að reyna að hefja töfluvörpun

### <a name="unable-to-complete-initial-data-sync"></a>Ekki er hægt að ljúka upphaflegri gagnasamstillingu

Þú gætir fengið villu eins og eftirfarandi þegar þú reynir að keyra upphaflega gagnasamstillingu:

*Ekki tókst að ljúka upphaflegir samstillingu gagna. Villa: tvískipt skrif tókust ekki - skráning viðbótar mistókst: Get ekki búið til lýsigögn fyrir uppflettingu tvískiptra skrifa. Tilvísun í villuhlut ekki stillt á tilvik hlutar.*

Þegar þú reynir að stilla stöðu vörpunar á **Í gangi** gætir þú fengið þessa villu. Lagfæringin fer eftir orsök villunnar:

+ Ef vörpunin er með háðar varpanir skaltu ganga úr skugga um að virkja háðar varpanir fyrir þessa töfluvörpun.
+ Hugsanlega vantar í vörpunina dálka upprunastaðar eða viðtökustaðar. Ef dálk í fjármála- og rekstrarappinu vantar skaltu fylgja skrefunum í hlutanum [Vantar töfludálka vandamál á kortum](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Ef dálk vantar í Dataverse skal smella á hnappinn **Uppfæra töflur** í vörpununum svo dálkarnir fyllist sjálfkrafa út í vörpuninni.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Villa vegna misræmis í útgáfu og lausnir tvöfaldrar skráningar uppfærðar

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að keyra töfluvörpunina:

+ *Viðskiptavinaflokkar (msdyn_customergroups) : Tvöföld skrif tókust ekki - Dynamics 365 for Sales lausn „Dynamics365Company“ er með misræmi í útgáfu. Útgáfa „2.0.2.10“ Áskilin útgáfa: „2.0.133“*
+ *Dynamics 365 for Sales lausn „Dynamics365FinanceExtended“ er með misræmi í útgáfu. Útgáfa: „1.0.0.0“ Áskilin útgáfa: „2.0.227“*
+ *Dynamics 365 for Sales lausn „Dynamics365FinanceAndOperationsCommon“ er með misræmi í útgáfu. Útgáfa: „1.0.0.0“ Áskilin útgáfa: „2.0.133“*
+ *Dynamics 365 for Sales lausn „CurrencyExchangeRates“ er með misræmi í útgáfu. Útgáfa: „1.0.0.0“ Áskilin útgáfa: „2.0.133“*
+ *Dynamics 365 for Sales lausn „Dynamics365SupplyChainExtended“ er með misræmi í útgáfu. Útgáfa: „1.0.0.0“ Áskilin útgáfa: „2.0.227“*

Til að laga vandamálið skal uppfæra lausnir tvöföldrar skráningar í Dataverse. Gakktu úr skugga um að uppfæra í nýjustu lausnina sem passar við nauðsynlega útgáfu af lausn.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

