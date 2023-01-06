---
title: Yfirlit fjárhagsáætlunar
description: Næstum öll fyrirtæki sem nota virknina Fjármál í Microsoft Dynamics 365 Finance munu geta stofnað skýrslur með áætlun á móti raunvirði. Þessi grein útskýrir lágmarksskilgreiningu sem er krafist til að stofna áætlanir í fjármálum- og rekstri eða hlaða þeim inn úr forriti óháðs aðila.
author: panolte
ms.date: 04/29/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60113"
- intro-internal
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 380afc399a050215bb2d7b1e5ddb20088226f654
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068961"
---
# <a name="budgeting-overview"></a>Yfirlit fjárhagsáætlunar 

[!include [banner](../includes/banner.md)]

Næstum öll fyrirtæki sem nota virknina Fjármál í Microsoft Dynamics 365 Finance munu geta stofnað skýrslur með áætlun á móti raunvirði. Þessi grein útskýrir lágmarksskilgreiningu sem er krafist til að stofna áætlanir í fjármálum- og rekstri eða hlaða þeim inn úr forriti óháðs aðila.

## <a name="overview"></a>Yfirlit

Samþykktri fjárhagsáætlun fyrir lögaðila er viðhaldið í skjalinu sem kallast *færsla í fjárhagsáætlunarskrá*. Línur í skjali færslu í fjárhagsáætlunarskrá eru þekktar sem færslur *fjárhagsáætlunarlykils* og innihalda upplýsingar um fjárhagsvídd, dagsetningar og upphæðir samþykktrar fjárhagsáætlunar. Skjal færslu fjárhagsáætlunarskrár er samþætt við grundvallarfjárhagsskýrslur og fyrirspurnarsíður þar sem raunverulegar fjárhagsupphæðir eru bornar saman við upphæðir fjárhagsáætlunar. 

Það eru margir aðferðir til að stofna færslur fjárhagsáætlunarskráar:

-   Færðu handvirkt inn upplýsingar um skjal á síðunni **Færslur fjárhagsáætlunarskrár**.
-   Notaðu sniðmátið Microsoft Excel sem hægt er að opna með því að smella á hnappinn **Opna í Excel** á síðunni **Færslur fjárhagsáætlunarskrár**.
-   Nota skal **færslur fjárhagsáætlunarlykils** gagnaeiningu í gagnastjórnun til að flytja inn færslur fjárhagsáætlunarskrár. Ætti að íhuga að nota þennan greiðslumáta og kveikja á **Byggt á safni vinnslu** færibreytu þegar þarf að flytja margar fjárhagsáætlunarfærslur inn í kerfið.
-   Ef fyrirtækið notar aðgerðir fjárhagsáætlunargerðar til að útbúa fjárhagsáætlunargögn, er hægt að nota reglubundna vinnslu **Mynda færslu í fjárhagsáætlunarskráar**.

Færslu fjárhagsáætlunarskrár telst lokið þegar stöður fjárhagsáætlunar hafa verið uppfærðar. Á síðunni **Færslur fjárhagsáætlunarskrár** er smellt á **Uppfæra innistæður fjárhagsáætlunar** fyrir valda færslu fjárhagsáætlunarskrár eða margar færslur. Þegar búið er að uppfæra stöður fjárhagsáætlunar, breytist staða færslu fjárhagsáætlunarskrár í **Lokið**. Ekki má enduropna lokna færslu fjárhagsáætlunarskrár fyrir breytingar. Þess vegna, ef leiðrétta þarf fjárhagsáætlunargögnin verður að stofna nýja færslu fjárhagsáætlunarskrár í stað þess að leiðrétta gögnin í lokinni færslu fjárhagsáætlunarskrár.

## <a name="configuration"></a>Stilling
Þegar fjárhagsáætlunargerð er skilgreind, skal byrja á síðunni **Færibreytum fjárhagsáætlunar**. Á þessari síðu verður að skilgreina fjárhagsáætlunarbók, númeraröð fyrir færslur fjárhagsáætlunarskrár og sjálfgefna hegðun í vinnusvæðum.

Næst, ef reglur eru til staðar sem stjórna samþykki á færslum fjárhagsáætlunarskrár, byggt á gerð fjárhagsáætlunar (til dæmis, flutningar eða endurskoðanir), verður að stofna verkflæði fyrir færslur fjárhagsáætlunarskrár á síðunni **Verkflæði fjárhagsáætlunar**. Ef aðstæður eru fyrir hendi þar sem flutningar gætu verið leyfðir án samþykkis verkflæðis, er hægt að skilgreina flutningsreglur fjárhagsáætlunar til að styðja við þessar aðstæður. 

Á síðunni **Fjárhagsáætlunarvídir** verður að velja fjárhagsvíddir sem eru notaðar fyrir fjárhagsáætlun, byggðar á víddum sem notaðar eru í bókhaldslyklinum. Hægt er velja allar fjárhagsvíddir eða undirflokk þeirra fyrir fjárhagsáætlun.

Skilgreina *fjárhagsáætlunarlíkan* sem samsvarar öllum eða sumar fjárhagsáætlunum. Hægt er að nota eitt fjárhagsáætlunarlíkan fyrir allar færslur fjárhagsáætlunarskrár. Einnig er hægt að stofna aðskild líkön sem byggja á gerð fjárhagsáætlunar, landfræðilegri staðsetningu eða einhverjum öðrum hætti sem fjárhagsáætlun kann að vera flokkuð. 

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

Virkni sem kynnt var í Microsoft Dynamics 365 Finance útgáfu 10.0.7 (janúar 2020) bætti við getu og sveigjanleika fyrir færslur í fjárhagsáætlunarskrá. Til að virkja þessar viðbætur skaltu fara á vinnusvæðið **Stjórnun eiginleika** og velja **Færslur í fjárhagsáætlunarskrá fyrir eingöngu magn** og/eða **Færslur í fjárhagsáætlunarskrá sem eru í vanskilum af upphæðargerð**.

Eina aðgerð **Færslur í fjárhagsskrá fyrir magn** gerir þér kleift að birta færslu í fjárhagsáætlunarskrá með upphæðum sem eingöngu eru magn. Til dæmis gætirðu bókað fjárhagsáætlunarfærslu með magninu 32 og verðinu núll, sem skilar sér í upphæðinni núll. Síðan geturðu notað þetta magn í tengslum við fjárhagsskýrslu til að ákvarða verð á magni. Athugaðu að engar fyrirspurnir eða skýrslur voru uppfærðar sem hluti af þessum eiginleika; aðgerðin gerir þér aðeins kleift að bóka upphæðina núll.

Eiginleikinn **Færslur í fjárhagsáætlunarskrá sem eru í vanskilum af fjárhæðargerð** gerir kleift að sjálfgefna upphæðargerðin í færslu í fjárhagsáætlunarskrá sé önnur upphæðargerð en kostnaður. Færslulínan í fjárhagsáætlunarskránni verður núna sjálfkrafa kostnaður þegar aðallykilgerðin er kostnaður; hún verður sjálfkrafa tekjur þegar aðallykilgerðin er tekjur; og hún verður sjálfkrafa kostnaður fyrir allar aðrar lyklagerðir.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Nota vinnusvæði og fyrirspurnarsíður til að rekja fjárhagsáætlun samanborið við rauntölur
Fjárhagsáætlunarstjóri getur farið yfir gildandi stöðu í fjárhagsáætlunar í vinnusvæðinu **Fjárhagsáætlanir og spár**. Fliparnir **Kostnaður yfir fjárhagsáætlun** og **Tekjur undir fjárhagsáætlun** veita fljótlegt yfirlit yfir samsetningar fjárhagsvídda þar sem markmið fjárhagsáætlunar nást ekki eða eru að nálgast þröskuld. Hægt er að sérsníða þröskuldsprósenta fjárhagsáætlunar og fjárhagsvíddasamstæður sem notaðir eru á þessum flipa með því að smella **Grunnstilla eigin vinnusvæði**. Hægt er að smella á **Stjórnendur eininga** til að sjá starfsmenn sem bera ábyrgð á tiltekinum samsetningum fjárhagsvíddar sem valdar eru á þessum flipum. Til dæmis, ef þú sérð að kostnaðaráætlun Aðgerðadeildar mun yfir þröskuld fjárhagsáætlunar, er auðveldlega hægt að finna og hafa samband við rekstrarstjóra deildar til að fjalla um vandamálið. 

> [!NOTE] 
> Reiturinn **Deildarstjóri** á síðunni **Fyrirtækiseiningar** ákvarðar hvaða stjórnendur styðja tiltekna samsetningar fjárhagsvíddar. Smellið á **Sjá meira** neðst á flipanum til að opna fyrirspurnarsíðuna **Rauntölur samanb. v. áætlun** fyrir frekari upplýsingar um upphæð fjárhagsáætlunar samanborið við raunverulegar upphæðir. 

Fyrirspurnarsíðan **Raun samanb. v. áætlun** gerir mögulegt að kafa í upplýsingar um fjárhagsáætlun samanborið við raunupphæðir. Veljið línu á fyrirspurnarsíðu og smellið síðan á **Stöður tímabils** til að sjá fjárhagsáætlun og raunupphæðir dreifast yfir fjárhagstímabil. Síðan **Færslur fjárhagsáætlunarlykla** veitir köfun í upplýsingar um upphæð fjárhagsáætlunar í færslum fjárhagsáætlunarlykla. Síðan **Færslur í færslubók** opnar fjárhagsfærslur sem eru hafðar með í útreiknaðri upphæð **Rauntölur** . 

Fyrirtækið sem er að nota virkni fjárhagsáætlunargerðar getur stofnað og notað *fjárhagsáætlunarspár* á vinnusvæðinu **Fjárhagsáætlanir og spár**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

