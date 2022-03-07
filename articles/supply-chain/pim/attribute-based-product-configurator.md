---
title: Söluverð sem byggir á eigind fyrir afurðarafbrigði með skorðum
description: Þetta efnisatriði lýsir því hvernig á að búa til söluverðlíkan með söluverðum sem byggja á íhlutum og eigindum frekar en á efnislegri uppskriftinni og leiðinni.
author: t-benebo
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e50b2d1e9ccf03a58e0ddf6d4ecfb34c6c504161
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577457"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a>Söluverð sem byggir á eigind fyrir afurðarafbrigði með skorðum

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að búa til söluverðlíkan með söluverðum sem byggja á íhlutum og eigindum frekar en á efnislegri uppskriftinni og leiðinni. Hægt er að búa til mörg söluverðlíkön fyrir hvert afbrigðalíkan afurðar.

## <a name="set-relevant-product-information-management-parameters"></a>Stilla viðeigandi færibreytur afurðarupplýsingastjórnunar

Áður en hafist er handa við að smíða verðlíkön verður að skilgreina sjálfgefinn gjaldmiðil, sem er notaður þegar söluverðlíkönin eru smíðuð. Einnig er hægt að velja hvort hengja eigi Microsoft Excel-skrá við með sundurliðun á verði fyrir allar pöntunar- eða tilboðslínur. Sundurliðun verðs gerir þér kleift að miðla upplýsingum með viðskiptavinum um hvernig þú komst niður á tiltekið söluverð fyrir skilgreinda afurð.

Sjálfgefinn gjaldmiðill valinn:

1. Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Færibreytur afurðaupplýsingastjórnunar**.
1. Opnið flipann **Líkön afurðarafbrigða sem byggja á skorðum**.
1. Opnið fellilistann **Sjálfgefinn gjaldmiðill** og veljið gjaldmiðilinn.

    ![Veljið sjálfgefinn gjaldmiðil fyrir afurðarafbrigði sem byggir á skorðum.](media/prod-config-currency.png "Stilla sjálfgefinn gjaldmiðil fyrir afurðarafbrigði sem byggir á skorðum")

1. Ef á að hengja við Excel-skrá með sundurliðun á verði fyrir allar pöntunar- og tilboðslínur, skal í hlutanum **Verðlíkan** stilla **Hengja við** á *Já*.

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a>Smíða söluverðlíkön

Söluverðlíkan smíðað:

1. Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.
1. Veljið afbrigðalíkan afurðar sem við á.
1. Á aðgerðasvæðinu skal opna flipann **Líkan** og í flokknum **Setja upp** skal velja **Verðlíkön**.
1. Síðan **Verðlíkön** opnast.
1. Veljið verðlíkan eða bætið nýju við hnitanetið.
1. Veljið **Breyta** til að opna breytingarsíðuna fyrir valið líkan, sem býður upp á eftirfarandi eiginleika:
    - Haus skjámyndarinnar sýnir sjálfgefinn gjaldmiðil og gerir kleift að bæta nýjum gjaldmiðlum við verðuppsetninguna.
    - Vinstri glugginn sýnir alla íhluti og þarfir notanda fyrir afurðarlíkanið. Hver hnútur í líkanatré afurðar getur verið með eina segð grunnverðs og valfrjálsan fjölda af segðarreglum. Regla segðar felur í sér skilyrði og segð og hver segðarregla nær yfir valkost afurðar sem hjálpar til við að stýra verði afurðarinnar.
    - Þegar skilyrði og segðir eru búnar til eru sömu virknitáknin tiltæk fyrir útreikninga í afurðarlíkani. Segðaritillinn styður einnig bæði skilyrði og segðir.
1. Velja skal hnút í vinstri dálknum og nota síðan eiginleikana sem lýst er í skrefinu á undan til að koma á fót verðlagningarreglum (sjá einnig dæmið sem gefið er upp eftir þetta ferli). Endurtakið þetta skref fyrir hvern hnút eftir því sem þörf krefur.

Eftirfarandi dæmi sýnir grunnverð á fastri tölu sem nemur 899,95 EUR, sem hægt er að breyta með einni eða fleiri eftirfarandi fimm segðarreglum, eftir því hvaða afbrigði er valið af viðskiptavininum:

- Fyrir hvíta áferð á skáp skal draga frá 59,95 EUR.
- Fyrir hornhlífar skal bæta við 35,95 EUR.
- Fyrir framhlið úr málmi skal bæta við 89,95 EUR.
- Fyrir rósaviðaráferð á skáp skal bæta við 119,95 EUR.
- Bætið við 12,95 EUR fyrir hverja einingu af hæð hátalara.

![Dæmi um verðlíkan.](media/prod-config-rules-example.png "Dæmi um verðlíkan")

## <a name="add-support-for-multiple-currencies"></a>Bæta við stuðningi fyrir marga gjaldmiðla

Þegar stillanleg afurð er seld athugar kerfið hvort verðin hafa verið sett með skýrum hætti í gjaldmiðli viðskiptavinarins. Ef svo er eru þessi gildi notuð. Ef ekki, notar kerfið gengi gjaldmiðla sem notað er fyrir sölufyrirtækið til að umbreyta sjálfgefnu gildi gjaldmiðils í gjaldmiðil viðskiptavinar.

Sérstöku verði bætt við viðbótargjaldmiðil:

1. Opnið breytingarsíðuna fyrir verðlíkanið eins og lýst er í [Smíða söluverðlíkön](#build-price-model).
1. Veljið hnappinn **Bæta við** í haus verðlíkansins til að opna felligluggann **Gjaldmiðlar**, sem sýnir tiltæka gjaldmiðla.
1. Veljið gjaldmiðil sem bæta á við í felliglugganum **Gjaldmiðlar** og veljið síðan **Í lagi**.
1. Fellilistinn **Núgildandi gjaldmiðill** inniheldur núna gjaldmiðilinn sem þú bættir við, ásamt öllum öðrum gjaldmiðlum sem kunna að hafa verið bætt við áður. Veljið nýja gjaldmiðilinn og takið eftir að hnitanetið í hlutanum **Segðarreglur** innihalda núna tvo segðarreiti:
    - **Segð** - Sýnir segðina (eða fast gildi) til að finna verðið með því að nota gjaldmiðil sem valinn er fyrir **Núgildandi gjaldmiðill**.
    - **Sjálfgefnar segðir** - Sýnir segðina (eða fast gildi) til að finna verðið með því að nota sjálfgefna gildið sem valið er (er sýnt í reitnum **Sjálfgefinn gjaldmiðill**).

    > [!NOTE]
    > Reiturinn **Skilyrði** fyrri segðarreglurnar er í „eigu“ sjálfgefins gjaldmiðils, sem þýðir að ekki er hægt að breyta skilyrðinu fyrir aðra gjaldmiðla. Einnig er ekki hægt að bæta við nýjum segðarreglum á meðan gjaldmiðill annar en sjálfgefni gjaldmiðillinn er valinn sem **Núgildandi gjaldmiðill**.
1. Breytið gildunum í dálknum **Segð** eins og þörf er á fyrir núgildandi gjaldmiðil.

Í dæminu hér að neðan er _EUR_ sjálfgefni gjaldmiðillinn og _USD_ hefur verið bætt við sem viðbótargjaldmiðill.

![Dæmi um líkan með mörgum gjaldmiðlum.](media/prod-config-rules-currency-example.png "Dæmi um líkan með mörgum gjaldmiðlum")

> [!NOTE]
> Ekki er hægt að bæta við segðarreglum sem eru einkvæmar fyrir gjaldmiðil sem ekki er sjálfgefinn. Til að stofna segðarreglur sem ættu aðeins að eiga við um gjaldmiðil annan en sjálfgefna gjaldmiðilinn, skal setja verð segðar fyrir sjálfgefna gjaldmiðilinn á núll. Setjið síðan á viðeigandi segð fyrir gjaldmiðilinn sem ekki er sjálfgefinn.

## <a name="test-your-price-model"></a>Verðlíkanið prófað

Til að prófa hvernig söluverðin virka í skilgreiningarlotu skal opna breytingarsíðuna fyrir verðlíkanið eins og lýst er í [Söluverðslíkön smíðuð](#build-price-model) og velja síðan **Prófa** á aðgerðasvæðinu. Svarglugginn **Prófa afurðarlíkan** opnast, þar sem hægt er að gera eftirfarandi:

- Notið skilgreiningarstillingarnar sem boðið er upp á hér til að velja valkosti afurðar og skoðið svo áhrifin sem þeir hafa á gildið sem sýnt fyrir **Verð og sendingardagsetning**.
- Veljið **Skoða verðsundurliðun** til að hlaða niður Excel-skjali sem sýnir ítarlegar upplýsingar um hvernig verðið var reiknað út.

![Vörulíkanið prófað.](media/prod-config-test.png "Vörulíkanið prófað")

Sóttur töflureiknir sýnir bæði heildargildið og framlagið sem prósentu fyrir hverja virka verðeiningu. Ef búið er að stilla valkostinn **Hengja við** fyrir verðlíkanið á síðunni **Færibreytur vöruupplýsingastjórnunar**, verður þetta Excel-skjal hengt við pöntunina eða tilboðslínuna.

![Excel-töflureiknir sem sýnir sundurliðun verðs.](media/prod-config-excel-example.png "Excel-töflureiknir sem sýnir sundurliðun verðs")

## <a name="set-up-selection-criteria-for-price-models"></a>Setja upp valskilyrði fyrir verðlíkön

Þegar verðlíkönin eru tilbúin þarf að setja inn að minnsta kosti eitt valskilyrði til að taka upp verðlíkanið þegar skilgreint er fyrir tilboð eða pöntun. Þetta er gert með því að setja upp eina eða fleiri fyrirspurnir. Í samsetningu við samsvarandi söluverðlíkön, bjóða líkönin upp á mikinn sveigjanleika í viðeigandi söluverðum fyrir ákveðna viðskiptavini, svæði, tímabil og önnur skilyrði.

Valskilyrði fyrir verðlíkön sett upp:

1. Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.
1. Veljið afbrigðalíkan afurðar sem við á.
1. Á aðgerðasvæðinu skal opna flipann **Líkan** og í flokknum **Setja upp** skal velja **Skilyrði verðlíkans**. Síðan **Skilyrði verðlíkans** opnast.
1. Ef fyrirspurnarlínan sem þú þarft er ekki enn til staðar skaltu velja **Ný** á aðgerðasvæðinu til að bæta nýrri línu við hnitanetið og gera eftirfarandi stillingar fyrir það:
    - **Heiti** - Færið inn heiti fyrir þessa línu.
    - **Lýsing** - Lýsið stuttlega fyrirspurninni og tilgangi hennar.
    - **Verðlíkanið** - Veljið [verðlíkan](#build-price-model) (úr núverandi skilgreiningarlíkani) sem fyrirspurnin gildir um þegar hún er ræst.
    - **Gerð pöntunar** - Veljið gerð pöntunar sem fyrirspurnin gildir um.
    - **Gildir frá** - Tilgreinið fyrsta daginn þegar fyrirspurnin tekur gildi.
    - **Gildir til** - Tilgreinið síðasta daginn sem fyrirspurnin gildir.

    ![Skilyrði verðlíkans.](media/prod-config-price-model-criteria.png "Skilyrði verðlíkans")

1. Veljið línuna fyrir fyrirspurnina sem á að skilgreina og veljið síðan **Breyta** á **Aðgerðarsvæðinu**. Svargluggi fyrirspurnarhönnuðar opnast. Hann virkar eins og flestir fyrirspurnarhönnuðir í Supply Chain Management. Notið hann til að skilgreina skilyrðin þar sem verðlíkanið fyrir línuna sem var valin á að gilda um.

1. Endurtakið skref 4-5 fyrir hverja fyrirspurn eins og nauðsynlegt er.
    > [!TIP]
    > Hægt er að spara tíma með því að afrita fyrirliggjandi línu sem er svipar til nýrrar línu sem þarf að bæta við. Til að gera þetta skal velja marklínu og síðan velja **Afrita** á aðgerðasvæðinu.

1. Þegar búið er að setja upp skilyrðin skal raða þeim upp í rétta röð í listanum **Skilyrði verðlíkans**. Til að færa til línu skal velja línuna og síðan velja **Upp** eða **Niður** á aðgerðasvæðinu.

    > [!IMPORTANT]
    > Á skilgreiningartíma byrjar kerfið að leita efst í listanum og notar fyrstu fyrirspurnina sem samsvarar gögnunum í tilboðs- eða pöntunarlínunni. Þess vegna þarf að setja ítarlegustu fyrirspurnirnar efst. Ef almenn fyrirspurn er sett efst í listann, verður hún notuð jafnvel þótt að kunni að vera fyrirspurn neðar í listanum sem passar ákveðnum viðskiptavini eða viðfangi skilgreiningarinnar.

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a>Stilla söluverð sem byggir á eigind fyrir útgáfu afurðarlíkans

Lokaskrefið er að tilgreina söluverð sem byggir á eigind fyrir útgáfu afurðarlíkans. Til að gera þetta:

1. Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.
1. Veljið afbrigðalíkan afurðar sem við á.
1. Á aðgerðasvæðinu skal opna flipann **Líkan** og í flokknum **Upplýsingar um vörulíkan** skal velja **Útgáfur**.
1. Síðan **Útgáfur** opnast. Gangið úr skugga um að **Verðlagningaraðferð** sé stillt á **Byggir á eigind**.
    ![Stilla aðferð verðlagningar svo hún byggi á eigind.](media/prod-config-versions.png "Stilla aðferð verðlagningar svo hún byggi á eigind")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]