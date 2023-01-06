---
title: Endurbæta rakningu niðurstaðna myndaðra rafrænna skýrslna til samanburðar við grunnlínugildi
description: Í þessari grein eru endurbætur á grunnlínueiginleikum rafrænnar skýrslugerðar í Microsoft Dynamics 365 Finance útgáfu 10.0.3 (júní 2019) útskýrðar.
author: kfend
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: d0f64c459ee72ffa2b0e540d4194ca887502780f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279061"
---
# <a name="improve-tracing-the-results-of-generated-er-reports-to-compare-with-baseline-values"></a>Endurbæta rakningu niðurstaðna myndaðra rafrænna skýrslna til samanburðar við grunnlínugildi

[!include[banner](../includes/banner.md)]

Þessi grein fjallar um fyrsta sett endurbóta sem hafa verið gerðar á grunnlínueiginleika á ramma rafrænnar skýrslugerðar (ER). Þessar endurbætur eru fáanlegar í Microsoft Dynamics 365 Finance útgáfu 10.0.3 (júní, 2019) og nýrri.

## <a name="automate-the-setting-of-baseline-rules"></a>Gera skilgreiningu á reglum grunnlína sjálfvirka

Greini [Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md) útskýrir hvernig á að skilgreina ER-ramma til að safna upplýsingum um framkvæmd ER-sniðs og meta niðurstöður þeirra framkvæmda. Dæmið í þessari grein sýnir skrefin sem verður að vera lokið.

Hér eru sum af skrefunum:

- Keyrðu ER-snið til að mynda skrá á útleið og geyma hana staðbundið.
- Bættu staðbundnu skránni við sem viðhengi grunnlínunnar sem var bætt við fyrir ER-snið.
- Skilgreina reglu grunnlínu fyrir viðbætta grunnlínu. Þessi skilgreining inniheldur eftirfarandi skref:

    - Tilgreina þátt ER-sniðs sem er notað til að mynda skrá á útleið.
    - Veldu viðhengið sem vísar til myndaðrar skrár á útleið.

> [!NOTE]
> Þessi skref verður að gera handvirkt, jafnvel þótt nýja ER-getan geri kleift að þau séu sjálfvirk. Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka eftirfarandi dæmi.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Dæmi: Gera skilgreiningu á reglum grunnlína sjálfvirka

Til að ljúka skrefunum í þessu dæmi verður fyrst að ljúka skrefunum í dæminu í greininni [Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md), upp í gegnum kaflann „Bæta við nýrri grunnlínu fyrir uppsett ER-snið“.

### <a name="review-added-baseline"></a>Skoðaðu viðbótargrunnlínu

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Veldu **Grunnlínur**.

    > [!NOTE]
    > Hnappurinn **Grunnlínur** á aðgerðarrúðunni er aðeins í boði þegar kveikt er á ER-notandafæribreytunni **Keyra í kembistillingum** fyrir núverandi fyrirtæki.

Grunnlínugildinu hefur verið bætt við fyrir valið snið **Snið til að læra ER-grunnlínur** en reglum grunnlína hefur ekki enn verið bætt við fyrir þessa grunnlínu.

![Síða grunnlína rafræns skýrslugerðarsniðs, engar reglur enn sem komið er.](media/GER-BaselineSample-AddBaseline2.PNG "Skjámynd af grunnlínusíðuni Rafrænt skýrslugerðarsnið")

### <a name="make-a-new-baseline-rule"></a>Gera nýja grunnlínureglu

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Í trénu stækkarðu **Líkan til að læra ER-grunnlínur**.
3. Í trénu skaltu velja **Líkan til að læra ER-grunnlínur\\Snið til að læra ER-grunnlínur**.
4. Á flýtiflipanum **Útgáfur** velurðu **Keyra**.
5. Í reitnum **Skrá kenni** slærðu inn **1**.
6. Stilltu valkostinn **Gera grunnslínukrár** á **Já**.
7. Veljið **Í lagi**.
8. Veldu **Grunnlínur**.

    ![Síður grunnlína rafræns skýrslugerðarsniðs, grunnlínur valdar.](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Skjámynd af grunnlínusíðuni Rafrænt skýrslugerðarsnið")

    Mynduð skrá á útleið hefur verið sjálfvirkt tengd við grunnlínu framkvæmds ER-sniðs. Grunnlínureglunni hefur verið sjálfkrafa bætt við þessa grunnlínu og inniheldur einnig tilvísun í viðhengda skrá.

9. Í reitinn **Heiti** skal færa inn **Grunnlína 1**.
10. Í reitinn **Sía skráarheiti** slærðu inn **.xml**.
11. Veljið **Vista**.

### <a name="run-the-format"></a>Keyrðu sniðið

Núna ertu tilbúin/n til að klára eftirstandandi skref í dæminu í greininni [Rekja myndaðar skýrsluniðurstöður og beru þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md), byrjaðu á hlutanum „Keyra uppsett ER-snið og endurskoða kladdann til að greina niðurstöðurnar“.

> [!NOTE]
> Þegar þú eyðir sjálfvirkt viðbættri reglu grunnlínu á flipann **Grunnlínur** er tilvísuðu viðhengi ekki sjálfkrafa eytt.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Skilgreina grunnlínuna þannig að hún hunsar stöðugt að breyta hlutum ER-úttaks

Þegar ER-snið hefur verið sett upp til að innihalda upplýsingar sem er breytt þegar sniðið er keyrt, verður sniðið að vera nauðsynlegt til að nota ER-grunnlínueiginleikann til að bera niðurstöðurnar saman við grunnlínugildin. Til dæmis geta upplýsingarnar verið vinnsludagsetning og tími eða einstakt auðkenni myndaðs skjals í mismunandi sniðum (altækt einkvæmt auðkenni \[GUID\], og svo framvegis). Nýja ER-getan gerir þér kleift að skilgreina reglu grunnlínu þannig að hún hunsi breytanlega þætti í ER-sniði þegar sniðið er keyrt með það að markmiði að bera grunnlínugildin saman við niðurstöður á útfærslu sniðsins. Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka eftirfarandi dæmi.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Dæmi: Skilgreina grunnlínuna þannig að hún hunsar stöðugt að breyta hlutum ER-úttaks

Til að ljúka skrefunum í þessu dæmi verður fyrst að ljúka skrefunum í dæminu í greininni [Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md).

### <a name="modify-a-configured-er-format"></a>Breyta skilgreindu ER-sniði

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Í trénu stækkarðu **Líkan til að læra ER-grunnlínur**.
3. Í trénu skaltu velja **Líkan til að læra ER-grunnlínur\\Snið til að læra ER-grunnlínur**.
4. Veljið **Hönnuður**.
5. Í trénu velurðu **Úttak\\Skrá**.
6. Veljið **Bæta við**.
7. Í fellilistanum í trénu velurðu **XML\\Eigind**.
8. Í reitinn **Heiti** slærðu inn **ProcessingDateTime**.
9. Veljið **Í lagi**.
10. Á flipann **Vörpun** í trénu velurðu **Úttak\\Skjal\\ProcessingDateTime**.
11. Veljið **Breyta formúlu**.
12. Í reitnum **Formúla** skráirðu eftirfarandi segð: **DATETIMEFORMAT(NOW(), "O")**
13. Veldu **Vista** og síðan **Prófa**.
14. Veldu **Prófa** aftur til að endurprófa skilgreinda segð.

    ![Síðan Formúluhönnuður.](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Skjámynd af síðunni Formúluhönnuður")

    > [!NOTE]
    > Flipinn **Prófa niðurstöðu** sýnir að skilgreind segð skilar mismunandi dagsetningu og tíma í hvert skipti sem það er kallað.

15. Lokaðu síðunni **Formúluhönnuður** og veldu síðan **Vista**.

    ![Síða sniðshönnuðar.](media/GER-BaselineSample-FormatMappingDesign2.PNG "Skjámynd af síðunni Sniðmátahönnuður")

16. Lokaðu síðunni **Sniðshönnuður**.

### <a name="remove-an-existing-baseline-rule"></a>Fjarlægðu núverandi grunnlínureglu

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Veldu **Grunnlínur**.
3. Í lista yfir grunnlínur skaltu velja grunnlínuna sem er skilgreint fyrir sniðið **Snið til að læra ER-grunnlínur**.
4. Á flýtiflipanum **Grunnlínur** velurðu **Eyða** til að fjarlægja grunnlínuregluna sem þú hefur stillt áður.

![Síða grunnlína rafræns skýrslugerðarsniðs, eytt.](media/GER-BaselineSample-AddBaseline3.PNG "Skjámynd af grunnlínusíðuni Rafrænt skýrslugerðarsnið")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Skilgreindu skipti fyrir bindingu á hönnuðu ER-sniði

1. Á síðunni **Skilgreiningar**, á flýtiflipanum **Endurnýjanir** velurðu **Velja íhluti**.
2. Í íhlutatré sniðmáta víkkarðu út **Úttak**, síðan **Úttak\\Skjal** og velur síðan hakreitinn fyrir **Úttak\\Skjal\\ProcessingDateTime**.
3. Veldu **Í lagi**.

![Síða grunnlína rafræns skýrslugerðarsniðs, íhlutir.](media/GER-BaselineSample-AddBaseline4.PNG "Skjámynd af grunnlínusíðuni Rafrænt skýrslugerðarsnið")

Íhluta valins ER-sniðs hefur verið bætt við lista yfir íhluti á flýtiflipanum **Endurnýjanir**. Þegar ER-grunnsniðið er keyrt í kembiham mun bindingu sniðsins fyrir hvern íhluta verða skipt út fyrir bindinguna sem er sýnd í dálkinum **Binding**. Til að breyta sjálfgefinni bindingu fyrir íhluti sem er skráður á flýtiflipanum **Endurnýjanir** velurðu **Breyta**.

### <a name="make-a-new-baseline-rule"></a>Gera nýja grunnlínureglu

Fylgdu leiðbeiningunum í „Dæmi: Gera skilgreiningu grunnlínureglna sjálfvirka“ sem er fyrr í þessari grein. Tilkynning varar við því að skrá á útleið hafi verið mynduð með því að nota grunnlínustillingar og að þvinguð endurnýjun á bindingum sniðs hafi átt sér stað.

![Tilkynning á skilgreiningasíðunni.](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Skjámynd af tilkynningu á síðunni Skilgreiningar")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Hindraðu viðvaranir um að endurnýjun á bindingum sniðs

Með því að stilla sérstakar ER-breytur er hægt að bæla tilkynningar sem vara við endurnýjun á sniðmátsbindingum. Þessi bæling getur verið gagnleg þegar sniðmátsbindingar eru endurnýjaðar í eftirlitslausum ham með því að nota Regression Suite Automation Tool. Í þessu tilviki getur viðvörunin talist bilun á prófunartilfellinu sem er í gangi.

1. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, á flipanum **Skilgreiningar**, velurðu **Færibreytur notanda**.
2. Stilltu valkostinn **Hindra grunnlínuviðvaranir** á **Já** og veldu síðan **Í lagi**.

### <a name="review-the-generated-baseline-file"></a>Yfirfara myndaða grunnlínuskrá

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Veldu **Grunnlínur**.
3. Veldu **Viðhengi**.
    > [!NOTE]
    > Mynduð skrá inniheldur texta vinnsludagsetningar og tíma (**„#“**) úr bindingu sem var stillt í viðbættri reglu grunnlínu, ekki úr bindingu sniðsins.
    
4. Lokaðu síðunni **Viðhengi**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Keyrðu uppsett ER-snið og endurskoðaðu skrána til að greina niðurstöðurnar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Í trénu stækkarðu **Líkan til að læra ER-grunnlínur**.
3. Í trénu skaltu velja **Líkan til að læra ER-grunnlínur\\Snið til að læra ER-grunnlínur**.
4. Á flýtiflipanum **Útgáfur** velurðu **Keyra**.
5. Í reitnum **Skrá kenni** ritarðu **1**.
6. Veljið **Í lagi**.
7. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Kembingarkladdar skilgreiningar**.

Framkvæmdakladdinn inniheldur upplýsingar um niðurstöður samanburðar á myndaðri skrá við skilgreinda grunnlínu. Kladdinn gefur til kynna að mynduð skrá og grunnlínan séu eins, jafnvel þó að framkvæmt snið innihaldi bindingu til að færa inn síbreytileg dags.- og tímagildi í skrána á útleið.

> [!NOTE]
> Þó að skrá á útleið hafi verið mynduð með því að nota grunnlínustillingar sem þvinga endurnýjun á bindingu sniðsins, færðu engar viðvaranir um endurnýjunina.

## <a name="exchange-baseline-settings-between-environments"></a>Skipta um grunnlínustillingar á milli umhverfa

### <a name="export-baseline-settings"></a>Flytja út grunnlínustillingar

Nýja ER-getan gerir þér kleift að flytja út grunnlínustillingar fyrir valið ER-snið úr núverandi umhverfi og geyma þær sem XML-skrár. 

Til að flytja út grunnstillingar skaltu á síðunni **Grunnlínusnið rafrænnar skýrslugerðar** velja **Flytja út**.

### <a name="import-baseline-settings"></a>Flytja inn grunnstillingar

Útfluttar grunnlínustillingar má flytja inn í mismunandi umhverfi. Fyrst verður að flytja umhverfið inn sem ER-snið. Síðan geturðu flutt grunnlínustillingar.

Til að flytja inn grunnlínustillingar úr staðbundið vistaðri XML-skrá skaltu á síðunni **Grunnlínur rafrænnar skýrslugerðar** velja **Flytja inn** og síðan **Skoða** til að velja XML-skrána.

![Svarglugginn Flytja inn grunnlínustillingar.](media/GER-BaselineSample-ImportBaseline1.PNG "Skjámynd af svarglugganum Innflutningur á grunnlínustillingum")

Til að flytja inn grunnlínustillingar úr XML-skrá sem er geymd á Microsoft SharePoint-þjóni, byggð á núverandi skjalastjórnunarstillingum og völdum skjalategundum, skaltu á síðunni **Grunnlínur rafræns skýrslugerðarsniðs** velja **Flytja inn úr uppruna**. Veldu síðan gerð skjalsins og XML-skrána. Tilskilin skjalagerð til að fá aðgang að SharePoint-möppunni verður að vera skilgreind fyrirfram.

![Svarglugginn Flytja inn úr uppruna.](media/GER-BaselineSample-ImportBaseline2.PNG "Skjámynd af svarglugganum Innflutningur úr uppruna")

> [!NOTE]
> Þú getur notað verkskráningu til að skrá skrefin til að velja nauðsynlega skjalagerð og skráarheiti í svarglugganum **Flytja inn úr uppruna**. Þannig geturðu haldið nauðsynlegum grunnlínustillingum á SharePoint-þjóninum og flutt þær síðan sjálfvirkt inn með því að spila verkskráninguna þegar þú keyrir sjálfvirk próf með því að nota Regression Suite Automation Tool.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md)
- [Tilföng verkskráningar](../user-interface/task-recorder.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

