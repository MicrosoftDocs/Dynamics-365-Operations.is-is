---
title: Skoða og setja upp fjárhagsskýrslur
description: Þessi grein veitir æfingar sem fara með þig í gegnum yfirlit og stofnun á fjárhagsskýrslum fyrir Microsoft Dynamics 365 Finance.
author: jcart1106
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.form: FinancialReportingSetup
ms.openlocfilehash: b6709f90065c91c55a489f101da430db33355a75
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273426"
---
# <a name="view-and-design-financial-reports"></a>Skoða og hanna fjárhagsskýrslur

[!include [banner](../includes/banner.md)]

Þessi grein veitir æfingar sem fara með þig í gegnum yfirlit og stofnun á fjárhagsskýrslum fyrir Microsoft Dynamics 365 Finance. Fjárhagsskýrsla samanstendur af yfirlitsupplifun innan forritsins og einssmells skýrsluhönnun sem gerir kleift að stofna og breyta fjárhagsskýrslum.

## <a name="exercise-1-generate-and-explore-a-default-financial-report"></a>Æfing 1: Búa til og skoða sjálfgefna fjárhagsskýrslu

Fyrir þessa æfingu verður fyrirliggjandi sjálfgefin skýrsla mynduð og athuguð. Þessi skýrsla inniheldur alla lykla og inniheldur einnig lykileiginleika (eigindir) fyrir lyklana. Þú munt kafa ofan í færsluupplýsingar, nota víddarafmarkanir, breyta gjaldmiðli í skýrslunni. Fyrst uppfærum við birtingarröð vídda fyrir fjárhagsskýrslugerð. Það gerir kleift að velja hvernig víddir birtast þegar hönnun og skoðun fjárhagsskýrslna er lokið.

1. Fara í **Fjárhagsvíddarskilgreining fyrir samþættingu forrita** undir **Víddir í bókhaldslyklum** í fjárhag.
2. Færðu víddirnar svo að þær verði í eftirfarandi röð:

    1. Aðallykill
    2. Fyrirtækiseining
    3. Kostnaðarstaður
    4. Deild

    > [!NOTE]
    > Aðrar víddir geta verið í þeirri röð sem þær eru þegar í.

3. Vista víddarstillinguna. Næst munum við búa til skýrslu og kanna gögnin í henni.
4. Fara í **Fjárhagsskýrslur** undir **Fyrirspurnir og skýrslur** í fjárhag.
5. Velja línuna fyrir skýrslu sem ber heitið **Upplýsingar um fjárhag - sjálfgefið**.
6. Veljið **Breyta**.

    > [!NOTE]
    > Þú færð áminningu um að sækja eins-smells skýrsluhönnun og skrá þig inn. Notaðu skilríkin þín til að skrá þig inn.

7. Breyta grunnárinu í 2012 og velja **Mynda**. Þegar skýrsla er mynduð úr skýrsluhönnun opnast hún í nýjum vafraflipa. Hægt er að annaðhvort athuga skýrsluna á nýja vafraflipanum eða fara á upprunalega vafraflipann og opna skýrsluna þaðan með því að velja hana af listanum **Fjárhagsskýrslur**.
8. Í opinni skýrslu velurðu eina af upphæðunum til að kafa í upplýsingar um lykil fyrir skýrsluna.
9. Þegar komið er í upplýsingar um lykilinn skal velja lykil með gögnum og **kafa á stig skýrslufærslu**. Á stigi skýrslufærslu er hægt að sjá eiginleika (eigindir) sem eru innifaldir í hönnun skýrslunnar. Það fer eftir færslu og lykli, en sumar eða allar eigindir gætu verið birtar.
10. Lokaðu færslustigi skýrslu.
11. Veljið sömu eða mismunandi lykla og **opna færslur fyrir fylgiskjal**. Færslur fylgiskjals er síaðar til að samsetningu tímabils, árs og lykils + víddar á valinn lykil. Hægt er að velja að skoða aðrar upplýsingar um færslur úr fylgiskjalsfærslum.
12. Lokaðu fylgiskjalsfærslunum. I fjárhagsskýrslu er hægt að velja að skoða gögn annaðhvort fyrir mismunandi tímabil og ár eða með mismunandi eigindum og víddum sem eru notaðar. Þetta er gert með því að nota **Skýrsluvalkosti**.
13. Veldu **Skýrsluvalkosti**.
14. Veldu **Bæta við víddarafmörkun** og veldu **Viðskiptaeiningu**.
15. Sláðu 001 inn í reitinn og veldu **í lagi**. Skýrslan sýnir nú aðeins gögnin fyrir 001 Viðskiptaeining. Þetta er sérsniðið yfirlit skýrslu og er ekki tiltækt fyrir aðra til að skoða.
16. Loka síaðri skýrslu. Hægt er að birta fjárhagsskýrslur í öllum gjaldmiðlum sem hefur verið bætt við forritið.
17. Veldu **Gjaldmiðill** og veldu svo **EUR**. Skýrslan birtir nú í evrum. Allir gjaldmiðilskóðar eða gjaldmiðilstákn sem hafðir eru með í skýrsluhönnun birtast nú í notuðum gjaldmiðli. Ef ekkert gjaldeyristákn er skilgreint fyrir gjaldmiðil er gjaldmiðilstáknið ekki birt.
18. Lokaðu skýrslunni **Fjárhagsupplýsingar**.
19. Lokaðu **Skýrsluhönnuninni**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>Æfing 2: Bæta viðbótarlykli við eiginleika í skýrsluhönnun
Í þessari æfingu breytirðu fyrirliggjandi sjálfgefna skýrslu. Þú uppfærir bæði línuskilgreiningu til að taka með alla lykla og uppfærir dálkskilgreiningu til að innihalda lyklaeigindir. Eftir að uppfærslum er lokið myndarðu nýstofnuðu skýrsluna og kannar hana. Við byrjum í lista yfir fjárhagsskýrslur.

1. Fara í **Fjárhagsskýrslur** undir Fyrirspurnir og skýrslur í fjárhag.
2. Velja línuna fyrir skýrslu sem ber heitið **Samantekt á prófjöfnuði - sjálfgefið.**
3. Veljið **Breyta**. **Samantekt á prófjöfnuði – Sjálfgefin** opnar í skýrsluhönnun.
4. Veldu **Skrá**, síðan **Vista sem** og gefðu skýrslunni heitið Ítarlegur prófjöfnuður með eigindum.

    > [!NOTE]
    > Í hvert skipti sem ný skýrsla er stofnuð í skýrsluhönnun er listi yfir fjárhagsskýrslur uppfærður.

5. Úr skýrsluskilgreiningu velurðu tákn línuskilgreiningar til að opna **Prófjöfnuð – Sjálfgefna línuskilgreiningu**.
6. Vista línuskilgreininguna sem **Ítarlegur prófjöfnuður með eigindum**.
7. Með bendilinn í röð 50 skal velja **Breyta**, síðan **Setja inn línur úr víddum**. Setja inn línur úr víddum gerir þér kleift að velja víddirnar sem þú vilt hafa í línuskilgreiningunni. Fyrir þessa æfingu ætlum við að byggja upp línuskilgreiningu með aðallykli.
8. Gangið úr skugga um **Aðallykill** innihaldi öll og-merki og velja **í lagi**. Línuskilgreining inniheldur nú alla aðallykla USMF lögaðila.
9. Flettu niður í línu 11110 og eyddu línu 11110.
10. Í línu 11080 **---(undirstrikaðar upphæðir)**.
11. Í línunni 11140 gerð **Samtala allra lykla** í dálki B.
12. Í dálki C velurðu **TIL** úr fellilistanum.
13. Sláðu inn **50:11080** í dálk D.
14. **Vistaðu** skýrsluskilgreininguna. Línuskilgreiningin inniheldur nú alla lykla plús samtölulínu til að leggja alla lyklana saman. Næst uppfærum við skilgreiningu dálks til að taka með viðbótareigindir lykils.
15. Úr skýrsluskilgreiningunni **Ítarlegur prófjöfnuður með eigindum** skal velja skilgreiningartákn dálks til að dálkskilgreininguna **Samantekt á prófjöfnuði – Sjálfgefin**.
16. Vista dálkskilgreiningu sem **Ítarlegur prófjöfnuður með eigindum** Skilgreining dálks inniheldur dálka fjárhagsgagna, lýsingardálk og dálka fyrir útreikning. Við ætlum að bæta við eigindadálkum í dálkskilgreiningu til að veita frekari upplýsingar um lykla.
17. Eftirfarandi eigindir verður bætt við dálkskilgreininguna:

    - Færslubókarnúmer
    - Lýsing færslubókar
    - Færsludagsetning
    - Búið til af
    - Síðast breytt af

18. Í dálki I velurðu **ATTR** sem gerð dálksins. Síðan skal velja **Færslubókarnúmer** sem eigindaflokk.
19. Haltu áfram að bæta við dálkum fyrir eftirstandandi eigindir.
20. Í línunni **Haus 2** línunni er bætt við lýsingum fyrir sérhvern nýjan dálk sem hefur verið bætt við.
21. Vista dálkskilgreininguna. Nú þegar línuskilgreining og skilgreining dálks hafa verið uppfærðar er nauðsynlegt að bæta þeim við skýrsluskilgreininguna.
22. Úr skýrsluskilgreiningunni **Ítarlegur prófjöfnuður með eigindum** skal velja Ítarlegur prófjöfnuður með eigindum fyrir bæði línuskilgreininguna og línuskilgreininguna.
23. Breyta grunnárinu í **2012**.
24. **Vista** skýrsluskilgreiningu og **mynda**. Þegar skýrslan lýkur myndun og opnast er hægt að skoðið skýrsluna eins og gert var í fyristu æfingu. Kafaðu niður á mismunandi lyklka til að sjá hvernig viðbótareigindir eru birtar.
25. Lokaðu skýrslunni **Ítarlegur prófjöfnuður með eigindir**.
26. Lokaðu **Skýrsluhönnuninni**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>Æfing 3: Stofna fjölvíddaskýrslu með skipuriti
Í þessari æfingu breytirðu fyrirliggjandi sjálfgefinni skýrslu. Þú stofnar skipurit og bætir við skýrsluskilgreining til að framleiða Kostnaðarstað/rekstrarreikning eftir deildum. Eftir að uppfærslum er lokið myndarðu Kostnaðarstað/rekstrarreikning eftir deildum og athugar skýrsluna með skipuritinu. Við byrjum í lista yfir fjárhagsskýrslur.

1. Fara í **Fjárhagsskýrslur** undir Fyrirspurnir og skýrslur í fjárhag.
2. Velja línuna fyrir skýrslu sem ber heitið **Rekstrarreikningur - sjálfgefinn**.
3. Veljið **Breyta**. **Rekstrarreikningur – Sjálfgefin** opnar í skýrsluhönnun.
4. Í valmyndinni **Skrá** er bent á **Nýtt** og síðan smellt á **Skilgreining skipurits**.
5. Á valmyndinni **Breyta** er smellt á **Setja inn einingar skipurits úr víddum**.
6. Hreinsið gátreitina fyrir allar víddir, nema **Kostnaðarstað**.
7. Smellið á reitinn **Úr Vídd** fyrir Vídd kostnaðarstaðar, sláið inn **007**, og styðið á Tab-lykilinn. Í reitinn **Til víddar** skal slá inn **018**.
8. **Vistaðu** meðfylgjandi skipurit með heitinu **Kostnaðarstaðir eftir deild.** Nú þegar skipuritið hefur verið stofnað breytirðu því svo að það innihaldi þrjár nýjar samamntektareiningar; Markaðssetningu, Aðgerðir og Smásölu.
9. Í valmyndinni **Gluggi** smellirðu á **Kostnaðarstaðir eftir deild**. (Ef skipuritnu hefur verið lokað þarf að velja það úr skilgreiningum skipurits í yfirlitssvæðinu.)
10. Smellið á einingu númer tvö, **Sölusýningar**, og smellið á táknið **Setja inn einingu skipurits**.
11. Tvísmelltu á einindadálkinn í auðu línunni og veldu **USMF**.
12. Sláðu inn **Markaðssetningar** í dálka B og C.
13. Smellt er á einingu númer fimm, **Þjónustuaðgerðir**, og hægrismellt. **Veldu Setja inn einingu skipurits**
14. Endurtakið skref 11.
15. Sláðu inn **Aðgerðir** í dálka B og C.
16. Smellt er á einingu númer tólf, **Verslun**, og hægrismellt. Veldu **Setja inn einingu skipurits**.
17. Endurtakið skref 11.
18. Sláðu inn **Retail** í dálka B og C. Athugaðu að einingar Markaðssetningar, Aðgerða og Smásölu birtast á sama stigi og gildandi samantekt eininga. Næst er nýjum einingum raðað. Einingar skipurits eru skipulagðar með hægrismelltum valkostum; færa upp og færa niður, eða með því að draga og sleppa.
19. Staðfesta einingu þrjú, **Sölusýningar**, er virk og hægrismella.
20. Veldu **Lækka einingu skipurits**. Athugið að einingin birtist núna sem undirhnútur **Markaðssetningar**.
21. Smellt er á einingu fjögur, **Markaðssetningar Herferð**, og hægrismella.
22. Veldu **Lækka einingu skipurits**.
23. Smellið á **Þjónustuaðgerðir** í myndræna framsetningu. Stutt er á og haldið niðri vinstri músarhnappi á meðan einingin er dregin í **Aðgerðir**. Slepptu vinstri músarhnappnum til að fella eininguna í samantekt Aðgerðarinnar. Endurtakið fyrir **Framleiðslu, Gæðaeftirlit, Vörustjórnun, Innkaupa- og Stjórnun**.
24. Gerðu **Verslun**, **Yfir**, **Verslunarkjarni**, og **Á netinu** að undirhlutum **Smásölu** með því að annaðhvort hækka þá eða eða sleppa þeim.
25. Vistaðu endurskipulagninguna. Nú þegar við höfum stofnað skipuritið og skipulagt það er hægt að bæta því við skýrsluskilgreininguna.
26. Í valmyndinni **Gluggi** velurðu **Rekstrarreikningur – Sjálfgefin** til að opna skýrsluskilgreininguna.
27. Smellið á felliörina **Gerð trés** og veljið **Skipurit**.
28. Smellið á felliörina Gerð trés og veljið **Kostnaðarstaðir eftir deildum**.
29. Breyta grunnárinu í **2012**, **vista** breytingar og **mynda** skýrsluna. Þegar skýrslan lýkur myndun og opnast er hægt að skoðið skýrsluna.
30. Veldu fellilistann **Skipurit** til að skoða einingar skipurits. Einnig er hægt að kafa niður í röð skýrslu til að sjá allar stöður fyrir allar einingar skipurits.
31. Lokaðu **Rekstrarreikningur – Sjálfgefin**.
32. Lokaðu **Skýrsluhönnuninni**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>Æfing 4: Stofna uppsöfnuð skýrslu með stigveldi fyrirtækis
Í þessari æfingu breytirðu fyrirliggjandi sjálfgefinni skýrslu. Þú bætir stigveldi fyrirtækis við í skýrsluskilgreiningu til að framleiða sameinaðan rekstrarreikning og efnahagsreikning. Eftir að uppfærslu er lokið myndarðu sameinaða skýrslu og athugar hana með skipuritinu. Við byrjum í lista yfir fjárhagsskýrslur.

1. Fara í **Fjárhagsskýrslur** undir Fyrirspurnir og skýrslur í fjárhag.
2. Veldu línuna fyrir skýrslu sem ber heitið **Efnahagsreikningur og rekstrarreikningur hlið við hlið – Sjálfgefin**.
3. Veljið **Breyta**. **Efnahagsreikningur og rekstrarreikningur hlið við hlið – Sjálfgefin** opnar í skýrsluhönnun.
4. Velja **Skrá** &gt; **Vista Sem** og heiti skýrslu **Sameinaðir Efnahagsreikningar og rekstrarreikningar hlið við hlið**.
5. Breyta grunnárinu í 2012.
6. Smellið á felliörina Gerð trés og veljið **Stigveldi fyrirtækis**.
7. Smellið á felliör Trés og veljið **Contoso Holdings**.
8. Vistaðu breytingarnar og myndaðu skýrsluna. Ef beðið er um velurðu allar einingar skipurits. Þegar skýrslan lýkur myndun og opnast er hægt að skoðið skýrsluna.
9. Veldu **Skýrsluvalkosti**.
10. Veldu **Bæta við víddarafmörkun** og veldu **Deild**.
11. Sláðu **022** inn í reitinn og veldu **í lagi**.
12. Loka síaðri skýrslu.
13. Veldu fellilistann **Skipurit** til að skoða einingar skipurits. Einnig er hægt að kafa niður í röð skýrslu til að sjá allar stöður fyrir allar einingar skipurits.
14. Lokaðu **Sameinaðir efnahagsreikningar og rekstrarreikningar hlið við hlið**.
15. Lokaðu **Skýrsluhönnuninni**.

## <a name="exercise-5-create-a-side-by-side-departmental-report"></a>Æfing 5: Stofna hlið við hlið deildarskýrslu
Í þessari æfingu býrð þú til nýja skýrslu. Skýrslan er hlið við hlið deildarrekstrarreikningur. Þú munt nota línuskilgreiningu en stofna nýja skýrsluskilgreiningu og nýja dálkskilgreiningu sem notar víddarafmarkanir. Við byrjum í lista yfir fjárhagsskýrslur.

1. Fara í **Fjárhagsskýrslur** undir Fyrirspurnir og skýrslur í fjárhag.
2. Velja **Nýja**. Hönnunarviðmót opnar með auða skýrsluskilgreiningu opna. Fyrsta verkefni þitt verður stofnun á dálkskilgreiningu.
3. Stofnaðu nýja dálkskilgreiningu með því að smella **Skrá**, síðan **Nýtt** og síðan **Dálkskilgreining**.
4. Í **Dálki A**, velja **DESC** fyrir gerð dálks.
5. Í **Dálki B**, velja **FD** fyrir gerð dálks.
6. Tvísmelltu í reitinn **Víddarafmörkun**.
7. Í glugganum **Vídd** tvísmellirðu á dálkinn **Deild**.
8. Í Einstaka eða afmörkun hluta svarglugganum, smellið á **úrfellingarmerkið** svo að reiturinn **Úr** birti lista yfir deildir.
9. Velja deild **022**, **Sala og markaðssetning** og smellið síðan á **í lagi**.
10. Endurtaka skal þrep 5 til 8 fyrir deildir 23-25.
11. Í línu **Haus 2** fyrir hvern FD-dálk skal slá inn eftirfarandi deildalýsingar:

    - Dálkur B – Sala og markaðssetning
    - Dálkur C – Aðgerðir
    - Dálkur D – Fjárhagur
    - Dálkur E – Upplýsingatækni

12. Vistaðu dálkskilgreiningu sem deildir hlið við hlið. Þar sem við notum fyrirliggjandi línuskilgreiningu er nú hægt að breyta skýrsluskilgreiningunni svo að hún noti nýstofnaða dálkskilgreiningu og fyrirliggjandi línuskilgreiningu.
13. Í valmyndinni **Gluggi** velurðu **Ný skýrsluskilgreining** til að opna skýrsluskilgreininguna.
14. Velja **Rekstrarreikningur – Sjálfgefin** sem línuskilgreiningu og **Hlið við Hlið Deildir** sem skilgreining dálks.
15. Vistaðu skýrsluskilgreininguna sem **Hlið við hlið rekstrarreikningur eftir deildum**.
16. Breyta grunnárinu í **2012**.
17. Breyta upplýsingastigi í **Fjárhagur, reikningur og færsla**.
18. **Vista** breytingarnar og **mynda**. Eftir að skýrslan lýkur myndun og opnast er hægt að skoða skýrsluna.

## <a name="additional-resources"></a>Frekari upplýsingar
[Fjárhagsskýrslugerð](../../../finance/general-ledger/financial-reporting-getting-started.md)

[Skoða fjárhagsskýrslur](../../../finance/general-ledger/view-financial-reports.md)

[Dynamics 365 Finance-blogg](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
