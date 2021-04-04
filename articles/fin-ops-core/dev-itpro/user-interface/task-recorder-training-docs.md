---
title: Búa til fylgiskjöl eða þjálfun með verkskráningu
description: Í þessu efnisatriði er útskýrt hvað verkskráning og leiðbeiningar um verkið eru, hvernig á að stofna skráningar, og hvernig á að sérsníða verkefni í Microsoft leiðir og hafa þau með í þínu Hjálp.
author: josaw1
manager: AnnBe
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b0a31b709c964bbb896079f2db5aeee3c1f22f2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563131"
---
# <a name="create-documentation-or-training-with-task-recorder"></a>Búa til fylgiskjöl eða þjálfun með verkskráningu

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvað verkskráning og leiðbeiningar um verkið eru, hvernig á að stofna verkskráningu, og hvernig á að sérsníða verkefni í Microsoft leiðir og hafa þau með í þínu Hjálp.

> [!IMPORTANT]
> Þú getur tekið upp þínar eigin verkefnaleiðbeiningar fyrir Dynamics 365 Human Resources en þú munt ekki geta vistað þær í BPM-bókasafni (Business Process Modeler) eða opnað þau úr hjálparsvæðinu á þessum tíma. Þú getur vistað þær á staðnum eða á staðarnetinu, og þá opna og endurspila þær með því að nota Verkskráningu. 

<a name="learn-about-task-recorder"></a>Læra um verkskráningar
-------------------------

Verkskráning er verkfæri sem hægt er að nota til að skrá aðgerðir sem framkvæmdar eru í notendaviðmótinu (UI). Þegar notuð er verkskráning eru öll atvik sótt sem framkvæmt er í Notendaviðmóti og eru keyrðir gagnvart þjóninum — þar á meðal bæta við gildum, breytt stillingum og fjarlægir gögn. Skrefin sem þú skráir kallast í sameiningu við *verkskráning*. Hægt er að nota verkskráningu á marga vegu:

-   **Hægt er að spila verkskráningu sem verkefnaleiðbeiningar.** Verkefni leiðbeiningunum eru integral stykki hinnar Hjálp reynslu. Verkefnaleiðbeiningar eru stýrð, leiðbeind, gagnvirk reynsla sem fer með þig í gegnum þrep viðskiptaferlis. Notandi er leiðbeint um að ljúka við hvert skref með sprettigluggum (eða "talblaðra"), sem verður lifandi í Notendaviðmóti og benda á UI einingar sem notandinn ætti að eiga samskipti við. „Talblaðra“ veitir einnig upplýsingar um hvernig á að eiga samskipti við einingar, svo sem „Smella skal hér“ eða „Í þessu svæði er fært inn gildi“. Verkefnaleiðbeiningar keyra gagnvart gildandi gagnasafni notanda og gögnin sem færð er inn eru vistuð í umhverfi notanda.
-   **Hægt er að vista verkskráningu í sem Word-skjöl.** Þannig geturðu auðveldlega búið til prentanlegar þjálfunarleiðbeiningar.

Hægt er að stofna eigin verkskráningu, spila verkskráningar sem veittar eru af Microsoft eða breyta verkskráningu sem veitt er af Microsoft til að endurspegla skilgreininguna. Nánari upplýsingar um verkskráningu er að finna í [Verkskráning](task-recorder.md).

## <a name="plan-your-task-recording"></a>Áætlaðu verkskráningu þína
Hvort sem verið er að stofna nýtt verkskráning eða byggja skráningu þína á Microsoft verkskráningu, eftirfarandi upplýsingar skal hafa í huga.

-   Áætla skal skráningu eins og myndskeið. Taktu allar ákvarðanir fram í tímann.
-   Farðu í gegnum viðskiptaferli einu sinni eða tvisvar án þess að skrá til að skilja skrefin..
-   Þegar þú gerð í gegnum ferlið áður en þú skráir, taktu eftir hvar þú nota flýtilykla eða **Enter** lykill, þannig að hægt er að forðast notkun þeirra í raunverulegri skráningu.
-   Auðkenndu eftirfarandi:
    -   Viltu flokka þrep saman í undirverkefni? Undirverkefni setja hluta ferlis sjónrænt í sundur. Til dæmis, ef verið er að stofna skráningu í fyrir „Stofnun og losun afurðar“ viltu kannski flokka saman skrefin sem þarf til að stofna afurð og flokka þá saman skrefin sem þarf til að losa vöru. Undirverk gera einnig auðvelda að lesa lengri ferli .
    -   Á að bæta við athugasemdum, og ef svo er, hvar? Sjá "Skilja mismunandi gerðir af athugsemdum" fyrir neðan fyrir frekari upplýsingar.
    -   Hvaða gildi er bætt í mismunandi svæðum þegar þú ljúka skrefum viðskiptaferlis? Það er góð hugmynd að vita hvaða þú velja eða færa inn svo þú þurfir ekki að rekja þig afturábak eða laga mistök á meðan skráning fer fram.

**Rita skal lýsingu og athugasemdir fram í tímann**

-   Við upphaf hvers verkskráning, er lýsingarsvæði sem gerir kleift að færa inn kynning fyrir skráninguna. Góð hugmynd er að skrifa og vista lýsingu fram í tímann í aðskilið skjal svo hægt sé að afrita og líma hana inn á verkskráningu þegar verið er að skrá verkefni. Þannig er hægt nota tíma til að fínstilla texta þegar þú ert ekki í ferlinu við að skrá. Klippa og líma texta auðveldar að gera skráningarferlið hraðara og þægilegra.
-   Fyrir hvert skref í verkskráningu er hægt að stofna athugasemdir. Þegar verkefnaleiðbeiningar eru spilaðar birtast athugasemdir í "talblöðru" sem athugasemd fyrir ofan eða neðan textann fyrir skrefið. Þegar athugasemdir eru skoðaðar sem texti í hjálparrúðunni, birtast þær sem innlína texta í skrefi. Eins og með lýsinguna er gott að skrifa og vista athugasemdir í aðskildu skjali. Þegar verið er að skrá verkskráning, skal klippa og líma athugasemdir úr því skjali.

**Skilja mismunandi gerðir af athugasemdum** Allar athugsemdir eru valfrjáls. Aðeins bæta þeim við ef það eru gagnlegar upplýsingar fyrir notandanum.

-   **Titill**: titilathugsemd birtast á undan skreftextanum sem verkskráning myndar sjálfkrafa. Í Leiðarvísi fyrir verk, birtist titilathugasemd fyrir ofan sjálfkrafa myndaða textann. Notið þessa gerð athugasemdar til að útskýra hvers vegna notandi er að gera skrefið eða til að veita viðbótarsamhengi.

Þetta er breytingarúðunni sem þú sérð hvenær athugasemd er bætt við á meðan þú stofnar skráningu. Færa inn titil athugasemdar í **Titill**. 

[![Breyti glugganum með athugasemdartilkynningu](./media/screen1.png)](./media/screen1.png) 

Svona lítur athugasemd titils út í talblöðrunni í verkefnaleiðbeiningar. 

[![Útlit titilsritunar í verkefnahandbók](./media/screen2.png)](./media/screen2.png)

-   **Titill**: athugasemdarskýring birtist eftir textaþrepið sem verkskráning myndar sjálfkrafa. Í verkefnaleiðbeiningar hún verður aðeins sýnilegur ef notandi smellir á **Sýna fleiri** tengil í talblöðru verkefnaleiðbeininga. Notið þessa gerð skýringar til að lýsa því sem notandi þarf að vita að ljúka við skref.

Þetta er breytingarúðunni sem þú sérð hvenær athugasemd er bætt við á meðan þú stofnar skráningu. Færa inn athugasemdaskýringu í **Athugasemdir:**. 

[![Að breyta rúðunni með athugasemd í athugasemdareitnum](./media/screen3.png)](./media/screen3.png) 

Svona lítur athugasemdarskýring út í talblöðrunni í verkefnaleiðbeiningum.

[![Útlit athugasemdaritunar í verkefnahandbók](./media/screen4.png)](./media/screen4.png)

-   **Upplýsingaskref**: Þessar skýringar eru stofnaðar með því að hægrismella á stýringu eða einhvers staðar í skjámyndinni &lt; **Verkskráning** &lt; **Bæta við upplýsingaskrefi.** Upplýsingaskref birtast sem númeruð skref á hvaða tímapunkti sem það er setja inn, jafnvel þótt engin aðgerð var skráð í notendaviðmóti. Hægt er að bæta upplýsingaskrefi á stigi skjámyndar eða upplýsingar sem eru tengdar stýringu. Þegar upplýsingaskref tengist skjámyndinni, birtist á talblaðra verkefnaleiðbeininga einhversstaðar á skjámynd þegar verkefnaleiðbeiningar eru spilaðar. Þegar upplýsingaskref tengist stýringu, bendir talblaðra verkefnaleiðbeininga á stýringuna á þegar verkefnaleiðbeiningar eru spilaðar. Í hjálparrúðunni birtist skýring upplýsingaskrefs sem númerað skref með hverjum þeim texta sem þú færðir inn. Notaðu upplýsingaskref til að undirbúa notanda fyrir næstu skref, til að lýsa skrefum sem þarf að gera utan við forritið eða til að vísa til annarra skráninga (þó að ekki sé hægt að búa til tengla í skýringum.).

**Ákvarða hversu lengi á að gera upptökuna**

-   Notandinn verður yfirleitt annað hvort lesa eða spila upptökuna frá upphafi til enda, svo ekki sameina skref eða verkefni sem eru betur gert sérstaklega.
-   Reyndu að taka ekki upp langar aðstæður sem nær yfir marga undirferla. Til dæmis, ef „stjórna þjónustuborði viðskiptavinar í verslun“ er of breið skal brjóta það upp í styttri verkefni eins og „Samþykkja skil“ og „Bæta við gjafakort“.
-   Ef verkefni má framkvæmt sem hluti af nokkrum viðskiptaferli, stofna aðskilin skráning á hana og þú getur vísa í hana í hinni skráningu.
-   Ef ferlið felur í sér mörg verk sem einstaklingurinn framkvæmir líklega öll í einu, er hægt að hafa verk í einni skráningu, t.d. "Setja upp og úthluta virknireglur."
-   Ef það er eitthvað sem einhver gerir einu sinni (ss stillingar) og síðan annað verkefni sem þeir geta gert strax á eftir en getur gert ítrekað, og á eigin spýtur, brjóta þá upp í tvö verkskráning.

**Ákveða hvar í Notendaviðmóti til að hefja skráningu** Síðan sem þú ert á þegar byrjað er að skrá verkskráningu hefur áhrif á hvaða síðu sem verkefnaleiðbeiningar er birt fyrir. Til dæmis, ef óskað er eftir að verkskráning sé skráð í hjálparglugganum þegar notandi smellir á hjálp á síðunni færibreytur fjárhags, verður að hefja skráningu á síðunni færibreytur fjárhags. **Vista skráningar sem .axtr skrár** Þegar þú ert búinn að stofnaðar eða breyttar skráningu verki, færðu nokkrum valkosti fyrir hvernig á að sækja eða vista skráninguna. Hægt er að sækja skrána sem verkskráningarpakka (.axtr) hlaða niður sem hráa skráningarskrá (.xml), hlaða niður sem Word-skjal sem eða vista skrána í LCS safnið. Það er góð hugmynd að vista alltaf verkskráningu sem verkskráningarpakkaskrá(.axtr). Þetta hjálpar til við auðvelda viðhald skrárinnar ef skýringar eða ferlin þarf að breyta síðar. Ef óskað er að sækja skrána sem Word-skjal skaltu einnig vista það sem verkskráningar pakkaskrá.

## <a name="create-your-task-recording"></a>Stofna verkskráningu þína
Nánari upplýsingar um ítarleg skref er að finna á [Tilföng verkskráningar](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Afrita og sérsníða Microsoft fyrir verkskráningu
Hægt er að sækja og breyta verkskráningu Microsoft og nota þær fyrir eigin fylgigögn hjálpar eða þjálfunarefni. Til að sækja Microsoft verkskráningu, skal fylgja þessum skrefum:

1.  Opna verkskráningu. Verkskráning er staðsett í **Stillingar** valmynd.
2.  Í rúðunni verkskráning, er smellt á **vinna Með skráningu.**
3.  Undir **hver er skráningin**, smellið á **er í LCS safn**.
4.  Smella á **velja LCS-safn**
5.  Veldu Microsoft alþjóðlegt safn.
6.  Í trénu, skal velja safnhnút viðskiptaferlis sem er verkskráning er tengd við.
7.  Smelltu á **Í lagi**.
8.  Smellt er á **Byrja**.
9.  Á þessum tímapunkti, gakktu í gegnum skráningu, og breyta hverju þrep um leið og þú endurskráir þau. **Ábending**: Ef aðeins þarf að breyta texta skráningar er hægt að opna skráningu í stillingunum **Breyta skýringum á skráningu** vista hana síðan.
10. Eftir að skráning hefur sinnt spilast til enda, smellið á **Stöðva** í slá verkskráningar efst á skjánum.
11. Veldu hvernig Á að vista stillingarnar.



<a name="additional-resources"></a>Frekari upplýsingar
--------

[Hjálparkerfi](../../fin-ops/get-started/help-overview.md)

[Tengja hjálparkerfið](../../fin-ops/get-started/help-connect.md)

[Verkskráning](task-recorder.md)

[Stofna Hjálparefni rich Client með Verkskráningar (ytri tengil)](https://mbspartner.microsoft.com/AX/Videos/970)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]