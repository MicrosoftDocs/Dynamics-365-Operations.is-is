---
title: Afstemma bankareining
description: Þetta efni lýsir því hvernig hægt er að afstemma bankareikning.
author: panolte
manager: AnnBe
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c77d08d5877ab27f9b6549a5b2a666150938fc08
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444454"
---
# <a name="reconcile-a-bank-account"></a>Afstemma bankareining

[!include[banner](../includes/banner.md)]

Þegar þú færð bankayfirlit, ættir þú reglulega að afstemma bankafærslur lögaðila við færslur á bankayfirliti.

Ekki er hægt að stemma bankayfirlit við bankareikning ef einhver ávísunin eða innborgunarseðillinn á listanum á yfirlitinu eru með stöðuna **Afturköllun í bið**. Þegar skoðunarmaður hefur bókað eða hafnað bakfærslu ávísunar eða afturköllun á greiðslu innborgunarseðils er staðan ekki lengur **Afturköllun í bið** og hægt er að stemma bankareikninginn af.

1.  Farið í **Reiðufjár- og bankastjórnun** \> **Bankareikningar** \> **Bankareikningar**. Veldu bankareikninginn sem á að sætta við bankayfirlitið og veldu **Afstemma** > **Afstemming reikninga**.

2.  Sláðu inn upplýsingar í reitina **Dagsetning bankayfirlits** og **Bankayfirlit**. Í reitinn **Lokastaða** er hægt að slá inn stöðu bankareikningsins eins og hún kemur fram á reikningsyfirliti frá bankanum.

3.  Veldu **Færslur** til að opna **Reikningsafstemming** síðu.

4.  Fyrir hverja færslu sem er á bankayfirlitinu skal velja gátreitinn **Hreinsað** ef upphæðin í Dynamics 365 Finance samsvarar upphæðinni á bankayfirlitinu. Þú getur einnig slegið inn eða breytt gildi í **Tegund bankafærslu**. Þetta reitagildi er mikilvægt vegna talnagagna um bankafærslur og skýrslugerðar.
    

    > [!NOTE]
    > <P>Ekki skal velja gátreitinn <STRONG>Hreinsað</STRONG> fyrir færslum sem eru ekki á bankayfirlitinu. Þessar færslur birtast áfram í þessari síðu þar til þær eru stemmdar af við síðara bankayfirlit.</P>
    > <P>Gátreiturinn <STRONG>Hreinsað</STRONG> er ekki tiltækur ef færslan er með stöðuna <STRONG>Afturköllun í bið</STRONG>. Færslur gætu haft þessa stöðu ef Finance er sett upp til að krefjast þess að bakfærslur eða afturkallanir séu sendar til yfirferðar áður en þær eru bókaðar. Þegar skoðunarmaður hefur bókað eða hafnað bakfærslu ávísunar eða afturköllun á er staðan ekki lengur <STRONG>Afturköllun í bið</STRONG> og hægt er að afstemma bankareikninginn við bankayfirlitið.</P>

    
    Til að velja **Hreinsað** gátreitinn fyrir bil ávísana sem allir birtast á bankayfirliti, veldu **Merkja ávísanabil**, og tilgreindu síðan bilið.

5.  Ef upphæð fyrir bankareikningsviðskipti samsvarar ekki fjárhæðinni fyrir viðskiptin á bankayfirliti skal færa fjárhæð leiðréttingarinnar í reitnum **Leiðréttingarfjárhæð**.
    

    > [!NOTE]
    > <P>Ef fjárhagstímabil færslunnar sem á að leiðrétta er lokað er ekki hægt að nota reitinn <STRONG>Leiðréttingarupphæð</STRONG>. Í staðinn skal stofna línu sem er með færsludagsetningu sem er á opnu fjárhagstímabili fyrir leiðréttinguna. Í þessu tilfelli verður þú að bæta fjárhagsvíddunum sem voru notuð við upphaflegu viðskiptin, og einnig á móti reikningnum á móti.</P>



6.  Stofnið færslur fyrir innfærslur, svo sem þóknanir og vexti sem eru á bankayfirlitinu en ekki skráðar í Finance. Sláðu inn **Tegund bankafærslna** og viðeigandi fjárhagsvíddir.

7.  Eftir því sem færslur á bankayfirlitinu eru merktar sem **Hreinsaðar** nálgast upphæðin í reitnum **Óafstemmt**, sem er endurreiknuð jafnóðum, núll. Þegar hún nær núlli skaltu velja **Afstemma lykil** til að bóka afstemminguna og færslurnar og leiðréttingarnar sem hafa verið gerðar.
    
    Þegar búið er að stemma af er ekki hægt að breyta færslurnar sem voru teknar með eða leiðrétta þær frekar og þær birtast ekki í síðari afstemmingum á reikningum.

8.  Notaðu til að skoða bankaviðskipti sem ekki hafa verið afstemmd **Óafstemmdar bankafærslur** skýrslu. Notaðu til að skoða bankayfirlit bankareiknings **Bankayfirlit** skýrslu.

## <a name="cancel-bank-statement-reconciliation"></a>Hætta við afstemmingu bankayfirlita 

Virknin Hætta við afstemmingu bankayfirlits auðveldar að hætta við afstemmingu bankayfirlit. Til að nota þennan eiginleika, virkjaðu **Hætta við afstemmingu bankayfirlit** í **Stjórnun eiginleika** vinnusvæði. Þú þarft einnig að virkja **Leyfa breytingu á bankayfirliti** breytu. Þetta er gert með því að fara í **Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar > Bankaafstemming**.
 
Aðeins er hægt að hætta við bankayfirlýsingu í tímaröð sem þau voru færð inn. Þegar afstemming bankayfirlits fellur niður verða nýjum viðskiptum og leiðréttingum snúið við og öll önnur viðskipti merkt sem ósamræmd.
 
Til að hætta við afstemmingu bankayfirlit skaltu velja bankayfirlitið og velja **Bankayfirlit > Hætt við bankaafstemmingu**. Á síðunni **Hætta við bankaafstemmingu**, veita **Ástæða kóða**, **Ástæða ummæla**, og **Aflýsingardagur**. Veldu **Í lagi** til að hefja niðurfellingu. Athugið að uppsagnadagur bankayfirlits verður að vera á eða eftir dagsetningu reikningsyfirlýsingarinnar. Eftir að afstemming bankayfirlits var felld niður, verðir reiturinn **Aflýsingardagur** fyrir bankayfirlitið uppfærður með veittum **Aflýsingardegi**. Veldu hnappinn **Færslur** til að skoða færslur sem afstemmingunni var aflýst fyrir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]