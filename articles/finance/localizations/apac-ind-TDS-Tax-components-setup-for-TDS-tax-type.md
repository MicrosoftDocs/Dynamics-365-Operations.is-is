---
title: Setja upp skatthluta fyrir TDS-skattgerðina
description: Þessi grein útskýrir hvernig á að setja upp staðgreiðsluhluti fyrir skatttegundina Tax Deducted at Source (TDS). Það útskýrir einnig hvernig skilgreina á mörkin sem eru notuð til að reikna út TDS fyrir hvern TDS-hluta.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: df2eb10ce9e372bb1e984f6ae1a2e889bbd90ad0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871158"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>Setja upp skatthluta fyrir TDS-skattgerðina

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp staðgreiðsluhluti fyrir skatttegundina Tax Deducted at Source (TDS). TDS-hlutarnir eru TDS, aukagjald, PE-Cess og SHE Cess. Þessi grein útskýrir einnig hvernig á að skilgreina þröskuldinn sem er notaður til að reikna út TDS fyrir hvern TDS íhlut. Auk þess er hægt að skilgreina undantekningamörk sem eru notuð til að reikna út TDS fyrir hvern TDS-hluta.

Fylgið þessum skrefum til að setja upp TDS-hluta.

1. Farið í **Skattur \> Uppsetning \> Staðgreiðsluskattur \> Staðgreiðsluskattshlutar**.

    [![Síða staðgreiðsluskattshluta.](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. Í reitnum **Skattgerð** skal velja **TDS** til að setja upp staðgreiðsluskattshluta fyrir skattgerð TDS.
3. Veldu **Nýtt** á aðgerðasvæðinu til að búa til línu.
4. Í reitnum **Staðgreiðsluskattshluti** skal færa inn heiti fyrir TDS-hluta.
5. Í reitnum **Flokkur staðgreiðsluskattshluta** skal velja flokk staðgreiðsluskattshluta TDS til að hengja TDS-hlutann við.
6. Í flipanum **Almennt**, í reitnum **Lýsing**, skal slá inn lýsingu á TDS einingunni.
7. Á aðgerðasvæðinu skal velja **Mörk** til að opna síðuna **Mörk** þannig að sé hægt að skilgreina mörkin sem eru notuð til að reikna út TDS fyrir TDS-hlutann.
8. Notið reitina **Frá dagsetningu** og **Til dagsetningar** til að skilgreina tímabilið sem mörkin eiga að gilda fyrir.
9. Í flýtiflipann **Almennt**, í reitinn **Mörk**, skal færa inn upphæð marka sem eru notuð til að reikna út TDS fyrir TDS-hlutann. Skatturinn verður dreginn frá upprunanum aðeins þegar uppsöfnuð reikningsupphæð fer yfir mörkin.

    Ef upphæð marka er til dæmis 10.000, þá er TDS reiknað eftir að uppsöfnuð reikningsupphæð fer yfir 10.000 (með öðrum orðum, þegar hún er 10.001 eða hærri).

10. Í reitinn **Undantekningarmörk** skal færa inn upphæð undantekningarmarka sem eru notuð til að reikna út TDS fyrir TDS-hlutann. Skatturinn í reikningslínu verður dreginn frá upprunanum aðeins þegar upphæðin fer yfir undantekningarmörkin.

    Ef til dæmis upphæð undantekningarmarka er 5000, þá er TDS reiknaðu í tiltekinni reikningslínu ef upphæð reikningslínunnar fer yfir 5000 (með öðrum orðum, ef hún er 5001 eða hærri).

    [![Þröskuldssíða.](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > Upphæð undantekningarmarka verður að vera minni en eða jafnt og upphæð marka.
    >
    > Skatturinn er dreginn frá færslu ef færsluupphæðin fer yfir undantekningarmörkin, jafnvel þótt uppsöfnuð reikningsupphæð fer ekki yfir mörkin sem eru tilgreind í reitnum **Mörk**.

11. Lokið síðunni **Mörk** til að fara aftur á síðuna **Staðgreiðsluskattshlutar**.
12. Á aðgerðasvæðinu skal velja **Afrita** til að opna svargluggann **Afrita staðgreiðsluskattshluta** þannig að hægt sé að afrita TDS-hlutana sem voru settir upp fyrir einn flokk TDS-hluta til annars flokks TDS-hluta.
13. Í reitnum **Frá** skal velja flokk TDS-hluta til að afrita TDS-hlutana úr. Í reitnum **Til** skal velja flokk staðgreiðsluskattshluta til að afrita TDS-hlutana í.

    > [!NOTE]
    > Algengir TDS-hlutar sem eru hengdir við báða flokka TDS-hluta eru ekki afritaðir.

14. Veljið **Í lagi** til að afrita og stofna TDS-hluta fyrir hinn flokk TDS-hluta á síðunni **Staðgreiðsluskattshlutar**.

    [![Svargluggi afritunar staðgreiðsluskattshluta.](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Lokið síðunni.
