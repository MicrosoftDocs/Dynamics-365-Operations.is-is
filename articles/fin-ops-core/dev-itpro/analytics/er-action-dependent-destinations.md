---
title: Skilgreina áfangastaði rafrænnar skýrslugerðar sem eru háðir aðgerð
description: Þessi grein útskýrir hvernig á að skilgreina áfangastað sem eru háðir aðgerð fyrir snið rafrænnar skýrslugerðar sem er skilgreint til að mynda skjöl á útleið.
author: kfend
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: babd123e4c8007e3adc545bb92a2dc83bab93f4e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286248"
---
# <a name="configure-action-dependent-er-destinations"></a>Skilgreina áfangastaði rafrænnar skýrslugerðar sem eru háðir aðgerð

[!include [banner](../includes/banner.md)]

Hægt er að skilgreina [áfangastaði](electronic-reporting-destinations.md) fyrir hvern úttakshlut (möppu eða skrá) fyrir [skilgreiningu rafræns skýrslugerðarsniðs](general-electronic-reporting.md) sem er notað [til](general-electronic-reporting.md#Configuration) að mynda skjal á útleið. Notendur sem keyra snið rafrænnar skýrslugerðar af þessari gerð og eru með viðeigandi aðgangsréttindi geta einnig breytt stillingum skilgreinds áfangastaðar við keyrslu.

Í Microsoft Dynamics 365 Finance **útgáfu 10.0.17 og nýrri** er hægt að keyra snið rafrænnar skýrslugerðar með því að [úthluta](er-apis-app10-0-17.md) aðgerðarkóða sem notandi notar með því að keyra það snið rafrænnar skýrslugerðar. Til dæmis í einingunni **Viðskiptakröfur**, í stillingum prentstýringar, er hægt að velja snið rafrænnar skýrslugerðar sem myndar ákveðið viðskiptaskjal á borð við reikning með frjálsum texta. Síðan er hægt að velja **Skoða** til að forskoða reikning eða **Prenta** til að senda hann til prentara. Ef notandaaðgerð er gerð fyrir keryslu á sniði rafrænnar skýrslugerðar við keyrslu er hægt að skilgreina mismunandi áfangastaði rafrænnar skýrslugerðar fyrir mismunandi notandaaðgerðir. Þessi grein útskýrir hvernig á að skilgreina áfangastaði rafrænnar skýrslugerðar fyrir þessa gerð rafræns skýrslugerðarsniðs.

## <a name="make-action-dependent-er-destinations-available"></a>Gera aðgerðarháða áfangastaði rafrænnar skýrslugerðar tiltæka

Til að skilgreina aðgerðarháða áfangastaði rafrænnar skýrslugerðar í núverandi Finance-tilviki og virkja [nýtt](er-apis-app10-0-17.md) API rafrænnar skýrslugerðar skal opna vinnusvæðið [Eiginleikastjórnun](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) og kveikja á eiginleikanum **Skilgreina tiltekna áfangastaði rafrænnar skýrslugerðar til að nota fyrir mismunandi prentstýringaraðgerðir**. Til að nota skilgreinda áfangastaði rafrænnar skýrslugerðar fyrir [ákveðnar](#reports-list-wave1) skýrslur við keyrslu skal virkja eiginleikann **Leiðarúttak fyrir skýrslur prentstýringar sem byggir á áfangastöðum rafrænnar skýrslugerðar sem fara eftir aðgerð notanda (bylgja 1)**.

## <a name="configure-action-dependent-er-destinations"></a>Skilgreina áfangastaði rafrænnar skýrslugerðar sem eru háðir aðgerð

Þegar kveikt er á eiginleikanum **Skilgreina tiltekna áfangastaði rafrænnar skýrslugerðar til að nota fyrir mismunandi prentstýringaraðgerðir** er hægt að skilgreina aðgerðarháða áfangastaði rafrænnar skýrslugerðar í flýtiflipanum **Viðtökustaður skráar** á síðunni **Áfangastaður rafrænnar skýrslugerðar**. Fyrir hvern hluta er hægt að bæta við færslu og virkja tiltekna áfangastaði rafrænnar skýrslugerðar. Fyrir hverja færslu þarf að tilgreina gerð skjals sem skilgreindir áfangastaðir rafrænnar skýrslugerðar eiga við um. Í reitnum **Tegund fylgiskjals** skal velja eitt eftirfarandi gilda:

- Veljið **Rafrænt** til að nota skilgreinda áfangastaði ef enginn aðgerðarkóði er gefinn upp við keyrslu.
- Veljið **Prentstýring** til að nota skilgreinda áfangastaði ef aðgerðarkóði er gefinn upp við keyrslu.
- Veljið **Hvað sem er** til að nota alltaf skilgreinda áfangastaði óháð því hvort notandaaðgerð er gefin upp við keyrslu.

Ef skjalagerðin **Prentstýring** er valin, þarf að tilgreina notandaaðgerðir sem skilgreindir áfangastaðir rafrænnar skýrslugerðar eiga við um. Í reitnum **Prentstýringaraðgerð** skal velja eitt eftirfarandi gilda:

- Veljið **Skoða** til að nota skilgreinda áfangastaði ef **Skoða** notandaaðgerðin er sýnd við keyrslu.
- Veljið **Prenta** til að nota skilgreinda áfangastaði ef notandaaðgerðin **Prenta** er gefin upp við keyrslu.
- Veljið **Senda** til að nota skilgreinda áfangastaði ef notandaaðgerðin **Senda** er gefin upp við keyrslu.

> [!NOTE]
> Hægt er að velja margar aðgerðir fyrir eina viðtökufærslu.

Ef skjalagerðin **Hvað sem er** er valin verður **Leita sjálfkrafa** sjálfkrafa fyrir valinu í reitnum **Prentstýringaraðgerð** sem notandaaðgerð og eftirfarandi hegðun kemur fram:

- Ef enginn aðgerðarkóði notanda er gefinn upp við keyrslu eru allir skilgreindir áfangastaðir rafrænnar skýrslugerðar notaðir.
- Ef aðgerðarkóði notanda er gefinn upp við keyrslu verður áfangastaður rafrænnar skýrslugerðar sem er fyrirframskilgreindur fyrir tiltekna aðgerð notaður **óháð því hvort hann hafi verið virkjaður**:

    - Þegar aðgerðin **Skoða** er gefin upp við keyrslu verður áfangastaðurinn **Skjár** fyrir rafræna skýrslugerð notaður.
    - Þegar aðgerðin **Senda** er gefin upp við keyrslu verður áfangastaðurinn **Tölvupóstur** fyrir rafræna skýrslugerð notaður.
    - Þegar aðgerðin **Prenta** er gefin upp við keyrslu verður áfangastaðurinn **Prentari** fyrir rafræna skýrslugerð notaður.

Til dæmis er hægt nota rafræna skýrslugerðarsniðið **Reikningur með frjálsum texta (Excel)** til að prenta [reikning með frjálsum texta](../../../finance/accounts-receivable/create-free-text-invoice-new.md) þegar hann er bókaður. Til að beina mynduðu skjali eitthvert þarf að skilgreina áfangastaði rafrænnar skýrslugerðar fyrir þetta snið rafrænnar skýrslugerðar. Til dæmis gæti þurft að skilgreina þessa áfangastaði rafrænnar skýrslugerðar til að framkvæma eftirfarandi fyrir myndað skjal:

- Safnvista skjalinu ef snið rafrænnar skýrslugerðar er keyrt en enginn aðgerðarkóði er gefinn upp (til dæmis þegar skjalið er sent rafrænt).
- Forskoða skjalið í vafra þegar notandi framkvæmir aðgerðina **Skoða**.
- Safnvista og prenta skjalið þegar notandi framkvæmir aðgerðina **Prenta**.
- Safnvista skjalinu og senda það í tölvupósti sem viðhengi í tölvupóstskeyti á útleið þegar notandi framkvæmir aðgerðina **Senda**.

Eftirfarandi mynd sýnir hvernig hægt er að ná þessu fram með því að skilgreina áfangastaði rafrænnar skýrslugerðar sem safn stakra viðtökufærslna þegar hver færsla er skilgreind fyrir eina aðgerð notanda:

![Viðtökusíða rafrænnar skýrslugerðar sem er með aðgerðarháðar stillingar áfangastaðar fyrir snið rafrænnar skýrslugerðar þegar hver viðtökufærsla er skilgreind fyrir eina aðgerð notanda.](./media/er-destination-action-dependent-01.png)

Eftirfarandi mynd sýnir hvernig hægt er að ná því sama fram með því að skilgreina áfangastaði rafrænnar skýrslugerðar sem safn stakra viðtökufærslna þegar hver færsla er skilgreind fyrir einn áfangastað:

![Viðtökusíða rafrænnar skýrslugerðar sem er með aðgerðarháðar stillingar áfangastaðar fyrir snið rafrænnar skýrslugerðar þegar hver viðtökufærsla er skilgreind fyrir einn áfangastað.](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Ef aðgerðarkóði er gefinn upp fyrir keyrslu rafræns skýrslugerðarsniðs, en engir áfangastaðir hafa verið skilgreindir fyrir þann aðgerðarkóða, verður [sjálfgefinn](electronic-reporting-destinations.md#default-behavior) áfangastaður notaður.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Breyta aðgerðarháðum áfangastöðum rafrænnar skýrslugerðar við keyrslu

Þegar snið rafrænnar skýrslugerðar er keyrt, ef notandaaðgerðum hefur verið úthlutað af notendum sem eru með tilheyrandi [heimildir](electronic-reporting-destinations.md#security-considerations) til að breyta skilgreindum stillingum áfangastaðar við keyrslu, birtist svargluggi sem býður upp á möguleikann á því að breyta stillingum skilgreinds áfangastaðar. Þessi svargluggi er valfrjáls og útlit hans veltur á því hvernig kallið, sem rammi rafrænnar skýrslugerðar gerir til að keyra snið rafrænnar skýrslugerðar, hefur verið innleitt. Ef þessi svargluggi birtist verða áfangastaðir rafrænnar skýrslugerðar í honum virkjaðir samkvæmt aðgerð notanda sem er gefin upp.

Eftirfarandi mynd sýnir dæmi um svargluggann **Áfangastaðir rafræns skýrslugerðarsniðs** sem birtist þegar reikningur með frjálsum texta er [bókaður](../../../finance/accounts-receivable/create-free-text-invoice-new.md) og rafræna skýrslugerðarsniðið **Reikningur með frjálsum texta (Excel)** er keyrt til að mynda þetta skjal ef aðgerðinni **Prentari** var úthlutað og áfangastaðir rafrænnar skýrslugerðar voru skilgreindir fyrir þetta snið eins og var sýnt fyrr í þessari grein.

![Svargluggi sem býður upp á valmöguleikann til að breyta upphaflega skilgreindum áfangastöðum rafrænnar skýrslugerðar fyrir keyrt snið rafrænnar skýrslugerðar.](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Ef skilgreindir voru áfangastaðir rafrænnar skýrslugerðar fyrir marga þætti í rafræna skýrslugerðarsniðinu sem er keyrt verður boðið upp á sérstakan valkost fyrir hvern skilgreindan þátt rafræna skýrslugerðarsniðsins.

## <a name="verify-the-provided-user-action"></a>Staðfesta uppgefna aðgerð notanda

Hægt er að staðfesta hvaða notandaaðgerð, ef einhver, er gefin upp fyrir snið rafrænnar skýrslugerðar sem er keyrt þegar tiltekin notandaaðgerð er framkvæmd. Þessi staðfesting er mikilvæg þegar þarf að skilgreina aðgerðarháða áfangastaði rafrænnar skýrslugerðar, en ekki er á hreinu hvaða aðgerðarkóði notanda, ef einhver, var gefinn upp. Til dæmis þegar hafist er handa við bókun reiknings með frjálsum texta og valkosturinn **Prenta reikning** er stilltur á **Já** í svarglugganum **Bóka reikning með frjálsum texta**, er hægt að stilla valkostinn **Nota ákvörðunarstað prentstýringar** á **Já** eða **Nei**.

Fylgið þessum skrefum til að staðfesta aðgerðarkóða notanda sem gefinn er upp.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Í svarglugganum **Færibreytur notanda** skal [stilla](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) valkostinn **Keyra í kembistillingu** á **Já**.
4. Framkvæmið notandaaðgerð með því að keyra snið rafrænnar skýrslugerðar. Munið að notandafæribreytur rafrænnar skýrslugerðar eru fyrirtækis- og notandamiðaðar.
5. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Kembingarkladdar skilgreiningar**.
6. Á síðunni **Kembikladdar skilgreiningar** skal sía keyrslukladda rafrænnar skýrslugerðar til að finna kladdann fyrir keyrslu rafræna skýrslugerðarsniðsins.
7. Farið yfir kladdafærslurnar sem verða að innihalda færsluna sem geymir uppgefinn aðgerðarkóða notanda ef einhver aðgerð hefur verið gefin upp fyrir keyrslu rafræna skýrslugerðarsniðsins.

    ![Síða keyrslukladda rafrænnar skýrslugerðar sem inniheldur upplýsingar um aðgerðarkóða notanda sem hefur verið gefinn upp fyrir síaða keyrslu rafræns skýrslugerðarsniðs.](./media/er-destination-action-dependent-03.png)

## <a name=""></a><a name="reports-list-wave1">Listi yfir viðskiptaskjöl (bylgja 1)</a>

Viðskiptaskjölum í eftirfarandi lista er stjórnað af eiginleikanum **Leiðarúttak fyrir skýrslur prentstýringar sem byggir á áfangastöðum rafrænnar skýrslugerðar sem fara eftir aðgerð notanda (bylgja 1)**:

- Reikningur viðskiptavinar (reikningur með frjálsum texta)
- Reikningur viðskiptavinar (sölureikningur)
- Innkaupapöntun
- Innkaupafyrirspurn innkaupapöntunar
- Staðfesting sölupöntunar
- Athugasemd innheimtubréfs
- Vaxtanóta
- Greiðslutilkynning lánardrottins
- Beiðni um tilboð

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)

[Breytingar á API rafræns skýrslugerðarramma fyrir Application update 10.0.17](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
