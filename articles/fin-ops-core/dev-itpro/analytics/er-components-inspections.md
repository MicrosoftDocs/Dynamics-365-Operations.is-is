---
title: Skoða grunnstilltan hlut rafrænnar skýrslugerðar til að koma í veg fyrir vandamál varðandi keyrslu
description: Þetta efnisatriði útskýrir hvernig á að skoða grunnstillta íhluti rafrænnar skýrslugerðar til að koma í veg fyrir vandamál varðandi keyrsluna sem gætu komið upp.
author: NickSelin
manager: AnnBe
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72db7660c07b2f57f8609ab6c14964193e842d75
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688568"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Skoða grunnstilltan hlut rafrænnar skýrslugerðar til að koma í veg fyrir vandamál varðandi keyrslu

[!include[banner](../includes/banner.md)]

Sérhvert grunnstillt [rafrænt skýrslugerðar](general-electronic-reporting.md) [snið](general-electronic-reporting.md#FormatComponentOutbound) og hlutur [líkanavörpunar](general-electronic-reporting.md#data-model-and-model-mapping-components) er hægt að [villuleita](er-fillable-excel.md#validate-an-er-format) á tíma hönnunar. Í þessari villuleit er samræmisathugun gerð til að koma í veg fyrir vandamál varðandi keyrsluna sem getur komið upp, t.d. villur við framkvæmd og afkastaminnkun. Fyrir hvert vandamál sem finnst er slóð einingarinnar sem tengist vandanum gefin upp. Í sumum vandamálum er sjálfvirk lagfæring tiltæk.

Sjálfgefið er að villuleit er sjálfkrafa notuð í eftirfarandi tilfellum fyrir grunnstillingu rafrænnar skýrslugerðar sem inniheldur fyrrnefnda hluti rafrænnar skýrslugerðar:

- Þú [flytur inn](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) nýja [útgáfu](general-electronic-reporting.md#component-versioning) af skilgreiningu rafrænnar skýrslugerðar í tilvikið þitt af Microsoft Dynamics 365 Finance.
- Þú breytir [stöðunni](general-electronic-reporting.md#component-versioning) á breytanlegri skilgreiningu rafrænnar skýrslugerðar úr **Drög** í **Lokið**.
- Þú [endurreiknar grunn](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) breytanlegrar skilgreiningar rafrænnar skýrslugerðar með því að nota nýja grunnútgáfu.

Hægt er að keyra þessa sannvottun beint. Veljið einn af eftirfarandi valkostum og fylgið skrefunum sem eru gefin upp:

- Valkostur 1:

    1. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
    2. Í skilgreiningatrénu í svæðinu vinstra megin er æskileg skilgreining rafrænnar skýrslugerðar valin sem inniheldur rafrænt skýrslugerðarsnið eða hlut líkanavörpunar rafrænnar skýrslugerðar.
    3. Í flýtiflipanum **Útgáfur** skal velja æskilega útgáfu af valdri skilgreiningu rafrænnar skýrslugerðar.
    4. Veldu **Villuleita** á aðgerðasvæðinu.

- Valkostur 2, fyrir snið rafrænnar skýrslugerðar:

    1. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
    2. Í skilgreiningatrénu í svæðinu vinstra megin er æskileg skilgreining rafrænnar skýrslugerðar valin sem inniheldur hlut rafræns skýrslugerðarsniðs.
    3. Í flýtiflipanum **Útgáfur** skal velja æskilega útgáfu af valdri skilgreiningu rafrænnar skýrslugerðar.
    4. Í aðgerðarúðunni skal velja **Hönnuður**.
    5. Á síðunni **Sniðshönnuður**, í aðgerðarúðunni, skal velja **Villuleita**.

- Valkostur 3, fyrir vörpun líkans fyrir rafræna skýrslugerð:

    1. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
    2. Í skilgreiningatrénu í svæðinu vinstra megin er æskileg skilgreining rafrænnar skýrslugerðar valin sem inniheldur hlut líkanavörpunar rafrænnar skýrslugerðar.
    3. Í flýtiflipanum **Útgáfur** skal velja æskilega útgáfu af valdri skilgreiningu rafrænnar skýrslugerðar.
    4. Í aðgerðarúðunni skal velja **Hönnuður**.
    5. Á síðunni **Líkanavörpun á gagnagjafa**, á aðgerðasvæðinu, skal velja **Hönnuður**.
    6. Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Villuleita**.

Til að sleppa villuleit þegar skilgreining er flutt inn skal fylgja þessum skrefum.

1. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Stillið **Sannprófa skilgreininguna eftir innflutning** valkostinn á **Nei**.

Til að sleppa villuleit þegar stöðu útgáfunnar er breytt eða endurreiknuð skal fylgja þessum skrefum.

1. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Stillið valkostinn **Sleppa prófun við breytingar á stöðu og endurreikning grunns skilgreiningar** á **Já**.

Rafræn skýrslugerð notar eftirfarandi flokka til að flokka saman eftirlit samræmisathugunar:

- **Keyranleiki** - Eftirlit sem finnur alvarleg vandamál sem gætu komið upp við keyrslu. Þessi vandamál koma helst upp á stiginu **Villa**. 
- **Afköst** - Eftirlit sem greinir vandamál sem gætu valdið óskilvirkri framkvæmd á skilgreindum hlutum rafrænnar skýrslugerðar. Þessi vandamál eru að mestu á stigi **Viðvörunar**.
- **Heillleiki gagna** - Eftirlit sem greinir vandamál sem gætu valdið gagnatapi eða vandamálum við keyrslu. Þessi vandamál eru að mestu á stigi **Viðvörunar**.

## <a name="list-of-inspections"></a>Listi yfir eftirlit

Eftirfarandi tafla veitir yfirlit yfir eftirlit sem rafræn skýrslugerð býður upp á. Frekari upplýsingar um þessi eftirlit skal nota tenglana í fyrsta dálknum til að fara í viðeigandi kafla í þessu efnisatriði. Þessir kaflar útskýra gerðir hluta sem rafræn skýrslugerð veitir eftirlit fyrir og hvernig hægt er að endurskilgreina hluti rafrænnar skýrslugerðar til að koma í veg fyrir vandamál.

<table>
<thead>
<tr>
<th>Nafn</th>
<th>Tegund</th>
<th>Stig</th>
<th>Skilaboð</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Umbreyting á gerð</a></td>
<td>Keyranleiki</td>
<td>Villa</td>
<td>
<p>Ekki er hægt að breyta segð af gerðinni &lt;gerð&gt; í reit af gerðinni &lt;gerð&gt;.</p>
<p><b>Keyrsluvilla:</b> Undantekning af gerð</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Samhæfisgerð</a></td>
<td>Keyranleiki</td>
<td>Villa</td>
<td>
<p>Ekki er hægt að nota grunnstillta segð sem bindingu á núverandi sniðseiningu við gagnagjafa þar sem þessi segð skilar gildi af gagnagerð &lt;gerð&gt; sem er utan umfangs gagnagerða sem eru studdar af núverandi sniðseiningu af gerðinni &lt;gerð&gt;.</p>
<p><b>Keyrsluvilla:</b> Undantekning af gerð</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Skilgreiningareiningu vantar</a></td>
<td>Keyranleiki</td>
<td>Villa</td>
<td>
<p>Slóð finnst ekki &gt;slóð&lt;</p>
<p><b>Keyrsluvilla</b> Eining skilgreiningarinnar &gt;slóð&lt; finnst ekki</p>
</td>
</tr>
<tr>
<td><a href='#i4'>Keyranleiki segðar með FILTER-aðgerð</a></td>
<td>Keyranleiki</td>
<td>Villa</td>
<td>
<p>Listasegðin í aðgerðinni SÍA er ekki fyrirspurnarhæf.</p>
<p><b>Keyrsluvilla:</b> Síun er ekki studd. Staðfestið skilgreininguna til að fá frekari upplýsingar um þetta.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>Keyranleiki um GROUPBY-gagnagjafa</a></td>
<td>Keyranleiki</td>
<td>Villa</td>
<td>Slóðin &lt;slóð&gt; styður ekki fyrirspurnir.</td>
</tr>
<tr>
<td>Keyranleiki</td>
<td>Villa</td>
<td>
<p>Ekki er hægt að keyra flokka eftir aðgerðina með fyrirspurn.</p>
<p><b>Keyrsluvilla:</b> Flokka eftir aðgerðina er ekki hægt að framkvæma með fyrirspurn.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>Keyranleiki JOIN-gagnagjafa</a></td>
<td>Keyranleiki</td>
<td>Villa</td>
<td>
<p>Ekki er hægt að tengja lista &lt;slóð&gt; sem er ekki sía í fyrirspurn.</p>
<p><b>Keyrsluvilla:</b> Aðgerðin „Tengdist gagnagjafa“ á að vera síusegð, ekki hefur verið náð í reiknaðan reit á réttan hátt.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>Ákjósanleiki FILTER vs WHERE aðgerðar</a></td>
<td>Afköst</td>
<td>Viðvörun</td>
<td>Betra er að nota FILTER-aðgerðina fyrir segðina í stað WHERE séð út frá afköstum. Veljið Laga til að skipta henni út sjálfkrafa.</td>
</tr>
<tr>
<td><a href='#i8'>Ákjósanleiki ALLITEMSQUERY vs ALLITEMS aðgerðar</a></td>
<td>Afköst</td>
<td>Viðvörun</td>
<td>Betra er að nota ALLITEMSQUERY-aðgerðina fyrir segðina í stað ALLITEMS séð út frá afköstum. Veljið Laga til að skipta henni út sjálfkrafa.</td>
</tr>
<tr>
<td><a href='#i9'>Taka tillit til tómra listatilvika</a></td>
<td>Keyranleiki</td>
<td>Viðvörun</td>
<td>
<p>Listinn &lt;slóð&gt; athugar ekki tilfelli á tómum lista, sem getur valdið villu á keyrslutíma. Bætið við athugun á tómum lista.</p>
<p><b>Keyrsluvilla:</b> Listi er auður í &lt;slóð&gt;</p>
<p><b><a href='#i9a'>Hugsanlegt vandamál</a>:</b> Verið er að fylla út línu einu sinni á meðan gagnagjafi sem tekið er úr inniheldur margar færslur</p>
</td>
</tr>
<tr>
<td><a href='#i10'>Keyranleiki segðar með FILTER-aðgerð (vistar í skyndiminni)</a></td>
<td>Keyranleiki</td>
<td>Villa</td>
<td>
<p>Ekki er hægt að nota Síu fyrir valda gerð gagnagjafa. Aðeins er hægt að nota gagnaveitu af gerðinni „Töflufærslur“ þegar hún er ekki í skyndiminni og engum földuðum gagnaveitum hefur verið bætt við handvirkt.</p>
<p><b>Keyrsluvilla:</b> Síun er ekki studd. Staðfestið skilgreininguna til að fá frekari upplýsingar um þetta.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Bindingu vantar</a></td>
<td>Keyranleiki</td>
<td>Viðvörun</td>
<td>
<p>Slóðin &gt;slóð&lt; hefur enga bindingu við neinn gagnagjafa þegar vörpun líkans er notuð</p>
<p><b>Keyrsluvilla:</b> Slóðin &lt;slóð&gt; er ekki bundin</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Ekki tengt sniðmát</a></td>
<td>Heillleiki gagna</td>
<td>Viðvörun</td>
<td>Skráin &lt;nafn&gt; tengist engum skráarhlutum og verður fjarlægð þegar stöðu skilgreiningarútgáfu hefur verið breytt.</td>
</tr>
<tr>
<td><a href='#i13'>Ekki samstillt snið</a></td>
<td>Heillleiki gagna</td>
<td>Viðvörun</td>
<td>Skilgreint heiti &lt;heiti íhlutar&gt; er ekki til í Excel-skjali &lt;heiti skjals&gt;</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Umbreyting á gerð

Rafræn skýrslugerð athugar hvort gagnagerð gagnalíkansreits sé samhæfur við gagnagerð segðar sem er skilgreind sem binding þess reits. Ef gagnagerðirnar eru ósamhæfar kemur upp villa við villuleit í hönnuði líkanavörpunar rafrænnar skýrslugerðar. Skilaboðin sem berast gefa til kynna að rafræn skýrslugerð geti ekki umbreytt segð af gerðinni A í reit af gerðinni B.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjaðu að skilgreina íhluti gagnalíkans rafrænnar skýrslugerðar og líkanavörpunar rafrænnar skýrslugerðar samtímis.
2. Í gagnalíkanstrénu skal bæta við reit sem er nefndur **X** og velja **Heiltölu** sem gagnagerðina.

    ![X-svæði og heiltölugagnagerð bætt við gangalíkanstréð á síðu gagnalíkans](./media/er-components-inspections-01.png)

3. Á gagnagjafasvæði líkanavörpunar skal bæta við gagnagjafa af gerðinni **Reiknaður reitur**.
4. Gefið nýja gagnagjafanum heitið **Y** og skilgreinið hann þannig að hann innihaldi segðina `INTVALUE(100)`.
5. Binda **X** við **Y**.
6. Í hönnuði gagnalíkansins skal breyta gagnagerðinni fyrir reitinn **X** úr **Heiltala** í **Int64**.
7. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar**.

    ![að villuleita breytanlegan íhlut líkanavörpunar á síðunni Hönnuður líkanavörpunar](./media/er-components-inspections-01.gif)

8. Veljið **Villuleita** til að skoða íhlut líkanavörpunar af valinni skilgreiningu rafrænnar skýrslugerðar á síðunni **Skilgreiningar**.

    ![Villuleita til að skoða íhlut líkanavörpunar á skilgreiningarsíðunni](./media/er-components-inspections-01a.png)

9. Athugið að staðfestingarvilla kemur upp. Skilaboðin gefa til kynna að gildið af gerðinni **Heiltala** sem `INTVALUE(100)` segðin af **Y** gagnagjafanum skilar, geti ekki verið vistað í gagnalíkansreit **X** af gerðinni **Int64**.

Eftirfarandi mynd sýnir keyrsluvilluna sem kemur upp ef viðvörunin er hunsuð og valið er **Keyra** til að keyra snið sem er skilgreint til að nota líkanavörpunina.

![Keyrsluvillur á sniðshönnunarsíðunni](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Enginn valkostur til að lagfæra vandamálið sjálfkrafa er tiltækur.

### <a name="manual-resolution"></a>Handvirk lausn

#### <a name="option-1"></a>Valkostur 1

Uppfærið skipulag gagnalíkansins með því að breyta gagnagerð gagnalíkansreitsins þannig að hún samsvari gagnagerð segðarinnar sem er skilgreind fyrir bindingu reitsins. Fyrir dæmið á undan þarf að breyta gagnagerð **X** aftur í **Heiltala**.

#### <a name="option-2"></a>Valkostur 2

Uppfærið líkanavörpunina með því að breyta segð gagnagjafans sem er bundin við gagnalíkanareitinn. Fyrir dæmið á undan þarf að breyta segð gagnagjafans **Y** í `INT64VALUE(100)`.

## <a name="type-compatibility"></a><a id="i2"></a>Samhæfisgerð

Rafræn skýrslugerð athugar hvort gagnagerð sniðseiningar sé samhæf við gagnagerð segðar sem er skilgreind sem binding þessarar sniðseiningar. Ef gagnagerðirnar eru ósamhæfar kemur upp villa við villuleit í aðgerðarhönnuði rafrænnar skýrslugerðar. Skilaboðin sem þú færð tilgreina að ekki sé hægt að nota grunnstillta segð sem bindingu á núverandi sniðseiningu við gagnagjafa þar sem þessi segð skilar gildi af gagnagerð „A“ sem er utan umfangs gagnagerða sem eru studdar af núverandi sniðseiningu af gerðinni „B“.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjaðu að skilgreina íhluti gagnalíkans rafrænnar skýrslugerðar og sniðs rafrænnar skýrslugerðar samtímis.
2. Í gagnalíkanstrénu skal bæta við reit sem er nefndur **X** og velja **Heiltölu** sem gagnagerðina.
3. Í sniðsskipulagstrénu skal bæta við sniðseiningu af gerðinni **Tölustafir**.
4. Gefið nýju sniðseiningunni heitið **Y**. Í reitnum **Tölugildi** skal velja **Heiltala** sem gagnagerðina.
5. Binda **X** við **Y**.
6. Í sniðsskipulagstrénu skal breyta gagnagerð sniðseiningar **Y** úr **Heiltala** í **Int64**.
7. Veljið **Villuleita** til að skoða breytanlegan sniðshlut á síðunni **Sniðshönnuður**.

    ![Að villuleita samhæfisgerð á sniðshönnunarsíðunni](./media/er-components-inspections-02.gif)

8. Athugið að staðfestingarvilla kemur upp. Skilaboðin segja til um að skilgreinda segðin geti aðeins samþykkt **Int64** gildi. Þess vegna getur gildið fyrir gagnalíkansreit **X** af gerðinni **Heiltala** ekki verið slegið inn í sniðseiningu **Y**.

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Enginn valkostur til að lagfæra vandamálið sjálfkrafa er tiltækur.

### <a name="manual-resolution"></a>Handvirk lausn

#### <a name="option-1"></a>Valkostur 1

Uppfærið sniðsskipulagið með því að breyta gagnagerð sniðseiningarinnar **Tölustafir** þannig að hún samsvari gagnagerð segðarinnar sem er skilgreind fyrir bindingu einingarinnar. Í dæminu á undan verður að breyta gildinu **Gerð tölustafa** af sniðseiningu **X** aftur í **Heiltala**.

#### <a name="option-2"></a>Valkostur 2

Uppfærið sniðsvörpun sniðseiningar **X** með því að breyta segðinni úr `model.X` í `INT64VALUE(model.X)`.

## <a name="missing-configuration-element"></a><a id="i3"></a>Skilgreiningareiningu vantar

Rafræn skýrslugerð athugar hvort bindisegðin innihaldi aðeins gagnagjafa sem eru skilgreindir í breytanlegum íhlut rafrænnar skýrslugerðar. Fyrir hverja bindingu sem inniheldur gagnagjafa sem vantar í breytanlegum íhlut rafrænnar skýrslugerðar kemur upp villa við villuleit í aðgerðarhönnuði rafrænnar skýrslugerðar eða í hönnuði líkanavörpunar rafrænnar skýrslugerðar.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjaðu að skilgreina íhluti gagnalíkans rafrænnar skýrslugerðar og líkanavörpunar rafrænnar skýrslugerðar samtímis.
2. Í gagnalíkanstrénu skal bæta við reit sem er nefndur **X** og velja **Heiltölu** sem gagnagerðina.

    ![Gagnalíkanstré með X-reit og gagnagerðina heiltala á gagnalíkanssíðunni](./media/er-components-inspections-01.png)

3. Á gagnagjafasvæði líkanavörpunar skal bæta við gagnagjafa af gerðinni **Reiknaður reitur**.
4. Gefið nýja gagnagjafanum heitið **Y** og skilgreinið hann þannig að hann innihaldi segðina `INTVALUE(100)`.
5. Binda **X** við **Y**.
6. Í hönnuði líkanavörpunar, á svæði gagnagjafa, skal eyða gagnagjafanum **Y**.
7. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar**.

    ![Skoða breytanlegan íhlut líkanavörpunar rafrænnar skýrslugerðar á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-03.gif)

8. Athugið að staðfestingarvilla kemur upp. Skilaboðin gefa til kynna að bindingin á gagnalíkansreit **X** inniheldur slóðina sem vísar til gagnagjafa **Y**, en þessi gagnagjafi finnst ekki.

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Veljið **Losa** til að laga vandann sjálfkrafa með því að fjarlægja bindingu gagnagjafa sem vantar.

### <a name="manual-resolution"></a>Handvirk lausn

#### <a name="option-1"></a>Valkostur 1

Losið gagnalíkansreitinn **X** til að hætta að vísa í gagnagjafa **Y** sem er ekki til.

#### <a name="option-2"></a>Valkostur 2

Á gagnagjafasvæðinu í hönnuði líkanavörpunar rafrænnar skýrslugerðar skal bæta við gagnagjafa **Y** aftur.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>Keyranleiki segðar með FILTER-aðgerð

Innbyggða aðgerðin [FILTER](er-functions-list-filter.md) fyrir rafrænna skýrslugerð er notuð til að fá aðgang að forritstöflum, yfirlitum eða gagnaeiningum með því að leggja fram eitt SQL-kall til að ná í nauðsynleg gögn sem lista yfir færslur. Gagnagjafi af gerðinni **Færslulisti** er notaður sem frumbreyta þessarar aðgerðar og tilgreinir upprunastað forrits fyrir kallið. Rafræn skýrslugerð athugar hvort hægt sé að koma á beinni SQL-fyrirspurn til gagnagjafa sem vísað er til í `FILTER`-aðgerðinni. Ef ekki er hægt að koma á fót beinni fyrirspurn kemur upp villa við villuleit í hönnuði líkanavörpunar rafrænnar skýrslugerðar. Skilaboðin sem birtast gefa til kynna að segð rafrænnar skýrslugerðar sem inniheldur `FILTER`-aðgerðina sé ekki hægt að keyra við keyrslu. 

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjið að skilgreina íhlut líkanavörpunar rafrænnar skýrslugerðar.
2. Bætið við gagnagjafa af gerðinni **Dynamics 365 for Operations \\ Töflufærslur**.
3. Heiti nýja gagnagjafans **Lánardrottinn**. Í reitnum **Tafla** skal velja **VendTable** til að tilgreina að þessi gagnagjafi biðji um VendTable-töfluna.
4. Bætið við gagnagjafa af gerðinni **Reiknaður reitur**.
5. Gefið nýja gagnagjafanum heitið **FilterVendor** og skilgreinið hann þannig að hann innihaldi segðina `FILTER(Vendor, Vendor.AccountNum="US-101")`.
6. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar** og staðfestið að hægt sé að senda `FILTER(Vendor, Vendor.AccountNum="US-101")`-segðinni í gagnagjafanum **Lánardrottinn** fyrirspurn.
7. Breytið gagnagjafanum **Lánardrottinn** með því að bæta við földuðum reit af gerðinni **Reiknaður reitur** til að fá stytt númer lánardrottnalykils.
8. Gefið nýja faldaða reitnum **$AccNumber** heiti og skilgreinið hann þannig að hann innihaldi segðina `TRIM(Vendor.AccountNum)`.
9. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar** og staðfestið að hægt sé að senda `FILTER(Vendor, Vendor.AccountNum="US-101")`-segðinni í gagnagjafanum **Lánardrottinn** fyrirspurn.

    ![Hægt er að senda fyrirspurn vegna villuleitar á segðinni á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-04.gif)

10. Takið eftir því að villa við villuleit kemur upp vegna þess að gagnagjafinn **Lánardrottinn** inniheldur faldaðan reit af gerðinni **Reiknaður reitur** sem leyfir ekki að þýða segð gagnagjafans **FilteredVendor** í beina SQL-strenginn.

Eftirfarandi mynd sýnir keyrsluvilluna sem kemur upp ef viðvörunin er hunsuð og valið er **Keyra** til að keyra snið sem er skilgreint til að nota líkanavörpunina.

![Keyrsluvillur sem koma upp þegar breytanlegt snið sniðshönnunarsíðunnar er keyrt](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Enginn valkostur til að lagfæra vandamálið sjálfkrafa er tiltækur.

### <a name="manual-resolution"></a>Handvirk lausn

#### <a name="option-1"></a>Valkostur 1

Í stað þess að bæta földuðum reit af gerðinni **Reiknaður reitur** við gagnagjafann **Lánardrottinn** skal bæta faldaða reitnum **$AccNumber** við gagnagjafann **FilteredVendor** og skilgreina hann þannig að hann innihaldi segðina `TRIM(FilteredVendor.AccountNum)`. Á þennan hátt er hægt að keyra segðina `FILTER(Vendor, Vendor.AccountNum="US-101")` á SQL-stigi og reikna faldaða reitinn **$AccNumber** eftir á.

#### <a name="option-2"></a>Valkostur 2

Breytið segðinni á gagnagjafa **FilteredVendor** úr `FILTER(Vendor, Vendor.AccountNum="US-101")` í `WHERE(Vendor, Vendor.AccountNum="US-101")`. Ekki er mælt með því að breyta segð fyrir töflu sem er með mikið gagnamagn (færslutafla) vegna þess að allar færslur verða sóttar og val á nauðsynlegum færslum verður gert í minni. Þess vegna getur þessi nálgun valdið slökum afköstum. Nánari upplýsingar er að finna í [WHERE-aðgerð rafrænnar skýrslugerðar](er-functions-list-where.md).

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>Keyranleiki um GROUPBY-gagnagjafa

Gagnagjafinn **GROUPBY** skiptir niðurstöðum fyrirspurnar í flokka af færslum, oftast í þeim tilgangi að gera eina eða fleiri uppsöfnun í hverjum flokki. Hægt er að skilgreina sérhvern **GROUPBY** gagnagjafa þannig að hann sé keyrður annaðhvort á gagnagrunnsstigi eða í minni. Þegar **GROUPBY** gagnagjafi er skilgreindur þannig að hann sé keyrður á gagnagrunnsstigi, athugar rafræn skýrslugerð hvort hægt sé að koma á fót beinni SQL-fyrirspurn við gagnagjafa sem vísað er til í þeim gagnagjafa. Ef ekki er hægt að koma á fót beinni fyrirspurn kemur upp villa við villuleit í hönnuði líkanavörpunar rafrænnar skýrslugerðar. Skilaboðin sem berast segja að ekki sé hægt að keyra skilgreinda gagnagjafann **GROUPBY** við keyrslu.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjið að skilgreina íhlut líkanavörpunar rafrænnar skýrslugerðar.
2. Bætið við gagnagjafa af gerðinni **Dynamics 365 for Operations \\ Töflufærslur**.
3. Gefið nýja gagngjafanum **Trans** heiti. Í reitnum **Tafla** skal velja **VendTrans** til að gefa til kynna að þessi gagnagjafi muni óska eftir VendTrans-töflunni.
4. Bætið við gagnagjafa af gerðinni **Flokka eftir**.
5. Gefa skal nýja gagnagjafanum heitið **GroupedTrans**, og grunnstilla hann á eftirfarandi hátt:

    - Veljið **Trans** gagnagjafann sem uppruna færslna sem á að flokka.
    - Í reitnum **Staðsetning keyrslu** skal velja **Fyrirspurn** til að tilgreina að ætlunin sé að keyra þennan gagnagjafa á gagnagrunnsstigi.

    ![Gagnagjafi skilgreindur á færibreytusíðunni „Breyta Flokka eftir“](./media/er-components-inspections-05a.gif)

6. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar** og staðfestið að hægt sé að senda skilgreindum gagnagjafa **GroupedTrans** fyrirspurn.
7. Breytið gagnagjafanum **Trans** með því að bæta við földuðum reit af gerðinni **Reiknaður reitur** til að fá stytt númer lánardrottnalykils.
8. Gefið nýja gagnagjafanum heitið **$AccNumber** og skilgreinið hann þannig að hann innihaldi segðina `TRIM(Trans.AccountNum)`.

    ![Gagnagjafi skilgreindur á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-05a.png)

9. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar** og staðfestið að hægt sé að senda skilgreindum gagnagjafa **GroupedTrans** fyrirspurn.

    ![Villuleitið hlut líkanavörpunar rafrænnar skýrslugerðar og staðfestið skilgreindan gagnagjafa, hægt er að senda GroupedTrans fyrirspurn á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-05b.png)

10. Takið eftir því að villa við villuleit kemur upp vegna þess að gagnagjafinn **Trans** inniheldur faldaðan reit af gerðinni **Reiknaður reitur** sem leyfir ekki að þýða kallið í gagnagjafann **FilteredVendor** í beina SQL-strenginn.

Eftirfarandi mynd sýnir keyrsluvilluna sem kemur upp ef viðvörunin er hunsuð og valið er **Keyra** til að keyra snið sem er skilgreint til að nota líkanavörpunina.

![Keyrsluvillur sem eiga sér stað þegar viðvörun er hunsuð á sniðshönnunarsíðu](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Enginn valkostur til að lagfæra vandamálið sjálfkrafa er tiltækur.

### <a name="manual-resolution"></a>Handvirk lausn

#### <a name="option-1"></a>Valkostur 1

Í stað þess að bæta földuðum reit af gerðinni **Reiknaður reitur** við gagnagjafann **Trans** skal bæta við faldaða reitnum **$AccNumber** fyrir atriðið **GroupedTrans.lines** fyrir gagnagjafann **GroupedTrans** og skilgreina hann þannig að hann innihaldi segðina `TRIM(GroupedTrans.lines.AccountNum)`. Á þennan hátt er hægt að keyra gagnagjafann **GroupedTrans** á SQL-stigi og reikna faldaða reitinn **$AccNumber** eftir á.

#### <a name="option-2"></a>Valkostur 2

Breytið gildi reitsins **Staðsetning keyrslu** fyrir gagnagjafann **GroupedTrans** úr **Fyrirspurn** í **Í minni**. Ekki er mælt með því að breyta segð fyrir töflu sem er með mikið gagnamagn (færslutafla) vegna þess að allar færslur verða sóttar og flokkun og uppsöfnun verður gerð í minni. Þess vegna getur þessi nálgun valdið slökum afköstum.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>Keyranleiki JOIN-gagnagjafa

Gagnagjafinn [JOIN](er-join-data-sources.md) sameinar færslur úr tveimur eða fleiri gagnagrunnstöflum byggt á tengdum reitum. Hægt er að skilgreina sérhvern **JOIN** gagnagjafa þannig að hann sé keyrður annaðhvort á gagnagrunnsstigi eða í minni. Þegar **JOIN** gagnagjafi er skilgreindur þannig að hann sé keyrður á gagnagrunnsstigi, athugar rafræn skýrslugerð hvort hægt sé að koma á fót beinni SQL-fyrirspurn við gagnagjafa sem vísað er til í þeim gagnagjafa. Ef ekki er hægt að koma á fót beinni SQL-fyrirspurn með a.m.k. einni tilvísun í gagnagjafa, kemur upp villa við villuleit í hönnuði líkanavörpunar rafrænnar skýrslugerðar. Skilaboðin sem berast segja að ekki sé hægt að keyra skilgreinda gagnagjafann **JOIN** við keyrslu.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjið að skilgreina íhlut líkanavörpunar rafrænnar skýrslugerðar.
2. Bætið við gagnagjafa af gerðinni **Dynamics 365 for Operations \\ Töflufærslur**.
3. Heiti nýja gagnagjafans **Lánardrottinn**. Í reitnum **Tafla** skal velja **VendTable** til að tilgreina að þessi gagnagjafi biðji um VendTable-töfluna.
4. Bætið við gagnagjafa af gerðinni **Dynamics 365 for Operations \\ Töflufærslur**.
5. Gefið nýja gagngjafanum **Trans** heiti. Í reitnum **Tafla** skal velja **VendTrans** til að gefa til kynna að þessi gagnagjafi muni óska eftir VendTrans-töflunni.
6. Bætið við gagnagjafa af gerðinni **Reiknaður reitur** sem faldaðan reit af gagnagjafanum **Lánardrottinn**.
7. Gefið nýja gagnagjafanum heitið **FilteredTrans** og skilgreinið hann þannig að hann innihaldi segðina `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.
8. Bætið við gagnagjafa af gerðinni **Join**.
9. Gefa skal nýja gagnagjafanum heitið **JoinedList**, og grunnstilla hann á eftirfarandi hátt:

    1. Bætið við gagnagjafanum **Lánardrottinn** sem fyrsta safn af færslum sem á að tengja.
    2. Bætið við gagnagjafanum **Vendor.FilteredTrans** sem annað safn af færslum sem á að tengja. Veljið **INNER** sem gerðina.
    3. Í reitnum **Keyra** skal velja **Fyrirspurn** til að tilgreina að ætlunin sé að keyra þennan gagnagjafa á gagnagrunnsstigi.

    ![Gagnagjafi skilgreindur á hönnunarsíðu töflutengingar](./media/er-components-inspections-06a.gif)

10. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar** og staðfestið að hægt sé að senda skilgreindum gagnagjafa **JoinedList** fyrirspurn.
11. Breytið segðinni á gagnagjafa **Vendor.FilteredTrans** úr `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` í `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.
12. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar** og staðfestið að hægt sé að senda skilgreindum gagnagjafa **JoinedList** fyrirspurn.

    ![Villuleitið breytanlegum hlutum líkanavörpunar og staðfestið að hægt sé að senda gagnagjafanum JoinedList fyrirspurn á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-06b.png)

13. Takið eftir að villa við villuleit kemur upp vegna þess að ekki er hægt að þýða segð gagnagjafans **Vendor.FilteredTrans** í beint SQL-kall. Þar að auki leyfir beint SQL-kall ekki kallið fyrir gagnagjafann **JoinedList** að vera þýtt yfir í beinan SQL-streng.

    ![Keyrsluvillur úr mislukkaðri villuleit á gagnagjafa JoinedList á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-06c.png)

Eftirfarandi mynd sýnir keyrsluvilluna sem kemur upp ef viðvörunin er hunsuð og valið er **Keyra** til að keyra snið sem er skilgreint til að nota líkanavörpunina.

![Breytanlegt snið keyrt á sniðshönnunarsíðu](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Enginn valkostur til að lagfæra vandamálið sjálfkrafa er tiltækur.

### <a name="manual-resolution"></a>Handvirk lausn

#### <a name="option-1"></a>Valkostur 1

Breytið segðinni á gagnagjafa **Vendor.FilteredTrans** úr `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` og aftur í `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` eins og viðvörunin ráðleggur.

![Uppfærð segð gagnagjafa á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>Valkostur 2

Breytið gildi reitsins **Keyra** fyrir gagnagjafann **JoinedList** úr **Fyrirspurn** í **Í minni**. Ekki er mælt með því að breyta segð fyrir töflu sem er með mikið gagnamagn (færslutafla) vegna þess að allar færslur verða sóttar og töflutenging verður gerð í minni. Þess vegna getur þessi nálgun valdið slökum afköstum. Viðvörunar er sýnd til að upplýsa um þessa hættu.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>Ákjósanleiki FILTER vs WHERE aðgerðar

Innbyggða aðgerðin [FILTER](er-functions-list-filter.md) fyrir rafrænna skýrslugerð er notuð til að fá aðgang að forritstöflum, yfirlitum eða gagnaeiningum með því að leggja fram eitt SQL-kall til að ná í nauðsynleg gögn sem lista yfir færslur. Aðgerðin [WHERE](er-functions-list-where.md) sækir allar færslur úr uppgefnum upprunastað og velur færslur í minni. Gagnagjafi af gerðinni **Færslulisti** er notaður sem frumbreyta beggja aðgerðanna og tilgreinir upprunastað til að ná í færslur. Rafræn skýrslugerð athugar hvort hægt sé að koma á beinu SQL-kalli til gagnagjafa sem vísað er til í aðgerðinni **WHERE**. Ef hægt að koma á fót beinu kalli kemur upp viðvörun villuleitar í hönnuði líkanavörpunar rafrænnar skýrslugerðar. Skilaboðin sem birtast ráðleggja að nota aðgerðina **FILTER** í staðinn fyrir aðgerðina **WHERE** til að auka skilvirknina.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjið að skilgreina íhlut líkanavörpunar rafrænnar skýrslugerðar.
2. Bætið við gagnagjafa af gerðinni **Dynamics 365 for Operations \\ Töflufærslur**.
3. Gefið nýja gagngjafanum **Trans** heiti. Í reitnum **Tafla** skal velja **VendTrans** til að gefa til kynna að þessi gagnagjafi muni óska eftir VendTrans-töflunni.
4. Bætið við gagnagjafa af gerðinni **Reiknaður reitur** sem faldaðan reit af gagnagjafanum **Lánardrottinn**.
5. Gefið nýja gagnagjafanum heitið **FilteredTrans** og skilgreinið hann þannig að hann innihaldi segðina `WHERE(Trans, Trans.AccountNum="US-101")`.
6. Bætið við gagnagjafa af gerðinni **Dynamics 365 for Operations \\ Töflufærslur**.
7. Heiti nýja gagnagjafans **Lánardrottinn**. Í reitnum **Tafla** skal velja **VendTable** til að tilgreina að þessi gagnagjafi biðji um VendTable-töfluna.
8. Bætið við gagnagjafa af gerðinni **Reiknaður reitur**.
9. Gefið nýja gagnagjafanum heitið **FilterVendor** og skilgreinið hann þannig að hann innihaldi segðina `WHERE(Vendor, Vendor.AccountNum="US-101")`.
10. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar**.

    ![Veljið villuleita til að skoða breytanlegan íhlut líkanavörpunar á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-07a.png)

11. Takið eftir að viðvaranir villuleitar ráðleggja að nota aðgerðina **FILTER** í staðinn fyrir aðgerðina **WHERE** fyrir gagnagjafana **FilteredVendor** og **FilteredTrans**.

    ![Viðvaranir villuleitar sem ráðleggja filter-aðgerð í staðinn fyrir where-aðgerð á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Veljið **Laga** til að skipta sjálfkrafa út aðgerðinni **WHERE** fyrir aðgerðina **FILTER** í segð allra gagnagjafa sem birtast í hnitanetinu í flipanum **Viðvaranir** fyrir þessa gerð eftirlits.

Annars er líka hægt að velja línuna fyrir ákveðna viðvörun í hnitanetinu og síðan velja **Laga það sem er valið**. Í þessu tilviki er segðinni sjálfkrafa aðeins breytt í gagnagjafanum sem er minnst á í valinni viðvörun.

![Veljið Laga til að skipta út where-aðgerðinni sjálfkrafa fyrir filter-aðgerðina á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>Handvirk lausn

Hægt er að leiðrétta segðir allra gagnagjafa sem nefndir eru í hnitaneti villuleitar með því að skipta út aðgerðinni **WHERE** í staðinn fyrir aðgerðina **FILTER**.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>Ákjósanleiki ALLITEMSQUERY vs ALLITEMS aðgerðar

Innbyggðu aðgerðirnar [ALLITEMS](er-functions-list-allitems.md) og [ALLITEMSQUERY](er-functions-list-allitemsquery.md) fyrir rafræna skýrslugerð eru notaðar til að fá útflatt gildi fyrir **Færslulista** sem samanstendur af lista yfir færslur sem sýnir öll atriði sem passa við tiltekna slóð. Rafræn skýrslugerð athugar hvort hægt sé að koma á beinu SQL-kalli til gagnagjafa sem vísað er til í aðgerðinni **ALLITEMS**. Ef hægt að koma á fót beinu kalli kemur upp viðvörun villuleitar í hönnuði líkanavörpunar rafrænnar skýrslugerðar. Skilaboðin sem birtast ráðleggja að nota aðgerðina **ALLITEMSQUERY** í staðinn fyrir aðgerðina **ALLITEMS** til að auka skilvirknina.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjið að skilgreina íhlut líkanavörpunar rafrænnar skýrslugerðar.
2. Bætið við gagnagjafa af gerðinni **Dynamics 365 for Operations \\ Töflufærslur**.
3. Heiti nýja gagnagjafans **Lánardrottinn**. Í reitnum **Tafla** skal velja **VendTable** til að tilgreina að þessi gagnagjafi biðji um VendTable-töfluna.
4. Bætið við gagnagjafa af gerðinni **Reiknaður reitur** til að ná í færslur fyrir ýmsa lánardrottna.
5. Gefið nýja gagnagjafanum heitið **FilterVendor** og skilgreinið hann þannig að hann innihaldi segðina `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.
6. Bætið við gagnagjafa af gerðinni **Reiknaður reitur** til að ná í færslur síaðra lánardrottna.
7. Gefið nýja gagnagjafanum heitið **FilteredVendorTrans** og skilgreinið hann þannig að hann innihaldi segðina `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.
8. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar**.

    ![Hönnunarsíða líkanavörpunar, villuleitarhnappur](./media/er-components-inspections-08a.png)

9. Takið eftir að viðvörun vegna villuleitar á sér stað. Skilaboðin ráðleggja að nota aðgerðina **ALLITEMSQUERY** í staðinn fyrir aðgerðina **ALLITEMS** fyrir gagnagjafann **FilteredVendorTrans**.

    ![Viðvörun villuleitar um að nota ALLITEMSQUERY í staðinn fyrir ALLITEMS aðgerðina í líkanavörpunarhlut rafrænnar skýrslugerðar á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Veljið **Laga** til að skipta sjálfkrafa út aðgerðinni **ALLITEMS** fyrir aðgerðina **ALLITEMSQUERY** í segð allra gagnagjafa sem birtast í hnitanetinu í flipanum **Viðvaranir** fyrir þessa gerð eftirlits.

Annars er líka hægt að velja línuna fyrir ákveðna viðvörun í hnitanetinu og síðan velja **Laga það sem er valið**. Í þessu tilviki er segðinni sjálfkrafa aðeins breytt í gagnagjafanum sem er minnst á í valinni viðvörun.

![Á hönnunarsíður líkanavörpunar skal velja Laga](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>Handvirk lausn

Hægt er að leiðrétta segðir allra gagnagjafa sem nefndir eru í hnitaneti villuleitar með því að skipta út aðgerðinni **ALLITEMS** í staðinn fyrir aðgerðina **ALLITEMSQUERY**.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Taka tillit til tómra listatilvika

Hægt er að skilgreina hluti rafræns skýrslugerðarsniðs eða líkanavörpunar rafrænnar skýrslugerðar til að fá reitargildi gagnagjafa af gerðinni **Færslulisti**. Rafræn skýrslugerð athugar hvort hönnunin taki tillit til tilviksins þar sem gagnagjafi sem kallað er á inniheldur engar færslur (hann er sem sagt tómur) til að koma í veg fyrir villur við keyrslu þegar gildi er sótt úr reit færslu sem er ekki til.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjaðu að skilgreina íhluti gagnalíkans rafrænnar skýrslugerðar, líkanavörpunar rafrænnar skýrslugerðar og sniðs rafrænnar skýrslugerðar samtímis.
2. Í gagnalíkanstré skal bæta við rótaratriði sem er nefnt **Root3**.
3. Breytið atriðinu **Root3** með því að bæta við földuðu atriði af gerðinni **Færslulisti**.
4. Gefið nýja faldaða atriðinu **Lánardrottinn** heiti.
5. Breytið atriðinu **Lánardtottir** á eftirfarandi hátt:

    - Bætið við földum reit af gerðinni **Strengur** og gefið honum heitið **Heiti**.
    - Bætið við földum reit af gerðinni **Strengur** og gefið honum heitið **AccountNumber**.

    ![Földum reitum bætt við gagnalíkanssíðuna](./media/er-components-inspections-09a.png)

6. Á gagnagjafasvæði líkanavörpunar skal bæta við gagnagjafa af gerðinni **Dynamics 365 for Operations \\ Töflufærslur**.
7. Heiti nýja gagnagjafans **Lánardrottinn**. Í reitnum **Tafla** skal velja **VendTable** til að tilgreina að þessi gagnagjafi biðji um VendTable-töfluna.
8. Bætið gagnagjafa af gerðinni **Almenn \\ innsláttarfæribreyta notanda** til að leita að lánardrottnalykli í svarglugga keyrslu.
9. Gefið nýja gagnagjafanum heitið **RequestedAccountNum**. Í reitinn **Merki** skal slá inn **Númer lánardrottnalykils**. Í reitnum **Heiti á gerð gagnaaðgerðar** skal skilja sjálfgefna gildið **Lýsing** eftir.
10. Bætið við gagnagjafa af gerðinni **Reiknaður reitur** til að sía lánardrottin sem spurst er fyrir um.
11. Gefið nýja gagnagjafanum heitið **FilteredVendor** og skilgreinið hann þannig að hann innihaldi segðina `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Bindið atriði gagnalíkans við skilgreinda gagnagjafa á eftirfarandi hátt:

    - Bindið **FilteredVendor** við **Lánardrottinn**.
    - Binda **FilteredVendor.AccountNum** við **Vendor.AccountNumber**.
    - Bindið **FilteredVendor.'name()'** við **Vendor.name**.

    ![Atriði gagnalíkans bundin við hönnunarsíðu líkanavörpunar](./media/er-components-inspections-09b.png)

13. Í tré sniðsskipulags skal bæta við eftirfarandi atriðum til að mynda skjal á útleið á XML-sniði sem inniheldur upplýsingar um lánardrottin:

    1. Bætið við rótinni **Uppgjör** fyrir XML-eininguna.
    2. Fyrir XML-eininguna **Uppgjör** skal bæta við földuðu XML-einingunni **Aðili**.
    3. Fyrir XML-eininguna **Aðili** skal bæta við eftirfarandi földuðum XML-eigindum:

        - Nafn
        - AccountNum

14. Bindið sniðseiningar til að bjóða upp á gagnagjafa á eftirfarandi hátt:

    - Bindið sniðseininguna **Uppgjör\\Aðili\\Heiti** við gagnagjafareitinn **model.Vendor.Name**.
    - Bindið sniðseininguna **Uppgjör\\Aðili\\AccountNum** við gagnagjafareitinn **model.Vendor.AccountNumber**.

15. Veljið **Villuleita** til að skoða breytanlegan sniðshlut á síðunni **Sniðshönnuður**.

    ![Villuleita sniðseiningar sem bundnar voru við gagnagjafa á sniðshönnunarsíðunni](./media/er-components-inspections-09c.png)

16. Athugið að staðfestingarvillur koma upp. Skilaboðin gefa til kynna að villan gæti verið út af skilgreindum sniðshlutunum **Uppgjör\\Aðili\\Heiti** og **Uppgjör\\Aðili\\AccountNum** við keyrslu ef listinn **model.Vendor** er tómur.

    ![Villa við villuleit sem tilkynnir um hugsanlega villu vegna skilgreindra sniðshluta](./media/er-components-inspections-09d.png)

Eftirfarandi mynd sýnir keyrsluvilluna sem kemur upp ef viðvörunin er hunsuð, valið er **Keyra** til að keyra sniðið og lykilnúmerið er valið fyrir lánardrottin sem er ekki til. Vegna þess að umbeðinn lánardrottinn er ekki til verður listinn **model.Vendor** tómur (þ.e. hann mun ekki innihalda neinar færslur).

![Keyrsluvillur vegna þess að það kom upp við keyrslu sniðsvörpunar](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Fyrir valda línu í hnitanetinu í flipanum **Viðvaranir** er hægt að velja **Losa**. Bindingin sem bendir á dálkinn **Slóð** er sjálfkrafa fjarlægð úr sniðseiningum.

### <a name="manual-resolution"></a>Handvirk lausn

#### <a name="option-1"></a>Valkostur 1

Hægt er að binda sniðseininguna **Uppgjör\\Aðili\\Heiti** við gagnagjafaatriðið **model.Vendor**. Við keyrslu kallar þessi binding fyrst á gagnagjafann **model.Vendor**. Þegar **model.Vendor** skilar tómum færslulista, eru földuðu sniðseiningarnar ekki keyrðar. Þess vegna koma engar viðvaranir villuleitar upp fyrir þessa sniðsskilgreiningu.

![Sniðseiningin bundin við atriði gagnagjafa á sniðshönnunarsíðunni](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>Valkostur 2

Breytið bindingu sniðseiningarinnar **Uppgjör\\Aðili\\Heiti** úr `model.Vendor.Name` í `FIRSTORNULL(model.Vendor).Name`. Uppfærð binding umbreytir með skilyrðum fyrstu færsluna af gagnagjafanum **model.Vendor** af gerðinni **Færslulisti** við nýjan gagnagjafa af gerðinni **Færsla**. Þessi nýi gagnagjafi inniheldur sömu reitina.

- Ef a.m.k. ein færsla er tiltæk í gagnagjafanum **model.Vendor**, eru reitir þeirrar færslu fylltir út með gildum reitanna fyrir fyrstu færslu gagnagjafans **model.Vendor**. Í þessu tilviki skilar uppfærð binding lánardrottnaheitinu.
- Annars verða allir reitir færslunnar sem er stofnuð fylltir út með sjálfgefna gildinu fyrir gagnagerð þessa reits. Í þessu tilfelli er auða strengnum skilað sem sjálfgefnu gildi af gagnagerðinni **Strengur**.

Þess vegna birtast engar viðvaranir villuleitar fyrir sniðseininguna **Uppgjör\\Aðili\\Heiti** þegar hún er bundin við `FIRSTORNULL(model.Vendor).Name` segðina.

![Breytt binding leysir úr viðvörunum villuleitar á sniðshönnunarsíðunni](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>Valkostur 3

Ef ætlunin er að tilgreina sérstaklega gögnin sem eru færð inn í myndað skjal þegar gagnagjafinn **model.Vendor** af gerðinni **Færslulisti** skilar engum færslum (textanum **Engar færslur** í þessu dæmi) skal breyta bindingunni á sniðseiningunni **Uppgjör\\Aðili\\Heiti** úr `model.Vendor.Name` í `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`. Einnig er hægt að nota segðina `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.

### <a name="additional-consideration"></a><a id="i9a"></a>Fleira sem þarf að hafa í huga

Eftirlitið varar einnig við öðru mögulegu vandamáli. Að sjálfgefnu, þegar sniðseiningarnar **Uppgjör\\Aðili\\Heiti** og **Uppgjör\\Aðila\\AccountNum** eru bundnar við viðeigandi reiti gagnagjafans **model.Vendor** af gerðinni **Færslulisti**, verða þessar bindingar keyrðar og fá gildi viðeigandi reita fyrstu færslu gagnagjafans **model.Vendor** ef sá listi er tómur.

Vegna þess að sniðseiningin **Uppgjör\\Aðili** hefur ekki verið bundin við gagnagjafann **model.Vendor**, verður einingin **Uppgjör\\Aðili** ekki endurtekin fyrir hverja færslu gagnagjafans **model.Vendor** við keyrslu sniðsins. Þess í stað verður myndað skjal fyllt út með upplýsingum úr aðeins fyrstu færslu færslulistans, ef sá listi inniheldur margar færslur. Þess vegna gæti komið upp vandamál ef sniðið á að fylla út myndað skjal með upplýsingum um alla lánardrottna úr gagnagjafanum **model.Vendor**. Til að leysa þetta vandamál skal binda eininguna **Uppgjör\\Aðili** við gagnagjafann **model.Vendor**.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>Keyranleiki segðar með FILTER-aðgerð (vistar í skyndiminni)

Ýmsar innbyggðar aðgerðir [FILTER](er-functions-list-filter.md) og [ALLITEMSQUERY](er-functions-list-allitemsquery.md) fyrir rafrænna skýrslugerð eru notaðar til að fá aðgang að forritstöflum, yfirlitum eða gagnaeiningum með því að leggja fram eitt SQL-kall til að ná í nauðsynleg gögn sem lista yfir færslur. Gagnagjafi af gerðinni **Færslulisti** er notaður sem frumbreyta hverrar aðgerðar fyrir sig og tilgreinir upprunastað forrits fyrir kallið. Rafræn skýrslugerð athugar hvort hægt sé að koma á beinu SQL-kalli til gagnagjafa sem vísað er til í eina af þessum aðgerðum. Ef ekki er hægt að koma á beinu kalli vegna þess að gagnagjafinn var merktur sem [vista í skyndiminni](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace) kemur upp villa við villuleit í hönnuði líkanavörpunar rafrænnar skýrslugerðar. Skilaboðin sem birtast gefa til kynna að segð rafrænnar skýrslugerðar sem inniheldur eina þessara aðgerða sé ekki hægt að keyra við keyrslu.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjið að skilgreina íhlut líkanavörpunar rafrænnar skýrslugerðar.
2. Bætið við gagnagjafa af gerðinni **Dynamics 365 for Operations \\ Töflufærslur**.
3. Heiti nýja gagnagjafans **Lánardrottinn**. Í reitnum **Tafla** skal velja **VendTable** til að tilgreina að þessi gagnagjafi biðji um VendTable-töfluna.
4. Bætið gagnagjafa af gerðinni **Almenn \\ innsláttarfæribreyta notanda** til að leita að lánardrottnalykli í svarglugga keyrslu.
5. Gefið nýja gagnagjafanum heitið **RequestedAccountNum**. Í reitinn **Merki** skal slá inn **Númer lánardrottnalykils**. Í reitnum **Heiti á gerð gagnaaðgerðar** skal skilja sjálfgefna gildið **Lýsing** eftir.
6. Bætið við gagnagjafa af gerðinni **Reiknaður reitur** til að sía lánardrottin sem spurst er fyrir um.
7. Gefið nýja gagnagjafanum heitið **FilteredVendor** og skilgreinið hann þannig að hann innihaldi segðina `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
8. Merkið skilgreinda gagnagjafann **Lánardrottinn** sem vistun í skyndiminni.

    ![Skilgreina hlut líkanavörpunar á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-10a.gif)

9. Veljið **Villuleita** til að skoða breytanlegan íhlut líkanavörpunar á síðunni **Hönnuður líkanavörpunar**.

    ![Villuleita síunaraðgerðina sem notuð er fyrir gagnagjafa lánardrottins í skyndiminni á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-10a.png)

10. Athugið að staðfestingarvilla kemur upp. Skilaboðin gefa til kynna að ekki sé hægt að nota aðgerðina **FILTER** á gagnagjafanum **Lánardrottinn** sem vistaður er í skyndiminni.

Eftirfarandi mynd sýnir keyrsluvilluna sem kemur upp ef viðvörunin er hunsuð og valið er **Keyra** til að keyra sniðið.

![Keyrsluvilla sem kom upp við keyrslu sniðsvörpunar á sniðshönnunarsíðunni](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Enginn valkostur til að lagfæra vandamálið sjálfkrafa er tiltækur.

### <a name="manual-resolution"></a>Handvirk lausn

#### <a name="option-1"></a>Valkostur 1

Fjarlægið flaggið **Skyndiminni** úr gagnagjafanum **Lánardrottinn**. Gagnagjafinn **FilteredVendor** verður þá keyrsluhæfur, en gagnagjafinn **Lánardrottinn** sem vísað er til í VendTable-töflunni verður opnaður í hvert skipti sem kallað er á gagnagjafann **FilteredVendor**.

#### <a name="option-2"></a>Valkostur 2

Breytið segðinni á gagnagjafa **FilteredVendor** úr `FILTER(Vendor, Vendor.AccountNum="US-101")` í `WHERE(Vendor, Vendor.AccountNum="US-101")`. Í þessu tilviki verður gagnagjafinn **Lánardrottinn** sem vísað er til í VendTable-töflunni aðeins opnaður við fyrsta kall í gagnagjafann **Lánardrottinn**. Hins vegar fer val færslna fram í minninu. Þess vegna getur þessi nálgun valdið slökum afköstum.

## <a name="missing-binding"></a><a id="i11"></a>Bindingu vantar

Þegar hlutur rafræns skýrslugerðarsniðs er skilgreindur, er grunngagnalíkan rafrænnar skýrslugerðar boðið sem sjálfgefinn gagnagjafi fyrir rafrænt skýrslugerðarsnið. Þegar skilgreint snið rafrænnar skýrslugerðar er keyrt, er [sjálfgefin líkanavörpun](er-country-dependent-model-mapping.md) fyrir grunnlíkanið notað til að fylla út gagnalíkanið með forritsgögnum. Hönnuður rafræns skýrslugerðarsniðs sýnir viðvörun ef sniðseining er bundin við atriði gagnalíkans sem ekki er bundið við neinn gagnagjafa í líkanavörpuninni sem er valin sem sjálfgefin líkanavörpun fyrir breytanlegt snið. Ekki er hægt að keyra þessa gerð bindingar á keyrslutíma vegna þess að sniðið sem keyrir getur ekki fyllt út bundna einingu með forritsgögnum. Þess vegna kemur villa við keyrslu.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Byrjaðu að skilgreina íhluti gagnalíkans rafrænnar skýrslugerðar, líkanavörpunar rafrænnar skýrslugerðar og sniðs rafrænnar skýrslugerðar samtímis.
2. Í gagnalíkanstré skal bæta við rótaratriði sem er nefnt **Root3**.
3. Breytið atriðinu **Root3** með því að bæta við nýju földuðu atriði af gerðinni **Færslulisti**.
4. Gefið nýja faldaða atriðinu **Lánardrottinn** heiti.
5. Breytið atriðinu **Lánardtottir** á eftirfarandi hátt:

    - Bætið við földum reit af gerðinni **Strengur** og gefið honum heitið **Heiti**.
    - Bætið við földum reit af gerðinni **Strengur** og gefið honum heitið **AccountNumber**.

    ![Bæta földum reitum við lánardrottnaatriðið á gagnalíkanssíðunni](./media/er-components-inspections-11a.png)

6. Á gagnagjafasvæði líkanavörpunar skal bæta við gagnagjafa af gerðinni **Dynamics 365 for Operations \\ Töflufærslur**.
7. Heiti nýja gagnagjafans **Lánardrottinn**. Í reitnum **Tafla** skal velja **VendTable** til að tilgreina að þessi gagnagjafi biðji um VendTable-töfluna.
8. Bætið gagnagjafa af gerðinni **Almenn \\ innsláttarfæribreyta notanda** til að spyrjast fyrir um lánardrottnalykil í svarglugga keyrslu.
9 Gefið nýja gagnagjafanum heitið **RequestedAccountNum**. Í reitinn **Merki** skal slá inn **Númer lánardrottnalykils**. Í reitnum **Heiti á gerð gagnaaðgerðar** skal skilja sjálfgefna gildið **Lýsing** eftir.
10. Bætið við gagnagjafa af gerðinni **Reiknaður reitur** til að sía lánardrottin sem spurst er fyrir um.
11. Gefið nýja gagnagjafanum heitið **FilteredVendor** og skilgreinið hann þannig að hann innihaldi segðina `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Bindið atriði gagnalíkans við skilgreinda gagnagjafa á eftirfarandi hátt:

    - Bindið **FilteredVendor** við **Lánardrottinn**.
    - Binda **FilteredVendor.AccountNum** við **Vendor.AccountNumber**.

    > [!NOTE]
    > Gagnalíkansreiturinn **Vendor.name** helst óbundinn.

    ![Atriði gagnalíkans bundin við skilgreinda gagnagjafa og atriði gagnalíkans sem helst áfram á hönnunarsíðu líkanavörpunar](./media/er-components-inspections-11b.png)

13. Í tré sniðsskipulags skal bæta við eftirfarandi atriðum til að mynda skjal á útleið á XML-sniði sem inniheldur upplýsingar um lánardrottin sem spurst er fyrir um:

    1. Bætið við rótinni **Uppgjör** fyrir XML-eininguna.
    2. Fyrir XML-eininguna **Uppgjör** skal bæta við földuðu XML-einingunni **Aðili**.
    3. Fyrir XML-eininguna **Aðili** skal bæta við eftirfarandi földuðum XML-eigindum:

        - Nafn
        - AccountNum

14. Bindið sniðseiningarnar til að bjóða upp á gagnagjafa á eftirfarandi hátt:

    - Bindið sniðseininguna **Uppgjör\\Aðili** við gagnagjafaatriðið **model.Vendor**.
    - Bindið sniðseininguna **Uppgjör\\Aðili\\Heiti** við gagnagjafareitinn **model.Vendor.Name**.
    - Bindið sniðseininguna **Uppgjör\\Aðili\\AccountNum** við gagnagjafareitinn **model.Vendor.AccountNumber**.

15. Veljið **Villuleita** til að skoða breytanlegan sniðshlut á síðunni **Sniðshönnuður**.

    ![Hlutur rafræns skýrslugerðarsniðs villuleitaður á sniðshönnunarsíðunni](./media/er-components-inspections-11c.png)

16. Takið eftir að viðvörun vegna villuleitar á sér stað. Skilaboðin segja að gagnagjafareiturinn **model.Vendor.Name** sé ekki bundinn við neinn gagnagjafa í líkanavörpuninni sem er skilgreind til að vera notuð af sniðinu. Þess vegna er ekki víst að sniðseiningin **Uppgjör\\Aðili\\Heiti** verður fyllt út við keyrslu og undantekning keyrslu gæti komið upp.

    ![Hlutur rafræns skýrslugerðarsniðs villuleitaður á sniðshönnunarsíðunni](./media/er-components-inspections-11d.png)

Eftirfarandi mynd sýnir keyrsluvilluna sem kemur upp ef viðvörunin er hunsuð og valið er **Keyra** til að keyra sniðið.

![Kleyra breytanlegt snið á sniðshönnunarsíðu](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Enginn valkostur til að lagfæra vandamálið sjálfkrafa er tiltækur.

### <a name="manual-resolution"></a>Handvirk lausn

#### <a name="option-1"></a>Valkostur 1

Breytið skilgreindri líkanavörpun með því að bæta við bindingu fyrir gagnagjafareitinn **model.Vendor.Name**.

#### <a name="option-2"></a>Valkostur 2

Breytið skilgreindu sniði með því að fjarlægja bindingu fyrir sniðseininguna **Uppgjör\\Aðili\\Heiti**.

## <a name="not-linked-template"></a><a id="i12"></a>Ekki tengt sniðmát

Þegar sniðshlutur rafrænnar skýrslugerðar er skilgreindur [handvirkt](er-fillable-excel.md#manual-entry) til að nota sniðmát til að mynda skjal á útleið, þarf að bæta handvirkt við einingunni **Excel\\skrá**, bæta við nauðsynlegu sniðmáti sem viðhengi breytanlegs hlutar og velja það viðhengi í viðbættri einingu **Excel\\Skrá**. Á þennan hátt er gefið til kynna að viðbætt eining muni fylla út valið sniðmát við keyrslu. Þegar útgáfa sniðshlutar er skilgreind í **Drög** [stöðunni](general-electronic-reporting.md#component-versioning), gætir þú viljað bæta nokkrum sniðmátum við breytanlegan hlut og velja síðan hvert sniðmát í einingunni **Excel\\Skrá** til að keyra rafrænt skýrslugerðarsnið. Á þennan hátt er hægt að sjá hvernig mismunandi sniðmát eru fyllt út við keyrslu. Ef þú ert með sniðmát sem ekki eru valin í neinni einingu **Excel\\Skrá**, sendir sniðshönnuður rafrænnar skýrslugerðar viðvörun um að þessum sniðmátum verði eytt úr útgáfu breytanlegs sniðshlutar rafrænnar skýrslugerðar þegar stöðunni er breytt úr **Drög** í **Lokið**.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Hefjið skilgreiningu sniðshlutar rafrænnar skýrslugerðar.
2. Í tré sniðsskipulagsins skal bæta við einingunni **Excel\\Skrá**.
3. Fyrir eininguna **Excel\\skrá** sem var bætt við skal bæta við skrá Excel-vinnubókar, **A.xlsx** sem viðhengi. Notið gerð skjals sem er skilgreint í [Færibreytur rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) til að tilgreina geymslu sniðmáta rafrænna skýrslugerðarsniða.
4. Fyrir eininguna **Excel\\skrá** skal bæta við annarri skrá Excel-vinnubókar, **B.xlsx**, sem viðhengi. Notið sömu skjalagerðina og var notuð fyrir vinnubókarskrá A.
5. Í einingunni **Excel\\skrá** skal velja vinnubókarskrá A.
6. Veljið **Villuleita** til að skoða breytanlegan sniðshlut á síðunni **Sniðshönnuður**.

    ![Villuleita breytanlegan sniðshlut vinnubókarskrá á sniðshönnunarsíðunni](./media/er-components-inspections-12a.gif)

7. Takið eftir að viðvörun vegna villuleitar á sér stað. Skilaboðin gefa til kynna að vinnubókarskráin **B.xlsx** sé ekki tengd við neina íhluti og að hún verði fjarlægð þegar búið er að breyta stöðunni á útgáfu skilgreiningarinnar.

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Enginn valkostur til að lagfæra vandamálið sjálfkrafa er tiltækur.

### <a name="manual-resolution"></a>Handvirk lausn

Breytið skilgreindu sniði með því að fjarlægja öll sniðmát sem ekki eru tengd við neina einingu **Excel\\skrá**.

## <a name="not-synced-format"></a><a id="i13"></a>Ekki samstillt snið

Þegar sniðshlutur rafrænnar skýrslugerðar er [skilgreindur](er-fillable-excel.md) til að nota Excel-sniðmát til að mynda skjal á útleið, er hægt að bæta handvirkt við einingunni **Excel\\skrá**, bæta við nauðsynlegu sniðmáti sem viðhengi breytanlegs hlutar og velja það viðhengi í viðbættri einingu **Excel\\Skrá**. Á þennan hátt er gefið til kynna að viðbætt eining muni fylla út valið sniðmát við keyrslu. Vegna þess að Excel-sniðmátinu sem bætt var við var hannað annars staðar gæti breytanlegt rafrænt skýrslugerðarsnið innihaldið Excel-heiti sem vantar í sniðsmátinu sem bætt var við. Sniðshönnuður rafrænnar skýrslugerðar varar við ósamræmi milli eiginleika sniðseininga rafrænnar skýrslugerðar sem vísa í heiti sem ekki eru höfð með í Excel-sniðmátinu sem bætt var við.

Eftirfarandi skref sýna hvernig þetta vandamál kann að koma upp

1. Hefjið skilgreiningu sniðshlutar rafrænnar skýrslugerðar.
2. Í tré sniðsskipulagsins skal bæta við einingunni **Excel\\Skrá** **Skýrsla**.
3. Fyrir eininguna **Excel\\skrá** sem var bætt við skal bæta við skrá Excel-vinnubókar, **A.xlsx** sem viðhengi. Notið gerð skjals sem er skilgreint í [Færibreytur rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) til að tilgreina geymslu sniðmáta rafrænna skýrslugerðarsniða.

    > [!IMPORTANT]
    > Ganga skal úr skugga um að viðbætt Excel-vinnubók innihaldi ekki heitið **ReportTitle**.

4. Bætið eftirfarandi einingu **Excel\\hólf** **Titill** sem faldaða einingu einingarinnar **Skýrsla**. Í reitinn **Excel-afmörkun** skal slá inn **ReportTitle**.
5. Veljið **Villuleita** til að skoða breytanlegan sniðshlut á síðunni **Sniðshönnuður**.

    ![Villuleita faldaðar einingar og reiti á sniðshönnunarsíðunni](./media/er-components-inspections-13a.png)

6. Takið eftir að viðvörun vegna villuleitar á sér stað. Skilaboðin gefa til kynna að heitið **ReportTitle** sé ekki til í vinnublaði **Sheet1** í Excel-sniðmátinu sem verið er að nota.

    ![Viðvörun villuleitar um að heitið ReportTitle sé ekki til í Sheet1 í Excel-sniðmáti](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Sjálfvirk lausn

Enginn valkostur til að lagfæra vandamálið sjálfkrafa er tiltækur.

### <a name="manual-resolution"></a>Handvirk lausn

#### <a name="option-1"></a>Valkostur 1

Breytið skilgreindu sniði með því að fjarlægja allar einingar sem vísa í Excel-heitin sem vantar í sniðmátið.

#### <a name="option-2"></a>Valkostur 2

[Uppfærið](er-fillable-excel.md#template-import) breytanleg snið rafrænnar skýrslugerðar með því að flytja inn Excel-sniðmát. Skipulag á breytanlegu sniði rafrænnar skýrslugerðar verður [samstillt](modify-electronic-reporting-format-reapply-excel-template.md) við skipulag á innfluttu Excel-sniðmáti.

### <a name="additional-consideration"></a>Fleira sem þarf að hafa í huga

Til að fá upplýsingar um hvernig hægt er að samstilla sniðsskipulagið við sniðmát rafrænnar skýrslugerðar í sniðmátsritli [Viðskiptaskjalastjórnunar](er-business-document-management.md) skal skoða [Uppfæra skipan sniðmáts viðskiptaskjals](er-bdm-update-structure.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[ALLITEMS ER-aðgerð](er-functions-list-allitems.md)

[ALLITEMSQUERY ER-aðgerð](er-functions-list-allitemsquery.md)

[INT64VALUE ER aðgerð](er-functions-conversion-int64value.md)

[INTVALUE ER aðgerð](er-functions-conversion-intvalue.md)

[FILTER ER-aðgerð](er-functions-list-filter.md)

[WHERE ER-aðgerð](er-functions-list-where.md)

[Nota JOIN-gagnagjafa til að sækja gögn úr mörgum forritstöflum í vörpun rafrænna skýrslugerðarlíkana](er-join-data-sources.md)

[Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md)

[Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]