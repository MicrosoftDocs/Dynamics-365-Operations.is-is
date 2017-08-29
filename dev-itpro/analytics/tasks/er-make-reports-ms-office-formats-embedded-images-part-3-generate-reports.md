--- 
title: "Mynda skýrslur á Microsoft Office-sniði með innfelldum myndum fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki „Kerfisstjóra“ eða „Þróunaraðila rafrænnar skýrslulausnar“ getur hannað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) til að búa til rafræn skjöl í MS office sniði (Excel og Word) sem innihalda ívafnar myndir."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4576d89923926971ab3ca30dc702baedf05f602a
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="generate-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a>Mynda skýrslur á Microsoft Office-sniði með innfelldum myndum fyrir rafræna skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki „Kerfisstjóra“ eða „Þróunaraðila rafrænnar skýrslulausnar“ getur hannað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) til að búa til rafræn skjöl í MS office sniði (Excel og Word) sem innihalda ívafnar myndir.

Í þessu dæmi muntu nota stofnaða Rafræn skýrslugerð skilgreiningar fyrir sýni fyrirtæki, „Litware, Inc.“.  Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Rafræn skýrslugerð í MS Office sniði með ívafnar myndir (Hluti 2: Endurskoða grunnstillingar)“. Hægt er að framkvæma þessi skref í „USMF“ fyrirtæki.


## <a name="run-format-with-initial-model-mapping"></a>Keyra snið með upphaflegu vörpun líkans
1. Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.
2. Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „USMF OPER“.
3. Í aðgerðasvæðinu er smellt á setja upp.
4. Smella skal á athuga.
5. Smella á Prenta athugun.
    * Keyra sniðið til prufu.  
6. Veljið Já í reitnum Snið fyrir framseljanlega ávísun
7. Smellið á „Í lagi“.
    * Endurskoða stofnað úttak. Athugið að lógó fyrirtækisins er í skýrslunni ásamt undirskrift frá viðurkenndum aðila. Myndin af undirskriftinni er tekin úr reit frá „Hólf“ gagnategund úr útlitskrá ávísunar sem tengist völdum bankareikningi.  
8. Útvíkka hluta Eintaka.
9. Smellið á „Breyta“.
10. Í reitnum vatnsmerki, skal færa inn „Prenta vatnsmerki sem ógilt“.
    * Breyta stillingu vatnsmerkjasniðsins þannig að það sýni vatnsmerkjatextann í mynduðu skjali í Excel lagaðri einingu.  
11. Smella á Prenta athugun.
12. Smellið á „Í lagi“.
    * Endurskoða stofnað úttak. Athugið að vatnsmerkið er sýnt í stofnuðu skýrslunni í samræmi við valmöguleikann.  
13. Lokið síðunni.
14. Í Aðgerðarrúðunni er smellt á Stjórna greiðslum.
15. Smellið á Ávísanir.
16. Smellt er á Sýna síur.
17. Notið eftirfarandi síur: færðu inn síugildi "381","385","389" á reitnum "heiti ávísunarnúmer" með því að nota síuvirknitáknið „er eitt af".
18. Í listanum er merkt við allar línur.
19. Smellið á Prenta afrit af ávísun
    * Keyra sniðið til að endurprenta valdar ávísanir.  
    * Endurskoða stofnað úttak. Athugið að valdar ávísanirnar hafa verið endurprentaðar. Lógó og merkimiðar fyrirtækisins eru ekki prentaðir út því þeir birtast á forprentaða forminu.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>Breyta vörpun innflutts gagnalíkans
1. Lokið síðunni.
2. Lokið síðunni.
3. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
4. Í trénu skal velja „Líkan fyrir ávísanir“.
5. Smellið á Hönnuður.
6. Smellt er á Varpa líkani á gagnagjafa.
7. Smellið á Hönnuður.
    * Við munum breyta bindingu undirskriftarafurðar gagnalíkans til að ná í undirskriftarmyndina frá skjalinu sem hefur verið hengt við útlitsskrá ávísunarinnar sem er tengd við valinn bankareikning.  
8. Slökkva á Sýna upplýsingar.
9. Í trénu skal víkka út „Útlit“.
10. Í trénu skal víkka út „Útlit\Undirskrift“.
11. Í trénu skal velja „Útlit\Undirskrift\mynd = ávísanareikningur.„<Tengsl“.BankChequeLayout.Signature1Bmp“.
12. Í trénu skal víkka út „ávísanareikningur“.
13. Í trénu skal víkka út „ávísanareikningur\<Tengsl“.
14. Í trénu skal víkka út „ávísanareikningur\<Tengsl\BankChequeLayout“.
15. Í trénu skal víkka út „ávísanareikningur\<Tengsl\BankChequeLayout\<Tengsl“.
16. Í trénu skal víkka út „ávísanareikningur\<Tengsl\BankChequeLayout\<Tengsl\<Skjöl“.
17. Í trénu skal víkka út „ávísanareikningur\<Tengsl\BankChequeLayout\<Tengsl\<Skjöl\getFileContentAsContainer()“.
18. Smelltu á Binda.
19. Smellið á „Vista“.
20. Lokið síðunni.
21. Lokið síðunni.
22. Lokið síðunni.
23. Lokið síðunni.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Keyra snið með því að nota leiðrétta vörpun líkans
1. Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið bankareikningur með gildið 'USMF OPER'.
3. Í aðgerðasvæðinu er smellt á setja upp.
4. Smella skal á athuga.
5. Smella á Prenta athugun.
6. Smellið á „Í lagi“.
    * Endurskoða stofnað úttak. Athugið að myndin frá viðhengi Skjalastjórnunar birtist sem undirskrift frá viðurkenndum aðila.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>Nota MS Word skjal sem sniðmát í innflutta sniðinu
1. Lokið síðunni.
2. Lokið síðunni.
3. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
4. Í trénu skal víkka út „Líkan fyrir ávísanir“.
5. Í trénu skal velja „Líkan fyrir ávísanir\Ávísanir prentsnið“.
6. Smellið á Hönnuður.
7. Smellt er á viðhengi
8. Smellið á Eyða.
9. Smella á Já.
10. Smellið á „Nýtt“.
11. Smella á Skrá
    * Smellið á Fletta og veljið fyrirfram niðurhalað „Ávísun snið Word.docx“ skjal.  
12. Lokið síðunni.
13. Sláið inn eða veldu gildi í reitnum sniðmát.
14. Smellið á „Vista“.
15. Lokið síðunni.
16. Smellið á „Breyta“.
17. Veljið Já í svæðinu drög keyrslu.
18. Lokið síðunni.
19. Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.
20. Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „USMF OPER“.
21. Smella skal á athuga.
22. Smella á Prenta athugun.
23. Smellið á „Í lagi“.
    * Endurskoða stofnað úttak. Athugið að úttakið hefur verið búið til sem MS Word skjal með ívafnar myndir þar sem lógó fyrirtækisins birtist, undirskrift frá viðurkenndum aðila og valinn texti vatnsmerkisins.  


