---
title: Styðja færibreytuköll á gagnlíkön rafrænnar skýrslugerðar
description: Í þessari grein er útskýrt hvernig á að framkvæma færibreytuköll á gagnalíkön rafrænnar skýrslugerðar.
author: kfend
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
ms.openlocfilehash: 5be189c19d963991ec012de189bbf7b721b88fef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275989"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>Styðja færibreytuköll á gagnlíkön rafrænnar skýrslugerðar

[!include [banner](../includes/banner.md)]

Til að búa til viðskiptaskjöl stillir þú lausn [Rafræna skýrslugerð](general-electronic-reporting.md) sem inniheldur eftirfarandi íhluti rafrænnar skýrslugerðar:

- **[Snið](er-overview-components.md#format-component)** – Þessi eining tilgreinir skipan sniðmáts viðskiptaskjals.
- **Sniðsvörpun** – Þessi eining stýrir því hvernig viðskiptaskjal er fyllt út á keyrslutíma.
- **[Vörpun líkans](er-overview-components.md#model-mapping-component)** – Þessi eining tilgreinir hvað gögnin sækja úr forritinu inn í sniðsvörpun.
- **[Gagnalíkan](er-overview-components.md#data-model-component)** – Þessi eining flytur upplýsingar á milli hverrar einingar fyrir sig.

Þegar þú keyrir snið rafrænnar skýrslugerðar, er hver eining sniðsins keyrð og byrjað er á rótarsniðseiningunni. Þegar sniðseining sem er keyrð er bundin við [gagnagjafa](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) er gagnagjafinn keyrður til að afhenda væntanleg gögn og nota þau til að fylla út sniðseininguna. Þegar kallað er á gagnagjafa af gerðinni *Líkan*, er kallað á viðeigandi vörpun líkans til að draga gögn út úr forritinu, byggt á stillingum vörpunar líkans.

Áður var ekki hægt að breyta færibreytum slíkra kalla á vörpun líkans til að gera þau háð rökum sniðsins sem er keyrt. Aðeins gagnaflæðið í kjölfarið var stutt.

<table>
<tbody>
<tr align="center">
<td>
<b>Snið</b><br>
Sníða&nbsp;einingu<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;beiðni&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;&lt;
</td>
<td><b>Sníða&nbsp;vörpun</b><br>
Gagnaveita<br>
&nbsp;
</td>
<td>
<i>Gagna&nbsp;líkan</i><br>
&gt;&nbsp;beiðni&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;&lt;
</td>
<td>
<b>Vörpun&nbsp;líkans</b><br>
Uppruni&nbsp;gagna<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;beiðni&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;&lt;
</td>
<td>
<b>Tafla</b><br>
Færsla<br>
Svæði
</td>
</tr>
</tbody>
</table>

Í útgáfu 10.0.15 og nýrri er hins vegar hægt að stilla gagnalíkanareiti sem aðeins er hægt að kalla fram þegar gildi stilltra færibreyta eru gefin upp. Þegar slíkur reitur er stilltur og kallaður fram úr sniðseomomgi, verða nauðsynlegar færibreytur að vera veittar á bundnu sniði sem frumbreytur kallsins. Í slíkum tilfellum er hægt að tilgreina gildi frumbreytanna út frá tilteknum gildum sniða. Þess vegna er hægt að nota **Breytilegar færibreytur fyrir keyrslutíma** fyrir köll gagnalíkans fyrir eftirfarandi gagnaflæði.

<table>
<tbody>
<tr align="center">
<td>
<b>Snið</b><br>
Sníða&nbsp;einingu&nbsp;1<br>
<br>
Sníða&nbsp;einingu&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;beiðni&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;beiðni&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Sníða&nbsp;vörpun</b><br>
Uppruni&nbsp;gagna&nbsp;1<br>
&nbsp;<br>
<b>value2=Func(value1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Gagna&nbsp;líkan</i><br>
&gt;&nbsp;field1&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;1&nbsp;&lt;<br>
<b>&gt;&nbsp;field2(value2)&nbsp;&gt;</b><br>
&lt;&nbsp;gildi&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Vörpun&nbsp;líkans</b><br>
Uppruni&nbsp;gagna&nbsp;1<br>
<br>
Uppruni&nbsp;gagna&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;beiðni&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;beiðni&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;gildi&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Tafla&nbsp;1</b><br>
Færsla&nbsp;1<br>
Reitur&nbsp;1<br>
<b>Tafla&nbsp;2</b><br>
Færsla&nbsp;2<br>
Reitur&nbsp;2
</td>
</tr>
</tbody>
</table>

Nýi eiginleikinn gerir þér kleift að breyta færibreytum kallsins í hvaða reit gagnalíkans sem er af gerðinni [*Færsla*](er-formula-supported-data-types-composite.md#record) eða [*Færslulisti*](er-formula-supported-data-types-composite.md#record-list). Eftirfarandi gagnagerðir eru studdar fyrir færibreytur reits gagnalíkans:

- [Boole-gildi](er-formula-supported-data-types-primitive.md#boolean)
- [Gámur](er-formula-supported-data-types-composite.md#container)
- [Dagsetning](er-formula-supported-data-types-primitive.md#date)
- [DateTime-gildi](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Heiltala](er-formula-supported-data-types-primitive.md#integer)
- [Rauntala](er-formula-supported-data-types-primitive.md#real)
- [Strengur](er-formula-supported-data-types-primitive.md#string)

Hægt er að tilgreina allar breytur í gagnalíkansreit þar sem hægt er að láta færibreytu í té sem stakt gildi skilgreindrar gagnagerðar og [*lista*](er-formula-supported-data-types-composite.md#record-list) yfir slík gildi.

> [!NOTE]
> Sjálfgefið gildi fyrir færibreytu gagnalíkansreits er ekki stutt. Ef þú bætir færibreytu við reit í gagnalíkani, og útgáfa þess gagnalíkans hefur þegar verið gefin út og birt, verður þú að [endurreikna](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) allar samsvarandi varpanir líkana og sniða í nýju útgáfuna af þessu líkani, vegna þess að þessi breyting á gagnalíkani er ekki samhæf aftur á bak.

Hægt er að skilgreina færibreytur gagnalíkansreita til að sérstilla snið kalla líkanavörpunar. Þessi aðferð getur hjálpað þér að draga úr fjölda varpana líkana sem verður að sérstilla fyrir mörg snið af stöku gagnalíkani. Þú getur einnig notað þessa aðferð til að bæta afköst framkvæmdar á sniðunum þínum og minnka tímann sem fer í að búa til viðskiptaskjöl. Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka dæminu í þessari grein.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Dæmi: Nota færibreytuköll á gagnlíkön rafrænnar skýrslugerðar

Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra eða forritara rafrænnar skýrslugerðar getur hannað lausn rafrænnar skýrslugerðar sem inniheldur gagnalíkan, vörpun líkans og sniðseiningu rafrænnar skýrslugerðar sem er stillt til að kalla á vörpun líkans úr sniði með því að leggja fram færibreytur fyrir kallinu, en gildi þess hefur verið reiknað á keyrslutíma með því að nota formúlu sniðsins sem er í keyrslu. 

Hægt er að ljúka skrefunum í **DEMF** fyrirtækinu. Ekki þarf að gera neinar breytingar á kóða. 

Í þessu dæmi muntu stofna nauðsynlegar ER-[skilgreiningar](general-electronic-reporting.md#Configuration) fyrir sýnifyrirtækið, **Litware, Inc.**. Tryggið að skilgreiningarveita fyrir sýndarfyrirtækið **Litware, Inc.** (`http://www.litware.com`) sé skráð fyrir ramma rafrænnar skýrslugerðar og merkt sem **Virk**. Ef skilgreiningarveita er ekki skráð, eða ef hún er ekki merkt sem **Virk**, skal fylgja skrefunum í greininni [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="business-scenario"></a>Sviðsmynd fyrirtækis

Þú ert með lausn fyrir rafræna skýrslugerð sem inniheldur snið sem þú getur keyrt til að búa til rafrænt skjal til endurskoðunar. Þetta snið inniheldur skattfærslur sem tengjast sölupöntunum og innkaupapöntunum og innihalda áskildar upplýsingar eins og færsludag og virði skatts. Frá og með nýju fjárhagsári hefur skipan þessa skjals breyst. Nú verður þú að senda inn lengra skjal sem inniheldur viðbótarupplýsingar (nöfn) allra aðila (viðskiptavini og lánardrottna) þar sem viðskiptin koma fram á mynduðum skýrslum. Því verður að breyta lausninni fyrir rafræna skýrslugerð þannig að hún búi til skjöl sem uppfylla þessa nýju kröfu.

### <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ramma rafrænnar skýrslugerðar til að hanna nýja lausn rafrænnar skýrslugerðar.

### <a name="design-a-domain-specific-data-model"></a>Hanna gagnalíkan fyrir sérstakt lén

Stofna þarf nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur áskilda einingu gagnalíkans. Þetta gagnalíkan verður seinna notað sem gagnagjafi þegar hannað er snið rafrænnar skýrslugerðar til að búa til skýrslu endurskoðunar.

Fylgdu eftirfarandi skrefum til að flytja inn nauðsynlegt gagnalíkan úr XML-skrá sem Microsoft lætur í té.

1. Sæktu skrána [Sample audit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) og vistaðu hana á staðbundinni tölvu.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, skal velja **Skipta út**\>**Hlaða úr XML-skrá**.
5. Veljið **Fletta** og finnið síðan og veljið skrána **Sample audit model.version.1.xml**.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

    ![Innflutt skilgreining gagnalíkans rafrænnar skýrslugerðar á skilgreiningasíðunni.](./media/er-data-model-parameterized-calls-imported-model.png)

Eftirfarandi mynd sýnir stillt gagnalíkan sem er hægt að breyta á síðunni **Hönnuður gagnalíkans**.

![Uppbygging gagnalíkans rafrænnar skýrslugerðar á síðu hönnuðar gagnalíkansins.](./media/er-data-model-parameterized-calls-model1.png)

Í dag er líkanið hannað til að sýna einungis skattfærslur sem hafa tilskildar upplýsingar.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Hanna líkanavörpun fyrir skilgreint gagnalíkan

Sem notandi í hönnunarhlutverki rafrænnar skýrslugerðar þarf að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur íhlut líkanavörpunar fyrir sýnishorn af gagnalíkanið Endurskoðun. Þessi eining framkvæmir stillta gagnalíkanið sem stillt er fyrir Microsoft Dynamics 365 Finance og er einungis notað í því forriti. Skilgreina verður íhlut líkanavörpunar til að tilgreina hugbúnaðarhluti sem þarf að nota til að fylla út skilgreint gagnalíkan með forritsgögnum við keyrslu. Til að ljúka þessu verki verður þú að skilja hvernig gagnauppbygging fyrirtækjaléns fyrir skatta er útfærð í Finance.

Fylgdu þessum skrefum til að flytja inn nauðsynlega vörpun líkans úr XML-skrá sem Microsoft lætur í té.

1. Sæktu skrána [Sample audit model.version.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) og vistaðu hana á staðbundinni tölvu.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, skal velja **Skipta út**\>**Hlaða úr XML-skrá**.
5. Veljið **Fletta** og leitaðu að og veldu skrána **Sample audit model mapping.version.1.1.xml**.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

    ![Innflutt skilgreining vörpunar líkans rafrænnar skýrslugerðar á skilgreiningasíðunni.](./media/er-data-model-parameterized-calls-imported-mapping.png)

Eftirfarandi mynd sýnir útgáfu af stilltu líkanavörpuninni sem er hægt að breyta á síðunni **Hönnuður gagnalíkans**.

![Skipan vörpunar líkans rafrænnar skýrslugerð á síðunni Hönnuður líkanavörpunar.](./media/er-data-model-parameterized-calls-mapping1.png)

Í dag er vörpun líkans hannað til að sýna skattfærslur sem hafa tilskildar upplýsingar. Það sækir upplýsingarnar úr jöfnunartöflunni `TaxTrans` með því að nota stilltu `TaxTrans` og `TaxTransFiltered` gagnagjafa rafrænnar skýrslugerðar.

### <a name="design-a-new-format"></a>Hanna nýtt snið

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar þarf að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur sniðs hluta. Þú verður að stilla sniðseininguna til að fylla út myndaðar skýrslur með skattfærslum með öllum áskildum upplýsingum.

Fylgdu þessum skrefum til að flytja inn áskilið snið úr XML skrá sem Microsoft lætur í té.

1. Sækið skrána [Sample audit format.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) og vistið hana á staðbundinni tölvu.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, skal velja **Skipta út**\>**Hlaða úr XML-skrá**.
5. Veljið **Fletta** og finnið síðan og veljið skrána **Sample audit format.version.1.1.xml**.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

    ![Innflutt skilgreining sniðs rafrænnar skýrslugerðar á skilgreiningasíðunni.](./media/er-data-model-parameterized-calls-imported-format.png)

Eftirfarandi mynd sýnir útgáfu af stilltu sniði sem er hægt að breyta á síðunni **Hönnuður gagnalíkans**.

![Skipan rafræns skýrslugerðarsniðs á sniðshönnunarsíðunni.](./media/er-data-model-parameterized-calls-format1.png)

Snið rafrænnar skýrslugerðar er stillt til að mynda skýrslu sem textaskrá á (CSV)-sniði með gildi aðskilin með kommu.

### <a name="run-the-imported-format"></a>Keyrðu innflutta sniðið

1. Á síðunni **Stillingar** skal velja **Sýnishorn af snið endurskoðunar** stillinguna og á Aðgerðasvæði skal velja **Keyra**.
2. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar** á flipanum **Færslur til að taka með** skal velja **Sía**.
3. Tilgreindu skilyrði til að velja skattfærslur fylgiskjals **PIV-110000004** og **INV-10000001**.
4. Veldu **Í lagi**.
5. Veldu **Í lagi**.
6. Farðu yfir skjalið sem er búið til og inniheldur skattfærslur valinna fylgiskjala.

    ![Forskoðun á myndaða skjalinu með skattfærslum.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>Breyta lausn innfluttu rafræn skýrslugerð

Samkvæmt nýju kröfunni verður skjalið sem þú verður senda inn að innihalda nöfn viðskiptavina og lánardrottna sem eiga færslurnar sem eru innfaldar. Því verður að breyta innfluttu lausninni fyrir rafræna skýrslugerð þannig að hún búi til skjal sem uppfyllir þessa nýju kröfu.

Ákveddu hvernig þú vilt framkvæma nauðsynlegar breytingar á innfluttum einingum rafrænnar skýrslugerðar.

Auðveldasta aðferðin er að framkvæma eftirfarandi breytingar:

- Í gagnalíkani þínu skaltu bæta við nýja reit `Transaction.Party.Name` gagnalíkans af gerðinni *Strengur*.
- Í vörpun líkans þíns skaltu stilla bindinguna fyrir nýja reitinn fyrir gagnalíkan með því að nota tiltæk töflutengsl til að sjá viðeigandi færslu á `DirPartyTable` jöfnunartöflunni og sækja gildið í `Name` reitnum úr henni.

Þó að þessi aðferð muni virka gæti hún valdið vandamálum varðandi frammistöðu í SQL-gagnagrunninum, vegna þess að `TaxTrans` er færslutaflan og getur því innihaldið mikið magn af færslum. Í þessu tilviki verður fjöldi kalla í `DirPartyTable` að vera jafn fjölda færslna í `TaxTrans` töflunni, en slíkt getur valdið vandamálum í tengslum við afköst.

Þú getur einnig gert eftirfarandi breytingar:

- Í gagnalíkaninu þínu skaltu bæta við nýju `Party` rótinni og nýja `Party.Name` reitnum.
- Í vörpun líkansins skaltu bæta við nýjum gagnagjafa sem tengja allar færslur taflna sem eru notaðar í töflutengingum til að fá aðgang að viðeigandi færslu á `DirPartyTable` jöfnunartöfluna, frá og með `TaxTrans` töflunni.

Þessi aðferð mun virka en gæti valdið vandamálum varðandi minnisnotkun. Jafnvel þegar nýr [JOIN](er-join-data-sources.md)-gagnagjafi er keyrður sem stök SQL-beiðni í gagnagrunn forritsins til að koma í veg fyrir vandamál með afköst gagnagrunnsins, verður að sækja niðurstöðuna í minni forritaþjónsins. Þar sem fjöldi færslna og fjöldi reita í þeim færslum verður nokkuð mikill gæti þessi aðferð notað mjög mikið af minni. Einnig gæti komið fram undantekning keyrslutíma vegna þess að minni er á þrotum.

Þú getur framkvæmt breytingarnar þegar keyrsla á sniði safnar saman í minni, einkvæmum auðkenniskóðum viðskiptavina og lánardrottna fyrir allar skattfærslur sem koma fram á myndaðri skýrslu. Vegna þess að aðeins ætti að geyma einkvæma kóða verður endanlegt kóðasett ekki nógu stórt til að hafa áhrif á minnisnotkun. Kóðasettið verður síðan sent til vörpunar líkansins sem færibreyta fyrir öðru kalli gagnagjafans af gerðinni *Líkan*. Á grundvelli kallsins mun vörpun líkansins keyra nýjan gagnagjafa rafrænnar skýrslugerðar eina SQL-beiðni til forritagagnagrunnsins til að sækja úr `DirPartyTable` töflunni, færslur aðeins fyrir þá aðila þar sem kóðarnir eru settir fram í meðfylgjandi kóðasetti.

### <a name="adjust-the-imported-data-model"></a>Breyta innfluttu gagnalíkani

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu í glugganum til vinstri skal velja **Sýnishorn af greiðslulíkani**.
3. Á flýtiflipanum **Útgáfur** skal velja útgáfu **2** með stöðuna **Drög**.
4. Veldu flýtiflipann **Stillingarhlutar**.
5. Veldu **Hönnuður** til að opna gagnalíkanið fyrir breytingar.
6. Á síðunni **Gagnamódel** skaltu ganga úr skugga um að `Root` reiturinn sé valinn og velja síðan **Nýtt**.
7. Í fellilistanum skaltu fylgja þessum skrefum:

    1. Í reitahópnum **Nýr hnútur sem** skaltu velja **Undireining virks hnútar** valkostinn.
    2. Í reitinn **Heiti** skal færa inn **Party**.
    3. Í reitnum **Gerð vöru** velurðu **Skráalisti**.
    4. Veldu **Bæta við** til að bæta við nýja reitnum.

8. Gakktu úr skugga um að `Root.Party` reiturinn sé valinn og síðan, á flipanum **Hnútur**, skal velja **Færibreytur**.
9. Í svarglugganum **Færibreytur** skal fylgja þessum skrefum:

    1. Á flipanum **Færibreytur** velurðu **Nýtt**.
    2. Í reitinn **Heiti** skal færa inn **PartyRefRecId**.
    3. Í reitnum **Tegund** skal velja **Int64**.
    4. Hakaðu í gátreitinn **Listi**.
    5. Veldu **Í lagi** til að klára að slá inn færibreyturnar.

    > [!NOTE]
    > Þú varst að stilla reitinn fyrir `Root.Party` gagnalíkan sem reit sem er kallað á þegar gildi er gefið upp í **PartyRefRecId** færibreytunni. Þetta gildi verður að vera til staðar í færslulistanum sem innihalda `Value` reit af gagnagerðinni *Int64*.

    ![Svargluggi færibreytur.](./media/er-data-model-parameterized-calls-model2a.png)

10. Gakktu úr skugga um að `Root.Party` reiturinn sé enn valinn og veldu síðan **Nýtt**.
11. Í fellilistanum skaltu fylgja þessum skrefum:

    1. Í reitahópnum **Nýr hnútur sem** skaltu velja **Undireining virks hnútar** valkostinn.
    2. Í reitinn **Heiti** skal færa inn **Name**.
    3. Í reitnum **Gerð vöru** velurðu **Strengur**.
    4. Veldu **Bæta við** til að bæta við nýja reitnum.

12. Veldu **Vista** og lokaðu síðunni **Gagnalíkan**.

    ![Uppbygging breytta gagnalíkans rafrænnar skýrslugerðar á síðu hönnuðar gagnalíkansins.](./media/er-data-model-parameterized-calls-model2b.png)

13. Á flýtiflipanum **Útgáfur** fyrir útgáfu **2**, velurðu **Breyta stöðu** \> **Lokið**. Veljið síðan **Í lagi**.

    > [!NOTE]
    > Breytingar á gagnalíkani eru geymdar í annarri endurskoðun á **Sýnishorn af greiðslulíkani** gagnalíkanseiningu sem er staðsett í seinni útgáfu stillingar rafrænnar skýrslugerðar fyrir **Sýnishorn af greiðslulíkani**.

![Uppfærð skilgreining gagnalíkans rafrænnar skýrslugerðar á skilgreiningasíðunni.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>Breyta innflutta líkanavörpun

1. Á síðunni **Skilgreiningar**, í skilgreiningatrénu í glugganum til vinstri skal stækka **Sýnishorn af greiðslulíkani**.
2. Veldu **Sýnishorn af vörpun greiðslulíkans** og síðan á flýtiflipanum **Útgáfur** velja aðra útgáfu vörpunar sem byggist á fyrsta gagnalíkaninu (útgáfu **1.2**) og hefur stöðunaf **Drög**.
3. Veldu **Endurreikna grunn**.
4. Í reitnum **Markútgáfa** skaltu loka útgáfu **2** í grunnlíkani **Sýnishorn af greiðslulíkani**.
5. Veldu **Í lagi** til að endurraða og samræma kortlagningu líkansins við nýlegar breytingar á líkönum.

    Takið eftir að útgáfunúmer breytanlegu vörpun líkans hefur breyst úr **1.2** í **2.2** til að sýna að önnur útgáfa líkansins er notuð sem grunnur.

6. Veljið **Hönnuður**.
7. Á síðunni **Líkanavörpun gagnagjafa** velurðu **Hönnuður** fyrir núverandi líkanavörpun.
8. Fylgið eftirfarandi skrefum til að bæta við nýjum gagnagjafa til að fá aðgang `DirPartyTable` að jöfnunartöflunni:

    1. Í rúðunni **Gerð gagnagjafa** skal velja **Dynamics 365 for Operations\>Töflufærslur**.
    2. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    3. Í reitinn **Heiti** skal færa inn **PartyTable**.
    4. Í reitinn **Tafla** skal slá inn **DirPartyTable**.
    5. Veljið **Í lagi** til að ljúka við að bæta við nýja gagnagjafanum.

9. Fylgdu eftirfarandi skrefum til að bæta nýjum gagnagjafa við beiðnir um `DirPartyTable` færslur, byggt á meðfylgjandi lista yfir auðkenniskóða færslna:

    1. Í glugganum **Gerðir gagnagjafa**, skal velja **Almennt \> Tómur geymir**.
    2. Í rúðunni **Gagnagjafar** skal velja **Bæta við rót**.
    3. Í reitinn **Heiti** skal færa inn **Data**.
    4. Veljið **Í lagi** til að ljúka við að bæta við nýja gagnagjafanum.
    5. Í glugganum **Gagnagjafar** skal velja gagnagjafann **Gögn**.
    6. Í rúðunni **Gerð gagnagjafa** skal velja **Aðgerðir\>Reiknaður reitur**.
    7. Í rúðunni **Gagnagjafar** skal velja **Bæta við**.
    8. Í reitinn **Heiti** skal færa inn **DirParty**.
    9. Veljið **Breyta formúlu**.
    10. Á síðunni **Formúluhönnuður** skaltu velja **Færibreytur**.
    11. Í svarglugganum **Færibreytur** skal fylgja þessum skrefum:

        1. Á flipanum **Færibreytur** velurðu **Nýtt**.
        2. Í reitinn **Heiti** skal færa inn **DirPartyId**.
        3. Í reitnum **Tegund** skal velja **Int64**.
        4. Hakaðu í gátreitinn **Listi**.
        5. Veldu **Í lagi**.

        > [!NOTE]
        > Þú varst að stilla þennan reiknaða reit þannig að hann taki við, á keyrslutímanum, við frumbreytu stakrar færibreytu sem er stillt sem færslulisti sem hefur einn `Value` reit af *Int64* gerð.

    12. Í reitnum **Formúla** skal færa inn eftirfarandi segð:

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > Þú varst að stilla `DirParty` útreiknaða reitinn til að sækja aðeins `DirPartyTable` færslur þar sem auðkenniskóðar færslu eru á `DirPartyId` listanum sem er gefinn upp sem færibreyta þegar kallað er á reitinn `DirParty`.

        ![Formúla til að sækja heiti aðila úr jöfnunartöflunni á síðu Formúluhönnuðar.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.
    14. Veldu **Vista** og veldu síðan **Í lagi** til að ljúka við að bæta við nýja gagnagjafanum.

10. Fylgið þessum skrefum til að binda nýja gagnagjafann við nýja reit gagnalíkansins, þannig að gagnalíkanið sé notað til að birta nöfn aðila:

    1. Í glugganum **Gagnalíkan** skal velja `Root.Party` gagnalíkansreitinn.
    2. Í rúðunni **Gagnalíkan** skal velja **Breyta**.
    3. Á síðunni **Formúluhönnuður**, í reitinn **Formúla**, skal slá inn segðina `Data.DirParty(PartyRefRecId)`.
    4. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.

        > [!NOTE]
        > Þú varst að stilla bindingu við kall á stillta `Data.DirParty` gagnagjafann og láta í té lista yfir auðkenniskóða færslu sem verða tilgreindir í sniðinu þegar kallað er á reitinn `Root.Party` fyrir gagnalíkan.

    5. Í glugganum **Gagnalíkan** skal velja `Root.Party.Name` gagnalíkansreitinn.
    6. Í rúðunni **Gagnalíkan** skal velja **Breyta**.
    7. Á síðunni **Formúluhönnuður**, í glugganum **Gagnagjafi**, stækkið **Gögn \> DirParty** og veljið **Nafn**.
    8. Veldu **Bæta við gagnagjafa**.
    9. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.

    ![Uppbygging aðlagaðrar vörpunar á líkani rafrænnar skýrslugerðar á síðunni Hönnuður líkanavörpunar.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Veljið **Vista** og lokið síðunni **Hönnuður líkanavörpunar**.
12. Lokið síðunni **Líkanavörpun á gagnagjafa**.
13. Á flýtiflipanum **Útgáfur** fyrir útgáfu **2.2**, velurðu **Breyta stöðu \> Lokið**. Veljið síðan **Í lagi**.

### <a name="adjust-the-imported-format"></a>Breyta innflutt snið

1. Á síðunni **Skilgreiningar** skal velja **Sýnishorn af snið endurskoðunar**.
2. Á flýtiflipanum **Útgáfur** skal velja útgáfu **1.2** með stöðuna **Drög**.
3. Veldu **Endurreikna grunn**.
4. Í reitnum **Markútgáfa** skaltu loka útgáfu **2** í grunnlíkani **Sýnishorn af greiðslulíkani**.
5. Veldu **Í lagi** til að breyta og samræma snið þitt við nýlegar breytingar á gagnalíkani.
6. Veljið **Hönnuður**.
7. Á síðunni **Sniðshönnuður**, í trjásniðinu vinstra megin, skal velja **Stækka/fella saman**.
8. Fylgdu þessum skrefum til að bæta við nýrri sniðseiningu til að safna og skrá auðkenniskóða aðila þar sem færslur koma fram í skýrslum sem eru búnar til.

    1. Í trjáskipan sniðs skal velja röðunareininguna **Report.Row.Trans**.
    2. Veljið **Bæta við**.
    3. Í svarglugganum **Bæta við** skal velja **Gagnagjafi \> Atriði**.
    4. Í svarglugganum **Eiginleiki hlutar**, í reitinn **Heiti**, skal færa inn **Id**.
    5. Í reitnum **Gagnagerð** skal velja **Int64**.
    6. Veldu **Í lagi**.

    > [!NOTE]
    > Hægt er að nota einingu **Gagnagjafa \> Atriði** til að framkvæma innri útreikninga og umbreytingu gagna einungis í umfangi sniðsins sem er í keyrslu. Með því að bæta þessari sniðseiningu við breytir þú því ekki efni skjalsins sem búið er til.

9. Fylgdu þessum skrefum til að bæta við nýjum sniðseiningum til að slá inn heiti aðila á mynduðum skýrslum:

    1. Veldu röðunareininguna **Report.Row**.
    2. Veljið **Bæta við**.
    3. Í svarglugganum **Bæta við** skal velja **Texti \> Röð**.
    4. Í svarglugganum **Eiginleiki einingar**, í reitinn **aðili**, skal færa inn **Aðili**.
    5. Veldu **Í lagi**.
    6. Veldu röðunareininguna **Report.Row.Party**.
    7. Veljið **Bæta við**.
    8. Í svarglugganum **Bæta við** skal velja **Texti \> Strengur**.
    9. Í svarglugganum **Eiginleiki einingar**, í reitinn **Heiti**, skal færa inn **Heiti**.
    10. Veldu **Í lagi**.

10. Fylgdu þessum skrefum til að bæta við nýjum gagnagjafa til að safna og skrá auðkenniskóða aðila þar sem færslur koma fram í skýrslum sem eru búnar til:

    1. Á flipanum **Vörpun** velurðu **Bæta við rót**.
    2. Í svarglugganum **Bæta við gagnagjafa** skal velja **Aðgerðir \> Gagnasafn**.
    3. Í svargluggann **Eiginleikar gagnagjafa fyrir „Gagnasöfnun“**, í reitinn **Heiti**, skal færa inn **PartyIds**.
    4. Í reitnum **Tegund atriðis** skal velja **Int64**.
    5. Veldu **Í lagi**.

11. Fylgdu þessum skrefum til að bæta við nýrri bindingu til að safna og skrá auðkenniskóða aðila þar sem færslur koma fram í skýrslum sem eru búnar til:

    1. Í trjáskipan sniðs skal velja röðunareininguna **Report.Row.Trans.Id**.
    2. Veljið **Breyta formúlu**.
    3. Sláðu inn segðina á síðunni **Formúluhönnuður** `PartyIds.Collect(model.Transaction.Party.RecId)`.
    4. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.

12. Fylgið eftirfarandi skrefum til að bæta við nýjum bindingum til að slá inn heiti aðila á mynduðum skýrslum:

    1. Í trjáskipan sniðs skal velja röðunareininguna **Report.Party**.
    2. Veljið **Breyta formúlu**.
    3. Sláðu inn segðina á síðunni **Formúluhönnuður** `model.Party(PartyIds.Result)`.
    4. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.
    5. Í trjáskipan sniðs skal velja röðunareininguna **Report.Party.Name**.
    6. Á flipanum **Vörpun** velurðu `model.Party.Name` reiturinn fyrir gagnalíkan.
    7. Veldu **Binda**.

    ![Uppbygging aðlagaðs snið rafrænnar skýrslugerðar á síðu Sniðshönnuðar.](./media/er-data-model-parameterized-calls-format2.png)

13. Veldu **Vista** og lokaðu síðunni **Sniðshönnuður**.
14. Lokið síðunni **Líkanavörpun á gagnagjafa**.
15. Á flýtiflipanum **Útgáfur** fyrir útgáfu **2.2**, velurðu **Breyta stöðu** \> **Lokið**. Veljið síðan **Í lagi**.

### <a name="run-the-adjusted-format"></a>Keyra breytt snið

1. Á síðunni **Stillingar** skal velja **Sýnishorn af snið endurskoðunar** og á Aðgerðasvæði skal velja **Keyra**.
2. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar** á flipanum **Færslur til að taka með** skal velja **Sía**.
3. Tilgreindu skilyrði til að velja skattfærslur fylgiskjals **PIV-110000004** og **INV-10000001**.
4. Veldu **Í lagi**.
5. Veldu **Í lagi**.
6. Farðu yfir skjalið sem er búið til og inniheldur skattfærslur valinna fylgiskjala og heiti samsvarandi viðskiptavinar og lánardrottins.

    ![Forskoðun á mynduðu skjali með skattfærslum og nöfnum aðila.](./media/er-data-model-parameterized-calls-output2.png)

7. Opnaðu **Viðskiptaskuldir** \> **Lánardrottnar** \> **Allir lánardrottnar** og skoðaðu upplýsingar um valda **PIV-110000004** fylgiskjalið, þar á meðal nafn lánardrottins.

    ![Yfirfara upplýsingar um fylgiskjal innkaupa á síðunum Allir lánardrottnar og Reikningabók.](./media/er-data-model-parameterized-calls-review1.gif)

8. Opnaðu **Viðskiptakröfur** \> **Viðskiptavinir** \> **Allir viðskiptavinir**, og fara yfir upplýsingar um valið fylgiskjal **INV-10000001**, þar á meðal nafn viðskiptavinar.

    ![Yfirfara upplýsingar um fylgiskjal sölu á síðunum Allir viðskiptavinir og Bókaður söluskattur.](./media/er-data-model-parameterized-calls-review2.gif)

Til að fá frekari upplýsingar um þessa framkvæmd lausnar rafrænnar skýrslugerðar skaltu nota [afkastarakningu](trace-execution-er-troubleshoot-perf.md) innbyggða þáttarans í rafrænni skýrslugerð.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað](er-calculated-field-type.md)
- [Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md)
- [Nota gagnagjafa GAGNASÖFNUNAR í rafrænum skýrslugerðarsniðum](er-data-collection-data-sources.md)
- [ValueInLarge ER aðgerð](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
