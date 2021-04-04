---
title: Úrræðaleit vegna vandamála tvöfaldrar skráningar í Finance and Operations forritum
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál með tvískrifunareiningunni í forritum Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9bff8ad0c5716648dec6eadfb21412a2b17f155e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561227"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Úrræðaleit vegna vandamála tvöfaldrar skráningar í Finance and Operations forritum

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál með **tvískrifunareiningunni** í forritum Finance and Operations.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Ekki er hægt að hlaða einingu tvískiptrar skriftar í Finance and Operations-forritinu

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

**Nauðsynlegt hlutverk til að laga vandann:** Kerfisstjóri í bæði Finance and Operations-forritum og Dataverse.

Þú gætir lent í eftirfarandi villu þegar þú tengir eða býrð til kort:

*Stöðukóði svars gefur ekki til kynna að hafi tekist: 403 (tokenexchange).<br> Lotukenni: \<your session id\><br> Kenni rótarvirkni: \<your root activity id\>*

Þessi villa getur komið fram ef þú hefur ekki nægar heimildir til að tengja tvöfalt skrif eða búa til kort. Þessi villa getur einnig komið upp ef Dataverse-umhverfið var endurstillt án þess að aftengja tvískipt skrif. Sérhver notandi með hlutverk kerfisstjóra í bæði Finance and Operations-forritum og Dataverse getur tengt umhverfin. Eingöngu notandinn sem setti upp tengingu tvöfaldrar skráningar getur bætt við nýjum töfluvörpunum. Eftir uppsetningu getur allir notendur með hlutverk kerfisstjóra fylgst með stöðunni og breytt vörpununum.

## <a name="error-when-you-stop-the-table-mapping"></a>Villa þegar töfluvörpun er stöðvuð

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stöðva töfluvörpunina:

*\[Forbidden\], \[{"staða":403,"uppruni":"","skilaboð":"Villa úr táknskiptum: Notanda er ekki heimild að fara í tengingu dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*

Þessi villa kemur upp þegar tengt umhverfi Dataverse er ekki í boði.

Til að laga málið, stofnaðu miða fyrir Data Integration teymið. Festu netsporið svo að gagnasamstillingarteymið geti merkt kortin sem **Ekki í gangi** í bakvinnslunni.

## <a name="error-while-trying-to-start-a-table-mapping"></a>Villa við að reyna að hefja töfluvörpun

Þú gætir fengið villu eins og eftirfarandi þegar þú reynir að stilla þessa stöðu vörpunar á **Í gangi**:

*Ekki tókst að ljúka upphaflegir samstillingu gagna. Villa: tvískipt skrif tókust ekki - skráning viðbótar mistókst: Get ekki búið til lýsigögn fyrir uppflettingu tvískiptra skrifa. Tilvísun í villuhlut ekki stillt á tilvik hlutar.*

Lagfæringin á þessari villu fer eftir orsök villunnar:

+ Ef vörpunin er með háðar varpanir skaltu ganga úr skugga um að virkja háðar varpanir fyrir þessa töfluvörpun.
+ Hugsanlega vantar í vörpunina dálka upprunastaðar eða viðtökustaðar. Ef það vantar dálk í Finance and Operations-forritið skaltu fylgja eftirfarandi skrefum í hlutanum [Vandamál vegna töfludálka sem vantar í varpanir](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Ef dálk vantar í Dataverse skal smella á hnappinn **Uppfæra töflur** í vörpununum svo dálkarnir fyllist sjálfkrafa út í vörpuninni.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]