---
title: Aldursskýrsla viðskiptavinar
description: Aldursgreiningarskýrsla viðskiptavinar sýnir stöðu sem er á gjalddaga hjá viðskiptavinum, raðað eftir dagsetningabili eða aldursgreiningartímabili.
author: JodiChristiansen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33bee60a3807c92cc97f0f5e6d660a67cdd7f297
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595090"
---
# <a name="customer-aging-report"></a>Aldursskýrsla viðskiptavinar 

Skýrslan **Aldursgreining viðskiptavinar** sýnir stöðu sem er á gjalddaga hjá viðskiptavinum, raðað eftir dagsetningabili eða aldursgreiningartímabili.

Þegar þessi skýrsla er búin til eru eftirfarandi sjálfgefnar færibreytur sýndar. Hægt er að nota þessar færibreytur til að sía gögnin sem verða sýnd í skýrslunni. Frekari upplýsingar er að finna í [Setja upp innheimtu](set-up-collections.md).

<table>
<colgroup>
<col>
<col>
</colgroup>
<thead>
<tr class="header">
<th><p>Svæði</p></th>
<th><p>lýsing</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Reikningsflokkun</strong></p></td>
<td><p>Veljið eina eða fleiri reikningsflokkanir til að hafa með í skýrslunni.</p>
<div class="alert">

**Athugið:** Þessi stýring er einungis í boði ef skilgreiningarlykillinn <STRONG>Hið opinbera</STRONG> er valinn.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Hafa með færslur án reikningsflokkunar</strong></p></td>
<td><p>Ef þessi gátreitur er valinn verða allar færslur sem eru ekki með úthlutaða reikningsflokkun birtar í þessari skýrslu.</p>
<div class="alert">

**Athugið:** Þessi stýring er einungis í boði ef skilgreiningarlykillinn <STRONG>Hið opinbera</STRONG> er valinn.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Aldursgreining frá og með</strong></p></td>
<td><p>Sláið inn dagsetninguna sem er notuð í núgildandi aldursgreiningarramma.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Staða þann</strong></p></td>
<td><p>Færið inn dagsetningu til að skoða stöðu viðskiptavinar. Þetta er einnig þekkt sem lokadagsetning fyrir færslur.</p></td>
</tr>
<tr class="even">
<td><p><strong>Upphafsdagsetning</strong></p></td>
<td><p>Færið inn dagsetningu sem er á fyrsta tímabilinu eða aldursgreiningartímabilinu sem á að hafa með í skýrslunni.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Skilyrði</strong></p></td>
<td><p>Velja dagsetningartegundina sem skýrslan á að byggjast á.</p>
<ul>
<li><p><strong>Færsludagsetning</strong> – Bókunardagsetning færslunnar. Til dæmis gæti þetta verið reikningsdagsetning sem er grunnurinn að útreikningi á gjalddaga.</p></li>
<li><p><strong>Gjalddagi</strong> – Gjalddagi færslunnar samkvæmt greiðsluskilmála.</p></li>
<li><p><strong>Dagsetning skjals</strong> – Notandaskilgreind dagsetning skjals sem er grundvöllur fyrir útreikning gjalddaga.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Skilgreining aldurstímabils</strong></p></td>
<td><p>Velja skal skilgreiningu aldurstímabils Reiturinn <strong>Tímabil</strong> er ekki notað ef valin er skilgreining aldurstímabils.</p>
<p>Skilgreiningar aldurstímabils sem eru með fleiri en sex aldurstímabil er ekki hægt að nota í prentuðu skýrslunni.</p>
<div class="alert">

**Athugið:** Hægt er að setja upp aldursgreiningartímabil á síðunni <STRONG>Skilgreiningar aldurstímabila</STRONG>.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Prenta lýsingu á aldurstímabili</strong></p></td>
<td><p>Veljið <strong>Já</strong> til að taka með lýsingar á aldurstímabilum efst í hverjum dálki aldurstímabils í skýrslunni. Veljið <strong>Nei</strong> til að prenta skýrsluna án dálkhausa.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bil</strong></p></td>
<td><p>Skilgreinið tímabilið sem á að nota með því að færa inn númer dags- eða mánaðareininganna á hverju tímabili. Til dæmis til að skoða aldursupplýsingar eftir viku skal færa inn 7 í þennan reit og velja <strong>Dagur</strong> í reitnum <strong>Dagur/Mán</strong>.</p>
<div class="alert">

**Athugaðu:** Upplýsingarnar sem eru færðar inn í þetta svæði eru eingöngu notaðar ef aldursgreiningarrammi hefur ekki verið valinn. Annars er prentstefnan skilgreind í skilgreiningu aldurstímabils.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Dagur/Mán.</strong></p></td>
<td><p>Veljið eininguna, annaðhvort <strong>Dagur</strong> eða <strong>Mánuður</strong>, sem er notuð til að skilgreina tímabilið í reitnum <strong>Tímabil</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Stefna prentunar</strong></p></td>
<td><p>Veljið hvort eigi að reikna út stöðu og prenta aldursgreiningarskýrslur fyrir gömul tímabil eða komandi tímabil. Dagsetningarnar eru metnar miðað við dagsetninguna sem valin er í reitnum <strong>Staða þann</strong>. Veljið <strong>Afturábak</strong> til að sýna upplýsingar um liðin tímabil. Veljið <strong>Áfram</strong> til að sýna upplýsingar um tímabil í framtíðinni.</p>
<div class="alert">
  
<STRONG>Athugaðu:</STRONG> Upplýsingarnar sem eru færðar inn í þetta svæði eru eingöngu notaðar ef aldursgreiningarrammi hefur ekki verið valinn.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Upplýsingar</strong></p></td>
<td><p>Veljið til að skrá færslurnar sem teknar eru með í stöðunum sem eru sýndar í þessari skýrslu.</p></td>
</tr>
<tr class="even">
<td><p><strong>Taka með upphæðir í færslugjaldmiðli</strong></p></td>
<td><p>Veljið til að taka með upphæð í færslugjaldmiðlinum til viðbótar við upphæð í bókhaldsgjaldmiðlinum. Ef þessi gátreitur er ekki valinn eru upphæðir í þessari skýrslu aðeins birtar í bókhaldsgjaldmiðlinum.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Neikvæð staða</strong></p></td>
<td><p>Veljið til að hafa með viðskiptavinalykla sem eru með neikvæðar stöður.</p></td>
</tr>
<tr class="even">
<td><p><strong>Undanskilja efnahagslykla sem standa á núlli</strong></p></td>
<td><p>Veljið til að útiloka viðskiptavinalykla sem eru með núllstöðu.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Greiðslustaða</strong></p></td>
<td><p>Velja til að birta greiðslur sem hafa ekki verið jafnaðar. Þær eru birtar í fyrsta dálki skýrslunnar.</p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]