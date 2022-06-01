---
title: Bættu frammistöðu ER lausna með því að fækka töflureitum sem eru sóttir á keyrslutíma
description: Þetta efnisatriði útskýrir hvernig þú getur hjálpað til við að bæta árangur með því að fækka töflureitum sem eru sóttir á keyrslutíma.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: dd192a7718ac4fd8bcb636ede6c005ca29ee5f08
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811831"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Bættu frammistöðu ER lausna með því að fækka töflureitum sem eru sóttir á keyrslutíma

[!include[banner](../includes/banner.md)]

Þú getur hannað [Rafræn skýrslugerð](general-electronic-reporting.md) (ER) [sniðum](er-overview-components.md#format-components-for-outgoing-electronic-documents) sem búa til sendandi skjöl á ýmsum sniðum. Þegar skjal er búið til kallar ER-snið til gagnagjafa sem voru stilltir í samsvarandi ER [módelkortlagningu](er-overview-components.md#model-mapping-component). Til að stilla aðgang að forritatöflum, fyrirspurnum eða einingum til að sækja skrár, geturðu notað ER gagnaheimildir *Taflaskrár* tegund. Sjálfgefið er gagnagjafi á *Taflaskrár* tegund sækir gildi allra reita í umbeðnum færslum. Hins vegar er hægt að stilla þessa tegund gagnagjafa þannig að hún sæki aðeins svæðisgildin sem eru nauðsynleg fyrir ER-sniðið sem er í gangi. Þessi uppsetning hjálpar til við að draga úr minnisnotkun forritaþjónsins sem framkvæmir gagnaöflun og frekari skyndiminni.

Til að læra meira um hvernig á að takmarka listann yfir sótta reiti gagnagjafa *Taflaskrár* tegund, kláraðu dæmið í þessu efni.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Dæmi: Fækkaðu töflureitum sem eru sóttir á keyrslutíma

Eftirfarandi aðferðir sýna hvernig notandi í hlutverki Kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur stillt ER líkanavörpun þannig að hún sæki aðeins þá reiti sem þarf til að keyra ER sniðið, til að draga úr neyslu á minni forritaþjóns.

Þessar aðferðir er hægt að ljúka í **USMF** fyrirtæki í Microsoft Dynamics 365 Fjármál. Ekki er þörf á neinni kóðun.

Til að klára þetta dæmi verður þú að hafa aðgang að **USMF** fyrirtæki í eitt af eftirfarandi hlutverkum:

- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

Í þessu dæmi muntu nota ER [stillingar](general-electronic-reporting.md#Configuration) sem veitt er fyrir **Litware, Inc.** sýnishorn fyrirtæki. Gakktu úr skugga um að stillingarveitan fyrir **Litware, Inc.** (`http://www.litware.com`) sýnishornsfyrirtæki er skráð fyrir ER ramma og að það sé merkt sem **Virkur**. Ef þessi stillingarveita er ekki á listanum eða ef hún er ekki merkt sem **Virkur**, fylgdu skrefunum í [Búðu til stillingarveitu og merktu hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ER ramma til að breyta gagnaheimildum ER lausnarinnar sem fylgir.

### <a name="import-the-sample-er-configurations"></a>Flytja inn sýnishorn af ER-stillingum

Ef þú hefur ekki enn lokið við dæmið í [Hannaðu nýja ER lausn til að prenta sérsniðna skýrslu](er-quick-start1-new-solution.md) efni, hlaðið niður og geymt XML skrárnar á staðnum fyrir eftirfarandi stillingar fyrir ER lausnina sem fylgir.

| Lýsing á efni            | Skráarheiti |
|--------------------------------|-----------|
| Skilgreining á gagnalíkani í ER    | [Spurningalistar model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| Stilling vörpunar ER-líkans | [Spurningalistar kortlagning.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| ER Sníða skilgreiningu        | [Spurningalistar format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Fylgdu síðan þessum skrefum til að hlaða upp stillingum meðfylgjandi ER lausnar í Finance tilvikið þitt.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Á **Stillingar** síðu, flyttu inn ER gagnalíkanstillingu.

    1. Veldu **Skipta** og veldu síðan **Hlaða úr XML skrá**.
    2. Veldu **Skoðaðu**, finndu og veldu **Spurningalistar model.version.1.xml** skrá og veldu síðan **Allt í lagi**.

4. Flyttu inn ER líkanskortstillingu.

    1. Veldu **Skipta** og veldu síðan **Hlaða úr XML skrá**.
    2. Veldu **Skoðaðu**, finndu og veldu **Spurningalistar kortlagning.1.1.xml** skrá og veldu síðan **Allt í lagi**.

5. Flyttu inn ER sniðstillingu.

    1. Veldu **Skipta** og veldu síðan **Hlaða úr XML skrá**.
    2. Veldu **Skoðaðu**, finndu og veldu **Spurningalistarsnið.1.1.xml** skrá og veldu síðan **Allt í lagi**.

6. Stækkaðu út í stillingartrénu **Fyrirmynd spurningalista**.
7. Skoðaðu listann yfir innfluttar ER stillingar í stillingartrénu.

    ![Farið yfir listann yfir innfluttar ER stillingar á síðunni Stillingar.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Farðu yfir meðfylgjandi kortlagningu ER líkana

1. Á **Stillingar** síðu, veldu **Kortlagning spurningalista**.
2. Í aðgerðarúðunni skal velja **Hönnuður**.
3. Á **Líkan til kortlagningar gagnagjafa** síðu, veldu **Hönnuður**.
4. Á **Módelkortahönnuður** síðu, á aðgerðarrúðunni, veldu **Hópsýn** að kveikja á **Hópur** útsýni.
5. Í **Gagnalíkan** rúðu, stækka **Spurningalisti**.

    Taktu eftir því að **Spurningalisti** gagnagjafi hefur verið stilltur til að fá aðgang að`KMCollection` umsóknartöflu.

6. Í **Uppsprettur gagna** rúðu, stækka **Taflaskrár** \> **Spurningalisti** \> **Fields**.

    Taktu eftir hversu margir reitir frá`KMCollection` umsóknartafla eru afhjúpuð af **Spurningalisti** gagnauppspretta *Taflaskrár* tegund.

    ![Farið yfir meðfylgjandi líkanavörpun á hönnuðarsíðu líkanakortlagningar þegar kveikt er á hópsýn.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Á aðgerðarrúðunni velurðu **Hópsýn** aftur til að slökkva **Hópur** skoða og veldu síðan **Sýna allt** \> **Sýna aðeins kortlagt**.

    Taktu eftir að nokkrir reitir af`KMCollection` umsóknartafla eru notuð til að fylla út **Spurningalisti** skráningarlisti í ER gagnalíkaninu:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Farið yfir meðfylgjandi líkanavörpun á síðunni Líkanskorthönnuður þegar slökkt er á hópsýn.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>Kveikja á afkastarakningu rafrænnar skýrslugerðar

Fylgdu skrefunum í [Kveiktu á ER frammistöðurakningu](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) til að stilla ER notendafæribreytur sem gera kleift að rekja framkvæmd ER hluti.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Keyrðu uppgefið ER snið með því að nota meðfylgjandi líkanskort

Fylgdu skrefunum í [Keyra hannað snið frá ER](er-quick-start1-new-solution.md#RunFormatFromER) að keyra uppgefið ER snið fyrir einn spurningalista frá **Stillingar** síðu.

### <a name="review-the-execution-trace-of-the-first-run"></a>Farðu yfir framkvæmdarspor fyrstu keyrslu

1. Fara til **Stjórn stofnunarinnar** \> **Rafræn skýrslugerð \> Stillingar**.
2. Á **Stillingar** síðu, stækkaðu **Fyrirmynd spurningalista**, og veldu **Spurningalistar kortlagning**.

    > [!NOTE]
    > Upplýsingarnar á **Útgáfur** Flýtiflipi gefur til kynna að þú hafir valið drög að útgáfu af **Spurningalistar kortlagning** stillingar. Þess vegna geturðu breytt innihaldi þessarar líkanakortlagningar.

3. Í aðgerðarúðunni skal velja **Hönnuður**.
4. Á **Líkan til kortlagningar gagnagjafa** síðu, veldu **Hönnuður**.
5. Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.
6. Í **Stillingar niðurstaðna afkastagetu** valmynd, veldu ummerkin sem var búin til við síðustu sniðkeyrslu.

    ![Val á rekningunni í valmyndinni Stillingar niðurstöður árangursrakningar.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Veldu **Í lagi**. 
8. Á **Upplýsingar** Flýtiflipi, síaðu **Spurningalisti** leið sem vísar til **Spurningalisti** gagnagjafa.
9. Skoðaðu upplýsingar um gagnagrunnsfyrirspurnina sem var búin til þegar **Spurningalisti** gagnaveita var kallað.

    Taktu eftir að allir sviðum`KMCollection` forrittafla var sótt á keyrslutíma þegar **Spurningalisti** gagnaveita var kallað.

    ![Farið yfir upplýsingar um gagnagrunnsfyrirspurnina á síðunni Hönnuður líkanakorta.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Breyttu meðfylgjandi ER líkanavörpun

1. Á **Módelkortahönnuður** síðu, í **Uppsprettur gagna** glugga, veldu **Spurningalisti** gagnagjafa.
2. Í **Uppsprettur gagna** rúðu, veldu **Breyta**.
3. Í **Eiginleikar gagnagjafa** valmynd, veldu **Veldu reiti** til að tilgreina lista yfir reiti þess sem vísað er til`KMCollection` forritatöflu sem verður sótt á keyrslutíma þegar hægt er að breyta **Spurningalisti** gagnagjafi er kallaður.

    ![Velja Velja reiti í Eiginleikum gagnagjafa valmynd til að byrja að stilla listann yfir reiti sem verða sóttir úr forritatöflunni með því að nota breytanlega gagnagjafa.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Á **Veldu reiti** síðu, veldu **Sjálfvirk útfylling**.

    The **Valdir reitir** listi er sjálfkrafa fylltur út, byggt á forstilltum gripum af líkanakortlagningunni. Öllum reitum og tengslum töflunnar sem vísað er til sem getið er um í hvaða bindingu, formúlu eða gagnauppsprettu líkanavörpunnar er bætt við listann.

    ![Stilla lista yfir reiti sem verða sóttir úr forritatöflunni á síðunni Veldu reiti.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Veldu **Vista**, og lokaðu **Veldu reiti** síðu.
6. Veldu **Allt í lagi** til að geyma breytingarnar sem þú hefur gert á stillingum gagnagjafans.
7. Á aðgerðarrúðunni velurðu **Sýna allt**.

    Taktu eftir því að **Spurningalisti** gagnagjafi sýnir nú textann **\<Fields are filtered\>**. Þessi texti gefur til kynna að gagnagjafinn hafi verið stilltur til að sækja takmarkaðan fjölda reita úr forritatöflunni sem vísað er til.

    ![Farið yfir uppfærða líkanavörpun á hönnuðarsíðu líkanakortlagningar.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Veldu **Vista** til að geyma breytingarnar sem þú hefur gert á breytanlegu líkanavörpuninni.

    > [!NOTE]
    > Á keyrslutíma greinir ER viðbættu tengslin og bætir öllum reitum sem eru notaðir í þeim við gagnagrunnsfyrirspurnina, jafnvel þótt þeim reitum hafi ekki verið bætt sérstaklega við listann yfir sótta reiti við hönnunartíma.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Keyrðu uppgefið ER snið með því að nota uppfærða líkanavörpun

Fylgdu skrefunum í [Keyra hannað snið frá ER](er-quick-start1-new-solution.md#RunFormatFromER) að keyra uppgefið ER snið fyrir einn spurningalista frá **Stillingar** síðu.

### <a name="review-the-execution-trace-of-the-second-run"></a>Farðu yfir framkvæmdarferil seinni keyrslunnar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á **Stillingar** síðu, stækkaðu **Fyrirmynd spurningalista**, og veldu **Spurningalistar kortlagning**.
3. Í aðgerðarúðunni skal velja **Hönnuður**.
4. Á **Líkan til kortlagningar gagnagjafa** síðu, veldu **Hönnuður**.
5. Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.
6. Í **Stillingar niðurstaðna afkastagetu** valmynd, veldu ummerkin sem var búin til við síðustu sniðkeyrslu.
7. Veldu **Í lagi**.
8. Á **Upplýsingar** Flýtiflipi, síaðu **Spurningalisti** leið sem vísar til **Spurningalisti** gagnagjafa.
9. Skoðaðu upplýsingar um gagnagrunnsfyrirspurnina sem var búin til þegar **Spurningalisti** gagnaveita var kallað.

    Taktu eftir að aðeins reitirnir sem eru nauðsynlegir til að fylla út gagnagjafann voru sóttir á keyrslutíma frá`KMCollection` umsóknartafla þegar **Spurningalisti** gagnaveita var kallað.

    > [!NOTE]
    > Sumum reitum, eins og reitum fyrir skiptingarauðkenni, auðkenni gagnasvæðis og færsluauðkenni, er sjálfkrafa bætt við af gagnastjórnunarramma Finance appsins.

    ![Farið yfir upplýsingar um gagnagrunnsfyrirspurnina fyrir uppfærða líkanavörpun á síðunni Líkanskorthönnuður.](./media/er-reduce-fetched-fields-number-query2.png)

Þú getur notað þessa tækni til að fækka sóttum færslum þegar þú verður að draga úr minnisnotkun með því að keyra ER líkanavörpun og ER sniði.

## <a name="limitations"></a>Takmarkanir

Þegar þú takmarkar fjölda sóttra reita fyrir gagnagjafa í *Taflaskrár* tegund geturðu ekki notað aðferðir forritatöflu sem gagnagjafinn vísar til, vegna þess að lýsigögn forritsins veita ekki upplýsingar um töflureiti sem þarf til að kalla þessar aðferðir.

## <a name="usage-notes"></a>Notkunarbréf

Þó að **Sjálfvirk útfylling** skipunin bætir reitum sjálfkrafa við, hún eyðir ekki reitum sem áður hefur verið bætt við sjálfkrafa, jafnvel þó að þeir séu ekki lengur notaðir í bindingum, formúlum og gagnaveitum breytanlegrar líkanavörpunar.

Þegar þú velur **Sjálfvirk útfylling**, ER greinir bindingar, formúlur og gagnaheimildir sem breytanlegu líkanavörpuninni hafði þegar þú opnaðir það til að breyta. Ef þú breytir bindingum, formúlum og gagnaveitum á breytanlegu líkanavörpuninni og þú vilt nota **Sjálfvirk útfylling** skipun, lokaðu líkanakortshönnuðinum og opnaðu hann svo aftur til að breyta líkanavörpunni þinni. 

## <a name="additional-resources"></a>Frekari upplýsingar

- [Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md)
- [Úrræðaleita vandamál sem tengjast afköstum í skilgreiningum rafrænnar skýrslugerðar](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
