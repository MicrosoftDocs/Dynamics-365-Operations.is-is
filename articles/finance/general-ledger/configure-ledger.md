---
title: Grunnstilla fjárhag
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að grunnstilla fjárhag fyrir hvern lögaðila. Þar eru upplýsingar um hvernig á að velja gjaldmiðla, fjárhagsdagatöl, bókhaldslykla og skipulag lykla sem á að nota í hverjum lögaðila.
author: kweekley
manager: ''
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: d2d0bebbdde96e6751f749dfbc0d4cdedd4036a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212326"
---
# <a name="configure-ledgers"></a>Grunnstilla fjárhag

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar um hvernig á að grunnstilla fjárhag fyrir hvern lögaðila. Þar eru upplýsingar um hvernig á að velja gjaldmiðla, fjárhagsdagatöl, bókhaldslykla og skipulag lykla sem á að nota í hverjum lögaðila.

## <a name="selecting-the-chart-of-accounts"></a>Val bókhaldslykils

Fyrir hvern lögaðila í Microsoft Dynamics 365 Finance þarf að grunnstilla upplýsingar um fjárhaginn. Síðan **Fjárhagur** gerir þér kleift að velja bókhaldslykilinn og skipulag lykla sem verður notað fyrir valinn lögaðila. Hægt er að deila bókhaldslyklunum og lykilskipulaginu með því að skilgreina síðuna **Fjárhagur** í hverjum lögaðila til að nota sama bókhaldslykil og lykilskipulag. Einnig er hægt að samnýta hluta grunnstillingarinnar í hverjum lögaðila fyrir sig og hafa tilteknar grunnstillingar í hverjum lögaðila.

Ef lögaðilarnir þurfa að vera með mismunandi bókhaldslykla eða lykilskipulag, gæti hnekkingareiginleiki lögaðilans komið að gagni. Með því að nota sama bókhaldslykil og lykilskipulag fyrir marga lögaðila og hafa síðan umsjón með öllum undantekningum í gegnum hnekkingar lögaðila, er hægt að einfalda viðhald með tímanum.

Til að grunnstilla bókhaldslyklana fyrir lögaðila skal fara í **Fjárhagur \> Uppsetning fjárhags \> Fjárhagur**. Á síðunni **Fjárhagur** skal velja **Bókhaldslykill** og síðan í listanum skal velja bókhaldslykilinn sem á að nota. Athugið að ekki er hægt að breyta bókhaldslyklum eftir að gildi er valið og færslur hafa verið bókaðar í lögaðilanum.

Frekari upplýsingar um hvernig á að skipuleggja og grunnstilla bókhaldslykla og aðallykla er að finna í [Áætla bókhaldslykla](plan-chart-of-accounts.md).

## <a name="selecting-account-structures"></a>Lykilskipulag valið

Hægt er að skilgreina hvern lögaðila í Dynamics 365 Finance til að nota eitt eða fleiri lykilskipulag. Hvert lykilskipulag skilgreinir fjárhagsvíddirnar og samsetningar aðallykla og fjárhagsvídda, sem verða heimilaðar þegar færslur eru bókaðar. Hægt er að nota sama lykilskipulagið í fleiri en einum lögaðila.

Hafa skal í huga að ef fleiri en eitt lykilskipulag er til staðar er aðeins hægt að velja lykilskipulag sem ekki er með samsetningar aðallykla og fjárhagsvídda sem skarast. Til dæmis er eitt lykilskipulagið þitt skilgreint til að bæta við viðskiptaeiningu fyrir aðallykla á milli 1000 og 1999. Í öðru lykilskipulagi hefurðu bætt við fjárhagsvídd deildar fyrir aðallykla sem hefjast á 1. Í þessu tilfelli er aðeins hægt að bæta við einu lykilskipulagi í sama lögaðilanum.

Til að skilgreina lykilskipulag fyrir fjárhaginn þinn, á síðunni **Fjárhagur**, í flýtiflipanum **Lykilskipulag**, skal velja **Bæta við**, velja lykilskipulag í listanum og síðan velja **Velja**. Það gæti tekið nokkrar mínútur að bæta lykilskipulagi við og vista það. Athugið að lykilskipulagið sem er valið verður að vera virkt. Að öðrum kosti verða upplýsingar um lykilskipulagið ekki virkjað í lögaðilanum þar sem þær eru tengdar.

Til að fjarlægja lykilskipulag, á síðunni **Fjárhagur**, í flýtiflipanum **Lykilskipulag**, skal velja **Fjarlægja**. Athugið að ef lykilskipulag er fjarlægt úr fjárhagnum er ekki hægt að fjarlægja neinar færslur sem voru bókaðar með því að nota skilgreininguna á þessu lykilskipulagi.

Frekari upplýsingar um hvernig lykilskipulag er sett upp er að finna í [Skilgreina lykilskipulag](configure-account-structures.md).

## <a name="configuring-calendars-for-the-ledger"></a>Skilgreining dagatala fyrir fjárhag

Annar þáttur fjárhagsins er fjárhagsdagatalið. Fjárhagsdagatal verður að vera valið fyrir hvern lögaðila. Hægt er að nota sama fjárhagsdagatalið í fleiri en einum lögaðila. Þegar fjárhagsdagatal er valið fyrir fjárhag er tekið afrit. Vísað er í þetta afrit sem fjárhagsdagatal. Fjárhagsdagatalið gerir kleift að velja stöðu tímabila og einingar á hverju tímabili.

Til að fá aðgang að og uppfæra dagatalið fyrir valinn lögaðila, á síðunni **Fjárhagur**, á aðgerðasvæðinu, skal velja **Fjárhagsdagatal**.

Til að velja dagatalið skal velja **Fjárhagsdagatöl** og velja svo dagatalið í listanum. Ef fjárhagsdagatalinu er breytt eftir að færslur hafa verið bókaðar í lögaðilanum, verður að velja **Endurreikna fjárhagstímabil**. Síðan, í svarglugganum sem birtist, er hægt að uppfæra fjárhagsstöður fyrir tímabilin í dagatalinu. Mælt er með því að keyra ferlið **Endurreikna fjárhagstímabil** í stillingunni **Runa** og að það sé keyrt þegar léttvægari ferli eru í gangi í kerfinu. Þetta ferli getur tekið nokkurn tíma, fer allt eftir fjölda færslna og fjárhagsvíddasamsetninga.

Ef ekkert fjárhagsdagatal er valið fyrir lögaðila birtast villuboð þegar reynt er að bóka færslu í þeim lögaðila.

Fyrir nánari upplýsingar, sjá [Fjárhagsdagatöl, fjárhagsár, og tímabil.](../budgeting/fiscal-calendars-fiscal-years-periods.md)

## <a name="using-a-balancing-financial-dimension"></a>Fjárhagsvídd afstemmingar notuð

Þegar búið er að velja bókhaldslykilinn og eitt lykilskipulag eða fleiri, er hægt að velja eina fjárhagsvídd sem á að nota sem fjárhagsvídd afstemmingar. Víddin sem er valin verður að vera til staðar í öllu lykilskipulagi. Hún verður einnig að vera afstemmd í öllum bókhaldsfærslum. Debet- og kreditfærslur verða sem sagt að vera jafnar fyrir aðallykilinn og fjárhagsvídd afstemmingar. Kerfið stofnar sjálfkrafa færslur til að jafna færslurnar, byggðar á aðallyklum sem eru tilgreindir í reitunum **Interunit - kredit** og **Interunit - debet** á síðunni **Lyklar fyrir sjálfvirka færslu**.

Frekari upplýsingar um mótfærslur er að finna í [Jafnaðar færslubækur fyrir millieiningabókhald](example-balanced-journals-interunit-accounting.md).

## <a name="configuring-currencies-for-the-ledger"></a>Skilgreining gjaldmiðla fyrir fjárhag

Síðan **Fjárhagur** er einnig notuð til að stjórna og skilgreina gjaldmiðlana sem verða notaðir þegar færslur eru bókaðar í fjárhagnum. Tilgreina verður bókhaldsgjaldmiðilinn, sem er sá gjaldmiðill sem er notaður í dálknum **Bókhaldsgjaldmiðill** í fjárhagnum í öllum fylgiskjölum. Að auki er hægt í dálknum **Skýrslugjaldmiðill** að velja annan gjaldmiðil. Ef valinn er skýrslugjaldmiðill verða allar færslur skráðar í þeim gjaldmiðli í dálknum **Skýrslugjaldmiðill** í fjárhagnum í öllum fylgiskjölum.

Ef færslur eru bókaðar í öðrum gjaldmiðli umbreytir kerfið sjálfkrafa færsluupphæðinni úr færslugjaldmiðlinum í bókhaldsgjaldmiðilinn og skýrslugjaldmiðilinn í fylgiskjalinu. Á síðunni **Fjárhagur**, í reitnum **Gerð gengis fyrir bókhaldsgjaldmiðil**, skal velja gerð gengis sem er skilgreint fyrir gengin sem á að nota til að umbreyta gildum úr færslugjaldmiðli í bókhaldsgjaldmiðil í fylgiskjali. Ef skýrslugjaldmiðill var valinn þarf einnig að stilla reitinn **Gerð gengis fyrir skýrslugjaldmiðil** til að gefa upp gengið sem á að nota til að umbreyta gildum úr færslugjaldmiðli í skýrslugjaldmiðil í fylgiskjali.

Ef verið er að nota virkni fjárhagsáætlunargerðar, er einnig hægt að stilla reitinn **Gengisgerð fjárhagsáætlunar** til að gefa til kyna gengið sem á að nota til að umbreyta færslum fjárhagsáætlunar úr einum gjaldmiðli í annan.

Ef notaðir eru tveir gjaldmiðlar eða ef notaður er einn gjaldmiðill, en færslur eru bókaðar í öðrum gjaldmiðli, verður að skilgreina flýtiflipann **Lyklar fyrir endurmat gjaldmiðils** á síðunni **Fjárhagur**. Í þessum flýtiflipa eru tilgreindir sjálfgefinn innleystur og óinnleystur hagnaðar -og rekstrarlyklar sem verða sjálfgefið notaðir þegar færslur eru bókaðar, ef enginn lykill er tilgreindur á síðunni **Lyklar gjaldmiðilsendurmats**. (Síðan **Lyklar gjaldmiðilsendurmats** er notuð til að skilgreina mismunandi lykla fyrir innleystan og óinnleystan hagnað og tap fyrir hvern gjaldmiðil.)

Innleystur hagnaður og tap er framlegð og tap sem verður til úr loknum færslum. Það er skráð í rekstraryfirlitið. Óinnleystur hagnaður og tap er framlegð og tap sem hefur átt sér stað, en færslunni er ekki lokið. Með öðrum orðum er til dæmis búið að bóka reikning, en reikningurinn er ekki enn jafnaður og greiddur. Óinnleystur hagnaður og tap er skráð á efnahagsreikninginn.

Frekari upplýsingar um hvernig á að nota þessa tvo gjaldmiðli er að finna í [Tvöfaldur gjaldmiðill](dual-currency.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]