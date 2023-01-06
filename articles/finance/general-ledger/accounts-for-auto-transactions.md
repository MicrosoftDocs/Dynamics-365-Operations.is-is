---
title: Lyklar fyrir sjálfvirkar færslur
description: Þessi grein útskýrir hvernig lyklar fyrir sjálfvirkar færslur eru notaðir fyrir bókun í gegnum Microsoft Dynamics 365 og gefur dæmi fyrir aðallykla fyrir sjálfvirkar færslur.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e72840fea1f5d89c908b00e2cf572bce6befbe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880760"
---
# <a name="accounts-for-automatic-transactions"></a>Lyklar fyrir sjálfvirkar færslur

Síðan **Lyklar fyrir sjálfvirkar færslur** (**Fjárhagur &gt; Bókunaruppsetning &gt; Lyklar fyrir sjálfvirkar færslur**) er notuð til að skilgreina sjálfgefinn aðallykil sem notaður er fyrir hverja bókunargerð í kerfinu. Þó að hægt sé að skilgreina flestar bókunargerðir á síðu einingar eða eiginleika er aðeins hægt að skilgreina sumar bókunargerðir á síðunni **Lyklar fyrir sjálfvirkar færslur**.

Til dæmis er hægt að tilgreina aðallykillinn sem er notaður fyrir bókunargerðina **Staða viðskiptavinar** í reitnum **Samantekt** á síðunni **Bókunarregla viðskiptavina** og nota annan aðallykil fyrir hverja reglu viðskiptavina. Þannig hefur þú meiri stjórn á bókunum. Á hinn bóginn geturðu aðeins tilgreint villulykil á síðunni **Lyklar fyrir sjálfvirkar færslur**.

Þegar þú opnar síðuna **Lyklar fyrir sjálfvirkar færslur** í nýjum lögaðila verður lyklalistinn tómur. Þú getur bætt við algengustu bókunargerðunum sem ættu að vera skilgreindar á síðunni með því að velja hnappinn **Stofna sjálfgefnar gerðir**. Síðan, fyrir hverja línu, er hægt að velja aðallykilinn í reitnum **Aðallykill**. Ef reiturinn **Aðallykill** er skilinn eftir auður fyrir bókunargerð og ekki er búið að skilgreina aðallykil á síðu einingar eða eiginleika koma upp villuboð þegar færsla sem notar bókunargerðina er bókuð. Skilaboðin verða yfirleitt: „Lykillinn fyrir \[Bókunargerð\] finnst ekki.“

## <a name="default-posting-types"></a>Sjálfgefnar bókunargerðir

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir sem eru búnar til þegar þú velur **Stofna sjálfgefnar gerðir** á síðunni **Lyklar fyrir sjálfvirkar færslur**. Þar er að finna sýnishorn af aðallyklum og lýsingar. „Debet/kredit?“ dálkur segir til um hvort færslan bóki yfirleitt debet eða kredit. Í sumum tilvikum er hægt að bóka færslu annað hvort með debet eða kredit. Dálkurinn „Millireikningur“ gefur til kynna hvort bókunargerð sé millireikningur. Ef bókunargerðin er millireikningur er upphæðin sem er bókuð á þennan lykil sjálfkrafa bakfærð þegar síðari færsla er bókuð.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Auramismunur í skýrslugjaldmiðli | 618160 | Ýmis kostnaður | Kostnaður | Bæði | Nr. | Þessi bókunargerð er notuð þegar auramismunur á sér stað þegar færsluupphæð í erlendum gjaldmiðli er færð yfir í skýrslugjaldmiðil. |
| Auramismunur í bókhaldsgjaldmiðli | 618160 | Ýmis kostnaður | Kostnaður | Bæði | Nr. | Þessi bókunargerð er notuð þegar auramismunur á sér stað þegar færsluupphæð í erlendum gjaldmiðli er færð yfir í bókhaldsgjaldmiðil. |
| Villulykill | 999999 | Villulykill | Kostnaður | Bæði | Nr. | Þessi bókunargerð er notuð þegar villa kemur upp í kerfinu. Reikninginn skal staðfesta á hverju tímabili og leysa skal úr öllum villum. |
| Niðurstaða í árslok | 300160 | Tekjur sem hefur verið aflað | Eigið fé | Bæði | Nr. | Þessi bókunargerð er notuð þegar vinnsla lokunar í árslok er keyrð til að færa stöðu lykla fyrir gerðina **Hagnaður og tap** inn á aðallykilinn sem er valinn fyrir niðurstöðu ársloka. |
| Staðgreiðsluafsláttur viðskiptavinar | Á ekki við | Á ekki við | Á ekki við | Á ekki við | Nr. | Bókunargerðin sem er skilgreind á síðunni **Lyklar fyrir sjálfvirkar færslur** er ekki notuð. Aðallykils er krafist þegar staðgreiðsluafsláttur er skilgreindur í viðskiptakröfum.|
| Staðgreiðsluafsláttur lánardrottins | Á ekki við | Á ekki við | Á ekki við | Á ekki við | Nr. | Bókunargerðin sem er skilgreind á síðunni **Lyklar fyrir sjálfvirkar færslur** er ekki notuð. Aðallykils er krafist þegar staðgreiðsluafsláttur er skilgreindur í viðskiptaskuldum. |

## <a name="additional-posting-types"></a>Fleiri bókunargerðir

Eftirfarandi tafla sýnir dæmi um fleiri bókunargerðir sem þarf að skilgreina ef nota á tengda eiginleika. Í þessum bókunargerðum er engin skilgreining bókunarreglu í boði í annarri einingu. „Debet/kredit?“ dálkur segir til um hvort færslan bóki yfirleitt debet eða kredit. Í sumum tilvikum er hægt að bóka færslu annað hvort með debet eða kredit. Dálkurinn „Millireikningur“ gefur til kynna hvort bókunargerð sé millireikningur. Ef bókunargerðin er millireikningur er upphæðin sem er bókuð á þennan lykil sjálfkrafa bakfærð þegar síðari færsla er bókuð.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Efnahagslykill fyrir samstæðumismun | 801200 | Hagnaður og tap - Endurmat | Kostnaður | Bæði | Nr. | Þessi bókunargerð er notuð þegar farið er í sameiningu sem felur í sér endurmat á gjaldmiðli og auramismunur kemur fram við endurmatið. |
| Rekstrarreikningur fyrir samstæðumismun | 801200 | Hagnaður og tap - Endurmat | Kostnaður | Bæði | Nr. | Þessi bókunargerð er notuð þegar farið er í sameiningu sem felur í sér endurmat á gjaldmiðli og auramismunur kemur fram við endurmatið. |
| Interunit - debit | 133500 | Interunit-viðskiptakröfur | Eign | Debet | Nr. | Þessi bókunargerð er notuð þegar þú velur jöfnunarvídd á síðu **Fjárhagur** og víddin jafnar ekki færslu sem er bókuð. |
| Millieining - kredit | 233500 | Interunit-viðskiptaskuld | Bótaábyrgð | Kredit | Nr. | Þessi bókunargerð er notuð þegar þú velur jöfnunarvídd á síðu **Fjárhagur** og víddin jafnar ekki færslu sem er bókuð. |
