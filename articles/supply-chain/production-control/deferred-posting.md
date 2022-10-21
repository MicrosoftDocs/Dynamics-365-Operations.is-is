---
title: Gera fullunnar vörur efnislega tiltækar áður en bókað er í færslubókum
description: Þegar framleidd vara er tilkynnt sem fullunnin er hún skráð sem tiltæk til frekari efnislegrar vinnslu og ein eða fleiri færslubækur eru bókaðar. Þessi grein lýsir því hvernig á að fresta dagbókarfærslum með því að gera það kleift að vinna úr þeim með runuvinnu í skilaboðaröð.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ee767a5d7c3dca2681861802ae42d7a07217c54d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689341"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Gera fullunnar vörur efnislega tiltækar áður en bókað er í færslubókum

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Þegar starfsmaður tilkynnir framleidda vöru sem fullunna skráir kerfið hana sem tiltæka fyrir frekari efnislega vinnslu (svo sem sendingu eða flutning). Meðan á þessu ferli stendur eru ein eða fleiri færslubækur einnig bókaðar (svo sem skýrslan eins og fullunnin færslubók, tínslulistadagbók og leiðarkortabók). Ef þú vilt gera vörur þínar líkamlega aðgengilegar áður en allar færslur hafa verið unnar, getur þú sett upp kerfið til að fresta færslubókunum. Frestað bókun er síðan stjórnað af runuvinnu sem mun vinna úr bókunum eins og kerfisauðlindir leyfa.

Eftirfarandi mynd sýnir hvernig ferlar til að bóka færslubækur eru kallaðir fram bæði með og án frestaðrar bókunar.

![Ferlið skýrslu eins og lokið með og án frestaðrar færslubókar.](media/deferred-posting-flowchart.png "Ferlið skýrslu eins og lokið með og án frestaðrar færslubókar")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Kveiktu á frestað dagbókarfærslu fyrir kerfið þitt

Áður en þú getur notað frestað dagbókarfærslu verður að vera kveikt á henni í kerfinu þínu. Stjórnendur geta notað [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæði til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Framleiðslustýring*
- **Eiginleikaheiti:** *(Forskoðun) Gerðu fullunnar vörur líkamlega aðgengilegar áður en þær eru bókaðar í færslubækur*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Setja upp færslubókunarvalkosti fyrir skýrslugerð sem lokið

Starfsmenn geta tilkynnt um hluti sem lokið með því að nota einhvern af eftirfarandi viðskiptavinum:

- Vefbiðlari
- Vöruhússtjórnun farsímaforrit
- Framleiðsluviðmót framleiðslugólfs

Vefbiðlarinn notar sömu stillingar fyrir birtingaraðferð og vöruhússtjórnun farsímaforritið. Hins vegar verður að stilla bókunaraðferðina sem framkvæmdarviðmót framleiðslugólfsins notar sérstaklega.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Stilltu dagbókarfærsluvalkosti fyrir vefþjóninn og vöruhússtjórnun farsímaforritið

Í farsímaforritinu tilkynna starfsmenn atriði sem lokið með því að opna valmyndaratriði fyrir farsíma þar sem **Vinnusköpunarferli** gildi er *Tilkynna sem lokið* eða *Tilkynntu sem lokið og settu í burtu*. Í vefbiðlaranum tilkynna starfsmenn hluti sem kláraðir úr **Allar framleiðslupantanir** listasíðu eða **Framleiðslupöntun (upplýsingar)** síðu. Þú getur stillt sjálfgefna aðferð fyrir allt fyrirtækið og getur einnig sett upp vöruhússértækar hnekkingar eftir þörfum.

Notaðu eftirfarandi aðferð til að stilla sjálfgefna bókunaraðferð fyrir allt fyrirtækið til að tilkynna vörur eins og þær eru búnar frá vefbiðlaranum eða vöruhúsastjórnun farsímaforritinu.

1. Fara til **Framleiðslueftirlit \> Uppsetning \> Framleiðslustýringarbreytur**.
1. Á **Tímarit** flipa, í **Tilkynna sem lokið dagbók** kafla, stilltu **Birtingaraðferð** reit í eitt af eftirfarandi gildum:

    - *Strax* – Þegar tilkynnt er um að vara sé lokið, vinnur kerfið að fullu úr öllum tengdum færslubókum áður en það merkir fullunna vöru sem líkamlega tiltækan.
    - *Frestað* – Þegar tilkynnt er um að hlut sé lokið, merkir kerfið fullunna hlutinn sem líkamlega tiltækan og bætir dagbókarfærslunum við skilaboðaröð. Kerfið bíður ekki þar til færslurnar eru fullunnar áður en það merkir fullunna vöru sem líkamlega tiltækan.

Notaðu eftirfarandi aðferð til að stilla vöruhússértækar hnekkingar fyrir sjálfgefna bókunaraðferð sem er stillt á **Framleiðslustýringarbreytur** síðu.

1. Fara til **Vöruhússtjórnun \> Uppsetning \> Sundurliðun birgða \> Vöruhús**.
1. Veldu vöruhúsið sem þú vilt setja upp.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á **Vöruhús** flýtiflipann, í **Framleiðslupantanir** kafla, stilltu **Birtingaraðferð** reit í eitt af eftirfarandi gildum:

    - *Erfa* – Valið vöruhús erfir stillinguna frá **Framleiðslustýringarbreytur** síðu.
    - *Strax* – Þegar tilkynnt er um að vara sé lokið, vinnur kerfið að fullu úr öllum tengdum færslubókum áður en það merkir fullunna vöru sem líkamlega tiltækan.
    - *Frestað* – Þegar tilkynnt er um að hlut sé lokið, merkir kerfið fullunna hlutinn sem líkamlega tiltækan og bætir dagbókarfærslunum við skilaboðaröð. Kerfið bíður ekki þar til færslurnar eru fullunnar áður en það merkir fullunna vöru sem líkamlega tiltækan.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Stilltu færslubókunarvalkosti fyrir framkvæmdarviðmót framleiðslugólfs

Notaðu eftirfarandi aðferð til að stilla bókunaraðferðina sem er notuð þegar vörur eru tilkynntar sem kláraðar frá framkvæmdarviðmóti framleiðslugólfs.

1. Fara til **Framleiðslueftirlit \> Uppsetning \> Framleiðsluframkvæmd \> Framleiðslupöntun vanskil**.
1. Á **Tilkynna sem lokið** flipa, í **Tilkynna sem lokið dagbók** kafla, stilltu **Birtingaraðferð** reit í eitt af eftirfarandi gildum:

    - *Strax* – Þegar tilkynnt er um að vara sé lokið, vinnur kerfið að fullu úr öllum tengdum færslubókum áður en það merkir fullunna vöru sem líkamlega tiltækan.
    - *Frestað* – Þegar tilkynnt er um að hlut sé lokið, merkir kerfið fullunna hlutinn sem líkamlega tiltækan og bætir dagbókarfærslunum við skilaboðaröð. Kerfið bíður ekki þar til færslurnar eru fullunnar áður en það merkir fullunna vöru sem líkamlega tiltækan.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Tímasettu runuvinnslu skilaboðavinnslu til að vinna úr frestuðum færslum

Lotuvinna skilaboðavinnslu ber ábyrgð á að vinna úr færslubókum eftir að þær hafa verið settar í biðröð. Til að tryggja að færslubókarfærslurnar þínar séu unnar verður þú að stilla þetta verk þannig að það keyri með reglulegu millibili. Notaðu eftirfarandi aðferð til að setja upp nauðsynlega runuvinnu.

1. Fara til **Kerfisstjórnun \> Skilaboða örgjörvi \> Skilaboða örgjörvi**.
1. Á **Færibreytur** flýtiflipann, stilltu **Skilaboðaröð** sviði til *Framleiðsla*.
1. Á **Hlaupa í bakgrunni** flýtiflipann, stilltu **Lotuvinnsla** valmöguleika til *Já*. Settu síðan upp endurtekna áætlun og stilltu aðrar stillingar eftir þörfum. Stillingarnar virka alveg eins og þær virka fyrir aðrar gerðir af [bakgrunnsstörf](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Microsoft Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>Fylgstu með framvindu frestaðra pósta

Frestað dagbókarfærslur eru í biðröð sem *skilaboð vinnsluaðila skilaboð* sem bíða þar til þeir eru afgreiddir af *skilaboðavinnsluaðila*. Skilaboðavinnslan ætti að vera sett upp til að keyra sem áætlað runuvinna. Til að skoða frestað færsluskilaboð sem hafa verið eða verða unnin af skilaboðavinnsluaðilanum, farðu á **Framleiðslueftirlit \> Framleiðslupantanir \> Frestað framleiðslupöntunarbókun**.

### <a name="message-grid-columns-and-filters"></a>Dálkar og síur í skilaboðakerfi

Þú getur notað reitina efst á **Frestað framleiðslupöntunarbókun** síðu til að hjálpa þér að finna ákveðin skilaboð sem þú ert að leita að.

Eftirfarandi síur eru í boði:

- **Tegund skilaboða** – Tilgreindu tegund skilaboða sem eru sýnd í hnitanetinu.
- **Staða skilaboða** – Tilgreindu stöðu skilaboðanna sem eru sýnd á hnitanetinu. Eftirfarandi ríki eru til:

    - *Í biðröð* – Skilaboðin eru tilbúin til vinnslu hjá skilaboðaúrvinnslunni.
    - *Meðhöndlað* – Skilaboðin voru unnin af skilaboðaforritinu.
    - *Hætt við* – Ekki tókst að vinna úr skilaboðunum í lokatilrauninni og var síðan afturkallað af notandanum.
    - *Mistókst* – Ekki tókst að vinna úr skilaboðunum í síðustu tilraun. Kerfið mun reyna aftur mistök þrisvar sinnum. Það mun þá gefast upp og skilja eftir skilaboðin í *Mistókst* ríki. Athugaðu að þú getur ekki hætt við eða breytt skilaboðum handvirkt fyrr en eftir síðustu af þessum þremur tilraunum.

- **Efni skilaboða** – Þessi sía leitar að texta í öllu efni skilaboða. (Skilaboðainnihald er ekki sýnt í ristinni.) Sían meðhöndlar flest sértákn (eins og bandstrik) sem bilstafi og hún meðhöndlar alla bilstáka sem Boolean OR rekstraraðila. Til dæmis, ef þú leitar að tilteknu`journalid` gildi sem jafngildir *USMF-123456*, mun kerfið finna öll skilaboð sem innihalda annað hvort "USMF" eða "123456." Í þessu tilfelli er listinn yfir niðurstöður líklega langur. Þess vegna er betra að slá bara inn *123456*, vegna þess að þú munt fá nákvæmari niðurstöður.

Þú getur líka flokkað og síað listann með því að velja einhverja dálkafyrirsagnir og slá inn skilyrði í fellivalmyndinni.

### <a name="view-the-message-log-message-content-and-details"></a>Skoða skilaboðaannál, innihald skilaboða og upplýsingar

Þú getur fundið nákvæmar upplýsingar um skeyti með því að velja þau í hnitanetinu og velja síðan **Log** eða **Hrá efni** flipann undir skeytanetinu, þar sem hver vinnsluatburður er sýndur.

Á tækjastikunni á flipanum **Kladdi** eru eftirfarandi hnappar:

- **Log** – Veldu þennan hnapp til að sýna vinnsluniðurstöðurnar. Þessi hnappur er sérstaklega gagnlegur þegar skilaboð hafa a **Niðurstaða í vinnslu** verðmæti á *Mistókst*, og þú vilt læra ástæðurnar fyrir vinnslubiluninni.
- **Búnt** – Hægt er að keyra margar skilaboðaaðgerðir sem hluta af sömu runuvinnslu. Velja þennan hnapp til að skoða þessi ítarlegu gögn. Til dæmis geturðu séð hvort ósjálfstæðir eru til staðar sem krefjast sérstakrar vinnsluröð fyrir sum skilaboð.

### <a name="manually-process-or-cancel-a-message"></a>Vinna handvirkt úr eða hætta við skilaboð

Þú getur unnið handvirkt eða hætt við skilaboð eftir þörfum, allt eftir núverandi ástandi þeirra. Veldu skilaboðin í hnitanetinu og veldu síðan **Ferli** eða **Hætta við** á aðgerðasvæðinu.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Setja upp viðskiptatilvik til að senda viðvaranir vegna misheppnaðra úrvinnsluniðurstaðna

Þú getur sett upp [viðskiptaviðburðir](../../fin-ops-core/dev-itpro/business-events/home-page.md) sem gera þér viðvart um misheppnaðar vinnsluniðurstöður. Fara til **Kerfisstjórnun \> Uppsetning \> Viðskiptaviðburðir \> Viðskiptaviðburðaskrá**, og virkjaðu viðskiptaviðburðinn sem er nefndur *Skilaboð vinnsluaðila unnin*.

Sem hluti af virkjunarferlinu ertu beðinn um að tilgreina hvort viðburðurinn sé sérstakur fyrir einn lögaðila eða eigi við um alla lögaðila. Þú ert líka beðinn um að gefa upp **Heiti endapunkts** gildi. Þetta gildi verður að vera skilgreint fyrst.

> [!NOTE]
> Ef **Þegar viðskiptaviðburður á sér stað** reiturinn er stilltur á *Microsoft Power Automate* (í staðinn fyrir *HTTPS* td), the **Heiti endapunkts** verðmæti skapast sjálfkrafa í Supply Chain Management, byggt á *Microsoft Power Automate* uppsetningu.
