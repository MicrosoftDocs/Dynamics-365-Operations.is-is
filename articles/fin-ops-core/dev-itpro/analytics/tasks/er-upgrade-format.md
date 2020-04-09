---
title: Rafræn skýrslugerð Uppfærðu snið með því að taka upp nýja grunnútgáfu sniðs
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur viðhaldið skilgreiningarsnið fyrir rafræna skýrslugerð (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52bc276a4a88971a7214fa09087cb1323b91aaf5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143275"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a>Rafræn skýrslugerð Uppfærðu snið með því að taka upp nýja grunnútgáfu sniðs

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur viðhaldið skilgreiningarsnið fyrir rafræna skýrslugerð (ER). Þetta ferli útskýrir hvernig sérsniðin útgáfu sniðs er hægt að mynda á grundvelli snið móttekið frá veitandi skilgreiningar (CP). Það útskýrir einnig hvernig eigi að taka upp nýja grunnútgáfu af því sniði.

Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlunum „Stofna skilgreiningarveitu og merkja hana sem virka” og „Nota stofnuð snið til að mynda rafræn skjöl fyrir greiðslur”. Hægt er að framkvæma þessum skrefum í GBSI fyrirtækinu.

## <a name="select-format-configuration-for-customization"></a>Veljið skilgreiningu sniðs fyrir sérsnið
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.

    Í þessu dæmi mun sýnifyrirtækið Litware, Inc. (https://www.litware.com) vinna sem skilgreiningarveita sem styður skilgreiningarsnið fyrir rafrænar greiðslur fyrir tiltekið land.    Sýnifyrirtæki Proseware, Inc. (http://www.proseware.com) mun vinna sem neytandi skilgreiningarsniðs sem Litware, Inc. útvegaði. Proseware, Inc. motar snið í sumum svæðum þess lands.  
2. Smelltu á Grunnstillingar skýrslugerðar
3. Smellt er á Sýna síur.
4. Notið eftirfarandi síur: færðu inn síugildi „UK sérsniðið upphugsað” á svæði „Heiti" með því að nota síuvirknitáknið „byrjar á”.
  
    Valið skilgreiningarsnið (UK sérsniðið upphugsað) BACS, er í eigu Litware, Inc.  

5. Smellt er á Sýna síur.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

    Útgáfa sniðs með stöðuna Lokið mun verða notað af Proseware, Inc. fyrir sérstillingu.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Stofna nýja skilgreiningu fyrir sérsniðið snið rafrænna skjala
Proseware, Inc. hefur móttekið útgáfa 1.1 fyrir skilgreiningar BACS (UK upphugsað) sem inniheldur upphaflegt snið til að mynda rafræn greiðsluskjöl úr Litware, Inc. í samræmi við þjónustuáskrift þeirra. Proseware, Inc. vill byrja að nota þetta sem staðal fyrir þeirra land en nokkur sérstillingar er krafist til að styðja sérstakar svæðisbundið kröfur. Proseware, Inc. villl einnig halda getunni til að uppfæra sérsniðnir snið um leið og ný útgáfu þess (með breytingum til að styðja við landsbundnar þarfir) kemur út hjá Litware, Inc. og það vill framkvæma þessa uppfærslu með sem minnstum tilkostnaði.  

Til að gera þetta þarf Proseware, Inc. að stofna skilgreiningu með því að nota Litware, Inc. skilgreininguna BACS (UK upphugsað) sem grunn.  

1. Lokið síðunni.
2. Veljið Proseware, Inc. til að gera hana að virkri veitu.
3. Smellt á Stilla sem virkt.
4. Smelltu á Grunnstillingar skýrslugerðar
5. Stækkið „Greiðslur (EINFÖLDUN líkan)“ í trénu.
6. Í trénu, veljið 'Payments (einfaldað líkan)\BACS (UK upphugsað)'.

    Velja skilgreiningu BACS (Bretland upphugsað) úr Litware, Inc. Proseware, Inc. mun nota útgáfu 1.1 sem grunn fyrir sérsniðnu útgáfuna.  

7. Smellt er á stofna skilgreiningu til að opna fellilistanum.

    Þetta gerir mögulegt að stofna nýja skilgreiningu fyrir sérsniðna greiðslusnið.  

8. Í svæðinu Nýtt, veljið 'Leiða af nafni: BACS (UK upphugsað), Litware, Inc'.

    Veljið valkost afleiddur til að staðfesta notkun BACS (UK upphugsað) sem grunn til að stofna sérsniðna útgáfu.  

9. Í reitinn Heiti skal slá inn 'BACS (UK upphugsað sérsniðið)'.
10. Færið inn 'BACS greiðsla lánardrottins (UK sérsniðið upphugsað)' í svæðinu Lýsingu.

    Virkt skilgreiningarveitu (Proseware, Inc) er sjálfkrafa færð inn hér. Þessa veitu mun geta unnið með þessa skilgreiningu. Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.  

11. Smelltu á Stofna skilgreiningu.

## <a name="customize-your-format-for-the-electronic-document"></a>Sérsníða snið fyrir rafrænt skjal
1. Smellið á Hönnuður.
2. Smellt er á Víkka/draga saman.
3. Smellt er á Víkka/draga saman.
4. Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank'.
5. Smelltu á Bæta við til að opna felligluggann.
6. Í trénu skal velja „XML/Element“.
7. Í svæðið Heiti, færðu inn ‚IBAN-númer'.
8. Smellt er á Í lagi.
9. Í tré skal velja 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.
10. Smelltu á Bæta við til að opna felligluggann.
11. Í trénu skal velja ‚Texti/Strengur'.
12. Smellt er á Í lagi.
13. Í tré skal velja 'Xml\Message\Payments\Item\Vendor\Name\String'.
14. Í reitinn hámarkslengd skal slá inn 60.
15. Smelltu á flipann Vörpun.
16. Í trénu skal víkka út 'model'.
17. Í trénu skal víkka út 'model\Payments'.
18. Útvíkka 'model\Payments\Creditor', í trénu.
19. Útvíkka 'model\Payments\Creditor\Account', í trénu.
20. Í tré skal velja 'model\Payments\Creditor\Account\IBAN'.
21. Í tré skal velja 'Xml\Message\Payments\Item = model.Payments\Vendor\Bank\IBAN\String'.
22. Smelltu á Binda.
23. Smellið á „Vista“.

## <a name="validate-the-customized-format"></a>Villuleita sérsniðna snið
1. Smella á Villuleita.

    Villuleita sérsniðna útlit sniðs og breytingar gagnakortalagning til að tryggja að allar bindingar eru í lagi.  

2. Lokið síðunni.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>Breyta stöðu núgildandi útgáfa grunnstillingar sérstillts sniðs
Breyta stöðu hannaðs skilgreiningarsniðs - úr DRÖG í LOKIÐ til að gera hann tiltækan fyrir myndun greiðsluskjals.  

1. Smellið á „Breyta stöðu“.

    Athugið að núverandi útgáfa valinnar skilgreiningar er í stöðunni DRÖG.  

2. Smelltu á Ljúka.
3. Sláið inn gildi í reitnum „Lýsing“.
4. Smellið á „Í lagi“.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

    Athugið að stofnuð skilgreining er vistuð sem lokin útgáfa 1.1.1. Þetta þýðir að það er útgáfa 1 sérsniðna BACS (UK sérsniðið upphugsað) snið, sem er byggð á sniði útgáfu 1 BACS (Bretland upphugsað), sem er byggð á 1 útgáfa gagnalíkans Greiðslna (einfaldaður líkan).  

## <a name="test-the-customized-format-to-generate-payment-files"></a>Prófa Sérsniðnar snið til að mynda greiðsluskrár
Ljúkið skrefunum í ferlinu „Nota stofnuð snið til að mynda rafræn skjöl fyrir greiðslur” í samhliða lotu Finance and Operations. Velja BACS snið (Bretland sérsniðið upphugsað) í færibreytum rafrænnar greiðslumáta. Gangið úr skugga um að stofnaða greiðsluskráin inniheldur nýlega kynnta XML-hnútnum sem setur fram iban-kóða í samræmi við svæðisbundið þarfir.  

## <a name="update-the-existing-country-specific-configuration"></a>Uppfæra fyrirliggjandi landsbunda skilgreiningu.
Litware, Inc. þarf að uppfæra skilgreiningu BACS (UK upphugsað) og aðlaga nýjar svæðisbundnar kröfur fyrir stjórnun á sniði rafræna skjalið. Síðar, þetta mun vera innan nýja útgáfu þessarar skilgreiningar sem verður í boði fyrir áskrifendur þjónustu, þar á meðal Proseware, Inc.  

Í raunverulegum vinnslum sem tengjast þjónustuveitum, er hægt að flytja inn hverja nýja útgáfa af BACS (UK upphugsað) úr geymslu Litware, Inc. með Proseware, Inc. Í þessu ferli verður líkt eftir þessu með því að uppfæra BACS (UK upphugsað) fyrir hönd þjónustuveitanda.  

1. Lokið síðunni.
2. Velja Litware, Inc. veitu.
3. Smellt á Stilla sem virkt.
4. Smelltu á Grunnstillingar skýrslugerðar
5. Stækkið „Greiðslur (EINFÖLDUN líkan)“ í trénu.
6. Í trénu, veljið 'Payments (einfaldað líkan)\BACS (UK upphugsað)'.

    Útgáfudrögin í eigu Litware, Inc. veita BACS (UK upphugsað) eru valin til að koma með breytingar til að styðja við nýjar svæðisbundnar kröfur.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>Staðfæra grunnsnið rafræna skjalsins.
Gefum okkur til staðar séu nýjar svæðisbundnar þarfir sem Litware, Inc. þarf að styðja:  

- Gildi fyrir SWIFT-kóða banka lánveitanda í hverri greiðslufærslu.
- Takmörkun uppá 100 stafi fyrir lengd textans fyrir nafn lánardrottins í myndunarskránni.  
- Nýjar landsbundnar kröfur  
- Velja útgáfu sem eru drög fyrir skilgreiningu sem óskað er til að kynna til leiks breytingar sem þarf.  


1. Smellið á Hönnuður.
2. Smellt er á Víkka/draga saman.
3. Smellt er á Víkka/draga saman.
4. Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank'.
5. Smelltu á Bæta við til að opna felligluggann.
6. Í trénu skal velja „XML/Element“.
7. Í svæðið Heiti, færðu inn ‚SWIFT'.
8. Smellt er á Í lagi.
9. Í tré skal velja 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.
10. Smelltu á Bæta við til að opna felligluggann.
11. Í trénu skal velja ‚Texti/Strengur'.
12. Smellt er á Í lagi.
13. Í tré skal velja 'Xml\Message\Payments\Item\Vendor\Name\String'.
14. Í reitinn hámarkslengd skal slá inn 100.
15. Smelltu á flipann Vörpun.
16. Í trénu skal víkka út 'model'.
17. Í trénu skal víkka út 'model\Payments'.
18. Útvíkka 'model\Payments\Creditor', í trénu.
19. Útvíkka 'model\Payments\Creditor\Agent', í trénu.
20. Í tré skal velja 'model\Payments\Creditor\Agent\SWIFT'.
21. Í tré skal velja 'Xml\Message\Payments\Item = model.Payments\Vendor\Bank\SWIFT\String'.
22. Smelltu á Binda.
23. Smellið á „Vista“.

## <a name="validate-the-localized-format"></a>Sannprófa staðbundinn snið
1. Smella á Villuleita.
2. Lokið síðunni.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>Breyta stöðu á gildandi útgáfu af grunnskilgreiningarsniði
Breyta stöðu uppfærðs grunns skilgreiningarsniðs - úr DRÖG í LOKIÐ til að gera hann tiltækan fyrir myndun greiðsluskjals og uppfærslur á skilgreiningarsniðum sem fengin eru úr því.  

1. Smellið á „Breyta stöðu“.

    Athugið að núverandi útgáfa valinnar skilgreiningar er í stöðunni DRÖG.  

2. Smelltu á Ljúka.
3. Sláið inn gildi í reitnum „Lýsing“.
4. Smellið á „Í lagi“.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>Breyta Grunnútgáfa fyrir sérsniðna skilgreiningarsnið

Proseware, Inc. er upplýst um að ný útgáfu 1,2 af skilgreiningar BACS (UK upphugsað) er tiltækt til að mynda rafræn greiðsluskjöl í samræmi við til nýlega tilkynntar landsbundnar þarfir. Proseware, Inc. vill byrja að nota það sem staðal fyrir landið.  

Til að svo megi verða þarf Proseware, Inc. að breyta grunnskilgreiningarútgáfa fyrir sérsniðna skilgreiningu BACS (UK upphugsað sérsniðið). Í stað útgáfu 1,1 af BACS (UK upphugsað) skal nota nýjú útgáfuna 1,2.  

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Veldu Proseware, Inc. veitandi til að merkja það sem virkt.
3. Smellt á Stilla sem virkt.
4. Smelltu á Grunnstillingar skýrslugerðar
5. Stækkið „Greiðslur (EINFÖLDUN líkan)“ í trénu.
6. Í trénu, víkka út "greiðslur" (einfaldað líkan)/BACS (UK upphugsað)
7. Í trénu skal velja 'greiðslur (einfaldað líkan)\BACS (UK upphugsað)\BACS (UK upphugsað sérsniðið)'.

    Velja skilgreiningu (Bretland sérsniðið upphugsað) BACS, sem er í eigu Proseware, Inc.  

    Nota útgáfu sem eru drög fyrir skilgreiningu sem valin er til að kynna til leiks breytingar sem þarf.  

8. Smellt er á Endurreikna grunn.

    Veljið nýja útgáfu 1,2 fyrir grunnskilgreiningu til að nota sem nýjan grunn til að uppfæra skilgreininguna.  

9. Smellið á „Í lagi“.

    Athugið að sumar árekstra hafa fundust milli samruna sérsniðnu útgáfunnar og nýja grunnútgáfa sem standa fyrir sumar breytingar sem ekki er hægt að sameina sjálfkrafa.  

## <a name="resolve-rebase-conflicts"></a>Leysa úr Árekstrar við endurreikning grunns
1. Smellið á Hönnuður.
    
    Athugið að breytingar á mörkum á textalengd á heiti lánardrottins var ekki hægt að leysa sjálfkrafa. Þess birtist það í lista yfir árekstra. Fyrir hverja árekstur af gerðinni Uppfærsla eru eftirtaldir valkostir tiltækir:- Nota í fyrra grunngildi (hnappinn yfir hnitanetinu) til að færa í gildi fyrri grunnútgáfa (0 í okkar tilfelli).  - Nota grunngildi (hnappinn yfir hnitanetinu) til að færa í nýtt gildi grunnútgáfu (100 í okkar tilfelli).  - Halda þínu eigin gildi (sérstillt) (60 í okkar tilfelli).  Smellið á Nota grunngildi til að nota landsbundin mörk uppá 100 stafi fyrir textalengd á heiti lánardrottins.  

    Athugaðu að Proseware, Inc. og Litware, Inc. hafa sérsniðnar og staðbundnar útgáfur af þessu sniði og nota IBAN og swift-kóða með tengdar íhluti sem sjálfkrafa eru sameinaðir í stjórnunarsniðið.  

2. Smellt er á Nota grunngildi

    Smellið á Nota grunngildi til að nota landsbundin mörk uppá 100 stafi fyrir heiti lánardrottins.  

3. Smellið á „Vista“.

    Að Vista snið fjarlægir árekstra sem leyst hefur verið úr af listanum yfir árekstra.  

4. Lokið síðunni.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>Breyta stöðu á nýju útgáfu af sérsniðnu skilgreiningarsniði
1. Smellið á „Breyta stöðu“.

    Breyta stöðu uppfærða, sérsniðna skilgreiningarsniðs úr Drög í Lokið. Þetta gerir skilgreiningu sniðs tiltækt fyrir myndun greiðsluskjala. Athugið að núverandi útgáfa valinnar skilgreiningar er í stöðunni DRÖG.  

2. Smelltu á Ljúka.
3. Sláið inn gildi í reitnum „Lýsing“.
4. Smellið á „Í lagi“.

    Athugið að hin stofnaða skilgreining er vistuð sem lokin útgáfa 1.2.2. Útgáfa 2 af grunnsniði BACS (UK sérsniðið upphugsað) snið, sem er byggð á sniði útgáfu 2 BACS (Bretland upphugsað), sem er byggð á 1 útgáfu gagnalíkans Greiðslna (einfaldaður líkan).  

## <a name="test-the-customized-format-for-payment-files-generation"></a>Prófa Sérsniðnar snið til að mynda greiðsluskrár
Ljúkið skrefunum í ferlinu „Nota stofnuð snið til að mynda rafræn skjöl fyrir greiðslur” í samhliða lotu Finance and Operations. Velja hið stofnaða „BACS snið (Bretland sérsniðið upphugsað)” í færibreytum rafrænnar greiðslumáta. Gangið úr skugga um að stofnaða greiðsluskráin innihaldi, nýlega kynnta af Proseware Inc., XML-hnúta sem setur fram IBAN-kóða í samræmi við svæðisbundið þarfir. Skráin ætti einnig að innihalda, nýlega kynnta af Litware, Inc., XML-hnúta sem setur fram SWIFT-kóða í samræmi við svæðisbundið þarfir.  

