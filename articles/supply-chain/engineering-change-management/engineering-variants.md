---
title: Búa til afbrigði fyrir hönnunarafurðir
description: Þessi grein lýsir því hvernig á að búa til afbrigði fyrir verkfræðivörur
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 08feb66dedfa79f5a21a7723a22f3bef883431e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870754"
---
# <a name="generate-variants-for-engineering-products"></a>Búa til afbrigði fyrir hönnunarafurðir

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til afbrigði fyrir verkfræðivörur.

## <a name="turn-variant-generation-for-engineering-products-on-or-off"></a>Kveiktu eða slökktu á framleiðslu afbrigða fyrir verkfræðivörur

Virknin sem lýst er í þessari grein krefst þess að bæði *Verkfræðibreytingastjórnun* og *Afbrigði kynslóð fyrir verkfræðivörur* kveikt er á eiginleikum fyrir kerfið þitt. Fyrir upplýsingar um hvernig á að kveikja eða slökkva á þessum eiginleikum, sjá [Yfirlit yfir verkfræðibreytingastjórnun](product-engineering-overview.md).

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Búa til eitt eða fleiri ný afbrigði af hönnunarafurð

Hægt er að búa til eitt eða fleiri ný afbrigði af afurð án þess að afrita upplýsingar úr fyrirliggjandi afurð. Þetta er gagnlegt þegar þarf að búa til nokkur vöruafbrigði á sama tíma.

Eftirfarandi ferli gefur dæmi um hvernig á að búa til nokkur afbrigði sem innihalda litavíddina.

1. Opnaðu síðuna **Losaðar afurðir** (farðu til dæmis í **Umsjón hönnunarbreytinga \> Almennt \> Útgefnar afurðir**).
1. Á aðgerðasvæðinu skaltu opna flipann **Afurð** og í flokknum **Ný** skal velja **Hönnunarafurð**.
1. **Nýi afurð** glugginn opnast. Veldu viðeigandi **Hönnunarflokkur**.
1. Ef hönnunarflokkur sem inniheldur víddir vöruvíddasamsetningar var valinn geturðu stillt gildi fyrir þær núna. Fyrir þetta dæmi, ef flokkurinn er með víddina **Litur** er hægt að stilla hann á *Bláan*.
1. Veljið aðrar stillingar eftir þörfum. Velja skal **Í lagi** til að stofna afurðina.
1. Afurðin og bláa V-1 afbrigðið eru stofnuð og nýja afurðina opnast.
1. Bæta við uppskriftum og bæta við leiðum á afbrigði eftir þörfum.
1. Á aðgerðasvæðinu skal opna flipann **Afurð** og í flokknum **Afurðarsniðmát** skal velja **Afurðarvíddir**.
1. Síðan **Afurðarvíddir** opnast. Þessi síða inniheldur flipa fyrir hverja tiltæka vídd. Á hverjum flipa skaltu bæta við röð fyrir hvert gildi sem þú munt styðja fyrir hverja viðeigandi vídd. (Í þessu dæmi getur þú bætt við línum í flipann **Litur** fyrir *Hvítt*, *Gult* og *Grænt*).
1. Lokaðu síðunni og veldu síðan **Útgefin afurðarafbrigði**. Taktu eftir að fyrsta afbrigðið sem þú bjóst til (blátt V-1) birtist.
1. Á aðgerðasvæðinu, í flipanum **Afurðarafbrigði**, skal velja **Tillögur um afbrigði**.
1. Í svarglugganum **Tillögur um afbrigði** skal fylgja einu af þessum skrefum:

    - Efst í svarglugganum er hluti fyrir hverja tiltæka vídd. Fyrir hverja vídd skal velja gátreitinn fyrir hvert gildi sem á að búa til tillögu um afbrigði fyrir og síðan velja **Leggja til** á tækjastikunni. Viðeigandi tillögum er bætt við hlutann **Afbrigði sem stungið er upp á**.
    - Veldu **Stinga upp á öllu** á tækjastikunni til að búa til tillögur um afbrigði fyrir allar tiltækar samsetningar af víddargildum. Tillögunum er bætt við hlutann **Afbrigði sem stungið er upp á**.

1. Í hlutanum **Afbrigði sem stungið er upp á** skal velja gátreitinn fyrir hvert afbrigði sem á að búa til. Veldu síðan **Búa til** til að búa til og losa valin afbrigði í hönnunarfyrirtækið. Eftirfarandi skilyrði eiga við:

    - Ekkert af þeim afbrigðum sem búin eru til verða með uppskrift eða leið.
    - Eiginleikar fyrir þessi afbrigði verða sjálfgefnir úr verkfræðiflokknum og verða ekki afritaðir úr fyrra afbrigði.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Búa til afbrigði sem afrit af öðru vöruafbrigði

Hægt er að búa til afbrigði af vöru sem er byggt á öðru vöruafbrigði. Uppskriftin og leiðin frá upprunalegu afurðarafbrigði eru afrituð í nýja afbrigðið. Þetta getur verið gagnlegt fyrir afmarkaðar framleiðsluafurðir þar sem getur reynst hjálplegt að búa til uppskrift sem byggir á fyrstu uppskrift og fylgjast með breytingum úr fyrra afbrigði. Til að viðhalda rekjanleika skráir kerfið hvaða afbrigði var afritað til að búa til nýtt afrit.

Eftirfarandi ferli gefur dæmi um hvernig á að búa til nýtt afbrigði sem inniheldur litavíddina með því að búa til afrit af fyrirliggjandi afbrigði

1. Opnaðu síðuna **Losaðar afurðir** (farðu til dæmis í **Umsjón hönnunarbreytinga \> Almennt \> Útgefnar afurðir**).
1. Á aðgerðasvæðinu skaltu opna flipann **Afurð** og í flokknum **Ný** skal velja **Hönnunarafurð**.
1. **Nýi afurð** glugginn opnast. Veldu viðeigandi **Hönnunarflokkur**.
1. Ef hönnunarflokkur sem inniheldur víddir vöruvíddasamsetningar var valinn geturðu stillt gildi fyrir þær núna. Fyrir þetta dæmi, ef flokkurinn er með víddina **Litur** er hægt að stilla hann á *Bláan*.)
1. Veljið aðrar stillingar eftir þörfum. Velja skal **Í lagi** til að stofna afurðina.
1. Afurðin og bláa V-1 afbrigðið eru stofnuð og nýja afurðina opnast.
1. Bætið við uppskrift og leið í afbrigðið eftir þörfum.
1. Bæta eiginleikum við afurðarafbrigðið eftir þörfum.
1. Bættu bláa V-1 afurðarafbrigðinu við hönnunarbreytingaröð.
1. Stilltu **Áhrif** á *Nýtt afbrigði*.
1. Veldu nýja litagildið (t.d. *Hvítt*). Athugið að eftirfarandi skilyrði eiga við: 
    - Nýja afbrigðið er með uppskrift og leið og hefur verið afritað frá fyrra afbrigði.
    - Nýja afbrigðið hefur eiginleikana afritaða úr fyrra afbrigðinu.
1. Samþykkja breytta pöntun.
1. Meðhöndla breytta pöntun. Eftir að pöntunin er afgreidd verður nýja V-1 afbrigðið búið til og losað í hönnunarfyrirtækið.
