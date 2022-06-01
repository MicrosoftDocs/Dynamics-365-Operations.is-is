---
title: Notaðu USER INNPUT PARAMETER gagnagjafa til að tilgreina færibreytur fyrir skýrslu
description: Þetta efni útskýrir hvernig á að nota USER INNPUT PARAMETER gagnagjafa til að tilgreina færibreytur fyrir skýrslur sem þú býrð til.
author: NickSelin
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 4e431c9dd59080af17fa073547073037ba233288
ms.sourcegitcommit: 6c1bf233748c4bc70fc5a1a9711758cdfd9e07dc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782544"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Notaðu USER INNPUT PARAMETER gagnagjafa til að tilgreina færibreytur fyrir skýrslu

[!include[banner](../includes/banner.md)]

Þegar þú hannar [Rafræn skýrslugerð](general-electronic-reporting.md) (ER) [módelkortlagningu](er-overview-components.md#model-mapping-component) og ER [sniði](er-overview-components.md#format-component) hluti, getur þú notað gagnagjafa a *NOTANDA INNTAK FRÆÐI* tegund til að fá nauðsynleg gildi sem hægt er að tilgreina í gagnafærslureitum í svarglugganum á keyrslutíma, áður en keyrsla á ER sniði hefst. Þetta efni lýsir *NOTANDA INNTAK FRÆÐI* gagnaheimildir sem nú eru studdar.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a> Lögboðnar eiginleikar

Þú verður að tilgreina eftirfarandi eiginleika fyrir gagnagjafa hvers og eins *NOTANDA INNTAK FRÆÐI* tegund:

- Í **Nafn** reit, sláðu inn innra heiti gagnagjafans. Þú getur notað þetta nafn í öðrum [tjáningar](er-formula-language.md) og bindingar á stilltu líkanavörpuninni eða sniðhlutanum.

## <a name="optional-properties"></a><a name="optional-properties"></a> Valfrjálsar eignir

Þú getur valfrjálst tilgreint eftirfarandi eiginleika fyrir gagnagjafa a *NOTANDA INNTAK FRÆÐI* tegund:

- Í **Merki** reit, tilgreindu merkimiðann sem er notaður fyrir tengda gagnafærslureitinn í svarglugganum á keyrslutíma. Þú getur bætt við mismunandi merkitexta fyrir mismunandi tungumálakóða með því að virkja **Merki** reit og velja síðan **Þýða**.
- Í **Hjálp** reit, tilgreindu hjálpartextann sem er sýndur við hönnunartíma neðst í **Sniðhönnuður** síðu eða **Módelkortahönnuður** síðu þegar breytanlegur gagnagjafi a *NOTANDA INNTAK FRÆÐI* gerð er valin. Þessi texti gæti veitt frekari upplýsingar um gagnagjafann til að hjálpa notendum þegar þeir stilla breytanlegt snið eða líkanakortlagningarhluta. Þú getur bætt við mismunandi hjálpartexta fyrir mismunandi tungumálakóða með því að velja **Þýða**.

    > [!NOTE]
    > The **Þýða** hnappinn sem þú getur notað til að bæta við [tungumálabundin merki og texti](er-design-multilingual-reports.md#format-component) verður aðeins tiltækt eftir að þú bætir við gagnagjafanum, vistar breytingarnar og opnar síðan gagnagjafann aftur til að breyta.

- Í **Lesið aðeins** reit, stilltu tjáningu sem skilar a *[Boolean](er-formula-supported-data-types-primitive.md#boolean)* gildi.

    - Ef stillta segðin skilar gildinu fyrir **Satt** á keyrslutíma birtist tengdur gagnainnsláttur reiturinn dimmur í svarglugganum og þú getur ekki breytt gildi hans.
    - Ef stillta segðin skilar gildinu fyrir **Rangt** á keyrslutíma, eða ef engin tjáning er stillt, er tengdur gagnafærslureitur tiltækur í svarglugganum og þú getur breytt gildi hans.

- Í **Sjálfgefið gildi** reit, stilltu segð sem skilar gildi færibreytutegundarinnar sem vísað er til. Þetta gildi er hægt að nota til að fylla út sjálfgefið gildi fyrir viðkomandi gagnafærslureit í svarglugganum á keyrslutíma.

    Þegar þú keyrir ER snið er gildið sem þú slærð inn í tengda gagnafærslureitinn í svarglugganum á keyrslu vistað í minni sem áður notað gildi. Áður notuð gildi eru vistuð fyrir sig fyrir hvern reit, keyrandi ER snið, núverandi notandi og núverandi skipulag (fyrirtæki).

    - Stilltu **Alltaf endurstillt á sjálfgefið gildi** valmöguleika til **Já** ef gildið sem er skilað af **Sjálfgefið gildi** tjáning ætti alltaf að nota sem sjálfgefið gildi, óháð gildinu sem áður var notað.
    - Stilltu **Alltaf endurstillt á sjálfgefið gildi** valmöguleika til **Nei** ef gildið sem er skilað af **Sjálfgefið gildi** tjáningargildi ætti aðeins að nota sem sjálfgefið gildi þegar áður notað gildi vantar.

    > [!NOTE]
    > Ef þú stillir **Alltaf endurstillt á sjálfgefið gildi** valmöguleika til **Já**, segð verður að vera stillt í **Sjálfgefið gildi** sviði.

- Ef þú stillir **Leyfa margfalt val** valmöguleika til **Já**, þú getur valið mörg gildi fyrir stilltu færibreytuna á keyrslutíma. Ef þú stillir það á **Nei**, þú getur aðeins valið eitt gildi.

    > [!NOTE]
    > Þessi valkostur á ekki við um alla *NOTANDA INNTAK FRÆÐI* tegundir. Á hönnunartíma er gerð undantekning til að upplýsa notandann um að stillta inntaksfæribreytan notanda styður ekki margfalt val og að aðeins sé hægt að velja eða slá inn eitt gildi.
    >
    > Ef þú stillir **Leyfa margfalt val** valmöguleika til **Já**, og þú tilgreindir tjáningu í **Sjálfgefið gildi** reit, þá er hægt að nota þá tjáningu til að stilla aðeins eitt sjálfgefið gildi.

- Veldu **Breyta sýnileika** valmöguleika til að tilgreina hvort stilltu færibreytuna eigi að birtast í svarglugganum á keyrslutíma.

    > [!NOTE]
    > Sjálfgefinn sýnileiki gagnagjafa a *NOTANDA INNTAK FRÆÐI* gerð fer eftir ER íhlutnum sem heldur þeim.
    >
    > - Ef gagnagjafi er stilltur í sniðhlutanum er hann sjálfgefið sýnilegur.
    > - Ef gagnagjafi er stilltur í líkanavörpunarhlutanum er hann aðeins sýnilegur ef gildi gagnagjafans hefur áhrif á útkomuna þegar ER íhlutur er keyrður. Til dæmis bættir þú við gagnagjafa en notaðir hann ekki í tjáningum og bindingum núverandi líkanskortshluta. Í þessu tilviki, sjálfgefið, mun viðkomandi gagnafærslureitur ekki birtast í svarglugganum á keyrslutíma. 

    Á **Formúluhönnuður** síðu, í **Formúla** reit, stilltu tjáningu sem skilar a *Boolean* gildi.

    - Ef stillt segðin skilar gildinu fyrir **Satt** á keyrslutíma, eða ef engin tjáning er stillt, er tengdur gagnafærslureitur sýnilegur í svarglugganum á keyrslutíma.
    - Ef stillt segðin skilar gildinu fyrir **Rangt**, tengdur gagnainnsláttur reiturinn er falinn í svarglugganum á keyrslutíma. Þegar það er kallað af öðrum tjáningum á keyrslutíma skilar það sjálfgefnu gildi, áður notaðu gildi, eða sjálfgefið fyrir núverandi gagnategundargildi, allt eftir öðrum stillingum.

## <a name="type-specific-properties"></a>Tegundarákveðnir eiginleikar

### <a name="application-dependent-user-input-parameter"></a>Forritsháð inntaksfæribreyta notanda

Notaðu gagnagjafa á **Almennt** \> **Innsláttarfæri notanda** gerð til að fá tilskilið gildi eða gildi gagnategundar sem er tilgreind fyrir núverandi tilvik af Microsoft Dynamics 365 Fjármálaumsókn. Þegar þú bætir gagnagjafa af þessari gerð við ER íhlut skaltu tilgreina eftirfarandi eiginleika:

- Í **Heiti rekstrargagnategundar (EDT, enum)** reit, veldu forrit [útbreidd gagnategund (EDT)](../extensibility/extensible-edts.md) eða umsóknarupptalningu.

> [!NOTE]
> Við mælum með að þú skoðir tjáningarnar sem eru stilltar í **Lesið aðeins** og **Sjálfgefið gildi** reiti þegar þú breytir **Heiti rekstrargagnategundar (EDT, enum)** tilvísun í breytanlegri gagnagjafa um þetta *NOTANDA INNTAK FRÆÐI* tegund.

Eftirfarandi mynd sýnir eiginleika`$TaxRegNum` gagnagjafi sem var stilltur í **Instat XML (DE)** ER snið stillingar. Þessi gagnagjafi er stilltur til að nota *Lýsing* EDT að bjóða upp á **Skattskráningarnúmer** gagnainnsláttarreiturinn í svarglugganum á keyrslutíma.

![Eiginleikar gagnagjafa USER INNPUT PARAMETER sláðu inn svargluggann á Format designer síðunni.](./media/er-user-input-parameter-data-sources-01.png)

Eftirfarandi mynd sýnir gluggann sem er sýndur á keyrslutíma þegar **Instat XML (DE)** ER snið stillingar er keyrt á [mynda](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) Intrastat yfirlýsingunni. Taktu eftir því að stillt **Skattskráningarnúmer** reiturinn er tiltækur fyrir gagnafærslu.

![Intrastat Report valmynd af ER sniði sem er í gangi á Intrastat síðunni.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Innsláttarfæribreyta notanda í tölusetningu gagnalíkans

Notaðu gagnagjafa á **Gagnalíkan** \> **Upptalning notendainntaksfæribreyta** gerð til að fá tilskilið gildi eða gildi eins gagnalíkans [upptalningu](er-formula-supported-data-types-primitive.md#enumeration). Þegar þú bætir gagnagjafa af þessari gerð við ER íhlut skaltu tilgreina eftirfarandi eiginleika:

- Í **Fyrirmynd** reit, tilgreinið tilvísun í grunngagnalíkanið.
- Í **Upptalning líkana** reit, tilgreinið tilvísun í upptalningu á gagnalíkaninu sem vísað er til.
- Í **Útgáfa** reit, veldu endurskoðunarnúmer ER gagnalíkansins sem inniheldur líkanaupptalninguna sem vísað er til.

    > [!TIP]
    > Á hönnunartíma geturðu skilið eftir **Útgáfa** reiturinn auður til að fá aðgang að lista yfir upptalningar fyrir íhlutinn sem vísað er í gagnalíkanið sem er í drögum að útgáfu samsvarandi ER gagnalíkans uppsetningu. Á þennan hátt geturðu samtímis breytt drögum útgáfa af líkanavörpun eða sniðhluta og drögum útgáfa af grunngagnalíkanihluta.
    >
    > Athugið hins vegar að **Útgáfa** reitinn má aðeins skilja eftir auðan í drögum að útgáfu líkanavörpunar eða sniðshluta. Þegar þú breytir stöðu ER líkanavörpun eða sniðstillingu frá **Drög** til **Lokið**, þessi reitur er sjálfkrafa fylltur út með hæsta endurskoðunarnúmeri líkansins sem er tiltækt í núverandi Finance tilviki. Ef þú kynnir nýja upptalningu eða nýtt upptalningargildi í drögum útgáfu grunngagnalíkans þíns og vísar til þess í breytanlegri líkanavörpun eða sniðshluta skaltu klára þá drög að útgáfa af grunngagnalíkaninu áður en drög að útgáfu ER þíns líkanakortlagningu eða sniðstillingu er lokið. Annars verður undantekningin „Slóð fannst ekki“ þegar þú breytir stöðu líkanavörpunar eða sniðstillingar frá **Drög** til **Lokið**. Skilaboðin munu upplýsa þig um að tilvísað upptalningu eða upptalningargildi vantar í grunngagnalíkanið.

Eftirfarandi mynd sýnir eiginleika`$ReportDirection` gagnagjafi sem var stilltur í **Instat XML (DE) Contoso** ER snið stillingar. The **Instat XML (DE) Contoso** uppsetning hefur verið [afleidd](general-electronic-reporting.md#Configuration) frá **Instat XML (DE)** stillingar. Þessi gagnagjafi er stilltur til að nota *Report Direction* líkanatalning til að bjóða upp á viðeigandi uppflettingarreit í svarglugganum á keyrslutíma.

![Eiginleikar gagnagjafans USER INNPUT PARAMETER sláðu inn svargluggann á Format designer síðunni.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Snið innsláttarfæribreytu notanda tölusetningar

Notaðu gagnagjafa á **Sniðtalning** \> **Upptalning notendainntaksfæribreyta** tegund til að fá tilskilið gildi eða gildi fyrir upptalningu á einu sniði. Þegar þú bætir gagnagjafa af þessari gerð við ER íhlut skaltu tilgreina eftirfarandi eiginleika:

- Í **Sniðtalning** reit, tilgreindu upptalningu á breytanlegu sniði.

> [!NOTE]
> Gagnauppsprettur af þessari gerð er aðeins hægt að stilla á umfangi breytanlegs sniðshluta.

## <a name="additional-resources"></a>Frekari upplýsingar

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Keyra gildi gagnaveitu af gerðinni USER INPUT PARAMETER úr frumkóða](er-initiate-uip-data-source-value-from-source-code.md)
