---
title: Greiðslueining
description: Þessi grein fjallar um greiðslueininguna og útskýrir hvernig á að stilla hana í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: fa1482cb73a40df5f9bc9d3037196def71accf18
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279476"
---
# <a name="payment-module"></a>Greiðslueining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um greiðslueininguna og útskýrir hvernig á að stilla hana í Microsoft Dynamics 365 Commerce.

Greiðslueiningin gerir viðskiptavinum kleift að greiða pantanir með kredit- eða debetkortum. Greiðslusamþætting fyrir þessa eining er í boði greiðslutengils Dynamics 365 fyrir Adyen. Frekari upplýsingar um hvernig setja á upp og skilgreina greiðslutengil er að finna í [Greiðslutengill Dynamics 365 fyrir Adyen](dev-itpro/adyen-connector.md).  

Frá og með Commerce útgáfu 10.0.14 hefur greiðslueiningin einnig verið samþætt við greiðslutengil Dynamics 365 fyrir PayPal til að gera viðskiptavinum kleift að greiða fyrir pantanir með PayPal. Frekari upplýsingar um hvernig skal setja upp og skilgreina greiðslutengil Dynamics 365 fyrir PayPal er að finna í [Greiðslutengill Dynamics 365 fyrir PayPal](paypal.md). 

## <a name="dynamics-365-payment-connector-for-adyen"></a>Dynamics 365-greiðslutengill fyrir Adyen 

Greiðslueiningin hýsir greiðsluupplýsingar sem er miðlað í gegnum Adyen í innfelldum HTML-ramma (iframe). Greiðslueiningin vinnur með Commerce Scale Unit til að sækja Adyen-greiðsluupplýsingar. Sem hluti af samvinnu Commerce Scale Unit, getur greiðslueiningin leyft upplýsingar um reikningsaðsetur að vera sett fram annaðhvort í iframe með Adyen eða aðskilinni einingu. Í Fabrikam-þemanu er reikningsaðsetrið sýnt í aðskilinni einingu. Þessi nálgun býður upp á meiri sveigjanleika fyrir sniðmótun, því að hægt er að sýna línur aðsetursins þannig að þær líkist línum afhendingaraðsetursins.

Greiðslueiningin leyfir einnig innskráðum viðskiptavinum að vista greiðsluupplýsingarnar sínar. Greiðsluupplýsingar og reikningsaðsetur eru vistuð og stjórnað í gegnum Adyen-greiðslutengilinn.

Greiðslueiningin nær yfir öll pöntunargjöld sem vildarpunktar eða gjafakort ná ekki þegar yfir. Ef samtala fyrir pöntun er að fullu dekkuð af vildarpunktum eða inneign gjafakorts, verður greiðslueiningin falin, og viðskiptavinurinn mun geta lagt inn pöntunina án hennar.

Adyen-greiðslutengillinn styður einnig öfluga sannvottun viðskiptavinar (SCA). Hluti af endurskoðaðri greiðsluþjónustutilskipun (PSD2) Evrópusambandsins (ESB) krefst þess að kaupendur á netinu verði auðkenndir utan umhverfis netverslunarinnar þegar þeir nota rafrænan greiðslumáta. Meðan á greiðsluferlinu stendur, er viðskiptavinum vísað á bankaþjónustusvæðið þeirra og síðan eftir sannvottun er þeim beint aftur í greiðsluferli Commerce. Á meðan á þessari framsendingu stendur verða upplýsingar sem viðskiptavinur færði inn meðan á greiðsluferli stóð (til dæmis sendingaraðsetur, afhendingarvalkostir, upplýsingar um gjafakort og vildarupplýsingar) haldið við. Áður en hægt er að kveikja á þessum eiginleika verður að skilgreina Adyen greiðslutengilinn fyrir öfluga sannvottun viðskiptavinar í Commerce Headquarters. Frekari upplýsingar er að finna í [Öflug sannvottun viðskiptavinar með Adyen](adyen_redirect.md). Þessi eiginleiki var virkjaður í Commerce Release 10.0.12.

> [!NOTE]
> Fyrir Adyen-greiðslutengil er aðeins hægt að nota iframe-einingu í greiðslueiningunni ef bætt er við Adyen URL á heimildalista síðunnar. Til að ljúka þessu skrefi skal bæta við **\*.adyen.com** á **child-src**, **connect-src**, **img-src**, **script-src** og **style-src** við öryggisreglur svæðisins þíns. Frekari upplýsingar er að finna í [Stjórna öryggisreglu fyrir efni](manage-csp.md). 

Eftirfarandi skýringarmynd sýnir dæmi um einingar gjafakorts, vildarpunkta og Adyen greiðslueiningar á greiðsluferlissíðu.

![Dæmi um gjafakort, vildarpunkta og Adyen-greiðslueiningar á greiðsluferlissíðu.](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>Dynamics 365 Payment Connector fyrir PayPal

Frá og með Commerce Release 10.0.14 er greiðslueiningin einnig samþætt við Dynamics 365 greiðslutengil fyrir PayPal. Frekari upplýsingar um hvernig setja á upp og skilgreina greiðslutengil er að finna í [Greiðslutengill Dynamics 365 fyrir PayPal](paypal.md).
 
Á síðu greiðsluferlis er hægt að hafa bæði Adyen og PayPal-tenglana skilgreinda. Viðbótareiginleikum hefur verið bætt við greiðslueininguna til að auðvelda auðkenningu á tenglunum sem einingin skal tengjast. Fyrir frekari upplýsingar, sjá **Stuðlar útboðsgerðir** og **Er frumgreiðsla** mát eiginleika í eftirfarandi töflu.
  
Þegar búið er að skilgreina greiðslueininguna til að nota PayPal-greiðslutengil birtist PayPal-hnappur á afgreiðslusíðu. Eftir kvaðningu frá viðskiptavini myndþýðir greiðslueiningin IFrame sem inniheldur PayPal-upplýsingar. Viðskiptavinurinn getur skráð sig inn og látið í té PayPal-upplýsingar sínar í slíkum IFrame til að ljúka færslunni sinni. Þegar viðskiptavinur kýs að greiða með PayPal verða eftirstöðvar pöntunarinnar skuldfærðar af PayPal.

PayPal-greiðslutengill þarf ekki reikningsaðseturseiningu vegna þess að allar upplýsingar varðandi reikninga eru afgreiddar af PayPal innan viðeigandi IFrame. Hins vegar eru einingar heimilisfangs viðtakanda og afhendingarvalkosta áskildar.

Eftirfarandi skýringarmynd sýnir dæmi um tvær greiðslueiningar á síðu greiðsluferils, ein eining skilgreind með Adyen-greiðslutenglinum og önnur eining skilgreind með PayPal-greiðslutenglinum.
![Dæmi um Adyen-greiðslu og PayPal-einingar á afgreiðslusíðu.](./media/ecommerce-paypal.png)

Eftirfarandi mynd sýnir dæmi um PayPal IFrame sem er ræst með PayPal-hnappnum. 
![Dæmi um Paypal iframe á afgreiðslusíðu.](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Eiginleikar greiðslueiningar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Fyrirsögn | Fyrirsagnartexti | Valfrjáls fyrirsögn fyrir greiðslueininguna. |
| Hæð iFrame | Dílar | Hæð iframe í dílum. Hægt er að stilla hæðina eftir þörfum. |
| Sýna greiðsluaðsetur | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt** verður reikningsaðsetrið lagt fram af Adyen innan iframe greiðslueiningarinnar. Ef hann er stilltur á **Ósatt** verður reikningsaðsetrið ekki lagt fram af Adyen og notandi Commerce verður að skilgreina einingu til að sýna reikningsaðsetrið greiðsluferlissíðunni. Þessi svæði hefur engin áhrif á PayPal-greiðslutengið því PayPal meðhöndlar reikningsaðsetrið að öllu leyti. |
| Hnekkja greiðslustíl | Kóði fyrir stölluð stílblöð (CSS) | Vegna þess að greiðslueiningin er hýst í iframe, er takmarkaður möguleiki á stílmótun. Hægt er að ná einhverri stílmótun með því að nota þennan eiginleika. Til að hnekkja stílbrigðum svæðis þarf að líma CSS-kóðann inn sem gildið fyrir þennan eiginleika. Hnekkingar og stílbrigði CSS-svæðissmiðs eiga ekki við um þessa einingu. |
|Studdir greiðslumátar| Strengur| Ef mörg greiðslutengi eru stillt, ættirðu að gefa upp studda útboðstegundarstrenginn eins og hann er skilgreindur í greiðslutengisstillingu höfuðstöðva Commerce (sjá eftirfarandi mynd). Sjálfgefið er stillt á Adyen-greiðslutengilinn ef enginn er til staðar. Bætt við í Commerce Release 10.0.14.|
|Er aðalgreiðsla|  **Satt** eða **Ósatt** | Ef **Satt** verða öll villuboð mynduð úr aðalgreiðslutenglinum á síðu greiðsluferlisins. Þegar bæði Adyen- og PayPal-greiðslutenglarnir eru skilgreindir skal stilla Adyen á **Satt**, en slíkum eiginleika við Commerce útgáfu 10.0.14.|
|Nota tengikenni| **Satt** eða **Ósatt** | Notaðu þennan eiginleika ef mörg greiðslutengi eru stillt fyrir síðuna. Ef **Satt**, tengi þurfa að nota tengi auðkenni fyrir greiðslufylgni.|
|Notaðu vafrastillingar tungumálakóða fyrir iFrame|  **Satt** eða **Ósatt** | (aðeins Adyen) Ef **Satt**, Adyen iFrame mun birta tungumálið út frá samhengi vafra notandans í stað þess að nota tungumálakóða viðskiptarásarinnar sem er stillt fyrir síðuna. Bætt við í Commerce Release 10.0.27.|

Skýringarmyndin hér á eftir sýnir dæmi um gildið **Studdir greiðslumátar** stillt á „PayPal“ í skilgreiningu greiðslutengilsins í Commerce Headquarters.
![Dæmi um studda greiðslumáta í Commerce Headquarters.](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Póstfang greiðanda

Nota má eininguna reikningsaðsetur síðu greiðsluferlisins ef reikningsaðseturslínur Adyen-greiðslutengilsins passa nægilega vel við útlit vefsvæðisins. 

Til að nota reikningsaðseturseiningu á síðu greiðsluferlisins þegar greiðslueiningin er samþætt við Adyen-greiðslutengil skal stilla eiginleikann **Sýna reikningsaðsetur** á **Ósatt** þannig að hægt sé að nota sérstillta reikningsaðseturseiningu í staðinn fyrir sjálfgefna Adyen-reikningsaðsetrið. Í þessu tilviki ætti höfundur síðu að hafa reikningsaðseturseiningu með á síðu greiðsluferlisins. Adyen-greiðslutengillinn gerir einnig kleift að nota heimilisfang viðtakanda sem reikningsaðsetur til að draga úr fjölda skrefa fyrir notanda vefsvæðisins.

Á svipaðan hátt og greiðslueiningum hefur eiginleikanum **Studdir greiðslumátar** verið bætt við eininguna reikningsaðsetur í Commerce útgáfu 10.0.14. Gildi eiginleikans skal vera sama og gildisins sem kemur fram í greiðslueiningunni til að tryggja að þær vinni saman. Hvað Adyen-greiðslutengilinn varðar, eiga bæði greiðslueiningin og reikningsaðseturseiningin að hafa þetta gildi autt (sjálfgefin stilling). Ekki er krafist sérstakrar reikningsaðseturseiningar fyrir PayPal-tengilinn. Fyrir aðrar gerðir greiðslutengla ætti strengurinn að vera samkvæmt skilgreiningu í Commerce Headquarters.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Bæta greiðslueiningu við greiðsluferlissíðu og stilla nauðsynlega eiginleika

Aðeins er hægt að bæta greiðslueiningu við greiðsluferliseiningu. Frekari upplýsingar um hvernig á að skilgreina greiðslueiningu fyrir greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).

## <a name="configure-the-adyen-and-paypal-payment-connectors-when-both-are-used"></a>Stilltu Adyen og PayPal greiðslutengi þegar bæði eru notuð

Ef bæði Adyen og PayPal greiðslutengarnir verða notaðir fyrir síðuna þína, fylgdu þessum skrefum í Commerce site builder til að bæta greiðslueiningum fyrir hvern tengi við afgreiðslueininguna og stilla síðan eiginleikana fyrir hverja einingu.

1. Í eiginleikarúðunni fyrir PayPal greiðslueininguna skaltu fylgja þessum skrefum:

    1. Á sviði fyrir **Stuðlar útboðsgerðir** eign, inn **PayPal**.
    1. Hreinsaðu gátreitinn fyrir **Er frumgreiðsla** eign.
    1. Veldu gátreitinn fyrir **Notaðu auðkenni tengis** eign.

1. Í eiginleikarúðunni fyrir Adyen greiðslueininguna skaltu fylgja þessum skrefum:

    1. Farðu af velli fyrir **Stuðlar útboðsgerðir** eign auð.
    1. Veldu gátreitinn fyrir **Er frumgreiðsla** eign.
    1. Veldu gátreitinn fyrir **Notaðu auðkenni tengis** eign.

> [!NOTE]
> Þegar þú stillir Adyen og PayPal tengin til að nota saman, **Dynamics 365 greiðslutengi fyrir Adyen** stillingar verða að vera í fyrsta sæti í netrásinni **Greiðslureikningar** tengistillingu í höfuðstöðvum Commerce. Til að staðfesta eða breyta tengipöntuninni skaltu fara á **Netverslanir**, og veldu rásina fyrir síðuna þína. Síðan, á **Settu upp** flipa, á **Greiðslureikningar** Flýtiflipi, undir **Tengi**, vertu viss um að **Dynamics 365 greiðslutengi fyrir Adyen** stilling er í fyrstu stöðu (þ.e. á efstu línu), og að **Dynamics 365 greiðslutengi fyrir PayPal** uppsetning er á annarri línu. Bættu við eða fjarlægðu tengjum eftir þörfum til að endurraða þeim.

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Sendingaraðseturseining](ship-address-module.md)

[Afhendingarkostaeining](delivery-options-module.md)

[Eining fyrir afhendingarupplýsingar](pickup-info-module.md)

[Pöntunarupplýsingaeining](order-confirmation-module.md)

[Gjafakortseining](add-giftcard.md)

[Dynamics 365-greiðslutengill fyrir Adyen](dev-itpro/adyen-connector.md)

[Dynamics 365 Payment Connector fyrir PayPal](paypal.md)

[Öflug sannvottun viðskiptavinar með Adyen](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
