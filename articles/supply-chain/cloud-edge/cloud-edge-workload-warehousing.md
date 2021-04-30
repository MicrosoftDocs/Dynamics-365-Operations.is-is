---
title: Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra
description: Þetta efnisatriði veitir upplýsingar um eiginleikann sem gera kvörðunareiningum kleift að keyra valin ferli úr vinnuálagi vöruhúsakerfis.
author: perlynne
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d6dffb1ea03b8d11519087163d2837d6cfe3df4e
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899168"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ekki er öll viðskiptavirkni í vöruhúsakerfinu studd fullkomlega fyrir vöruhús sem keyra vinnuálag á einingakvarða. Gætið þess að nota aðeins þau ferli sem Þetta efnisatriði lýsir sérstaklega sem studd ferli.

## <a name="warehouse-execution-on-scale-units"></a>Framkvæmd vöruhúss í einingarkvörðum

Þessi eiginleiki gerir einingarkvörðum kleift að keyra valda ferla af möguleikum vöruhúsakerfisins.

Í þessu efnisatriði eru framkvæmdir vöruhúsakerfisins í vöruhúsi sem er skilgreint sem einingarkvarði þekktar sem *Framkvæmdakerfi vöruhúss* (*WES*).

## <a name="prerequisites"></a>Forkröfur

Þú verður að vera með Dynamics 365 Supply Chain Management miðstöð og einingarkvarða sem hefur verið settur upp með vinnuálagi vöruhúsakerfisins. Frekari upplýsingar um skipulag og uppsetningarferli er að finna í [Nota einingarkvarða til að stuðla að aukinni getu gagnvart vinnuálagi Supply Chain Management](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Hvernig WES-vinnuálagið virkar í einingarkvörðum

Fyrir ferlana í vinnuálagi vöruhúsakerfisins eru gögnin samstillt milli miðstöðvar og einingarkvarða.

Mælieining getur aðeins haldið utan um gögnin sem hún á. Hugtakið um eignarétt gagna fyrir einingarkvarða hjálpar til við að koma í veg fyrir árekstra. Þess vegna er mikilvægt að skilja hvaða ferlar eru í eigu annars vegar miðstöðvar og hins vegar einingarkvarða.

Einingarkvarðarnir eiga eftirfarandi gögn:

- **Gögn bylgjuvinnslu** - Valdar aðferðir bylgjuvinnslu eru meðhöndlaðar sem hluti af bylgjuvinnslu einingarkvarða.
- **Gögn verkvinnslu** - Eftirfarandi gerðir af úrvinnslu verkbeiðna eru studdar:

  - **Birgðahreyfingar** (handvirk hreyfing og hreyfing eftir vinnusniðmáti)
  - **Innkaupapantanir** (frágangsvinna í gegnum vöruhúsapöntun þegar vöruhúsapantanir eru ekki tengdar við farm)
  - **Sölupantanir** (einföld tiltekt og hleðsla)
  - **Flutningspantanir** (aðeins á útleið með einfaldri tiltektar- og hleðsluvinnu)

- **Móttökugögn vöruhúsapöntunar** - Þessi gögn eru aðeins notuð fyrir innkaupapantanir sem eru losaðar handvirkt til vöruhúss.
- **Gögn númeraplötu** - Númeraplötur er hægt að stofna í miðstöðinni og einingarkvarða. Búið er að úthluta meðhöndlun á árekstrum. Athugið að þessi gögn eru ekki bundin við vöruhús.

## <a name="outbound-process-flow"></a>Vinnsluflæði á útleið

Miðstöðin á eftirfarandi gögn:

- Öll upprunaskjöl, svo sem sölupantanirnar og flutningspantanir
- Úthlutun pöntunar og hleðsluvinnsla á útleið
- Ferli losunar í vöruhús, stofnun sendingar, bylgjustofnun og bylgjulok

Einingarkvarðarnir eiga raunverulegu bylgjuvinnsluna (á borð við verkúthlutun, áfyllingarvinnu og eftirspurnarvinnu) þegar bylgja hefur verið losuð. Starfskraftar í vöruhúsi geta þar af leiðandi unnið úr vinnu á útleið með farsímaforriti vöruhúsakerfis sem er tengt við einingarkvarðann.

![Vinnsluflæði bylgju](./media/wes-wave-processing-ga.png "Vinnsluflæði bylgju")

## <a name="inbound-process-flow"></a>Vinnsluflæði á innleið

Miðstöðin á eftirfarandi gögn:

- Öll upprunaskjöl, svo sem innkaupapantanir og skilapantanir
- Hleðsluvinnsla á innleið
- Allur kostnaður fjárhagslegar uppfærslur

> [!NOTE]
> Hugmyndin á bak við innkaupapöntunarferlið á innleið er önnur en ferlið á útleið. Hægt er að nota sama vöruhúsið í annað einingakvarða eða miðstöð eftir því hvort innkaupapöntunin hefur verið losuð í vöruhúsið eða ekki. Þegar pöntun hefur verið losuð í vöruhúsið er aðeins hægt að vinna með þá pöntun eftir innskráningu á einingakvarða.

Ef verið er að nota ferlið *Losa í vöruhús* eru [*vöruhúsapantanir*](cloud-edge-warehouse-order.md) stofnaðar og eignaréttur tengds móttökuferlis er úthlutaður til einingarkvarðans. Miðstöðin getur ekki skráð móttöku á innleið.

Skrá verður inn á miðstöðina til að nota ferlið *Losa í vöruhús*. Farðu inn á eina af eftirfarandi síðum til að tímasetja þetta:

- **Innkaup og aðföng > Innkaupapöntun > Allar innkaupapantanir > Vöruhús > Aðgerðir > Losa í vöruhús**
- **Vöruhúsakerfi > Losa í vöruhús > Sjálfvirk losun innkaupapantana**

Þegar **Sjálfvirk losun innkaupapantana** er notuð er hægt að velja tilteknar innkaupapöntunarlínur sem byggja á fyrirspurn. Dæmigerð atburðarás væri að setja upp endurtekna runuvinnslu sem losar allar staðfestar innkaupapöntunarlínur sem búist er við að berist næsta dag.

Starfskrafturinn getur keyrt móttökuferlið með farsímaforriti vöruhúsakerfis sem er tengt við einingarkvarðann. Gögnin eru svo skráð af einingarkvarðanum og tilkynnt gagnvart vöruhúsapöntun á innleið. Stofnun og vinnsla frágangs sem fylgir í kjölfarið verður einnig meðhöndluð af einingarkvarðanum.

Ef þú ert ekki að nota ferlið *losa í vöruhús* og ert þar af leiðandi ekki að nota *vöruhúsapantanir*, getur miðstöðin unnið úr móttöku vöruhúss og úrvinnslu vinnu á eigin vegum úr einingarkvörðum.

![Vinnsluflæði á innleið](./media/wes-inbound-ga.png "Vinnsluflæði á innleið")

## <a name="supported-processes-and-roles"></a>Studdar vinnslur og hlutverk

Ekki eru allir vöruhúsakerfisferlar studdir í vinnuálagi WES í einingarkvarða. Þess vegna er mælt með því að úthluta hlutverkum sem samsvara þeirri virkni sem er í boði fyrir hvern notanda.

Til að auðvelda þetta ferli er haft með sýnishlutverk sem kallast *Vöruhúsastjórnandi í vinnuálagi* í sýnigögnum í **Kerfisstjórnun \> Öryggi \> Öryggisstillingar**. Tilgangurinn með þessu hlutverki er sá að gera vöruhúsastjórnendum kleift að fá aðgang að WES í einingarkvarðanum. Hlutverkið veitir aðgang að síðunum sem eiga við í samhengi við vinnuálag sem er hýst í einingarkvarða.

Notandahlutverkum í einingarkvarða er úthlutað sem hluta af upphaflegri gagnasamstillingu úr miðstöðinni við einingarkvarðann.

Til að breyta hlutverkum sem úthlutað er á notanda skal fara í **Kerfisstjórnun \> Öryggi \> Úthluta notendum á hlutverk**. Notendur sem eru aðeins í hlutverki vöruhúsastjórnanda í einingarkvarðanum eiga aðeins að fá úthlutað hlutverkinu *Vöruhúsastjórnandi í vinnuálagi*. Þessi nálgun tryggir að þessir notendur hafi aðeins aðgang að studdri virkni. Fjarlægið öll önnur hlutverk sem þessum notanda er úthlutað.

Notendur sem eru í hlutverki vöruhúsastjórnanda í bæði miðstöðinni og einingarkvörðunum eiga að fá úthlutað fyrirliggjandi hlutverkinu *Starfskraftur í vöruhúsi*. Hafa skal í huga að þetta hlutverk veitir starfskröftum í vöruhúsi aðgang að eiginleikum (svo sem móttökuvinnslu flutningspöntunar) sem birtast í notandaviðmótinu en eru ekki studdir í einingarkvörðum sem stendur.

## <a name="supported-wes-processes"></a>Studd WES-ferli

Hægt er að virkja eftirfarandi vöruhúsaferli fyrir vinnuálag WES í einingarkvarða:

- Valdar bylgjuaðferðir fyrir sölu- og flutningspantanir (úthlutun, eftirspurnaráfylling, gámun, stofnun vinnu og prentun bylgjumerkis)
- Vinna úr vöruhúsavinnu sölu- og flutningspöntunar með farsímaforriti vöruhúsakerfis (þ.m.t. áfyllingarvinna)
- Spyrjast fyrir um lagerbirgðir í farsímaforriti vöruhúsakerfis
- Búa til og stjórna birgðahreyfingum með farsímaforriti vöruhúsakerfis
- Skráning innkaupapantana og sinna frágangsvinnu með farsímaforriti vöruhúsakerfis

Eftirfarandi verkbeiðnigerðir eru studdar fyrir vinnuálag WES sem stendur í uppsetningum einingarkvarða:

- Sölupantanir
- Flutningsútgáfa
- Áfylling
- Birgðahreyfing
- Innkaupapantanir (tengdar við vöruhúsapantanir)

Engar aðrar úrvinnslur á upprunaskjalagerðum eða vöruhúsavinnu eru studdar sem stendur í einingakvörðum. Til dæmis, fyrir WES-vinnuálag í einingakvarða, er ekki hægt að framkvæma móttökuferli flutningspöntunar (innhreyfingar flutnings) eða vinna úr vinnu reglulegrar talningar.

> [!NOTE]
> Valmyndaratriði og hnappar fartækis fyrir óstuddar aðgerðir eru ekki sýnd í _Farsímaforriti vöruhúsakerfis_ þegar það er tengt við uppsetningu einingarkvarða.

> [!WARNING]
> Þegar vinnuálag er notað í einingarkvarða er ekki hægt að keyra óstudd ferli fyrir það tiltekna vöruhús í miðstöðinni. Töflurnar sem eru síðar í þessu efnisatriði lýsa studdum eiginleikum.
>
> Valdar vinnugerðir vöruhúss er hægt að stofna bæði í miðstöðinni og einingarkvörðum, en aðeins tilheyrandi miðstöð eða einingarkvarði getur viðhaldið þeim (uppsetningin sem bjó til gögnin).
>
> Jafnvel þegar tiltekið ferli er stutt af einingarkvarða skal hafa í huga að öll nauðsynleg gögn samstillast hugsanlega ekki úr miðstöðinni til einingarkvarðans, eða frá einingarkvarða til miðstöðvar, sem getur leitt til óvæntrar kerfisvinnslu. Dæmi eru:
> 
> - Ef notuð er fyrirspurn staðsetningarleiðbeiningar sem tengir saman færslu gagnatöflu sem er aðeins til í uppsetningu miðstöðvarinnar.
> - Ef notaðar eru aðgerðir staðsetningarstöðu og/eða rúmmálshleðslu staðsetningar. Þessi gögn verða ekki samstillt á milli uppsetninganna og munu því aðeins virka þegar staðsetning birgða á lager er uppfærð í einni uppsetningunni.

Eftirfarandi virkni vöruhúsastjórnunar er ekki studd eins og er fyrir vinnuálag einingarkvarða:

- Vinnsla á innleið fyrir innkaupapöntunarlínur sem úthlutað er á hleðslu
- Vinnsla á innleið fyrir innkaupapantanir verks
- Ferli á innleið og útleið fyrir vörur sem eru með virkar rakningarvíddir **Eigandi** og/eða **Raðnúmer**
- Vinnslu á birgðum sem eru með stöðugildi útilokunar
- Breyting á birgðastöðu meðan á vinnuhreyfingu stendur
- Sveigjanlegar frátekningar á vídd á vöruhúsastigi fyrir ráðstafaða pöntun
- Notkun aðgerðarinnar *Staðsetningarstaða vöruhúss* (gögnin eru ekki samstillt milli uppsetninga)
- Notkun aðgerðarinnar *Númeraplötustaða staðsetningar*
- Notkun *Afurðarsía* og *Afurðarsíuflokka*, þ.m.t. stillingunnar **Fjöldi daga til að blanda runur**
- Samþætting við gæðastjórnun
- Úrvinnsla á vörum með framleiðsluþyngd
- Úrvinnsla með vörur sem eru aðeins virkar fyrir flutningsstjórnun
- Úrvinnsla á neikvæðum lagerbirgðum
- Vinnsla vöruhúsavinnu með sérsniðnum vinnugerðum
- Vinnsla vöruhúsavinnu með athugasemdum sendingar
- Vinnsla vöruhúsavinnu með ræsingu þröskulds fyrir reglulega talningu
- Vinna vinnslu í vöruhúsi með efnismeðhöndlun/warehouse automation
- Notkun á mynd afurðarsniðmátsgagna (til dæmis farsímaforrit vöruhúsakerfis)

> [!WARNING]
> Sumar vöruhúsaaðgerðir verða ekki í boði fyrir vöruhús sem keyra vinnuálag vöruhúsakerfisins í einingarkvarða og eru ekki heldur studdar í vinnuálagi miðstöðvar eða einingarkvarða.
> 
> Hægt er að vinna úr öðrum möguleikum fyrir bæði, en krefst vandvirkni í sumum aðstæðum, svo sem þegar birgðir á lager eru uppfærðar fyrir sama vöruhúsið í bæði miðstöð og einingarkvarða vegna uppfærsluferlis ósamstilltra gagna.
> 
> Sérstakar aðgerðir (t.d. *loka á vinnu*), sem eru studdar bæði í miðstöð og einingarkvörðum, verða aðeins studdar fyrir eiganda gagnanna.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Útleið (aðeins stutt fyrir sölu-og flutningspantanir)

Eftirfarandi tafla sýnir hvaða eiginleikar á útleið eru studdir og hvar þeir eru studdir þegar vinnuálag vöruhúsakerfis er notað í einingarkvörðum í skýi og edge.

| Vinna                                                      | Stöð | Vinnuálag WES í einingarkvarða |
|--------------------------------------------------------------|-----|------------------------------|
| Úrvinnsla upprunaskjals                                   | Já | Ekkert |
| Hleðslu- og flutningsstjórnunarvinnsla                | Já | Ekkert |
| Losa í vöruhús                                         | Já | Ekkert |
| Áætluð dreifing frá dreifingarstöð                                        | Ekkert  | Ekkert |
| Sendingarsamstæða                                       | Já | Ekkert |
| Bylgjuvinnsla sendingar                                     | Já, en aðeins frumstilling og frágangur bylgjunnar eru meðhöndluð í miðstöðinni. Þetta þýðir að flutningur á útleið og meðhöndlun sölupöntunar er aðeins hægt að vinna með einingakvarðanum.|<p>Nei, miðstöðin sér um frumstillingu og frágang og **Hleðsluáætlun og röðun** eru ekki studd<p><b>Athugið:</b> Aðgangur að miðstöðinni er nauðsynlegur til að ljúka við bylgjustöðuna sem hluti af bylgjuvinnslunni.</p> |
| Viðhalda sendingu fyrir bylgju                                  | Já | Ekkert |
| Vinnsla vöruhúsavinnu (þ.m.t. prentun númeraplötu)        | Ekkert  | <p>Já, en aðeins fyrir ofangreinda eiginleika sem eru studdir. |
| Klasatiltekt                                              | Ekkert  | Já|
| Handvirkt pökkunarferli, þ.m.t úrvinnsla vinnunnar „Tiltekt pakkaðs gáms“                                           | Ekkert <P>Sumar vinnslur er hægt að gera eftir upphaflegt tiltektarferli sem einingarkvarðinn sér um, en ekki er mælt með því vegna eftirfarandi útilokaðra aðgerða.</p>  | Ekkert  |
| Fjarlægja gám úr hópi                        | Ekkert  | Ekkert                           |
| Röðunarferli á útleið                                  | Ekkert  | Ekkert |
| Prentun á hleðslutengdum skjölum                           | Já | Ekkert |
| Farmbréf og ASN-myndun                            | Já | Ekkert |
| Staðfesting sendingar                    | Já  | Ekkert |
| Staðfesting sendingar með „Staðfesta og flytja“                    | Ekkert  | Ekkert |
| Fylgiseðill og reikningsfærsla                | Já | Ekkert |
| Stutt tiltekt (sölu- og flutningspantanir)                    | Ekkert  | Ekkert |
| Umframtiltekt (sölu-og flutningspantanir)                     | Ekkert  | Ekkert |
| Breyting vinnustaðsetninga (sölu-og flutningspantanir)         | Ekkert  | Já|
| Ljúka vinnu (sölu-og flutningspantanir)                    | Ekkert  | Já|
| Prenta vinnuskýrslu                                            | Já | Ekkert |
| Bylgjumerki                                                   | Ekkert  | Já|
| Skipta vinnu                                                   | Ekkert  | Já|
| Úrvinnsla vinnu - Stjórnað af „Flutningshleðslu“            | Ekkert  | Ekkert |
| Minnka tiltekið magn                                       | Ekkert  | Ekkert |
| Bakfæra vinnu                                                 | Ekkert  | Ekkert |
| Bakfæra staðfestingu sendingar                                | Já | Ekkert |

### <a name="inbound"></a>Á innleið

Eftirfarandi tafla sýnir hvaða eiginleikar á útleið eru studdir og hvar þeir eru studdir þegar vinnuálag vöruhúsakerfis er notað í einingarkvörðum í skýi og edge.

| Vinna                                                          | Stöð | Vinnuálag WES í einingarkvarða<BR>*(Vörur merktar „Já“ eiga aðeins við um vöruhúsapantanir)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Úrvinnsla&nbsp;upprunaskjals&nbsp;                                       | Já | Ekkert |
| Hleðslu- og flutningsstjórnunarvinnsla                    | Já | Ekkert |
| Staðfesting sendingar á innleið                                            | Já | Ekkert |
| Losun innkaupapöntunar til vöruhúss (vinnsla vöruhúsapöntunar) | Já | Ekkert |
| Afpöntun vöruhúsapöntunarlína<p>Athugið að þetta er aðeins stutt þegar engin skráning er gegn línunni</p>          | Já | Ekkert |
| Móttaka og frágangur innkaupapöntunarvöru                       | <p>Já,&nbsp;þegar&nbsp;það&nbsp;er ekki vöruhúsapöntun</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, þegar innkaupapöntun er ekki hluti af <i>hleðslu</i></p> |
| Móttaka og frágangur innkaupapöntunarlínu                        | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, þegar innkaupapöntun er ekki hluti af <i>hleðslu</i></p></p> |
| Móttaka og frágangur skilapöntunar                               | Já | Ekkert |
| Móttaka og frágangur blandaðrar númeraplötu                        | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttaka farmvöru                                             | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttaka og frágangur númeraplötu                              | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttaka og frágangur flutningspöntunarvöru                        | Já | Ekkert |
| Móttaka og frágangur flutningspöntunarlínu                        | Já | Ekkert |
| Hætta við vinnu (á innleið)                                              | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, en aðeins þegar valkosturinn <b>Afskrá innhreyfingu þegar verk er afturkallað</b> (á síðunni <b>Færibreytur vöruhúsakerfis</b>) er hreinsaður</p> |
| Meðhöndlun innhreyfingarskjals afurða fyrir innkaupapöntun                          | Já | Ekkert |
| Móttaka innkaupapantana með vanafhendingu                        | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Já, en aðeins með því að gera afturköllunarbeiðni úr miðstöðinni |
| Móttaka innkaupapöntunar með umframafhendingu                        | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Já  |
| Móttekið með stofnun vinnunnar *Dreifing frá dreifingarstöð*                   | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttekið með stofnun vinnunnar *Gæðapöntun*                  | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttekið með stofnun vinnunnar *Sýnataka gæðavinnu*          | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttekið með stofnun vinnunnar *Gæði í gæðaskoðun*       | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttekið með stofnun gæðapöntunar                            | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Úrvinnsla vinnu - Stjórnað af *Frágangur klasa*                             | Já | Ekkert |
| Úrvinnsla vinnu með *Stutt tiltekt*                                           | Já | Ekkert |
| Hleðsla númeraplötu                                           | Já | Ekkert |

### <a name="warehouse-operations-and-exception-handing"></a>Vöruhúsaaðgerðir og meðhöndlun undantekningar

Eftirfarandi tafla sýnir hvaða eiginleikar vöruhúsaaðgerða og meðhöndlunarundantekningar eru studdir og hvar þeir eru studdir þegar vinnuálag vöruhúsakerfis er notað í einingarkvörðum í skýi og edge.

| Vinna                                            | Stöð | Vinnuálag WES í einingarkvarða |
|----------------------------------------------------|-----|------------------------------|
| Fyrirspurn vegna númeraplötu                              | Já | Já                          |
| Vörufyrirspurn                                       | Já | Já                          |
| Staðsetningarfyrirspurn                                   | Já | Já                          |
| Breyta vöruhúsi                                   | Já | Já                          |
| Hreyfing                                           | Já | Já                          |
| Hreyfingar eftir sniðmáti                               | Já | Já                          |
| Flutningur í vöruhús                                 | Já | Ekkert                           |
| Stofna flutningspantanir úr farsímaforriti vöruhúsakerfis           | Já | Ekkert                           |
| Leiðrétting (inn/út)                                | Já | Ekkert                           |
| Breyting á birgðastöðu                            | Já | Ekkert                           |
| Regluleg talning og vinnsla talningarmisræmis | Já | Ekkert                           |
| Endurprenta merki (prentun númeraplötu)             | Já | Já                          |
| Röðun númeraplötu                                | Já | Ekkert                           |
| Númeraplötuskipti                                | Já | Ekkert                           |
| Pakka í ívafnar númeraplötur                                | Já | Ekkert                           |
| Innskráning ökumanns                                    | Já | Ekkert                           |
| Útskráning ökumanns                                   | Já | Ekkert                           |
| Breyta ráðstöfunarkóða runu                      | Já | Já                          |
| Sýna opinn verkefnalista                             | Já | Já                          |
| Númeraplötur í samstæðu                         | Já | Ekkert                           |
| Áfyllingarvinnsla fyrir lágm/hám og þröskuld svæðis| Já <p>Tillaga á ekki að taka með sömu staðsetningar sem hluta af fyrirspurnunum</p>| Já                          |
| Áfyllingarvinnsla hólfuð                  | Já  | Já<p>Athugið að ljúka verður uppsetningu á einingakvarðanum</p>                           |
| Loka og opna fyrir vinnu                             | Já | Já                          |
| Skipta um notanda                                        | Já | Já                          |
| Breyta vinnuhópi á vinnu                           | Já | Já                          |
| Hætta við vinnu                                        | Já | Já                          |


### <a name="production"></a>Framleiðsla

Framleiðsluaðstæður vöruhúsakerfis eru ekki studdar sem stendur í vinnuálagi einingarkvarða eins og tilgreint er í eftirfarandi töflu.

| Vinna | Stöð | Vinnuálag WES í einingarkvarða |
|---------|-----|------------------------------|
| <p>Öll vöruhúsakerfisferli sem tengjast framleiðslu. Hér eru nokkur dæmi:</p><li>Losa í vöruhús</li><li>Bylgjuvinnsla framleiðslu</li><li>Tiltekt hráefnis</li><li>Frágangur RAF og fullunninna vara</li><li>Frágangur aukaafurða og hliðarafurða</li><li>Kanban-frágangur</li><li>Kanban-tiltekt</li><li>Hefja framleiðslupöntun</li><li>Framleiðslurýrnun</li><li>Síðasta bretti framleiðslu</li><li>Skrá efnisnotkun</li><li>Tæma kanban</li></ul> | Já | Ekkert |

## <a name="maintaining-scale-units-for-wes"></a>Vinna með einingarkvörðum fyrir WES

Nokkrar runuvinnslur keyra á bæði miðstöðinni og einingarkvörðum.

Í uppsetningu miðstöðvar er hægt að vinna með runuvinnslur handvirkt. Hægt er að stjórna eftirfarandi þremur runuvinnslum í **Vöruhúsastjórnun \> Reglubundin verkefni \> Stjórnun vinnuálags í bakvinnslu**:

- Vinna úr uppfærslutilvikum vinnustöðu
- Skilaboðaúrvinnsla kvörðunareiningar til miðstöðvar.
- Skrá móttökur á upprunapöntun
- Ljúka vöruhúsapöntunum
- Vinna úr svörum vegna uppfærslu á magni fyrir pöntunarlínur vöruhúss

Í vinnuálaginu í einingarkvörðum er hægt að stjórna eftirfarandi runuvinnslum í **Vöruhúsastjórnun \> Reglubundin verkefni \> Stjórnun vinnuálags**:

- Töflufærslur bylgjuvinnslu
- Skilaboðaúrvinnsla vöruhúsamiðstöðvar til kvörðunareiningar
- Vinna úr beiðnum um magnuppfærslur fyrir vöruhúsapöntunarlínur

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
