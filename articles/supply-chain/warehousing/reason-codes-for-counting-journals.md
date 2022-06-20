---
title: Ástæðukóðar fyrir birgðatalningu
description: Þessi grein lýsir því hvernig á að setja upp og nota ástæðukóða fyrir talningu verkefna.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 7d182f1d979543eeec700924d2bd180ee06be8ce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857113"
---
# <a name="reason-codes-for-inventory-counting"></a>Ástæðukóðar fyrir birgðatalningu

[!include [banner](../includes/banner.md)]

Ástæðukóðar gera þér kleift að greina niðurstöður talningarferlis og hvers kyns misræmi sem á sér stað í því ferli. Hægt er að tilgreina ástæðuna fyrir því að gera talningu, t.d. brotið bretti eða lagerleiðrétting sem byggist á sýnishornum birgða. Á sama tíma getur þú notað leiðréttingaraðgerðina til að bóka virði leiðréttingar á lagerbirgðum á viðeigandi mótlykil sem byggir á ástæðunni fyrir hverja birgðaleiðréttingu.

## <a name="recommendation"></a>Ráðlagt

Áður en kerfið er sett upp er mælt með því að skilgreina áætlun til að vinna með ástæðukóðum. Reyndu til dæmis að svara eftirfarandi spurningum:

- Eiga ástæðukóðar að vera áskildir í vöruhúsum?
- Eiga ástæðukóðar að vera áskildir eða valfrjálsir á sumum vörum?
- Hversu marga ástæðukóða þarftu á að halda?
- Þarftu að forvelja takmarkaðan lista af ástæðukóðum fyrir leiðréttingar?
- Hvernig eiga notendur strikamerkjaskanna að nota ástæðukóða? Eiga ástæðukóðarnir að vera forvaldir, áskildir eða óbreytanlegir?
- Þurfa starfskraftar í vöruhúsi öðruvísi tilhögun á ástæðukóðum fyrir farsímaskanna? Ef svarið er já, er hægt að búa til fleiri valmyndaratriði og úthluta þeim á mismunandi fólk.
- Eiga ástæðukóðar að keyra fjárhagsbókanir mótlykils?

## <a name="turn-on-reason-code-features-in-your-system"></a>Kveikja á eiginleika ástæðukóða í kerfinu

Ef þú sérð ekki alla eiginleikana sem lýst er í þessari grein í kerfinu þínu þarftu líklega að kveikja á *Bókaðu leiðréttingar á hendi með því að nota stillanlega ástæðukóða sem tengdir eru mótreikningum* eiginleiki. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Bóka breytingar á lager með stillanlegum ástæðukóðum sem eru tengdir við mótlykla*

## <a name="set-up-reason-codes"></a>Setja upp ástæðukóða

### <a name="set-up-reason-code-policies"></a>Setja upp reglur ástæðukóða

Hægt er að búa til margar reglur um ástæðukóða þegar og hvernig ástæðukóðar talningar eru notaðir. Hver regla um ástæðukóða getur verið með eina af tveimur gerðum ástæðukóða (*Valfrjálst* eða *Áskilið*). Reglur ástæðukóða talningar er hægt að nota á stigi vöruhúss eða stigi vöru.

Til að búa til reglu fyrir ástæðukóða skaltu fylgja eftirfarandi skrefum.

1. Farðu í **Birgðastjórnun** \> **Uppsetning** \> **Birgðir** \> **Reglur ástæðukóða talningar**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta reglu við hnitanetið.
1. Stilltu reitinn **Heiti** fyrir nýju regluna.
1. Í reitnum **Gerð ástæðukóða talningar** skal velja annaðhvort *Áskilið* eða *Valfrjálst* til að tilgreina hvort val á ástæðukóða eigi að vera valfrjáls eða áskilin í einum af eftirfarandi ferlum birgðaleiðréttingar:

    - Regluleg talning (fartæki)
    - Stundartalning (fartæki)
    - Þröskuldstalning (fartæki)
    - Leiðrétting inn (fartæki)
    - Leiðrétting út (fartæki)
    - Talningarbók (þungbiðlari)
    - Leiðrétting magns/nettalning (þungbiðlari)

Hægt er að setja upp reglur um ástæðukóða bæði fyrir einstök vöruhús og afurðir. Uppsetning ástæðukóða afurðar getur hnekkt uppsetningu á vöruhúsi afurðar.

> [!NOTE]
> Fyrir vöruhús og vörur þar sem reiturinn **Regla ástæðukóða talningar** er stilltur á *Áskilið* er ekki hægt að ljúka talningabókinni og henni verður lokað þar til ástæðukóði er gefinn upp. Nánari upplýsingar er að finna í næsta hluta.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Úthluta reglum um ástæðukóða talningar á vöruhús

Til að úthluta reglu um ástæðukóða talningar á vöruhús skal fylgja þessum skrefum.

1. Farðu í **Birgðastjórnun** \> **Uppsetning** \> **Sundurliðun birgða** \> **Vöruhús**.
1. Í listanum velurðu Vöruhús.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, í flokknum **Uppsetning**, skal velja **Regla um ástæðukóða talningar**. Í felliglugganum **Úthluta reglu ástæðukóða talningar** skal því næst fylgja einu af þessum skrefum:

    - Til að nota uppsetningu reglunnar fyrir hverja vöru til að ákvarða hvort talningabækur séu áskildar fyrir hana skal sleppa því að færa inn gildi (eða eyða núverandi gildi).
    - Til að krefjast ástæðukóða í talningabókum fyrir vöruhúsið skal velja reglu ástæðu þar sem reiturinn **Gerð ástæðukóða talningar** er stilltur á *Áskilið*.
    - Ef ástæðukóði er valfrjáls í talningabókum fyrir vöruhúsið skal velja reglu ástæðu þar sem reiturinn **Gerð ástæðukóða talningar** er stilltur á *Valfrjálst*.

### <a name="assign-counting-reason-code-policies-to-products"></a>Úthluta reglum um ástæðukóða talningar á afurðir

Til að úthluta reglu um ástæðukóða talningar á afurð skal fylgja þessum skrefum.

1. Farðu í **Afurðaupplýsingastjórnun** \> **Afurðir** \> **Losaðar afurðir**.
1. Veldu afurð úr hnitanetinu.
1. Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Uppsetning**, skal velja **Regla um ástæðukóða talningar**. Í felliglugganum **Úthluta reglu ástæðukóða talningar** skal því næst fylgja einu af þessum skrefum:

    - Til að nota uppsetningu reglunnar fyrir vöruhúsið til að ákvarða hvort talningabækur séu áskildar fyrir afurðina skal sleppa því að færa inn gildi (eða eyða núverandi gildi).
    - Til að krefjast ástæðukóða í talningabókum fyrir afurðina skal velja reglu ástæðu þar sem reiturinn **Gerð ástæðukóða talningar** er stilltur á *Áskilið*. Þessi stilling hnekkir öllum stillingum ástæðukóða á stigi vöruhúss.
    - Ef ástæðukóði er valfrjáls í talningabókum fyrir afurðina skal velja reglu ástæðu þar sem reiturinn **Gerð ástæðukóða talningar** er stilltur á *Valfrjálst*. Þessi stilling hnekkir öllum stillingum ástæðukóða á stigi vöruhúss.

### <a name="set-up-counting-reason-codes"></a>Setja upp ástæðukóða talningar

Til að setja upp ástæðukóða talningar skal fylgja þessum skrefum.

1. Farðu í **Birgðastjórnun** \> **Uppsetning** \> **Birgðir** \> **Ástæðukóðar talningar**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Stilltu reitina **Ástæðukóði talningar** og **Lýsing** fyrir nýju línuna.
1. Til að úthluta mótlykli skal slá inn eða velja gildi í reitnum **Mótlykill**.

    > [!NOTE]
    > Ef mótlykli er úthlutað á ástæðukóða talningar þegar talningabók er bókuð er þessi ástæðukóði talningar notaður og gildið er bókað á móti úthlutuðum mótlykli í staðinn fyrir sjálfgefinn lykil birgðabókunarreglu.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Setja upp flokka ástæðukóða talningar

*Ástæðukóðaflokkar talningar* er hægt að nota sem hluta af valmyndaratriðunum *Leiðrétting inn* og *Leiðrétting út* í fartækjaforriti Warehouse Management til að takmarka lista yfir ástæðukóða talningar. (Nánari upplýsingar um talningu ástæðukóðahópa er að finna í [Settu upp valmyndaratriði fyrir farsíma til að stilla inn og út](#setup-adjustment-in-out) kafla síðar í þessari grein.)

1. Farðu í **Birgðastjórnun** \> **Uppsetning** \> **Birgðir** \> **Ástæðukóðaflokkar talningar**.
1. Á aðgerðasvæðinu skal velja **Nýr** til að bæta við hópi.
1. Stilltu reitina **Ástæðuflokkur talningar** og **Lýsing flokks** fyrir nýja flokkinn.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Í hlutanum **Upplýsingar** skal velja **Ný** á tækjastikunni til að bæta línu við hnitanetið. Stilltu svo reitinn **Ástæðukóði talningar** fyrir nýju línuna. 
1. Endurtakið fyrri skref til að úthluta fleiri kóðum eftir þörfum. Ef þú verður að fjarlægja kóða úr flokknum skaltu velja hann og velja svo **Eyða** á tækjastikunni.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Setja upp ástæðukóða fyrir valmyndaratriði fartækis

Þú getur stillt ástæðukóða fyrir eftirfarandi gerðir af lagerleiðréttingum:

- Regluleg talning
- Stundartalning
- Þröskuldstalning
- Leiðrétting inn
- Leiðrétting út

Í flestum tilvikum er hægt að skilgreina eftirfarandi upplýsingar fyrir hvert viðeigandi valmyndaratriði í fartæki:

- Hvort ástæðukóðinn sjáist fyrir starfskraft fartækis meðan á talningu stendur.
- Sjálfgefni ástæðukóðinn sem er sýndur í valmyndaratriði fartækis.
- Hvort notandi geti breytt ástæðukóða.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Setja upp valmyndaratriði fartækis fyrir talningarferli

Til að setja upp valmyndaratriði fartækis fyrir talningarferli skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsastjórnun** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis**.
1. Veldu viðeigandi valmyndaratriði í listaglugganum eða búðu til nýjan valmyndarhlut.
1. Á aðgerðasvæðinu skal velja **Regluleg talning**.
1. Í reitnum **Sjálfgefinn ástæðukóði talningar** skal stilla sjálfgefinn ástæðukóða sem á að skrá þegar talning er gerð með því að nota valmyndaratriði fartækis.
1. Í reitnum **Birta ástæðukóða talningar** veljið eitt eftirfarandi gilda.

    - *Lína* – Sýndu ástæðukóðann eftir að hvert frávik er skráð.
    - *Fela* – Ekki sýna ástæðukóða.

1. Stilltu **Breyta ástæðukóða talningar** á *Já* til að starfskraftur geti breytt ástæðukóða þegar hann er sýndur á fartækinu meðan á talningu stendur. Stilltu hann á *Nei* til að koma í veg fyrir að starfsmaðurinn breyti kóðanum.

> [!NOTE]
> Hægt er að virkja hnappinn **Regluleg talning** á valmyndaratriði hvaða fartækis sem er þar sem talning getur farið fram. Dæmi um það eru valmyndaratriðin fyrir stundartalningar, notendastýrð verk og kerfisstýrð verk.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>Setja upp valmyndaratriði fartækis fyrir leiðréttingu inn og leiðréttingu út

Til að setja upp valmyndaratriði fartækis fyrir leiðréttingu inn eða leiðréttingu út skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsastjórnun** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að stofna valmyndaratriði.
1. Stilltu reitina **Heiti atriðis í fartæki** og **Titill** fyrir nýja valmyndaratriðið.
1. Stilltu reitinn **Háttur** á *Verk*.
1. Stilltu valkostinn **Nota núverandi verk** á *Nei*.
1. Í reitnum **Ferli verkstofnunar** skal velja *Leiðrétting inn* eða *Leiðrétting út*.
1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti. (Öllum þessum reitum er bætt við þegar valið er *Leiðrétting inn* eða *Leiðrétting út* í reitnum **Ferli verkstofnunar**.)

    - **Nota leiðbeiningar fyrir ferli** – Ef þú býrð til ferli fyrir *Leiðrétting út* skaltu ganga úr skugga um að þessi valkostur er á *Já*. Ef þú býrð til ferli fyrir *Leiðrétting út* er þessi valkostur alltaf stilltur á *Já*.
    - **Sjálfgefinn ástæðukóði talningar** – Stilltu sjálfgefinn ástæðukóða sem á að skrá þegar talning er gerð með því að nota valmyndaratriði fartækis.
    - **Birta ástæðukóða talningar** – Veldu eitt af eftirfarandi gildum:

        - *Lína* – Sýndu ástæðukóðann eftir að hvert frávik er skráð.
        - *Fela* – Ekki sýna ástæðukóða.

    - **Breyta ástæðukóða talningar** - Ef þú stillir valkostinn á *Já* getur starfskraftur breytt ástæðukóða þegar hann er sýndur á fartækinu meðan á talningu stendur. Stilltu hann á *Nei* til að koma í veg fyrir að starfsmaðurinn breyti kóðanum.
    - **Ástæðukóðaflokkur talningar** – Veldu flokk ástæðukóða ef þú vilt takmarka listann yfir valkosti sem starfsmaðurinn hefur úr að velja. Fyrir upplýsingar um hvernig á að setja upp ástæðukóðahópa, sjá [Settu upp talningarástæðukóðahópa](#reason-groups) kafla fyrr í þessari grein. 

> [!NOTE]
> Þegar þú úthlutar ástæðukóðaflokki talningar á valmyndaratriðin *Leiðrétting inn* og *Leiðrétting út* þar sem valkosturinn **Nota leiðbeiningar fyrir ferli** er stilltur á *Já* geturðu fengið takmarkaðan lista yfir ástæðukóða talningar sem hluta af úrvinnslunni í fartækjaforrit Warehouse Management.
>
> Valkosturinn **Nota leiðbeiningar fyrir ferli** getur einnig hjálpað til við að koma í veg fyrir mikið magn leiðréttinga eigi sér stað fyrir mistök. (Til dæmis gæti starfsmaður óvart skannað strikamerki vörunúmers í stað magns.) Til að setja upp þessa virkni skaltu stilla valkostinn **Nota leiðbeiningar fyrir ferli** á *Já* fyrir hvert viðeigandi valmyndaratriði fyrir sig. Farðu síðan í **Vöruhúsastjórnun \> Uppsetning \> Starfsmaður** og stilltu reitinn **Takmörkun á magni leiðréttingar** fyrir hvern viðeigandi starfsmann í vöruhúsinu til að tilgreina hámarksmagn leiðréttingar sem starfsmaðurinn getur skráð.

## <a name="processing-that-uses-counting-reason-codes"></a>Vinnsla sem notar ástæðukóða talningar

Þegar starfsmenn nota fartækjaforrit Warehouse Management eru ástæðukóðarnir skráðir. Nema ef samþykktarferli talningar hefur verið skilgreint, eru skráðir ástæðukóðar strax notaðir sem hluti af bókun talningarbókar sem fylgir.

### <a name="cycle-count-approvals"></a>Samþykki reglulegrar talningar

Áður en talning er samþykkt getur starfskraftur breytt ástæðukóðanum sem tengist talningunni. Þegar talning er samþykkt er ástæðukóði sleginn inn í línu talningarbókar.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Breyta ástæðukóðum fyrir samþykki á lotufjölda

Til að breyta samþykki reglulegrar talningar skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsastjórnun** \> **Regluleg talning** \> **Verk reglulegrar talningar bíður yfirferðar**.
1. Veldu reglulega talningu í hnitanetinu.
1. Á aðgerðasvæðinu, í flipanum **Vinna**, skal velja **Regluleg talning**. Veldu síðan nýjan ástæðukóða í reitnum **Ástæðukóði**.

Ástæðukóðum er bætt við færslubókarlínur í talningarbókum af gerðinni *Talningarbók*.

1. Farðu í **Birgðastjórnun** \> **Færslubókarfærslur** \> **Vörutalning** \> **Talning**.
2. Í línuupplýsingum talningarbókar, í reitnum **Ástæðukóði talningar** skal velja ástæðukóða sem hentar aðstæðum.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>Skoða ástæðukóða sem skráðir eru í talningarferilinn

Til að skoða ástæðukóða sem hafa verið skráðir í talningarferlinum skal fylgja þessum skrefum.

1. Farðu í **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Talningarsaga**.
1. Veldu skrá vörutalningar úr listaglugganum.
1. Í reitnum **Ástæðukóði talningar** skal skoða talningarsöguna sem hefur verið skráð fyrir ástæðukóða.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Nota ástæðukóða fyrir leiðréttingu á magni eða talningu á netinu

Til að nota ástæðukóða fyrir leiðréttingu á magni eða talningu á netinu skal fylgja þessum skrefum.

1. Farið í **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Lagerlisti**.
1. Á aðgerðasvæðinu skal velja **Leiðrétting magns**.
1. Veldu **Leiðrétt magns** og síðan í reitnum **Ástæðukóði talningar** skal velja ástæðukóða.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
