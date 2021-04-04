---
title: Yfirlit rafrænna undirskrifta
description: Þessi grein gefur yfirlit yfir rafrænar undirskriftir og lýsir hvernig hægt er að nota þær.
author: maertenm
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d0279f4ce7e3c7fcd8a10bbf16a6fbdd8a423b7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565650"
---
# <a name="electronic-signatures-overview"></a>Yfirlit rafrænna undirskrifta

[!include [banner](../includes/banner.md)]

Þessi grein gefur yfirlit yfir rafrænar undirskriftir og lýsir hvernig hægt er að nota þær.

## <a name="what-is-an-electronic-signature"></a>Hvað er rafræn undirskrift?

Rafræn undirskrift staðfestir deili á þeim aðila sem er í þann mund að hefja eða samþykkja ferli. Innan sumra atvinnugreina er rafræn undirskrift jafn bindandi að lögum og handskrifuð.

Reglur kveða á um rafrænar undirskriftir innan ýmissa atvinnugreina sem eru háðar opinberum reglugerðum, svo sem við lyfja-, matvæla- og drykkjarvöruframleiðslu og í flugvéla- og geimiðnaði og varnariðnaði. Þær eru einnig nauðsynlegar samkvæmt reglum 21 CFR hluta 11, sem gefnar eru út af Matvæla- og lyfjaeftirliti Bandaríkjanna (FDA).

> [!NOTE]
> Rafræn undirskrift ein og sér er ekki það sama og stafræn undirskrift. Rafræn undirskrift er aðeins staðgengill handskrifaðra undirskrifta, en stafrænar undirskriftir hafa ítarlegri öryggiseiginleika. Með stafrænum undirskriftum er hægt að kanna hvort notandi eða vinnsla hafi átt við gögn. Einnig er hægt að staðfesta stafrænar undirskriftir án þess að eigandi skírteinis sem var notað til undirskriftar geti þráttað fyrir það. Rafrænar undirskriftir deila nokkrum eiginleikum með stafrænum undirskriftum, eins og lýst er hér fyrir neðan.

## <a name="electronic-signatures"></a>Rafrænar undirskriftir

Hægt er að nota rafrænar undirskriftir fyrir mikilvæg viðskiptaferli. Rafrænar undirskriftir eru innbyggður hluti sumra ferla. Hægt er að búa til kröfur um rafrænar undirskriftir fyrir hvaða gagnagrunn eða svæði sem er.

Rafrænar undirskriftir deila nokkrum eiginleikum með stafrænum undirskriftum. Allir notendur sem skrifa undir skjöl þurfa að hafa gilt dulritað skírteini. Þegar skjal er undirritað er einkalykillinn sem tengist skírteininu sannprófaður. Upplýsingar um rafrænar undirskriftir eru skráðar í kladda til þess að hægt sé að rekja slóð aðgerða. Setja upp rafrænar undirskriftir, sjá [Uppsetning rafrænna undirskrifta](tasks/set-up-electronic-signatures.md).

## <a name="users-who-require-access-to-electronic-signatures"></a>Notendur sem þarfnast aðgangs að rafrænar undirskriftir

Þrenns konar notendur krefjast vanalega öryggisaðgangs að rafrænum undirskriftum: Stjórnendur rafrænna undirskrifta, áritendur og endurskoðendur rafrænna undirskrifta.

### <a name="electronic-signature-administrator"></a>Stjórnandi rafrænna undirskrifta

Stjórnandi rafrænna undirskrifta setur upp kröfur um rafrænar undirskriftir, almennar færibreytur og samþykkjendur og fær viðvörum um það þegar sannvottun undirskriftar mistekst. Sjálfgefið er að notendur sem tilheyra öryggishlutverki **upplýsingatæknistjóra** hafi heimild til að stjórna rafrænum undirskriftum.

### <a name="signer"></a>Áritari

Áritari skrifar undir skjöl og ferli sem þarfnast undirskrifta. Sjálfgefið er að notendur sem tilheyra öryggishlutverki **Kerfisnotandi** hafi heimild til undirrita skjöl rafrænt.

> [!NOTE]
> Áritari kann að þurfa viðbótarheimildir til að fá aðgang að gögnum sem tengjast skjölum eða ferlum sem er skrifað undir. Notendur sem gera breytingar á gögnum og þurfa að skrifa undir þær verða að hafa heimildir til að breyta gögnunum. Notandi sem skrifar undir fyrir hönd annars notanda gæti ekki þurft aðgang að gögnunum. Dæmi af þessari gerð notanda er yfirmaður sem skrifar undir fyrir breytingar starfsmanns.

### <a name="electronic-signature-auditor"></a>Endurskoðandi rafrænna undirskrifta

Endurskoðandi rafrænna undirskrifta skoðar kladda gagnagrunns og kladda undirskrifta sem er aðgengilegur úr kladda gagnagrunnsins. Sjálfgefið er að notendur sem tilheyra öryggishlutverki **upplýsingatæknistjóra** hafi heimild til að endurskoða rafrænum undirskriftum.

Ef notað er hlutverk annað en **upplýsingatæknistjóri** skal ganga úr skugga um að hlutverki er úthlutað eftirfarandi réttindum:

- Skoða mistök rafrænna undirskrifta
- Skoða gagnagrunnskladda

## <a name="signing-documents-electronically"></a>Rafræn undirskrift skjals

### <a name="get-a-certificate"></a>Sækja skírteini

Áður en skjöl eru undirrituð rafrænt í þarf að biðja um skírteini.

> [!NOTE]
> Microsoft SQL Server eiginleikar eru notaðir til að stofna skírteini og virkja rafræna undirritun. Ekki þarf að hafa annað umhverfi fyrir skírteini eða lykla.

Þegar þú biður um skírteini eru opinn lykill og einkalykill stofnaðir fyrir þig. Einkalykillinn er dulritaður með aðgangsorði sem aðeins þú veist hvað er. Þegar þú undirritar skjöl rafrænt er auðkenni þitt sannprófað þegar þú færir inn aðgangsorðið.

Til að biðja um skírteini, á **Valkosti** síðunni á **Lykla** flipanum, smellið **Fá skírteini**.

Þú þarft að slá inn og staðfestu aðgangsorðið sem þú notar vegna undirskrifta. Aðgangsorðið er notað til að verja lykilinn þinn og heimila notkun skírteinisins. Aðgangsorðið er ekki vistað í gagnagrunninum og er ekki aðgengilegt öðrum, þ.m.t. kerfisstjóra.

Ef þú manst ekki aðgangsorðið sem þarf til að tengjast skírteininu þarf að endurstilla skírteinið. Endurstilling þess hefur ekki áhrif á skjöl sem þú hefur undirritað með því. Til að endurstilla skírteinið, á **Valkosti** síðunni er smellt á **Endurstilla skírteini**.

### <a name="sign-a-document-electronically"></a>Rafræn undirskrift skjals

Síðan **Skrifa undir skjal** birtist þegar breyting er gerð sem krefst rafrænnar undirskriftar.

1. Á **Skrifa undir skjal** síðunni smellirðu á **Skjal** til að skoða breytingar sem voru gerðar á skjalinu.
2. Veldu ástæðukóða á flipanum **Undirskrift**.
3. Færið inn athugasemd ef athugasemd er krafist.
4. Ef notandakennið þitt birtist ekki á svæðinu **Áritari** skaltu velja það af listanum.
5. Færið inn staðsetningu þína, ef þörf er á þessum upplýsingum.
6. Smelltu á **Í lagi**.

### <a name="sign-for-another-users-changes"></a>Skrifa undir fyrir breytingar annars notanda

Stundum þarf notandi að skrifa undir fyrir breytingar annars notanda. Til dæmis gæti stjórnandi þurft að skrifa undir breytingar sem starfsmaður gerir á uppskrift. Notaðu þetta ferli til að gera notanda að áritara fyrir annan notanda.

> [!NOTE]
> Þegar notandi skrifar undir fyrir breytingar annars notanda verður undirskriftin að vera veitt á vinnustöð notandans sem gerði breytingarnar. Notandinn getur ekki vistað breytinguna fyrr en undirskrift hefur verið innt af hendi.

Fylgið eftirfarandi skrefum til að tilgreina samþykkjendur.

1. Á síðunni **Valkosti** á flipanum **Lykla**, smellið **Tilgreina samþykkjanda**.
2. Í **notandakenni samþykktaraðila** reit, velja kenni þess notanda sem á að skrifa undir breytingar annars notanda.
3. Í **undirrita fyrir notandakenni** reit, velja kenni notandans sem þarf að skrifa undir fyrir þegar hann gerir breytingar.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]