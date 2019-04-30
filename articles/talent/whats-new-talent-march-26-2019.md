---
title: Hvað er nýtt eða breytt í Dynamics 365 for Talent (26. mars 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
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
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 568a16a17ed3269c7b72f27f0d4b7bbdbd56630e
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/12/2019
ms.locfileid: "949829"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-26-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 for Talent (26. mars 2019)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

### <a name="enhancements-to-interview-scheduling"></a>Endurbætur á áætlanagerð viðtals
Eftirfarandi viðbætur eru í boði í áætlanagerð viðtals.

- Ráðningaraðilar eða ráðningarstjórar geta nú handvirkt ræst áminningu fyrir viðtal til að senda inn endurgjöf þeirra. Tengd sniðmát fyrir tölvupóst fyrir áminninguna er einnig stillanleg.
- Á meðan samantekt viðtals er deilt með umsækjandanum, getur áætlunaraðili viðtals valið að fela nöfnin á spyrlum og einnig valið að fela raðir úr yfirliti á samantekt viðtals.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

### <a name="embedded-images-in-activities"></a>Innfelldar myndir í aðgerðum
Þú getur nú fellt myndir beint inn í aðgerðir. Auk þess að geta afritað og límt myndir af vefnum, er hægt að hlaða upp myndum úr staðbundnu skráarkerfi. Stærð aðgerðarinnar takmarkast við 1 MB. Ef myndin er of stór skaltu breyta stærð hennar og reyna að hlaða upp aftur.

[![Vörpun](./media/embedimages.png)](./media/embedimages.png)

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR
**Smíði 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Stuðningur fyrir sérstillt svæði er í boði fyrir valdar einingar í Common Data Service 

Eftirfarandi Common Data Service einingar styðja nú svæði viðskiptavinar sem eru stofnuð í Dynamics 365 for Talent:

- Starfskraftur
- Þjóðernisuppruni
- Uppgjafahermennskustaða
- Tungumálskóði
- Vinnsla
- Vinnslugerð
- Starfshlutverk
- Staða
- Tegund stöðu
 
### <a name="employment-history-not-displayed-chronologically"></a>Ráðningarsaga birtist ekki í tímaröð
Með þessari breytingu sýnir síða ráðningarsögu nú færslur starfsmanns í tímaröð, óháð fyrirtæki. Einnig er hægt að nota flokkunarmöguleika til að flokka eftir fyrirtæki.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Launafyrirkomulag fastra launa birtist ekki þegar notandi takmarkast við fyrirtæki í öryggi.
Í þessari útgáfu birtist nú launafyrirkomulag fastra launa þegar notandi takmarkast við fyrirtæki í öryggi. Allar öryggisstillingar verða heiðraðar og föst áætlanir munu birtast fyrir þau fyrirtæki þar sem notandinn hefur aðgangsheimild. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Ekki er hægt að eyða starfsfærslum með opna í Excel möguleikann í Talent
Með þessari útgáfu getur þú nú fjarlægt starfsfærslur með því að nota valkostinn **Opna í Excel** í Dynamics 365 for Talent.

### <a name="upgrade-to-common-data-service"></a>Uppfæra í Common Data Service
Frestur til að uppfæra í Common Data Service rennur brátt út. Skráðu þig inn á stjórnandamiðstöð PowerApps til að ákvarða hvort þurfi að uppfæra gagnagrunninn þinn. Frekari upplýsingar um fresti og nauðsynlegar ráðstafanir til að uppfæra er að finna í [Uppfæra í Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Í kynningarútgáfu

Nánari upplýsingar um virkun á forskoðunareiginleikum er að finna í [Fá aðgang að forskoðunareiginleikum í Talent](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Leyfa að tilgreina ástæðukóða fyrir leyfisgerðir
Fyrirtæki gætu þurft viðbótarupplýsingar sem tengjast frítímabeiðnum. Til að fá þessar upplýsingar þurfa starfsmenn að hafa með ástæðukóða á frítímabeiðnum sínum. Með þessari útgáfu getur þú nú tilgreint ástæðukóðana sem tengjast ákveðinni leyfisgerð og gert starfsmönnum kleift að velja ástæðukóða fyrir frítímabeiðnir sínar.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Stilla ástæðukóða þannig að þeirra sé krafist þegar frítími er sendur inn fyrir tilteknar leyfisgerðir
Fyrirtæki gætu krafist þess að ástæðukóðar verðir settir á ákveðnar leyfisgerðir þegar starfsfólk sendir inn frítíma. Hugsanlega verður þetta nauðsynlegt út af lagaskilyrðum í landi/svæði eða vegna stefnu fyrirtækis. Þessi útgáfa gerir mannauðsstjóra kleift að tilgreina hvaða leyfisgerðir þurfa ástæðukóða. Þessu verður framfylgt þegar starfsmenn leggja inn beiðni um frítíma þar sem leyfið krefst ástæðukóða.

## <a name="coming-soon"></a>Væntanlegt

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Ítarlegt launaöryggi (fast og breytilegt)
Í mörgum fyrirtækjum er hugsanlegt að launa- og fríðindastjórar hafi aðeins aðgang að ákveðnum launafærslum. Þessar færslur gætu verið fyrir stjórnendur eða svæðisbundna starfsmenn. Með þessari breytingu geta mannauðsstjórar haft umsjón með launafyrirkomulaginu fyrir mismunandi starfsmannahópa í fyrirtækinu. Hægt er að úthluta öryggishlutverkum á fastar og breytilegar áætlanir sem ákvarða aðgang að áætlunum og starfsmannaupplýsingum sem tengjast áætlunum, t.d. launa- eða bónusfærslur. Aðeins þau hlutverk sem eru með aðgang geta unnið úr launum fyrir þessa starfsmenn.

###  <a name="email-support-for-alerts"></a>Tölvupóstur út af viðvörunum
Í verkvangsuppfærslu 25 geta notendur stofnað viðvörunarreglur sem senda sjálkrafa tilkynningar í tölvupósti á tengiliði þegar þær ræsast út af tilviki. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Afrita athuganir starfsmanns: Breytingar á notandaviðmóti
Með þessari breytingu er borið kennsl á tvítekningar á meðan þú færir inn heiti á reitum og staða sýnir hversu margar tvítekningar fundust. Þú getur valið tengilinn sem gefinn er upp til að opna nýja síðu til að meta hvort nota skuli samsvörun sem borin var kennsl á. Til að forðast að trufla gagnafærslu, opnast tvítekin skjámynd ekki sjálfkrafa.
