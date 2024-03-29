---
title: Stofnun sjálfvirks viðskiptavinar
description: Þessi grein lýsir því hvernig á að búa til sjálfgefna viðskiptavin til að nota þegar rás er búin til í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 79e145c21be9178622b7c105afefecb78062e3b5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273586"
---
# <a name="create-a-default-customer"></a>Stofnun sjálfvirks viðskiptavinar

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til sjálfgefna viðskiptavin til að nota þegar rás er búin til í Microsoft Dynamics 365 Commerce.

Þegar þú býrð til rás þarftu að bjóða upp á sjálfgefinn viðskiptavin. Auðvelt er að búa til sjálfgefinn viðskiptavin eftir að hafa búið til viðskiptavinahópinn og aðsetursbók viðskiptavinarins.

## <a name="create-a-customer-group"></a>Viðskiptavinaflokkur stofnaður

Ef engir viðskiptavinahópar hafa verið búnir til geturðu búið til einn. Dæmi geta verið hópar til að tákna mismunandi viðskiptavinahópa, svo sem heildsölu, smásölu, internet, starfsmenn, osfrv.

Til að stofna viðskiptavinaflokk, skal fylgja eftirfarandi skrefum.

1. Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Viðskiptavinir \> Viðskiptavinaflokkar**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitnum **Viðskiptavinaflokkur** slærðu inn kenni viðskiptavinahópsins.
1. Í reitinn **Lýsing** ritarðu viðeigandi lýsingu.
1. Í reitinn **Greiðsluskilmálar** ritarðu viðeigandi gildi.
1. Í reitinn **Tími milli gjalddaga reiknings og greiðsludags** slærðu inn viðeigandi gildi.
1. Í reitinn **Sjálfgefinn skattahópur** slærðu inn skattahóp ef við á.
1. Veldu gátreitinn **Verð eru með virðisaukaskatti** ef við á.
1. Í reitinn **Sjálfgefin ástæða afskrifta** slærðu inn viðeigandi gildi, ef við á.

Eftirfarandi mynd sýnir nokkra stillta viðskiptavinahópa.

![Viðskiptavinaflokkar.](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Stofna aðsetursbók viðskiptavinar

Viðskiptavinur þarf að tengjast heimilisfangaskrá. Ef hún hefur ekki enn verið stofnuð verður þú að stofna hana.

Til að stofna aðsetursbók viðskiptavina skal fylgja eftirfarandi skrefum.

1. Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Aðsetursbækur**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitnum **Heiti** færirðu inn heiti.
1. Í reitinn **Lýsing** skal færa inn lýsingu.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir dæmi um aðsetursbók.

![Aðsetursbók.](media/address-book.png)

## <a name="create-a-default-customer"></a>Stofnun sjálfvirks viðskiptavinar

Til að stofna sjálfgefinn viðskiptavin skal fylgja eftirfarandi skrefum.

1. Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Viðskiptavinir \> Allir viðskiptavinir**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í fellilistanum **Gerð** velurðu „Einstaklingur”.
1. Í fellilistanum **Viðskiptavinalykill** velurðu eða slærð inn lykilnúmer (til dæmis „100001“).
1. Í fellilistanum **Fornafn** velurðu eða slærð inn nafn (til dæmis „Sjálfgefið“).
1. Í fellilistanum **Miðnafn** velurðu eða slærð inn nafn (til dæmis „Retail“).
1. Í fellilistanum **Eftirnafn** velurðu eða slærð inn nafn (til dæmis „Customer“).
1. Í fellilistanum **Gjaldmiðill** velurðu eða slærð inn gjaldmiðil (til dæmis „USD“).
1. Í fellivalmyndinni **Gjaldmiðill** velurðu þann hóp viðskiptavina sem áður var stofnaður.
1. Í fellilistanum **Aðsetursbækur** velurðu fyrirliggjandi aðsetursbók viðskiptavina.
1. Veldu **Vista** til að vista og fara aftur á upplýsingaskjá viðskiptavina fyrir nýja viðskiptavininn.

> [!NOTE]
> Það er ekki nauðsynlegt að bæta við heimilisfangi fyrir sjálfgefinn viðskiptavin.

Eftirfarandi mynd sýnir dæmi um stofnun viðskiptavinr.

![Stofnun sjálfvirks viðskiptavinar.](media/default-customer-creation.png)

Eftirfarandi mynd sýnir sjálfgefna stillingu viðskiptavina.

![Dæmi um stillingu viðskiptavinar.](media/default-customer-configuration1.png)

Flest sjálfgefin gildi á skjá viðskiptavinarins geta verið áfram, en tveimur gildum ætti að breyta.

1. Stækkaðu á upplýsingaskjá viðskiptavinarins **Sjálfgefin sölupöntun**.
1. Í fellilistanum **Vefsvæði** velurðu eða slærð inn fyrirframstillta síðu.
1. Í fellilistanum **Vöruhús** velurðu eða slærð inn fyrirframstillt vöruhús.

Eftirfarandi mynd sýnir dæmi um stillingu viðskiptavinr.

![Dæmi um stillingu viðskiptavinar.](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit rása](channels-overview.md)

[Skilyrði fyrir uppsetningu rásar](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
