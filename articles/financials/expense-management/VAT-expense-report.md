---
title: "Endurgreiðsla virðisaukaskatts í útgjaldastýringu"
description: "Þetta efnisatriði útskýrir hvernig á að fá endurgreiðslur á gjaldgengum virðisaukaskatti (VSK)."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: is-is
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a>Endurgreiðsla virðisaukaskatts í útgjaldastýringu

[!include [banner](../includes/banner.md)]

Til að fá endurgreiðslur á gjaldgengum virðisaukaskattsfærslum (VSK) þarf fyrirtæki eða stofnun að bera kennsl á, safna, staðfesta og leggja fram nákvæmar upplýsingar. Þetta ferli felur í sér mörg verk og getur, fer eftir stærð fyrirtækis, þurft nokkra starfsmenn eða hlutverk.

Til að endurheimta virðisaukaskatt með því að nota útgjaldastýringu verður að fylgja eftirfarandi forsendum:

- Skattkóðar verða að vera stofnaðir fyrir lönd/svæði sem eru úthlutuð á kostnaðarflokka.
- Stofna verður VSK-flokk fyrir hvern skattkóða.
- Stofna verður VSK-kóða vöru fyrir hvern VSK-flokk.

Eftir að forsendur eru uppfylltar, fylgja starfsmenn þessum skrefum til að óska eftir endurgreiðslum vegna VSK-færslna.

1. Á kostnaðarskýrslu skal færa inn skattaupplýsingar um kreditkortafærslur til að bera kennsl á gjaldgengar VSK endurgreiðslur.
2. Tryggið að allar skattaupplýsingar séu til staðar og bókið síðan kostnaðarskýrsluna.
3. Vinnukostnaður sem er gjaldgengur fyrir alþjóðlega endurgreiðslu virðisaukaskatts.
4. Senda gögn um endurgreiðslu virðisaukaskatts til þriðja aðila lánardrottins til að skrá skil á alþjóðlegri endurgreiðslu.
5. Vinna úr kostnaði fyrir innlenda endurgreiðslu virðisaukaskatts.

Eftirfarandi kaflar gefa dæmi sem sýna hvernig starfsmenn Cantoso ljúka hverju skrefi.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Á kostnaðarskýrslu skal færa inn skattaupplýsingar um kreditkortafærslur til að bera kennsl á gjaldgengar VSK endurgreiðslur

Nancy, sölufulltrúi Contoso, sem er með aðsetur í Bandaríkjunum, kom nýlega úr söluferð til Bretlands. Í ferðinni stofnaði hún nokkra persónulega kostnaði á kreditkorti vegna máltíða. Núna þarf Nancy að stofna kostnaðarskýrslu til að afstemma kostnaðinn.

Þegar Nancy færir upplýsingar inn á kostnaðarskýrsluna velur hún **Bretland** í reitnum **Land/Svæði** á síðunni **Breyta kostnaðarskýrslu**. Listinn yfir VSK-flokka er síðan síaður þannig að hann sýni aðeins flokkana sem eiga við um Bretland. Nancy velur VSK-flokkinn **Bretland 001** og velur síðan VSK-vöruflokkinn **Máltíðir**. Hún bætir síðan við nýrri færslu fyrir gistingu. Vegna þess að það er aðeins einn VSK-flokkur og VSK-vöruflokkur fyrir gistingu í Bretlandi, fyllast þessar upplýsingar sjálfkrafa inn á kostnaðarskýrslu Nancy.

Samkvæmt stefnu Contoso skal allur kostnaður hafa samsvarandi kvittun. Þess vegna, þegar Nancy vistar kostnaðarskýrslu sína, fær hún skilaboð um að hún þurfi að láta kvittun fylgja með hverri færslu sem hún skráði á kostnaðarskýrsluna. Nancy staðfestir að hún hafi látið stafræna mynd af hverri færslukvittun fylgja með kostnaðarskýrslunni og sendir síðan skýrsluna til samþykktar. Síðan sendir hún pappírskvittanir til teymis bakvinnslu. Þessi hópur mun senda gögn um endurgreiðslu virðisaukaskatts til þriðja aðila lánardrottins sem skráir skil á alþjóðlegri endurgreiðslu virðisaukaskatts fyrir Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Tryggið að allar skattaupplýsingar séu til staðar og bókið síðan kostnaðarskýrsluna

April, gjaldkeri Contoso, verður að færa inn allar skattaupplýsingar sem eru ekki til staðar í kostnaðarskýrslu áður en hægt er að bóka skýrsluna. Hún opnar síðuna **Upplýsingar kostnaðarskýrslu** og sér samþykkta kostnaðarskýrslu Nancy. April opnar síðan kostnaðarskýrsluna til að skoða færsluupplýsingarnar. Hún sér að Nancy færði ekki inn VSK-flokk vöru fyrir eina færsluna. Vegna þess að þessar upplýsingar eru ekki veittar, getur April ekki bókað kostnaðarskýrsluna. Því kíkir April á síðuna **Skattaskilgreiningar** í kostnaðarstjórnun og finnur viðeigandi VSK-flokk vöru fyrir landið/svæðið og færslugerðina. Núna getur April bókað kostnaðarskýrsluna í fjárhag.

Þegar April bókar kostnaðarskýrsluna er stofnaður VSK endurkræfur vinnuliður stofnaður. Vinnuliðnum er úthlutað til meðlims í bakvinnsluteyminu. April fær skilaboð sem staðfestir að bókunin hafi heppnast. Í skilaboðunum kemur einnig fram fjöldi VSK-færslna sem voru auðkenndar til endurheimtu.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Vinna úr kostnaði sem er gjaldgengur fyrir alþjóðlega endurgreiðslu virðisaukaskatts

Arnie, sem er meðlimur í bakvinnsluteymi Contoso, er ábyrgur fyrir því að staðfesta að allar nauðsynlegar upplýsingar um endurgreiðslu virðisaukaskatts séu innifaldar í kostnaðarskýrslum. Hann opnar síðuna **Endurheimt kostnaðarskatts** og velur kostnaðarskýrsluna sem Nancy sendi inn. Arnie staðfestir að allar nauðsynlegar kvittanir séu meðfylgjandi og að réttur VSK-flokkur og VSK-kóði vöru hafi verið færður inn.

Þegar Arnie fær pappírskvittanir frá Nancy staðfestir hann kvittanirnar á móti stafrænu kvittunum og breytir síðan stöðu kostnaðarskýrslunnar í **Tilbúin til endurgreiðslu**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Senda gögn um endurgreiðslu virðisaukaskatts til þriðja aðila lánardrottins til að skrá skil á alþjóðlegri endurgreiðslu

Þegar Arnie er tilbúinn til að senda gögn kostnaðarskýrslunnar til þriðja aðila lánardrottins sem mun skrá skil á endurgreiðslu virðisaukaskatts, opnar hann síðuna **Endurheimt kostnaðarskatts**. Hann síar síðuna svo hún sýni aðeins kostnaðarskýrslurnar sem eru merktar sem **Tilbún til endurgreiðslu**. Arnie velur síðan **Skrá** &gt; **Flytja út í Excel**. VSK upplýsingarnar í kostnaðarskýrslunni eru fluttar út í vinnublað Microsoft Excel. Arnie sendir vinnublaðið til þriðja aðila lánardrottins og lætur fylgja með skilaboð um að pappírskvittanirnar hafi verið sendar með inniheldur skilaboð sem segir að pappírskvittanir hafi verið sendar hraðsendingu.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Vinna úr kostnaði vegna innlendrar endurgreiðslu virðisaukaskatts

Arnie verður að staðfesta að færslur kostnaðarskýrslunnar séu gjaldgengar fyrir endurgreiðslu á virðisaukaskatti og að stafrænu kvittanirnar séu tengdar skýrslunni. Til að byrja að vinna úr gjaldgengum kostnaði vegna innlendrar endurgreiðslu, opnar Arnie síðuna **Endurheimt kostnaðarskatts** og velur kostnaðarskýrsluna sem krefst staðfestingar. Hann staðfestir að kvittanirnar séu á nafni fyrirtækisins í stað starfsmanns. Fyrir endurgreiðslu virðisaukaskatts verða kvittanir að vera á nafni fyrirtækisins. Arnie staðfestir síðan að réttur VSK-flokkur og VSK-kóði vöru hafi verið færður inn.

Þegar Arnie tekur við pappírskvittununum breytir hann stöðu kostnaðarskýrslunnar í **Tilbúin til endurgreiðslu**. Hann getur síðan skráð skilin hjá viðeigandi skattyfirvöldum. Í þessu tilviki er IRS viðeigandi skattyfirvald í Bandaríkjunum.

