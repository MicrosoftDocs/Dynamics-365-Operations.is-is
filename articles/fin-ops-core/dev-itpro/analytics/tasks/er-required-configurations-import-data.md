---
title: Rafræn skýrslugerð Stofna nauðsynlegt grunnstillingar til að flytja inn gögn úr ytri skrá
description: Í þessari grein er útskýrt hvernig á að hanna skilgreiningar rafrænnar skýrslugerðar til að flytja gögn inn í Microsoft Dynamics 365 Finance-forritið úr ytri skrá.
author: kfend
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
ms.openlocfilehash: 199873af83ec14d441aa3927dc84509486e4927a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290155"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>Rafræn skýrslugerð Stofna nauðsynlegt grunnstillingar til að flytja inn gögn úr ytri skrá

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur sett upp grunnstillingar fyrir Rafræn skýrslugerð til að flytja inn gögn í Microsoft-forritið úr ytri skrá. Í þessu dæmi mun stofna nauðsynlega grunnstillingu Rafræn skýrslugerð fyrir dæmi um fyrirtæki, Litware, Inc. Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Stofna grunnstillingarveitu í Rafræna skýrslugerð og merkja hana sem virka”. Skrefin er hægt að klára með því að nota USMF gagnasafnið. Þú verður líka að hlaða niður og vista eftirfarandi skrár staðbundið: 

| Lýsing á efni                       | Skrárnafn                                     |
|-------------------------------------------|-----------------------------------------------|
| Skilgreining á gagnalíkani í ER - 1099 | [1099model,xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)                  |
| Skilgreining fyrir snið rafrænnar skýrslugerðar - 1099    | [1099format.xml](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)                  |
| Sýnishorn af skjali á innleið á XML-sniði                          | [1099entries.xml](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)        |
| Sýnishorn af vinnubók til að stýra gögnum skjala á innleið                          | [1099entries.xlsx](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx) |

Rafræn skýrslugerð býður notendum í viðskiptum upp á að geta grunnstillt innflutningsferli á ytri gagnaskjölum í töflur, annaðhvort í .XML eða .TXT sniði. Fyrst verður að setja upp grunnstilling óhlutbundins gagnalíkans og gagnalíkan fyrir Rafræn skýrslugerð, til að standa fyrir gögnin sem flutt eru inn. Næst þarf að skilgreina uppbygging skráarinnar sem flutt er inn og aðferð sem nota til að tengja gögnin úr skránni í óhlutbundið gagnalíkan. Grunnstilling á sniði Rafræn skýrslugerðar sem varpar í uppsett gagnalíkan verður að vera stofnað fyrir þetta óhlutbundið gagnalíkan. Síðan þarf að víkka út grunnstillingu gagnalíkans með vörpun sem lýsir því hvernig innflutt gögn er haldið áfram sem óhlutbundið gögn í gagnalíkani og hvernig notað til að uppfæra töflur.  Grunnstilling gagnalíkans Rafræn skýrslugerðar verður að fylgja ný líkansvörpun sem lýsir bindingu gagnalíkans við áfangastaði forrits.  

Eftirfarandi sviðsmynd sýnir innflutningsmöguleika gagna í Rafræn skýrslugerð. Þetta inniheldur lánardrottnafærslur sem eru raktar ytra og svo flutt inn til að koma síðar í skýrslu í uppgjör lánardrottins fyrir 1099.   

## <a name="add-a-new-er-model-configuration"></a>Bæta við nýrri grunnstillingu líkans í Rafræn skýrslugerð
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.

    Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, „Litware, Inc.“ sé tiltæk og merkt Virk. Ef ekki sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.   

2. Smelltu á Grunnstillingar skýrslugerðar

    Í stað þess að stofna nýtt líkan til að styðja innflutningur gagna, skal hlaða skrá 1099model.xml, sem áður var sótt. Þessi skrá inniheldur sérstillt gagnalíkan yfir færslur lánardrottins. Þetta gagnalíkan er varpað í gagnahluti sem eru í gagnaeiningu AOT.   

3. Smellt er á Skipta út.
4. Smellt er á Hlaða úr XML-skrá.

    Smellt er á Fletta og flett á skrána 1099model.xml sem áður var sótt.  

5. Smellið á „Í lagi“.
6. Í tré skal velja '1099 Greiðslulíkan'.

## <a name="review-data-model-settings"></a>Fara yfir stillingar gagnalíkans
1. Smellið á Hönnuður.

    Þetta líkan er sett upp til að standa fyrir færslur lánardrottins frá viðskiptasjónarmiði og eru aðskildar uppsetningu.   

2. Í trénu skal víkka út '1099-MISC'.
3. Í tré skal velja '1099-MISC\Transactions'.
4. Í trénu skal víkka út '1099-MISC\Transactions'.

    Færslueiningin í þessu líkani stendur fyrir stakar færslur. Undireiningar eru notaðar til að tilgreina nauðsynlegt upplýsingar, t.d. lánardrottnalykil og færsludagsetningu fyrir hverja færslu.   

5. Lokið síðunni.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð sem styður innflutningur gagna
Skrefin í þessu undirverki sýna hvernig stofna má nýja grunnstillingu sniðs til að stjórna gagnainnflutningi úr ytri skrám.   
1. Smellt er á stofna skilgreiningu til að opna fellilistanum.
2. Í svæði Nýtt skal slá inn „Snið byggir á gagnalíkani 1099 Greiðslulíkan“.
3. Velja Já í svæði Styður gagnainnflutning.
4. Ýtt á ESC-lykil til að loka þessari síðu.

    Í stað þess að stofna nýtt snið til að styðja við gagnainnflutning, hlaða skránni 1099format.xml sem áður var sótt. Þessi skrá inniheldur skilgreinda uppbygging skráar sem flutt er inn og vörpun á uppbyggingu sérstillt gagnalíkan yfir færslur lánardrottins.   
5. Smellt er á Skipta út.
6. Smellt er á Hlaða úr XML-skrá.
    Smellt er á Fletta og flett á skrána 1099format.xml sem áður var sótt.  
7. Smellið á „Í lagi“.
8. Í trénu skal víkka út ‚1099 Greiðslulíkan'.
9. Í tré skal velja '1099 Greiðslulíkan\Snið til að flytja inn færslur lánardrottna'.

## <a name="review-format-settings"></a>Fara yfir stillingar sniðs
1. Smellið á Hönnuður.
2. Kveikið á „Sýna upplýsingar“.
3. Smellt er á Víkka/draga saman.
4. Smellt er á Víkka/draga saman.

    Uppsetta sniðið stendur fyrir væntanlegt uppbygging fyrir ytri skrá. Þessi skrá verður að vera á XML-sniði og vera með rótareininguna uppgjör. Hver færsla lánardrottins er kynnt af færslueiningu sem er skilgreind sem núll-til-margar margfeldni. Þetta þýðir að skrá á innleið getur innihaldið allt frá núll til margar færslur. Faldaðar einingar „færslueiningarinnar“ standa fyrir eigindir stakrar færslu. Athugið að allar eigindir, nema land, eru merktur sem skyldubundinn, sem þýðir að þær verða að vera í innflutningsskránni.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Fara yfir stillingar í vörpun sniðs í gagnalíkan
1. Smellt er á Varpa sniði á líkan.

    Vörpunin „Fyrir lánardrottna í innflutningi“ færslur inniheldur gagnaflutningsreglur úr XML-skrá á innleið, í valinn hluta af sérstilltu gagnalíkani, sem er skilgreint með því að velja skilgreininguna 1099-MISC.  

2. Smellið á Hönnuður.
3. Kveikið á „Sýna upplýsingar“.
4. Í trénu skal víkka út „snið: Færsla“.
5. Í trénu skal velja „snið: Færsla“.

    Athugið að uppsett snið er sett hér fram sem íhlutur gagnaveitu.  

6. Í trénu skal víkka út „`format: Record\*settlement: XML Element 1..1 (settlement): Record`“.
7. Í trénu skal víkka út „`format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list`“.
8. Í trénu skal víkka út „`format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`“.
9. Í trénu skal víkka út „`format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record`“.
10. Í trénu skal velja „`format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`“.

    Athugið að kynning á skyldubundnum og valkvæmum einingum sniðs er ólík í fyrirframskilgreindur íhlutur gagnaveitu „sniðs“.  
11. Í trénu skal víkka út „Færslur: Skráningalisti= format.settlement.'$enumerated''.

    Athugið að einingar sniðsins sem skilgreinir uppbyggingu innfluttrar skrár eru festar við einingar í sérstilltu gagnalíkani. Út frá þessum bindingum verður innihald þessara innfluttu XML-skráa vistað í keyrslutíma í fyrirliggjandi gagnalíkani. Athugið sérstaklega bindingu landseiningarinnar. Fyrir hverja færslueiningu í skrá á innleið sem ekki er með slíka einingu verður fyllt út í gagnalíkan með sjálfgefinn landskóði „USA“.  

12. Smellt er á flipann Sannprófanir.

    Þessi vörpun sniðs gæti innihaldið notandaskilgreindar reglur til að sannprófa nákvæmni innfluttra gagna út frá viðskiptasjónarmiði. Til dæmis, út frá stillingu, fyrir hverja færslu í innfluttri skrá án skilgreinds landskóða, munu myndast viðvörunarboð í upplýsingaskránni sem láta notandi vita um málið og vísar á númeraröð færslu.  

13. Lokið síðunni.

## <a name="run-the-format-mapping-to-the-data-model"></a>Keyra vörpun sniðs í gagnalíkan
Framkvæmið þessar vörpun sniðs til prófunar. Notið skrána 1099entries.xml sem áður var sótt. Hægt er að flytja út þessa skrá úr vinnubókinni 1099entries.xml sem er notuð til að vinna með lánardrottnafærslur. Myndað úttak verður flutt inn úr valinni XML-skrá og fyllir út sérstillt gagnalíkan í rauninnflutningi.  

1. Smellið á „Keyra“.

    Smellt er á Fletta og flett á skrána 1099entries.xml sem áður var sótt.  

2. Smellið á „Í lagi“.

    Athugið viðvörunarboðin um landskóða sem vantar í færslu í innfluttri skrá.  
    
    Farið yfir úttak í XML-sniði, sem stendur fyrir gögn sem hafa verið innflutt úr valinni skrá og tengd við gagnalíkan.   

3. Lokið síðunni.
4. Lokið síðunni.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Fara yfir stillingar fyrir vörpun líkans í áfangastaði
1. Í tré skal velja '1099 Greiðslulíkan'.
2. Smellið á Hönnuður.
3. Smellt er á Varpa líkani á gagnagjafa.

    Vörpun fyrir 1099 handvirkan innflutning færslur hefur verið skilgreind með áttargerðinni „Á áfangastað“. Þetta merkir að hún hefur verið slegin inn til að styðja við gagnainnflutning og inniheldur reglusafn sem skilgreinir hvernig innflutt ytri skrá og gögn úr viðhaldinni óhlutbundinni gagnalíkani er notað til að uppfæra töflur í forritinu.  

4. Smellið á Hönnuður.
5. Í trénu skal víkka út ‚líkan: Gagnalíkan 1099 Greiðslulíkan'.
6. Í trénu skal víkka út ‚líkan: Gagnalíkan 1099 Greiðslulíkan\Færslur: Skráningarlisti'.

    Athugið að uppsett líkan er sett hér fram sem eining gagnaveitu. Við keyrslu mun hún innihalda gögn sem eru innflutt úr ytri skrá. Nokkrum töflum var bætt við sem gagnaveitueiningum til að tryggja að innflutt gögn uppfylli kröfur gagna úr núgildandi forriti, þar með talinn hvort lánardrottnalykill fyrir innflutningsfærslu er tiltækur í kerfinu, hvort samsetning innflutningsland og ríkjakóða er til og svo framvegis.  

7. Í trénu skal víkka út ‚líkan: Gagnalíkan 1099 Greiðslulíkan\Færslur: Skráningarlisti\$failed: Útreiknaður reitur = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean'.
8. Smellið á „Breyta“.
9. Smellt er á Breyta formúla.

    Þegar a.m.k. ein prófun virkar ekki fyrir staka innflutta færslu er þessi færsla merkt sem misheppnuð með eigind gagnaveitu „$failed”.  

10. Lokið síðunni.
11. Smellið á Hætta við.
12. Í trénu skal velja 'tax1099trans: Tafla 'VendSettlementTax1099' skráningar= model.Validated'.
13. Smellt er á Breyta áfangastað.

    Áfangastaður Rafræn skýrslugerð var bætt við til að tilgreina hvernig innflutt gögn uppfæra töflur forrits. Í þessu tilviki hefur gagnatafla VendSettlementTax1099 verið valin. Vegna þess að færsluaðgerðin Setja inn hefur verið valin verða innfluttar færslur settar inn í töfluna VendSettlementTax1099. Athugið að stök vörpun líkans getur innihaldið marga áfangastaður. Þetta merkir að innflutt gögn er hægt að nota til að uppfæra margar töflur í forriti í einu. Töflur, yfirlit og gagnaeiningar er hægt að nota sem áfangastaði Rafræn skýrslugerð.   

    Ef beðið er um vörpun úr stað í forritinu (t.d. hnappur eða valmyndaratriði) sem var sérstillur fyrir þessa aðgerð, ætti að merkja áfangastaður í Rafræn skýrslugerð sem samþættingarstað. Í þessu dæmi er ERTableDestination#VendSettlementTax1099 þessi staður.  

14. Smellið á Hætta við.
15. Smellt er á Sýna allt.
16. Smellt er á Sýna aðeins varpað.
17. Í trénu skal víkka 'tax1099trans: Tafla 'VendSettlementTax1099' skráningar= model.Validated'.

    Athugið að gagnaveitueiningin sem inniheldur einu sannprófuðu færsluna er bundin við stofnaðan áfangastað. Hægt er að sía innfluttar færslur til að sleppa þeim sem ekki passa við gögn forrits.  

18. Í trénu skal velja ‚mistókst: Tafla 'VendSettlementTax1099Entity' skráningar= model.Failed'.
19. Smellt er á flipann Sannprófanir.

    Þessi vörpun líkans gæti innihaldið notandaskilgreindar reglur til að sannprófa réttleika innfluttra gagna út frá fyrirliggjandi forritsgögnum. Til dæmis, út frá núgildandi stillingu, fyrir hverja færslu í innfluttri skrá með lánardrottnalykil sem ekki er í kerfinu, munu myndast viðvörunarboð í upplýsingaskránni sem láta notandi vita um málið og vísar á ranga lánardrottnalykilinn.  

    Athugið að valkostur Bóka sannprófun aðgerðar er hægt að nota fyrir hverja sannprófun, til að tilgreina hvort halda verður áfram með innflutningsferli eða stöðva það, auk þess að hvort hægt er að halda áfram innskoti/uppfærslum eða hætta við það.  

20. Smellt er á Sýna aðeins varpað.
21. Smellt er á Sýna allt.
22. Lokið síðunni.

    Framkvæma þessa vörpun líkans til að prófa uppsett snið og vörpun líkana. Nota skrána 1099entries.xml. Gögnin úr valinni skrá verða flutt inn í kerfi.  

23. Smellið á „Keyra“.

    Athugið að svargluggi inniheldur engar viðbótarspurningar um vörpun sniðs sem verður að nota til að þátta innflutt skrá og svo tengja gögn við gagnalíkan. Ástæðan er sú að nú er aðeins eitt snið sem notar þetta líkan, sem er merkt sem uppsett til að styðja gagnainnflutning.  
    
    Skilgreina auðkenni afsláttarmiði til að skilja innfluttar færslur frá öðrum færsla sem er kannski búið að slá inn handvirkur eða flytja inn.  

24. Í svæði Slá inn auðkenni afsláttarmiða, skal slá inn 'IMPORT-001'.

    Fletta og finna skrána '1099entries.xml'.  

25. Smellið á „Í lagi“.

    Listi yfir myndaðar viðvaranir skilar upplýsingar um rangar lánardrottnalykla, rangan hólfakóða skatts fyrir 1099, landskóða sem vantar og svo framvegis. Berið þennan lista yfir viðvaranir saman við efni sem er í framkvæmdar XML-skrá.  

26. Lokið síðunni.
27. Lokið síðunni.
28. Lokið síðunni.
29. Lokið síðunni.
30. Fara í Viðskiptaskuldir > Reglubundin verkefni > Skattur 1099 > Uppgjör lánardrottins fyrir 1099.

    Þetta eyðublað sýnir uppsafnaður færslur í töflunni Tax1099Summary sem hafa verið stofnaðar út frá innfluttum færslum.  

31. Í svæði Frá-dagsetningu, stilla á dagsetningu ' 2000-01-01 ".
32. Smellt er á Handvirkar 1099-færslur.

    Þessi skjámynd inniheldur lista yfir færslur sem var bætt handvirkur við og þær sem voru innfluttar.  

33. Opnið dálkasíuna Afsláttarmiði.
34. Sláið inn síugildið „IMPORT-001“ í svæðið „Afsláttarmiði“ og notið virknitáknið „byrjar á“ í síu.

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Fara yfir tengsl á milli varpana líkans og sniðs
1. Lokið síðunni.
2. Lokið síðunni.
3. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
4. Smelltu á Grunnstillingar skýrslugerðar
5. Í tré skal velja '1099 Greiðslulíkan'.

    Segjum að vilja styðja við innflutningur á sömu gögn en úr .TXT-skráarsnið.   

6. Smellt er á Stofna skilgreiningu til að opna svargluggi. 
7. Í svæði Nýtt skal slá inn „Snið byggir á gagnalíkani 1099 Greiðslulíkan“.
8. Í reitinn Heiti skal slá inn „Flytja inn gögn úr TXT-skrá“.
9. Velja Já í svæði Styður gagnainnflutning.
10. Smelltu á Stofna skilgreiningu.
11. Smellið á Hönnuður.
12. Smellt er á Varpa sniði á líkan.
13. Smellið á „Nýtt“.
14. Sláið inn eða veldu gildi í reitnum skilgreining.

    Veljið valkostur '1099-MISC'.  

15. Í reitinn Heiti skal slá inn „Flytja inn gögn úr TXT-skrá“.
16. Í reitinn Lýsing skal slá inn „Flytja inn gögn úr TXT-skrá“.
17. Smellið á „Vista“.
18. Lokið síðunni.
19. Lokið síðunni.
20. Smella á Breyta.

    Ef bráðabótin „KB 4012871 Stuðningur fyrir GER líkanavörpun í aðskildum grunnstillingum með getu til að tilgreina ólíkar gerðir af frumskilyrðum til að nota þær á ólíkar gerðir af Dynamics 365 Finance „ ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), skal framkvæma næsta skref „Kveikja á flagginu „Sjálfgefið fyrir líkanavörpun““ fyrir grunnstillingu sniðs sem slegin inn. Annars skal sleppa næsta skrefi.  

21. Veljið Já í reitnum „Sjálfgefið fyrir líkanavörpun“.
22. Í tré skal velja '1099 Greiðslulíkan'.
23. Smellið á Hönnuður.
24. Smellt er á Varpa líkani á gagnagjafa.
25. Smellið á „Keyra“.

    Ef bráðabótin „KB 4012871 Stuðningur fyrir GER líkanavörpun í aðskildum grunnstillingum með getu til að tilgreina ólíkar gerðir af frumskilyrðum til að nota þær á ólíkar gerðir af ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), skal velja æskilegt vörpun líkans í uppflettingarreitnum. Ef bráðabótin hefur ekki verið sett upp, sleppa næsta skrefi þar sem vörpun hefur þegar verið falin af skilgreiningu á sjálfgefið grunnstilling sniðs.  
    
    Ef bráðabótin KB 4012871 hefur ekki verið sett upp, athugið að svargluggi inniheldur viðbótarspurningu um vörpun líkans sem er notuð til að þátta skrána sem er flutt inn. Gögnin eru síðan tengd úr svarglugga í gagnalíkan. Sem stendur er hægt að velja hvaða vörpun sniðs verður að nota út frá gerð skráar sem ætlunin er að flytja inn.  
    
    Ef ætlunin er að kalla á þessa vörpun líkans úr stað í forritinu sem er sérstilltur fyrir aðgerðina, verður að merkja áfangastað í Rafræn skýrslugerð og vörpun líkans sem hluta af samþættingunni.  

26. Smellið á Hætta við.
27. Lokið síðunni.
28. Lokið síðunni.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
