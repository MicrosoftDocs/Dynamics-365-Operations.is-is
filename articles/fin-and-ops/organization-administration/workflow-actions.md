---
title: "Verkflæðisaðgerðir"
description: "Þessi grein útskýrir aðgerðir sem hver þátttakandi í verkflæðissamþykki getur gripið til."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bbaac72d8adb764c4b186b022100248b1c5a3804
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="workflow-actions"></a>Verkflæðisaðgerðir

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir aðgerðir sem hver þátttakandi í verkflæðissamþykki getur gripið til.

Verkflæði getur innihaldið nokkra hópa fólks: upphafsmann, viðtakanda verks, stjórnendur og samþykktaraðila. Til dæmis í eftirfarandi verkflæði fyrir kostnaðarskýrslur er Samúel upphafsmaður, meðlimir í biðröð eru viðtakendur verks, Jón er stjórnandi og Friðrik, Súsanna og Anna eru samþykkjendur.   

[![Verkflæði\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif) 

Eftirfarandi kaflar útskýra þær verkflæðisaðgerðir sem hver flokkur getur framkvæmt.

## <a name="actions-that-an-originator-can-perform"></a>Aðgerðir sem upphafsmaður getur framkvæmt
Stofnandinn byrjar verkflæðistilvik með því að senda skjal til vinnslu. Til dæmis verður Samúel að smella á hnappinn **Senda** á síðunni **Kostnaðarskýrsla** til að senda kostnaðarskýrsluna sína.

## <a name="actions-that-a-task-assignee-can-perform"></a>Aðgerðir sem verkþegi getur framkvæmt
Hægt er að úthluta verkefni til margra eða á vinnuliðalista sem er vaktaður af nokkrum einstaklingum. Hins vegar getur aðeins ein manneskja lokið verkinu. Til dæmis hefur Samúel sent kostnaðarskýrslu og vísað innhreyfingum sínum á kostnaðarskýrsludeild fyrirtækisins til endurskoðunar. 

Starfsmenn kostnaðarskýrsludeildar Adventure Works fylgjast með biðröðinni. Júlía, starfsmaður í þeirri deild, hefur samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels. Nú getur hún framkvæmt eina af eftirfarandi aðgerðum: ljúka, hafna, úthluta, biðja um breytingu, endurúthluta eða losa. 

**Ábending:** Mismunandi aðgerðir eru til boða eftir því hvernig forritarinn hannaði verkefnið.

### <a name="complete"></a>Ljúka

Þegar notandi lýkur verkefni er skjalinu sem var sent til vinnslu úthlutað til næsta notanda í verkflæðinu, ef næsti notandi er til staðar. Ef ekki er þörf á frekari vinnslu endar verkflæðisferlið. 

Til dæmis hefur Júlía, starfsmaður í kostnaðarskýrsludeild Adventure Works, samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels. Eftir að Júlía lýkur endurskoðuninni er skjalinu úthlutað til Jóns.

### <a name="reject"></a>Hafna

Þegar notandi hafnar skjali endar verkflæðisferlið. 

Til dæmis hefur Júlía, starfsmaður í kostnaðarskýrsludeild Adventure Works, samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels. Þegar Júlía hefur samþykkt kostnaðarskýrsluna lýkur verkflæðiferlinu. 

Samúel getur síðan sent kostnaðarskýrsluna aftur. Hann getur gert breytingar fyrst eða hann getur endursent upprunalega útgáfu. Ef Samúel sendir kostnaðarskýrsluna aftur, hefst verkflæðisferlið á handvirkri endurskoðun.

### <a name="delegate"></a>Fulltrúi

Þegar notandi skipar fulltrúa fyrir verkefni, er verkefninu úthlutað til annars notanda. 

Til dæmis hefur Júlía, starfsmaður í kostnaðarskýrsludeild Adventure Works, samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels. Júlía úthlutar verkinu til Tim sem er aðstoðarmaður hennar. 

Síðan starfar Tim fyrir hönd Júlíu. Þess vegna er kostnaðarskýrslunni úthlutað til Jóns þegar Tim lýkur yfirferð sinni, rétt eins og Júlía hefði lokið verkinu.

### <a name="request-change"></a>Beiðni um breytingu

Þegar notandi biður um breytingu á skjalinu sem var sent, er það sent aftur til stofnandans. 

Til dæmis hefur Júlía, starfsmaður í kostnaðarskýrsludeild Adventure Works, samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels. Júlía tekur eftir villum í kostnaðarskýrslunni og gerir beiðni um breytingar. Kostnaðarskýrslan er send til baka til Samúels. 

Samúel getur sent kostnaðarskýrsluna aftur. Hann getur gert umbeðnar breytingar fyrst eða hann getur endursent upprunalega útgáfu. Ef Samúel endursendir kostnaðarskýrsluna, verður starfsmaður í vinnuliðalistanum að endurskoða innhreyfingarnar aftur.

### <a name="reassign"></a>Endurúthluta

Meðlimir vinnuliðalista geta endurúthlutað skjölum sem eru í þeirri biðröð yfir á aðra biðröð. 

Til dæmis er Júlía, starfsmaður kostnaðarskýrsludeildar Adventure Works, fylgjast með biðröðinni. Til að dreifa vinnuálaginu getur hún endurúthlutað kostnaðarskýrslunni og innhreyfingum sem fylgja með henni í aðra biðröð.

### <a name="release"></a>Losun

Einstaka sinnum gæti meðlimur vinnuliðalista samþykkt verk en síðan ákveðið að hann eða hún geti ekki lokið verkinu. Í þessu tilfelli getur sá aðili sem samþykkti verkið losað skjalið aftur í vinnuliðalistann. 

Til dæmis hefur Júlía, starfsmaður í kostnaðarskýrsludeild Adventure Works, samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels. Ef Júlía ákveður að hún geti ekki lokið verkinu getur hún losað skjalið. Kostnaðarskýrslunni er skilað til baka í biðröðina, svo að aðrir starfsmenn kostnaðarskýrsludeildar Adventure Works geti lokið verkinu.

## <a name="actions-that-a-decision-maker-can-perform"></a>Aðgerðir sem stjórnandi getur framkvæmt
Yfirleitt er skjal tengt stjórnanda, þar sem það er spurning sem stjórnandinn verður að svara spurningu. Svar við spurningunni er yfirleitt **Já** eða **Nei**, eða **Satt** eða **Ósatt**. Ef stjórnandi velur ekki einn af þessum valkostum getur hann eða hún úthlutað ákvörðuninni.

### <a name="choice-1-or-choice-2"></a>\[Choice 1\] eða \[Choice 2\]

Stjórnandi verður að svara spurningu sem tengist skjalinu. Svar við spurningunni er yfirleitt **Já** eða **Nei**, eða **Satt** eða **Ósatt**. Svarið sem stjórnandinn velur ákvarðar þá verkflæðisgrein sem er notuð til að vinna skjalið. 

Til dæmis er kostnaðarskýrslu Samúels úthlutað á Jón. Jón verður að ákveða hvort upplýsingarnar í skjalinu krefjast símtals til yfirmanns Samúels. Ef Jón ákveður að símtal sé nauðsynlegt er kostnaðarskýrslunni úthlutað til Agnesar, sem verður þá að hringja í yfirmann Samúels. Ef Jón ákveður að símtal sé ekki nauðsynlegt er kostnaðarskýrslunni úthlutað til Friðriks til samþykktar.

### <a name="delegate"></a>Fulltrúi

Þegar stjórnandi framselur ákvörðun, er skjalinu úthlutað til annars notanda sem þarf að taka ákvörðunina. 

Til dæmis er kostnaðarskýrslu Samúels úthlutað á Jón. Jón framselur ákvörðuninni til Maríu, sem er aðstoðarmaður hans. 

Síðan starfar María fyrir hönd Jóns. Ef María ákveður að símtal til yfirmanns Samúels sé nauðsynlegt er kostnaðarskýrslunni úthlutað til Agnesar, sem verður þá að hringja í yfirmann Samúels. Ef María ákveður að símtal sé ekki nauðsynlegt er kostnaðarskýrslunni úthlutað til Friðriks til samþykktar.

## <a name="actions-that-an-approver-can-perform"></a>Aðgerðir sem samþykktaraðili getur framkvæmt
Þegar skjali er úthlutað til samþykkjanda getur hann gripið til eftirfarandi aðgerða: Samþykkja, hafna, framselja eða biðja um breytingar.

### <a name="approve"></a>Samþykkja

Þegar samþykkjandi samþykkir skjal er því úthlutað til næsta notanda í verkflæðinu, ef næsti notandi er til staðar. Ef ekki er þörf á frekari vinnslu endar verkflæðisferlið. 

Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $6,000 og þessu skjali hefur verið úthlutað til Friðriks. Þegar Friðrik samþykkir skjalið er því úthlutað til Súsönnu til samþykktar. Þegar Súsanna samþykkir kostnaðarskýrsluna lýkur verkflæðiferlinu.

### <a name="reject"></a>Hafna

Þegar samþykkjandi hafnar skjali endar verkflæðisferlið. 

Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $12,000 og þessu skjali hefur verið úthlutað til Súsönnu. Ef Súsanna hafnar kostnaðarskýrslunni lýkur verkflæðiferlinu. 

Samúel getur sent kostnaðarskýrsluna aftur. Hann getur gert breytingar fyrst eða endursent upprunalega útgáfu af kostnaðarskýrslunni. Ef Samúel sendir kostnaðarskýrsluna aftur, hefst verkflæðisferlið á samþykktarferlinu.

### <a name="delegate"></a>Fulltrúi

Þegar samþykkjandi skipar fulltrúa fyrir skjal, er skjalinu úthlutað til annars notanda til samþykktar. 

Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $12,000 og þessu skjali hefur verið úthlutað til Friðriks. Friðrik úthlutar kostnaðarskýrslunni til Önnu. 

Síðan starfar Anna fyrir hönd Friðriks. Þetta þýðir að þegar Anna samþykkir skjalið þá er því úthlutað til Súsönnu til samþykktar, rétt eins og ef Friðrik hafi samþykkt það. Þegar Súsanna samþykkir skjalið er það sent til Önnu til samþykktar.

### <a name="request-change"></a>Beiðni um breytingu

Þegar samþykkjandi biður um breytingu á skjalinu er það sent aftur til stofnandans. 

Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $12,000 og þessu skjali hefur verið úthlutað til Súsönnu. Ef Súsanna biður um breytingu er kostnaðarskýrslan send til baka til Samúels. 

Samúel getur sent kostnaðarskýrsluna aftur. Hann getur gert umbeðnar breytingar fyrst eða endursent upprunalega útgáfu af kostnaðarskýrslunni. Ef Samúel endursendir kostnaðarskýrsluna þá er hún send til Friðriks til samþykktar, því að Friðrik var fyrsti samþykkjandinn í samþykktarferlinu.




