---
title: Gæðatengingar
description: Þetta efnisatriði lýsir því hvernig er hægt að nota gæðatengingar í Microsoft Dynamics 365 Supply Chain Management til að búa til gæðapantanir sjálfkrafa sem tengjast sölum þínum, innkaupum og framleiðsluferlum.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28984730e5660414eec1ba087eb5de1eba4cbbb8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571930"
---
# <a name="quality-associations"></a>Gæðatengingar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig er hægt að nota gæðatengingar í Microsoft Dynamics 365 Supply Chain Management til að búa til gæðapantanir sjálfkrafa sem tengjast sölum þínum, innkaupum og framleiðsluferlum.

Gæðatenging skilgreinir allar eftirfarandi upplýsingar fyrir gæðapöntun sem er mynduð:

- Færslutilvikið
- Safn prófana sem þarf að framkvæma á vörum
- Viðunandi gæðastigi (AQL)
- Úrtaksáætlunin

Gæðatengingu verður að skilgreina fyrir hvert afbrigði viðskiptaferlis sem krefst sjálfvirkrar myndunar gæðapöntunar. Til dæmis er hægt að mynda gæðapöntun í viðskiptaferlum fyrir innkaupapantanir, biðgeymslupantanir, sölupantanir eða framleiðslupantanir.

## <a name="working-with-quality-associations"></a>Vinna með gæðatengingar

Viðskiptaferli sem notar gæðatengingu getur verið tengt mismunandi upprunaskjölum, eins og innkaupapöntunum, sölupöntunum eða framleiðslupöntunum.

Hver gæðatengingafærsla skilgreinir einnig prófanir, viðunandi gæðastig og úrtaksáætlun sem eiga við myndaðar gæðapantanir. Skilgreina verður gæðatengingafærslu fyrir hvert afbrigði viðskiptaferlis. Til dæmis er hægt að setja upp gæðatengingu sem myndar gæðapöntun þegar innhreyfingarskjal afurða innkaupapöntun er uppfært. Það fer eftir uppsetningu á keyrsluáætlun hvort hægt sé að stöðva kveikjuferlið sjálft á meðan gæðapöntun er opin. Einnig er hægt að loka á síðari ferli, t.d. innkaupapantanir og reikninga.

> [!NOTE]
> Meðan gæðapantanir eru opnar er birgðamagn sjálfkrafa stöðvað til útgáfu. Það fer eftir **Alger stöðvun** stillingunni á síðunni **Vörusýnishorn** hvort magn sé annaðhvort magn í gæðapöntun eða magn í upprunaskjalslínu. Frekari upplýsingar er að finna í [Vörusýnataka gæðastjórnunar](quality-item-sampling.md).

Fyrir tiltekið viðskiptaferli auðkennir gæðatengingarfærslan tilvik og skilyrði sem mynda skal gæðapöntun fyrir. Skilyrðin geta átt sérstaklega við svæði eða lögaðila. Aðeins er hægt að mynda gæðapöntun sem felur í sér eyðileggingarprófun þegar lagerbirgðir eru til staðar fyrir tilvikið.

Til að vinna með gæðatengingar skal fara í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðatengingar**. Eftirfarandi dæmi sýna hvernig gæðatengingafærsla er skilgreind fyrir afbrigði hvers viðskiptaferlis. Í eftirfarandi töflu eru dæmin tekin saman eftir tilviki og skilyrðum sem skilgreind eru af gæðatengingarfærslu.

<table>
<thead>
<tr>
<th>Gerð tilvísunar</th>
<th>Gerð tilviks</th>
<th>Framkvæmd</th>
<th>Lokun tilviks</th>
<th>Tilvísun skjals</th>
</tr>
</thead>
<tbody>
<tr>
<td>Birgðir</td>
<td>Ekki tiltækt</td>
<td>Ekki tiltækt</td>
<td>Ekkert</td>
<td>Allt</td>
</tr>
<tr>
<td rowspan="7">Sala</td>
<td rowspan="4">Tiltektarferli er áætlað</td>
<td rowspan="4">Fyrir</td>
<td>Ekkert</td>
<td rowspan="22">Tilgreint kenni, Flokkur eða Allir aðeins</td>
</tr>
<tr>
<td>Tiltektarferli</td>
</tr>
<tr>
<td>Fylgiseðill</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="3">Fylgiseðill</td>
<td rowspan="3">Fyrir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Fylgiseðill</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="15">Innkaup</td>
<td rowspan="7">Innhreyfingaskjal</td>
<td rowspan="4">Fyrir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Innhreyfingaskjal</td>
</tr>
<tr>
<td>Innhreyfingarskjal afurðar</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="3">Eftir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Innhreyfingarskjal afurðar</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="3">Skráning</td>
<td rowspan="3">Ekki tiltækt</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Innhreyfingarskjal afurðar</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="5">Innhreyfingarskjal afurðar</td>
<td rowspan="3">Fyrir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Innhreyfingarskjal afurðar</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="2">Eftir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="8">Framleiðsla</td>
<td rowspan="3">Skráning</td>
<td rowspan="3">Ekki tiltækt</td>
<td>Ekkert</td>
<td rowspan="12">Allt</td>
</tr>
<tr>
<td>Bóka tilbúið</td>
</tr>
<tr>
<td>Við skil</td>
</tr>
<tr>
<td rowspan="5">Bóka tilbúið</td>
<td rowspan="3">Fyrir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Bóka tilbúið</td>
</tr>
<tr>
<td>Við skil</td>
</tr>
<tr>
<td rowspan="2">Eftir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Við skil</td>
</tr>
<tr>
<td rowspan="4">Biðgeymsla</td>
<td rowspan="3">Bóka tilbúið</td>
<td rowspan="2">Fyrir</td>
<td>Bóka tilbúið</td>
</tr>
<tr>
<td>Við skil</td>
</tr>
<tr>
<td>Eftir</td>
<td>Við skil</td>
</tr>
<tr>
<td>Við skil</td>
<td>Fyrir</td>
<td>Við skil</td>
</tr>
<tr>
<td rowspan="3">Leiðaraðgerð</td>
<td rowspan="3">Bóka tilbúið</td>
<td rowspan="2">Fyrir</td>
<td>Engum</td>
<td rowspan="3">Tiltekið kenni, flokkur eða allt og tiltekið tilfang, flokkur eða allt</td>
</tr>
<tr>
<td>Bóka tilbúið</td>
</tr>
<tr>
<td>Eftir</td>
<td>Engum</td>
</tr>
<tr>
<td rowspan="3">Framleiðsla aukaafurðar</td>
<td>Skráning</td>
<td>Ekki tiltækt</td>
<td rowspan="3">Engum</td>
<td rowspan="3">Allir</td>
</tr>
<tr>
<td rowspan="2">Bóka tilbúið</td>
<td>Fyrir</td>
</tr>
<tr>
<td>Eftir</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Eiginleikinn *Gæðastjórnun fyrir vöruhúsaferli* bætir við möguleikum fyrir úrvinnslu gæðapantana fyrir framleiðslu þar sem **Gerð tilviks** er stillt á *Tilkynna sem lokið* og reiturinn **Framkvæmd** er stilltur á *Eftir á* og fyrir innkaup þar sem reiturinn **Gerð tilviks** er stilltur á *Skráning*. Frekari upplýsingar er að finna í [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md).

Eftirfarandi tafla veitir frekari upplýsingar um hvernig hægt er að mynda gæðapantanir fyrir tilgreindar gerðir ferla.

<div class="tableSection">
<table>
<thead>
<tr>
<th>Gerð ferlis</th>
<th>Þegar hægt er að mynda gæðapantanir sjálfvirkt</th>
<th>Þegar hægt er að mynda gæðapantanir ef eyðileggingarprófun er áskilin</th>
<th>Upplýsingar um skilyrði</th>
<th>Upplýsingar um handvirka myndun</th>
</tr>
</thead>
<tbody>
<tr>
<td>Innkaupapöntun</td>
<td>Á undan eða eftir komulista eða innhreyfingarskjal afurða fyrir efni sem er móttekið er bókuð</td>
<td>Eftir innhreyfingarskjal afurða fyrir efni sem er móttekið er bókað, þar sem efnið verður að vera tiltækt fyrir eyðileggingarprófun</td>
<td>Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</td>
<td>Gæðapöntun sem er stofnuð handvirkt og vísar í innkaupapöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</td>
</tr>
<tr>
<td>Biðgeymslupöntun</td>
<td>Á undan eða eftir biðgeymslupöntunin er skráð sem lokið eða lokið</td>
<td>Ekki er hægt að mynda gæðapantanir sem krefjast eyðileggingarprófana. Gert er ráð fyrir að virkni biðgeymslupöntunar annist ráðstöfun á efni sem er eyðilagt.</td>
<td>Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</td>
<td>Gæðapöntun sem er stofnuð handvirkt og vísar í biðgeymslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</td>
</tr>
<tr>
<td>Sölupöntun</td>
<td>Á undan á áætluðu tiltektarferli eða fylgiseðilsuppfærslu fyrir vörur sem verið er að senda</td>
<td>Á hvaða þrepi sem er</td>
<td>Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða viðskiptavinar eða samsetningu þessara skilyrða.</td>
<td>Gæðapöntun sem er stofnuð handvirkt og vísar í sölupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</td>
</tr>
<tr>
<td>Framleiðslupöntun</td>
<td>Á undan eða eftir að tilbúið magn fyrir framleiðslupöntun er skráð</td>
<td>Eftir að tilbúið magn fyrir framleiðslupöntun er skráð</td>
<td>Þörf á gæðapöntun getur verið vegna tiltekins svæðis eða vöru eða samsetningu þessara skilyrða.</td>
<td>Gæðapöntun sem er stofnuð handvirkt og vísar í framleiðslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</td>
</tr>
<tr>
<td>Framleiðslupöntun sem er með leiðaraðgerð</td>
<td>Á undan eða eftir að skýrslu er lokið fyrir aðgerð</td>
<td>Á undan eða eftir að skýrsluframleiðslu er lokið fyrir síðustu aðgerð</td>
<td>Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða rekstrartilfanga eða samsetningu þessara skilyrða.</td>
<td>Gæðapöntun sem er stofnuð handvirkt og vísar í leiðaraðgerð getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</td>
</tr>
<tr>
<td>Birgðir</td>
<td>Ekki er hægt að mynda gæðapöntun sjálfkrafa fyrir færslu í birgðabók eða fyrir flutningspantanafærslur.</td>
<td></td>
<td></td>
<td>Stofna verður gæðapöntun handvirkt fyrir birgðamagn vöru. Efnislegra lagerbirgða er krafist.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Dæmi um sjálfvirka myndun þjónustupantana

### <a name="purchasing"></a>Innkaup

Í innkaupum, ef þú stillir reitinn **Gerð tilviks** á *Innhreyfingarskjal afurðar* og reitinn **Framkvæmd** á *Eftir* á síðunni **Gæðatengingar** færðu eftirfarandi niðurstöður:

- Ef valkosturinn **Eftir uppfærðu magni** er stilltur á *Já* myndast gæðapöntun fyrir hverja innhreyfingu gegn innkaupapöntuninni, byggð á mótteknu magni og stillingum í vörusýni. Í hvert skipti sem magn er móttekið gegn innkaupapöntuninni myndast nýjar gæðapantanir miðað við nýlega fengið magn.
- Ef valkosturinn **Eftir uppfærðu magni** er stilltur á *Nei* myndast gæðapöntun fyrir fyrstu innhreyfinguna gegn innkaupapöntuninni, byggð á mótteknu magni. Að auki eru ein eða fleiri gæðapantanir búnar til miðað við eftirstandandi magn, eftir því hverjar rakningarvíddirnar eru. Gæðapantanir eru ekki myndaðar fyrir síðari innhreyfingar gegn innkaupapöntuninni.

### <a name="production"></a>Vinnsla

Í framleiðslu, ef þú stillir reitinn **Gerð tilviks** á *Tilkynna sem lokið* og reitinn **Framkvæmd** á *Eftir* á síðunni **Gæðatengingar** færðu eftirfarandi niðurstöður:

- Ef valkosturinn **Eftir uppfærðu magni** er stilltur á *Já* myndast gæðapöntun fyrir hvert lokið magn og stillingar í vörusýni. Í hvert sinn sem magn er skráð sem lokið gagnvart framleiðslupöntuninni eru nýjar gæðapantanir búnar til út frá nýlega loknu magni. Þessi myndunarrök eru í samræmi við innkaup.
- Ef valkosturinn **Eftir uppfærðu magni** er stilltur á *Nei* myndast gæðapöntun fyrir fyrsta skiptið sem magn er tilkynnt sem lokið, byggt á loknu magni. Að auki eru ein eða fleiri gæðapantanir búnar til miðað við eftirstandandi magn, eftir því hverjar rakningarvíddirnar eru í vörusýninu. Gæðapantanir eru ekki búnar til fyrir seinna lokið magn.

<table>
<thead>
<tr>
<th>Gæðaforskriftir</th>
<th>Uppfært magn á</th>
<th>Á rakningarvídd</th>
<th>Niðurstaða</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prósenta: 10%</td>
<td>Já</td>
<td>
<p>Rununúmer: Nr.</p>
<p>Raðnúmer: Nr.</p>
</td>
<td>
<p>Pöntunarmagn: 100</p>
<ol>
<li>Tilkynna sem lokið fyrir 30
<ul>
<li>Gæðapöntun 1 fyrir 3 (10% af 30)</li>
</ul>
</li>
<li>Tilkynna sem lokið fyrir 70
<ul>
<li>Gæðapöntun 2 fyrir 7 (10% eftirstandandi pöntunarmagn, sem er 70 í þessu tilviki)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fast magn: 1</td>
<td>Nei</td>
<td>
<p>Rununúmer: Nr.</p>
<p>Raðnúmer: Nr.</p>
</td>
<td>Pöntunarmagn: 100
<ol>
<li>Tilkynna sem lokið fyrir 30
<ul>
<li>Gæðapöntun 1 fyrir 1 (fyrir fyrsta tilkynnta sem lokið magn, sem hefur föst gildi 1)</li>
<li>Gæðapöntun 2 fyrir 1 (fyrir eftirstandandi magn, sem er enn með fast gildi 1)</li>
</ul>
</li>
<li>Tilkynna sem lokið fyrir 10
<ul>
<li>Engar gæðapantanir eru búnar til.</li>
</ul>
</li>
<li>Tilkynna sem lokið fyrir 60
<ul>
<li>Engar gæðapantanir eru búnar til.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fast magn: 1</td>
<td>Já</td>
<td>
<p>Rununúmer: Já</p>
<p>Raðnúmer: Já</p>
</td>
<td>
<p>Pöntunarmagn: 10</p>
<ol>
<li>Tilkynna sem lokið fyrir 3: 1 fyrir rununúmer b1, raðnúmer s1; 1 fyrir rununúmer b2, raðnúmer s2; og 1 fyrir rununúmer b3, raðnúmer s3
<ul>
<li>Gæðapöntun 1 fyrir 1 af lotunúmeri b1, raðnúmer s1</li>
<li>Gæðapöntun 2 fyrir 1 lotunúmer b2, raðnúmer s2</li>
<li>Gæðapöntun 3 fyrir 1 lotunúmer b3, raðnúmer s3</li>
</ul>
</li>
<li>Tilkynna sem lokið fyrir 2: 1 fyrir rununúmer b4, raðnúmer s4; og 1 fyrir rununúmer b5, raðnúmer s5
<ul>
<li>Gæðapöntun 4 fyrir 1 lotunúmer b4, raðnúmer s4</li>
<li>Gæðapöntun 5 fyrir 1 lotunúmer b5, raðnúmer s5</li>
</ul>
</li>
</ol>
<p><strong>Ath.:</strong> Hægt er að endurnýta rununa.</p>
</td>
</tr>
<tr>
<td>Fast magn: 2</td>
<td>Nei</td>
<td>
<p>Rununúmer: Já</p>
<p>Raðnúmer: Já</p>
</td>
<td>
<p>Pöntunarmagn: 10</p>
<ol>
<li>Tilkynna sem lokið fyrir 4: 1 fyrir rununúmer b1, raðnúmer s1; 1 fyrir rununúmer b2, raðnúmer s2; 1 fyrir rununúmer b3, raðnúmer s3; og 1 fyrir rununúmer b4, raðnúmer s4
<ul>
<li>Gæðapöntun 1 fyrir 1 af lotunúmeri b1, raðnúmer s1</li>
<li>Gæðapöntun 2 fyrir 1 lotunúmer b2, raðnúmer s2</li>
<li>Gæðapöntun 3 fyrir 1 lotunúmer b3, raðnúmer s3</li>
<li>Gæðapöntun 4 fyrir 1 lotunúmer b4, raðnúmer s4</li>
</ul>
<ul>
<li>Gæðapöntun 5 fyrir 2, án tilvísunar í lotunúmer og raðnúmer</li>
</ul>
</li>
<li>Tilkynna sem lokið fyrir 6: 1 fyrir rununúmer b5, raðnúmer s5; 1 fyrir rununúmer b6, raðnúmer s6; 1 fyrir rununúmer b7, raðnúmer s7; 1 fyrir rununúmer b8, raðnúmer s8; 1 fyrir rununúmer b9, raðnúmer s9; og 1 fyrir rununúmer b10, raðnúmer s10
<ul>
<li>Engar gæðapantanir eru búnar til.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gæðastjórnunarferli](quality-management-processes.md)
- [Virkja stjórnun gæða og ósamkvæmni](enable-quality-management.md)
- [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
