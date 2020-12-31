---
title: Hanna grunnstillingar rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði
description: Eftirfarandi skref útskýra hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili rafræn skýrslugerð getur grunnstilla snið rafræn skýrslugerð til að mynda skýrslur sem skjöl í Microsoft Word.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d4959b511022e1aa98544d23da6afcda1f6adf2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681926"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>Hanna grunnstillingar rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili rafræn skýrslugerð getur grunnstilla snið rafræn skýrslugerð (ER) til að mynda skýrslur sem skjöl í Microsoft Word. Hægt er að framkvæma þessum skrefum í GBSI fyrirtækinu.

Til að ljúka þessum skrefum verður fyrst að ljúka við skref í verkefnaleiðbeiningar „Búa til grunnstilling Rafræn skýrslugerð til að mynda skýrslur í OPENXML-snið“. Fyrirfram verður líka að hlaða niður og vista eftirfarandi sniðmát staðbundið fyrir sýnishorn skýrslu:

- [Sniðmát greiðsluskýrslu](https://go.microsoft.com/fwlink/?linkid=862266)
- [Afmarkað sniðmát greiðsluskýrslu](https://go.microsoft.com/fwlink/?linkid=862266)


Þetta ferli er fyrir eiginleika sem var bætt við í Microsoft Dynamics 365 for Operations, útgáfu 1611.


## <a name="select-the-existing-er-report-configuration"></a>Velja fyrirliggjandi grunnstilling skýrsla í Rafræn skýrslugerð
1. Í **Skoðunarrúðunni ferðu í Einingar > Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð**. Gakktu úr skugga um að veitandi grunnstillingar „Litware, Inc.“ sé merkt sem virk.  
2. Smellið á **Skilgreiningar skýrslugerðar**. Við munum endurnota fyrirliggjandi grunnstillingu Rafræn skýrslugerð sem var fyrst hönnuð til að mynda skýrsluúttak í OPENXML-sniði.  
3. Stækkið eða fellið saman „Greiðslulíka“ í trénu.
4. Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.
5. Smellið á Hönnuður.

## <a name="replace-the-excel-template-with-the-word-template"></a>Skipta Excel-sniðmáti út fyrir Word-sniðmát

Núna er Excel-skjal notað sem sniðmát til að mynda úttak í OPENXML-sniði. Við munum flytja inn sniðmát skýrslunnar í Word-sniði.

1. Smelltu á **Viðhengi**. Skipta út fyrirliggjandi Excel-sniðmát fyrir Word-sniðmát sem áður var sótt, SampleVendPaymDocReport.docx. Athugaðu að þetta sniðmát inniheldur aðeins útlit skjals sem á að mynda sem úttak í Rafræn skýrslugerð.  
2. Smellið á **Eyða**.
3. Smellið á **Já**.
4. Smellt er á **Nýtt**.
5. Smelltu á **Skrá**.
6. Smellið á **Fletta**. Fletta á og velja SampleVendPaymDocReport.docx sem áður var sótt. Smellt er á **OK**. Velja sniðmát sem sótt í fyrra skref.  
7. Sláið inn eða veldu gildi í reitnum **sniðmát**.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Víkka Word-sniðmát út með því bæta við sérstilltum XML-hluta
1. Smellt er á **Vista**. Auk þess að vista breyting á grunnstilling, aðgerðin Vista uppfærir viðhengt Word-sniðmát. Uppbygging hannaða sniðsins er flutt í viðhengt Word-skjal sem nýr sérstilltur XML-hluti með heitinu „Skýrsla“. Athugaðu að viðhengda Word-sniðmát inniheldur ekki aðeins útlit skjalsins sem á að mynda sem úttak Rafræn skýrslugerð, heldur líka inniheldur uppbygging gagna sem Rafræn skýrslugerð setur inn í sniðmát í þessari keyrslu.  
2. Smelltu á **Viðhengi**.
    + Nú þarf að binda einingar sérstillta XML-hlutans „Skýrsla“ við hluta í Word-skjal.  
    + Ef þú þekkir Word-skjöl sem hægt er að hanna sem skjámynd sem innihalda efnisstjórnun sem eru bundin af einingum af sérstillt XML-hlutar, skal spila öll skref næsta undirverkefnis til að mynda slíkt skjal. Sjá frekari upplýsingar í [Stofna eyðublöð sem notendur fylla út eða prenta í Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US). Annars skal sleppa öllum skrefum í næsta undirverkefni.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Fá Word með sérstillt XML-hluta til að framkvæma gagnatengsl

Opnaðu þetta skjal í Word og gerðu eftirfarandi:  
1. Opnaðu flipann Word Developer (sérstilltu borðann ef hann er ekki virkur enn).
2. Veldu XML vörpunarglugga.
3. Veldu sérstillta XML-hlutann „Skýrsla“ í uppflettingu.
4. Framkvæmdu vörpun eininga í völdum sérstilltum XML-hluta og efnisstjórnun í Word-skjal.  5. Vistaðu uppfært Word-skjal á staðbundið drif.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Hlaða upp Word-sniðmát með sérstillt XML-hluta sem er bundinn við efnisstjórnun
1. Smellið á **Eyða**.
2. Smellið á **Já**. Bæta við nýju sniðmáti. Ef þú laukst við skrefin í fyrra undirverk skal velja Word-skjal sem var undirbúið og vista staðbundinn. Annars skal velja MS Word-sniðmátið SampleVendPaymDocReportBounded.docx sem áður var sótt.  
3. Smellt er á **Nýtt**.
4. Smelltu á **Skrá**.
5. Smellið á **Fletta**. Fletta á og velja SampleVendPaymDocReportBounded.docx sem áður var sótt. Smellt er á **OK**.
6. Í svæði **Sniðmát** skal velja skjal sem var hlaðið niður í fyrra skrefi.
7. Smellt er á **Vista**.
8. Lokið síðunni.

## <a name="execute-the-format-to-create-word-output"></a>Framkvæma snið til að mynda Word-úttak
1. Í **Aðgerðarrúðunni** smellirðu á **Skilgreiningar**.
2. Smelltu á **Færibreytur notanda**.
3. Veljið Já í reitnum **Stillingar keyrslu**.
4. Smellt er á **OK**.
5. Smellið á **Breyta**.
6. Veljið Já í reitnum **Drög keyrslu**.
7. Smellt er á **Vista**.
8. Lokið síðunni.
9. Lokið síðunni.
10. Í **skoðunarrúðunni** ferðu í **Einingar > Viðskiptaskuldir > Greiðslur > Greiðslubók**.
11. Smellið á **Línur**.
12. Merkið eða afmerkið allar línur í listanum.
13. Smelltu á **Greiðslustöðu**.
14. Smelltu á **Ekkert**.
15. Smelltu á **Mynda greiðslur**.
16. Smellt er á **OK**.
17. Smellt er á **OK**. Greina myndað úttak. Athuga að myndað úttak er sett fram í Word-snið og inniheldur upplýsingar um unnar greiðslur.  

