---
title: Aðili og altæk aðsetursbók
description: Þetta efnisatriði lýsir virkni aðila og altækrar aðsetursbókar tvöfaldrar skráningar.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750789"
---
# <a name="party-and-global-address-book"></a>Aðili og altæk aðsetursbók

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Aðili og altæk aðsetursbók eru hugtök í forritum Finance and Operations. Aðili getur verið stofnun/fyrirtæki eða einstaklingur. Það er hentugt að vista altækt og stjórna eiginleikum **Aðila** eins og heiti, tungumáli, tengiliðum og aðsetrum. Þegar gildi eiginleika breytist á einum stað breytist það á öllum stöðum þar sem **Aðilinn** kemur við sögu.

## <a name="party"></a>Aðili

*Aðili* er einstaklingur eða fyrirtæki sem stundar viðskipti. Með því að nota aðilahugtakið getur einstaklingur eða fyrirtæki spilað fleiri en eitt hlutverk (starfsmaður, viðskiptavinur, lánardrottinn eða tengiliður) í viðskiptum. Hlutverkið byggir á samhenginu og tilgangi. Hér eru nokkur dæmi úr tveimur skálduðum fyrirtækum, Contoso og Fabrikam.

+ **Starfskraftur**: Starfsmaður. Sem dæmi, starfsmaður Contoso.
+ **Lánardrottinn**: Fyrirtæki birgja eða í einkaeigu sem veitir fyrirtæki eða þjónustu vöru eða þjónustu. Ef til dæmis Fabrikam selur Contoso varning þá er Fabrikam í hlutverki lánardrottins.
+ **Tengiliður**: Einstaklingur til að hafa samband við. Ef til dæmis Contoso kaupir varning af Fabrikam myndi starfsmaður Contoso hafa samband við tengilið hjá Fabrikam.
+ **Viðskiptavinur**: Viðskiptavinur er einstaklingur eða fyrirtæki sem kaupir hluti frá fyrirtæki. Til dæmis ef Contoso kaupir varning af Fabrikam þá er Contoso viðskiptavinur Fabrikam.

Aðilalíkanið er oft notað til að tákna miðlungsflókin eða flókin tengsl milli fyrirtækja og fólks, sérstaklega þegar aðili spilar fleiri en eitt hlutverk. Hér eru nokkur algeng dæmi:

+ Aðili getur bæði verið viðskiptavinur og lánardrottinn. Til dæmis gæti Fabrikam í Norður-Ameríku selt Contoso rafmagnsvíra og keypt samsetta hátalara af Contoso. Í Evrópu selur Fabrikam hluti til Contoso en kaupir ekkert af Contoso.
+ Aðili getur verið bæði starfsmaður og viðskiptavinur. Til dæmis kaupir starfsmaður Contoso raftæki af Contoso til persónulegra nota.
+ Það geta verið ýmis konar tengsl milli einstaklings og fyrirtækis. Til dæmis getur Fabrikam útvegað sérfræðiþjónustu og ræður samræmingaraðila staðsetningar. Samræmingaraðilinn tengir sérfræðinginn við verkbeiðnir frá nokkrum viðskiptavinum Fabrikam. Contoso er einn viðskiptavinalykill. Þegar Contoso þarf á sérfræðingi að halda hefur Contoso samband við samfræðingaraðilann sem þá kemur beiðninni áleiðis. Samræmingaraðilinn sér um beiðnir fyrir alla viðskiptavini og býr til margs konar tengsl.

Eftirfarandi mynd sýnir gagnalíkan fyrir aðila:

![Gagnamódel fyrir aðila](media/party-gab-image1.png)

> [!Tip]
> Þegar reynt er að búa til nýja reikningsfærslu skal nota reitinn „Aðili“ til að leita að færslunni eftir heiti. Ef þú finnur færsluna þarftu aðeins að velja hana. Forritið fyllir sjálfkrafa út öll gögnin frá aðilanum. Ekki þarf að slá inn alla áskilda reiti. Þessa hegðun er hægt að finna í tilbúnum sniðum reiknings, tengiliðar og lánardrottins.

Ekki eru öllu aðilahlutverk Finance and Operations-forrita studd með tvöfaldri skráningu. Til að fá heildarlista yfir aðilahlutverk skal skoða [Yfirlit altækrar aðsetursbókar](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Altæk aðsetursbók

Altæka aðsetursbókin er skráasafn yfir póstföng og rafræn aðsetur fyrirtækja og einstaklinga sem stunda viðskipti.

Altæka aðsetursbókin geymir og meðhöndlar mörg póstföng og rafræn aðsetur eftir þörfum. Gerum til dæmis ráð fyrir því að Fabrikam eigi bensínstöðvar á 50 staðsetningum. Hver staður er með eigið póstfang, netfang og símanúmer. Aðalbensínstöðin fær rukkun vegna allra kaupa í viðskiptaskyni, en kaupin eru send beint á bensínstöðina sem óskaði eftir kaupunum. Altæka aðsetursbókin geymir aðalbensínstöðina sem reikningsheimilisfangið og allar bensínstöðvar sem heimilisfang viðtakanda fyrir Fabrikam. Hægt er að vista aðsetrin í eitt skipti og sækja þau eftir þörfum fyrir tilboð og pantanir.

Einstaklingur eða fyrirtæki geta gegnt fleiri en einu hlutverki eftir því hvert samhengi viðskiptanna er. Þegar svo á við gætu póstföngin og rafrænu aðsetrin verið þau sömu. Í þessu tilviki ætti breyting á aðsetri í einu hlutverki að birtast í hinu hlutverkinu og öfugt. Altæka aðsetursbókin geymir og sér um aðsetrin alls staðar.

![Gagnalíkan fyrir altæka aðsetursbók](media/party-gab-image2.png)

## <a name="contacts"></a>Tengiliðir

Í forritum viðskiptavinar er *Tengiliður* einstaklingur. Hinsvegar hefur taflan **Tengiliður** verið yfirhlaðin til að tákna einstakling, notanda í gátt, B2C-viðskiptavin eða lánardrottin. Framsetningin er óbein og ekki er hægt að greina muninn án þess að kíkja á tengdar færslur. Taflan **Tengiliður** hefur verið takmörkuð við 1:1 vensl við töfluna **Reikningur**. Sem hluti af aðilalíkani og líkani altækrar aðsetursbókar kynnir tvöföld skráning sérstaka eiginleika til sögunnar fyrir flokkun og tvöföld skráning leyfir N:N vensl milli einstaklings sem er **Tengiliður** og fyrirtækis (reikningseining eða lánardrottnaeining).

Til eru tvær gerðir **Tengiliður** lína:

+ Strikaður tengiliður – Lína tengiliðar með áskildu gildi í reitnum **Fyrirtæki**.
+ Óstrikaður tengiliður – Lína tengiliðar með reitinn **Fyrirtæki** auðan.

Taflan **Tengiliðir** getur geymt þessar gerðir af línum:

Gerð línu | lýsing
---|---
Einstaklingur sem er viðskiptavinur, til dæmis seljanlegur tengiliður eða B2C-viðskiptavinur. | Strikuð tengiliðafærsla þar sem reiturinn **Fyrirtæki** er ekki auður og reiturinn **Er viðskiptavinur** er stilltur á **Já**.
Einstaklingur sem er lánardrottinn, til dæmis lánardrottinn sem er einkafyrirtæki. | Strikuð tengiliðafærsla þar sem reiturinn **Fyrirtæki** er ekki auður og reiturinn **Er lánardrottinn** er stilltur á **Já**.
Einstaklingur sem er bæði viðskiptavinur og lánardrottinn. | Strikuð tengiliðafærsla þar sem reiturinn **Fyrirtæki** er ekki auður og reiturinn **Er viðskiptavinur** er stilltur á **Já** og reiturinn **Er lánardrottinn** er stilltur á **Já**. Einstaklingur getur bæði verið framleiðandi fyrir eina afurð og neytandi annarrar afurðar. Bæði Finance and Operations-forrit og tvöföld skráning styðja þessi vensl.
Einstaklingur sem er tengiliður fyrir fyrirtæki en er ekki viðskiptavinur eða lánardrottinn. | Óstrikuð tengiliðafærsla þar sem reiturinn **Fyrirtæki** er auður og reiturinn **Er viðskiptavinur** er stilltur á **Nei** og reiturinn **Er lánardrottinn** er stilltur á **Nei**.

## <a name="contact-for-party"></a>Tengiliður fyrir aðila

**Tengiliður fyrir aðila** geymir og sér um N:N vensl milli **Reikningslína** og **Tengliðalína**. Hann getur síað strikaðar línur **Tengiliðar** frá óstrikuðum línum og tengt eingöngu óstrikaðar **Tengiliðalínur** við línur **Reiknings** eða **Lánardrottins**.

Til dæmis eru Natasha Jones og Miguel Reyes dýralæknar sem bjóða upp á umönnun fyrir bóndabæi á sínu svæði. Natasha þjónustar Seattle og Miguel þjónustar Kent. Í forriti viðskiptavinar eru bóndabæirnir sýndir sem viðskiptavinir og dýralæknarnir sem tengiliðir. Ein **Tengiliðafærsla** fyrir Natasha tengist öllum bóndabæjum sem Natasha vinnur með. Á sama hátt er ein **Tengiliðafærsla** fyrir Miguel sem tengist öllum bóndabæjum sem Miguel vinnur með.

Þessi vensl eru geymd í töflunni **Tengiliður fyrir aðila**. Hægt er að finna upplýsingarnar í tilbúnu skjámyndunum:

+ Þegar þú ert í skjámyndinni **Reikningur** er til staðar flipi sem heitir **Tengdir tengiliðir**. Notið þennan flipa til að tengja einn eða fleiri tengiliði við **Reikningur** línu. Í þessari skjámynd er tengiliði úthlutað fyrir fyrirtæki. Þegar tengiliðum hefur verið úthlutað er hægt að velja einn sem aðaltengilið fyrir þann reikning. Með því að nota skjámyndina **Flýtistofnun** er aðeins hægt að velja tengilið. Það sama á við þegar skjámyndin **Lánardrottinn** er notuð og færslugerðin er **Fyrirtæki**.
+ Þegar skjámyndin **Tengiliður** er opin og línan er viðskiptavinur eða lánardrottinn eða bæði (strikaður tengiliður) er flipi sem heitir **Tengdir tengiliðir**. Notið þennan flipa til að tengja einn eða fleiri tengiliði. Í þessari skjámynd er tengiliði úthlutað fyrir B2C-viðskiptavin eða lánardrottin. Þegar tengiliðum hefur verið úthlutað er hægt að velja einn sem aðaltengilið. Með því að nota skjámyndina **Flýtistofnun** er aðeins hægt að velja tengilið.
+ Þegar skjámyndin **Tengiliður** er opin og línan er tengiliður (óstrikaður tengiliður) er flipi sem heitir **Tengd fyrirtæki**. Notið þennan flipa til að tengja einn eða fleiri viðskiptavini eða lánardrottna. Í þessari skjámynd er viðskiptavini eða lánardrottni úthlutað á undirliggjandi tengilið. Viðskiptavinurinn eða lánardrottinn getur verið fyrirtæki, einstaklingur eða bæði. Aðeins er hægt að velja eitt gildi úr svæðunum fjórum á sama tíma.

    ![Tengd fyrirtæki flipinn](media/party-gab-image3.png)

    + Ef **Kenni aðila** er valið, þá verður undirliggjandi tengiliði úthlutað á öll hlutverkin fyrir valinn aðila.
    + Ef valið er **Tengdur tengiliður**, þá er strikaður tengiliður valinn sem er af gerðinni einstaklingur.
    + Ef valið er **Tengdur reikningur** eða **Lánardrottinn**, þá er fyrirtæki valið.

    Burtséð frá valinu, þá eru tengslin stofnuð á stigi aðilans og á við um öll hlutverk aðilans og geymd í einingunni „Tengiliður fyrir aðila“.

> [!Note]
> Birtingarheiti fyrir töfluna **Tengiliður fyrir aðila** í forriti viðskiptavinar er **Tengiliður fyrir viðskiptavin/lánardrottin**.

Þegar **Tengliðalína** er opnuð þar sem **Er viðskiptavinur** er **Nei** og **Er lánardrottinn** er **Nei** sést flipinn **Tengd fyrirtæki**. Notið þennan flipa til að tengja eitt eða fleiri fyrirtæki viðskiptavinar eða lánardrottins við tengiliðinn.

Þegar lína **Tengiliðar** er opnuð þar sem **Er viðskiptavinur** er **Já** eða **Er lánardrottinn** er **Já** sést flipinn **Tengdir tengiliðir**. Notið þennan flipa til að tengja einn eða fleiri tengiliði.

## <a name="postal-address"></a>Póstaðsetur

Nýr flipi sem kallast **Aðsetur** hefur verið bætt við skjámyndirnar **Reikningur**, **Tengiliður** og **Lánardrottinn**. **Aðsetrin** fyrir stuðning N aðsetra með því að nota hnitanet eins og sýnt er á þessari mynd:

![Hnitanet fyrir póstfang](media/party-gab-image4.png)

+ Dálkurinn **Hlutverk póstfangs** sýnir tilgang aðsetursins.
+ Dálkurinn **Er aðal** sýnir aðalaðsetrið.
+ Dálkurinn **Númer aðseturs** sýnir röð aðsetursins.
+ Hnappurinn **+ Nýtt aðsetur** gerir kleift að búa til nýtt aðsetur. Hægt er að stofna eins mörg heimilisföng og þörf er á.

Reitirnir **Aðsetur 1** og **Aðsetur 2** í flipanum **Samantekt** í skjámyndinni **Reikningur** samsvarar aðsetrunum **Afhending** og **Reikningur**.

![Samantektarflipi fyrir póstfang](media/party-gab-image5.png)

Reitirnir **Aðsetur 1**, **Aðsetur 2** og **Aðsetur 3** í flipanum **Samantekt** í skjámyndinni **Tengiliður** samsvarar aðsetrunum **Viðskipti**, **Afhending** og **Reikningur**.

## <a name="electronic-address"></a>Rafrænt aðsetur

Nýr flipi sem kallast **Rafræn aðsetur** hefur verið bætt við skjámyndirnar **Reikningur**, **Tengiliður** og **Lánardrottinn**. **Aðsetrin** fyrir stuðning N aðsetra með því að nota hnitanet eins og sýnt er á þessari mynd:

![Hnitanet fyrir rafrænt aðsetur](media/party-gab-image6.png)

+ Dálkurinn **Gerð** sýnir gerð aðsetursins.
+ Dálkurinn **Er aðal** sýnir aðalaðsetrið.
+ Dálkurinn **Tilgangur** sýnir tilgang rafræna aðsetursins.
+ **+ Nýtt rafrænt aðsetur** gerir kleift að búa til nýtt aðsetur. Hægt er að stofna eins mörg heimilisföng og þörf er á.

Rafræn aðsetur eru aðeins í boði í þessu hnitaneti. Í síðari útgáfum verða allir reitir rafræns aðseturs og póstfangs fjarlægðir úr öðrum flipum, t.d. flipunum **Samantekt** og **Upplýsingar**.

## <a name="setup-instructions"></a>Leiðbeiningar um uppsetningu

Ef þú ert núverandi viðskiptavinur tvöfaldrar skráningar þá þarf að fara eftir eftirfarandi uppsetningarleiðbeiningum. Annars er hægt að sleppa þessun hluta.

1. Stöðvið eftirfarandi varpanir vegna þess að ekki er þörf á þeim lengur. Þess í stað skal keyra vörpunina Tengiliðir V2 (msdyn_contactforparties).

    + CDS Tengiliðir V2 og Tengiliðir (eiga við um tengiliði viðskiptavinar)
    + CDS Tengiliðir V2 og Tengiliðir (eiga við um tengiliði lánardrottins)

2. Eftirfarandi einingavarpanir eru uppfærðar fyrir aðilavirknina þannig að nota þarf nýjustu útgáfu af þessum vörpunum.

Varpa | Uppfæra þessa útgáfu | Breytingar
---|---|---
Viðskiptavinir V3 (lyklar) | 1.0.0.5 |Fjarlægði reitina PartyNumber og aðra aðilatengda reiti eins og heiti, persónulegar upplýsingar, póstfang, rafrænt aðsetur tengiliðar o.s.frv.
Viðskiptavinir V3 (tengiliðir) | 1.0.0.5 | Fjarlægði reitina PartyNumber og aðra aðilatengda reiti eins og heiti, persónulegar upplýsingar, póstfang, rafrænt aðsetur tengiliðar o.s.frv.
Lánardrottnar V2 (msdyn_vendors) | 1.0.0.6 | Fjarlægði reitina PartyNumber og aðra aðilatengda reiti eins og heiti, persónulegar upplýsingar, póstfang, rafrænt aðsetur tengiliðar o.s.frv.
CDS-sölutilboðshaus (tilboð) | 1.0.0.6 | Skipti út tengiliðnum fyrir ContactforParty-tilvísun.
Sölureikningshausar V2 (invoices) | 1.0.0.4 | Skipti út tengiliðnum fyrir ContactforParty-tilvísun.
Hausar CDS-sölupöntunar (sölupantanir) | 1.0.0.5 | Skipti út tengiliðnum fyrir ContactforParty-tilvísun.
Tengiliðir V2 (msdyn_contactforparties) | 1.0.0.2 | Þetta er nýtt kort. Fyrir fyrri útgáfur aðilalausnarinnar skal ganga úr skugga um að uppfæra þessa vörpun í nýjustu útgáfuna eins og minnst er á.
Staðsetningar póstfanga CDS-aðila (msdyn_partypostaladdresses) | 1.0.0.1  | Þetta er ný vörpun sem bætt er við sem hluti af fyrri forskoðunarútgáfu aðila.
CDS-póstfangsferill V2 (msdyn_postaladdresses) | | Þetta er ný vörpun sem bætt er við sem hluti af fyrri forskoðunarútgáfu aðila.
Staðsetningar CDS-póstfanga (msdyn_postaladdresscollections) | | Þetta er ný vörpun sem bætt er við sem hluti af fyrri forskoðunarútgáfu aðila.
Tengiliðir aðila V3(msdyn_partyelectronicaddresses) | | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.

## <a name="templates"></a>Sniðmát

Safn af töflukortum vinna saman fyrir samskipti aðila og altækrar aðsetursbókar eins og sýnt er í eftirfarandi töflu.

Finance and Operations-forritið | Forrit viðskiptavinatengsla     | lýsing
----------------------------|-----------------------------|------------
[Titlar tengiliðar](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Viðskiptavinir V3](mapping-reference.md#101) | lyklar |
[Viðskiptavinir V3](mapping-reference.md#116) | tengiliðir |
[CDS-aðilar](mapping-reference.md#220) | msdyn_parties |
[Staðsetningar póstfanga CDS-aðila](mapping-reference.md#233) | msdyn_partypostaladdresses |
[CDS-póstfangsferill V2](mapping-reference.md#235) | msdyn_postaladdresses |
[Staðsetningar CDS-póstfanga](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS-sölutilboðshaus](mapping-reference.md#215) | tilboð |
[Hausar CDS-sölupöntunar](mapping-reference.md#217) | salesorders |
[Kveðjuorð](mapping-reference.md#222) | msdyn_complimentaryclosings |
[Tengiliðir V2](mapping-reference.md#221) | msdyn_contactforparties |
[Hlutverk ákvarðanatöku](mapping-reference.md#224) | msdyn_decisionmakingroles |
[Starfshlutverk](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Stig viðskiptavildar](mapping-reference.md#226) | msdyn_loyaltylevels |
[Tengiliðir aðila V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Persónubundnar manngerðir](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Sölureikningshausar V2](mapping-reference.md#118) | reikningar |
[Ávörp](mapping-reference.md#228) | msdyn_salutations |
[Lánardrottnar V2](mapping-reference.md#202) | msdyn_vendors |

Frekari upplýsingar er að finna í [Tilvísun vörpunar á tvöfaldri skráningu](mapping-reference.md).
