---
title: Styðja breytubreytt símtöl ER gagnalíkana
description: Þetta efnisatriði útskýrir hvernig á að innleiða símtöl með færibreytum af rafrænum skýrslugerð (ER) gagnalíkönum.
author: NickSelin
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 968b0769607e9fdbed57c25b727ed44988a92913
ms.sourcegitcommit: 399d0d3f8e2ebb81b6b9d640365ebe182690bab2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419514"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>Styðja breytubreytt símtöl ER gagnalíkana

[!include [banner](../includes/banner.md)]

Til að búa til viðskiptaskjöl stillirðu [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) lausn sem inniheldur eftirfarandi ER hluti:

- **[Snið](er-overview-components.md#format-component)** – Þessi hluti tilgreinir uppbyggingu viðskiptaskjals.
- **Snið kortlagning** – Þessi hluti stjórnar því hvernig viðskiptaskjal er fyllt út á keyrslutíma.
- **[Líkanskortlagning](er-overview-components.md#model-mapping-component)** – Þessi hluti tilgreinir hvað gögnin draga úr forritinu í sniðkortlagningu.
- **[Gagnalíkan](er-overview-components.md#data-model-component)** – Þessi hluti sendir upplýsingar á milli einstakra íhluta.

Þegar þú keyrir ER snið er sérhver sniðþáttur keyrður, byrjað á rótarsniði. Alltaf þegar sniðþáttur sem er keyrður inniheldur bindingu við a [gagnagjafa](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents), gagnagjafinn er keyrður til að afhenda væntanleg gögn og nota þau til að fylla út sniðþáttinn. Þegar gagnagjafi á *Fyrirmynd* gerð er kölluð, viðeigandi líkanskortlagning er kölluð til að draga gögn út úr forritinu, byggt á líkanakortlagningarstillingum.

Áður var ekki hægt að stilla þessi líkankortlagningarsímtöl til að gera þau háð rökfræði sniðsins sem er keyrt. Aðeins eftirfarandi gagnaflæði var stutt.

<table>
<tbody>
<tr align="center">
<td>
<b>Snið</b><br>
Snið&nbsp; þáttur<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp; beiðni&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;&lt;
</td>
<td><b>Snið&nbsp; kortlagningu</b><br>
Gagnaveita<br>
&nbsp;
</td>
<td>
<i>Gögn&nbsp; fyrirmynd</i><br>
&gt;&nbsp; beiðni&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;&lt;
</td>
<td>
<b>Fyrirmynd&nbsp; kortlagningu</b><br>
Gögn&nbsp; heimild<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp; beiðni&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;&lt;
</td>
<td>
<b>Tafla</b><br>
Færsla<br>
Reitur
</td>
</tr>
</tbody>
</table>

Hins vegar, í útgáfu 10.0.15 og nýrri, er hægt að stilla reiti gagnalíkana sem aðeins er hægt að kalla fram þegar gildi stilltu færibreytanna eru gefin upp. Þegar slíkur reitur er stilltur og kallaður frá sniðihluta verður að gefa upp nauðsynlegar færibreytur í sniðbindingu sem rök fyrir símtalinu. Í þessum tilvikum er hægt að tilgreina gildi röksemda út frá sniðssértækum gildum. Þess vegna getur þú notað **dynamic runtime parametrisation** fyrir gagnalíkanasímtöl til að styðja við eftirfarandi gagnaflæði.

<table>
<tbody>
<tr align="center">
<td>
<b>Snið</b><br>
Snið&nbsp; þáttur&nbsp; 1<br>
<br>
Snið&nbsp; þáttur&nbsp; 2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp; beiðni&nbsp; 1&nbsp;&gt;<br>
&lt;&nbsp; gildi&nbsp; 1&nbsp;&lt;<br>
&gt;&nbsp; beiðni&nbsp; 2&nbsp;&gt;<br>
&lt;&nbsp; gildi&nbsp; 3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Snið&nbsp; kortlagningu</b><br>
Gögn&nbsp; heimild&nbsp; 1<br>
&nbsp;<br>
<b>gildi2=Func(gildi1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Gögn&nbsp; fyrirmynd</i><br>
&gt;&nbsp; reit 1&nbsp;&gt;<br>
&lt;&nbsp; gildi&nbsp; 1&nbsp;&lt;<br>
<b>&gt;&nbsp; reit2(gildi2)&nbsp;&gt;</b><br>
&lt;&nbsp; gildi&nbsp; 3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Fyrirmynd&nbsp; kortlagningu</b><br>
Gögn&nbsp; heimild&nbsp; 1<br>
<br>
Gögn&nbsp; heimild&nbsp; 2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp; beiðni&nbsp; 1&nbsp;&gt;<br>
&lt;&nbsp; gildi&nbsp; 1&nbsp;&lt;<br>
&gt;&nbsp; beiðni&nbsp; 2&nbsp;&gt;<br>
&lt;&nbsp; gildi&nbsp; 3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Tafla&nbsp; 1</b><br>
Met&nbsp; 1<br>
Field&nbsp; 1<br>
<b>Tafla&nbsp; 2</b><br>
Met&nbsp; 2<br>
Field&nbsp; 2
</td>
</tr>
</tbody>
</table>

Nýja virknin gerir þér kleift að stilla símtalið í hvaða gagnalíkansvið sem er [*Met*](er-formula-supported-data-types-composite.md#record) eða [*Met listi*](er-formula-supported-data-types-composite.md#record-list) tegund. Eftirfarandi gagnategundir eru studdar fyrir færibreytur gagnalíkanareits:

- [Boole-gildi](er-formula-supported-data-types-primitive.md#boolean)
- [Gámur](er-formula-supported-data-types-composite.md#container)
- [Dagsetning](er-formula-supported-data-types-primitive.md#date)
- [DateTime-gildi](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Heiltala](er-formula-supported-data-types-primitive.md#integer)
- [Rauntala](er-formula-supported-data-types-primitive.md#real)
- [Strengur](er-formula-supported-data-types-primitive.md#string)

Þú getur tilgreint hverja færibreytu gagnalíkanareits þar sem hægt er að gefa upp röksemdafærsluna sem eitt gildi skilgreindrar gagnagerðar og [*lista*](er-formula-supported-data-types-composite.md#record-list) slíkra verðmæta.

> [!NOTE]
> Sjálfgefið gildi fyrir færibreytu gagnalíkanareits er ekki stutt. Ef þú bætir færibreytu við reit í gagnalíkani og útgáfan af því gagnalíkani hefur þegar verið gefin út og birt verður þú [endurbæta](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) allar samsvarandi líkanavörp og snið við nýju útgáfuna af þessu líkani, vegna þess að þessi gagnalíkanbreyting er ekki afturábaksamhæf.

Þú getur stillt reiti með breytibreyttum gagnalíkönum til að gera líkanakortlagningarsímtöl sniðssértæk. Þessi nálgun getur hjálpað þér að fækka líkanavörpunum sem þarf að stilla fyrir mörg snið eins gagnalíkans. Þú getur líka notað þessa nálgun til að bæta framkvæmdarafköst sniðanna þinna og draga úr þeim tíma sem þarf til að búa til viðskiptaskjöl. Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka dæminu í þessu efni.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Dæmi: Notaðu símtöl með færibreytum af ER gagnalíkönum

Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænna skýrslna getur hannað ER lausn sem inniheldur gagnalíkan, líkanavörpun og snið ER íhlut sem eru stilltir til að kalla líkanavörpun frá sniði með því að útvega rök fyrir símtalinu, en gildi þess hefur verið reiknað út á keyrslutíma með því að nota formúlu hlaupasniðsins. 

Hægt er að ljúka skrefunum í **DEMF** fyrirtækinu. Engar kóðabreytingar eru nauðsynlegar. 

Í þessu dæmi muntu búa til nauðsynlega ER [stillingar](general-electronic-reporting.md#Configuration) fyrir **Litware, Inc.** sýnishorn fyrirtæki. Gakktu úr skugga um að stillingarveitan fyrir **Litware, Inc.** (`http://www.litware.com`) sýnishornsfyrirtæki er skráð fyrir ER ramma og að það sé merkt sem **Virkur**. Ef þessi stillingarveita er ekki á listanum eða ef hún er ekki merkt sem **Virkur**, fylgdu skrefunum í [Búðu til stillingarveitu og merktu hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="business-scenario"></a>Sviðsmynd fyrirtækis

Þú ert með ER lausn sem inniheldur snið sem þú getur keyrt til að búa til rafrænt skjal í endurskoðunarskyni. Þetta snið inniheldur skattfærslur sem tengjast sölupantanir og innkaupapantanir og hafa nauðsynlegar upplýsingar, svo sem færsludagsetningu og skattgildi. Frá og með nýju fjárhagsári hefur uppbygging þessa skjals breyst. Þú verður nú að leggja fram aukið skjal sem inniheldur viðbótarupplýsingar (nöfn) allra aðila (viðskiptavina og lánardrottna) þar sem færslur eru sýndar á mynduðum skýrslum. Þess vegna verður þú að breyta ER lausninni þinni þannig að hún búi til skjöl sem uppfylla þessa nýju kröfu.

### <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ER ramma til að hanna nýja ER lausn.

### <a name="design-a-domain-specific-data-model"></a>Hanna gagnalíkan fyrir sérstakt lén

Þú verður að búa til nýja ER-stillingu sem inniheldur nauðsynlegan gagnalíkan íhlut. Þetta gagnalíkan verður notað sem gagnagjafi síðar, þegar þú hannar ER snið til að búa til endurskoðunarskýrslu.

Fylgdu þessum skrefum til að flytja inn nauðsynlegt gagnalíkan úr XML skrá sem er útveguð af Microsoft.

1. Sækja [Dæmi um endurskoðunarmodel.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) skrá og vistaðu hana á tölvunni þinni.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á **Stillingar** síðu, á aðgerðarrúðunni, veldu **Skipti** \> **Hlaða úr XML skrá**.
5. Veldu **Skoðaðu**, og finndu síðan og veldu **Dæmi um endurskoðunarmodel.version.1.xml** skrá.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

    ![Innflutt ER gagnalíkanstilling á síðunni Stillingar.](./media/er-data-model-parameterized-calls-imported-model.png)

Eftirfarandi mynd sýnir breytanlegu útgáfu af stilltu gagnalíkaninu á **Hönnuður gagnalíkana** síðu.

![Uppbygging ER gagnalíkans á síðunni Gagnalíkanahönnuður.](./media/er-data-model-parameterized-calls-model1.png)

Eins og er er líkanið hannað til að afhjúpa aðeins skattfærslur sem hafa nauðsynlegar upplýsingar.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Hanna líkanavörpun fyrir skilgreint gagnalíkan

Sem notandi í hlutverki þróunaraðila rafrænna skýrslna verður þú að búa til nýja ER-stillingu sem inniheldur líkanavörpunaríhlut fyrir sýnishorn endurskoðunargagnalíkans. Þessi hluti útfærir uppsetta gagnalíkanið fyrir Microsoft Dynamics 365 Finance og er sérstakt fyrir það app. Skilgreina verður íhlut líkanavörpunar til að tilgreina hugbúnaðarhluti sem þarf að nota til að fylla út skilgreint gagnalíkan með forritsgögnum við keyrslu. Til að klára þetta verkefni verður þú að skilja hvernig gagnaskipulag skattaviðskiptalénsins er útfært í Finance.

Fylgdu þessum skrefum til að flytja inn nauðsynlega líkanavörpun úr XML-skrá sem er útveguð af Microsoft.

1. Sækja [Dæmi um úttektarlíkan mapping.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) skrá og vistaðu hana á tölvunni þinni.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á **Stillingar** síðu, á aðgerðarrúðunni, veldu **Skipti** \> **Hlaða úr XML skrá**.
5. Veldu **Skoðaðu**, og finndu síðan og veldu **Dæmi um úttektarlíkan mapping.version.1.1.xml** skrá.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

    ![Innflutt ER líkanskortstillingar á síðunni Stillingar.](./media/er-data-model-parameterized-calls-imported-mapping.png)

Eftirfarandi mynd sýnir breytanlega útgáfu af stilltu líkanavörpuninni á **Módelkortahönnuður** síðu.

![Uppbygging ER líkanakortlagningar á hönnuðarsíðu líkanakortlagningar.](./media/er-data-model-parameterized-calls-mapping1.png)

Eins og er er líkanskortlagningin hönnuð til að afhjúpa skattfærslur sem hafa nauðsynlegar upplýsingar. Það sækir þessar upplýsingar frá`TaxTrans` forritatöflu með því að nota stillt`TaxTrans` og`TaxTransFiltered` ER gagnaheimildir.

### <a name="design-a-new-format"></a>Hannaðu nýtt snið

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar þarf að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur sniðs hluta. Þú verður að stilla sniðhlutinn til að fylla út myndaðar skýrslur með skattfærslum sem hafa allar nauðsynlegar upplýsingar.

Fylgdu þessum skrefum til að flytja inn áskilið snið úr XML skrá sem er útveguð af Microsoft.

1. Sækja [Dæmi um endurskoðunarsnið.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) skrá og vistaðu hana á tölvunni þinni.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á **Stillingar** síðu, á aðgerðarrúðunni, veldu **Skipti** \> **Hlaða úr XML skrá**.
5. Veldu **Skoðaðu**, og finndu síðan og veldu **Dæmi um endurskoðunarsnið.version.1.1.xml** skrá.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

    ![Innflutt ER-sniðsstilling á síðunni Stillingar.](./media/er-data-model-parameterized-calls-imported-format.png)

Eftirfarandi mynd sýnir breytanlega útgáfu af stilltu sniðinu á **Sniðhönnuður** síðu.

![Uppbygging ER sniðsins á síðunni Format designer.](./media/er-data-model-parameterized-calls-format1.png)

ER sniðið er stillt til að búa til skýrslu sem textaskrá á CSV-sniði (comma-separated values).

### <a name="run-the-imported-format"></a>Keyrðu innflutta sniðið

1. Á **Stillingar** síðu, veldu **Dæmi um endurskoðunarsnið** stillingar og veldu síðan á aðgerðarrúðunni **Hlaupa**.
2. Í **Rafræn skýrslufæribreytur** valmynd, á **Skrár til að hafa með** flipa, veldu **Sía**.
3. Tilgreindu skilyrði til að velja skattfærslur á **PIV-110000004** og **INV-10000001** fylgiskjölum.
4. Veldu **Í lagi**.
5. Veldu **Í lagi**.
6. Skoðaðu myndað skjal sem inniheldur skattfærslur á völdum fylgiskjölum.

    ![Forskoðun á mynduðu skjali með skattfærslum.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>Stilltu innfluttu ER lausnina

Samkvæmt nýju kröfunni verður skjalið sem þú verður að leggja fram innihalda nöfn viðskiptavina og söluaðila sem eiga viðskipti með. Þess vegna verður þú að breyta innfluttu ER lausninni þannig að hún myndar skjal sem uppfyllir þessa nýju kröfu.

Ákveða hvernig þú vilt innleiða nauðsynlegar breytingar á innfluttum ER íhlutum.

Augljós aðferð er að innleiða eftirfarandi breytingar:

- Bættu nýju við í gagnalíkaninu þínu`Transaction.Party.Name` gagnalíkan sviði *Strengur* tegund.
- Í líkanavörpunni skaltu stilla bindinguna fyrir nýja gagnalíkanreitinn með því að nota tiltæk töflutengsl til að fá aðgang að viðeigandi skrá yfir`DirPartyTable` umsóknartöflu og sæktu gildið á`Name` sviði frá því.

Þó að þessi nálgun virki gæti hún valdið afköstum í SQL gagnagrunninum vegna þess`TaxTrans` er færslutaflan og getur því innihaldið mikið magn af færslum. Í þessu tilviki er fjöldi símtala til`DirPartyTable` verður að jafna fjölda skráa í`TaxTrans` töflu sem getur valdið frammistöðuvandamálum.

Að öðrum kosti gætirðu innleitt eftirfarandi breytingar:

- Bættu nýju við í gagnalíkaninu þínu`Party` rót og nýja`Party.Name` sviði.
- Í líkanavörpun þinni skaltu bæta við nýjum gagnagjafa sem mun sameina allar skrár yfir töflur sem eru notaðar í töflusamböndum til að fá aðgang að viðkomandi skrá yfir`DirPartyTable` umsóknartafla, frá og með`TaxTrans` borð.

Þó að þessi nálgun virki gæti hún valdið minnisnotkunarvandamálum. Jafnvel þegar ný [GANGA TIL](er-join-data-sources.md) gagnagjafi er keyrt sem ein SQL beiðni til gagnagrunns forritsins til að koma í veg fyrir afköst gagnagrunnsvandamála, niðurstaðan verður að vera sótt í minni umsóknarþjónsins. Vegna þess að fjöldi skráa og fjöldi reita í þeim skrám verður nokkuð mikill gæti þessi aðferð valdið mjög mikilli minnisnotkun. Undantekning úr minni runtime gæti jafnvel verið hent.

Þú getur útfært breytingarnar þegar keyrt snið safnar, í minni, einstökum auðkenniskóðum viðskiptavina og lánardrottna fyrir allar skattfærslur sem verða kynntar á myndaðri skýrslu. Vegna þess að aðeins ætti að geyma einstaka kóða, mun endanlegt sett af kóða ekki vera nógu stórt til að hafa áhrif á minnisnotkun. Kóðasamstæðan verður síðan send til líkanvörpunar sem rök fyrir öðru símtali gagnagjafans *Fyrirmynd* tegund. Byggt á því símtali mun líkankortlagningin keyra nýjan ER gagnagjafa sem gerir eina SQL beiðni til gagnagrunns forritsins til að sækja, frá`DirPartyTable` töflu, skrár aðeins fyrir þá aðila sem eru með kóða í meðfylgjandi kóðasetti.

### <a name="adjust-the-imported-data-model"></a>Stilltu innfluttu gagnalíkanið

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á **Stillingar** síðu, í stillingartrénu í vinstri glugganum, veldu **Dæmi um endurskoðunarlíkan**.
3. Á **Útgáfur** Flýtiflipi, veldu útgáfu **2** sem hefur stöðu á **[Drög](general-electronic-reporting.md#component-versioning)**.
4. Veldu flýtiflipann **Stillingarhlutar**.
5. Veldu **Hönnuður** til að opna gagnalíkanið til að breyta.
6. Á **Gagnalíkan** síðu, vertu viss um að`Root` reiturinn er valinn og veldu síðan **Nýtt**.
7. Í fellilistanum skaltu fylgja þessum skrefum:

    1. Í **Nýr hnút sem** reitahópur, veldu **Barn virks hnúts** valmöguleika.
    2. Í **Nafn** reit, slá inn **Partí**.
    3. Í reitnum **Gerð vöru** velurðu **Skráalisti**.
    4. Veldu **Bæta við** til að klára að bæta við nýja reitnum.

8. Gakktu úr skugga um að`Root.Party` reiturinn er valinn og síðan á **Hnútur** flipa, veldu **Færibreytur**.
9. Í **Færibreytur** valmynd, fylgdu þessum skrefum:

    1. Á **Færibreytur** flipa, veldu **Nýtt**.
    2. Í **Nafn** reit, slá inn **PartyRefRecId**.
    3. Í **Tegund** reit, veldu **Int64**.
    4. Veldu **Listi** gátreit.
    5. Veldu **Allt í lagi** til að klára að slá inn færibreytur.

    > [!NOTE]
    > Þú stilltir bara`Root.Party` gagnalíkan reit sem reit sem er kallað þegar gildi er gefið upp í **PartyRefRecId** breytu. Þetta gildi verður að vera til staðar í listanum yfir færslur sem innihalda a`Value` sviði á *Int64* gagnategund.

    ![Parameters valmynd.](./media/er-data-model-parameterized-calls-model2a.png)

10. Gakktu úr skugga um að`Root.Party` reiturinn er enn valinn og veldu síðan **Nýtt**.
11. Í fellilistanum skaltu fylgja þessum skrefum:

    1. Í **Nýr hnút sem** reitahópur, veldu **Barn virks hnúts** valmöguleika.
    2. Í **Nafn** reit, slá inn **Nafn**.
    3. Í reitnum **Gerð vöru** velurðu **Strengur**.
    4. Veldu **Bæta við** til að klára að bæta við nýja reitnum.

12. Veldu **Vista**, og lokaðu **Gagnalíkan** síðu.

    ![Uppbygging aðlagaðs ER gagnalíkans á síðunni Gagnalíkönhönnuður.](./media/er-data-model-parameterized-calls-model2b.png)

13. Á **Útgáfur** Hraðflipi, fyrir útgáfu **2**, veldu **Breyta stöðu** \> **Heill**. Veljið síðan **Í lagi**.

    > [!NOTE]
    > Breytingar á gagnalíkaninu þínu eru geymdar í annarri endurskoðun á **Dæmi um endurskoðunarlíkan** gagnalíkan hluti sem er staðsettur í annarri útgáfu af **Dæmi um endurskoðunarlíkan** ER stillingar.

![Uppfærð uppsetningu ER gagnalíkans á síðunni Stillingar.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>Stilltu innfluttu líkanavörpunina

1. Á **Stillingar** síðu, í stillingartrénu í vinstri glugganum, stækkaðu **Dæmi um endurskoðunarlíkan**.
2. Veldu **Dæmi um kortlagningu endurskoðunarlíkana**, og síðan, á **Útgáfur** Flýtiflipi, veldu seinni kortlagningarútgáfuna sem er byggð á fyrstu útgáfu gagnalíkans (útgáfa **1.2**), og það hefur stöðuna **Drög**.
3. Veldu **Endurreikna grunn**.
4. Í **Markútgáfa** reit, leyfi útgáfu **2** af **Dæmi um endurskoðunarlíkan** grunn líkan.
5. Veldu **Allt í lagi** til að endurbyggja og samræma líkanakortlagningu við nýlegar breytingar á gagnalíkönum.

    Taktu eftir að útgáfunúmer breytanlegrar líkanavörpunar þíns hefur breyst frá **1.2** til **2.2** til að gefa til kynna að önnur gerð útgáfan sé notuð sem grunn.

6. Veljið **Hönnuður**.
7. Á **Líkan til kortlagningar gagnagjafa** síðu, veldu **Hönnuður** fyrir núverandi líkanakortlagningu.
8. Fylgdu þessum skrefum til að bæta við nýjum gagnagjafa til að fá aðgang að`DirPartyTable` umsóknartafla:

    1. Í **Tegund gagnagjafa** rúðu, veldu **Dynamics 365 for Operations\> Taflaskrár**.
    2. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    3. Í **Nafn** reit, slá inn **Veisluborð**.
    4. Í **Tafla** reit, slá inn **DirPartyTable**.
    5. Veldu **Allt í lagi** til að klára að bæta við nýja gagnagjafanum.

9. Fylgdu þessum skrefum til að bæta við nýjum gagnagjafa til að biðja um`DirPartyTable` skrár, byggðar á tilgreindum lista yfir auðkenniskóða skráa:

    1. Í **Tegund gagnagjafa** rúðu, veldu **Almennt \> Tómur gámur**.
    2. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    3. Í **Nafn** reit, slá inn **Gögn**.
    4. Veldu **Allt í lagi** til að klára að bæta við nýja gagnagjafanum.
    5. Í **Uppsprettur gagna** glugga, veldu **Gögn** gagnagjafa.
    6. Í **Tegund gagnagjafa** rúðu, veldu **Aðgerðir \> Reiknaður reitur**.
    7. Í **Uppsprettur gagna** rúðu, veldu **Bæta við**.
    8. Í **Nafn** reit, slá inn **DirParty**.
    9. Veljið **Breyta formúlu**.
    10. Á **Formúluhönnuður** síðu, veldu **Færibreytur**.
    11. Í **Færibreytur** valmynd, fylgdu þessum skrefum:

        1. Á **Færibreytur** flipa, veldu **Nýtt**.
        2. Í **Nafn** reit, slá inn **DirPartyId**.
        3. Í **Tegund** reit, veldu **Int64**.
        4. Veldu **Listi** gátreit.
        5. Veldu **Í lagi**.

        > [!NOTE]
        > Þú hefur bara stillt þennan reiknaða reit þannig að hann samþykki, á keyrslutíma, röksemdafærslu einnar færibreytu sem er stilltur sem færslulisti sem hefur eina`Value` sviði á *Int64* tegund.

    12. Í reitnum **Formúla** skal færa inn eftirfarandi segð:

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > Þú stilltir bara`DirParty` reiknað reit til að sækja eingöngu`DirPartyTable` skrár þar sem auðkenniskóðar skráar eru innifalin í`DirPartyId` listi sem er gefinn upp sem rök þegar`DirParty` sviði heitir.

        ![Formúla til að sækja nöfn aðila úr umsóknartöflunni á formúluhönnuðarsíðunni.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.
    14. Veldu **Vista**, og veldu síðan **Allt í lagi** til að klára að bæta við nýja gagnagjafanum.

10. Fylgdu þessum skrefum til að binda nýja gagnagjafann við nýja gagnalíkansviðið, þannig að gagnalíkanið sé notað til að afhjúpa nöfn aðila:

    1. Í **Gagnalíkan** glugga, veldu`Root.Party` reit gagnalíkans.
    2. Í rúðunni **Gagnalíkan** skal velja **Breyta**.
    3. Á **Formúluhönnuður** síðu, í **Formúla** reit, sláðu inn tjáninguna `Data.DirParty(PartyRefRecId)`.
    4. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.

        > [!NOTE]
        > Þú stilltir bara bindinguna til að kalla á stillta`Data.DirParty` gagnagjafa og gefðu upp lista yfir skráaauðkenniskóða sem verða tilgreindir á sniði þegar`Root.Party` gagnalíkansvið er kallað.

    5. Í **Gagnalíkan** glugga, veldu`Root.Party.Name` reit gagnalíkans.
    6. Í rúðunni **Gagnalíkan** skal velja **Breyta**.
    7. Á **Formúluhönnuður** síðu, í **Uppspretta gagna** rúðu, stækka **Gögn \> DirParty**, og veldu **Nafn**.
    8. Veldu **Bæta við gagnagjafa**.
    9. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.

    ![Uppbygging leiðréttrar ER líkanavörpunar á hönnuðarsíðu líkanakortlagningar.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Veldu **Vista**, og lokaðu **Módelkortahönnuður** síðu.
12. Lokið síðunni **Líkanavörpun á gagnagjafa**.
13. Á **Útgáfur** Hraðflipi, fyrir útgáfu **2.2**, veldu **Breyta stöðu \> Heill**. Veljið síðan **Í lagi**.

### <a name="adjust-the-imported-format"></a>Stilltu innflutt snið

1. Á **Stillingar** síðu, veldu **Dæmi um endurskoðunarsnið**.
2. Á **Útgáfur** Flýtiflipi, veldu útgáfu **1.2** sem hefur stöðu á **Drög**.
3. Veldu **Endurreikna grunn**.
4. Í **Markútgáfa** reit, leyfi útgáfu **2** af **Dæmi um endurskoðunarlíkan** grunn líkan.
5. Veldu **Allt í lagi** til að endurbæta og samræma sniðið við nýlegar breytingar á gagnalíkani.
6. Veljið **Hönnuður**.
7. Á **Sniðhönnuður** síðu, í sniðbyggingartrénu í vinstri glugganum, veldu **Stækka/fella saman**.
8. Fylgdu þessum skrefum til að bæta við nýrri sniðeiningu til að safna skráaauðkenniskóðum aðila þar sem færslur eru sýndar á mynduðum skýrslum.

    1. Í sniði uppbyggingu tré, veldu **Report.Row.Trans** röð þáttur.
    2. Veljið **Bæta við**.
    3. Í **Bæta við** valmynd, veldu **Uppspretta gagna \> Atriði**.
    4. Í **Eiginleikar íhluta** valmynd, í **Nafn** reit, slá inn **kt**.
    5. Í **Gagnategund** reit, veldu **Int64**.
    6. Veldu **Í lagi**.

    > [!NOTE]
    > A **Uppspretta gagna \> Atriði** eining er hægt að nota til að framkvæma innri útreikninga og gagnaumbreytingu aðeins á umfangi hlaupandi sniðs. Þess vegna, með því að bæta við þessari sniðeiningu, breytirðu ekki innihaldi myndaðs skjals.

9. Fylgdu þessum skrefum til að bæta við nýjum sniðþáttum til að slá inn nöfn aðila á útbúnar skýrslur:

    1. Veldu **Report.Row** röð þáttur.
    2. Veljið **Bæta við**.
    3. Í **Bæta við** valmynd, veldu **Texti \> Röð**.
    4. Í **Eiginleikar íhluta** valmynd, í **Nafn** reit, slá inn **Partí**.
    5. Veldu **Í lagi**.
    6. Veldu **Report.Row.Party** röð þáttur.
    7. Veljið **Bæta við**.
    8. Í **Bæta við** valmynd, veldu **Texti \> Strengur**.
    9. Í **Eiginleikar íhluta** valmynd, í **Nafn** reit, slá inn **Nafn**.
    10. Veldu **Í lagi**.

10. Fylgdu þessum skrefum til að bæta við nýjum gagnagjafa til að safna skráaauðkenniskóðum aðila sem hafa viðskipti með á mynduðum skýrslum:

    1. Á **Kortlagning** flipa, veldu **Bæta við rót**.
    2. Í **Bæta við gagnagjafa** valmynd, veldu **Aðgerðir \> Gagnasafn**.
    3. Í **Eiginleikar gagnasöfnunar 'gagnasöfnun'** valmynd, í **Nafn** reit, slá inn **PartyIds**.
    4. Í **Tegund vöru** reit, veldu **Int64**.
    5. Veldu **Í lagi**.

11. Fylgdu þessum skrefum til að bæta við nýrri bindingu til að safna skráaauðkenniskóðum aðila þar sem viðskiptin eru sýnd á mynduðum skýrslum:

    1. Í sniði uppbyggingu tré, veldu **Report.Row.Trans.Id** gagnaþáttur.
    2. Veljið **Breyta formúlu**.
    3. Á **Formúluhönnuður** síðu, sláðu inn tjáninguna `PartyIds.Collect(model.Transaction.Party.RecId)`.
    4. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.

12. Fylgdu þessum skrefum til að bæta við nýjum bindingum til að slá inn nöfn aðila á myndaðar skýrslur:

    1. Í uppbyggingartrénu skaltu velja **Report.Party** röð þáttur.
    2. Veljið **Breyta formúlu**.
    3. Á **Formúluhönnuður** síðu, sláðu inn tjáninguna `model.Party(PartyIds.Result)`.
    4. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.
    5. Í uppbyggingartrénu skaltu velja **Report.Party.Name** röð þáttur.
    6. Á **Kortlagning** flipann, veldu`model.Party.Name` reit gagnalíkans.
    7. Veldu **Binda**.

    ![Uppbygging aðlagaðs ER sniðs á síðunni Format designer.](./media/er-data-model-parameterized-calls-format2.png)

13. Veldu **Vista**, og lokaðu **Sniðhönnuður** síðu.
14. Lokið síðunni **Líkanavörpun á gagnagjafa**.
15. Á **Útgáfur** Hraðflipi, fyrir útgáfu **2.2**, veldu **Breyta stöðu** \> **Heill**. Veljið síðan **Í lagi**.

### <a name="run-the-adjusted-format"></a>Keyrðu breytta sniðið

1. Á **Stillingar** síðu, veldu **Dæmi um endurskoðunarsnið**, og veldu síðan á aðgerðarrúðunni **Hlaupa**.
2. Í **Rafræn skýrslufæribreytur** valmynd, á **Skrár til að hafa með** flipa, veldu **Sía**.
3. Tilgreindu skilyrði til að velja skattfærslur á **PIV-110000004** og **INV-10000001** fylgiskjölum.
4. Veldu **Í lagi**.
5. Veldu **Í lagi**.
6. Skoðaðu myndað skjal sem inniheldur skattfærslur á völdum fylgiskjölum og nöfn samsvarandi viðskiptavinar og lánardrottins.

    ![Forskoðun á mynduðu skjali með skattfærslum og nöfnum aðila.](./media/er-data-model-parameterized-calls-output2.png)

7. Fara til **Viðskiptaskuldir** \> **Söluaðilar** \> **Allir söluaðilar**, og skoðaðu upplýsingar um valið **PIV-110000004** skírteini, þar á meðal nafn seljanda.

    ![Farið yfir upplýsingar um innkaupaskírteini á síðunni Allir lánardrottnar og reikningsbókarsíður.](./media/er-data-model-parameterized-calls-review1.gif)

8. Fara til **Reikningur fáanlegur** \> **Viðskiptavinir** \> **Allir viðskiptavinir**, og skoðaðu upplýsingar um valið **INV-10000001** skírteini, þar á meðal nafn viðskiptavinar.

    ![Farið yfir upplýsingar um söluskírteini á síðunni Allir viðskiptavinir og Bókaður söluskattur.](./media/er-data-model-parameterized-calls-review2.gif)

Fyrir frekari upplýsingar um þessa framkvæmd ER lausnarinnar, notaðu innbyggða ER [frammistöðuspor](trace-execution-er-troubleshoot-perf.md) flokkari.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað](er-calculated-field-type.md)
- [Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md)
- [Nota gagnagjafa GAGNASÖFNUNAR í rafrænum skýrslugerðarsniðum](er-data-collection-data-sources.md)
- [ValueInLarge ER aðgerð](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
