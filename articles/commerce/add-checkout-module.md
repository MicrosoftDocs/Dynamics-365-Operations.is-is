---
title: Greiðsluferliseining
description: Þetta efni lýsir hvernig bæta skal greiðsluferliseiningu við nýja síðu og stilla nauðsynlega eiginleika.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 8439b88ccda3f72e5a9b918c6c89bd406599b516
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818227"
---
# <a name="checkout-module"></a>Greiðsluferliseining

[!include [banner](includes/banner.md)]

Þetta efni lýsir hvernig bæta skal greiðsluferliseiningu við nýja síðu og stilla nauðsynlega eiginleika.

## <a name="overview"></a>Yfirlit

Greiðsluferliseining er sérstakur gámur sem hýsir allar einingar sem þarf til að búa til pöntun. Hún býður upp á skref fyrir skref flæði sem viðskiptavinur notar til að færa inn allar viðeigandi upplýsingar til að kaupa. Hún tekur upp sendingarfang, sendingaraðferð og innheimtuupplýsingar. Hún veitir einnig pöntunaryfirlit og aðrar upplýsingar sem tengjast pöntun viðskiptavina.

Í greiðsluferliseiningu eru gögn byggð á auðkenni körfunnar. Auðkenni þessa körfu er vistað sem vafrakaka. Auðkenni körfu er krafist til að afhenda upplýsingar í greiðsluferliseiningunni, svo sem hlutina í pöntuninni, heildarupphæðinni og afslætti. 

Eftirfarandi mynd sýnir dæmi um greiðsluferliseiningu Fabrikam á greiðsluferlissíðu.

![Dæmi um greiðsluferliseiningu](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Eiginleikar greiðsluferliseiningar

Greiðsluferliseining sýnir pöntunaryfirlit og veitir virkni til að ganga frá pöntun. Til að safna öllum upplýsingum viðskiptavinarins sem þarf áður en hægt er að ganga frá pöntun þarf að bæta viðbótareiningum við greiðsluferliseininguna. Þess vegna hafa smásalar sveigjanleika til að bæta sérsniðnum einingum við greiðsluferlisflæðið eða útiloka einingar, byggðar á kröfum þeirra.

| Nafn eiginleika | Gildi | lýsing |
|----------------|--------|-------------|
| Fyrirsögn greiðsluferlis | Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Fyrirsögn fyrir greiðsluferliseininguna. |
| Fyrirsögn fyrir samantekt pöntunar | Fyrirsagnartexti | Fyrirsögn fyrir hluta pöntunarsamantektar í einingunni. |
| Fyrirsögn fyrir línuatriði körfu | Fyrirsagnartexti | Fyrirsögn fyrir línuatriði körfu sem er sýnd í greiðsluferliseiningunni. |
| Sýna sendingargjöld á línuatriði | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt** verða sendingargjöldin sem eiga við um línuatriði sýnd í körfulínum. Ef kveikt er á eiginleikanum **Hausgjald með engri hlutfallsskiptingu** í Commerce Headquarters, verður sendingargjaldið notað á hausstigi, ekki línustigi. Þessum eiginleika var bætt við í Commerce útgáfu 10.0.13. |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>Einingar sem hægt er að nota í greiðsluferliseiningu

- **Sendingaraðsetur** - Þessi eining gerir viðskiptavini kleift að bæta við eða velja póstfang fyrir pöntun. Frekari upplýsingar um þessa einingu er að finna í [Eining sendingaraðseturs](ship-address-module.md).

    Eftirfarandi mynd sýnir dæmi um sendingaraðseturseiningu á greiðsluferlissíðu.

    ![Dæmi um sendingaraðseturseiningu](./media/ecommerce-shippingaddress.PNG)

- **Afhendingarvalkostir** – Þessi eining gerir viðskiptavini kleift að velja afhendingarmáta fyrir pöntun. Frekari upplýsingar um þessa einingu er að finna í [Eining afhendingarvalkosta](delivery-options-module.md).

    Eftirfarandi mynd sýnir dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu.
 
    ![Dæmi um einingu afhendingarvalkosts](./media/ecommerce-deliveryoptions.PNG)

- **Gámur í greiðsluferlishlutanum** - Þessi eining er gámur sem þú getur sett margar einingar í til að stofna hluta innan greiðsluferlisflæðisins. Til dæmis er hægt að setja allar greiðslutengdar einingar í þennan gám til að láta þær birtast sem einn hluta. Þessi eining hefur aðeins áhrif á skipulag flæðisins.

- **Gjafakort** - Þessi eining gerir viðskiptavini kleift að greiða fyrir pöntun með því að nota gjafakort. Frekari upplýsingar um þessa einingu er að finna í [Eining gjafakorts](add-giftcard.md).

- **Vildarpunktar** - Þessi eining gerir viðskiptavini kleift að greiða fyrir pöntun með því að nota vildarpunkta. Hún veitir samantekt á tiltækum punktum og stigum sem eru að renna út og lætur viðskiptavininn velja fjölda stiga sem á að innleysa. Ef viðskiptavinurinn er ekki skráður inn eða er ekki meðlimur vildarkerfis eða ef heildarupphæðin í körfunni er 0 (núll) er þessi eining sjálfkrafa falin.

- **Greiðsla** – Þessi eining leyfir viðskiptavini að greiða pöntun með kredit-eða debetkorti. Viðskiptavinir geta einnig gefið upp reikningsaðsetur fyrir greiðsluvalkostinn sem þeir velja. Frekari upplýsingar um þessa einingu er að finna í [Greiðslueining](payment-module.md).

    Eftirfarandi mynd sýnir dæmi um einingar gjafakorts, vildarpunkta og greiðslu á greiðsluferlissíðu.

    ![Dæmi um einingar gjafakorts, vildarpunkta og greiðslu á greiðsluferlissíðu](./media/ecommerce-payments.PNG)

- **Upplýsingar um tengiliði** - Þessi eining gerir viðskiptavini kleift að bæta við eða breyta tengiliðaupplýsingum (netfangi) fyrir pöntun.

- **Textabálkur** - Þessi eining inniheldur öll skilaboð sem eru knúin áfram af innihaldsstjórnunarkerfinu (CMS). Til dæmis gæti hún innihaldið skilaboð sem segja: „Fyrir vandamál með pöntunina þína skaltu hafa samband í 1-800-Fabrikam.“ 

- **Skilmálar greiðsluferlis** – Þessi eining sýnir sniðinn texta sem inniheldur skilmála og gátreit fyrir innslátt viðskiptavinar. Gátreiturinn valkvæður og stillanlegur. Einingin tekur við innslættinum og hægt er að nota hann til að athuga áður en pöntun er gerð, en er ekki hluti af samantektarupplýsingum pöntunarinnar. Hægt er að bæta þessari einingu við greiðsluferlissvæðið, svæði greiðsluferlishluta eða hólf skilmála, eftir viðskiptaþörfum. Ef henni er bætt við greiðsluferlissvæðið eða hólfasvæði greiðsluferlishlutans, birtist hún sem skref í greiðsluferlinu. Ef henni er bætt við hólf skilmálanna, birtist hún nálægt hnappi pöntunarinnlagnar.

    Eftirfarandi mynd sýnir dæmi um skilmála á greiðsluferlissíðu.

    ![Dæmi um skilmála á greiðsluferlissíðu](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>Samskipti við Commerce Scale Unit

Flestar greiðsluupplýsingar, svo sem póstfang og sendingaraðferð, eru geymdar í körfunni og unnar sem hluti af pöntuninni. Eina undantekningin er kreditkortaupplýsingarnar. Þessar upplýsingar eru unnar beint með því að nota Adyen greiðslutengilinn. Greiðslan er heimiluð, en hún er ekki gjaldfærð fyrr en pöntunin er uppfyllt.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Bæta greiðsluferliseiningu við síðu og stilla nauðsynlega eiginleika

Fylgdu þessum skrefum til að bæta greiðsluferliseiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.
1. Í svarglugganum **Nýtt brot** skal velja eininguna **Greiðsluferli**.
1. Undir **Heiti brots** skal slá inn heitið **Greiðsluferlisbrot** og síðan velja **Í lagi**.
1. Veldu hólfið **Greiðsluferliseining**.
1. Hægra megin á eiginleikasvæðinu skal velja blýantstáknið, slá inn texta fyrirsagnar í reitinn og síðan velja gátmerkistáknið.
1. Í hólfinu **Upplýsingar um greiðsluferli** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í svarglugganum **Bæta við einingu** skal velja einingarnar **Sendingaraðsetur**, **Afhendingarvalkostir**, **Hólf greiðsluferlishluta** og **Samskiptaupplýsingar** og síðan velja **Í lagi**.
1. Í einingunni **Hólf greiðsluferlishluta** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja einingarnar **Gjafakort**, **Vildarkerfi** og **Greiðsla** og síðan velja **Í lagi**. Með þessum hætti tryggirðu að allir greiðslumáta birtist saman í hluta.
1. Í hólfinu **Skilmálar** skal bæta við **Skilmálar greiðsluferlis** einingu ef þess gerist þörf. Í eiginleikasvæði einingarinnar skal stilla skilmálatextann eins og er við hæfi.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðubrotið. Ekki er víst að sumar einingar sem ekki eru með körfusamhengi séu sýndar í forskoðuninni.
1. Veldu **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.
1. Búðu til sniðmát sem notar nýja greiðsluferlisbrotið.
1. Búðu til greiðslusíðu sem notar nýja sniðmátið.

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðslueining](payment-module.md)

[Eining sendingaraðseturs](ship-address-module.md)

[Eining afhendingarvalkosta](delivery-options-module.md)

[Pöntunarupplýsingaeining](order-confirmation-module.md)

[Gjafakortseining](add-giftcard.md)
