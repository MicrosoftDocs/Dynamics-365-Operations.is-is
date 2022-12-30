---
title: Gera fullunnar vörur efnislega tiltækar áður en bókað er í færslubókum
description: Þegar framleidd vara er skráð sem tilbúin er hún skráð sem laus til frekari efnislegrar vinnslu og ein eða fleiri færslbækur eru bókaðar. Þessi grein lýsir því hvernig á að fresta færslum í færslubókum með því að gera þeim kleift að vinna úr þeim með runuvinnslu í skilaboðabiðröð.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689341"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Gera fullunnar vörur efnislega tiltækar áður en bókað er í færslubókum

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Þegar starfskraftur tilkynnir vöru sem fullunnin skráir kerfið vöruna sem tiltæka fyrir frekari efnislega afgreiðslu (t.d. sendingu eða frágang). Meðan á þessu ferli stendur eru einnig bókaðar ein eða fleiri færslubækur (færslubók fyrir tilbúið, færslubók tiltektarlista og færslubók leiðarspjalda). Ef þú vilt gera hlutina efnislega tiltæka áður en unnið hefur verið úr öllum bókunum getur þú sett upp kerfið til að fresta bókunum í færslubók. Frestuðum bókunum er síðan stjórnað af runuvinnslu sem mun vinna úr bókununum eftir því sem tilföng kerfisins leyfa.

Eftirfarandi skýringarmynd sýnir hvernig ferli til að bóka í færslubækur eru kölluð fram bæði með og án frestaðrar bókunar.

![Ferli skráð sem lokið og án frestunar á færslu í færslubók.](media/deferred-posting-flowchart.png "Ferli skráð sem lokið og án frestunar á færslu í færslubók")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Kveiktu á frestuðum færslum í færslubók fyrir kerfið þitt

Áður en hægt er að nota eiginleikann frestun á færslu í færslubók þarf að kveikja á honum í kerfinu. Stjórnendur geta notað vinnusvæðið [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Framleiðslustýring*
- **Heiti eiginleika:** *(Forskoðun) Gera fullunnar vörur efnislega tiltækar áður en bókað er í færslubókum*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Setja upp valkosti færslu í færslubók til að tilkynna um lok skýrslugerðar

Starfskraftar geta tilkynnt vörur sem klára með því að nota einhverja af eftirfarandi biðlurum:

- Vefbiðlari
- Farsímaforrit Warehouse Management
- Viðmót framkvæmdar á framleiðslugólfi

Vefbiðlari notar sömu stillingar fyrir bókunaraðferð og farsímaforrit vöruhúsakerfis. Hins vegar verður að stilla sérstaklega þá bókunaraðferð sem viðmót fyrir framkvæmd á framleiðslugólfi notar.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Veldu valkosti færslu í færslubók fyrir vefbiðlara og farsímaforrit vöruhúsakerfis

Í farsímaforritinu tilkynna starfskraftar vörur sem kláruð með því að opna valmyndaratriði fyrir fartæki þar sem gildi **Ferli verkstofnunar** er *Tilkynna sem lokið* eða *Tilkynna sem lokið og ganga frá*. Í vefbiðlaranum tilkynna starfskraftar vörur sem tilbúna frá síðunni **Allar framleiðslupantanir** eða síðunni **Framleiðslupöntun (upplýsingar)**. Hægt er að stilla sjálfgefna aðferð fyrir allt fyrirtækið og einnig er hægt að setja upp sértækar hnekkingar fyrir vöruhús eins og þú krefst.

Notið eftirfarandi ferli til að stilla sjálfgefna bókunaraðferð fyrir allt fyrirtækið til að tilkynna vörur sem klára úr vefbiðlaranum eða farsímaforriti vöruhúsakerfis.

1. Farið í **Framleiðslustýring \> Uppsetning \> Færibreytur framleiðslustýringar**.
1. Á flipanum **Færslubækur** í hlutanum **Færslubók fyrir tilbúið** skal stilla reitinn **Bókunaraðferð** á eitt af eftirfarandi gildum:

    - *Strax* – Þegar vara er tilkynntur sem kláraður vinnur kerfið að fullu úr öllum tengdum færslum í færslubók áður en það merkir lokið vöru sem efnislega tiltækt.
    - *Frestað* – Þegar vara er skráð sem lokið merkir kerfið lokið vöru sem efnislega tiltæka og bætir færslum í færslubók við biðröð skilaboða. Kerfið bíður ekki þar til búið er að fullvinna bókanir áður en það merkir lokið vöru sem efnislega tiltækt.

Notið eftirfarandi ferli til að stilla vöruhúsasértækar hnekkingar fyrir sjálfgefna bókunaraðferð sem er stillt á síðunni **Færibreytur framleiðslustýringar**.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Sundurliðun birgða \> Vöruhús**.
1. Velja vöruhúsið sem á að setja upp.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á flýtiflipanum **Vöruhús** í hlutanum **Framleiðslupantanir**, skal stilla reitinn **Bókunaraðferð** eitt af eftirfarandi gildum:

    - *Afritun* – Valda vöruhúsið afritar stillinguna af síðunni **Færibreytur framleiðslustýringar**.
    - *Strax* – Þegar vara er tilkynntur sem kláraður vinnur kerfið að fullu úr öllum tengdum færslum í færslubók áður en það merkir lokið vöru sem efnislega tiltækt.
    - *Frestað* – Þegar vara er skráð sem lokið merkir kerfið lokið vöru sem efnislega tiltæka og bætir færslum í færslubók við biðröð skilaboða. Kerfið bíður ekki þar til búið er að fullvinna bókanir áður en það merkir lokið vöru sem efnislega tiltækt.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Stilla valkosti færslu í færslubók fyrir viðmót fyrir keyrsluviðmót framleiðslugólfs

Notaðu eftirfarandi ferli til að stilla bókunaraðferðina sem er notuð þegar vörur eru tilkynntir semviðmót fyrir framkvæmd á framleiðslugólfi notar.

1. Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Sjálfgildi framleiðslupöntunar**.
1. Á flipanum **Bóka sem tilbúið** í hlutanum **Færslubók fyrir tilbúið** skal stilla reitinn **Bókunaraðferð** á eitt af eftirfarandi gildum:

    - *Strax* – Þegar vara er tilkynntur sem kláraður vinnur kerfið að fullu úr öllum tengdum færslum í færslubók áður en það merkir lokið vöru sem efnislega tiltækt.
    - *Frestað* – Þegar vara er skráð sem lokið merkir kerfið lokið vöru sem efnislega tiltæka og bætir færslum í færslubók við biðröð skilaboða. Kerfið bíður ekki þar til búið er að fullvinna bókanir áður en það merkir lokið vöru sem efnislega tiltækt.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Áætla runuvinnslu úrvinnsluaðila skilaboða til að vinna úr frestuðum færslum

Lotuvinnsla úrvinnsluaðila skilaboða ber ábyrgð á úrvinnslu færslna í færslubók eftir að þær hafa verið settar í biðröð. Til að tryggja að unnið sé úr færslum í færslubók verður að stilla verkið þannig að það keyri með reglulegu millibili. Notaðu eftirfarandi ferli til að setja upp áskilda runuvinnslu.

1. Opnið **Kerfisstjórnun \> Skilaboðaúrvinnsla \> Skilaboðaúrvinnsla**.
1. Í flýtiflipanum **Færibreytur**, stillið reitinn **Skilaboðabiðröð** á *Framleiðsla*.
1. Á flýtiflipanum **Keyra í bakgrunni** skal stilla valkostinn **Runuvinnsla** á *Já*. Síðan setur þú upp endurtekna áætlun og stillir aðrar stillingar eins og á þarf að halda. Stillingarnar virka rétt eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Microsoft Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>Rekja framvindu frestaðra færslna

Frestaðar dagbókarfærslur eru í biðröð sem *skilaboð um skilaboðaúrvinnslu* sem bíða þar til þau eru unnin af *úrvinnsluaðila skilaboða*. Úrvinnsluaðili skilaboða ætti að setja upp til að keyra sem runuvinnslu. Til að skoða frestuð skilaboð sem hafa verið eða verða unnin af úrvinnsluaðila skilaboða skaltu fara í **Framleiðslustýring \> Framleiðslupöntun \> Bókun frestaðrar framleiðslupöntunar**.

### <a name="message-grid-columns-and-filters"></a>Dálkar og síur í skilaboðakerfi

Hægt er að nota reitina efst á síðunni **Bókun frestaðrar framleiðslupöntunar** til að auðvelda að finna ákveðin skilaboð sem leitað er að.

Eftirfarandi síur eru í boði:

- **Tegund skilaboða** – Tilgreindu tegund skilaboða sem eru sýnd í hnitanetinu.
- **Staða skilaboða** – Tilgreina stöðu skilaboða sem eru sýnd á hnitanetinu. Eftirfarandi stöður eru til:

    - *Í biðröð* – Skilaboðin eru tilbúin til vinnslu hjá skilaboðaúrvinnslunni.
    - *Meðhöndlað* – Skilaboðin voru unnin af skilaboðaforritinu.
    - *Hætt við* – Ekki tókst að vinna úr skilaboðum meðan á lokatilrauninni stóð og notandinn hætti síðan við.
    - *Mistókst* – Ekki tókst að vinna úr skilaboðunum í síðustu tilraun. Kerfið mun þrisvar sinnum reyna aftur að senda misheppnuð skilaboð. Síðan stöðvast það og skilaboð um stöðuna *Mistókst*. Athugaðu að þú getur ekki hætt við eða breytt skilaboðum handvirkt fyrr en eftir síðustu tilraun af þessum þremur tilraunir.

- **Efni skilaboða** – Þessi sía leitar að texta í öllu efni skilaboða. (Efni skilaboða er ekki sýnt í hnitanetinu.) Sían vinnur flest sértákn (á borð við bandstrik) sem stafabilstákn sem Boole OR-virknitákn. Til dæmis þýðir þetta að ef leitað er að tilteknu `journalid` gildi sem jafngildir *USMF-123456* mun kerfið finna öll skilaboð sem innihalda „USMF“ eða „123456“. Í þessu tilfelli er líklegt að niðurstöðulistinn sé langur. Því er betra að slá inn *123456*, því þá fást sértækari niðurstöður.

Einnig er hægt að flokka og sía listann með því að velja einhverja af dálkafyrirsögnunum og slá inn skilyrði í svarglugga fellilistans.

### <a name="view-the-message-log-message-content-and-details"></a>Skoða skilaboðaannál, innihald skilaboða og upplýsingar

Nákvæmar upplýsingar um skilaboð er hægt að finna með því að velja þau í hnitanetinu og síðan opna flipana **Kladdi** eða **Hráefni** undir hnitaneti skilaboða þar sem hvert tilvik úrvinnslu er sýnt.

Á tækjastikunni á flipanum **Kladdi** eru eftirfarandi hnappar:

- **Kladdi** – Veldu þennan hnapp til að sýna niðurstöður úr vinnslu. Þessi hnappur er sérstaklega gagnlegur þegar skilaboð hafa gildið *Niðurstaða úrvinnslu* **Mistókst** og þú vilt kynna þér ástæður þess að úrvinnsla mistókst.
- **Búnt** – Hægt er að keyra margar skilaboðaaðgerðir sem hluta af sömu runuvinnslu. Velja þennan hnapp til að skoða þessi ítarlegu gögn. Til dæmis er hægt að sjá hvort tengsl séu til staðar sem krefjast sérstakrar vinnsluraðar fyrir tiltekin skilaboð.

### <a name="manually-process-or-cancel-a-message"></a>Vinna handvirkt úr eða hætta við skilaboð

Þú getur vinna úr eða hætta við skilaboð handvirkt eftir þörfum, eftir núverandi stöðu þeirra. Veljið skilaboðin í hnitanetinu og síðan velja **Vinna úr** eða **Hætta við** á aðgerðasvæðinu

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Setja upp viðskiptatilvik til að senda viðvaranir vegna misheppnaðra úrvinnsluniðurstaðna

Hægt er að setja upp [viðskiptatilvik](../../fin-ops-core/dev-itpro/business-events/home-page.md) sem láta þig vita af niðurstöðum úr úrvinnslu sem mistókst. Opnaðu **Kerfisstjórnun \> Uppsetning \> Viðskiptatilvik \> Vörulisti viðskiptatilvika,** og virkjaðu viðskiptatilvik sem er nefndur *Skilaboð um skilaboðaúrvinnslu meðhöndluð*.

Sem hluti af virkjunarferlinu ertu beðin/n um að tilgreina hvort tilvikið eigi eingöngu við um einn lögaðila eða eigi við um alla lögaðila. Þú ert einnig beðin(n) um að gefa upp gildi **Heiti endastöðvar**. Þetta gildi verður að vera skilgreint fyrst.

> [!NOTE]
> Ef reiturinn **Þegar viðskiptatilvik á sér stað** er stillt á *Microsoft Power Automate* (frekar en til dæmis *HTTPS*) verður gildið **Heiti endastöðvar** sjálfkrafa stofnað í Supply Chain Management samkvæmt *Microsoft Power Automate* uppsetningunni.
