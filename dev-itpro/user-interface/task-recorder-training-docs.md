---
title: "Stofna fylgiskjölum eða þjálfun með verkskráningu"
description: "Í þessu efnisatriði er útskýrt hvað verkskráning og leiðbeiningar um verkið eru, hvernig á að stofna verkskráningu, og hvernig á að sérsníða verkefni í Microsoft leiðir og hafa þau með í þínu Hjálp."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8b44dc66cdcd1ede59cb9bb4ed05be27dd465599
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Stofna fylgiskjölum eða þjálfun með verkskráningu

[!include[banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvað verkskráning og leiðbeiningar um verkið eru, hvernig á að stofna verkskráningu, og hvernig á að sérsníða verkefni í Microsoft leiðir og hafa þau með í þínu Hjálp.

<a name="learn-about-task-recorder"></a>Læra um verkskráningar
-------------------------

Verkskráning er Microsoft Dynamics 365 for Operations verkfæri sem hægt er að nota til að skrá aðgerðir sem framkvæmdar eru í notendaviðmótinu (UI) vörunnar. Þegar notuð er verkskráning eru öll atvik sótt sem framkvæmt er í Notendaviðmóti og eru keyrðir gagnvart þjóninum — þar á meðal bæta við gildum, breytt stillingum og fjarlægir gögn. Skrefin sem þú skráir kallast í sameiningu við *verkskráning*. Hægt er að nota verkskráningu á marga vegu:

-   **Hægt er að spila verkskráningu sem verkefnaleiðbeiningar.** Leiðbeiningar um verkið eru hluti af Dynamics 365 for Operations hjálparupplifun. Verkefnaleiðbeiningar eru stýrð, leiðbeind, gagnvirk reynsla sem fer með þig í gegnum þrep viðskiptaferlis. Notandi er leiðbeint um að ljúka við hvert skref með sprettigluggum (eða "talblaðra"), sem verður lifandi í Notendaviðmóti og benda á UI einingar sem notandinn ætti að eiga samskipti við. "Talblaðra" veitir einnig upplýsingar um hvernig á að eiga samskipti við einingar, svo sem "Smella skal hér" eða "Í þessu svæði er fært inn gildi." Verkefnaleiðbeiningar keyra gagnvart gildandi gagnasafni notanda og gögnin sem færð er inn eru vistuð í umhverfi notanda.
-   **Verkskráning getur birst sem skref ferlis í hjálparrúðu.** Nota má hjálparrúðuna til að leita að og sýna verkskráningar. Hægt er að opna rúðuna Hjálp með því að smella á **?** táknið í efstu skoðunarrein eða hægt er að nota flýtivísunarlykilsamsetningu, **Ctrl + Shift +?**. Hægt er að lesa þrep verkskráningar í hjálparglugganum eða hægt er að kjósa að spila verkskráningu sem leiðarvísi fyrir verk, svo það leiðir notandann í gegnum Notendaviðmóti.
-   **Hægt er að vista verkskráningu í BPM.** Hægt er að vista verkskráning í línu stigveldis í viðskiptaferlavinnsla (BPM) safnið í Lifecycle Services (LCS). Lista yfir skef og flæðirit viðskiptaferlis verður mynduð úr skráningunni. Hægt er að sýna verkskráningar sem hafa verið vistaðar BPM safn í Dynamics 365 for Operations sem hjálp.
-   **Hægt er að vista verkskráningu í sem Word-skjöl.** Þannig geturðu auðveldlega búið til prentanlegar þjálfunarleiðbeiningar.

Hægt er að stofna eigin verkskráningu, spila verkskráningar sem veittar eru af Microsoft eða breyta verkskráningu sem veitt er af Microsoft til að endurspegla skilgreininguna. Fyrir nánari upplýsingar um Verkskráning sjá [verkskráning í Dynamics 365 for Operations.](task-recorder.md)

## <a name="plan-your-task-recording"></a>Áætlaðu verkskráningu þína
Hvort sem verið er að stofna nýtt verkskráning eða byggja skráningu þína á Microsoft verkskráningu, eftirfarandi upplýsingar skal hafa í huga.

-   Áætla skal skráningu eins og myndskeið. Taktu allar ákvarðanir fram í tímann.
-   Farðu í gegnum viðskiptaferli einu sinni eða tvisvar án þess að skrá til að skilja skrefin..
-   Þegar þú gerð í gegnum ferlið áður en þú skráir, taktu eftir hvar þú nota flýtilykla eða **Enter** lykill, þannig að hægt er að forðast notkun þeirra í raunverulegri skráningu.
-   Auðkenndu eftirfarandi:
    -   Viltu flokka þrep saman í undirverkefni? Undirverkefni setja hluta ferlis sjónrænt í sundur. Til dæmis, ef verið er að stofna skráningu í fyrir "Stofnun og losa afurðar " viltu kannski flokka saman skrefin sem þarf til að stofna afurð og flokka þá saman skrefin sem þarf til að losa vöru. Undirverk gera einnig auðvelda að lesa lengri ferli .
    -   Á að bæta við athugasemdum, og ef svo er, hvar? Sjá "Skilja mismunandi gerðir af athugsemdum" fyrir neðan fyrir frekari upplýsingar.
    -   Hvaða gildi er bætt í mismunandi svæðum þegar þú ljúka skrefum viðskiptaferlis? Það er góð hugmynd að vita hvaða þú velja eða færa inn svo þú þurfir ekki að rekja þig afturábak eða laga mistök á meðan skráning fer fram.

**Rita skal lýsingu og athugasemdir fram í tímann**

-   Við upphaf hvers verkskráning, er lýsingarsvæði sem gerir kleift að færa inn kynning fyrir skráninguna. Góð hugmynd er að skrifa og vista lýsingu fram í tímann í aðskilið skjal svo hægt sé að afrita og líma hana inn á verkskráningu þegar verið er að skrá verkefni. Þannig er hægt nota tíma til að fínstilla texta þegar þú ert ekki í ferlinu við að skrá. Klippa og líma texta auðveldar að gera skráningarferlið hraðara og þægilegra.
-   Fyrir hvert skref í verkskráningu er hægt að stofna athugasemdir. Þegar verkefnaleiðbeiningar eru spilaðar birtast athugasemdir í "talblöðru" sem athugasemd fyrir ofan eða neðan textann fyrir skrefið. Þegar athugasemdir eru skoðaðar sem texti í hjálparrúðunni, birtast þær sem innlína texta í skrefi. Eins og með lýsinguna er gott að skrifa og vista athugasemdir í aðskildu skjali. Þegar verið er að skrá verkskráning, skal klippa og líma athugasemdir úr því skjali.

**Skilja mismunandi gerðir af athugasemdum** Allar athugsemdir eru valfrjáls. Aðeins bæta þeim við ef það eru gagnlegar upplýsingar fyrir notandanum.

-   **Titill**: titilathugsemd birtast á undan skreftextanum sem verkskráning myndar sjálfkrafa. Í Leiðarvísi fyrir verk, birtist titilathugasemd fyrir ofan sjálfkrafa myndaða textann. Notið þessa gerð athugasemdar til að útskýra hvers vegna notandi er að gera skrefið eða til að veita viðbótarsamhengi.

Þetta er breytingarúðunni sem þú sérð hvenær athugasemd er bætt við á meðan þú stofnar skráningu. Færa inn titil athugasemdar í **Titill**. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

Svona lítur athugasemd titils út í talblöðrunni í verkefnaleiðbeiningar. 

[![screen2](./media/screen2.png)](./media/screen2.png)

-   **Titill**: athugasemdarskýring birtist eftir textaþrepið sem verkskráning myndar sjálfkrafa. Í verkefnaleiðbeiningar hún verður aðeins sýnilegur ef notandi smellir á **Sýna fleiri** tengil í talblöðru verkefnaleiðbeininga. Notið þessa gerð skýringar til að lýsa því sem notandi þarf að vita að ljúka við skref.

Þetta er breytingarúðunni sem þú sérð hvenær athugasemd er bætt við á meðan þú stofnar skráningu. Færa inn athugasemdaskýringu í **Athugasemdir:**. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Svona lítur athugasemdarskýring út í talblöðrunni í verkefnaleiðbeiningum.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Upplýsingaskref**: Þessar skýringar eru stofnaðar með því að hægrismella á stýringu eða einhvers staðar í skjámyndinni &lt;**verkskráning**&lt; **Bæta við upplýsingaskrefi. **Upplýsingaskref birtast sem númeruð skref á hvaða tímapunkti sem það er setja inn, jafnvel þótt engin aðgerð var skráð í Notendaviðmóti. Hægt er að bæta upplýsingaskrefi á stigi skjámyndar eða upplýsingar sem eru tengdar stýringu. Þegar upplýsingaskref tengist skjámyndinni, birtist á talblaðra verkefnaleiðbeininga einhversstaðar á skjámynd þegar verkefnaleiðbeiningar eru spilaðar. Þegar upplýsingaskref tengist stýringu, bendir talblaðra verkefnaleiðbeininga á stýringuna á þegar verkefnaleiðbeiningar eru spilaðar. Í hjálparrúðunni birtist skýring upplýsingaskrefs sem númerað skref með hverjum þeim texta sem þú færðir inn. Notaðu upplýsingaskref til að undirbúa notanda fyrir næstu skref, til að lýsa skrefum sem þarf að gera utan Dynamics 365 for Operations eða að vísa til annarra skráninga (þó að ekki sé hægt að búa til tengla í skýringum.).

**Ákvarða hversu lengi á að gera upptökuna**

-   Notandinn verður yfirleitt annað hvort lesa eða spila upptökuna frá upphafi til enda, svo ekki sameina skref eða verkefni sem eru betur gert sérstaklega.
-   Reyndu að taka ekki upp langar aðstæður sem nær yfir marga undirferla. Til dæmis, ef "stjórna þjónustuborði viðskiptavinar í verslun " er of breið skal brjóta það upp í styttri verkefni eins og "Samþykkja skil" og "Bæta við gjafakort."
-   Ef verkefni má framkvæmt sem hluti af nokkrum viðskiptaferli, stofna aðskilin skráning á hana og þú getur vísa í hana í hinni skráningu.
-   Ef ferlið felur í sér mörg verk sem einstaklingurinn framkvæmir líklega öll í einu, er hægt að hafa verk í einni skráningu, t.d. "Setja upp og úthluta virknireglur."
-   Ef það er eitthvað sem einhver gerir einu sinni (ss stillingar) og síðan annað verkefni sem þeir geta gert strax á eftir en getur gert ítrekað, og á eigin spýtur, brjóta þá upp í tvö verkskráning.

**Ákveða hvar í Notendaviðmóti til að hefja skráningu** Síðan sem þú ert á þegar byrjað er að skrá verkskráningu hefur áhrif á hvaða síðu sem verkefnaleiðbeiningar er birt fyrir. Til dæmis, ef óskað er eftir að verkskráning sé skráð í hjálparglugganum þegar notandi smellir á hjálp á síðunni færibreytur fjárhags, verður að hefja skráningu á síðunni færibreytur fjárhags. **Vista skráningar sem .axtr skrár** Þegar þú ert búinn að stofnaðar eða breyttar skráningu verki, færðu nokkrum valkosti fyrir hvernig á að sækja eða vista skráninguna. Hægt er að sækja skrána sem verkskráningarpakka (.axtr) hlaða niður sem hráa skráningarskrá (.xml), hlaða niður sem Word-skjal sem eða vista skrána í LCS safnið. Það er góð hugmynd að vista alltaf verkskráningu sem verkskráningarpakkaskrá(.axtr). Þetta hjálpar til við auðvelda viðhald skrárinnar ef skýringar eða ferlin þarf að breyta síðar. Ef óskað er að sækja skrána sem Word-skjal skaltu einnig vista það sem verkskráningar pakkaskrá.

## <a name="create-your-task-recording"></a>Stofna verkskráningu þína
Fyrir nákvæm leiðbeiningaskref sjá [Hvernig stofna á verkskráningu](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Afrita og sérsníða Microsoft fyrir verkskráningu
Hægt er að sækja og breyta verkskráningu Microsoft og nota þær fyrir eigin fylgigögn hjálpar eða þjálfunarefni. Til að sækja Microsoft verkskráningu, skal fylgja þessum skrefum:

1.  Opna verkskráningu í Dynamics 365 for Operations. Verkskráning er staðsett í **Stillingar** valmynd.
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

## <a name="include-your-task-recordings-in-the-help-pane"></a>Taka verkskráningu með í rúðunni Hjálp
Til að sýna þína eigin sérsniðna verkskráningu í rúðunni hjálp þannig að hægt er að spila þau sem verkefnaleiðbeiningar eða skoða texta , þarf að vista verkskráningu í eigin safn BPM og síðan uppfæra færibreytum hjálparkerfis til að vísa í safn fyrir BPM. Fyrir nánari upplýsingar sjá [Tengja við hjálpargögnin.](../get-started/help-connect.md)

<a name="see-also"></a>Sjá einnig
--------

[Hjálparsíður fyrir Dynamics 365 for Operations](..\get-started\help-overview.md)

[Tengjast hjálp](..\get-started\help-connect.md)

[Opna verkskráningu í Dynamics 365 for Operations](task-recorder.md)

[Nýlega viðbættar aðgerðir verkskráningar](\core\get-started\recently-added-editing-features-in-task-recorder)

[Stofna ný þjálfunarsöfn fyrir Dynamics AX innan Lifecycle Services með Verkskráningu (Ytri tengil)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Stofna Hjálparefni rich Client með Verkskráningar (ytri tengil)](https://mbspartner.microsoft.com/AX/Videos/970)




