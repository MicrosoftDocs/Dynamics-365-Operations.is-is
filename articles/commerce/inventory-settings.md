---
title: Nota birgðastillingar
description: Þessi grein fjallar um birgðastillingar og lýsir því hvernig eigi að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 49310a44f8b9c636734e04d4eed9445384b55791
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405321"
---
# <a name="apply-inventory-settings"></a>Nota birgðastillingar

[!include [banner](includes/banner.md)]

Þessi grein fjallar um birgðastillingar og lýsir því hvernig eigi að nota þær í Microsoft Dynamics 365 Commerce.

Birgðastillingar tilgreina hvort athuga eigi birgða áður en afurðir eru settar í körfuna. Þær skilgreina einnig birgðatengd skilaboð um smásöluvörur, t.d. „Á lager“ og „Lítið eftir“. Þessar stillingar ganga úr skugga um að ekki sé hægt að kaupa afurð ef hún er ekki til á lager.

Dynamics 365 Commerce leggur mat á lagerstöðu fyrir afurðir. Upplýsingar um hvernig áætlað framboð á lager er reiknað er að finna í [Reikna tiltækar birgðir fyrir smásölurásir](calculated-inventory-retail-channels.md).

Í Commerce-vefssmið er hægt að skilgreina birgðaþröskuld og birgðabil fyrir afurð eða flokk. Það ákvarðar hvort birgðir geti verið flokkaðar sem á lager, lítið til á lager eða ekki til á lager. Frekari upplýsingar er að finna í [Stilla birgðabiðminni og birgðastöðu](inventory-buffers-levels.md).

> [!NOTE]
> Stuðningur við birgðaþröskulda og svið er tiltækur í Dynamics 365 Commerce útgáfu 10.0.12.

## <a name="inventory-settings"></a>Birgðastillingar

Í Commerce eru birgðastillingar skilgreindar í **Stillingar svæðis \> Viðbætur \> Birgðastjórnun** í svæðissmið. Til eru sex birgðastillingar en ein þeirra er úreld:

- **Virkja birgðaathugun í forriti** – Þessi stilling kveikir á birgðaathugun afurðar. Einingarnar kaupgluggi og sækja í verslun athuga þá birgðir afurðar og leyfa að afurð sé bætt í körfuna aðeins ef birgðir eru til staðar.
- **Birgðastaða byggir á** – Þessi stilling skilgreinir hvernig birgðastöður eru reiknaðar. Tiltæk gildi eru **Samtals tiltækt**, **Efnislegt magn tiltækt** og **Þröskuldur fyrir ekki til á lager**. Í Commerce er hægt að skilgreina birgðaþröskuld og birgðabil fyrir hverja afurð og flokk. API-birgðir skila birgðaupplýsingum um afurð fyrir bæði eiginleikann **Samtals tiltækt** og **Efnislegt magn tiltækt**. Smásöluaðilinn ákveður hvort nota eigi **Samtals tiltækt** eða **Efnislegt magn tiltækt** til að ákvarða birgðatalninguna og samsvarandi bil fyrir „til á lager“ og „ekki til á lager“ stöðurnar.

    Gildið **Þröskuldur fyrir ekki til á lager** í stillingunni **Birgðastaða byggir á** er gamalt, úrelt gildi. Þegar það er valið er birgðatalningin ákvörðuð út frá niðurstöðum gildisins **Samtals tiltækt**, en þröskuldurinn er skilgreindur af talnastillingunni **Þröskuldur fyrir ekki til á lager** sem er útskýrð seinna. Þessi þröskuldsstilling á við um allar afurðir á svæði rafrænna viðskipta. Ef birgðir eru undir þröskuldstölunni er litið á að afurð sé ekki til á lager. Annars er það talið til á lager. Möguleikar gildisins **Þröskuldur fyrir ekki til á lager** eru takmarkaðir og ekki er mælt með því að það sé notað í útgáfu 10.0.12 eða síðar.

- **Birgðastig fyrir mörg vöruhús** – Þessi stilling gerir kleift að reikna birgðastöðuna gagnvart sjálfgefnu vöruhúsi eða mörgum vöruhúsum. Valkosturinn **Byggt á einu vöruhúsi** mun reikna út birgðastöðuna út frá sjálfgefna vöruhúsinu. Einnig getur svæði rafrænna viðskipta bent á mörg vöruhús til að auðvelda uppfyllingu. Í því tilfelli er valkosturinn **Byggt á samtölu fyrir vöruhús sendingar og afhendingar** notaður til að gefa til kynna birgðaframboð. Til dæmis þegar viðskiptavinur kaupir vöru og velur „sendingu“ sem afhendingarmátann, varan getur verið send frá einhverju vöruhúsi í uppfyllingarflokknum sem er með birgðir á lausu. Upplýsingasíða afurðar (PDP) mun sýna skilaboðin „Á lager“ fyrir sendingu ef eitthvert vöruhús sendingar í uppfyllingarflokknum er með birgðir. 

    > [!IMPORTANT] 
    > Stillingin **Birgðastaða fyrir mörg vöruhús** er í boði frá og með Commerce-útgáfu 10.0.19. Ef verið er að uppfæra úr eldri útgáfu af Commerce verður að uppfæra appsettings.json-skrána handvirkt. Leiðbeiningar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Birgðastillingar fyrir listasíður afurða** – Þessi stilling skilgreinir hvernig vörur sem eru ekki til á lager eru sýndar í afurðalistum sem eru settir fram eftir vörusafns- og leitarniðurstöðueiningu. Tiltæk gildi eru **Sýna í röð með öðrum vörum**, **Fela vörur á listanum sem ekki eru til á lager** og **Sýna vörur sem eru ekki til á lager neðst á listanum**. Til að nota þessa stillingu þarf fyrst að skilgreina nokkrar stillingar skilyrða í Commerce Headquarters. Fyrir frekari upplýsingar, sjá [Birgðameðvituð vöruskráning](inventory-aware-product-listing.md).

    > [!IMPORTANT] 
    > Stillingin **Birgðastillingar fyrir síður afurðalista** er tiltæk frá og með Commerce-útgáfu 10.0.20. Ef verið er að uppfæra úr eldri útgáfu af Commerce verður að uppfæra appsettings.json-skrána handvirkt. Leiðbeiningar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Birgðasvið** – Þessi stilling skilgreinir birgðasviðsskilaboðin sem eru sýnd á vefeiningum. Það gildir aðeins ef annaðhvort gildið **Samtals tiltækt** eða gildið **Efnislegt magn tiltækt** er valið fyrir stillinguna **Birgðastaða byggist á**. Tiltæk gildi eru **Allt**, **Litlar birgðir og ekki til á lager** og **Ekki til á lager**.

    - Þegar **Allt** er valið verða skilaboð fyrir öll birgðasvið, frá á lager („Til á lager“ skilaboð) til ekki til á lager („Ekki til á lager“ skilaboð) sýnd.
    - Þegar **Litlar birgðir og ekki til á lager** er valið verða skilaboð fyrir öll birgðasvið, nema á lager („Til á lager“ skilaboð) sýnd.
    - Þegar **Ekki til á lager** er valið verður aðeins „Ekki til á lager“ skilaboðin sýnd.

- **Þröskuldur fyrir ekki til á lager** - Þessi gamla talnastilling tekur aðeins gildi ef gildið **Þröskuldur fyrir ekki til á lager** er valið fyrir stillinguna **Birgðastaða byggist á**.

> [!IMPORTANT] 
> Þessar stillingar eru í boði í Dynamics 365 Commerce útgáfu 10.0.12. Ef verið er að uppfæra úr eldri útgáfu af Dynamics 365 Commerce verður að uppfæra appsettings.json-skrána handvirkt. Leiðbeiningar um uppfærslu appsettings.json skrárinnar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Einingar sem nota birgðastillingar

Einingarnar kaupgluggi, óskalisti, verslunarval, karfa og körfutákn nota birgðastillingar til að sýna birgðasviðin og skilaboðin.

Í dæminu á eftirfarandi mynd sýnir PDP lagerskilaboð („Tiltækt“).

![Dæmi um upplýsingasíðu afurðar sem er með skilaboðin á lager.](./media/pdp-InStock.png)

Í dæminu á eftirfarandi mynd sýnir PDP skilaboðin „Ekki til á lager“.

![Dæmi um upplýsingasíðu afurðar sem er með skilaboðin ekki til á lager.](./media/pdp-outofstock.png)

Í dæminu á eftirfarandi mynd sýnir karfa lagerskilaboð („Tiltækt“).

![Dæmi um körfueiningu sem er með skilaboðin til á lager.](./media/cart-instock.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Skilgreina birgðabiðminni og birgðastöðu](inventory-buffers-levels.md)

[Körfueining](add-cart-module.md)

[Kaupgluggaeining](add-buy-box.md)

[Síður og einingar fyrir stjórnun reikninga](account-management.md)

[Eining til að velja verslun](store-selector.md)

[Uppfærslur á SDK og kjarnasafni](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
