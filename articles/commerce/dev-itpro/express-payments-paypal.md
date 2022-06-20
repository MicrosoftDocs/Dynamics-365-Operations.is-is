---
title: Skilgreina hraðgreiðslur fyrir PayPal
description: Þessi grein lýsir því hvernig á að stilla hraðgreiðslur fyrir PayPal til að virkja hraðari útgreiðslumöguleika í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b69b7384992fb86370ff6881824a7d2c9a77d2c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905283"
---
# <a name="configure-express-payments-for-paypal"></a>Skilgreina hraðgreiðslur fyrir PayPal

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að stilla hraðgreiðslur fyrir PayPal til að virkja hraðari útgreiðslumöguleika í Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Lykilhugtök

| Hugtak | Lýsing |
|---|---|
| PayPal veski | Upplifun viðskiptavina og samþætting sem er studd af PayPal tenginu. Það er einnig þekkt sem PayPal hnappurinn. |
| Veski | Greiðslutegund sem inniheldur ekki hefðbundna greiðslueiginleika, eins og bankakenninúmer (BIN) svið og gildistíma, sem eru notuð til að greina á milli kredit- og debetkortategunda. |
| Greiðsla tjá | Viðskiptaeining sem styður hraðari greiðsluhegðun þegar studdir greiðslumátar eru notaðir. Þessi grein fjallar um notkun á hraðgreiðslueiningunni með PayPal. |

Dynamics 365 Commerce býður upp á samþættingu úr kassanum fyrir PayPal veski. Þegar Dynamics 365 Payment Connector fyrir PayPal er stillt birtist PayPal hnappurinn sem valinn greiðslumáti við greiðslu á netinu. Þegar notendur velja PayPal er þeim bent á að ganga frá greiðslu beint í gegnum PayPal og er síðan skilað í netverslunina til að ganga frá pöntun sinni. PayPal greiðslukörfu gerir viðskiptavinum kleift að nota greiðslureikningsupplýsingarnar sínar til að fylla út greiðslueyðublaðið fyrirfram, svo að þeir geti klárað greiðsluferlið hraðar.

Commerce hefur bætt við hraðgreiðslueiningu til að auðvelda hraðafgreiðslu. Hægt er að nota hraðgreiðslueininguna í broti sem hægt er að setja á greiðslu- eða körfusíðu. Þegar PayPal er stillt er sama Dynamics 365 Payment Connector fyrir PayPal tengitilvísun notað fyrir bæði hraðgreiðslumöguleikann og venjulega greiðslumöguleikann.

## <a name="paypal-checkout-in-commerce"></a>PayPal útskráning í Commerce

### <a name="prerequisites"></a>Forkröfur

Settu upp PayPal veskið fyrir umhverfið þitt eins og lýst er í [Dynamics 365 greiðslutengi fyrir PayPal](../paypal.md).

Ef þú ert að nota PayPal sem valmöguleika í venjulegu greiðsluflæði (þar sem notendur slá inn reikningsupplýsingar handvirkt án þess að nota flýtiútfyllingaraðgerðir), fylgdu uppsetningarleiðbeiningunum í [Greiðslueining](../payment-module.md).

### <a name="payment-express-module-with-paypal"></a>Hraðgreiðslueining með PayPal

Hraðgreiðslueiningin vinnur með stuðningi við greiðslumáta til að bjóða viðskiptavinum vefsvæðisins möguleika á að skrá sig hraðar með því að fylla út upplýsingar um greiðsluþjónustureikning þeirra á meðan á útskráningu stendur. Hraðgreiðslueiningin notar stillta greiðslutengilinn til að fylla út greiðslueyðublaðið með upplýsingum um notandareikning eins og heimilisfang, tengiliðaupplýsingar og valinn greiðslumáta.

Þegar PayPal hraðafgreiðslu er notað og notandi velur PayPal hnappinn í hraðgreiðsluhluta greiðslusíðunnar, þá er PayPal greiðsla iFrame gluggi er opnaður. Notandinn skráir sig síðan inn á PayPal reikninginn sinn til að nota sendingarfang reikningsins, reikningsfang, netfang og PayPal greiðslumáta að eigin vali til að greiða fyrir færsluna.

Eftir að notandinn lýkur aðgerðinni í PayPal glugganum er honum vísað aftur á verslunarsíðu afgreiðslusíðunnar, þar sem útfyllingareyðublaðið er fyrirfram útfyllt með þeim upplýsingum sem hann valdi. Í hraðgreiðsluflæðinu verður fyrsti afhendingarvalkosturinn sem er í boði fyrir sendingarheimilisfangið sem er skilað fyrirfram útfyllt fyrir notandann. Notandinn hefur þá möguleika á að skoða pöntunina og breyta pöntunarupplýsingum áður en hann velur **Panta** að ganga frá pöntuninni.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>Bættu hraðgreiðslueiningunni með PayPal við brot

Til að bæta hraðgreiðslueiningunni með PayPal við brot í Commerce site builder skaltu fylgja þessum skrefum.

1. Farðu á síðuna þína.
1. Í vinstri yfirlitsrúðunni, veldu **Brot**, og veldu síðan **Nýtt**.
1. Í **Nýtt brot** valmynd, finndu og veldu **Greiðsla tjá** mát og síðan undir **Nafn brots**, sláðu inn nafn fyrir brotið (til dæmis, **Hraðútskráning**).
1. Veldu **Allt í lagi** til að búa til brotið.
1. Í yfirlitsskjánum skaltu velja rauf greiðsluhraðaeiningarinnar sem þú bjóst til.
1. Í eiginleikarúðunni velurðu **Fyrirsögn**.
1. Í **Fyrirsögn** valmynd, í **Texti fyrirsagnar** reit, sláðu inn fyrirsagnartextann sem þú vilt sýna fyrir hraðgreiðsluhlutann á síðunni þinni (til dæmis, **Hraðútskráning**).
1. Undir **Fyrirsagnarstig**, veldu fyrirsagnarstigið (til dæmis, **H2**).
1. Veldu **Í lagi**.
1. Í eiginleikarúðunni, í **Hæð á iFrame** reit, sláðu inn eða stilltu hæðina á iFrame þáttur (td **60**).
1. Í **Stuðlar útboðsgerðir** reit, slá inn **PayPal**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Bættu hraðgreiðslubrotinu við greiðslusíðuna

Fylgdu þessum skrefum til að bæta hraðgreiðslubrotinu við greiðslusíðuna í vefsvæðisgerð.

1. Farðu á síðuna þína.
1. Í vinstri yfirlitsrúðunni, veldu **Síður**, og veldu síðan útskráningarsíðu síðunnar þinnar.
1. Veldu **Breyta** til að breyta síðunni.
1. Í **Aðal** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.

    > [!NOTE]
    > Ef gámaeining sem inniheldur afgreiðslubút er þegar til, færðu hraðgreiðsluhlutann þannig að hann birtist fyrir ofan núverandi afgreiðslugám í **Aðal** rifa. Hraðgreiðsluhlutinn verður síðan sýndur fyrir ofan venjulegan kassagám. Til að færa gámaeiningu upp eða niður skaltu velja sporbaug (**...**), og veldu síðan **Fara upp** eða **Færðu þig niður**.

1. Í **Ílát** eiginleikarúðu, mælum við með að þú stillir eignastillingarnar á eftirfarandi hátt:

    - **Skipulag gáma** – Veldu **Staflað**.
    - **Breidd** – Veldu **Fylltu ílát**.
    - **Börn sýnd** – Veldu **Þrír**.

1. Í **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við broti**.
1. Í **Veldu brot** valmynd, finndu og veldu hraðgreiðslubrotið sem þú bjóst til og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Bættu greiðsluhraðabrotinu við körfusíðuna

Fylgdu þessum skrefum til að bæta hraðgreiðslubrotinu við körfusíðuna í vefsíðugerð.

1. Farðu á síðuna þína.
1. Í vinstri yfirlitsrúðunni, veldu **Síður**, og veldu síðan körfusíðu síðunnar þinnar.
1. Veldu **Breyta** til að breyta síðunni.
1. Í **Aðal** rifa, finndu ílátið sem inniheldur **Karfa** mát. The **Karfa** eining mun innihalda a **Greiðsla tjá** rifa.
1. Veldu **Greiðsla Express** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Greiðsla tjá** mát og veldu síðan **Allt í lagi**.
1. Í eiginleikarúðunni, í **Stuðlar útboðsgerðir** reit, slá inn **Paypal**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

### <a name="modes-of-delivery"></a>Afhendingarmátar

Þegar hraðgreiðslueiningin er stillt til að nota PayPal, verður fyrsti afhendingarvalkosturinn sem er skilaður fyrir sendingarheimilisfangið sem var valið fyrir PayPal reikninginn útfyllt fyrirfram. Notendur munu geta breytt sendingarheimili ef þeir vilja.

Röð afhendingarmáta er stillt í **Afhendingarmátar** kafla fyrir rásina í höfuðstöðvum Commerce. Frekari upplýsingar er að finna í [Setja upp afhendingarmáta](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Afgreiðslueiningin mun einnig nota afhendingarvalkostareininguna þegar afhendingarmátar eru sýndir við útskráningu. Fyrir frekari upplýsingar, sjá [Afhendingarmöguleikaeining](../delivery-options-module.md).

Afhendingarmáti er bætt við listann fyrir netverslun í höfuðstöðvum Commerce. Fara til **Verslun og verslun \> Rásir \> Netverslanir**, og veldu auðkenni rásar fyrir verslunina þína. Veldu síðan **Uppsetning \> Afhendingarmátar**. Afhendingarmátarnir sem sýndir eru í stillingunum munu birtast á svipaðan hátt á síðunni. Til að bæta við eða fjarlægja afhendingarmáta fyrir smásölurás eða vöru skaltu velja **Stjórna afhendingarmátum** á aðgerðasvæðinu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Algengar spurningar um greiðslur](payments-retail.md)

[Greiðsluferliseining](../add-checkout-module.md)

[Greiðslueining](../payment-module.md)

[Setja upp afhendingarmáta](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Afhendingarkostaeining](../delivery-options-module.md)
