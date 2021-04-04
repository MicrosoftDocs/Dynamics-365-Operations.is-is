---
title: Endurnýta stillingar rafrænnar skýrslugerðar með Excel-sniðmátum til að búa til skýrslur á Word-sniði
description: Þetta efnisatriði lýsir því hvernig skýrslusnið sem voru hönnuð til að mynda skýrslur sem Excel-vinnubækur geta verið skilgreind til að búa til skýrslur sem Word-skjöl.
author: NickSelin
manager: AnnBe
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 601896bad72b079759b1a07efba8717101e94362
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569312"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>Endurnýta stillingar rafrænnar skýrslugerðar með Excel-sniðmátum til að búa til skýrslur á Word-sniði

[!include [banner](../../includes/banner.md)]

Til að búa til skýrslur sem Microsoft Word-skjöl er hægt að [skilgreina](../er-design-configuration-word.md) nýtt [rafrænt skýrslugerðar](../general-electronic-reporting.md)[snið](../general-electronic-reporting.md#FormatComponentOutbound). Að öðrum kosti er hægt að nota snið sem var upphaflega hannað til að mynda skýrslur sem Excel-vinnubækur. Í þessu tilfelli þarf að skipta Excel-sniðmátinu út fyrir Word-sniðmát.

Eftirfarandi ferli sýna hvernig notandi annaðhvort í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur skilgreint snið rafrænnar skýrslugerðar til að búa til skýrslur sem Word-skrár með því að endurnýta snið rafrænnar skýrslugerðar sem var hannað til að mynda skýrslur sem Excel-skrár.

Hægt er að ljúka við allar þessar aðgerðir í GBSI-fyrirtækinu.

## <a name="prerequisites"></a>Forkröfur

Til að ljúka þessum ferlum þarf fyrst að fylgja skrefunum í verkleiðbeiningunni [Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði](er-design-reports-openxml-2016-11.md).

Einnig þarf að hlaða niður og vista eftirfarandi sniðmát staðbundið fyrir sýnishorn skýrslu:

- [Sniðmát greiðsluskýrslu (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=862266)
- [Bundið sniðmát greiðsluskýrslu (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=862266)

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611 (nóvember 2016).

## <a name="select-the-existing-er-report-configuration"></a>Velja fyrirliggjandi grunnstilling skýrsla í Rafræn skýrslugerð

1. Í Dynamics 365 Finance skal fara í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Gangið úr skugga um að skilgreiningarveitan **Litware, Inc** sé valin sem **Virk**. Ef svo er ekki skal fylgja skrefunum í verkleiðbeiningunni [Stofna skilgreiningarveitendur og merkja þá sem virka](er-configuration-provider-mark-it-active-2016-11.md).
3. Veldu **Skilgreiningar skýrslugerðar**. Endurnota skal fyrirliggjandi skilgreiningu rafrænnar skýrslugerðar sem var fyrst hönnuð til að mynda skýrsluúttak á OPENXML-sniði.
4. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan** og velja **Dæmi um vinnublaðsskýrslu**.

    > [!NOTE]
    > Útgáfudrögum valins sniðs rafrænnar skýrslugerðar er hægt að breyta í flýtiflipanum **Útgáfur**.

5. Veljið **Hönnuður**.
6. Athugið að á síðunni **Sniðshönnuður** gefur titill á einingu rótarsniðs til kynna að Excel-sniðmátið sé í notkun sem stendur.

![Núverandi skilgreining valin](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>Fara yfir sótt Word-sniðmát

1. Í Word-skjáborðsforritinu skal opna sniðmátsskrána **SampleVendPaymDocReport.docx** sem var sótt hér áður.
2. Gangið úr skugga um að sniðmátið innihaldi aðeins útlit skjalsins sem á að mynda sem úttak rafrænnar skýrslugerðar.

![Útlit Word-sniðmátsins í skjáborðsforritinu](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Skipta Excel-sniðmáti út fyrir Word-sniðmát og bæta við sérsniðnum XML-hluta

Núna er Excel-skjal notað sem sniðmát til að mynda úttak í OPENXML-sniði. Þessu sniðmáti verður skipt út fyrir Word-sniðmátskránni SampleVendPaymDocReport.docx sem var sótt hér á undan. Þú munt einnig víkka Word-sniðmát út með því bæta við sérstilltum XML-hluta.

1. Í Finance, á síðunni **Sniðshönnuður**, í flipanum **Snið**, skal velja **Viðhengi**.
2. Á síðunni **Viðhengi** skal velja **Eyða** til að fjarlægja fyrirliggjandi Excel-sniðmát. Veljið **Já** til að staðfesta breytinguna.
3. Veljið **Ný** \> **Skrá**.

    > [!NOTE]
    > Velja verður gerð skjals sem var [skilgreint](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) í færibreytum rafrænnar skýrslugerðar til að vista sniðmát rafrænna skýrslugerðarsniða.

4. Veljið **Fletta** og flettið síðan og veljið skrána **SampleVendPaymDocReport.docx** sem var sótt áður.
5. Veljið **Í lagi**.
6. Lokaðu síðunni **Viðhengi**.
7. Á síðunni **Sniðshönnuður**, í reitinn **Sniðmát**, skal færa inn eða velja skrána **SampleVendPaymDocReport.docx** til að nota Word-sniðmátið í staðinn fyrir Excel-sniðmátið sem var valið hér áður.
8. Veljið **Vista**.

    Auk þess að vista breyting á grunnstilling uppfærir aðgerðin **Vista** viðhengt Word-sniðmát. Stigveldisskipulagi hannaða sniðsins er bætt við viðhengt Word-skjal sem nýr sérstilltur XML-hluti sem heitir **Skýrsla**. Viðhengt Word-sniðmát inniheldur útlit skjalsins sem verður myndað sem úttak rafrænnar skýrslugerðar og skipulag gagna sem rafræn skýrslugerð færir inn í sniðmátið við keyrslu.

9. Athugið að titill á einingu rótarsniðs gefur til kynna að Word-sniðmátið sé í notkun sem stendur.

    ![Excel-sniðmáti skipt út fyrir Word-sniðmát og sérsniðnum XML-hluta bætt við](../media/er-design-configuration-word-2016-11-image03.gif)

10. Í flipanum **Snið** skal velja **Viðhengi**.

Nú er hægt að varpa einingum sérsniðna XML-hlutans **Skýrslur** í efnisstýringar Word-skjalsins.

Ef þú kannast við ferlið við hönnun Word-skjala sem snið sem innihalda [efnisstýringar](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) sem er varpað í einingar [sérsniðinna XML-hluta](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) skal ljúka öllum skrefum í næsta ferli til að búa til skjalið. Frekari upplýsingar er að finna [Búa til snið sem notendur ljúka við eða prenta í Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b). Annars skal sleppa næsta ferli.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Sækja Word-skjal sem er með sérsniðinn XML-hluta og varpa gögnum

1. Í Finance, á síðunni **Viðhengi**, skal **Opna** til að sækja valið sniðmát úr Finance og vista það staðbundið sem Word-skjal.
3. Í Word-skjáborðsforritinu skal opna skjalið sem var sótt.
4. Í flipanum **Þróunaraðili** skal velja **XML-vörpunarsvæði**.

    > [!NOTE]
    > Ef flipinn **Þróunaraðili** birtist ekki í borðanum skal sérsníða borðann til að bæta honum við.

5. Á svæðinu **XML-vörpun**, í reitnum **Sérsniðinn XML-hluti**, skal velja sérsniðna XML-hlutann **Skýrsla**.
6. Varpið einingum valda sérsniðna XML-hlutans **Skýrsla** og efnisstýringum Word-skjalsins.
7. Vistið uppfært Word-skjal staðbundið sem **SampleVendPaymDocReportBounded.docx**.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Fara yfir Word-sniðmátið þar sem sérsniðnum XML-hluta er varpað í efnisstýringar

1. Í Word-skjáborðsforritinu skal opna sniðmátsskrána **SampleVendPaymDocReportBounded.docx**.
2. Gangið úr skugga um að sniðmátið innihaldi útlit skjalsins sem á að mynda sem úttak rafrænnar skýrslugerðar. Efnisstýringarnar sem eru notaðar sem staðgenglar fyrir gögn sem rafræn skýrslugerð færir inn í þetta sniðmát við keyrslu byggjast á vörpunum sem eru skilgreindar milli eininga sérsniðna XML-hlutans **Skýrsla** og efnisstýringar Word-skjalsins.

![Forskoða Word-sniðmát í skjáborðsforritinu](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Hlaða upp Word-sniðmáti þar sem sérsniðnum XML-hluta er varpað í efnisstýringar

1. Í Finance, á síðunni **Viðhengi**, skal velja **Eyða** til að fjarlægja Word-sniðmátið sem er með engar varpanir milli eininga sérsniðna XML-hlutans **Skýrsla** og efnisstýringar. Veljið **Já** til að staðfesta breytinguna.
2. Veljið **Ný** \> **Skrá** til að bæta við nýrri sniðmátsskrá sem inniheldur varpanir milli eininga sérsniðna XML-hlutans **Skýrsla** og efnisstýringar.

    > [!NOTE]
    > Velja verður gerð skjals sem var [skilgreint](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) í færibreytum rafrænnar skýrslugerðar til að vista sniðmát rafrænna skýrslugerðarsniða.

3. Veljið **Fletta** og flettið síðan að og veljið skrána **SampleVendPaymDocReportBounded.docx** sem var sótt eða undirbúin með því að ljúka ferlinu í hlutanum [Ná í Word sem er með sérsniðinn XML-hluta til að gera gagnavörpun](#get-word-doc).
4. Veljið **Í lagi**.
5. Lokaðu síðunni **Viðhengi**.
6. Á síðunni **Sniðshönnuður**, í reitnum **Sniðmát**, skal velja skjalið sem var sótt.
7. Veljið **Vista**.
8. Lokaðu síðunni **Sniðshönnuður**.

## <a name="mark-the-configured-format-as-runnable"></a>Merkja skilgreint snið sem keyranlegt

Til að keyra útgáfudrög breytanlega sniðsins þarf að gera það [keyranlegt](../er-quick-start2-customize-report.md#MarkFormatRunnable).

1. Í Finance, á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
2. Í glugganum **Færibreytur notanda** skal stilla valkostinn **Keyra stillingar** á **Já** og síðan velja **Í lagi**.
3. Veljið **Breyta** til að gera núverandi síðu breytanlega ef þörf krefur.
4. Fyrir þegar völdu skilgreininguna **Dæmi um vinnublaðsskýrslu** skal stilla valkostinn **Keyra drög** á **Já**.
5. Veljið **Vista**.

## <a name="run-the-format-to-create-output-in-word-format"></a>Keyra snið til að búa til úttak á Word-sniði

1. Í Finance skal fara í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók**.
2. Í greiðslubók sem var færð inn áður skal velja **Línur**.
3. Á síðunni **Greiðslur lánardrottna** skal velja allar línur í hnitanetinu.
4. Veljið **Greiðslustaða** \> **Engin**.

    ![Greiðslur til úrvinnslu á greiðslusíðu lánardrottins](../media/er-design-configuration-word-2016-11-image05.png)

5. Á aðgerðasvæðinu skal velja **Búa til greiðslur**.
6. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í reitnum **Greiðslumáti** skal velja **Rafrænn**.
    2. Í reitnum **Bankareikningur** skal velja **GBSI OPER**.
    3. Veljið **Í lagi**.

7. Í **Svargluggi rafrænna skýrslufæribreyta** velurðu **Í lagi**.
8. Myndað úttak er sett fram í Word-snið og inniheldur upplýsingar um unnar greiðslur. Greina myndað úttak.

    ![Myndað úttak á Word-sniði](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Hanna nýja skilgreiningu rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði](../er-design-configuration-word.md)
- [Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]