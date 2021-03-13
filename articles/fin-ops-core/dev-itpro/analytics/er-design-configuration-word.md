---
title: Hanna nýja skilgreiningu rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði
description: Þetta efnisatriði útskýrir hvernig notendur geta skilgreint nýtt snið rafrænnar skýrslugerðar til að búa til skýrslur sem Microsoft Word-skjöl.
author: NickSelin
manager: AnnBe
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 535e46eb033bf2796ab8e4b0d2e29767ad0a8cdf
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094155"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Hanna nýja skilgreiningu rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði

[!include [banner](../includes/banner.md)]

Til að búa til skýrslur sem Microsoft Word-skjöl þarf að hanna sniðmát fyrir skýrslrnar með til dæmis Word-skjáborðsforritinu. Eftirfarandi mynd sýnir dæmi um sniðmát fyrir stjórnunarskýrsluna sem hægt er að búa til þannig að hún sýni upplýsingar um afgreiddar greiðslur lánardrottna.

![Dæmi um sniðmát fyrir stjórnunarskýrsluna í skjáborðsforriti Word](./media/er-design-configuration-word-image1.png)

Til að nota Word-skjal sem sniðmát fyrir skýrslur á Word-sniði er hægt að skilgreina nýja [rafræna skýrslugerðar](general-electronic-reporting.md) [lausn](er-quick-start1-new-solution.md). Þessi lausn verður að fela í sér [skilgreiningu](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar sem inniheldur [sniðshlut](general-electronic-reporting.md#FormatComponentOutbound) rafrænnar skýrslugerðar.

> [!NOTE]
> Þegar ný skilgreining rafræns skýrslugerðarsniðs er búin til þannig að hún búi til skýrslur á Word-sniði þarf annaðhvort að velja **Word** sem sniðgerð í fellilistaglugganum **Stofna skilgreiningu** eða skilja reitinn **Sniðsgerð** eftir auðan.

![Skilgreining sniðs stofnuð á skilgreiningarsíðunni](./media/er-design-configuration-word-image2.gif)

Sniðsþáttur rafrænnar skýrslugerðar fyrir lausnina verður að innihalda sniðseininguna **Excel\\Skrá** og sú sniðseining verður að vera tengd við Word-skjal sem verður notað sem sniðmát fyrir myndaðar skýrslur við keyrslu. Til að skilgreina sniðsþátt rafrænnar skýrslugerðar þarf að opna útgáfu [draga](general-electronic-reporting.md#component-versioning) fyrir stofnaða skilgreiningu rafrænnar skýrslugerðar í sniðshönnuði rafrænnar skýrslugerðar. Síðan skal bæta við einingunni **Excel\\Skrá**, hengja Word-sniðmátið við breytanlegt snið rafrænnar skýrslugerðar og tengja það sniðmát við eininguna **Excel\\Skrá** sem var bætt við.

> [!NOTE]
> Þegar sniðmát er hengt við þarf að nota [gerð skjals](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) sem var áður [skilgreind](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) í færibreytum rafrænnar skýrslugerðar til að vista sniðmát rafrænna skýrslugerðarsniða.

![Sniðmát hengt við á síðu sniðshönnuðar](./media/er-design-configuration-word-image3.gif)

Hægt er bæta við földuðum einingum **Excel\\Afmörkun** og **Excel\\Hólf** fyrir eininguna **Excel\\Skrá** til að tilgreina skipulag gagna sem verið fært inn í myndaðar skýrslur við keyrslu. Síðan þarf að binda þessar einingar við gagnagjafa breytanlegs sniðs rafrænnar skýrslugerðar til að tilgreina raunveruleg gögn sem verða færð inn í myndaðar skýrslur við keyrslu.

![Földuðum einingum bætt við á síðu sniðshönnuðar](./media/er-design-configuration-word-image4.gif)

Þegar breytingar á rafrænu skýrslugerðarsniði eru vistaðar á hönnunartíma verður stigveldi sniðsskipulags vistað í viðhengdu Word-sniðmáti sem [sérstilltur XML-hluti](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) sem heitir **Skýrsla**. Ná þarf í breytta sniðmátið, sækja það úr Finance, vista það staðbundið og opna það í skjáborðsforriti Word. Eftirfarandi mynd sýnir dæmi um sniðmát, sem vistað er staðbundið, fyrir stjórnunarskýrsluna sem inniheldur sérstillta XML-hlutann **Skýrsla**.

![Sýnishorn af skýrslusniðmáti forskoðað í skjáborðsforriti Word](./media/er-design-configuration-word-image5.gif)

Þegar bindingar á sniðseiningunum **Excel\\Afmörkun** og **Excel\\Hólf** eru keyrðar á keyrslutíma munu gögn sem allar bindingar skila fara inn í myndað Word-skjal sem sjálfstæðir reitir í sérstillta XML-hlutanum **Skýrsla**. Til að slá inn gildin úr reitum sérsniðna XML-hlutans í mynduðu skjali þarf að bæta viðeigandi [efnisstýringu](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) Word við Word-sniðmátið til að þjóna hlutverki staðgengils fyrir gögn sem verður fyllt út í við keyrslu. Til að tilgreina hvernig fyllt er í efnisstýringar skal varpa allri efnisstýringu í viðeigandi reit sérstillta XML-hlutans **Skýrsla**.

![Efnisstýringum bætt við og varpað í skjáborðsforrit Word](./media/er-design-configuration-word-image6.gif)

Síðan þarf að skipta út upprunalegu Word-sniðmáti breytanlega sniði rafrænnar skýrslugerðar í staðinn fyrir breytt sniðmát sem nú inniheldur efnisstýringar Word sem var varpað í reitina í sérstilla XML-hlutanum **Skýrsla**.

![Sniðmáti skipt út á síðu sniðshönnuðar](./media/er-design-configuration-word-image7.gif)

Þegar skilgreint snið rafrænnar skýrslugerðar er keyrt er viðhengt Word-sniðmát notað til að mynda nýja skýrslu. Raunveruleg gögn eru geymd í Word-skýrslunni sem sérsniðinn XML-hluti sem heitir **Skýrsla**. Þegar mynduð skýrsla er opnuð er fyllt út í efnisstýringar Word með gögnum úr sérsniðna XML-hlutanum **Skýrsla**.

## <a name="frequently-asked-questions"></a>Algengar spurningar

**Spurning:** Ég skilgreindi snið rafrænnar skýrslugerðar til að prenta Word-skjal sem inniheldur aðsetur fyrirtækis. Í Word-sniðmátinu fyrir þetta snið rafrænnar skýrslugerðar setti ég inn efnisstýringu sniðins texta til að gefa upp aðsetur fyrirtækis. Í Finance færði ég inn aðsetur fyrirtækisins sem texta í mörgum línum og valdi **Færa inn** til að bæta við vendingu fyrir hverja línu sem ég slæ inn. Þess vegna vænti ég þess að aðsetur fyrirtækisins muni birtast sem texti í mörgum línum í mynduðum skjölum. Aðsetrið birtist hins vegar sem texti í einni línu sem inniheldur sértákn í staðinn fyrir vendingar. Hvað er að stillingunum mínum?

**Svar:** Í stað þess að nota efnisstýringu sniðins texta skal nota efnisstýringu ósniðins texta og velja gátreitinn **Leyfa vendingu (margar efnisgreinar)** í eiginleikum stýringar.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Endurnýta stillingar rafrænnar skýrslugerðar með Excel-sniðmátum til að búa til skýrslur á Word-sniði](./tasks/er-design-configuration-word-2016-11.md)
- [Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)
