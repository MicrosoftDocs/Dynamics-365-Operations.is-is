---
title: "Dreifing á fjárhagsupphæðum"
description: "Þessi grein veitir upplýsingar um dreifingu á fjárhagsupphæð og lýsir valkostunum sem eru tiltækar fyrir vinnslu á þeim. Dreifingar á fjárhagsupphæð eru notaðar til að úthluta upphæðum fyrir upprunaskjalið á tiltekinn fjárhagslykil."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 52cb689723584c862d85fa51a643b42096372a29
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="accounting-distributions"></a>Dreifing á fjárhagsupphæðum

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um dreifingu á fjárhagsupphæð og lýsir valkostunum sem eru tiltækar fyrir vinnslu á þeim. Dreifingar á fjárhagsupphæð eru notaðar til að úthluta upphæðum fyrir upprunaskjalið á tiltekinn fjárhagslykil. 

Dreifingar á fjárhagsupphæð eru geta í öllu forritinu sem er notað og framlengt af hverju upprunaskjalið, eins og  innkaupapöntun, reiknings lánardrottins, kostnaðarskýrslu og reikningur með frjálsum texta. Að sjálfgefnu er sjálfgefna dreifing á fjárhagsupphæð mynduð fyrir hverja línu upprunaskjals og peningaupphæð og er virk fyrir breytingu ef skilyrði mæla svo fyrir. 

> [!Note] 
> Sum skjöl styðja einnig peningaupphæðir skjals fyrir haus, eins og gjalda fyrir pantanir og reikninga. 

Almenn getu dreifingar á fjárhagsupphæð veita eftirfarandi valkostum fyrir dreifingu vinnslu dreifingar á fjárhagsupphæð  :

-   **Dreifa fjárhæðir** - Skoða og breyta þeim dreifing á fjárhagsupphæð fyrir einstakar hausa skjals eða línur og allar  undirlínur, svo sem skatta eða gjöld.
    -   Fyrir Efstu dreifingu peningaupphæðar (yfirstig dreifingar), gætu aðallykils og fjárhagsvídda verið hægt að breyta beint í sundurliðað innfærslustýringu í hnitanetinu. Útvíkkað verð er gott dæmi um slíkar yfirdreifingar.
    -   Upphæðum dreifingar eru á grundvelli tíimabilsgjaldmiðil skjalsins. Venjulega er þessi gjaldmiðill færslugjaldmiðli . gjaldmiðilsupphæðir Bókhalds og skýrslugerðar  eru myndaðar sem hluti af bókhald undirbókar.
    -   Dreifing birta bókhaldsdagsetningu og bókhaldstilvik. Yfirleitt, er bókhaldstilvik stillt á **Ekkert** þar til skjal er bókað/skráðar. Á þeim tímapunkti verður bókhaldstilvik **Upprunalegt**. Eftir að dreifingar hafa verið bókaðar geturðu ekki breytt dreifingunum.
    -   **Skipta** hnappur gæti virkjaður fyrir yfirstig dreifingar. **Skipta** býr til nýja dreifing á fjárhagsupphæð og skipta getur byggt á prósentu, upphæð eða magn.
    -   **Dreifa jafnt** er hægt að nota í samsetningu með **Skipta** til að úthluta sjálfkrafa upphæð jafnt á allar dreifingar.
    -   **Endurstilla** hnappur gæti verið virkjaður fyrir yfirstig dreifingar þegar fleiri en einn dreifingar eru til. **Endurstilla** bakfærir allar handvirkar breytingar í dreifingu með því að eyða öllum fyrirliggjandi dreifingum mynda sjálfgefna dreifingu aftur.
    -   Allar undirskipað dreifingu, eins og afslátt, gjöld og virðisaukaskatt, fylgir alltaf yfirstig dreifingar. Hægt er að skoða vensl yfireiningar/undireiningar á **Tilvísun** &gt; **Upplýsingar yfireiningar**.
    -   Aðallykils og fjárhagsvídda gæti verið hægt að breyta fyrir undireiningar líka.
    -   Fjárhagsvíddir í dreifingu á fjárhagsupphæð fylgja sjálfgefnu mynstur sem skjal getur  útvíkkað. Frekari upplýsingar um ferlið fást í tengdum greinum.
    -   Frávik dreifingar gætu myndast í samsvörunaraðstæðum, eins og jöfnun milli innkaupapöntunar og reiknings lánardrottins. Hægt er að skoða jöfnunartengsl milli dreifingar á fjárhagsupphæð við **Tilvísun** &gt; **Skjalsupplýsingar**.
    -   **Leiðrétta** hnappur birtist og er virk fyrir skjöl sem styðja leiðréttingar. **Leiðrétta** stofnar nýja arðgreiðslu. Fyrst skal stofna dreifingar sem bakfæra upprunalegu dreifingar. Ekki er hægt að breyta þessum dreifingum. Næst, ný leiðréttandi dreifingar á fjárhagsupphæð eru stofnaðar. Hægt er að breyta þessar dreifingar hægt var að breyta upphaflegri dreifingar.
    -   **upplýsingar um verk** hnappurinn er virkjaður sem viðauki þegar lína er tengd  verki. Fjárhagsupphæð gerir kleift að breyta upplýsingum eins og fjármögnunaraðila og línueiginleika.
    -   Hægt er að skoða gildandi bókhaldsstaða skjals í **Tilvísun**. Staðan er fyrir allt skjalið og gefur til kynna hvort skjalið er í vinnslu eða lokið.
-   ** Skoða dreifingar** - Skoða dreifingu á fjárhagsupphæð fyrir allar línur og peningaupphæðir á skjali. Ekki er hægt að breyta dreifingu fjárhagsupphæða í þessu yfirliti.


Nánari upplýsingar má nálgast á [Um bókhaldsfærslur dreifingar og undirbókar færslubók fyrir reikningur með frjálsum texta](accounting-distributions-subledger-journal-entries-vendor-invoices.md).



