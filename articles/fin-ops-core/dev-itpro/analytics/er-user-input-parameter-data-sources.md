---
title: Nota INNSLÁTTARFÆRIBREYTU NOTANDA gagnagjafa til að tilgreina færibreytur fyrir skýrslu
description: Þessi grein útskýrir hvernig á að nota USER INPUT PARAMETER-gagnagjafana til að tilgreina færibreytur fyrir skýrslu sem á að búa til
author: kfend
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: c6d0f1a0d9c5eb70a9812459a25d5b14407cce7a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278708"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Nota INNSLÁTTARFÆRIBREYTU NOTANDA gagnagjafa til að tilgreina færibreytur fyrir skýrslu

[!include[banner](../includes/banner.md)]

Þegar þú hannar [Rafræna skýrslugerð](general-electronic-reporting.md) (ER) [líkanavörpun](er-overview-components.md#model-mapping-component) og [snið](er-overview-components.md#format-component) geturðu notað gagnagjafa af gerðinni *INNSLÁTTARFÆRIBREYTA NOTANDA* til að fá nauðsynleg gildi sem hægt er að tilgreina í reitum gagnaskráningar í svarglugga við keyrslu áður en keyrsla rafræns skýrslugerðarsniðs hefst. Þessi grein lýsir gagnagjöfunum *INNSLÁTTARFÆRIBREYTA NOTANDA* sem eru studdir sem stendur.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a>Áskildir eiginleikar

Tilgreina verður eftirfarandi eiginleika fyrir gagnagjafa af öllum gerðum *INNSLÁTTARFÆRIBREYTU NOTANDA*:

- Innra heiti gagnagjafa er ritað í reitinn **Heiti**. Hægt er að nota þetta heiti í öðrum [segðum](er-formula-language.md) og bindingum skilgreindrar líkanavörpunar eða sniðshluta.

## <a name="optional-properties"></a><a name="optional-properties"></a>Valfrjálsir eiginleikar

Hægt er að tilgreina eftirfarandi eiginleika fyrir gagnagjafa af gerðinni *INNSLÁTTARFÆRIBREYTA NOTANDA*:

- Í reitnum **Merki** skal tilgreina merkið sem notað er fyrir tengda reiti gagnaskráningar í svarglugganum við keyrslu. Hægt er að bæta við mismunandi merkjatextum fyrir mismunandi tungumálakóða með því að virkja reitinn **Merki** og velja síðan **Þýða**.
- Í reitnum **Hjálp** skal tilgreina hjálpartexta sem birtist á hönnunartíma neðst á síðunni **Sniðshönnuður** eða síðunni **Hönnuður líkanavörpunar** þegar breytanlegur gagnagjafi af gerðinni *INNSLÁTTARFÆRIBREYTA NOTANDA* er valinn. Þessi texti gæti veitt viðbótarupplýsingar um gagnagjafann til að hjálpa notendum þegar þeir skilgreina breytanlega þætti sniðs eða líkanavörpunar. Hægt er að bæta við mismunandi hjálpartexta fyrir mismunandi tungumálakóða með því að velja **Þýða**.

    > [!NOTE]
    > Hnappurinn **Þýða** sem hægt er að nota til að bæta við [merki og texti á tilteknu tungumáli](er-design-multilingual-reports.md#format-component) verður aðgengilegur aðeins eftir að þú bætir gagnagjafanum við, vistar breytingar og enduropnar síðan gagnagjafann til að gera breytingar.

- Í reitnum **Skrifvarið** skal skilgreina segð sem skilar *[Boole-gildi](er-formula-supported-data-types-primitive.md#boolean)*.

    - Ef skilgreind segð skilar gildinu **Satt** við keyrslu verður tengdur gagnaskráningarreitur skyggður í svarglugganum og ekki hægt að breyta gildinu í honum.
    - Ef skilgreinda segðin skilar gildinu **Ósatt** við keyrslu eða ef engin segð er skilgreind verður tengdur gagnaskráningarreitur aðgengilegur í svarglugganum og hægt að gera breytingar á gildinu í honum.

- Í reitnum **Sjálfgefið gildi** skal skilgreina segð sem skilar gildinu á færibreytugerðinni sem vísað er í. Hægt er að nota þetta gildi til að fylla út sjálfgefið gildi fyrir reitinn fyrir tengd gögn í svarglugganum á keyrslutímanum.

    Þegar rafrænt skýrslugerðarsnið er keyrt er gildið sem slegið er inn í tengdan gagnaskráningarreit í svarglugganum við keyrslu vistað í minni sem áður notað gildi. Áður notuð gildi eru vistuð fyrir hvern reit fyrir sig, rafrænt skýrslugerðarsnið sem er keyrt, núverandi notanda og núverandi fyrirtæki.

    - Stilltu valkostinn **Endurstilla alltaf á sjálfgildi** á **Já** ef gildinu sem segðin **Sjálfgefið gildi** skilar á alltaf að vera notað sem sjálfgefið gildi burtséð frá áður notuðu gildi.
    - Stilltu valkostinn **Endurstilla alltaf á sjálfgildi** á **Nei** ef gildinu sem segðin **Sjálfgefið gildi** skilar á alltaf að vera notað sem sjálfgefið gildi aðeins þegar áður notað gildi vantar.

    > [!NOTE]
    > Ef þú stillir valkostinn **Endurstilla alltaf á sjálfgildi** á **Já** þarf að skilgreina segð í reitnum **Sjálfgefið gildi**.

- Ef þú stillir valkostinn **Leyfa fjölval** á **Já** geturðu valið mörg gildi fyrir skilgreinda færibreytu við keyrslu. Ef stillt er á **Nei** er aðeins hægt að velja eitt gildi.

    > [!NOTE]
    > Þessi valkostur á ekki við um allar gerðir *USER INPUT PARAMETER*. Á hönnunartíma kemur upp undantekning sem útskýrir fyrir notanda að skilgreind innsláttarfæribreyta notanda styður ekki fjölval og að aðeins sé hægt að velja eða slá inn eitt gildi.
    >
    > Ef þú stillir valkostinn **Leyfa fjölval** á **Já** og þú tilgreindir segð í reitnum **Sjálfgefið gildi** verður hægt að nota þá segð til að stilla aðeins eitt sjálfgefið gildi.

- Veldu valkostur **Breyta sýnileika** til að tilgreina hvort sýna eigi skilgreinda færibreytu í svarglugganum við keyrslu.

    > [!NOTE]
    > Sjálfgefinn sýnileiki gagnagjafa af gerðinni *INNSLÁTTARFÆRIBREYTA NOTANDA* fer eftir þætti rafræns skýrslugerðarsniðs sem geymir þær.
    >
    > - Ef gagnagjafi er skilgreindur í sniðsþættinum er hann sjálfgefið sýnilegur.
    > - Ef gagnagjafi er skilgreindur í þætti líkanavörpunar er hann aðeins sýnilegur ef gildi gagnagjafans hefur áhrif á útkomuna þegar rafrænn skýrslugerðarþáttur er keyrður. Ef þú bætir til dæmis við gagnagjafa en notaðir ekki segðir og bindingar fyrir núverandi þátt líkanavörpunar. Í þessu tilviki verður viðeigandi gagnaskráningarreitur sjálfgefið ekki sýndur í svarglugganum við keyrslu. 

    Á síðunni **Formúluhönnuður**, í reitinn **Formúla**, skal skilgreina segð sem skilar *Boole*-gildi.

    - Ef skilgreinda segðin skilar gildinu **Satt** við keyrslu eða ef engin segð er skilgreind verður tengdur gagnaskráningarreitur sýnilegur í svarglugganum við keyrslu.
    - Ef skilgreinda segðin skilar gildinu **Ósatt** verður tengdur gagnaskráningarreitur falinn í svarglugganum við keyrslu. Þegar aðrar segðir kalla á hana við keyrslu skilar hún sjálfgefnu gildi, áður notuðu gildi eða sjálfgildinu fyrir núverandi gildi gagnagerðar eftir því hverjar aðrar stillingar eru.

## <a name="type-specific-properties"></a>Eiginleikar eftir gerð

### <a name="application-dependent-user-input-parameter"></a>Innsláttarfæribreyta notanda eftir forriti

Notaðu gagnagjafa af gerðinni **Almennt** \> **Innsláttarfæribreyta notanda** til að fá eitt eða fleiri nauðsynleg gildi sem eru tilgreind fyrir núverandi tilvik af Microsoft Dynamics 365 Finance forritinu. Þegar gagnagjafa af þessari gerð er bætt við rafrænan skýrslugerðarþátt skal tilgreina eftirfarandi eiginleika:

- Í reitnum **Heiti gagnagerðar fyrir aðgerð (EDT, fasttexti)** skal velja [aukna gagnagerð (EDT)](../extensibility/extensible-edts.md) forrits eða tölusetningu forrits.

> [!NOTE]
> Mælt er með að fara yfir segðir sem eru skilgreindar í reitunum **Skrifvarið** og **Sjálfgefið gildi** þegar tilvísuninni **Heiti gagnagerðar fyrir aðgerð (EDT, fasttexti)** er breytt í breytanlegan gagnagjafa af gerðinni *INNSLÁTTARFÆRIBREYTA NOTANDA*.

Eftirfarandi mynd sýnir eiginleika `$TaxRegNum` gagnagjafans sem var skilgreindur í skilgreiningu á rafræna skýrslugerðarsniðinu **Instat XML (DE)**. Þessi gagnagjafi er skilgreindur til að nota EDT *lýsinguna* til að bjóða upp á gagnaskráningarreitinn **Skattskráningarnúmer** í svarglugganum við keyrslu.

![Eiginleikar gagnagjafa af gerðinni INNSLÁTTARFÆRIBREYTA NOTANDA í svarglugga á síðu sniðshönnuðar.](./media/er-user-input-parameter-data-sources-01.png)

Eftirfarandi mynd sýnir svargluggann sem sýndur er við keyrslu þegar skilgreining rafræna skýrslugerðarsniðsins **Instat XML (DE)** er keyrð til að [mynda](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) Intrastat-skattskýrslu. Taktu eftir að skilgreindi reiturinn **Skattskráningarnúmer** er í boði fyrir gagnaskráningu.

![Svargluggi Intrastat skýrslu fyrir rafrænt skýrslugerðarsnið sem er keyrt á Intrastat-síðunni.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Innsláttarfæribreyta notanda í tölusetningu gagnalíkans

Notaðu gagnagjafa af gerðinni **Gagnalíkan** \> **Innsláttarfæribreyta notanda tölusetningar** til að fá eitt eða fleiri nauðsynleg gildi fyrir eina [tölusetningu](er-formula-supported-data-types-primitive.md#enumeration) gagnalíkans. Þegar gagnagjafa af þessari gerð er bætt við rafrænan skýrslugerðarþátt skal tilgreina eftirfarandi eiginleika:

- Tilgreinið tilvísun í grunngagnalíkan í reitnum **Líkan**.
- Í reitnum **Tölusetning líkans** skal tilgreina tilvísun í tölusetningu á tilvísuðu gagnalíkani.
- Í reitnum **Útgáfa** skal velja endurskoðunarnúmer fyrir gagnalíkansþátt rafrænnar skýrslugerðar sem inniheldur tölusetningu líkans sem vísað er í.

    > [!TIP]
    > Á hönnunartíma er hægt að skilja reitinn **Útgáfa** eftir auðan til að fá aðgang að lista yfir tölusetningar fyrir gagnalíkansþátt sem vísað er í sem er að finna í útgáfudrögum af samsvarandi gagnalíkansskilgreiningu rafrænnar skýrslugerðar. Þannig er hægt að breyta samtímis útgáfudrögum líkanavörpunar eða sniðsþætti og útgáfudrögum á þætti grunngagnalíkans.
    >
    > Athugaðu samt að aðeins má skilja reitinn **Útgáfa** eftir auðan í útgáfudrögum líkanavörpunar og sniðsþáttar. Þegar stöðu líkanavörpunar rafrænnar skýrslugerðar eða sniðsskilgreiningar er breytt úr **Drögum** í **Lokið** verður þessi reitur sjálfkrafa fylltur út með hæsta endurskoðunarnúmeri líkansins sem er tiltækt í núverandi Finance-tilviki. Ef ný tölusetning eða nýtt tölusetningargildi er kynnt í útgáfudrögum á grunngagnalíkaninu og vísað er í það í breytanlegri líkanavörpun eða sniðsþætti skal ljúka þeim útgáfudrögum af skilgreiningu grunngagnalíkans áður en útgáfudrögum fyrir líkanavörpun rafrænnar skýrslugerðar eða sniðsskilgreiningar er lokið. Annars kemur upp undantekningin „Slóð finnst ekki“ þegar stöðu líkanavörpunar eða sniðsskilgreiningar er breytt úr **Drögum** í **Lokið**. Skilaboðin láta þig vita að í gagnalíkanavörpunina vanti tölusetningu eða tölusetningargildi sem vísað er í.

Eftirfarandi mynd sýnir eiginleika `$ReportDirection` gagnagjafans sem var skilgreindur í skilgreiningu rafræna skýrslugerðarsniðsins **Instat XML (DE) Contoso**. Skilgreiningin **Instat XML (DE) Contoso** hefur verið [afleidd](general-electronic-reporting.md#Configuration) úr skilgreiningunni **Instat XML (DE)**. Þessi gagnagjafi er skilgreindur til að nota tölusetningarlíkanið *ReportDirection* til að bjóða upp á viðeigandi uppflettireit í svarglugganum við keyrslu.

![Eiginleikar gagnagjafans af gerðinni INNSLÁTTARFÆRIBREYTA NOTANDA í svarglugganum á síðu sniðshönnuðar.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Snið innsláttarfæribreytu notanda tölusetningar

Notaðu gagnagjafa af gerðinni **Tölusetning sniðs** \> **Innsláttarfæribreyta notanda tölusetningar** til að fá eitt eða fleiri nauðsynleg gildi fyrir eina tölusetningu sniðs. Þegar gagnagjafa af þessari gerð er bætt við rafrænan skýrslugerðarþátt skal tilgreina eftirfarandi eiginleika:

- Í reitnum **Tölusetning sniðs** skal tilgreina tölusetningu breytanlegs sniðs.

> [!NOTE]
> Aðeins er hægt að skilgreina gagnagjafa af þessari gerð í umfangi breytanlegs sniðsþáttar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Keyra gildi gagnaveitu af gerðinni USER INPUT PARAMETER úr frumkóða](er-initiate-uip-data-source-value-from-source-code.md)
