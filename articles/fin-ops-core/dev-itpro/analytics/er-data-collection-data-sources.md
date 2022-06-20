---
title: Nota gagnagjafa GAGNASÖFNUNAR í rafrænum skýrslugerðarsniðum
description: Þessi grein útskýrir hvernig á að nota DATA COLLECTION gagnaveitur í rafrænum skýrslugerðum (ER).
author: NickSelin
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 7591bed5d01ce2c2f434f0e7c81e441eda98483e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883847"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>Nota gagnagjafa GAGNASÖFNUNAR í rafrænum skýrslugerðarsniðum

[!include [banner](../includes/banner.md)]

Þú getur notað rekstrarhönnuðinn á [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) ramma til að stilla sniðshluta ER lausnar sem er notuð til að búa til skjöl á útleið á mismunandi sniðum. Skipulag stigveldis fyrir skilgreindan sniðsþátt samanstendur af ýmsum gerðum af sniðsþáttum. Þessir sniðþættir eru notaðir til að fylla mynda skjöl með tilskildum upplýsingum á keyrslutíma. Sjálfgefið er, þegar þú keyrir snið rafrænnar skýrslugerðar, að sniðsþættirnir séu keyrðir í sömu röð og þeir eru settir fram í sniðsstigveldinu: eitt í einu, frá efsta til neðsta.

Þegar rafræn skýrslugerð keyrir sniðsþátt sem inniheldur bindingu er formúla þeirrar bindingar keyrð og sniðsþátturinn bætir gildinu við myndað skjal. Til dæmis getur bindingin fært gildi fyrir reitinn gagnalíkan yfir í sniðsþátt. Þú getur skilgreint gagnagjafa GAGNASÖFNUNAR til að safna gildum fyrir reiti gagnalíkans á keyrslutíma, til að leggja saman gildin og fylla út myndað skjal með söfnuðum gildum. Til að nota þessa aðferð skal breyta upphaflegri bindingu þannig að skilgreindur gagnagjafi GAGNASÖFNUNAR sé notaður til að færa gildið fyrir reit gagnalíkans yfir í sniðsþátt. Með því að færa gildi í gegnum gagnagjafa GAGNASÖFNUNAR getur þú safnað nauðsynlegum upplýsingum til frekari notkunar.

Þegar þú skilgreinir gagnagjafa GAGNASÖFNUNAR skaltu tilgreina gerð gildis sem verður stjórnað í gagnagjafanum. Eftirfarandi [gagnagerðir](er-formula-supported-data-types-primitive.md) eru sem stendur studdar fyrir söfnun gilda:

- Boole
- Dagsetning
- DateTime-gildi
- Guid
- Int64
- Heiltala
- Rauntala
- Strengur
- Tími

Þú getur notað `Collect(Value)` aðferð gagnagjafa GAGNASÖFNUNAR til að flytja gildi yfir í gagnagjafa til söfnunar. Í þessari aðferð er `Value` frumbreytan annaðhvort fasti eða gild slóð fyrir reit gagnagjafa af viðeigandi gagnagerð.

Notaðu `Result` eiginleika gagnagjafa GAGNASÖFNUNAR til að nálgast listann yfir söfnuð gildi. Þessi eiginleiki skilar [færslulista](er-formula-supported-data-types-composite.md#record-list). Færslur færslulistans innihalda `Value` reitinn sem þú getur notað til að nálgast uppsöfnuð gildi.

Sjálfgefið safnar gagnagjafi GAGNASÖFNUNAR aðeins einkvæmum gildum.

Til að safna öllum gildum skal stilla reitinn **Safna öllum gildum** fyrir skilgreindan gagnagjafa GAGNASÖFNUNAR á **Já**. Þegar reiturinn **Safna öllum gildum** er stilltur á **Já** verður færibreytustillti eiginleikinn `Sum(Flag)` í boði. Þú getur notað þennan eiginleika til að fá heildarupphæð allra safnaðra gilda fram að þessu. Í þessum eiginleika er `Flag` frumbreytan [Boole-gildi](er-formula-supported-data-types-primitive.md#boolean) sem er notað til að gefa til kynna hvort þurfi að endurstilla samtals gildið.

- Þegar gildið **Ósatt** er gefið upp er samlagningu haldið áfram úr fyrri safnaðri upphæð.
- Þegar gildið **Satt** er gefið upp er byrjað á nýrri samlagningu.

Eftirfarandi gagnagerðir eru sem stendur studdar fyrir samlagningu:

- Int64
- Heiltala
- Rauntala

Til að læra meira um þennan eiginleika skaltu ljúka við dæmið sem fylgir.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Dæmi: Skilgreina snið rafrænnar skýrslugerðar til að gera talningu og samlagningu með því að nota gagnagjafa GAGNASÖFNUNAR

Þetta dæmi sýnir hvernig notandi í hlutverki kerfisstjóra eða hagnýts ráðgjafa rafrænnar skýrslugerðar getur skilgreint snið rafrænnar skýrslugerðar sem er með gagnagjafa GAGNASÖFNUNAR sem er notaður til að reikna út hlaupandi samtölu og safna samanlögðum gildum.

Verklagsreglurnar í þessu dæmi er hægt að ljúka í USMF fyrirtækinu í Microsoft Dynamics 365 Fjármál.

### <a name="upload-and-use-the-provided-er-solution"></a>Hlaða upp og nota uppgefna lausn rafrænnar skýrslugerðar

1. [Flytja inn dæmið um skilgreiningar rafrænnar skýrslugerðar](er-defer-sequence-element.md#import-the-sample-er-configurations).
2. [Virkja skilgreiningarveitu](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [Fara yfir innflutta líkanavörpun](er-defer-sequence-element.md#review-the-imported-model-mapping).
4. [Yfirfara innflutt snið.](er-defer-sequence-element.md#review-the-imported-format)
5. [Keyra innflutt snið](er-defer-sequence-element.md#run-the-imported-format).

### <a name="run-the-format-of-the-provided-er-solution"></a>Keyra snið á uppgefinni lausn rafrænnar skýrslugerðar

1. Á síðunni **Sniðshönnuður** skal velja **Keyra**.
2. Í **Svargluggi rafrænna skýrslufæribreyta** velurðu **Í lagi**.
3. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Sótt skrá sem inniheldur niðurstöður úr upphaflegri keyrslu sniðs](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>Breyta sniði rafrænnar skýrslugerðarlausnar til að reikna út hlaupandi samtölu skatts

Ef færslumagnið er mikið meira en magnið í núverandi dæmi gæti tíminn sem fer í samlagninguna aukist og valdið vandamálum varðandi afköst. Með því að breyta stillingum sniðsins getur þú hjálpað til við að koma í veg fyrir þessi afkastavandamál. Þar sem þú hefur aðgang að skattgildum til að hafa þau með í útbúinni skýrslu getur þú endurnotað þær upplýsingar til að leggja saman skattgildi.

1. Á síðunni **Sniðshönnuður**, í flipanum **Vörpun**, skal velja **Bæta við rót**.
2. Í svarglugganum **Bæta við gagnagjafa** skal velja **Aðgerðir** \> **Gagnasafn**.
3. Í svarglugganum **Eiginleikar gagnagjafa „Gagnasöfnunar“** skal fylgja þessum skrefum:

    1. Í reitinn **Heiti** skal færa inn **CollectedTaxValues**.
    2. Í reitnum **Gerð vöru** velurðu **Rauntala**.
    3. Í reitnum **Safna öllum gildum** skal velja **Já**.
    4. Veldu **Í lagi**.

4. Veldu tölusniðsþáttinn í **Skýrsla\\Línur\\Færsla\\TaxAmount**.

    > [!NOTE]
    > Sem stendur er `@.Value` bindingin skilgreind fyrir þessa einingu. Því er myndað skjal fyllt út með skattgildum úr reitnum `model.Data.List.Value`.

5. Veljið **Breyta formúlu**.
6. Á síðunni **Formúluhönnuður** skal fylgja þessum skrefum:

    1. Í reitnum **Formúla** skal skipta út `@.Value` fyrir `CollectedTaxValues.Collect(@.Value)`.
    2. Vistaðu breytingarnar og lokaðu síðunni.

    > [!NOTE]
    > Nýja bindingin mun flytja sömu skattgildi yfir á skjal sem búið er til. Þeim gildum verður þó einnig safnað í gagnagjafanum **CollectedTaxValues**.

7. Veldu tölusniðsþáttinn í **Skýrsla\\Lína\\Færsla\\Hlaupandi samtala**.
8. Veljið **Breyta formúlu**.
9. Á síðunni **Formúluhönnuður** skal fylgja þessum skrefum:

    1. Í reitinn **Formúla** skal færa inn `CollectedTaxValues.Sum(false)`.
    2. Vistaðu breytingarnar og lokaðu síðunni.

    > [!NOTE]
    > Nýja bindingin mun flytja í myndað skjal heildarupphæð skattgilda sem hafa þegar verið slegin inn.

    ![Tölulegir þættir sem eru með uppfærðar bindingar á síðu sniðshönnuðar](./media/er-data-collection-data-sources-02.png)

10. Veldu **Vista** og síðan **Keyra**.
11. Í **Svargluggi rafrænna skýrslufæribreyta** velurðu **Í lagi**.
12. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Sótt skrá sem inniheldur niðurstöður keyrslu á breyttu sniði](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>Breyta sniðinu til að meta lista yfir innheimt skattgildi

1. Á síðunni **Sniðshönnuður**, í flipanum **Snið**, velur þú tölusniðsþáttinn **Skýrsla\\Línur\\Færsla\\Hlaupandi samtala** og fylgir svo eftirfarandi skrefum:

    1. Í reitnum **Gerð tölustafa** skal breyta gildinu úr **Rauntölu** í **Heiltölu**.
    2. Í reitnum **Tölustafasnið** skal breyta gildinu úr **F2** í **F0**.

3. Í flipanum **Vörpun** skal velja **Breyta formúla**.
4. Á síðunni **Formúluhönnuður** skal fylgja þessum skrefum:

    1. Í reitinn **Formúla** skal færa inn `COUNT(CollectedTaxValues.Result)`.
    2. Vistaðu breytingarnar og lokaðu síðunni.

    > [!NOTE]
    > Nýja bindingin mun færa yfir í myndað skjal færslufjöldann úr listanum þar sem skattgildunum er safnað saman.

5. Veldu **Vista** og síðan **Keyra**.
6. Í **Svargluggi rafrænna skýrslufæribreyta** velurðu **Í lagi**.
7. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Sótt skrá sem inniheldur niðurstöður annarrar keyrslu á breyttu sniði](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Ef ég þarf að reikna út hlaupandi samtölur og safna gögnum, hver er munurinn á milli þess að nota gagnagjafa GAGNASÖFNUNAR og nota innbyggðar aðgerðir GAGNASÖFNUNAR?

Nota má bæði gagnagjafa GAGNASÖFNUNAR og innbyggðar aðgerðir [GAGNASÖFNUNAR](er-functions-category-data-collection.md) fyrir gagnasöfnun, samlagningu og talningu út frá upplýsingum sem eru fluttar yfir í myndað skjal á útleið. Þegar þú hinsvegar tekur ákvörðun um hvora leiðina eigi að nota þarftu að velta fyrir þér eftirfarandi atriðum.

| Gagnaveita | Innbyggðar aðgerðir |
|-------------| ------------------ |
| Aðeins gildum er safnað. | <p>Nefndum gildum er safnað. Því er hægt að reikna samtölur fyrir aðskilda flokka af gildum.</p><p>Auk þess er hægt að draga flokka út sem lista.</p><p>Einnig er hægt að safna textagildum.</p> |
| Einkvæmum gildum er sjálfkrafa safnað. | Viðbótarstillingar eru nauðsynlegar til að draga út lista yfir einkvæm gildi úr söfnuðum gildum. |
| Afköst ráðast af magni safnaðra gilda. | Í raun fara afköst ekki eftir magni uppsafnaðra gilda. |
| Þessi leið virkar fyrir allar gerðir skjala á útleið. | Þessi leið virkar aðeins fyrir textaskjöl og XML-skjöl. |

## <a name="additional-resources"></a>Frekari upplýsingar

- [Skilgreina snið til að gera talningu og samlagningu](./tasks/er-format-counting-summing-1.md)
- [Fresta keyrslu raðeininga á sniði rafrænnar skýrslugerðar](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
