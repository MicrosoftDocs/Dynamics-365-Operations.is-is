---
title: Aðili og altæk aðsetursbók
description: Þessi grein lýsir virkni aðila og altækrar aðsetursbókar tvöfaldrar skráningar.
author: RamaKrishnamoorthy
ms.date: 08/02/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 7f06b6e69b76bf12092fdceca5b45a6750b52233
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228991"
---
# <a name="party-and-global-address-book"></a>Aðili og altæk aðsetursbók

[!include [banner](../../includes/banner.md)]



*Aðili* og *altæk aðsetursbók* eru hugtök í forritum fjármála- og reksturs. Aðili getur verið stofnun/fyrirtæki eða einstaklingur. Það er hentugt að vista altækt og stjórna eiginleikum aðila eins og heiti, tungumáli, tengiliðum og aðsetrum. Því næst, þegar eiginleikagildi er breytt á einum stað, sést breytingin á öllum stöðum þar sem aðilinn kemur við sögu.

## <a name="party"></a>Aðili

Aðili er einstaklingur eða fyrirtæki sem stundar viðskipti. Þegar aðilahugtakið er notað getur einstaklingur eða fyrirtæki spilað fleiri en eitt hlutverk í viðskiptum (t.d. starfsmaður, viðskiptavinur, lánardrottinn eða tengiliður). Hlutverkið byggir á samhenginu og tilgangi. Hér eru nokkur dæmi um hlutverk frá tveimur upphugsuðum fyrirtækjum, Contoso og Fabrikam:

+ **Starfskraftur** – Starfsmaður. Sem dæmi má nefna starfsmann Contoso.
+ **Lánardrottinn** – Fyrirtæki birgja eða í einkaeigu sem veitir fyrirtæki eða þjónustu vöru eða þjónustu. Ef Fabrikam selur til dæmis birgðir til Contoso er Fabrikam lánardrottinn Contoso.
+ **Tengiliður** – Einstaklingur til að hafa samband við. Ef til dæmis Contoso kaupir varning af Fabrikam myndi starfsmaður Contoso hafa samband við tengilið hjá Fabrikam.
+ **Viðskiptavinur** – Einstaklingur eða fyrirtæki sem kaupir hluti frá fyrirtæki. Til dæmis ef Contoso kaupir varning af Fabrikam er Contoso viðskiptavinur Fabrikam.

Aðilalíkanið er oft notað til að tákna miðlungsflókin eða flókin tengsl milli fyrirtækja og fólks, sérstaklega þegar aðili spilar fleiri en eitt hlutverk. Hér eru nokkur algeng dæmi:

+ Aðili getur bæði verið viðskiptavinur og lánardrottinn. Til dæmis gæti Fabrikam í Norður-Ameríku selt Contoso rafmagnsvíra og keypt samsetta hátalara af Contoso. Í Evrópu selur Fabrikam hluti til Contoso en kaupir ekkert af Contoso.
+ Aðili getur verið bæði starfsmaður og viðskiptavinur. Til dæmis kaupir starfsmaður Contoso raftæki af Contoso til persónulegra nota.
+ Það geta verið margs konar tengsl milli einstaklings og fyrirtækis. Til dæmis getur Fabrikam útvegað sérfræðiþjónustu og ræður samræmingaraðila staðsetningar. Samræmingaraðilinn tengir sérfræðingana við verkbeiðnir frá nokkrum viðskiptavinum Fabrikam. Contoso er einn af viðskiptavinum Fabrikam. Þegar Contoso krefst sérfræðiþjónustu hefur það samband við samræmingaraðilann sem greiðir þá úr beiðninni. Vegna þess að samræmingaraðilinn sér um beiðnir fyrir alla viðskiptavini þá er um margs konar tengsl að ræða.

Eftirfarandi skýringarmynd sýnir gagnalíkan fyrir aðila.

![Gagnamódel fyrir aðila.](media/party-gab-image1.png)

> [!TIP]
> Þegar reynt er að búa til nýja reikningsfærslu skal nota reitinn **Aðili** til að leita að færslunni eftir heiti. Á þennan hátt þarftu bara að velja færsluna ef þú finnur hana. Forritið fyllir þá sjálfkrafa út öll gögnin frá aðilanum. Ekki þarf að stilla alla nauðsynlega reiti handvirkt. Þessa hegðun er hægt að finna á tilbúnum síðunum **Reikningur**, **Tengiliður** og **Lánardrottinn**.

Tvöföld skráning styður ekki öll hlutverk aðila í forritum fjármála- og reksturs. Til að fá heildarlista yfir aðilahlutverk skal skoða [Yfirlit altækrar aðsetursbókar](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Altæk aðsetursbók

Altæka aðsetursbókin er skráasafn yfir póstföng og rafræn aðsetur fyrirtækja og einstaklinga sem stunda viðskipti.

Altæka aðsetursbókin geymir og meðhöndlar mörg póstföng og rafræn aðsetur eftir þörfum. Til dæmis á Fabrikam bensínstöðvar á 50 staðsetningum. Hver staður er með eigið póstfang, netfang og símanúmer. Aðalbensínstöðin fær rukkun vegna allra kaupa í viðskiptaskyni, en sent er beint á bensínstöðina sem óskaði eftir kaupunum. Altæka aðsetursbókin geymir aðalbensínstöðina sem reikningsheimilisfangið fyrir Fabrikam og geymir hverja bensínstöð fyrir sig sem heimilisfang viðtakanda. Heimilisföngin er hægt að geyma í eitt skipti og síðan sækja þau þegar þarf að nota þau vegna beiðna eða pantana.

Það fer eftir viðskiptasamhenginu hvort einstaklingur eða fyrirtæki gegni fleiri en einu hlutverki og sama póstfangið og rafræna heimilisfangið kann að vera notað fyrir öll hlutverkin. Í þessu tilviki ætti breyting á aðsetri í einu hlutverki að birtast í öllum hinum hlutverkunum. Altæka aðsetursbókin geymir og sér um aðsetrin alls staðar.

Eftirfarandi skýringarmynd sýnir gagnalíkanið fyrir altæku aðsetursbókina.

![Gagnalíkan fyrir altæka aðsetursbók.](media/party-gab-image2.png)

## <a name="contact"></a>Tengiliður

Í forritum viðskiptavinar er tengiliður einstaklingur. Hinsvegar hefur taflan **Tengiliður** verið yfirhlaðin til að tákna einstakling, notanda í gátt, B2C-viðskiptavin eða lánardrottin. Framsetningin er óbein og ekki er hægt að gera greinarmun nema með því að skoða viðeigandi færslur. Taflan **Tengiliður** hefur verið takmörkuð við bein tengsl við töfluna **Reikningur**. Sem hluti af aðilalíkani og líkani altækrar aðsetursbókar kynnir tvöföld skráning sérstaka eiginleika til sögunnar fyrir flokkun og tvöföld skráning leyfir margs konar (N:N) vensl milli einstaklings og fyrirtækis (einingin **Reikningur** eða **Lánardrottinn**).

Til eru tvær gerðir **Tengiliður** lína:

+ **Strikaður tengiliður** – **Tengiliðalína** þar sem reiturinn **Fyrirtæki** er með áskilið gildi.
+ **Óstrikaður tengiliður** – **Tengiliðalína** þar sem reiturinn **Fyrirtæki** er autt.

Taflan **Tengiliður** getur geymt eftirfarandi gerðir af línum.

| Gerð línu | lýsing |
|----------|-------------|
| Einstaklingur sem er viðskiptavinur (til dæmis seljanlegur tengiliður eða B2C-viðskiptavinur) | Strikuð tengiliðafærsla þar sem reiturinn **Fyrirtæki** er ekki auður og reiturinn **Er viðskiptavinur** er stilltur á **Já**. |
| Einstaklingur sem er lánardrottinn (til dæmis lánardrottinn sem er einkafyrirtæki) | Strikuð tengiliðafærsla þar sem reiturinn **Fyrirtæki** er ekki auður og reiturinn **Er lánardrottinn** er stilltur á **Já**. |
| Einstaklingur sem er bæði viðskiptavinur og lánardrottinn. | Strikuð tengiliðafærsla þar sem reiturinn **Fyrirtæki** er ekki auður og reiturinn **Er viðskiptavinur** er stilltur á **Já** og reiturinn **Er lánardrottinn** er stilltur á **Já**. Einstaklingur getur bæði verið framleiðandi fyrir eina afurð og neytandi annarrar afurðar. Bæði fjármála- og reksturs-forrit og tvöföld skráning styðja þessi vensl. |
| Einstaklingur sem er tengiliður fyrir fyrirtæki en er ekki viðskiptavinur eða lánardrottinn | Óstrikuð tengiliðafærsla þar sem reiturinn **Fyrirtæki** er auður og reiturinn **Er viðskiptavinur** er stilltur á **Nei** og reiturinn **Er lánardrottinn** er stilltur á **Nei**. |

## <a name="contact-for-party-table"></a>Taflan tengiliður fyrir aðila

Taflan **Tengiliður fyrir aðila** geymir og sér um N:N vensl milli **Reikningslína** og **Tengliðalína**. Hún getur síað strikaðar línur **Tengiliðar** frá óstrikuðum línum og tengt eingöngu óstrikaðar **Tengiliðalínur** við línur **Reiknings** eða **Lánardrottins**.

Til dæmis eru Natasha Jones og Miguel Reyes dýralæknar sem bjóða upp á umönnun fyrir bóndabæi á sínu svæði. Natasha þjónustar Seattle og Miguel þjónustar Kent. Í forriti viðskiptavinar eru bóndabæirnir sýndir sem viðskiptavinir og dýralæknarnir eru sýndir sem tengiliðir. Ein **Tengiliðafærsla** fyrir Natasha tengist öllum bóndabæjum sem Natasha vinnur með. Á sama hátt er ein **Tengiliðafærsla** fyrir Miguel sem tengist öllum bóndabæjum sem Miguel vinnur með.

Þessi vensl eru geymd í töflunni **Tengiliður fyrir aðila**. Upplýsingarnar er að finna á tilbúnu síðunum **Reikningur**, **Tengiliður** og **Lánardrottinn**:

+ Á síðunni **Reikningur** er hægt að nota flipann **Tengdir tengiliðir** til að tengja einn eða fleiri tengiliði við línuna **Reikningur**. Á þennan hátt er tengiliðum úthlutað fyrir fyrirtæki. Síðan er hægt að velja einn tengilið sem aðaltengilið fyrir reikninginn. Ef síðan **Flýtistofnun** er notuð er aðeins hægt að velja tengilið. Það sama á við þegar síðan **Lánardrottinn** er notuð og færslugerðin er **Fyrirtæki**.
+ Á síðunni **Tengiliður**, þegar línan er viðskiptavinur, lánardrottinn eða bæði (strikaður tengiliður), er hægt að nota flipann **Tengdir tengiliðir** til að tengja einn eða fleiri tengiliði. Á þennan hátt er tengiliðum úthlutað fyrir B2C-viðskiptavin eða lánardrottin. Síðan er hægt að velja einn tengilið sem aðaltengilið. Ef síðan **Flýtistofnun** er notuð er aðeins hægt að velja tengilið.
+ Á síðunni **Tengiliður**, þegar línan er einstaklingur sem tengiliður (óstrikaður tengiliður), er hægt að nota flipann **Tengd fyrirtæki** til að tengja einn eða fleiri viðskiptavini eða lánardrottna. Á þennan hátt er viðskiptavinum eða lánardrottnum úthlutað á undirliggjandi tengiliði. Viðskiptavinurinn eða lánardrottinn getur verið fyrirtæki, einstaklingur eða bæði. Aðeins er hægt að velja gildi í einum af þeim fjórum reitum í einu:

    + Ef gildi er valið í reitnum **Kenni aðila** er öllum hlutverkum úthlutað á undirliggjandi tengilið fyrir valdan aðila.
    + Ef gildi er valið í reitnum **Tengdur tengiliður** er verið að velja strikaðan tengilið af gerðinni **Einstaklingur**.
    + Ef gildi er valið í reitnum **Tengdur reikningur** eða **Tengdur lánardrottinn** er verið að velja fyrirtæki.

    ![Flipinn tengd fyrirtæki á tengiliðasíðunni.](media/party-gab-image3.png)

    Burtséð frá valinu, þá eru tengslin stofnuð á stigi aðilans og á við um öll hlutverk aðilans og geymd í einingunni **Tengiliður fyrir aðila**.

> [!NOTE]
> Birtingarheiti fyrir töfluna **Tengiliður fyrir aðila** í forritum viðskiptavinar er **Tengiliður fyrir viðskiptavin/lánardrottin**.

Þegar línan **Tengiliður** er opnuð þar sem bæði reiturinn **Er viðskiptavinur** og **Er lánardrottinn** eru stilltir á **Nei** verður flipinn **Tengd fyrirtæki** sýndur. Notið þennan flipa til að tengja einn eða fleiri viðskiptavini eða lánardrottna við tengiliðinn.

Þegar **Tengiliðalína** er opnuð þar sem annaðhvort reiturinn **Er viðskiptavinur** eða **Er lánardrottinn** er stilltur á **Já** verður flipinn **Tengdir tengiliðir** sýndur. Notið þennan flipa til að tengja einn eða fleiri tengiliði.

## <a name="postal-addresses"></a>Póstföng

Nýr **Aðsetursflipi** hefur verið bætt við síðurnar **Reikningur**, **Tengiliður** og **Lánardrottinn**. Þessi flipi styður mörg póstföng með því að nota hnitanet eins og sýnt er á eftirfarandi mynd.

![Hnitanet fyrir póstföng.](media/party-gab-image4.png)

Netið inniheldur eftirfarandi dálka:

+ **Hlutverk póstfangs** – Tilgangur póstfangsins.
+ **Er aðalaðsetur** – Gildi sem tilgreinir hvort aðsetur er aðalaðsetur.
+ **Númer aðseturs** – Röð aðseturs.

Hægt er að nota hnappinn **Nýtt aðsetur** fyrir ofan hnitanetið til að búa til eins mörg póstföng eins og þörf er á.

Í viðskiptavinaforritum, þegar notandi færir inn heimilisföng á flipanum **Samantekt** á síðunni **Lyklar** samsvara reitirnir **Heimilisfang 1** og **Heimilisfang 2** heimilisföngum fyrir **Afhending** **Reikningur**. Þegar notandi býr til póstfang í forritum fjármála- og reksturs munu fyrstu tvö aðsetur viðskiptavinafærslunnar birtast í reitunum **Aðsetur1** og **Aðsetur2** og notandinn hefur möguleikann á að breyta tilgangi aðsetursins í **Afhending** og **Reikningur**.

![Samantektarflipi fyrir póstföng.](media/party-gab-image5.png)

Reitirnir **Aðsetur 1**, **Aðsetur 2** og **Aðsetur 3** í flipanum **Samantekt** á síðunni **Tengiliður** samsvarar aðsetrunum **Viðskipti**, **Afhending** og **Reikningur**.

## <a name="electronic-addresses"></a>Rafræn aðsetur

Nýr flipi **Rafræns aðseturs** hefur verið bætt við síðurnar **Reikningur**, **Tengiliður** og **Lánardrottinn**. Þessi flipi styður mörg rafræn aðsetur með því að nota hnitanet eins og sýnt er á eftirfarandi mynd.

![Hnitanet fyrir rafræn aðsetur.](media/party-gab-image6.png)

Netið inniheldur eftirfarandi dálka:

+ **Gerð** – Gerð rafræns heimilisfangs.
+ **Er aðalaðsetur** Gildi sem tilgreinir hvort aðsetur er aðalaðsetur.
+ **Tilgangur** – Tilgangur rafræna aðsetursins.

Hægt er að nota hnappinn **Nýtt rafrænt aðsetur** fyrir ofan hnitanetið til að búa til eins mörg aðsetur eins og þörf er á.

Í hæfnisferlinu getur þú gefið bæði upp símanúmer á vinnustað og farsímanúmer. Símanúmer fyrirtækis telst aðalsímanúmer ef **IsMobile=Nei** og farsímanúmer telst aukasímanúmer ef **IsMobile=Já**.

> [!TIP]
> Notaðu flipana **Aðsetur** og **Rafræn aðsetur** í skjámyndunum **Reikningur** og **Tengiliður** til að stjórna gáttum og rafrænum aðsetrum. Þetta tryggir að vistfangagögn séu samstillt við fjármála- og reksturs-forrit.

## <a name="setup"></a>Uppsetning

1. Opna umhverfi í forriti viðskiptavinar.

2. Settu upp allar lausnir skilyrða eins og lýst er í [Sérstakur pakki fyrir tvöfalda skráningu forrita](separated-solutions.md).

3. Setjið upp [Lausn tvöfaldrar skráningar á aðila og altækri aðsetursbók](https://aka.ms/dual-write-gab).

4. Opnið fjármála- og rekstrarforritið. Farið í gagnastjórnunareininguna og veljið flipa tvöföldrar skráningar. Stjórnunarsíða tvöföldrar skráningar opnast.

5. Setjið á báðar lausnir sem settar voru upp í skrefum 2 og 3 með aðgerðinni [Nota lausn](link-your-environment.md).

6. Stöðvið eftirfarandi varpanir vegna þess að ekki er þörf á þeim lengur. Keyrðu `Contacts V2 (msdyn_contactforparties)` kortið í staðinn.

    + CDS Tengiliðir V2 og Tengiliðir (eiga við um tengiliði viðskiptavinar)
    + CDS Tengiliðir V2 og Tengiliðir (eiga við um tengiliði lánardrottins)

7. Eftirfarandi einingavarpanir eru uppfærðar fyrir aðilavirknina þannig að nota þarf nýjustu útgáfu af þessum vörpunum.

    Varpa | Uppfæra þessa útgáfu | Breytingar
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.2 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.6 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `Customers V3 (accounts)` | 1.0.0.5 |Fjarlægði `PartyNumber` og aðra aðilatengda reiti eins og heiti, persónulegar upplýsingar, póstfang, rafrænt aðsetur tengiliðar.
    `Customer V3 (contacts)` | 1.0.0.5 | Fjarlægði `PartyNumber` og aðra aðilatengda reiti eins og heiti, persónulegar upplýsingar, póstfang, rafrænt aðsetur tengiliðar.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | Fjarlægði `PartyNumber` og aðra aðilatengda reiti eins og heiti, persónulegar upplýsingar, póstfang, rafrænt aðsetur tengiliðar.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | Skipti út tengiliðnum fyrir `ContactforParty`-tilvísun.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | Skipti út tengiliðnum fyrir `ContactforParty`-tilvísun.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | Skipti út tengiliðnum fyrir `ContactforParty`-tilvísun.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.2 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `Complimentary Closings (msdyn_compliemntaryclosings)` | 1.0.0.0 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.
    `CDS Address roles (msdyn_addressroles)` | 1.0.0.0 | Þetta er nýtt kort sem var bætt við sem hluta af þessari útgáfu.

8. Áður en ofangreind kort eru keyrð verður að uppfæra samþættingarlyklana handvirkt eins og lýst er í eftirfarandi skrefum. Veldu síðan **Vista**.

    | Varpa | Lyklar |
    |-----|------|
    | Lykill |  accountnumber [Lykilnúmer]<br>msdyn_company.cdm_companycode [Fyrirtæki (Fyrirtækjakóði)] |
    | Tengiliður | msdyn_contactpersonid [Reikningsnúmer/kenni tengiliðs]<br>msdyn_company.cdm_companycode [Fyrirtæki (Fyrirtækjakóði)] |
    | Tengiliður fyrir viðskiptavin/lánardrottin | msdyn_contactforpartynumber [Tengiliður fyrir aðilanúmer]<br>msdyn_associatedcompanyid.cdm_companycode [Tengt fyrirtæki (fyrirtækjakóði)] |
    | Lánardrottinn | msdyn_vendoraccountnumber [Númer lánardrottnalykils]<br>msdyn_company.cdm_companycode [Fyrirtæki (Fyrirtækjakóði)]|

9. Í Dataverse hefur hámarksfjöldi stafa fyrir greiningarreglu afritunar aukist úr 450 í 700 stafi. Þetta hámark gerir þér kleift að bæta einum eða fleiri lyklum við greiningarreglur afritunar. Víkkið út greiningarreglu afritunar fyrir töfluna **Lyklar** með því að stilla eftirfarandi reiti.

    | Svæði | Virði |
    |-------|-------|
    | Nafn | Reikningar með sama reikningsheiti. |
    | lýsing | Greinir reikningsfærslur sem eru með sömu gildin í eigind reikningsheitis. |
    | Gerð grunnfærslu | Lykill |
    | Samsvörun færslugerðar | Lykill |
    | Heiti reiknings (reitur) | Nákvæm samsvörun |
    | Fyrirtæki (reitur) | Nákvæm samsvörun |
    | Venslagerð (reitur) | Nákvæm samsvörun |
    | Aðilakenni (reitur) | Nákvæm samsvörun |
    | Velja (reit) | (Autt) |

    ![Afritunarregla fyrir lykla.](media/duplicate-rule-1.PNG)

10. Víkkið út greiningarreglu afritunar fyrir töfluna **Tengiliðir** með því að stilla eftirfarandi reiti.

    | Svæði | Virði |
    |-------|-------|
    | Nafn | Tengiliðir með sama fornafn og eftirnafn. |
    | lýsing | Greina tengiliðafærslur sem hafa sömu gildi í reitunum Fornafn og Eftirnafn. |
    | Gerð grunnfærslu | Tengiliður |
    | Samsvörun færslugerðar | Tengiliður |
    | Fornafn (reitur) | Nákvæm samsvörun |
    | Eftirnafn (reitur) | Nákvæm samsvörun |
    | Fyrirtæki (reitur) | Nákvæm samsvörun |
    | Aðilakenni (reitur) | Nákvæm samsvörun |
    | Velja (reit) | (Autt) |

    ![Afritunarregla fyrir tengiliði.](media/duplicate-rule-2.PNG)

11. Ef þú ert núverandi notandi tvöfaldrar skráningar skaltu fylgja leiðbeiningunum í [Uppfæra í altæka aðila- og aðsetursbókarlíkanið](upgrade-party-gab.md) og uppfæra gögnin þín. **Ekki halda áfram í skref 12 án þess að ljúka þessu skrefi.** Ef þú ert nýr notandi með tvöfalda skráningu skaltu halda áfram í skref 12.

12. Ef þú ert notandi tvöfaldrar skráningar skaltu ljúka skrefi 11 og síðan geturðu keyrt varpanir í eftirfarandi röð. Ef þú ert nýr viðskiptavinur með tvöfalda skráningu getur þú haldið áfram beint. Ef villuboð koma upp sem segir „Staðfesting verks mistókst“. Vantar reit áfangastaðar ...“, opnaðu þá vörpun og veldu **Endurhlaða töflur** og keyrðu vörpun svo aftur.

    Forrit fjármála- og reksturs | Forrit viðskiptavinatengsla  
    ----------------------------|------------------------
    [CDS-aðilar](mapping-reference.md#220) | msdyn_parties
    [Staðsetningar CDS-póstfanga](mapping-reference.md#234) | msdyn_postaladdresscollections
    [CDS-póstfangsferill V2](mapping-reference.md#235) | msdyn_postaladdresses
    [Staðsetningar póstfanga CDS-aðila](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Tengiliðir aðila V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Viðskiptavinir V3](mapping-reference.md#101) | lyklar
    [Viðskiptavinir V3](mapping-reference.md#116) | tengiliðir
    [Lánardrottnar V2](mapping-reference.md#202) | msdyn_vendors
    [Titlar tengiliðar](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Kveðjuorð](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Ávörp](mapping-reference.md#228) | msdyn_salutations
    [Hlutverk ákvarðanatöku](mapping-reference.md#224) | msdyn_decisionmakingroles
    [Starfshlutverk](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Stig viðskiptavildar](mapping-reference.md#226) | msdyn_loyaltylevels
    [Persónubundnar manngerðir](mapping-reference.md#227) | msdyn_personalcharactertypes
    [Tengiliðir V2](mapping-reference.md#221) | msdyn_contactforparties
    [CDS-sölutilboðshaus](mapping-reference.md#215) | tilboð
    [Hausar CDS-sölupöntunar](mapping-reference.md#217) | salesorders
    [Sölureikningshausar V2](mapping-reference.md#118) | reikningar
    [CDS-vistfangshlutverk](mapping-reference.md#301) | msdyn_addressroles

> [!NOTE]
> `CDS Contacts V2 (contacts)`-vörpunin er vörpunin sem var stöðvuð í skrefi 1. Þegar reynt er að keyra önnur kort gætu þessi tvö kort birst í listanum yfir háða. Ekki keyra þessi kort.
>
> Ef aðilabók og altæk aðsetursbók eru uppsettar þarf að slökkva á viðbótinni sem heitir `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead`. Ef lausn aðilabókar og altækrar aðsetursbókar er fjarlægð þarf að endurvirkja viðbótina.
>
> Ekki ætti að nota reitinn `msdyn_*partynumber` (textareitur í einni línu) sem er með í töflunum **Reikningur**, **Tengiliður** og **Lánardrottinn** frá og með þessu. Heiti merkis er með forskeytið **(Úrelt)** til glöggvunar. Í staðinn skal nota **msdyn_partyid** reitinn. Þessi reitur er leit í **msdyn_party** töflunni.
>
> Töfluheiti | Gamall reitur | Nýr reitur
> --------|-------|--------
> Lykill | `msdyn_partynumber` | `msdyn_partyid`
> Tengiliður | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Sniðmát

Safn af töflukortum vinna saman fyrir samskipti aðila og altækrar aðsetursbókar eins og sýnt er í eftirfarandi töflu.

| Forrit fjármála- og reksturs | Forrit viðskiptavinatengsla | Lýsing |
|----------------------------|-------------------------|-------------|
| [Titlar tengiliðar](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Viðskiptavinir V3](mapping-reference.md#101) | lyklar |
| [Viðskiptavinir V3](mapping-reference.md#116) | tengiliðir |
| [CDS-aðilar](mapping-reference.md#220) | msdyn\_parties |
| [Staðsetningar póstfanga CDS-aðila](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [CDS-póstfangsferill V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [Staðsetningar CDS-póstfanga](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS-sölutilboðshaus](mapping-reference.md#215) | tilboð |
| [Hausar CDS-sölupöntunar](mapping-reference.md#217) | salesorders |
| [Kveðjuorð](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [Tengiliðir V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [Hlutverk ákvarðanatöku](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [Starfshlutverk](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Stig viðskiptavildar](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Tengiliðir aðila V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Persónubundnar manngerðir](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Sölureikningshausar V2](mapping-reference.md#118) | reikningar |
| [Ávörp](mapping-reference.md#228) | msdyn\_salutations |
| [Lánardrottnar V2](mapping-reference.md#202) | msdyn\_vendors |
| [CDS-vistfangshlutverk](mapping-reference.md#301) |msdyn\_vistfangaskrár|

Frekari upplýsingar er að finna í [Tilvísun vörpunar á tvöfaldri skráningu](mapping-reference.md).

## <a name="address-roles-as-a-multi-select-drop-down-list"></a>Vistfangahlutverk sem fellilisti með mörgum valkostum
Póstfang eða rafrænt vistfang getur þjónað fleiri en einum tilgangi. Til dæmis getur póstfang þjónað sem bæði reikningsaðsetur og afhendingaraðsetur. Í þessum tilvikum getur notandi valið bæði **Reikning** og **Afhending** í fellilistanum eins og sýnt er á eftirfarandi mynd. 

![Fellilistinn tilgangur/hlutverk](media/purpose.png)

## <a name="known-issues-and-limitations"></a>Þekkt vandamál og takmarkanir

+ Í forritum fjármála- og reksturs, þegar viðskiptavinur er stofnaður ásamt aðsetri og það vistað, er hugsanlegt að aðsetrið samstillist ekki við töfluna **Aðsetur**. Þetta er vegna vandamáls varðandi röðun á verkvangi tvöfaldrar skráningar. Sem hjáleið skal stofna viðskiptavininn fyrst og vista hann. Bætið síðan aðsetrinu við.
+ Í forritum fjármála- og reksturs, þegar færsla viðskiptavinar er með aðalaðsetri og nýr tengiliður er stofnaður fyrir þann viðskiptavin, þá erfir tengiliðafærslan aðalaðsetur frá tengdri færslu viðskiptavinar. Þetta gerist einnig fyrir tengilið lánardrottins. Dataverse styður ekki þessa hegðun sem stendur. Ef tvöföld skráning er virkjuð eru tengiliðir viðskiptavina sem eru erfðir með aðalaðsetri úr forriti fjármála- og reksturs samstilltir við Dataverse ásamt aðsetri þeirra.
+ Í forritum fjármála- og reksturs er hægt að stofna tengiliðafærslu úr skjámyndinni **Bæta við tengilið**. Þegar reynt er að stofna nýjan tengilið úr skjámyndinni **Skoða tengilið** mistekst aðgerðin. Þetta er þekkt vandamál.

    ![Þekkt vandamál með Bæta við tengilið.](media/party-gab-contact-issue.png)

+ **Upphafleg samstilling** styður ekki tímareitina **Tiltækt frá** og **Tiltækt til** í **ContactForParty** vegna þess að DIXF breytir gildinu í streng í stað heiltölu. Breytingin leiðir til villunnar `Cannot convert the literal '<say 08:00:00>' to the expected type edm.int32`.
+ Ekki er hægt að færa inn póstfang fram í tímann með því að nota fjármála- og reksturs-forrit með tvöfaldri skráningu vegna þess að Dataverse styður ekki dagsetningarvirkni. Ef fært er inn póstfang dagsett fram í tímann með því að nota fjármála- og reksturs-forrit, samstillist það að fullu við Dataverse og aðsetrið mun sjást strax í notandaviðmótinu. Allar uppfærslur á þessari færslu leiða til villu þar sem hún er með framvirka dagsetningu en ekki líðandi dagsetningu í forriti fjármála- og reksturs.
