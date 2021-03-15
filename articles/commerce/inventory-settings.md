---
title: Nota birgðastillingar
description: Í efnisatriði er fjallað um birgðastillingar og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 77a3bde12fd047e15d7730903416cdb5263a8cd9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972810"
---
# <a name="apply-inventory-settings"></a>Nota birgðastillingar

[!include [banner](includes/banner.md)]

Í efnisatriði er fjallað um birgðastillingar og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Birgðastillingar tilgreina hvort athuga eigi birgða áður en afurðir eru settar í körfuna. Þær skilgreina einnig birgðatengd skilaboð um smásöluvörur, t.d. „Á lager“ og „Lítið eftir“. Þessar stillingar ganga úr skugga um að ekki sé hægt að kaupa afurð ef hún er ekki til á lager.

Dynamics 365 Commerce leggur mat á lagerstöðu fyrir afurðir. Upplýsingar um hvernig áætlað framboð á lager er reiknað er að finna í [Reikna tiltækar birgðir fyrir smásölurásir](calculated-inventory-retail-channels.md).

Í Commerce-vefssmið er hægt að skilgreina birgðaþröskuld og birgðabil fyrir afurð eða flokk. Það ákvarðar hvort birgðir geti verið flokkaðar sem á lager, lítið til á lager eða ekki til á lager. Frekari upplýsingar er að finna í [Stilla birgðabiðminni og birgðastöðu](inventory-buffers-levels.md).

> [!NOTE]
> Stuðningur við birgðaþröskulda og svið er tiltækur í Dynamics 365 Commerce útgáfu 10.0.12.

## <a name="inventory-settings"></a>Birgðastillingar

Í Commerce eru birgðastillingar skilgreindar í **Stillingar svæðis \> Viðbætur \> Birgðastjórnun** í svæðissmið. Til eru fjórar birgðastillingar en ein þeirra er úreld:

- **Virkja birgðaathugun í forriti** – Þessi stilling kveikir á birgðaathugun afurðar. Einingarnar kaupgluggi og sækja í verslun athuga þá birgðir afurðar og leyfa að afurð sé bætt í körfuna aðeins ef birgðir eru til staðar.
- **Birgðastaða byggir á** – Þessi stilling skilgreinir hvernig birgðastöður eru reiknaðar. Tiltæk gildi eru **Samtals tiltækt**, **Efnislegt magn tiltækt** og **Þröskuldur fyrir ekki til á lager**. Í Commerce er hægt að skilgreina birgðaþröskuld og birgðabil fyrir hverja afurð og flokk. API-birgðir skila birgðaupplýsingum um afurð fyrir bæði eiginleikann **Samtals tiltækt** og **Efnislegt magn tiltækt**. Smásöluaðilinn ákveður hvort nota eigi **Samtals tiltækt** eða **Efnislegt magn tiltækt** til að ákvarða birgðatalninguna og samsvarandi bil fyrir „til á lager“ og „ekki til á lager“ stöðurnar.

    Gildið **Þröskuldur fyrir ekki til á lager** í stillingunni **Birgðastaða byggir á** er gamalt, úrelt gildi. Þegar það er valið er birgðatalningin ákvörðuð út frá niðurstöðum gildisins **Samtals tiltækt**, en þröskuldurinn er skilgreindur af talnastillingunni **Þröskuldur fyrir ekki til á lager** sem er útskýrð seinna. Þessi þröskuldsstilling á við um allar afurðir á svæði rafrænna viðskipta. Ef birgðir eru undir þröskuldstölunni er litið á að afurð sé ekki til á lager. Annars er það talið til á lager. Möguleikar gildisins **Þröskuldur fyrir ekki til á lager** eru takmarkaðir og ekki er mælt með því að það sé notað í útgáfu 10.0.12 eða síðar.

- **Birgðasvið** – Þessi stilling skilgreinir birgðasviðin sem skilaboð eru sýnd fyrir í einingum svæðis. Það gildir aðeins ef annaðhvort gildið **Samtals tiltækt** eða gildið **Efnislegt magn tiltækt** er valið fyrir stillinguna **Birgðastaða byggist á**. Tiltæk gildi eru **Allt**, **Litlar birgðir og ekki til á lager** og **Ekki til á lager**.

    - Þegar **Allt** er valið verða skilaboð fyrir öll birgðasvið, frá á lager („Til á lager“ skilaboð) til ekki til á lager („Ekki til á lager“ skilaboð) sýnd.
    - Þegar **Litlar birgðir og ekki til á lager** er valið verða skilaboð fyrir öll birgðasvið, nema á lager („Til á lager“ skilaboð) sýnd.
    - Þegar **Ekki til á lager** er valið verður aðeins „Ekki til á lager“ skilaboðin sýnd.

- **Þröskuldur fyrir ekki til á lager** - Þessi gamla talnastilling tekur aðeins gildi ef gildið **Þröskuldur fyrir ekki til á lager** er valið fyrir stillinguna **Birgðastaða byggist á**.

> [!IMPORTANT] 
> Þessar stillingar eru í boði í Dynamics 365 Commerce útgáfu 10.0.12. Ef verið er að uppfæra úr eldri útgáfu af Dynamics 365 Commerce verður að uppfæra appsettings.json-skrána handvirkt. Leiðbeiningar um uppfærslu appsettings.json skrárinnar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Einingar sem nota birgðastillingar

Einingarnar kaupgluggi, óskalisti, verslunarval, karfa og körfutákn nota birgðastillingar til að sýna birgðasviðin og skilaboðin.

Eftirfarandi mynd sýnir dæmi um upplýsingasíðu afurðar sem sýnir á lager („Tiltækt“) skilaboðin.

![Dæmi um upplýsingasíðu afurðar sem er með skilaboðin á lager](./media/pdp-InStock.png)

Eftirfarandi mynd sýnir dæmi um upplýsingasíðu afurðar sem sýnir „ekki til á lager“ skilaboðin.

![Dæmi um upplýsingasíðu afurðar sem er með skilaboðin ekki til á lager](./media/pdp-outofstock.png)

Eftirfarandi mynd sýnir dæmi um körfu sem sýnir skilaboðin til á lager („Tiltækt“).

![Dæmi um körfueiningu sem er með skilaboðin til á lager](./media/cart-instock.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Skilgreina birgðabiðminni og birgðastöðu](inventory-buffers-levels.md)

[Körfueining](add-cart-module.md)

[Kaupgluggaeining](add-buy-box.md)

[Síður og einingar fyrir stjórnun reikninga](account-management.md)

[Eining til að velja verslun](store-selector.md)

[Uppfærslur á SDK og kjarnasafni](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]