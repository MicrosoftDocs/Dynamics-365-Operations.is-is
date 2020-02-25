---
title: Greiðsluferliseining
description: Þetta efni lýsir hvernig bæta skal greiðsluferliseiningu við nýja síðu og stilla nauðsynlega eiginleika.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3805c0faabc8afc3decffb924b7f25332ff1ab16
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025391"
---
# <a name="checkout-module"></a>Greiðsluferliseining


[!include [banner](includes/banner.md)]

Þetta efni lýsir hvernig bæta skal greiðsluferliseiningu við nýja síðu og stilla nauðsynlega eiginleika.

## <a name="overview"></a>Yfirlit

Greiðsluferliseining er sérstakur gámur sem hýsir allar einingar sem þarf til að búa til pöntun. Hún býður upp á skref fyrir skref flæði sem viðskiptavinur notar til að færa inn allar viðeigandi upplýsingar til að kaupa. Hún tekur upp sendingarfang, sendingaraðferð og innheimtuupplýsingar. Hún veitir einnig pöntunaryfirlit og aðrar upplýsingar sem tengjast pöntun viðskiptavina.

Í greiðsluferliseiningu eru gögn byggð á auðkenni körfunnar. Auðkenni þessa körfu er vistað sem vafrakaka. Auðkenni körfu er krafist til að afhenda upplýsingar í greiðsluferliseiningunni, svo sem hlutina í pöntuninni, heildarupphæðinni og afslætti.

## <a name="checkout-module-properties"></a>Eiginleikar greiðsluferliseiningar

Greiðsluferliseining sýnir pöntunaryfirlit og veitir virkni til að ganga frá pöntun. Til að safna öllum upplýsingum viðskiptavinarins sem þarf áður en hægt er að ganga frá pöntun þarf að bæta viðbótareiningum við greiðsluferliseininguna. Þess vegna hafa smásalar sveigjanleika til að bæta sérsniðnum einingum við greiðsluferlisflæðið eða útiloka einingar, byggðar á kröfum þeirra.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Einingar sem hægt er að nota í greiðsluferliseiningu

- **Sendingaraðsetur** - Þessi eining gerir viðskiptavini kleift að bæta við eða velja póstfang fyrir pöntun. Ef viðskiptavinurinn er skráður inn birtast öll heimilisföng sem áður voru vistuð fyrir þann viðskiptavin. Viðskiptavinurinn getur síðan valið á milli þessara heimilisfanga. Viðskiptavinurinn getur einnig bætt við nýju heimilisfangi. Sendingaraðsetrið er notað fyrir allar vörur í pöntuninni sem krefjast sendingar. Ekki er hægt að sérsníða það fyrir einstakar línuvörur. Sniðmát sendingaraðaseturs er skilgreint fyrir hvert land eða svæði og reglum um land/svæði er framfylgt með þessari einingu. Þrátt fyrir að þessi eining veiti ekki staðfestingu á heimilisfangi er hægt að útfæra staðfestingu heimilisfangs með sérstillingu. Ef pöntunin inniheldur aðeins hluti sem verða sóttir í versluninni er þessi eining sjálfkrafa falin.
- **Afhendingarkostir** - Þessi eining gerir viðskiptavini kleift að velja afhendingarvalkost fyrir pöntun. Afhendingarkostir eru byggðir á sendingaraðsetri. Ef sendingaraðsetri er breytt verður að sækja afhendingarvalkostina aftur. Ef pöntunin inniheldur aðeins hluti sem verða sóttir í versluninni er þessi eining sjálfkrafa falin.
- **Gámur í greiðsluferlishlutanum** - Þessi eining er gámur sem þú getur sett margar einingar í til að stofna hluta innan greiðsluferlisflæðisins. Til dæmis er hægt að setja allar greiðslutengdar einingar í þennan gám til að láta þær birtast sem einn hluta. Þessi eining hefur aðeins áhrif á skipulag flæðisins.
- **Gjafakort** - Þessi eining gerir viðskiptavini kleift að greiða fyrir pöntun með því að nota gjafakort. Hún styður aðeins Microsoft Dynamics 365 Commerce gjafabréf. Hægt er að nota eitt eða fleiri gjafakort á pöntun. Ef inneign gjafakortsins nær ekki yfir upphæðina í körfunni er hægt að sameina gjafakortið með öðrum greiðslumáta. Aðeins er hægt að innleysa gjafakort ef viðskiptavinurinn er skráður inn.
- **Vildarpunktar** - Þessi eining gerir viðskiptavini kleift að greiða fyrir pöntun með því að nota vildarpunkta. Hún veitir samantekt á tiltækum punktum og stigum sem eru að renna út og lætur viðskiptavininn velja fjölda stiga sem á að innleysa. Ef viðskiptavinurinn er ekki skráður inn eða er ekki meðlimur vildarkerfis eða ef heildarupphæðin í körfunni er 0 (núll) er þessi eining sjálfkrafa falin.
- **Greiðsla** - Þessi eining gerir viðskiptavini kleift að greiða fyrir pöntun með því að nota kreditkort. Ef vildarpunktar eða gjafakort ná yfir heildarupphæðina í körfunni eða ef hún er 0 (núll) er þessi eining sjálfkrafa falin. Kreditkortasamþætting er veitt af Adyen greiðslutenglinum fyrir þessa einingu. Fyrir frekari upplýsingar um notkun þessa tengils, sjá [Dynamics 365 Adyen greiðslutengil](dev-itpro/adyen-connector.md).
- **Innheimtuaðsetur** - Þessi eining gerir viðskiptavini kleift að veita innheimtuupplýsingar. Þessar upplýsingar eru unnar ásamt kreditkortaupplýsingum af Adyen. Þessi eining felur í sér valkost sem gerir það að verkum að viðskiptavinir nota innheimtuaðsetur sitt sem póstfang.
- **Upplýsingar um tengiliði** - Þessi eining gerir viðskiptavini kleift að bæta við eða breyta tengiliðaupplýsingum (netfangi) fyrir pöntun.
- **Textabálkur** - Þessi eining inniheldur öll skilaboð sem eru knúin áfram af innihaldsstjórnunarkerfinu (CMS). Til dæmis gæti hún innihaldið skilaboð sem segja: „Fyrir vandamál með pöntunina þína skaltu hafa samband í 1-800-Fabrikam.“ 

## <a name="commerce-scale-unit-interaction"></a>Samskipti við Commerce Scale Unit

Flestar greiðsluupplýsingar, svo sem póstfang og sendingaraðferð, eru geymdar í körfunni og unnar sem hluti af pöntuninni. Eina undantekningin er kreditkortaupplýsingarnar. Þessar upplýsingar eru unnar beint með því að nota Adyen greiðslutengilinn. Greiðslan er heimil en er ekki gjaldfærð.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Bæta greiðsluferliseiningu við nýja síðu og stilla nauðsynlega eiginleika

Fylgdu þessum skrefum til að bæta greiðsluferliseiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Brot \> Nýtt brot** og nefndu nýja brotið **Greiðsluferlisbrot**.
1. Bættu greiðsluferlieiningu við brotið.
1. Bæta fyrirsögn við greiðsluferlieininguna.
1. Bættu við sendingaraðfangi, afhendingarvalkostum, gámi fyrir greiðsluferlishluta og upplýsingum um tengiliði. 
1. Bætið við gjafakorti, vildarpöntum og greiðslueiningum í gámaeiningadeild greiðsluhlutans. Með þessum hætti tryggirðu að allir greiðslumáta birtist saman í hluta.
1. Vistaðu og forskoðaðu brotið. Ekki er víst að sumar einingar sem ekki eru með körfusamhengi séu sýndar í forskoðuninni.
1. Ljúktu við að breyta brotinu, vistaðu það og birtu.
1. Búðu til sniðmát sem notar nýja greiðsluferlisbrotið.
1. Búðu til greiðslusíðu sem notar nýja sniðmátið.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupkassaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Pöntunarstaðfestingareining](order-confirmation-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)
