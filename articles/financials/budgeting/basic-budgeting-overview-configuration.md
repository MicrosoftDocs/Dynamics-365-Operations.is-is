---
title: "Yfirlit fjárhagsáætlunar"
description: "Næstum hvert einasta fyrirtæki sem notar virknina Financials í Microsoft Dynamics 365 for Finance and Operations verður að geta stofnað skýrslur um fjárhagsáætlun samanborið við raunvirði. Í þessari grein er farið yfir nauðsynlegar lágmarksstillingar til að hægt sé að stofna áætlanir í Finance and Operations eða hlaða þeim úr forriti óháðs aðila."
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 1d768ee6d2244a237972f7183f27a60b93eea819
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="budgeting-overview"></a>Yfirlit fjárhagsáætlunar 

[!include[banner](../includes/banner.md)]


Næstum hvert einasta fyrirtæki sem notar virknina Financials í Microsoft Dynamics 365 for Finance and Operations verður að geta stofnað skýrslur um fjárhagsáætlun samanborið við raunvirði. Í þessari grein er farið yfir nauðsynlegar lágmarksstillingar til að hægt sé að stofna áætlanir í Finance and Operations eða hlaða þeim úr forriti óháðs aðila.

<a name="overview"></a>Yfirlit
--------

Samþykkt fjárhagsáætlun fyrir lögaðila er viðhaldið í skjalinu sem kallast á *færsla í fjárhagsáætlunarskrá*. Línur í skjali færslu í fjárhagsáætlunarskrá eru þekkt sem færsla *fjárhagsáætlunarlykils* , og innihalda upplýsingar um fjárhagsvídd, dagsetningar og upphæðir samþykktrar fjárhagsáætlunar. Skjal færslu fjárhagsáætlunarskrár er samþætt við grundvallar fjárhagsskýrslur og síður fyrirspurnarsíður þar sem raunverulegur fjárhagsupphæðir eru borin saman við upphæð fjárhagsáætlunar. 

Það eru margar aðferðir til að stofna færslur í fjárhagsáætlunarskrá í Finance and Operations:

-   Færa handvirkt inn upplýsingar um skjal á **færslur fjárhagsáætlunarskrár** síðu.
-   Nota Microsoft Excel sniðmát sem hægt er að opna með því að smella á **Opna í Excel** hnappinn á **færslur fjárhagsáætlunarskrár** síðunni.
-   Nota skal **færslur fjárhagsáætlunarlykils** gagnaeiningu í gagnastjórnun til að flytja inn færslur fjárhagsáætlunarskrár. Ætti að íhuga að nota þennan greiðslumáta og kveikja á **Byggt á safni** **vinnslu** færibreytu þegar þarf að flytja margar fjárhagsáætlunarfærslur inn í kerfið.
-   Ef fyrirtækið notar aðgerðir fjárhagsáætlunargerðar til að útbúa fjárhagsáætlunargögn, er hægt að nota í **Mynda færslu í fjárhagsáætlunarskráa** reglubundna vinnslu.

Færsla fjárhagsáætlunarskrár telst lokið þegar stöður fjárhagsáætlunar hafa verið uppfærðar. Á **færslur fjárhagsáætlunarskrár** síðunni er smellt á **Uppfæra staða fjárhagsáætlunar** fyrir valda færslu fjárhagsáætlunarskrár eða margar færslur. Þegar búið er að uppfæra stöður fjárhagsáætlunar, breytist staða færslu fjárhagsáætlunarskrár í **Lokið**. Lokin færsla fjárhagsáætlunarskrár má ekki vera enduropnaður fyrir breytingar. Þess vegna ef fjárhagsáætlunargögn þarf að leiðrétta, verður að stofna nýja færslu fjárhagsáætlunarskrár í stað þess að leiðrétta gögnin í lokinni færslu fjárhagsáætlunarskrár.

## <a name="configuration"></a>Stilling
Þegar fjárhagsáætlunargerð er skilgreind, skal byrja á **færibreytum Fjárhagsáætlunar** síðu. Á þessari síðu verður að skilgreina fjárhagsáætlunarbók, númeraröð fyrir færslur fjárhagsáætlunarskrár og sjálfgefinni hegðun í vinnusvæðum.

Næst, ef eru reglur sem stjórna samþykki á færslum fjárhagsáætlunarskrár , byggt á gerð fjárhagsáætlunar (til dæmis, flutningum eða endurskoðanir), verður að stofna verkflæði fyrir færslur fjárhagsáætlunarskrár í **verkflæði fyrir Fjárhagsáætlun** síðu. Ef aðstæður eru fyrir hendi þar sem flutningum gætu verið leyfð án samþykkis verkflæðis, er hægt að skilgreina flutningsreglur fjárhagsáætlunar til að styðja við þessar aðstæður. 

Á **Fjárhagsáætlunarvídir** síðu, verður að velja fjárhagsvíddir sem eru notaðar fyrir fjárhagsáætlun, byggðar á víddum sem notaðar eru í bókhaldslyklinum. Hægt er að allar fjárhagsvíddunum eða undirflokk þeirra fyrir fjárhagsáætlun.

Skilgreina *fjárhagsáætlunarlíkan* sem samsvarar öllum eða sumar fjárhagsáætlunum. Hægt er að nota eitt fjárhagsáætlunarlíkan fyrir allar færslur fjárhagsáætlunarskrár. Einnig er hægt að stofna aðskildar líkön sem byggja á gerð fjárhagsáætlunar, landfræðileg staðsetning eða einhvern annan hátt sem er hægt að flokka fjárhagsáætlun. 

> [!NOTE] 
> Ef fjárhagsáætlunarstýring er notuð, er hægt að tengja aðeins eitt fjárhagsáætlunarlíkan við tiltekna tímabil fjárhagsáætlunar. 

Stofna *fjárhagsáætlunarkóða* sem auðkenna gerð fjárhagsáætlunarfærslu til að skrá og allar tengdar verkflæði. Fjárhagsáætlunarkóðarnir getur stutt eftirfarandi gerðir fjárhagsáætlunar:

-   Upprunaleg fjárhagsáætlun
-   Flytja
-   Endurskoðun
-   Fjárúthlutun
-   Áætluð fjárúthlutun
-   Fjárhagsáætlun frá fyrra tímabili

Fjárhagsáætlunarkóðarnir veita þér endurskoðunarslóð fyrir samþykktar breytingar á fjárhagsáætlun í gegnum ferli fjárhagsáætlunar. Ef verkflæði tengist fjárhagsáætlunarkóða , verður verkflæðið virkt fyrir allar færslur fjárhagsáætlunarskrár sem nota þá fjárhagsáætlunarkóða, og verkflæðisskref verður að vera lokið áður færsla fjárhagsáætlunarskrár getur ná **Lokið** stig.  

Einnig er hægt að velja að setja upp *flutningsreglur áætlunar*. Til að Nota flutningsreglur áætlunar, velja **Nota reglur fyrir fjárhagsáætlunarfærslur** á **færibreytur Fjárhagsáætlunar** síðu. Þegar flutningsreglur fjárhagsáætlunar eru notaðir, ef notandi stofnar skjal með því að nota fjárhagsáætlunarkóða af gerðinni **Flutningur** , verða stöður fjárhagsáætlunar ekki uppfærðar ef flutningsreglur áætlunar er brotin. Til dæmis er hægt að leyfa skjöl fyrir flutning fjárhagsáætlunar þar sem kostnaður fjárhagsáætlunar er fluttur á milli aðallykla fyrir Sölu og Markaðssetningar deild, en hægt er að hindra fjárhagsáætlun frá því að vera flutt frá eða í þeirri deild nema verkflæðissamþykki hefur verið veittur fyrir þá gerð færslu fjárhagsáætlunarlykils.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>nota vinnusvæði og fyrirspurnarsíður til að rekja fjárhagsáætlun samanborið við rauntölur
Fjárhagsáætlunarstjóri getur farið yfir gildandi stöðu í fjárhagsáætlunar í **fjárhagsáætlanir og spár** vinnusvæði. Í **Kostnaður yfir fjárhagsáætlun** og **Tekjur undir fjárhagsáætlun** flipum veita fljótlegt yfirlit yfir samsetningar fjárhagsvídda þar sem markmið fjárhagsáætlunar nást ekki eða eru að nálgast þröskuld. Hægt er að sérsníða þröskuldsprósenta fjárhagsáætlunar og fjárhagsvíddasamstæður sem notaðir eru á þessum flipa með því að smella **Grunnstilla eigin vinnusvæði**. Hægt er að smella á **stjórnendur Eininga** til að sjá starfsmönnum sem bera ábyrgð tiltekinni samsetningum fjárhagsvíddar sem valdar eru á þessum flipa. Til dæmis, ef þú sérð að kostnaðaráætlun Aðgerðadeildar mun yfir þröskuld fjárhagsáætlunar, er auðveldlega hægt að finna og hafa samband við rekstrarstjóra deildar til að fjalla um vandamálið. 

> [!NOTE] 
> **Deildarstjóri** reitur á **Fyrirtækiseiningar** síðu ákvarðar hvaða stjórnendur styðja tiltekna samsetning fjárhagsvíddar. Smellið á **Sjá meira** neðst á flipanum til að opna í **rauntölur samanb. v. Áætlun** fyrirspurnarsíðu fyrir frekari upplýsingar um upphæð fjárhagsáætlunar samanborið við raunverulega upphæðir. 

**Raun samanb. v. áætlun** fyrirspurnarsíðu gerir það mögulegt að kafa í upplýsingar um fjárhagsáætlun borinn saman við raunupphæðir. Veljið línu á fyrirspurnarsíðu og smellið síðan á **stöður Tímabils** til að sjá fjárhagsáætlun og raunupphæðir dreifast yfir fjárhagstímabil. Í **færslur fjárhagsáætlunarskrár** síða gefur köfun í upplýsingar um upphæð fjárhagsáætlunar í færslu fjárhagsáætlunarskrár. **færslur í Almennri færslubók** síðu opnar fjárhagsfærslur sem eru hafðar með í útreiknaða upphæð **Rauntölur** . 

Fyrirtækið sem er að nota virkni Fjárhagsáætlunargerðar getur stofnað og nota *fjárhagsáætlunarspár*í á **fjárhagsáætlanir og spár** vinnusvæði.




