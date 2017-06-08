---
title: "Yfirlit yfir rafrænar undirskriftir"
description: "Þessi grein gefur yfirlit yfir rafrænar undirskriftir og lýsir hvernig hægt er að nota þær í Microsoft Dynamics 365 for Operations."
author: maertenm
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5adf45769657e4da81af00b2114a2c1a98655207
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="electronic-signature-overview"></a>Yfirlit yfir rafrænar undirskriftir

[!include[banner](../includes/banner.md)]


Þessi grein gefur yfirlit yfir rafrænar undirskriftir og lýsir hvernig hægt er að nota þær í Microsoft Dynamics 365 for Operations.

<a name="what-is-an-electronic-signature"></a>Hvað er rafræn undirskrift?
--------------------------------

Rafræn undirskrift staðfestir deili á þeim aðila sem er í þann mund að hefja eða samþykkja ferli. Innan sumra atvinnugreina er rafræn undirskrift jafn bindandi að lögum og handskrifuð. Reglur kveða á um rafrænar undirskriftir innan ýmissa atvinnugreina sem eru háðar opinberum reglugerðum, svo sem við lyfja-, matvæla- og drykkjarvöruframleiðslu og í flugvéla- og geimiðnaði og varnariðnaði. Þær eru einnig nauðsynlegar samkvæmt reglum 21 CFR hluta 11, sem gefnar eru út af Matvæla- og lyfjaeftirliti Bandaríkjanna (FDA). **Athugið:** Rafræn undirskrift er ekki það sama og stafræn undirskrift. Rafræn undirskrift er aðeins staðgengill handskrifaðra undirskrifta, en stafrænar undirskriftir hafa ítarlegri öryggiseiginleika. Með stafrænum undirskriftum er hægt að kanna hvort notandi eða vinnsla hafi átt við gögn. Einnig er hægt að staðfesta stafrænar undirskriftir án þess að eigandi skírteinis sem var notað til undirskriftar geti þráttað fyrir það. Rafrænar undirskriftir í  Microsoft Dynamics 365 for Operations eru með innbyggða virkni stafrænnar undirskriftum, eins og lýst er hér fyrir neðan.

## <a name="electronic-signatures-in-dynamics-365-for-operations"></a>Rafrænar undirskriftir í Dynamics 365 for Operations
Hægt er að nota rafrænar undirskriftir fyrir mikilvæg viðskiptaferli í Dynamics 365 for Operations. Rafrænar undirskriftir eru innbyggður hluti sumra ferla. Hægt er að búa til kröfur um rafrænar undirskriftir fyrir hvaða gagnagrunn eða svæði sem er. Rafrænar undirskriftir deila nokkrum eiginleikum með stafrænum undirskriftum. Allir notendur sem skrifa undir skjöl þurfa að hafa gilt dulritað skírteini. Þegar skjal er undirritað er einkalykillinn sem tengist skírteininu sannprófaður. Dynamics 365 for Operations skráir upplýsingar um rafrænar undirskriftir í kladda til þess að hægt sé að rekja slóð aðgerða. Setja upp rafrænar undirskriftir, sjá [Uppsetning rafrænna undirskrifta (verkefnaleiðbeiningar)](http://ax.help.dynamics.com/en/wiki/set-up-electronic-signatures/).

## <a name="users-who-require-access-to-electronic-signatures"></a>Notendur sem þarfnast aðgangs að rafrænar undirskriftir
Þrenns konar notendur krefjast vanalega öryggisaðgangs að rafrænum undirskriftum: Stjórnendur rafrænna undirskrifta, áritendur og endurskoðendur rafrænna undirskrifta.

### <a name="electronic-signature-administrator"></a>Stjórnandi rafrænna undirskrifta

Stjórnandi rafrænna undirskrifta setur upp kröfur um rafrænar undirskriftir, almennar færibreytur og samþykkjendur og fær viðvörum um það þegar sannvottun undirskriftar mistekst. Sjálfgefið er að notendur sem tilheyra öryggishlutverki **upplýsingatæknistjóra** hafi heimild til að stjórna rafrænum undirskriftum.

### <a name="signer"></a>Áritari

Áritari skrifar undir skjöl og ferli sem þarfnast undirskrifta. Sjálfgefið er að notendur sem tilheyra öryggishlutverki **Kerfisnotandi** hafi heimild til undirrita skjöl rafrænt. **Athugasemd** Áritari kann að þurfa viðbótarheimildir til að fá aðgang að gögnum sem tengjast skjölum eða ferlum sem er skrifað undir. Notendur sem gera breytingar á gögnum og þurfa að skrifa undir þær verða að hafa heimildir til að breyta gögnunum. Notandi sem skrifar undir fyrir hönd annars notanda gæti ekki þurft aðgang að gögnunum. Dæmi af þessari gerð notanda er yfirmaður sem skrifar undir fyrir breytingar starfsmanns.

### <a name="electronic-signature-auditor"></a>Endurskoðandi rafrænna undirskrifta

Endurskoðandi rafrænna undirskrifta skoðar kladda gagnagrunns og kladda undirskrifta sem er aðgengilegur úr kladda gagnagrunnsins. Sjálfgefið er að notendur sem tilheyra öryggishlutverki **upplýsingatæknistjóra** hafi heimild til að endurskoða rafrænum undirskriftum. Ef notað er hlutverk annað en **upplýsingatæknistjóri** skal ganga úr skugga um að hlutverki er úthlutað eftirfarandi réttindum:

-   Skoða mistök rafrænna undirskrifta
-   Skoða gagnagrunnskladda

## <a name="signing-documents-electronically"></a>Rafræn undirskrift skjals
### <a name="get-a-certificate"></a>Sækja skírteini

Áður en skjöl eru undirrituð rafrænt í Dynamics 365 for Operations þarf að biðja um skírteini. **Athugið:** Dynamics 365 for Operations notar aðgerðir Microsoft SQL Server til að stofna skírteini og virkja rafræna undirritun. Ekki þarf að hafa annað umhverfi fyrir skírteini eða lykla. Þegar þú biður um skírteini eru opinn lykill og einkalykill stofnaðir fyrir þig í gagnagrunni Dynamics 365 for Operations. Einkalykillinn er dulritaður með aðgangsorði sem aðeins þú veist hvað er. Þegar þú undirritar skjöl rafrænt er auðkenni þitt sannprófað þegar þú færir inn aðgangsorðið. Til að biðja um skírteini, á **Valkosti** síðunni á **Lykla** flipanum, smellið **Fá skírteini**. Þú þarft að slá inn og staðfestu aðgangsorðið sem þú notar vegna undirskrifta. Aðgangsorðið er notað til að verja lykilinn þinn og heimila notkun skírteinisins. Aðgangsorðið er ekki vistað í gagnagrunninum og er ekki aðgengilegt öðrum, þ.m.t. kerfisstjóra Dynamics 365 for Operations. Ef þú manst ekki aðgangsorðið sem þarf til að tengjast skírteininu þarf að endurstilla skírteinið. Endurstilling þess hefur ekki áhrif á skjöl sem þú hefur undirritað með því. Til að endurstilla skírteinið, á **Valkosti** síðunni er smellt á **Endurstilla skírteini**.

### <a name="sign-a-document-electronically"></a>Rafræn undirskrift skjals

Síðan **Skrifa undir skjal** birtist þegar breyting er gerð sem krefst rafrænnar undirskriftar.

1.  Á **Skrifa undir skjal** síðunni smellirðu á **Skjal** til að skoða breytingar sem voru gerðar á skjalinu.
2.  Veldu ástæðukóða á flipanum **Undirskrift**.
3.  Færið inn athugasemd ef athugasemd er krafist.
4.  Ef notandakennið þitt birtist ekki á svæðinu **Áritari** skaltu velja það af listanum.
5.  Færið inn staðsetningu þína, ef þörf er á þessum upplýsingum.
6.  Smelltu á **Í lagi**.

### <a name="sign-for-another-users-changes"></a>Skrifa undir fyrir breytingar annars notanda

Stundum þarf notandi að skrifa undir fyrir breytingar annars notanda. Til dæmis gæti stjórnandi þurft að skrifa undir breytingar sem starfsmaður gerir á uppskrift. Notaðu þetta ferli til að gera notanda Dynamics 365 for Operations að áritara fyrir annan notanda. **Athugið:** Þegar notandi skrifar undir fyrir breytingar annars notanda verður undirskriftin að vera veitt á vinnustöð notandans sem gerði breytingarnar. Notandinn getur ekki vistað breytinguna fyrr en undirskrift hefur verið innt af hendi. Fylgið eftirfarandi skrefum til að tilgreina samþykkjendur.

1.  Á síðunni **Valkosti** á flipanum **Lykla**, smellið **Tilgreina samþykkjanda**.
2.  Í **notandakenni samþykktaraðila** reit, velja kenni þess notanda sem á að skrifa undir breytingar annars notanda.
3.  Í **undirrita fyrir notandakenni** reit, velja kenni notandans sem þarf að skrifa undir fyrir þegar hann gerir breytingar.




