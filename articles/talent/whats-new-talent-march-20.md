---
title: Hvað er nýtt eða breytt í Dynamics 365 Talent (20. mars 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
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
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a7a44e1c9d8dcb4b2cc81a682a044d26cdc1149e
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812696"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-20-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 Talent (20. mars 2019)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

### <a name="setting-the-audience-on-activities"></a>Að velja notandahóp fyrir aðgerðir
Aðgerðir í kerfinu geta nú verið með notandahóp skilgreindan. Hægt er að stilla aðgerðir (t.d. viðtal, áætlun, endurgjöf og EEO) fyrir alla umsækjendur, umsækjendur innan fyrirtækis og umsækjendur utan fyrirtækis. Sérsniðnir aðgerðir, t.d. Microsoft Forms, YouTube-myndbönd og vefefni er hægt að senda á alla umsækjendur, umsækjendur innan fyrirtækis, umsækjendur utan fyrirtækis eða ráðningarhópinn.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Bæta sýnileika á störfum á ráðningarsíðu: Leitarvélabestun
Þessi eiginleiki gerir skriðlum leitarvélar kleift að ná til og vísa í starfsauglýsingar á ráðningarsíðu Attract. Þetta auðveldar umsækjendum að finna störf sem birt eru á ráðningarsíðu Attract með því að nota vinsælar leitarvélar.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Sýna þeim umsækjendum sem gleyma aðgangsupplýsingum sínum vísbendingu um innskráningu
Ef umsækjandi gleymir aðgangsupplýsingum sem hann notaði til að sækja um starf með því að opna hlekk sem var vistaður eða sendur í tölvupósti, sér hann nú vísbendingu með nafni þjónustuaðilans og notandanafni (brenglað). Þetta hjálpar honum að nota réttar aðgangsupplýsingar til að opna starfsumsóknina sína.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Hjálpa umsækjendum innan fyrirtækis að skoða störf innan fyrirtækis
Vandamál hefur verið lagað þar sem umsækjendur utan fyrirtækis gátu séð nafn ráðningaraðilans eða ráðningarstjórans fyrir starf. Nú geta aðeins umsækjendur innan fyrirtækis séð meðlimi ráðningarhóps fyrir starf. Það er líka auðveldara fyrir umsækjendur innan fyrirtækis að skoða og sækja eingöngu um störf innan fyrirtækis. Þegar umsækjandi reynir að opna hlekkinn til að skoða eða sækja um starf sem er eingöngu innan fyrirtækis, neyðist hann til að sannvotta sig með Azure Active Directory-aðgangsupplýsingum. Umsækjendur innan fyrirtækis geta einnig haft samband við meðlim ráðningarhópsins til að láta í ljós áhuga á starfi eða til að fá að vita meira um starfið. Þessi möguleiki er í boði fyrir öll störf fyrir einungis umsækjendur innan fyrirtækis. Nánari upplýsingar er að finna í [Settu upp ferilssíðu í Microsoft Dynamics 365 Talent - Attract](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Merkja við silfurhafa til að úthluta verðmætum umsækjendum fyrir framtíðarstöður
Ráðningaraðilar og ráðningarstjórar geyma oft lista yfir umsækjendur sem hentuðu stöðunni vel en var ekki hægt að bjóða þeim starfið því að annar fékk starfið. Slíkir umsækjendur, kallaðir silfurhafar, eru verðmætir því að þeir geta dregið úr tímanum sem tekur að ráða næst þegar svipuð staða opnast. Attract gerir nú ráðningaraðilum og ráðningarstjórum kleift að setja silfurhafa inn á umsækjendalistann ef umsækjandinn kemst á boðsstigið. Þeir sem eru merktir sem silfurhafar birtast á umsækjendalista fyrir starfið, en einnig í yfirliti hæfileikasafns þegar þessir umsækjendur eru meðlimir í einhverjum söfnum ráðningaraðila eða ráðningarstjóra. Að auki mun merkingin birtast í starfssögunni sem hluti af hæfileikasafni í notandaupplýsingum umsækjanda. Hægt er að forskoða þennan eiginleika með því að fá stjórnanda til að kveikja á honum með [Stjórnun eiginleika í stjórnandamiðstöðinni](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="add-applicants-to-talent-pools"></a>Bæta umsækjendum við hæfileikasöfn
Nú er auðveldara að bæta umsækjendum við hæfileikasöfn með því að kalla á nýja aðgerð í umsækjandalistanum. Með því að velja táknið **Bæta við hæfileikasafn** getur ráðningaraðili eða ráðningarstjóri valið úr listanum sínum yfir hæfileikasöfn og auðveldlega bætt umsækjendum við hæfileikasöfn beint úr umsækjendalista starfsins.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Stilla hvort ferilskrá sé nauðsynleg til að sækja um ákveðið starf
Á grunni athugasemda viðskiptavina geta ráðningaraðilar nú stillt hvort ferilskrá, í formi skráar sem hlaðið er upp, er nauðsynleg þegar sótt er um tiltekið starf. Þessi stilling er hluti af umsóknaraðgerð, aðgengileg í ráðningarferlinu. Þegar hún er virk verða allir hugsanlegir umsækjendur beðnir um að hlaða upp ferilskrá þegar þeir sækja um þessa stöðu. Umsóknin verður ekki talin kláruð nema ferilskrá sé hlaðið upp. Þetta hjálpar til við að draga úr flækjum í umsækjendasafni með því að tryggja að allir umsækjendur útvegi nægar upplýsingar til að leyfa ráðningaraðila að flokka þær.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Umsækjendur geta sótt um starf með LinkedIn-notandasíðu sinni
Umsækjendur sem eru nú þegar með uppfærða notandasíðu á LinkedIn geta sótt um störf með aðeins einum smelli í gegnum notandasíðuna.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Fylgjast með því hvernig notandasíða umsækjanda varð til í kerfinu og hvaðan umsækjendur finna störfin sem þeir sækja um
Nú er hægt að finna út hvernig tiltekin notandasíða umsækjanda varð til í Attract með því að skoða uppruna notandasíðu undir upplýsingum umsækjanda á síðunni **Notandaupplýsingar** fyrir notandasíðu umsóknar eða hæfileikasafns. Með svipuðum hætti er hægt að finna út hversu margir umsækjendur fundu starfið með því að líta á upprunastað umsóknar sem finnst í **Umsóknaraðgerð** í straumi umsóknaraðgerðar. Þessar upplýsingar eru líka í boði í starfssögunni á notandasíðu hæfileikasafns. Þegar ráðningaraðilar eða ráðningarstjórar bæta við umsækjendum handvirkt, verða þeir einnig beðnir um að tilgreina uppruna umsóknarinnar eða notandasíðu umsækjanda. Þegar umsækjandi sækir um í fyrsta skipti verður uppruni notandasíðu þeirra sá sami og er fyrir umsóknina hans. Hægt er að forskoða þennan eiginleika með því að fá stjórnanda til að kveikja á honum með [Stjórnun eiginleika í stjórnandamiðstöðinni](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature). Hafðu í huga að núverandi umsækjendur og umsóknaraðilar verða ekki með neinar upprunaupplýsingar. Hins vegar geta ráðningaraðilar bætt þessum upplýsingum við handvirkt.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2195

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Attract-samþætting hendir tvíteknum færsluvillum fyrir umsóknir
Í þessari uppfærslu hefur vandamál vegna tvítekinna færslna verið lagað. Þetta vandamál kemur upp þegar vinnusvæðið **Starfsmannastjórnun** er opnað.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Ekki er hægt að loka skjámynd þegar nafnaröð er breytt
Breytingar hafa verið gerðar til að leiðrétta vandamál þegar nafnaröð er breytt í skjámynd starfsmanna.

## <a name="coming-soon"></a>Væntanlegt

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Ítarlegt launaöryggi (fast og breytilegt)
Í mörgum fyrirtækjum er hugsanlegt að launa- og fríðindastjórar hafi aðeins aðgang að ákveðnum launafærslum. Þessar færslur gætu verið fyrir stjórnendur eða svæðisbundna starfsmenn. Með þessari breytingu geta mannauðsstjórar haft umsjón með launafyrirkomulaginu fyrir mismunandi starfsmannahópa í fyrirtækinu. Hægt er að úthluta öryggishlutverkum á fastar og breytilegar áætlanir sem ákvarða aðgang að áætlunum og starfsmannaupplýsingum sem tengjast áætlunum, t.d. launa- eða bónusfærslur. Aðeins hlutverk með veittan aðgang geta unnið úr launum fyrir þessa starfsmenn.

###  <a name="email-support-for-alerts"></a>Tölvupóstur út af viðvörunum
Með verkvangsuppfærslu 24 fyrir Finance and Operations geta notendur stofnað viðvörunarreglur sem senda sjálfkrafa tilkynningar í tölvupósti á tengiliði þegar þær ræsast út af tilviki.

### <a name="duplicate-employee-check-interface-changes"></a>Afrita athugun starfsmanns: Viðmót breytist
Með þessari breytingu er borið kennsl á tvítekningar á meðan þú færir inn heiti á reitum og staða sýnir hversu margar tvítekningar fundust. Þú getur valið tengilinn sem gefinn er upp til að opna nýja síðu til að meta hvort nota skuli samsvörun sem borin var kennsl á. Tvítekin skjámynd opnast ekki sjálfkrafa, til að koma í veg fyrir truflandi gagnafærslu.


