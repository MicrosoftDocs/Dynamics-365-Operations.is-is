---
title: Sameina sendingar handvirkt með því að nota síðuna „Sameina sendingar“
description: Þessi grein sýnir atburðarás þar sem margar pantanir eru gefnar út í vöruhúsið og síðan sameinaðar síðar með því að nota síðuna Sameina sendingar.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: d24542a126d64621525f62e694bbc7174b474810
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897343"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Sameina sendingar handvirkt með því að nota síðuna „Sameina sendingar“

[!include [banner](../includes/banner.md)]

Þessi grein sýnir atburðarás þar sem margar pantanir eru gefnar út í vöruhúsið og síðan sameinaðar síðar með því að nota **Sameina sendingar** síðu.

## <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Atburðarásin í þessari grein vísar til gilda og skráa sem eru innifalin í stöðluðum kynningargögnum sem eru veitt fyrir Microsoft Dynamics 365 Supply Chain Management. Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Setja upp samstæðureglur sendingar og afurðarsíur

Aðstæðurnar sem hér er lýst gera ráð fyrir að þegar hafi verið kveikt á eiginleikanum, farið hafi verið í gegnum æfingarnar í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) og reglur og aðrar færslur sem þar er lýst stofnaðar. Gætið þess að gera þessar æfingar áður en haldið er áfram með þessar aðstæður.

## <a name="create-the-sales-orders-for-this-scenario"></a>Búa til sölupantanir fyrir þessar aðstæður

Byrjaðu á því að stofna safn af sölupöntunum sem hægt er að vinna með. Vinna verður með vöruhús sem er virkt fyrir ítarlegt ferli vöruhúsakerfis. Nema annað vöruhús er tilgreint með skýrum hætti verður að nota sama vöruhúsið fyrir hvert eftirtalinna pöntunarsetta.

Opnaðu **Viðskiptakröfur \> Pantanir \> Allar sölupantanir** og búðu til safn sölupantana sem eru með stillingarnar sem lýst er í eftirfarandi undirhlutum.

### <a name="create-sales-orders-1-and-2"></a>Búa til sölupöntun 1 og 2

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-007*
    - **Hópur:** *ShipCons*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

### <a name="create-sales-orders-3-and-4"></a>Búa til sölupöntun 3 og 4

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-007*
    - **Hópur:** – Hafa þennan reit auðan.

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

## <a name="release-the-orders-to-the-warehouse"></a>Losa pantanirnar í vöruhúsið

Fylgdu þessum skrefum til að losa hverja sölupöntun sem þú bjóst til fyrir þessar aðstæður í vöruhúsið.

1. Opna **Viðskiptakröfur \> Pantanir \> Allar sölupantanir**.
1. Finnið og veljið sölupöntun sem á að losa.
1. Á aðgerðasvæðinu, á flipanum **Vöruhús**, skal velja **Aðgerðir \> Losa í vöruhús** til að losa valda sölupöntun.
1. Endurtakið þetta ferli fyrir hverja sölupöntun sem var stofnuð fyrir þessar aðstæður.

## <a name="consolidate-shipments"></a>Sameina sendingar

1. Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.
1. Finnið og veljið sendingu sem var stofnuð þegar sölupöntun 1 var losuð í vöruhúsið. (Reiturinn **Samstæðuregla sendingar** ætti að vera stilltur á *Pöntunarhópur*.)
1. Á aðgerðasvæðinu, á flipanum **Sendingar**, skal velja **Sendingar \> Sameina sendingar**.
1. Staðfestið sendingarnar sem lagðar eru til fyrir sameiningu. Aðeins ætti að mæla með einni sendingu með sömu reglu fyrir sameiningu.
1. Lokið síðunni **Sendingarsamstæða**.
1. Finndu og veldu sendingu sem var stofnuð þegar sölupöntun 3 var losuð í vöruhúsið. (Reiturinn **Samstæðuregla sendingar** ætti að vera stilltur á *Sjálfgefið*.)
1. Á aðgerðasvæðinu, á flipanum **Sendingar**, skal velja **Sendingar \> Sameina sendingar**.
1. Gangið úr skugga um að engar sendingar séu ráðlagðar fyrir sameiningu.
1. Velja **Sýna síur**.
1. Á svæðinu **Síur** skal fjarlægja síuna **Pöntunarnúmer** og velja **Nota**.
1. Staðfestið sendingarnar sem lagðar eru til fyrir sameiningu. Aðeins ætti að mæla með einni sendingu með sömu reglu fyrir sameiningu.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Samstæðureglur sendingar](about-shipment-consolidation-policies.md)
- [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]