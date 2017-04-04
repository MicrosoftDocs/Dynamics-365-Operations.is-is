---
title: "Stofna fylgiskjölum eða þjálfun með verkskráningu"
description: "Í þessu efnisatriði er útskýrt hvaða verkskráningu og leiðbeiningar um verkið eru, hvernig á að stofna verkskráningu, og hvernig á að sérsníða verkefni í Microsoft leiðir og hafa þær með í þínu Hjálp."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Stofna fylgiskjölum eða þjálfun með verkskráningu
Í þessu efnisatriði er útskýrt hvaða verkskráningu og leiðbeiningar um verkið eru, hvernig á að stofna verkskráningu, og hvernig á að sérsníða verkefni í Microsoft leiðir og hafa þær með í þínu Hjálp.

<a name="learn-about-task-recorder"></a>Læra um verkskráningar
-------------------------

Verkskráning er Microsoft Dynamics 365 fyrir Aðgerðir verkfæri sem hægt er að nota til að skrá aðgerðir sem framkvæma á afurð notandaviðmót (UI). Þegar notuð er verkskráning eru öll atvik sótt sem framkvæmt er í Notendaviðmóti og eru keyrðir gagnvart þjóninum — þar á meðal bæta við gildum, breytt stillingum og fjarlægir gögn. Skrefin sem þú skráir kallast í sameiningu við *verkskráning*. Hægt er að nota verkskráningu á marga vegu:

-   **Hægt er að spila verkskráningu sem verkefnaleiðbeiningar.** Leiðbeiningar um verkið eru integral gagnabút Dynamics 365 fyrir Aðgerðir sem Hjálpa reynslu. Leiðarvísi fyrir verk er stýrt með leiðsögn, gagnvirk reynslu gegnum skrefin í viðskiptaferli. Notandi er leiðbeint um að ljúka við hvert skref með sprettigluggum (eða "talblaðra"), sem verður lifandi í Notendaviðmóti og benda á UI einingar sem notandinn ætti að eiga samskipti við. "bubble" veitir einnig upplýsingar um hvernig á að eiga samskipti við einingar, svo sem "Smella skal hér" eða "Í þessu svæði er fært inn gildi." Leiðarvísi fyrir verk keyrir gagnvart gildandi gagnasafn notanda og gögnin sem færð er inn er vistuð í umhverfi notanda.
-   **Hægt er að birta verkskráningu sem leiðbeiningar skrefum í Hjálp glugganum.** Nota Hjálp rúðunni til að leita að og sýna verkskráningu. Hægt er að opna rúðuna Hjálp með því að smella á **?** Tákn í efstu skoðunarrein eða hægt er að nota flýtivísun lykill samsetningu, **Ctrl + Shift +?**. Hægt er að lesa þrep í verki skráningu í Hjálp glugganum eða hægt er að kjósa það að spila verkskráningu sem leiðarvísi fyrir verk, svo það leiðir notandann í gegnum Notendaviðmóti.
-   **Hægt er að vista verkskráningu í BPM.** Hægt er að vista verkskráning í línu stigveldis í viðskiptaferlavinnsla (BPM) safnið í Lifecycle Services (LCS). Lista yfir skef og flæðirit viðskiptaferlis verður mynduð úr skráningunni. Hægt er að sýna verkskráningu sem hafa verið vistaðar BPM safn í Dynamics 365 fyrir Aðgerðir sem aðstoða Við.
-   **Hægt er að vista verkskráningu í sem Word-skjöl.** Þannig geturðu auðveldlega búið til prentanlegar þjálfunarleiðbeiningar.

Hægt er að stofna eigin verkskráningu, spila verkskráningu sem veittar eru af Microsoft eða breyta verkskráningu veitt til Microsoft til að endurspegla skilgreininguna. Sjá frekari upplýsingar um verkskráning [verkskráning í Dynamics 365 aðgerða](task-recorder.md).

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
-   Fyrir hvert skref í verkskráningu er hægt að stofna athugasemdir. Þegar verkefnaleiðbeiningar eru spilaðar birtast athugasemdir í "talblöðru" sem athugasemd fyrir ofan eða neðan textann fyrir skrefið. Þegar skoðuð og texta í Hjálp rúðunni, birtast annotations sem flokkaþjónustu texta í skrefi. Eins og með lýsinguna er gott að skrifa og vista athugasemdir í aðskildu skjali. Þegar verið er að skrá verkskráning, skal klippa og líma athugasemdir úr því skjali.

**Skilja mismunandi gerðir af athugasemdum ** Allar athugsemdir eru valfrjáls. Aðeins bæta þeim við ef það eru gagnlegar upplýsingar fyrir notandanum.

-   **Titill**: titill skýring birtast áður en myndar skref textann sem verk verkskráningar sjálfkrafa. Í á leiðarvísi fyrir verk, birtist skýring titil fyrir ofan sjálfkrafa textann. Notið þessa gerð athugasemdar til að útskýra hvers vegna notandi er að gera skrefið eða til að veita viðbótarsamhengi.

Þetta er breytingarúðunni sem þú sérð hvenær athugasemd er bætt við á meðan þú stofnar skráningu. Færa inn titil athugasemdar í **Titill**. 

[![skjár1](./media/screen1.png)](./media/screen1.png) 

Svona lítur athugasemd titils út í talblöðrunni í verkefnaleiðbeiningar. 

[![skjár2](./media/screen2.png)](./media/screen2.png)

-   **Titill**: athugasemdarskýring birtist eftir textaþrepið sem verkskráning myndar sjálfkrafa. Í verkefnaleiðbeiningar hún verður aðeins sýnilegur ef notandi smellir á **Sýna fleiri** tengil í talblöðru verkefnaleiðbeininga. Notið þessa gerð skýringar til að lýsa því sem notandi þarf að vita að ljúka við skref.

Þetta er breytingarúðunni sem þú sérð hvenær athugasemd er bætt við á meðan þú stofnar skráningu. Færa inn athugasemdaskýringu í **Athugasemdir:**. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Þetta er það skýring athugasemdir eitthvað eins og í á "bubble" í leiðarvísi fyrir verk.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Upplýsingar um skref**: Þessar annotations eru stofnaðar með því að hægri smella á stýringu eða einhvers staðar í skjámyndinni &lt;**verkskráningar**&lt; ** bæta Við skrefi upplýsingakóða. ** Upplýsingakóða skref birtast sem númeraða skref á hvaða tímapunkti er að setja inn, jafnvel þótt engin aðgerð var skráð í Notendaviðmóti. Hægt er að bæta upplýsingaskrefi á stigi skjámyndar eða upplýsingar sem eru tengdar stýringu. Þegar upplýsingaskref tengist skjámyndinni, birtist á talblaðra verkefnaleiðbeininga einhversstaðar á skjámynd þegar verkefnaleiðbeiningar eru spilaðar. Þegar upplýsingar um skref tengist eftirlit, sem leiðarvísi fyrir verk "bubble" verður að benda stýringu þegar leiðarvísi fyrir verk er sinnt. Í rúðunni Hjálp inn upplýsingar um skref skýring birtast númeraða skref með hvaða texta er færð inn. Fylgið skrefum upplýsingakóða til að útbúa notanda fyrir næsta skref til að lýsa skref sem þarf að gera utan Dynamics 365 aðgerða eða til að vísa í öðrum skráningar (þó er hægt að stofna hyperinks í annotations.).

**Ákvarða hversu lengi á að gera upptökuna**

-   Notandinn verður yfirleitt annað hvort lesa eða spila upptökuna frá upphafi til enda, svo ekki sameina skref eða verkefni sem eru betur gert sérstaklega.
-   Reyndu að taka ekki upp langar aðstæður sem nær yfir marga undirferla. Til dæmis, ef "stjórna þjónustuborði viðskiptavinar í verslun " er of breið skal brjóta það upp í styttri verkefni eins og "Samþykkja skil" og "Bæta við gjafakort."
-   Ef verkefni má framkvæmt sem hluti af nokkrum viðskiptaferli, stofna aðskilin skráning á hana og þú getur vísa í hana í hinni skráningu.
-   Ef ferlið felur í sér mörg verk sem einstaklingurinn framkvæmir líklega öll í einu, er hægt að hafa verk í einni skráningu, t.d. "Setja upp og úthluta virknireglur."
-   Ef það er eitthvað sem einhver gerir einu sinni (ss stillingar) og síðan annað verkefni sem þeir geta gert strax á eftir en getur gert ítrekað, og á eigin spýtur, brjóta þá upp í tvö verkskráning.

**Ákveða hvar í Notendaviðmóti til að hefja skráningu** síðu sem eru á þegar byrjað er að skrá verkskráningu hefur áhrif á hvaða síðu sem leiðarvísi fyrir verk er birt fyrir. Til dæmis ef óskað er eftir við verkefni skráningu eiga að vera skráðir í Hjálp glugganum þegar notandi smellir á Hjálp á síðunni fjárhags, verður að ræsa við skráningu á síðunni fjárhags. **Vista skráningar sem .axtr skrár** Þegar þú ert búinn að stofnaðar eða breyttar skráningu verki, færðu nokkrum valkosti fyrir hvernig á að sækja eða vista skráninguna. Hægt er að sækja skrána sem verkskráningarpakka (.axtr) hlaða niður sem hráa skráningarskrá (.xml), hlaða niður sem Word-skjal sem eða vista skrána í LCS safnið. Það er góð hugmynd að vista alltaf verkskráningu sem verkskráningarpakkaskrá(.axtr). Þetta hjálpar til við auðvelda viðhald skrárinnar ef skýringar eða ferlin þarf að breyta síðar. Ef óskað er að sækja skrána sem Word-skjal skaltu einnig vista það sem verkskráningar pakkaskrá.

## <a name="create-your-task-recording"></a>Stofna verkskráningu þína
Ítarleg walk-through skrefin, [Hvernig stofna á verkskráningu](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Afrita og sérsníða Microsoft fyrir verkskráningu
Hægt er að sækja og breyta verkskráningu Microsoft á að nota þær fyrir eigin Hjálp fylgigögn eða þjálfun efni. Til að sækja Microsoft verkskráningu, skal fylgja þessum skrefum:

1.  Opna verkskráning í Dynamics 365 fyrir Aðgerðir. Verkskráning er staðsett í **Stillingar** valmynd.
2.  Í rúðunni verkskráning, er smellt á **vinna Með skráningu.**
3.  Undir **hver er skráningin **, smellið á **er í LCS safn**.
4.  Smella á **velja LCS-safn**
5.  Velja altæka safn Microsoft.
6.  Í trénu, skal velja safnhnút viðskiptaferlis sem er verkskráning er tengd við.
7.  Smelltu á **Í lagi**.
8.  Smellt er á **Byrja**.
9.  Á þessum tímapunkti, þrep í gegnum skráningu breytt öll þrep sem fara til að skrá það aftur. **Athugasemd**: Ef aðeins þarf að breyta textanum á skráningu, er hægt að opna skrá í **Breyta annotations á skráningu** stillingu, og þá vista hana.
10. Eftir að skráning hefur sinnt spilast til enda, smellið á **Stöðva** í slá verkskráningar efst á skjánum.
11. Veldu hvernig Á að vista stillingarnar.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Taka við verkskráningu rúðunni Hjálp
Til að sýna eigin sérsniðna verkskráningu rúðunni Hjálp þannig að hægt er að sinnt aftur leiðbeiningar um verkið sem þeir eða skoða texta sem, þarf vista skal verkskráningu eigin safn BPM og síðan uppfæra skal færibreytum Hjálparkerfis vísa í safn fyrir BPM. Nánari upplýsingar, sjá [hjálparkerfinu að Tengjast.](../get-started/help-connect.md)

<a name="see-also"></a>Sjá einnig
--------

[Dynamics 365 aðgerða Hjálp](..\get-started\help-overview.md)

[Tengja Hjálp](..\get-started\help-connect.md)

[Verkskráning í Dynamics 365 fyrir Aðgerðir](task-recorder.md)

[Nýlega bætt við verk aðgerðir verkskráningar](\core\get-started\recently-added-editing-features-in-task-recorder)

[Stofna nýja þjálfun söfn fyrir Dynamics AX innan Lifecycle Services með verkskráningu (Ytri tengil)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Stofna Hjálparefni rich Client með Verkskráningar (ytri tengil)](https://mbspartner.microsoft.com/AX/Videos/970)


