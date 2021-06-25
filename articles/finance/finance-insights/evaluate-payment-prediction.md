---
title: Leggja mat á upprunalega greiðsluspá viðskiptavinarins (forskoðun)
description: Þetta efnisatriði lýsir skrefum sem má taka til að skilja greiðsluspá viðskiptavinar og meta skilvirkni hennar.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 014684595c7cd65383dc12d9eec2dd8ea7b8c20f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186739"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a>Leggja mat á upprunalega greiðsluspá viðskiptavinarins (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hvernig á að meta spálíkan eftir að þú kveikir á Fjármálainnsýn og hefur myndað og þjálfað fyrsta líkanið. Þetta efnisatriði fjallar um líkan til að spá fyrir um greiðslur viðskiptavinar. Efnisatriðið lýsir skrefum sem hægt er að nota til að skilja greiðsluspá viðskiptavinar og meta skilvirkni hennar.

## <a name="getting-details-about-the-model"></a>Sækja frekari upplýsingar um líkanið

Á síðunni **Færibreytur Fjármálainnsýnar** í Microsoft Dynamics 365 Finance, birtist tengillinn **Auka nákvæmni líkans** við hlið nákvæmniseinkunnarinnar.

[![Tengill til að auka nákvæmni líkans](./media/prediction-model.png)](./media/prediction-model.png)

Um leið og smellt er á tengilinn opnast AI Builder, þar sem hægt er að fá frekari upplýsingar um núverandi líkan og frekari skref til að bæta líkanið. Skýringarmyndin hér á eftir sýnir síðuna sem opnast.

[![AI Builder](./media/what-to-predict.png)](./media/what-to-predict.png)

Eftirfarandi upplýsingar birtast á síðunni sem opnast:

- Í hlutanum **Frammistaða** varpar frammistöðueinkunnin ljósi á gæði líkansins. Frekari upplýsingar um þessa Einkunn er að finna í hlutanum [Frammistaða spálíkans](/ai-builder/prediction-performance) í fylgiskjölum AI Builder.
- Hlutinn **Áhrifamestu gögnin** sýnir hversu mikilvægar mismunandi innsláttargerðir gagna voru fyrir líkanið. Hægt er að meta þennan lista og samsvarandi prósentuhlutfall til að ákvarða hvort upplýsingarnar eru í samræmi við þekkingu þína á fyrirtækinu þínu og markaðinum.

    [![Hlutar frammistöðu og áhrifamestu gagna fyrir spálíkanið](./media/models.png)](./media/models.png)

- Í hlutanum **Frammistaða** skal velja **Skoða frekari upplýsingar** til að fá frekari upplýsingar um einkunnina önnur atriði. Frekari upplýsingar á eftirfarandi skýringarmynd sýna að líkanið notar minni upplýsingar en ráðlagt er. Þar af leiðir sendi kerfið frá sér viðvörunarboð.

    [![Viðvaranir um frammistöðu líkansins](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>Nánari skoðun

Nákvæmni er ágætis viðmið til að meta líkan í upphafi og frammistöðueinkunn veitir ágætis yfirsýn en hins vegar býður AI Builder upp á ítarlegri mæligildi til að nota við slíkt mat. Til að hlaða niður frekari upplýsingum í hlutanum **Frammistaða** skal smella á hnappinn úrfellingarhnappinn (**...**) við hliðina á hnappinum **Nota líkan** og síðan velja **Hlaða niður ítarlegri mæligildum**.

[![Skipunin um að hlaða niður ítarlegri mæligildum](./media/performance.png)](./media/performance.png)

Eftirfarandi skýringarmynd sýnir sniðið sem hægt er að hlaða niður gögnunum í.

[![Snið gagna sem hlaðið er niður](./media/data-format.png)](./media/data-format.png)

Þegar greina á niðurstöðurnar frekar er skoðun á „ruglingsfylkinu“ ágætis byrjunarreitur. Hér eru til dæmis gögnin sem eru sýnd fyrir þetta mæligildi í skýringarmyndinni hér á undan.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

Hægt er að víkka þessi gögn á eftirfarandi hátt.

| &nbsp;                   | Spáð í tíma | Spáð seint | Spáð mjög seint |
|--------------------------|-------------------|----------------|---------------------|
| Raunveruleg greiðsla sem barst á tíma   | **71**            | 0              | 21                  |
| Raunveruleg greiðsla sem barst seint      | 5                 | **0**          | 27                  |
| Raunveruleg greiðsla sem barst mjög seint | 2                 | 0              | **45**              |

Ruglingsfylkið sýnir niðurstöður tilraunagagnasafns sem er valið af handahófi úr þjálfunarferlinu. Þar sem þessir lokuðu reikningar voru ekki notaðir til að þjálfa líkanið eru reikningarnir upplögð tilvik til að prófa líkanið. Vegna þess að raunstaða reikningsins er þekkt er einnig hægt að sjá frammistöðu líkansins.

Fyrsta atriðið sem skal fylgjast með er algengasta raungildið. Þrátt fyrir að þetta gildi sé ekki fullkomlega samstillt við allt gagnasafnið er það fullnægjandi nálgun. Í þessu tilviki á **Raunveruleg greiðsla sem barst á tíma** sér stað í 92 af 171 allra reikninga og er algengasta raungildið. Þess vegna er slíkt góð grunnlína fyrir líkanið. Ef þú giskaðir á að allir reikningarnir bærust á tíma, hefðir þú rétt fyrir þér í 92 af 171 skiptum (þ.e. í 54 prósent tilvika).

Mikilvægt er að skilja jöfnuð gagnasafnsins. Í þessu tilviki voru 92 af 171 reikningum greiddir á réttum tíma, 32 voru greiddir of seint og 47 voru greiddir mjög seint. Þessi gildi gefa til kynna nokkuð jafnað gagnasafn vegna þess að engar ómerkilegar niðurstöður eru í hverjum flokki. Aðstæður þar sem ein staða gefur mjög fáar niðurstöður getur verið afar krefjandi fyrir vélnámslíkan.

Nákvæmni líkansins gefur til kynna fjölda réttra spáa fyrir prófunargagnasafnið. Þessar réttu spár eru gildin sem birtast feitletruð í dæminu hér á undan. Í þessu tilviki stuðla gildin að nákvæmni útreikninga sem nema 67,8 prósent (= \[71 + 0 + 45\] ÷ 171). Þetta gildi er bæting um 14 prósentugildi miðað við grunnlínu spár sem nemur 54 prósent og gefur vísbendingu um gæði líkansins.

Þegar ruglingsfylkið er skoðað nánar kemur í ljós að líkanið stendur sig vel við að spá fyrir um greiðslur reikninga sem berast í tíma og berast seint. Hins vegar spáir líkanið rangt til um 32 reikninga sem voru í reynd greiddir seint (en ekki mjög seint). Þessi niðurstaða bendir til þess að þróa og bæta verði líkanið.

Tala sem sýnir frammistöðu líkansins á betri hátt en nákvæmni er einkunn F1-fjölvans. Slík einkunn tekur mið af niðurstöðum hverrar flokkunarstöðu (á réttum tíma, seint og mjög seint). Hér eru til dæmis gögnin sem birtast fyrir mæligildi „F1-fjölvans“ í skýringarmyndinni hér á undan.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

Í þessu tilviki er einkunn F1-fjölvans u.þ.b.49,3 prósent sem sýnir að líkanið veitir ekki skilvirkar spár í hverri stöðu, þrátt fyrir að heildareinkunn fyrir nákvæmni virðist vera fullnægjandi.

## <a name="improving-the-model"></a>Endurbætur líkansins

Þegar niðurstöður fyrsta líkansins hafa verið metnar, gæti verið gott að bæta líkanið við með því að bæta við eða fjarlægja eiginleikadálka eða með því að sía alla hluta gagnasafnsins sem styðja ekki nákvæmar spár. Loka skal AI Builder og nota svo tengilinn **Endurbæta líkanið** í Dynamics 365 Finance til að endurræsa ferli AI Builder. Hægt er að prófa sig áfram með ólíka eiginleika án þess að slíkt hafi áhrif á útgefna líkanið. Útgefna líkanið verður einungis fyrir áhrifum þegar smellt er á **Birta**. Hafðu í huga að stakt líkan er notað fyrir tilvikið af Dynamics 365 Finance. Því skaltu fara vandlega yfir öll ný líkön áður en þau eru birt.

## <a name="for-more-information"></a>Frekari upplýsingar

Frekari upplýsingar um hvernig skal meta spálíkön er að finna í [Niðurstöður vélnámslíkana](/confusion-matrix.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
