---
title: Stilltu Google Pay með Adyen
description: Þessi grein lýsir því hvernig á að stilla Google Pay með Adyen í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c3f049946c66fcd8560f7c08a4cb2beab0dcd5b2
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2022
ms.locfileid: "9115014"
---
# <a name="configure-google-pay-with-adyen"></a>Stilltu Google Pay með Adyen

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að stilla Google Pay með Adyen í Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce býður upp á samþættingu úr kassanum fyrir Google Pay þegar Adyen greiðslugáttarþjónustan er notuð. Google Pay er greiðslumáti með stafrænu veski sem notar Google Pay söluaðilareikning í samráði við Adyen greiðsluþjónustuna. Þegar hann er stilltur er Google Pay hnappurinn tiltækur sem valinn greiðslumáti við greiðslu á netinu. Þegar notendur velja **Google Pay** í studdum vafra eða tæki er þeim bent á að ganga frá greiðslu beint með Google Pay þjónustunni. Þeim er síðan skilað í netverslunina til að ljúka pöntuninni.

Þegar Google Pay er notað með hraðgreiðslueiningunni í Commerce eru greiðslureikningsupplýsingar notandans sjálfkrafa útfylltar á greiðsluformið til að hjálpa notandanum að komast hraðar í gegnum greiðsluferlið. Viðskipti fela í sér hraðgreiðslueiningu sem gerir hegðun með hraðgreiðslum kleift. Hægt er að nota hraðgreiðslueininguna í broti sem er innifalið á kassa- eða körfusíðunni. Tilvísun Dynamics 365 Payment Connector fyrir Google Pay tengi er notað til viðbótar við Dynamics 365 Payment Connector fyrir Adyen til að virkja bæði flýtigreiðslu og venjulegt greiðsluval þegar PayPal er stillt. Google Pay er einnig hægt að stilla með Adyen greiðslustöðvum og Commerce Point of Sale (POS) til notkunar í verslun.

## <a name="key-terms"></a>Lykilhugtök

| Hugtak | Lýsing |
|---|---|
| Google Pay | Einnig þekktur sem Google Pay „hnappurinn“, Google Pay er veskisgreiðslutilboð sem er stutt í gegnum Adyen tengið. Það gerir upplifun viðskiptavina og samþættingu kleift sem er studd af Dynamics Google Pay tengi. |
| Veski | Greiðslutegund sem inniheldur ekki hefðbundna greiðslueiginleika, svo sem svið bankaauðkennisnúmers (BIN) og gildistíma sem eru notuð til að greina á milli kredit- og debetkortategunda. |
| Greiðsla hraðaeining | A Dynamics 365 Commerce eining sem styður hraðari greiðsluhegðun með studdum greiðslumáta. |

## <a name="prerequisites"></a>Forkröfur

Notkun Google Pay með Adyen í viðskiptum krefst Google Merchant reiknings. Fyrir upplýsingar um hvernig á að setja upp Google Merchant reikninginn þinn, sjáðu [Adyen skjöl á Google Pay](https://docs.adyen.com/payment-methods/google-pay/) og Google [Gátlisti fyrir samþættingu](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist).

Google Pay greiðslumáti verður einnig að vera samþættur Adyen reikningnum þínum. Fyrir leiðbeiningar um samþættingu tengla, sjá [Adyen Google Pay](https://www.adyen.com/payment-methods/google-pay).

Þú verður líka að virkja aukna veskisaðgerðina inn Dynamics 365 Commerce höfuðstöðvar. Fara til **Vinnurými \> Eiginleikastjórnun**, leitaðu að **Aukinn stuðningur við veski og endurbætur á greiðslum** eiginleiki, veldu eiginleikann og veldu síðan **Virkja**. Eftir að aðgerðin hefur verið virkjað skaltu keyra **1110** dreifingaráætlun til að gera breytinguna aðgengilega á öllum rásum.

## <a name="map-the-google-pay-payment-method"></a>Kortaðu Google Pay greiðslumátann

Google Pay er greiðslumáti með stafrænu veski. Fyrir upplýsingar um hvernig á að setja upp greiðslukortlagningu fyrir Google Pay, sjá [Greiðslustuðningur fyrir veski](../wallets.md).

Fylgdu þessum skrefum til að kortleggja greiðslumáta Google Pay við kortaútboðstegundir fyrir bæði POS og netrásir.

1. Í höfuðstöðvum viðskipta, farðu til **Verslun og verslun \> Rásaruppsetning \> Greiðslumáta \> Tegundir korta**.
1. Veldu **Nýtt** til að bæta við línu fyrir Google Pay.
1. Í **auðkenni** reit, slá inn **GooglePay**.
1. Í **Rafræn greiðsluheiti** reit, slá inn **Google Pay**.
1. Í **Tegund** reit, slá inn **Veski**.
1. Í **Útgefandi** reit, slá inn **Google**.
1. Á aðgerðarrúðunni velurðu **Kortlagning örgjörva** að opna **Greiðslukortlagningaraðferðir örgjörva** valmynd.
1. Undir **Ókortlagðar greiðslumáta örgjörva**, muntu sjá lista yfir ókortlagða greiðslumáta örgjörva, sem hver um sig er paraður við viðeigandi tengi. Fylgdu þessum skrefum fyrir hverja kortaútboðstegund til að kortleggja ókortlagða greiðslumáta Google Pay örgjörva við kortaútboðsgerðir:

    1. Undir **Tegundir kortaútboðs**, veldu kortaútboðstegund.
    1. Í **Ókortlagðar greiðslumáta örgjörva** dálk, veldu bæði **Dynamics 365 greiðslutengi fyrir Adyen** tengi (til notkunar á POS) og **Dynamics 365 greiðslutengi fyrir Google Pay** tengi (til notkunar í netrásum).
    1. Veljið **Bæta við**. Úrvalið er bætt við **Kortlagðar greiðslumáta örgjörva** dálki.

1. Þegar þú hefur lokið við að kortleggja greiðslumáta skaltu velja **Vista**.
1. Á **Tegundir korta** síðu, veldu **Vista**.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Stilltu Commerce netverslun fyrir Google Pay

Til að stilla Commerce netverslun til að nota Google Pay skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum viðskipta, farðu til **Verslun og verslun \> Rásir \> Netverslanir**.
1. Veldu rás netverslunar síðunnar þinnar með því að velja rásina **Auðkenni smásölurásar** gildi.
1. Á **Greiðslureikningar** Flýtiflipi, undir **Tengi**, staðfesta að **Dynamics 365 greiðslutengi fyrir Adyen** tengi er skráð. Ef það er ekki skráð skaltu fylgja leiðbeiningunum í [Settu upp Dynamics 365 Payment Connector fyrir Adyen](adyen-connector-setup.md) að bæta því við.

    > [!NOTE]
    > Í flestum tilfellum er **Dynamics 365 greiðslutengi fyrir Adyen** tengi verður að vera skráð sem fyrsta tengið fyrir rásina þína (fyrsta tengið er einnig þekkt sem aðaltengi). Því næst verða önnur tengi sem notuð verða, svo sem **Dynamics 365 greiðslutengi fyrir PayPal** og **Dynamics 365 greiðslutengi fyrir GooglePay** tengi.

1. Eftir **Dynamics 365 greiðslutengi fyrir Adyen** tengi hefur verið bætt við, veldu **Bæta við** að bæta við **Dynamics 365 greiðslutengi fyrir GooglePay** tengi. Stilltu síðan eftirfarandi eiginleika fyrir tengið.

    | Reitur                  | Lýsing | Áskilið | Sjálfkrafa stillt | Sýnisgildi |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Samsetningarheiti          | Heiti samsetningar fyrir Dynamics 365 Payment Connector fyrir GooglePay. | Já | Já | *Tvöfaldur nafn* |
    | Kenni þjónustureiknings     | Einkvæmt auðkenni fyrir uppsetningu sölueiginleika. Þetta auðkenni er stimplað á greiðslufærslur og auðkennir sölueiginleikana sem eftirvinnsluferli (eins og reikningagerð) ættu að nota. | Já | Já | *GUID* |
    | Google söluauðkenni     | Sláðu inn Google Merchant ID sem er úthlutað á Google Merchant reikninginn þinn. Þessi eiginleiki er nauðsynlegur fyrir framleiðsluumhverfi en er valfrjáls fyrir prófunarumhverfi. Fyrir frekari upplýsingar, heimsækja <https://pay.google.com/>. | Já | Nr. | *Tölulegt auðkenni* |
    | Kenni lykils söluaðila    | Sláðu inn einstakt Adyen kaupmannsauðkenni. Þetta gildi er gefið upp þegar þú skráir þig hjá Adyen eins og lýst er í [Skráðu þig hjá Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Já | Nr. | *Söluauðkenni* |
    | API lykill í skýinu          | Sláðu inn Adyen Cloud API lykilinn. Til að fá þennan lykil skaltu fylgja leiðbeiningunum í [Hvernig á að sækja API lykilinn](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Já | Nr. | "abcdefg" |
    | Umhverfi gáttar    | Adyen hlið umhverfið til að kortleggja. Möguleg gildi eru **Próf** og **Lifa**. Þú ættir að stilla þennan reit á **Lifa** aðeins fyrir framleiðslutæki og viðskipti. | Já | Já | "Lifa" |
    | Studdir gjaldmiðlar   | Gjaldmiðlar sem tengið ætti að vinna úr. Í kortatilvikum getur Adyen stutt fleiri gjaldmiðla í gegnum [Dynamic gjaldmiðlaviðskipti](https://www.adyen.com/pos-payments/dynamic-currency-conversion) eftir að viðskiptabeiðnin er send í greiðslustöðina. Hafðu samband við þjónustudeild Adyen til að fá lista yfir studda gjaldmiðla. | Já | Já | "USD;EUR" |
    | Studdir greiðslumátar | Útboðsgerðirnar sem tengið á að vinna úr. | Já | Já | „GooglePay“ |

1. Eftir að þú hefur lokið við að stilla eiginleika tengisins skaltu keyra **1070 (Rásarstillingar**) dreifingaráætlunarstarf.

## <a name="configure-commerce-pos-for-google-pay"></a>Stilltu Commerce POS fyrir Google Pay

POS stillingin notar stillingar vélbúnaðarsniðsins **EFT þjónusta** reit fyrir Dynamics 365 Payment Connector fyrir Adyen. Fyrir upplýsingar um hvernig á að stilla rafræna millifærsluþjónustu (EFT) fyrir Dynamics 365 Payment Connector fyrir Adyen í höfuðstöðvum Commerce, sjá [Settu upp Dynamics 365 POS vélbúnaðarprófílhluta](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Örgjörvakortlagningin fyrir Adyen tengið fangar veskiskortategundirnar sem Google Pay notar í POS-útstöðinni.

### <a name="use-the-payment-express-module-with-google-pay"></a>Notaðu hraðgreiðslueininguna með Google Pay

Commerce greiðsluhraðseiningin vinnur með stuðningi við greiðslumáta til að gefa viðskiptavinum vefsvæðisins möguleika á að skrá sig hraðar með því að nota greiðsluþjónustureikningsupplýsingarnar þeirra á meðan á greiðsluferlinu stendur. Hraðgreiðslueiningin vísar í stillta tengihnappinn og skilar notandavöldum pöntunarupplýsingum (heimilisfang, tengiliðaupplýsingar og greiðslumáta) til að forfylla útgreiðslueyðublaðið.

Þegar hraðgreiðslueiningin er notuð með Google Pay, ef viðskiptavinir velja Google Pay hnappinn í **Greiðsla Express** kafla er Google Pay iframe glugginn opnaður. Notendur geta síðan skráð sig inn á Google reikninginn sinn til að nota sendingarheimilisfang, reikningsfang, netfang og valinn Google Pay greiðslumáta til að greiða fyrir færsluna.

Þegar notendur ljúka við aðgerðina í Google Pay glugganum er þeim vísað á útskráningarsíðu viðskiptasíðunnar, þar sem útfyllingareyðublaðið er fyrirfram útfyllt með Google Pay reikningsupplýsingum þeirra. Eftir að notendur fara aftur á greiðslusíðuna úr Google Pay glugganum munu þeir sjá eftirfarandi upplýsingar:

- Í hraðgreiðsluflæðinu verður fyrsti afhendingarvalkosturinn sem er í boði fyrir sendingarheimilisfangið sem var skilað forvalinn fyrir viðskiptavininn.
- Þegar Google Pay er notað er engu tengiliðanetfangi skilað. Notendur gestaútritunar verða að slá inn netfang í tengiliðahlutanum á útskráningarsíðunni. Innskráðir notendur munu sjálfkrafa fylla út tengiliðagögnin af Dynamics viðskiptavinareikningnum sínum (aðalnetfangið sem þeir notuðu til auðkenningar).

Viðskiptavinir hafa möguleika á að skoða pantanir og breyta pöntunarupplýsingum áður en þeir velja **Panta** að ganga frá pöntuninni.

### <a name="configure-google-pay-in-site-builder"></a>Stilltu Google Pay í vefsíðugerð 

Áður en þú stillir brotin þín eða síður með Google Pay þarftu að tryggja að öryggisstefnur þínar fyrir síðuna þína séu stilltar í Commerce site builder.

Fylgdu þessum skrefum til að tryggja að öryggisstefnur þínar fyrir efni séu settar í vefsvæðisgerð.

1. Á síðunni þinni skaltu fara á **Vefstillingar \> Framlengingar**.
1. Á **Innihaldsöryggisstefna** flipa, bæta við línu fyrir`*.google.com` til **barn-src**, **-src**, **-forfeður**, **-src**, **-src**, **-src**, og **style-src** tilskipunum.
1. Þegar þú hefur lokið skaltu velja **Vista og birta**.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Stilltu hraðgreiðslubrotið með Google Pay í vefsvæðisgerðinni

Til að setja upp hraðgreiðslubrotið með Google Pay fyrir netverslunina skaltu fylgja þessum skrefum.

1. Í Site Builder, farðu á **Brot**.
1. Veljið **Nýtt**.
1. Í **Nýtt brot** valmynd, veldu **Ílát** mát, sláðu inn heiti brota (til dæmis, **Hraðútskráning**), og veldu síðan **Allt í lagi**. 
1. Veldu nýja brotið **Sjálfgefinn gámur** rifa.
1. Í eiginleikarúðunni til hægri, stilltu eiginleikana fyrir gámaeininguna:

    - **Fyrirsögn** – Sláðu inn fyrirsögn til að birta fyrir hraðgreiðsluhlutann á síðunni þinni (til dæmis, **Hraðútskráning**).
    - **Skipulag gáma** – Veldu **Flæði**.
    - **Breidd** – Veldu **Fylltu ílát**.
    - **Börn sýnd** – Veldu **Þrír** til að tilgreina fjölda barna sem passa í röð hraðgreiðsluhluta greiðslusíðunnar (til dæmis textareit, hraðgreiðslu fyrir PayPal og hraðgreiðslu fyrir Google Pay).
    - **CSS nafn bekkjar** - Koma inn **msc-express-greiðslugámur** (nauðsynlegt).

    > [!IMPORTANT]
    > - The **CSS nafn bekkjar** gildi verður að vera stillt á **msc-express-greiðslugámur** til að stjórna hegðun gámsins við útskráningu. Þessi hegðun felur í sér að fela, falla saman og aðrar aðgerðir sem eiga við hraðgreiðsluhlutann á meðan á greiðsluflæði stendur. The **msc-express-greiðslugámur** flokkur vinnur með sjálfgefnum aðgerðum sem eru gefnar út með útskráningareiningunni fyrir einingasafnið.
    > - Fleiri stílar geta verið með á móti **CSS nafn bekkjar**. Ef þú sérsniður hegðun einingarinnar skaltu athuga stílstýringarnar ef þú ert að nota sömu einingabókasafnskóðaða hegðun í afgreiðslueiningunni fyrir hraðgreiðsluhegðun.

1. Í **Sjálfgefinn gámur** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Greiðsla tjá** mát og veldu síðan **Allt í lagi**.
1. Í **Greiðsla tjá** mátareiginleikarúðu, stilltu eða stilltu **Hæð á iFrame** gildi í punktum (til dæmis, **60**).
1. Í **Stuðlar útboðsgerðir** reit, slá inn **GooglePay**. Gildið verður að passa við **Stuðlar útboðsgerðir** streng í tenginu sem er sett upp fyrir rásina (eins og lýst er í [Stilltu Commerce netverslun fyrir Google Pay](#configure-a-commerce-online-store-for-google-pay) kafla fyrr í þessari grein).

    > [!NOTE]
    > Þú getur endurtekið skref 6 til 9 til að bæta við **Greiðsla tjá** einingar fyrir aðra greiðslumáta. Samræma **Stuðlar útboðsgerðir** gildi með viðbótar stilltum greiðslutegundum (til dæmis, **Paypal**).

1. Valfrjálst: Þú getur bætt textablokkareiningu við sjálfgefna gámaeiningu til að innihalda leiðbeiningar eða upplýsingagjöf. Eftir að þú hefur bætt við einingunni skaltu slá inn viðeigandi texta í eiginleikaglugganum **Ríkur texti** sviði. Þú getur staðsetja textann fyrir ofan eða fyrir neðan greiðsluhraðaeiningarnar með því að velja sporbaug (**...**) í **Textablokk** rauf og velur síðan **Fara upp** eða **Færðu þig niður**.
1. Veldu **Vista** til að vista breytingarnar og veldu síðan **Ljúktu við klippingu**.
1. Veldu **Birta** að birta brotið.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Bættu hraðgreiðslubrotinu við greiðslusíðuna

Fylgdu þessum skrefum til að bæta hraðgreiðslubrotinu við greiðslusíðuna.

1. Í Site Builder, farðu á **Síður**, og veldu síðan útskráningarsíðu síðunnar þinnar.
1. Veljið **Breyta**.
1. Í **Aðal rauf**, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Í eiginleikarúðunni til hægri, stilltu eiginleikana fyrir gámaeininguna:

    - **Skipulag gáma** – Veldu **Staflað**.
    - **Breidd** – Veldu **Fylltu ílát**.
    - **Börn sýnd** – Veldu **Þrír** til að tilgreina fjölda barna sem passa í röð hraðgreiðsluhluta greiðslusíðunnar (til dæmis textareit, hraðgreiðslu fyrir PayPal og hraðgreiðslu fyrir Google Pay).

1. Í **Ílát** mát rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við broti**.
1. Í **Veldu brot** valmynd, veldu hraðgreiðslubrotið sem þú bjóst til og veldu síðan **Allt í lagi**.
1. Veldu **Vista** til að vista breytingarnar og veldu síðan **Ljúktu við klippingu**.
1. Veldu **Birta** að birta síðuna.

> [!NOTE]
> Ef greiðslusíðan inniheldur nú þegar gám sem hefur greiðslubrotið, og þú vilt að greiðsluhraðareiningin sé birt fyrir ofan venjulegan greiðslugám, geturðu staðsett hana fyrir ofan eða neðan núverandi greiðslu með því að velja sporbaug (**...**) í **Aðal rauf**, og velur síðan **Fara upp** eða **Færðu þig niður**.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Bættu greiðsluhraðabrotinu við körfusíðuna

Til að bæta greiðsluhraðabrotinu við körfusíðuna skaltu fylgja þessum skrefum.

1. Í Site Builder, farðu á **Síður**, og veldu síðan körfusíðu síðunnar þinnar.
2. Veljið **Breyta**.
3. Í yfirlitsskjánum skaltu stækka **Aðal rauf** í tréskjánum og finndu ílátið sem inniheldur **Karfa** mát.
4. Í **Karfa** mát, veldu **Greiðsla Express** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
5. Í **Veldu einingar** valmynd, veldu **Greiðsla tjá** mát og veldu síðan **Allt í lagi**.
6. Veldu **Greiðsla tjá** mát rauf. Síðan, í eiginleikarúðunni til hægri, undir **Stuðlar útboðsgerðir**, koma inn **GooglePay**. Gildið verður að passa við **Stuðlar útboðsgerðir** streng í tenginu sem var sett upp fyrir rásina (eins og lýst er í [Stilltu Commerce netverslun fyrir Google Pay](#configure-a-commerce-online-store-for-google-pay) kafla fyrr í þessari grein).
1. Veldu **Vista** til að vista breytingarnar og veldu síðan **Ljúktu við klippingu**.
1. Veldu **Birta** að birta síðuna.

Notendur geta innihaldið allt að þrjá studda **Greiðsla Express** einingar (með öðrum orðum, þrír tiltækir studdir greiðslumöguleikar) í körfunni **Greiðsla Express** rifa.

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Settu upp Google Pay sem valkost í greiðsluhlutanum fyrir greiðslu

Þú getur sett upp Google Pay sem valmöguleika í hlutanum fyrir greiðslugreiðslur fyrir greiðslu eingöngu, ekki hraða virkni. Afgreiðslueyðublaðið verður fyllt út af notanda og Google Pay greiðslusíðan mun aðeins gera útgreiðsluna tilbúna til greiðslu með Google Pay. Engar Google reikningsupplýsingar verða notaðar til að skrifa yfir útfylltar upplýsingar um útskráningu.

> [!NOTE]
> Eftirfarandi aðferð gerir ráð fyrir að vefsíðan þín noti stöðvunarbrot sem er stillt með afhendingarupplýsingum, sendingarfangi, afhendingarvalkostum, tengiliðaupplýsingum, valfrjálsum skilmálum og skilyrðum og hluta fyrir greiðsluþætti. Sjálfgefin útskráningareining bókasafns er gefin út með afgreiðsluhlutaíláti sem hefur textablokk, vildarpunkta, gjafakort og greiðslueiningar. Fyrir frekari upplýsingar, sjá [Greiðslueining](../payment-module.md).

Til að setja upp Google Pay sem venjulegan greiðslumöguleika í **Greiðslumáti** hluta afgreiðslusíðunnar skaltu fylgja þessum skrefum.

1. Í Site Builder, farðu á **Brot**, og veldu síðan útskráningarbrot vefsvæðisins þíns.
1. Veljið **Breyta**.
1. Í **Upplýsingar um úttekt** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Greiðsla** mát og veldu síðan **Allt í lagi**.
1. Í **Greiðsla** Eiginleikarúðu einingarinnar til hægri, stilltu eiginleikana fyrir gámaeininguna:

    - **Fyrirsögn** – Sláðu inn fyrirsögn til að birta fyrir hraðgreiðsluhlutann á síðunni þinni (til dæmis, **Google Pay**).
    - **Hæð á iFrame** - Breyttu gildinu í valinn hönnunarhæð í punktum (til dæmis, **75**). 
    - **Stuðlar útboðsgerðir** - Koma inn **GooglePay** til að passa við uppsetninguna fyrir Google Pay tengið í höfuðstöðvum Commerce.
    - **Er frumgreiðsla** – Skildu eftir gátreitinn. (Þessi eign er venjulega virkjuð fyrir Adyen útskráningareininguna.)
    - **Hnekkt greiðslustíl** – Þessi eign er ekki studd fyrir Google Pay stillingar.
    - **Notaðu auðkenni tengis** – Þessi eign verður að vera valin ef mörg greiðslutengi eru notuð á síðunni.

1. Settu eininguna fyrir ofan eða fyrir neðan aðrar greiðslueiningar með því að velja sporbaug (**...**) í **Greiðsla** rauf og velur síðan **Fara upp** eða **Færðu þig niður**.
1. Veldu **Vista** til að vista breytingarnar og veldu síðan **Ljúktu við klippingu**.
1. Velja **Birta**.

### <a name="modes-of-delivery"></a>Afhendingarmátar

Með hraðgreiðslueiningunni sem notar Google Pay verður fyrsti afhendingarvalkosturinn sem er skilaður á móti völdum sendingarheimilisfangi af Google Pay reikningnum forvalinn. Notendur hafa tækifæri til að breyta sendingarheimilisfanginu í annan valkost ef þeir vilja.

Röð þar sem afhendingaraðferðir eru sýndar í hraðgreiðslueiningunni er stillt á rásinni **Afhendingarmátar** síðu í höfuðstöðvum Commerce. Í höfuðstöðvum viðskipta, farðu til **Verslun og verslun \> Rásir \> Netverslanir**, og veldu **Auðkenni smásölurásar** gildi fyrir verslunina þína. Á aðgerðarrúðunni, á **Uppsetning** flipa, veldu **Afhendingarmátar**. Afhendingarmátarnir sem eru skráðir munu birtast í sömu röð í hraðgreiðslueiningunni. Veldu **Stjórna afhendingarmátum** á aðgerðarrúðunni til að bæta við eða fjarlægja afhendingarmáta fyrir smásölurás eða vöru. Fyrir frekari upplýsingar um hvernig á að setja upp afhendingarmáta, sjá [Settu upp afhendingarmáta](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Afgreiðslueiningin notar einnig afhendingarvalmöguleikaeininguna þegar afhendingarmátar eru sýndir við útskráningu. Fyrir frekari upplýsingar, sjá [Afhendingarmöguleikaeining](../delivery-options-module.md).

Afhendingarmátar birtast þegar þeim er bætt við **Afhendingarmátar** lista í vefverslun.

## <a name="additional-resources"></a>Frekari upplýsingar

[Algengar spurningar um greiðslur](payments-retail.md)

[Greiðsluferliseining](../add-checkout-module.md)

[Greiðslueining](../payment-module.md)
