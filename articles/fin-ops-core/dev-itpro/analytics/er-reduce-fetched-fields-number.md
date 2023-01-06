---
title: Aukið afköst lausna fyrir rafræna skýrslugerð með því að minnka fjölda töflureita sem eru sóttir við keyrslu
description: Þessi grein útskýrir hvernig hægt er að auka afköst með því að minnka fjölda töflureita sem eru sóttir við keyrslu
author: kfend
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 5c9481f1021a5dba6e1d4020bbf85a10bd551ac0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278827"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Aukið afköst lausna fyrir rafræna skýrslugerð með því að minnka fjölda töflureita sem eru sóttir við keyrslu

[!include[banner](../includes/banner.md)]

Hægt er að hann [Rafræn skýrslugerð](general-electronic-reporting.md) (ER) [snið](er-overview-components.md#format-components-for-outgoing-electronic-documents) sem býr til skjöl á útleið á ýmsum sniðum. Þegar skjal er búið til kallar snið rafrænnar skýrslugerðar á gagnagjafa sem voru skilgreindir í samsvarandi [líkanavörpun](er-overview-components.md#model-mapping-component) rafrænnar skýrslugerðar. Til að stilla aðgang að forritatöflum, fyrirspurnum eða aðilum til að sækja skrá er hægt að nota gagnagjafa rafrænnar skýrslugerðar af gerðinni *Töflufærslur*. Gagnagjafi af gerðinni *Töflufærslur* sækir sjálfgefið gildin í öllum reitum í umbeðnum færslum. Hins vegar geturðu skilgreint þessa gerð af gagnagjafa þannig að hún sæki aðeins reitargildin sem þarf til að keyra snið rafrænnar skýrslugerðar. Þessi skilgreining hjálpar til við að draga úr minnisnotkun forritsþjóns sem sækir gögn og frekari skyndiminnsfærslur.

Ljúktu dæminu í þessari grein til að fræðast meira um hvernig á að takmarka listann yfir sótta reiti gagnagjafa af gerðinni *Töflufærslur*.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Dæmi: Minnka fjölda töflureita sem eru sóttir við keyrslu

Eftirfarandi ferlar sýna hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur skilgreint líkanavörpun rafrænnar skýrslugerðar þannig að hún sæki aðeins reiti sem þarf til að keyra snið rafrænnar skýrslugerðar til að koma í veg fyrir minnisnotkun forritsþjóns.

Hægt er að ljúka þessum ferlum í **USMF**-fyrirtækinu í Microsoft Dynamics 365 Finance. Ekki er þörf á neinni kóðun.

Til að ljúka þessu dæmi verður þú að hafa aðgang að **USMF** fyrirtæki fyrir eitt af eftirfarandi hlutverkum:

- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

Í þessu dæmi muntu nota [skilgreiningar](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar fyrir sýnifyrirtækið **Litware, Inc.**. Tryggið að skilgreiningarveita fyrir sýndarfyrirtækið **Litware, Inc.** (`http://www.litware.com`) sé skráð fyrir ramma rafrænnar skýrslugerðar og merkt sem **Virk**. Ef skilgreiningarveita er ekki skráð, eða ef hún er ekki merkt sem **Virk**, skal fylgja skrefunum í greininni [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ramma rafrænnar skýrslugerðar til að breyta gagnagjöfum þeirrar lausnar rafrænnar skýrslugerðar sem boðið er upp á.

### <a name="import-the-sample-er-configurations"></a>Flytja inn sýnishorn af ER-stillingum

Ef þú hefur ekki enn lokið dæminu í greininni [Hanna nýja lausn rafrænnar skýrslugerðar til að prenta sérsniðna skýrslu](er-quick-start1-new-solution.md) skaltu sækja og vista staðbundið XML-skrár fyrir eftirfarandi skilgreiningar af uppgefinni lausn rafrænnar skýrslugerðar.

| Lýsing á efni            | Skráarheiti |
|--------------------------------|-----------|
| Skilgreining á gagnalíkani í ER    | [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| Stilling vörpunar ER-líkans | [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| ER Sníða skilgreiningu        | [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Fylgdu svo þessum skrefum til að hlaða upp skilgreiningum af uppgefinni lausn rafrænnar skýrslugerðar í Finance-tilvikið.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar** skal flytja inn skilgreiningu á gagnalíkani rafrænnar skýrslugerðar.

    1. Veldu **Skipta** og veldu síðan **Hlaða úr XML skrá**.
    2. Veljið **Fletta**, finnið og veljið skrána **Questionnaires model.version.1.xml** og veljið síðan **OK**.

4. Flytja inn skilgreiningu vörpunar líkans fyrir rafræna skýrslugerð

    1. Veldu **Skipta** og veldu síðan **Hlaða úr XML skrá**.
    2. Veldu **Fletta**, finndu og veldu skrána **Questionnaires mapping.1.1.xml** og veldu síðan **Í lagi**.

5. Flytja inn skilgreiningu ER-sniðs.

    1. Veldu **Skipta** og veldu síðan **Hlaða úr XML skrá**.
    2. Veldu **Fletta**, finndu og veldu skrána **Questionnaires format.1.1.xml** og veldu síðan **Í lagi**.

6. Á skilgreiningartrénu, skal útvíkka **Líkan spurningalista**.
7. Skoðaðu listann yfir innfluttar ER stillingar í stillingartrénu.

    ![Farið yfir lista yfir innfluttar skilgreining rafrænnar skýrslugerðar á skilgreiningasíðunni.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Farðu yfir fyrirliggjandi líkanavörpun rafrænnar skýrslugerðar

1. Á síðunni **Skilgreiningar** skal velja **Vörpun spurningalista**.
2. Í aðgerðarúðunni skal velja **Hönnuður**.
3. Á síðunni **Vörpun líkans í gagnagjafa** skal velja **Hönnuður**.
4. Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Yfirlit flokks** til að kveikja á yfirlitinu **Flokkur**.
5. Í rúðunni **Gagnalíkan** skal útvíkka **Spurningalisti**.

    Taktu eftir að gagnagjafinn **Spurningalisti** hefur verið skilgreindur til að fá aðgang að `KMCollection` forritstöflunni.

6. Í rúðunni **Gagnagjafar** skal stækka **Töflufærslur** \> **Spurningalisti** \> **Reitir**.

    Taktu eftir því hversu margir reitir frá `KMCollection` forritstöflunni eru sýndir af hálfu gagnagjafa **Spurningalista** af gerðinni *Töflufærslur*.

    ![Farið yfir uppgefna líkanavörpun á hönnunarsíðu líkanavörpunar þegar kveikt er á flokksyfirlitinu.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Á aðgerðasvæðinu skal velja **Flokksyfirlit** aftur til að slökkva á yfirlitinu **Flokkur** og velja síðan **Sýna allt** \> **Sýna aðeins varpað**.

    Taktu eftir því að nokkrir reitir `KMCollection` forritstöflunnar eru notaðir til að fylla út færslulistann **Spurningalisti** í gagnalíkani rafrænnar skýrslugerðar:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Farið yfir uppgefna líkanavörpun á hönnunarsíðu líkanavörpunar þegar slökkt er á flokksyfirliti.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>Kveikja á afkastarakningu rafrænnar skýrslugerðar

Fylgdu skrefunum í [Kveikja á afkastarakningu rafrænnar skýrslugerðar](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) til að stilla notandafæribreytur rafrænnar skýrslugerðar sem gera kleift að rekja rafræna skýrslugerðarþætti.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Keyrðu meðfylgjandi snið rafrænnar skýrslugerðar með því að nota meðfylgjandi líkanavörpun.

Fylgdu skrefunum í [Keyra hannað snið úr rafrænni skýrslugerð](er-quick-start1-new-solution.md#RunFormatFromER) til að keyra uppgefið snið rafrænnar skýrslugerðar fyrir einn spurningalista af síðunni **Skilgreiningar**.

### <a name="review-the-execution-trace-of-the-first-run"></a>Yfirfara framkvæmdarakningu fyrstu keyrslu

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð \> Skilgreiningar**.
2. Á síðunni **Skilgreiningar** skal útvíkka **Líkan spurningalista** og velja síðan **Vörpun spurningalista**.

    > [!NOTE]
    > Upplýsingarnar í flýtiflipanum **Útgáfur** gefa til kynna að þú valdir útgáfudrög fyrir skilgreininguna **Vörpun spurningalista**. Því er hægt að breyta efni þessa líkanavörpunarinnar.

3. Í aðgerðarúðunni skal velja **Hönnuður**.
4. Á síðunni **Vörpun líkans í gagnagjafa** skal velja **Hönnuður**.
5. Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.
6. Í svarglugganum **Stillingar fyrir niðurstöðu afkastarakningar** skal velja rakninguna sem var gerð við síðustu keyrslu á sniði.

    ![Val á rakningu í svarglugganum „Stillingar fyrir niðurstöðu afkastarakningar“.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Veldu **Í lagi**. 
8. Í flýtiflipanum **Upplýsingar** skal sía slóðina **Spurningalisti** sem bendir á gagnagjafann **Spurningalisti**.
9. Farðu yfir upplýsingarnar um fyrirspurn gagnagrunns sem var mynduð þegar kallað var á gagnagjafann **Spurningalisti**.

    Taktu eftir því að allir reitir `KMCollection` forritstöflunnar voru sóttir við keyrslu þegar kallað er á gagnagjafann **Spurningalisti**.

    ![Farið yfir upplýsingarnar um fyrirspurn gagnagrunns á hönnunarsíðu líkanavörpunar.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Breyta meðfylgjandi vörpun á líkan rafrænnar skýrslugerðar

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnagjafar**, skal velja gagnagjafann **Spurningalisti**.
2. Í rúðunni **Gagnagjafar** skal velja **Breyta**.
3. Í svarglugganum **Eiginleikar gagnagjafa** skal velja **Velja reiti** til að tilgreina lista yfir reiti af `KMCollection` forritstöflunni sem vísað er í sem verður sótt við keyrslu þegar kallað er á breytanlega gagnagjafann **Spurningalisti**.

    ![Veldu „Velja reiti“ í svarglugganum „Eiginleikar gagnagjafa“ til að byrja að skilgreina lista yfir reiti sem verða sóttir úr forritstöflunni með því að nota breytanlegan gagnagjafa.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Á síðunni **Velja reiti** skal velja **Sjálfvirk útfylling**.

    Listinn **Valdir reitir** er sjálfkrafa fylltur út samkvæmt fyrirfram skilgreindum gervingum líkanavörpunar. Öllum reitum og tengslum tilvísaðrar töflu sem minnst er á í bindingu, formúlu eða gagnagjafa líkanavörpunar er bætt við listann.

    ![Skilgreinir lista yfir reiti sem verða sóttir úr forritstöflunni á síðunni „Velja reiti“.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Veljið **Vista** og lokið síðunni **Velja reiti**.
6. Veldu **Í lagi** til að vista breytingarnar sem þú gerðir á stillingum gagnagjafans.
7. Á aðgerðasvæðinu skal velja **Sýna allt**.

    Takið eftir að gagnagjafinn **Spurningarlisti** sýnir nú textann **\<Fields are filtered\>**. Þessi texti gefur til kynna að gagnagjafinn hafi verið skilgreindur til að sækja takmarkaðan fjölda reita úr forritstöflunni sem vísað er í.

    ![Farið yfir uppfærða vörpun líkans á síðunni Hönnuður líkanavörpunar.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Veldu **Vista** til að geyma breytingarnar sem þú gerðir á breytanlegri líkanavörpun.

    > [!NOTE]
    > Við keyrslu greinir rafræn skýrslugerð tengsl sem bætt var við og bætir öllum reitum sem eru notaðir í þeim við fyrirspurn gagnagrunnsins, jafnvel þótt þessum reitum var ekki sérstaklega bætt við listann yfir sótta reiti á hönnunartíma.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Keyrðu meðfylgjandi snið rafrænnar skýrslugerðar með því að nota uppfærða líkanavörpun

Fylgdu skrefunum í [Keyra hannað snið úr rafrænni skýrslugerð](er-quick-start1-new-solution.md#RunFormatFromER) til að keyra uppgefið snið rafrænnar skýrslugerðar fyrir einn spurningalista af síðunni **Skilgreiningar**.

### <a name="review-the-execution-trace-of-the-second-run"></a>Yfirfara framkvæmdarakningu annarrar keyrslu

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar** skal útvíkka **Líkan spurningalista** og velja síðan **Vörpun spurningalista**.
3. Í aðgerðarúðunni skal velja **Hönnuður**.
4. Á síðunni **Vörpun líkans í gagnagjafa** skal velja **Hönnuður**.
5. Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.
6. Í svarglugganum **Stillingar fyrir niðurstöðu afkastarakningar** skal velja rakninguna sem var gerð við síðustu keyrslu á sniði.
7. Veldu **Í lagi**.
8. Í flýtiflipanum **Upplýsingar** skal sía slóðina **Spurningalisti** sem bendir á gagnagjafann **Spurningalisti**.
9. Farðu yfir upplýsingarnar um fyrirspurn gagnagrunns sem var mynduð þegar kallað var á gagnagjafann **Spurningalisti**.

    Taktu eftir að aðeins reitirnir sem þarf til að fylla út gagnagjafann voru sóttir við keyrslu úr `KMCollection` forritstöflunni þegar kallað var á gagnagjafann **Spurningalisti**.

    > [!NOTE]
    > Sumum reitum, til dæmis reitum fyrir auðkenni skiptingar, auðkenni gagnasvæðis og færslukenni, er sjálfkrafa bætt við af ramma gagnastjórnunar í Finance-forritinu.

    ![Farið yfir upplýsingarnar um fyrirspurn gagnagrunns fyrir uppfærða líkanavörpun á hönnunarsíðu líkanavörpunar.](./media/er-reduce-fetched-fields-number-query2.png)

Hægt er að nota þessa tækni til að draga úr fjölda færslna sem er sóttur þegar draga þarf úr minnisnotkun fyrir líkanavörpun og snið rafrænnar skýrslugerðar sem eru keyrð.

## <a name="limitations"></a>Takmarkanir

Þegar fjöldi sóttra reita er takmarkaður fyrir gagnagjafa af gerðinni *Töflufærslur* er ekki hægt að nota aðferðir forritstöflu sem gagnagjafinn vísar í því að lýsigögn forritsins bjóða ekki upp á upplýsingar um töflureiti sem þarf til að kalla á þessar aðferðir.

## <a name="usage-notes"></a>Notkunarbréf

Þótt skipunin **Sjálfvirk útfylling** bætir við reitum eyðir hún ekki sjálfkrafa áður viðbættum reitum jafnvel þótt þeir séu ekki lengur notaðir í bindingum, formúlum og gagnagjöfum fyrir breytanlega líkanavörpun.

Þegar **Sjálfvirk útfylling** er valið greinir rafræn skýrslugerð bindingar, formúlur og gagnagjafa sem breytanlega líkanavörpunin var með þegar þú opnaðir hana til að gera breytingar. Ef bindingum, formúlum og gagnagjöfum breytanlegrar líkanavörpunar er breytt og þú vilt nota skipunina **Sjálfvirk útfylling** skal loka hönnuði líkanavörpunar og síðan opna hann aftur til að gera breytingar á líkanavörpuninni. 

## <a name="additional-resources"></a>Frekari upplýsingar

- [Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md)
- [Úrræðaleita vandamál sem tengjast afköstum í skilgreiningum rafrænnar skýrslugerðar](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
