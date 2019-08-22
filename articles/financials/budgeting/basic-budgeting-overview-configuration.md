---
title: Yfirlit fjárhagsáætlunar
description: Næstum öll fyrirtæki sem nota virknina Fjármál í Microsoft Dynamics 365 for Finance and Operations munu geta stofnað skýrslur með áætlun á móti raunvirði. Í þessari grein er farið yfir nauðsynlegar lágmarksstillingar til að hægt sé að stofna áætlanir í Finance and Operations eða hlaða þeim úr forriti óháðs aðila.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9871d41c8e0c8f05acfd6618ca537a98ab0dd71b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834272"
---
# <a name="budgeting-overview"></a>Yfirlit fjárhagsáætlunar

[!include [banner](../includes/banner.md)]

Næstum öll fyrirtæki sem nota virknina Fjármál í Microsoft Dynamics 365 for Finance and Operations munu geta stofnað skýrslur með áætlun á móti raunvirði. Í þessari grein er farið yfir nauðsynlegar lágmarksstillingar til að hægt sé að stofna áætlanir í Finance and Operations eða hlaða þeim úr forriti óháðs aðila.

<a name="overview"></a>Yfirlit
--------

Samþykktri fjárhagsáætlun fyrir lögaðila er viðhaldið í skjalinu sem kallast *færsla í fjárhagsáætlunarskrá*. Línur í skjali færslu í fjárhagsáætlunarskrá eru þekktar sem færslur *fjárhagsáætlunarlykils* og innihalda upplýsingar um fjárhagsvídd, dagsetningar og upphæðir samþykktrar fjárhagsáætlunar. Skjal færslu fjárhagsáætlunarskrár er samþætt við grundvallarfjárhagsskýrslur og fyrirspurnarsíður þar sem raunverulegar fjárhagsupphæðir eru bornar saman við upphæðir fjárhagsáætlunar. 

Það eru margar aðferðir til að stofna færslur í fjárhagsáætlunarskrá í Finance and Operations:

-   Færðu handvirkt inn upplýsingar um skjal á síðunni **Færslur fjárhagsáætlunarskrár**.
-   Notaðu sniðmátið Microsoft Excel sem hægt er að opna með því að smella á hnappinn **Opna í Excel** á síðunni **Færslur fjárhagsáætlunarskrár**.
-   Nota skal **færslur fjárhagsáætlunarlykils** gagnaeiningu í gagnastjórnun til að flytja inn færslur fjárhagsáætlunarskrár. Þú ættir að íhuga að nota þennan greiðslumáta og kveikja á **Byggt á safni** **vinnslu** færibreytu þegar þarf að flytja margar fjárhagsáætlunarfærslur inn í kerfið.
-   Ef fyrirtækið notar aðgerðir fjárhagsáætlunargerðar til að útbúa fjárhagsáætlunargögn, er hægt að nota reglubundna vinnslu **Mynda færslu í fjárhagsáætlunarskráar**.

Færslu fjárhagsáætlunarskrár telst lokið þegar stöður fjárhagsáætlunar hafa verið uppfærðar. Á síðunni **Færslur fjárhagsáætlunarskrár** er smellt á **Uppfæra innistæður fjárhagsáætlunar** fyrir valda færslu fjárhagsáætlunarskrár eða margar færslur. Þegar búið er að uppfæra stöður fjárhagsáætlunar, breytist staða færslu fjárhagsáætlunarskrár í **Lokið**. Ekki má enduropna lokna færslu fjárhagsáætlunarskrár fyrir breytingar. Þess vegna, ef leiðrétta þarf fjárhagsáætlunargögnin verður að stofna nýja færslu fjárhagsáætlunarskrár í stað þess að leiðrétta gögnin í lokinni færslu fjárhagsáætlunarskrár.

## <a name="configuration"></a>Stilling
Þegar fjárhagsáætlunargerð er skilgreind, skal byrja á síðunni **Færibreytum fjárhagsáætlunar**. Á þessari síðu verður að skilgreina fjárhagsáætlunarbók, númeraröð fyrir færslur fjárhagsáætlunarskrár og sjálfgefna hegðun í vinnusvæðum.

Næst, ef reglur eru til staðar sem stjórna samþykki á færslum fjárhagsáætlunarskrár, byggt á gerð fjárhagsáætlunar (til dæmis, flutningar eða endurskoðanir), verður að stofna verkflæði fyrir færslur fjárhagsáætlunarskrár á síðunni **Verkflæði fjárhagsáætlunar**. Ef aðstæður eru fyrir hendi þar sem flutningar gætu verið leyfðir án samþykkis verkflæðis, er hægt að skilgreina flutningsreglur fjárhagsáætlunar til að styðja við þessar aðstæður. 

Á síðunni **Fjárhagsáætlunarvídir** verður að velja fjárhagsvíddir sem eru notaðar fyrir fjárhagsáætlun, byggðar á víddum sem notaðar eru í bókhaldslyklinum. Hægt er velja allar fjárhagsvíddir eða undirflokk þeirra fyrir fjárhagsáætlun.

Skilgreina *fjárhagsáætlunarlíkan* sem samsvarar öllum eða sumum fjárhagsáætlunum. Hægt er að nota eitt fjárhagsáætlunarlíkan fyrir allar færslur fjárhagsáætlunarskrár. Einnig er hægt að stofna aðskild líkön sem byggja á gerð fjárhagsáætlunar, landfræðilegri staðsetningu eða einhverjum öðrum hætti sem fjárhagsáætlun kann að vera flokkuð. 

> [!NOTE] 
> Ef fjárhagsáætlunarstýring er notuð er aðeins hægt að tengja eitt fjárhagsáætlunarlíkan við tiltekið tímabil fjárhagsáætlunar. 

Stofna *fjárhagsáætlunarkóða* sem auðkenna gerð fjárhagsáætlunarfærslu til að skrá og öll tengd verkflæði. Fjárhagsáætlunarkóðarnir geta stutt eftirfarandi gerðir fjárhagsáætlunar:

-   Upprunaleg fjárhagsáætlun
-   Flytja
-   Endurskoðun
-   Fjárúthlutun
-   Áætluð fjárúthlutun
-   Fjárhagsáætlun frá fyrra tímabili

Fjárhagsáætlunarkóðarnir veita þér endurskoðunarslóð fyrir samþykktar breytingar á fjárhagsáætlun í gegnum ferli fjárhagsáætlunar. Ef verkflæði tengist fjárhagsáætlunarkóða , verður verkflæðið virkt fyrir allar færslur fjárhagsáætlunarskrár sem nota þá fjárhagsáætlunarkóða, og verkflæðisskref verður að vera lokið áður en færsla fjárhagsáætlunarskrár getur náð stiginu **Lokið**.  

Einnig er hægt að velja að setja upp *flutningsreglur áætlunar*. Til að nota flutningsreglur áætlunar skal velja **Nota reglur fyrir fjárhagsáætlunarfærslur** á síðunni **Færibreytur fjárhagsáætlunar**. Þegar flutningsreglur fjárhagsáætlunar eru notaðar, ef notandi stofnar skjal með því að nota fjárhagsáætlunarkóða af gerðinni **Flutningur** , verða stöður fjárhagsáætlunar ekki uppfærðar ef flutningsreglur áætlunar eru brotnar. Til dæmis er hægt að leyfa skjöl fyrir flutning fjárhagsáætlunar þar sem kostnaður fjárhagsáætlunar er fluttur á milli aðallykla fyrir Sölu- og markaðsdeild, en hægt er að hindra fjárhagsáætlun frá því að vera flutt frá eða í þá deild nema verkflæðissamþykki hafi verið veitt fyrir þá gerð færslu fjárhagsáætlunarlykils.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Nota vinnusvæði og fyrirspurnarsíður til að rekja fjárhagsáætlun samanborið við rauntölur
Fjárhagsáætlunarstjóri getur farið yfir gildandi stöðu í fjárhagsáætlunar í vinnusvæðinu **Fjárhagsáætlanir og spár**. Fliparnir **Kostnaður yfir fjárhagsáætlun** og **Tekjur undir fjárhagsáætlun** veita fljótlegt yfirlit yfir samsetningar fjárhagsvídda þar sem markmið fjárhagsáætlunar nást ekki eða eru að nálgast þröskuld. Hægt er að sérsníða þröskuldsprósenta fjárhagsáætlunar og fjárhagsvíddasamstæður sem notaðir eru á þessum flipa með því að smella **Grunnstilla eigin vinnusvæði**. Hægt er að smella á **Stjórnendur eininga** til að sjá starfsmenn sem bera ábyrgð á tiltekinum samsetningum fjárhagsvíddar sem valdar eru á þessum flipum. Til dæmis, ef þú sérð að kostnaðaráætlun Aðgerðadeildar mun yfir þröskuld fjárhagsáætlunar, er auðveldlega hægt að finna og hafa samband við rekstrarstjóra deildar til að fjalla um vandamálið. 

> [!NOTE] 
> Reiturinn **Deildarstjóri** á síðunni **Fyrirtækiseiningar** ákvarðar hvaða stjórnendur styðja tiltekna samsetningar fjárhagsvíddar. Smellið á **Sjá meira** neðst á flipanum til að opna fyrirspurnarsíðuna **Rauntölur samanb. v. áætlun** fyrir frekari upplýsingar um upphæð fjárhagsáætlunar samanborið við raunverulegar upphæðir. 

Fyrirspurnarsíðan **Raun samanb. v. áætlun** gerir mögulegt að kafa í upplýsingar um fjárhagsáætlun samanborið við raunupphæðir. Veljið línu á fyrirspurnarsíðu og smellið síðan á **Stöður tímabils** til að sjá fjárhagsáætlun og raunupphæðir dreifast yfir fjárhagstímabil. Síðan **Færslur fjárhagsáætlunarlykla** veitir köfun í upplýsingar um upphæð fjárhagsáætlunar í færslum fjárhagsáætlunarlykla. Síðan **Færslur í færslubók** opnar fjárhagsfærslur sem eru hafðar með í útreiknaðri upphæð **Rauntölur** . 

Fyrirtækið sem er að nota virkni fjárhagsáætlunargerðar getur stofnað og notað *fjárhagsáætlunarspár* á vinnusvæðinu **Fjárhagsáætlanir og spár**.



