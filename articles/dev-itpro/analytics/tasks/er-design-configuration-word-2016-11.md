---
title: Hanna grunnstillingar rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði
description: Eftirfarandi skref útskýra hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili rafræn skýrslugerð getur grunnstilla snið rafræn skýrslugerð til að mynda skýrslur sem skjöl í Microsoft Word.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd138fb5fea4098a862fbecba5e8ec226ed6afa9
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850304"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>Hanna grunnstillingar rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði

[!include [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili rafræn skýrslugerð getur grunnstilla snið rafræn skýrslugerð (ER) til að mynda skýrslur sem skjöl í Microsoft Word. Hægt er að framkvæma þessum skrefum í GBSI fyrirtækinu.

Til að ljúka þessum skrefum verður fyrst að ljúka við skref í verkefnaleiðbeiningar „Búa til grunnstilling Rafræn skýrslugerð til að mynda skýrslur í OPENXML-snið“. Fyrirfram verður líka að hlaða niður og vista eftirfarandi sniðmát staðbundið fyrir sýnishorn skýrslu:

- [Sniðmát greiðsluskýrslu](https://go.microsoft.com/fwlink/?linkid=862266)
- [Afmarkað sniðmát greiðsluskýrslu](https://go.microsoft.com/fwlink/?linkid=862266)


Þetta ferli er fyrir eiginleika sem var bætt við í Microsoft Dynamics 365 for Operations, útgáfu 1611.


## <a name="select-the-existing-er-report-configuration"></a>Velja fyrirliggjandi grunnstilling skýrsla í Rafræn skýrslugerð
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Gakktu úr skugga um að veitandi grunnstillingar „Litware, Inc.“ sé merkt sem virk.  
2. Smelltu á Grunnstillingar skýrslugerðar
    * Við munum endurnota fyrirliggjandi grunnstillingu Rafræn skýrslugerð sem var fyrst hönnuð til að mynda skýrsluúttak í OPENXML-sniði.  
3. Stækkið eða fellið saman „Greiðslulíka“ í trénu.
4. Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.
5. Smellið á Hönnuður.

## <a name="replace-the-excel-template-with-the-word-template"></a>Skipta Excel-sniðmáti út fyrir Word-sniðmát
    * Núna er Excel-skjal notað sem sniðmát til að mynda úttak í OPENXML-sniði. Við munum flytja inn sniðmát skýrslunnar í Word-sniði.  
1. Smellt er á viðhengi
    * Skipta út fyrirliggjandi Excel-sniðmát fyrir Word-sniðmát sem áður var sótt, SampleVendPaymDocReport.docx. Athugaðu að þetta sniðmát inniheldur aðeins útlit skjals sem á að mynda sem úttak í Rafræn skýrslugerð.  
2. Smellið á Eyða.
3. Smella á Já.
4. Smellið á „Nýtt“.
5. Smella á Skrá
6. Smellið á Fletta. Fletta á og velja SampleVendPaymDocReport.docx sem áður var sótt. Smellið á „Í lagi“.
    * Velja sniðmát sem sótt í fyrra skref.  
7. Sláið inn eða veldu gildi í reitnum sniðmát.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Víkka Word-sniðmát út með því bæta við sérstilltum XML-hluta
1. Smellið á „Vista“.
    * Auk þess að vista breyting á grunnstilling, aðgerðin Vista uppfærir viðhengt Word-sniðmát. Uppbygging hannaða sniðsins er flutt í viðhengt Word-skjal sem nýr sérstilltur XML-hluti með heitinu „Skýrsla“. Athugaðu að viðhengda Word-sniðmát inniheldur ekki aðeins útlit skjalsins sem á að mynda sem úttak Rafræn skýrslugerð, heldur líka inniheldur uppbygging gagna sem Rafræn skýrslugerð setur inn í sniðmát í þessari keyrslu.  
2. Smellt er á viðhengi
    * Nú þarf að binda einingar sérstillta XML-hlutans „Skýrsla“ við hluta í Word-skjal.  
    * Ef þú þekkir Word-skjöl sem hægt er að hanna sem skjámynd sem innihalda efnisstjórnun sem eru bundin af einingum af sérstillt XML-hlutar, skal spila öll skref næsta undirverkefnis til að mynda slíkt skjal. Nánari upplýsingar er að finna á https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US. Annars skal sleppa öllum skrefum í næsta undirverkefni.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Fá Word með sérstillt XML-hluta til að framkvæma gagnatengsl
    * Opna þetta skjal í Word og gera eftirfarandi: - Opna flipann Word Developer (sérstilltu borðann ef hann er ekki virkur).  - Velja XML vörpunargluggi.  - Velja sérstillta XML-hlutann „Skýrsla“ í uppflettingu.  - Framkvæma vörpun eininga í völdum sérstilltum XML-hluta og efnisstjórnun í Word-skjal.  - Vista uppfærður Word-skjal í staðbundið drif.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Hlaða upp Word-sniðmát með sérstillt XML-hluta sem er bundinn við efnisstjórnun
1. Smellið á Eyða.
2. Smella á Já.
    * Bæta við nýju sniðmáti. Ef þú laukst við skrefin í fyrra undirverk skal velja Word-skjal sem var undirbúið og vista staðbundinn. Annars skal velja MS Word-sniðmátið SampleVendPaymDocReportBounded.docx sem áður var sótt.  
3. Smellið á „Nýtt“.
4. Smella á Skrá
5. Smellið á Fletta. Fletta á og velja SampleVendPaymDocReportBounded.docx sem áður var sótt. Smellt er á Í lagi.
6. Í svæði Sniðmát skal velja skjal sem sótt í fyrra skref.
7. Smellið á „Vista“.
8. Lokið síðunni.

## <a name="execute-the-format-to-create-word-output"></a>Framkvæma snið til að mynda Word-úttak
1. Í Aðgerðarrúðunni er smellt á skilgreiningar.
2. Smelltu á Færibreytur notanda
3. Veljið Já í svæðinu Stillingar keyrslu.
4. Smellið á „Í lagi“.
5. Smellið á „Breyta“.
6. Veljið Já í svæðinu drög keyrslu.
7. Smellið á „Vista“.
8. Lokið síðunni.
9. Lokið síðunni.
10. Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.
11. Smellið á „Línur“.
12. Merkið eða afmerkið allar línur í listanum.
13. Smellt er á greiðslustöðu.
14. Smellt á Ekkert.
15. Smelltu á Mynda greiðslur.
16. Smellið á „Í lagi“.
17. Smellið á „Í lagi“.
    * Greina myndað úttak. Athuga að myndað úttak er sett fram í Word-snið og inniheldur upplýsingar um unnar greiðslur.  

