---
title: Dreifing á fjárhagsupphæðum
description: Þessi efni veitir upplýsingar um dreifingu á fjárhagsupphæð og lýsir valkostunum sem eru tiltækar fyrir vinnslu á þeim.
author: sunfzam
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f81444e0865715925dad2483e8c789221bccb2b
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595315"
---
# <a name="accounting-distributions"></a>Dreifing á fjárhagsupphæðum

[!include [banner](../includes/banner.md)]

Þessi efni veitir upplýsingar um dreifingu á fjárhagsupphæð og lýsir valkostunum sem eru tiltækar fyrir vinnslu á þeim. Dreifingar á fjárhagsupphæð eru notaðar til að úthluta upphæðum fyrir upprunaskjalið á tiltekinn fjárhagslykil. 

Dreifingar á fjárhagsupphæð eru geta í öllu forritinu sem er notað og framlengt af hverju upprunaskjalið, eins og innkaupapöntun, reiknings lánardrottins, kostnaðarskýrslu og reikningur með frjálsum texta. Að sjálfgefnu er sjálfgefna dreifing á fjárhagsupphæð mynduð fyrir hverja línu upprunaskjals og peningaupphæð og er virk fyrir breytingu ef skilyrði mæla svo fyrir. 

> [!NOTE] 
> Sum skjöl styðja einnig peningaupphæðir skjals fyrir haus, eins og gjalda fyrir pantanir og reikninga. 

Almenn geta dreifingar á fjárhagsupphæð veitir eftirfarandi valkosti fyrir vinnslu dreifingar á fjárhagsupphæð:

-   **Dreifa upphæðum** – Skoða og breyta fjárhagsupphæðum fyrir einstakar skjalahausa eða -línur og allar undirlínur, svo sem skatta eða gjöld.
    -   Fyrir Efstu dreifingu peningaupphæðar (yfirstig dreifingar), gætu aðallykils og fjárhagsvídda verið hægt að breyta beint í sundurliðað innfærslustýringu í hnitanetinu. Útvíkkað verð er gott dæmi um slíkar yfirdreifingar.
    -   Upphæðum dreifingar eru á grundvelli tíimabilsgjaldmiðil skjalsins. Venjulega er þessi gjaldmiðill færslugjaldmiðli . Gjaldmiðilsupphæðir bókhalds og skýrslugerðar eru myndaðar sem hluti af bókhaldi undirbókar.
    -   Dreifing birta bókhaldsdagsetningu og bókhaldstilvik. Yfirleitt, er bókhaldstilvik stillt á **Ekkert** þar til skjal er bókað/skráðar. Á þeim tímapunkti verður bókhaldstilvik **Upprunalegt**. Eftir að dreifingar hafa verið bókaðar geturðu ekki breytt dreifingunum.
    -   **Skipta** hnappur gæti virkjaður fyrir yfirstig dreifingar. **Skipta** býr til nýja dreifing á fjárhagsupphæð og skipta getur byggt á prósentu, upphæð eða magn.
    -   **Dreifa jafnt** er hægt að nota í samsetningu með **Skipta** til að úthluta sjálfkrafa upphæð jafnt á allar dreifingar.
    -   Hnappurinn **Endurstilla** gæti verið virkjaður fyrir yfirstig dreifingar þegar fleiri en ein dreifing er til staðar. **Endurstilla** bakfærir allar handvirkar breytingar í dreifingu með því að eyða öllum fyrirliggjandi dreifingum mynda sjálfgefna dreifingu aftur.
    -   Allar undirskipað dreifingu, eins og afslátt, gjöld og virðisaukaskatt, fylgir alltaf yfirstig dreifingar. Hægt er að skoða vensl yfireiningar/undireiningar á **Tilvísun** &gt; **Upplýsingar yfireiningar**.
    -   Aðallykill og fjárhagsvídd gætu einnig verið breytanlegar fyrir undireiningu.
    -   Fjárhagsvíddir í dreifingu á fjárhagsupphæð fylgja sjálfgefnu mynstri sem skjal getur útvíkkað.
    -   Frávik dreifingar gætu myndast í samsvörunaraðstæðum, eins og jöfnun milli innkaupapöntunar og reiknings lánardrottins. Hægt er að skoða jöfnunartengsl milli dreifingar á fjárhagsupphæð við **Tilvísun** &gt; **Skjalsupplýsingar**.
    -   **Leiðrétta** hnappur birtist og er virk fyrir skjöl sem styðja leiðréttingar. **Leiðrétta** stofnar nýja arðgreiðslu. Fyrst skal stofna dreifingar sem bakfæra upprunalegu dreifingar. Ekki er hægt að breyta þessum dreifingum. Næst, ný leiðréttandi dreifingar á fjárhagsupphæð eru stofnaðar. Hægt er að breyta þessar dreifingar hægt var að breyta upphaflegri dreifingar.
    -   Hnappurinn **Upplýsingar um verk** er virkjaður sem viðauki þegar lína er tengd verki. Fjárhagsupphæð gerir kleift að breyta upplýsingum eins og fjármögnunaraðila og línueiginleika.
    -   Hægt er að skoða gildandi bókhaldsstaða skjals í **Tilvísun**. Staðan er fyrir allt skjalið og gefur til kynna hvort skjalið er í vinnslu eða lokið.
-   **Skoða dreifingar** - Skoða dreifingu á fjárhagsupphæð fyrir allar línur og peningaupphæðir í skjalinu. Ekki er hægt að breyta dreifingu fjárhagsupphæða í þessu yfirliti.

Í útgáfu 10.0.13 hefur eiginleika verið bætt við sem villuleitar töflu yfir dreifingu á fjárhagsupphæð til að ganga úr skugga um að nýju reitirnir séu settir upp á réttan hátt. Þessi eiginleiki kallast **Virkja viðbótarvilluleit í gögnum skjala með því að nota bókhaldsramma upprunaskjals**. Til að nota eiginleikann verður að virkja hann á vinnusvæðinu **Eiginleikastjórnun**. Til að virkja eiginleikann skal leita að heiti eiginleikans í reitnum **Leita** á síðunni **Eiginleikastjórnun** og síðan velja **Virkja núna**.

Nánari upplýsingar má nálgast á [Dreifing á fjárhagsupphæðum og færslur undirbókar fyrir lánardrottnareikninga](accounting-distributions-subledger-journal-entries-vendor-invoices.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
