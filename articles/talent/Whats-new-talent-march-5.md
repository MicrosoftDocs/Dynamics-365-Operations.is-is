---
title: Hvað er nýtt eða breytt í Dynamics 365 Talent (5. mars 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 855eafaca88d180997cf5a68c7f0fe975c177f88
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898920"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 Talent (5. mars 2019)

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

### <a name="extending-option-sets-in-attract"></a>Safn valkosta fyrir stækkunarhæfni í Attract

Í Attract eru mörg svæði sem eru söfn valkosta innan Common Data Service. Nýir möguleikar hafa verið kynntir til að stækka söfn valkosta, fyrst ástæðureiturinn **Höfnun**, reiturinn **Starfsgerð** og reiturinn **Starfsaldursgerð**.

> [!IMPORTANT]
> Virknin fyrir auglýsingu starfs á LinkedIn krefst notkunar á reitunum **Starfsgerð** og **Starfsaldursgerð** á síðunni **Upplýsingar um starf**. Sjálfgefin gildi í þessum reitum eru studd af LinkedIn og birtast þegar starfið er auglýst. Ef þú auglýsir störf á LinkedIn og þú breytir núverandi gildum á safni valkosta fyrir þessi svæði, mun starfið samt birtast en LinkedIn mun ekki sýna sérstilltu gildin **Starfsgerð** og **Starfsaldursgerð**.

## <a name="changes-in-onboarding"></a>Breytingar á nýliðun

### <a name="private-preview-for-onboard-teams"></a>Einkaforskoðun fyrir Onboard-hópa
Þú getur nú auðveldlega deilt og verið í samstarfi með sniðmát þvert yfir allt fyrirtækið. Frekari upplýsingar eru í [Deila bestu starfsvenjum yfir allt fyrirtækið með Onboard Teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Einkaforskoðun fyrir staðgengla viðtakanda
Þú getur auðgað sniðmát þitt með því að úthluta aðgerðum á hlutverk í stað einstaklinga. Hlutverkum er síðan úthlutað á einstaklinga við stofnun á leiðbeiningum. Frekari upplýsingar er að finna í [Einfalda stýringu leiðbeininga með úthlutun aðgerða á hlutverk](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>Breytingar í Core HR
**Smíði 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>Skilgreina verkflæði til að samþykkja sjálfkrafa eða fylgja verkflæði þegar mannauðsstjóri eða næsti yfirmaður sendir inn eða uppfærir beiðni um frítíma
Nýjum skilyrðum verkflæðis hefur verið bætt við svo leyfisbeiðnir verði samþykktar sjálfkrafa ef þær eru sendar inn af yfirmanni starfsmanns eða mannauðsstjóra. Ein leið til að ná þessu sjálfvirka samþykki í verkflæði er að virkja sjálfvirka aðgerð í verkflæðissamþykkinu.

Skilyrðunum sem hefur verið bætt við fela í sér:

- Sent inn af - Notað til að meta auðkenni kerfisnotanda sem sendi inn beiðni um verkflæði.
- Sent inn fyrir hönd - Notað til að meta leyfisbeiðni ef hún var send inn fyrir hönd starfsmanns sem tengist beiðninni.
- Sent inn af mannauðsstjóra - Notað til að meta hvort kerfisnotandi sem sendi beiðnina inn í verkflæði sé með hlutverk mannauðsstjóra.
- Sent inn af yfirmanni - Notað til að meta hvort notandi sem sendi inn leyfisbeiðni til verkflæðis sé næstur í stjórnendastigveldi starfsmannsins sem tengist beiðninni.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Virkja föst laun starfsmanns fyrir komandi stöðuverkefni
Það er dæmigert fyrir starfsmenn að byrja hjá fyrirtæki með upphafsdagsetningu fram í tímann. Þessi breyting gerir kleift að skilgreina föst laun fyrir starfsmenn með stöðuverkefni fram í tímann.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Svæði launastöðu eru auð þegar breyting er gerð á stöðunni
Með þessari breytingu, þegar beiðnir eru gerðar um breytingar á núverandi stöðum, munu launasvæðin fá að sjálfgefnu núverandi gildi.

### <a name="other-miscellaneous-bug-fixes"></a>Ýmsar aðrar villuleiðréttingar
Aðrar minniháttar villuleiðréttingar eru með þessari útgáfu.

### <a name="upgrade-to-common-data-service"></a>Uppfæra í Common Data Service
Frestur til að uppfæra í Common Data Service rennur brátt út. Skráðu þig inn á stjórnandamiðstöð Power Apps til að ákvarða hvort þurfi að uppfæra gagnagrunninn þinn. Frekari upplýsingar um fresti og nauðsynlegar ráðstafanir til að uppfæra er að finna í [Uppfæra í Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Væntanlegt

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Ítarlegt launaöryggi (fast og breytilegt)
Í mörgum fyrirtækjum geta margir umsjónaraðilar launa og fríðinda eingöngu fengið aðgang að ákveðnum launafærslum, t.d. færslur fyrir yfirmenn eða svæðisbundna starfsmenn. Með þessari breytingu geturðu haft umsjón með launafyrirkomulaginu fyrir mismunandi starfsmannahópa í fyrirtækinu. Hægt er að úthluta föstum og breytilegum áætlunum öryggishlutverkum, sem ákvarðar aðgang að áætlunum og starfsmannaupplýsingum sem tengjast áætlunum, t.d. launa- eða bónusfærslur. Aðeins hlutverk með veittan aðgang geta unnið úr launum fyrir þessa starfsmenn.

###  <a name="platform-update-24-for-finance-and-operations"></a>Verkvangsuppfærsla 24 fyrir Finance and Operations
Frekari upplýsingar um verkvangsuppfærslu 24 fyrir Finance and Operations er að finna í [Hvað er nýtt og hvað hefur breyst í Finance and Operations verkvangsuppfærsla 24 (mars 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
