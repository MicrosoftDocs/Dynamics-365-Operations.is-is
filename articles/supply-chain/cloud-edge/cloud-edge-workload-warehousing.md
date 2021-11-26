---
title: Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra
description: Þetta efnisatriði veitir upplýsingar um eiginleikann sem gera kvörðunareiningum kleift að keyra valin ferli úr vinnuálagi vöruhúsakerfis.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 2c2d2604dc1948d067311a12d00422ef074ac61a
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641161"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ekki er öll viðskiptavirkni í vöruhúsakerfinu studd fullkomlega fyrir vöruhús sem keyra vinnuálag á einingakvarða. Gætið þess að nota aðeins þau ferli sem Þetta efnisatriði lýsir sérstaklega sem studd ferli.

## <a name="warehouse-execution-on-scale-units"></a>Framkvæmd vöruhúss í einingarkvörðum

Vinnuálag vöruhúsakerfis gera einingakvarða skýja og jaðra kleift að keyra valda ferla úr möguleikum vöruhúsakerfisins.

## <a name="prerequisites"></a>Forkröfur

Þú verður að vera með Dynamics 365 Supply Chain Management miðstöð og einingarkvarða sem hefur verið settur upp með vinnuálagi vöruhúsakerfisins. Frekari upplýsingar um skipulag og uppsetningarferli er að finna í [Einingarkvarðar í dreifðri blandaðri grannfræði](cloud-edge-landing-page.md).

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Hvernig vinnuálag vöruhúsakeyrslu virkar í einingakvörðum

Fyrir ferlana í vinnuálagi vöruhúsakerfisins eru gögnin samstillt milli miðstöðvar og einingarkvarða.

Mælieining getur aðeins haldið utan um gögnin sem hún á. Hugtakið um eignarétt gagna fyrir einingarkvarða hjálpar til við að koma í veg fyrir árekstra. Þess vegna er mikilvægt að skilja hvaða vinnslugögn eru í eigu annars vegar miðstöðvar og hins vegar einingarkvarða.

Það fer eftir viðskiptaferlunum hvort sama gagnafærslan geti breytt eignarhaldi milli miðstöðvar og einingakvarða. Dæmi um þessa atburðarás er gefið upp í eftirfarandi hluta.

> [!IMPORTANT]
> Sum gögn er hægt að búa til í bæði miðstöðinni og einingakvarðanum. Dæmin fela m.a. í sér **Númeraplötur** og **Rununúmer**. Boðið er upp á sérstaka meðhöndlun ágreinings í aðstæðum þar sem sama einkvæma færslan er stofnuð í bæði miðstöðinni og einingakvarðanum í sama samstillta ferlinu. Þegar þetta gerist mun næsta samstilling mistakast og þú verður fara í **Kerfisstjórnun > Fyrirspurnir > Fyrirspurnir um vinnuálag > Tvíteknar færslur** þar sem hægt er að skoða og sameina gögnin.

## <a name="outbound-process-flow"></a>Vinnsluflæði á útleið

Ferli eignarhalds á gögnum á útleið fer eftir því hvort þú notar ferli farmáætlunar. Í öllum tilvikum á miðstöðin *upprunaskjölin*, t.d. sölupantanir og flutningspantanir, auk úthlutunarferlis pöntunar og færslugagna tengdrar pöntunar. En þegar þú notar ferli farmáætlunar verða farmarnir stofnaðir í miðstöðinni og því í eigu miðstöðvarinnar í upphafi. Sem hluti af ferlinu *Losa í vöruhús* er eignarhald farmgagnanna flutt í sérstaka uppsetningu einingakvarða, sem verður eigandi tilheyrandi *bylgjuvinnslu sendingar* (svo sem stofnun vinnuúthlutunar, áfyllingarvinnu og eftirspurnarvinnu). Starfskraftar í vöruhúsi geta þar af leiðandi aðeins unnið úr vinnu sölupöntunar og flutningspöntunar á útleið með Warehouse Management-fartækjaforriti sem er tengt við uppsetninguna sem keyrir tiltekið vinnuálag einingakvarðans.

Um leið og lokavinnsla vinnu kemur birgðum fyrir á lokaáfanga sendingarstaðar (Útskoti) sendir einingakvarðinn miðstöðinni merki um að uppfæra birgðafærslur upprunaskjalsins í *Tekið til*. Þar til þetta ferli keyrir og verður samstillt til baka verða lagerbirgðir í vinnuálagi einingakvarðans efnislega fráteknar á stigi vöruhúss og þú getur afgreitt strax staðfestingu sendingar á útleið án þess að þurfa að bíða eftir því að samstillingunni ljúki. Tilheyrandi sölufylgiseðill og reikningsfærsla eða sending flutningspöntunar fyrir farminn verður meðhöndlaður í miðstöðinni.

Eftirfarandi skýringarmynd sýnir flæðið á útleið og gefur til kynna hvar einstaka viðskiptaferlar gerast. (Veljið skýringarmyndina til að stækka hana.)

[![Vinnsluflæði á útleið.](media/wes_outbound_warehouse_processes-small.png "Vinnsluflæði á útleið")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Utanumhald með farmáætlun

Þegar þú notar ferli farmáætlunar eru farmar og sendingar stofnaðar í miðstöðinni og eignarhald gagnanna er flutt í einingakvarðana sem hlut af ferlinu *Losa í vöruhús* eins og sýnt er á eftirfarandi mynd.

![Utanumhald með farmáætlun.](./media/wes_outbound_processing_with_load_planning.png "Utanumhald með farmáætlun")

### <a name="outbound-processing-without-load-planning"></a>Ferli útleiðar án farmáætlunar

Þegar þú notar ekki ferli farmáætlunar eru sendingar búnar til í einingakvörðunum. Farmar eru búnir til í einingakvörðunum sem hluti af bylgjuferlinu.

![Ferli útleiðar án farmáætlunar.](./media/wes_outbound_processing_without_load_planning.png "Ferli útleiðar án farmáætlunar")

## <a name="inbound-process-flow"></a>Vinnsluflæði á innleið

Miðstöðin á eftirfarandi gögn:

- Öll upprunaskjöl, svo sem innkaupa- og framleiðslupantanir
- Hleðsluvinnsla á innleið
- Allur kostnaður fjárhagslegar uppfærslur

> [!NOTE]
> Hugmyndin á bak við innkaupapöntunarferlið á innleið er önnur en ferlið á útleið. Hægt er að nota sama vöruhúsið í annað einingakvarða eða miðstöð eftir því hvort innkaupapöntunin hefur verið losuð í vöruhúsið. Þegar pöntun hefur verið losuð í vöruhúsið er aðeins hægt að vinna með þá pöntun eftir innskráningu á einingakvarða.
>
> Ef verið er að nota ferlið *Losa í vöruhús* eru [*vöruhúsapantanir*](cloud-edge-warehouse-order.md) stofnaðar og eignaréttur tengds móttökuferlis er úthlutaður til einingarkvarðans. Miðstöðin getur ekki skráð móttöku á innleið.

Skrá verður inn á miðstöðina til að nota ferlið *Losa í vöruhús*. Fyrir úrvinnslu innkaupapöntunar skal fara inn á eina af eftirfarandi síðum til að tímasetja hana:

- **Innkaup og aðföng > Innkaupapöntun > Allar innkaupapantanir > Vöruhús > Aðgerðir > Losa í vöruhús**
- **Vöruhúsakerfi > Losa í vöruhús > Sjálfvirk losun innkaupapantana**

Þegar **Sjálfvirk losun innkaupapantana** er notuð er hægt að velja tilteknar innkaupapöntunarlínur sem byggja á fyrirspurn. Dæmigerð atburðarás væri að setja upp endurtekna runuvinnslu sem losar allar staðfestar innkaupapöntunarlínur sem búist er við að berist næsta dag.

Starfskrafturinn getur keyrt móttökuferlið með farsímaforriti Warehouse Management sem er tengt við einingarkvarðann. Gögnin eru svo skráð af einingarkvarðanum og tilkynnt gagnvart vöruhúsapöntun á innleið. Stofnun og vinnsla frágangs sem fylgir í kjölfarið verður einnig meðhöndluð af einingarkvarðanum.

Ef þú ert ekki að nota ferlið *losa í vöruhús* og ert þar af leiðandi ekki að nota *vöruhúsapantanir*, getur miðstöðin unnið úr móttöku vöruhúss og úrvinnslu vinnu á eigin vegum úr einingarkvörðum.

![Vinnsluflæði á innleið.](./media/wes-inbound-ga.png "Vinnsluflæði á innleið")

Þegar starfsmaður gerir skráningu á innleið með móttökuferli í Warehouse Management-fartækjaforriti gagnvart einingakvarðanum er innhreyfing skráð gagnvart tengdri vöruhúsapöntun sem er geymd í einingakvarðanum. Vinnuálag einingakvarðans sendir þá miðstöðinni merki um að uppfæra tengdar færslur innkaupapöntunarlínu í *Skráðar*. Um leið og þessu er lokið er hægt að keyra innhreyfingarskjal innkaupapöntunar í miðstöðinni.

Eftirfarandi skýringarmynd sýnir flæðið á innleið og gefur til kynna hvar einstaka viðskiptaferlar gerast. (Veljið skýringarmyndina til að stækka hana.)

[![Vinnsluflæði á innleið](media/wes_inbound_warehouse_processes-small.png "Vinnsluflæði á innleið")](media/wes_inbound_warehouse_processes.png)

## <a name="supported-processes-and-roles"></a>Studdar vinnslur og hlutverk

Ekki eru allir vöruhúsakerfisferlar studdir í vinnuálagi vöruhúsakeyrslu í einingarkvarða. Þess vegna er mælt með því að úthluta hlutverkum sem samsvara þeirri virkni sem er í boði fyrir hvern notanda.

Til að auðvelda þetta ferli er haft með sýnishlutverk sem kallast *Vöruhúsastjórnandi í vinnuálagi* í sýnigögnum í **Kerfisstjórnun \> Öryggi \> Öryggisstillingar**. Tilgangurinn með þessu hlutverki er sá að gera vöruhúsastjórnendum kleift að fá aðgang að vinnuálagi vöruhúsakeyrslu í einingarkvarðanum. Hlutverkið veitir aðgang að síðunum sem eiga við í samhengi við vinnuálag sem er hýst í einingarkvarða.

Notandahlutverkum í einingarkvarða er úthlutað sem hluta af upphaflegri gagnasamstillingu úr miðstöðinni við einingarkvarðann.

Til að breyta hlutverkum sem úthlutað er á notanda skal fara í **Kerfisstjórnun \> Öryggi \> Úthluta notendum á hlutverk**. Notendur sem eru aðeins í hlutverki vöruhúsastjórnanda í einingarkvarðanum eiga aðeins að fá úthlutað hlutverkinu *Vöruhúsastjórnandi í vinnuálagi*. Þessi nálgun tryggir að þessir notendur hafi aðeins aðgang að studdri virkni. Fjarlægið öll önnur hlutverk sem þessum notanda er úthlutað.

Notendur sem eru í hlutverki vöruhúsastjórnanda í bæði miðstöðinni og einingarkvörðunum eiga að fá úthlutað fyrirliggjandi hlutverkinu *Starfskraftur í vöruhúsi*. Hafa skal í huga að þetta hlutverk veitir starfskröftum í vöruhúsi aðgang að eiginleikum (svo sem móttökuvinnslu flutningspöntunar) sem birtast í notandaviðmótinu en eru ekki studdir í einingarkvörðum sem stendur.

### <a name="supported-warehouse-execution-processes"></a>Studdir ferlar fyrir keyrslu vöruhúsa

Hægt er að virkja eftirfarandi vöruhúsaferli fyrir vinnuálag vöruhúsakeyrslu í einingarkvarða:

- Valdar bylgjuaðferðir fyrir sölu- og flutningspantanir (staðfesting, stofnun álags, úthlutun, eftirspurnaráfylling, gámun, stofnun vinnu og prentun bylgjumerkis)

- Vinna úr vöruhúsavinnu sölu- og flutningspöntunar með vöruhúsaforritinu (þ.m.t. áfyllingarvinna)
- Spyrjast fyrir um lagerbirgðir í vöruhúsaforriti
- Búa til og stjórna birgðahreyfingum með vöruhúsaforriti
- Regluleg talningarvinna búin til og unnið úr henni með því að nota vöruhúsaforritið
- Að gera leiðréttingar á birgðaskrá með því að nota vöruhúsaforritið
- Skráning innkaupapantana og sinna frágangsvinnu með vöruhúsaforriti

Eftirfarandi vinnugerðir er hægt að búa til í einingakvarða og er því hægt að vinna úr sem hluti af vinnuálagi vöruhúsakerfisins:

- **Birgðahreyfingar** – Handvirk hreyfing og hreyfing eftir vinnusniðmáti.
- **Regluleg talning** – Þar á meðal samþykktar-/höfnunarferli misræmis sem hluti af talningaraðgerðum.
- **Innkaupapantanir** – Frágangsvinna í gegnum vöruhúsapöntun þegar vöruhúsapantanir eru ekki tengdar við farm.
- **Sölupantanir** – Einföld tiltekt og hleðsla.
- **Úthreyfing flutnings** – Einföld tiltekt og hleðsla.
- **Áfylling** – Að undanskildum hráefnum fyrir framleiðslu.
- **Frágangur á fullunnum vörum** – Eftir ferlið tilkynna sem tilbúna afurð.
- **Frágangur aukaafurða og hliðarafurða** – Eftir ferlið tilkynna sem tilbúna afurð.

Engar aðrar úrvinnslur á upprunaskjalagerðum eða vöruhúsavinnu eru studdar sem stendur í einingakvörðum. Til dæmis, fyrir vinnuálag vöruhúsakeyrslu í einingakvarða, er ekki hægt að framkvæma móttökuferli flutningspöntunar (innhreyfingar flutnings), þetta þarf tilvik miðstöðvar að vinna úr.

> [!NOTE]
> Valmyndaratriði og hnappar fartækis fyrir óstuddar aðgerðir eru ekki sýnd í _Farsímaforriti Warehouse Management_ þegar það er tengt við uppsetningu einingarkvarða.
> 
> Þegar vinnuálag er notað í einingarkvarða er ekki hægt að keyra óstudd ferli fyrir það tiltekna vöruhús í miðstöðinni. Töflurnar sem eru síðar í þessu efnisatriði lýsa studdum eiginleikum.
>
> Valdar vinnugerðir vöruhúss er hægt að stofna bæði í miðstöðinni og einingarkvörðum, en aðeins tilheyrandi miðstöð eða einingarkvarði getur viðhaldið þeim (uppsetningin sem bjó til gögnin).
>
> Jafnvel þegar tiltekið ferli er stutt af einingarkvarða skal hafa í huga að öll nauðsynleg gögn samstillast hugsanlega ekki úr miðstöðinni til einingarkvarðans, eða frá einingarkvarða til miðstöðvar, sem getur leitt til óvæntrar kerfisvinnslu. Dæmi um þessa sviðsmynd eru:
> 
> - Ef notuð er fyrirspurn staðsetningarleiðbeiningar sem tengir saman færslu gagnatöflu sem er aðeins til í uppsetningu miðstöðvarinnar.
> - Ef notaðar eru aðgerðir staðsetningarstöðu og/eða rúmmálshleðslu staðsetningar. Þessi gögn verða ekki samstillt á milli uppsetninganna og munu því aðeins virka þegar staðsetning birgða á lager er uppfærð í einni uppsetningunni.

Eftirfarandi virkni vöruhúsastjórnunar er ekki studd eins og er fyrir vinnuálag einingarkvarða:

- Vinnsla á innleið fyrir innkaupapöntunarlínur sem úthlutað er á hleðslu.
- Vinnsla á innleið fyrir innkaupapantanir verks.
- Að hafa umsjón með heildarkostnaði, nota ferðir og fylgjast með vörum í flutningi.
- Ferli á innleið og útleið fyrir vörur sem eru með virkar rakningarvíddir **Eigandi** og/eða **Raðnúmer**.
- Vinnslu á birgðum sem eru með stöðugildi útilokunar.
- Breyting á birgðastöðu meðan á vinnuhreyfingu stendur.
- Sveigjanlegar frátekningar á vídd á vöruhúsastigi fyrir ráðstafaða pöntun.
- Notkun aðgerðarinnar *Staðsetningarstaða vöruhúss* (gögnin eru ekki samstillt milli uppsetninga).
- Notkun aðgerðarinnar *Númeraplötustaða staðsetningar*.
- Notkun *Afurðarsía* og *Afurðarsíuflokka*, þ.m.t. stillingunnar **Fjöldi daga til að blanda runur**.
- Samþætting við gæðastjórnun.
- Úrvinnsla á vörum með framleiðsluþyngd.
- Úrvinnsla með vörur sem eru aðeins virkar fyrir flutningsstjórnun.
- Úrvinnsla á neikvæðum lagerbirgðum.
- Vinnsla vöruhúsavinnu með athugasemdum sendingar.
- Vinna vinnslu í vöruhúsi með efnismeðhöndlun/sjálfvirkni vöruhúss.
- Myndir af afurðarsniðmátsgögnum (til dæmis í farsímaforriti Warehouse Management).
- Samnýting gagna milli fyrirtækja fyrir afurðir.

> [!WARNING]
> Sumar vöruhúsaaðgerðir verða ekki í boði fyrir vöruhús sem keyra vinnuálag vöruhúsakerfisins í einingarkvarða og eru ekki heldur studdar í vinnuálagi miðstöðvar eða einingarkvarða.
> 
> Hægt er að vinna úr öðrum möguleikum fyrir bæði, en krefst vandvirkni í sumum aðstæðum, svo sem þegar birgðir á lager eru uppfærðar fyrir sama vöruhúsið í bæði miðstöð og einingarkvarða vegna uppfærsluferlis ósamstilltra gagna.
> 
> Sérstakar aðgerðir (t.d. *loka á vinnu*), sem eru studdar bæði í miðstöð og einingarkvörðum, verða aðeins studdar fyrir eiganda gagnanna.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Útleið (aðeins stutt fyrir sölu-og flutningspantanir)

Eftirfarandi tafla sýnir hvaða eiginleikar á útleið eru studdir og hvar þeir eru studdir þegar vinnuálag vöruhúsakerfis er notað í einingarkvörðum í skýi og edge.

| Vinna                                                      | Stöð | Vinnuálag vöruhúsakeyrslu í einingakvarða |
|--------------------------------------------------------------|-----|------------------------------|
| Úrvinnsla upprunaskjals                                   | Já | Nei |
| Hleðslu- og flutningsstjórnunarvinnsla                | Já, en aðeins ferli farmáætlunar. Vinnsla flutningsstjórnunar er ekki studd  | Nei |
| Losa í vöruhús                                         | Já | Nei |
| Áætluð dreifing frá dreifingarstöð                                        | Nei  | Nei |
| Sendingarsamstæða                                       | Já, þegar álagsáætlun er notuð | Já |
| Bylgjuvinnsla sendingar                                     | Nei  |Já, nema **Hleðsluáætlun og röðun** |
| Viðhalda sendingu fyrir bylgju                                  | Nei  | Já|
| Vinnsla vöruhúsavinnu (þ.m.t. prentun númeraplötu)        | Nei  | Já, en aðeins fyrir ofangreinda studda möguleika |
| Klasatiltekt                                              | Nei  | Já|
| Handvirkt pökkunarferli, þ.m.t úrvinnsla vinnunnar „Tiltekt pakkaðs gáms“ | Nei <P>Sumar vinnslur er hægt að gera eftir upphaflegt tiltektarferli sem einingarkvarðinn sér um, en ekki er mælt með því vegna eftirfarandi útilokaðra aðgerða.</p>  | Nei |
| Fjarlægja gám úr hópi                                  | Nei  | Nei |
| Röðunarferli á útleið                                  | Nei  | Nei |
| Prentun á hleðslutengdum skjölum                           | Já | Já|
| Farmbréf og ASN-myndun                            | Nei  | Já|
| Staðfesting sendingar                                             | Nei  | Já|
| Staðfesting sendingar með „Staðfesta og flytja“            | Nei  | Nei |
| Fylgiseðill og reikningsfærsla                        | Já | Nei |
| Stutt tiltekt (sölu- og flutningspantanir)                    | Nei  | Já, án þess að fjarlægja frátekningar fyrir upprunaskjöl|
| Umframtiltekt (sölu-og flutningspantanir)                     | Nei  | Já|
| Breyting vinnustaðsetninga (sölu-og flutningspantanir)         | Nei  | Já|
| Ljúka vinnu (sölu-og flutningspantanir)                    | Nei  | Já|
| Prenta vinnuskýrslu                                            | Já | Já|
| Bylgjumerki                                                   | Nei  | Já|
| Skipta vinnu                                                   | Nei  | Já|
| Úrvinnsla vinnu - Stjórnað af „Flutningshleðslu“            | Nei  | Nei |
| Minnka tiltekið magn                                       | Nei  | Nei |
| Bakfæra vinnu                                                 | Nei  | Nei |
| Bakfæra staðfestingu sendingar                                | Nei  | Já|

### <a name="inbound"></a>Á innleið

Eftirfarandi tafla sýnir hvaða eiginleikar á útleið eru studdir og hvar þeir eru studdir þegar vinnuálag vöruhúsakerfis er notað í einingarkvörðum í skýi og edge.

| Vinna                                                          | Stöð | Vinnuálag vöruhúsakeyrslu í einingakvarða<BR>*(Vörur merktar „Já“ eiga aðeins við um vöruhúsapantanir)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Úrvinnsla&nbsp;upprunaskjals&nbsp;                             | Já | Nei |
| Hleðslu- og flutningsstjórnunarvinnsla                    | Já | Nei |
| Heildarkostnaður og móttaka á vörum í flutningi                       | Já | Nei |
| Staðfesting sendingar á innleið                                    | Já | Nei |
| Losun innkaupapöntunar til vöruhúss (vinnsla vöruhúsapöntunar) | Já | Nei |
| Afpöntun vöruhúsapöntunarlína<p>Athugið að þetta er aðeins stutt þegar engin skráning er gegn línunni</p> | Já | Nei |
| Móttaka og frágangur innkaupapöntunarvöru                       | <p>Já,&nbsp;þegar&nbsp;það&nbsp;er ekki vöruhúsapöntun</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, þegar innkaupapöntun er ekki hluti af <i>hleðslu</i></p> |
| Móttaka og frágangur innkaupapöntunarlínu                       | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, þegar innkaupapöntun er ekki hluti af <i>hleðslu</i></p></p> |
| Móttaka og frágangur skilapöntunar                              | Já | Nei |
| Móttaka og frágangur blandaðrar númeraplötu                       | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Já |
| Móttaka farmvöru                                              | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Móttaka og frágangur númeraplötu                             | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Móttaka og frágangur flutningspöntunarvöru                       | Já | Nei |
| Móttaka og frágangur flutningspöntunarlínu                       | Já | Nei |
| Hætta við vinnu (á innleið)                                            | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, en aðeins þegar valkosturinn <b>Afskrá innhreyfingu þegar verk er afturkallað</b> (á síðunni <b>Færibreytur vöruhúsakerfis</b>) er hreinsaður</p> |
| Meðhöndlun innhreyfingarskjals afurða fyrir innkaupapöntun                        | Já | Nei |
| Móttaka innkaupapantana með vanafhendingu                      | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Já, en aðeins með því að gera afturköllunarbeiðni úr miðstöðinni |
| Móttaka innkaupapöntunar með umframafhendingu                       | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Já  |
| Móttekið með stofnun vinnunnar *Dreifing frá dreifingarstöð*                 | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Móttekið með stofnun vinnunnar *Gæðapöntun*                  | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Móttekið með stofnun vinnunnar *Sýnataka gæðavinnu*          | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Móttekið með stofnun vinnunnar *Gæði í gæðaskoðun*       | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Móttekið með stofnun gæðapöntunar                            | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Úrvinnsla vinnu - Stjórnað af *Frágangur klasa*                 | Já | Nei |
| Úrvinnsla vinnu með *Stutt tiltekt*                               | Já | Nei |
| Hleðsla númeraplötu                                           | Já | Já |

### <a name="warehouse-operations-and-exception-handing"></a>Vöruhúsaaðgerðir og meðhöndlun undantekningar

Eftirfarandi tafla sýnir hvaða eiginleikar vöruhúsaaðgerða og meðhöndlunarundantekningar eru studdir og hvar þeir eru studdir þegar vinnuálag vöruhúsakerfis er notað í einingarkvörðum í skýi og edge.

| Vinna                                            | Stöð | Vinnuálag vöruhúsakeyrslu í einingakvarða |
|----------------------------------------------------|-----|------------------------------|
| Fyrirspurn vegna númeraplötu                              | Já | Já                          |
| Vörufyrirspurn                                       | Já | Já                          |
| Staðsetningarfyrirspurn                                   | Já | Já                          |
| Breyta vöruhúsi                                   | Já | Já                          |
| Hreyfing                                           | Já | Já                          |
| Hreyfingar eftir sniðmáti                               | Já | Já                          |
| Flutningur í vöruhús                                 | Já | Nei                           |
| Stofna flutningspöntun úr vöruhúsaforriti           | Já | Nei                           |
| Leiðrétting (inn/út)                                | Já | Já, en ekki í aðstæðum fyrir aðlögun á útleið þar sem fjarlægja verður birgðafrátekningu með stillingunni **Fjarlægja frátekningar** í birgðaleiðréttingargerðum</p>                           |
| Breyting á birgðastöðu                            | Já | Nei                           |
| Regluleg talning og vinnsla talningarmisræmis | Já | Já                           |
| Endurprenta merki (prentun númeraplötu)             | Já | Já                          |
| Röðun númeraplötu                                | Já | Nei                           |
| Númeraplötuskipti                                | Já | Nei                           |
| Pakka í ívafnar númeraplötur                                | Já | Nei                           |
| Innskráning ökumanns                                    | Já | Nei                           |
| Útskráning ökumanns                                   | Já | Nei                           |
| Breyta ráðstöfunarkóða runu                      | Já | Já                          |
| Sýna opinn verkefnalista                             | Já | Já                          |
| Númeraplötur í samstæðu                         | Já | Nei                           |
| Áfyllingarvinnsla fyrir lágm/hám og þröskuld svæðis| Já <p>Tillaga á ekki að taka með sömu staðsetningar sem hluta af fyrirspurnunum</p>| Já                          |
| Áfyllingarvinnsla hólfuð                  | Já  | Já<p>Athugið að ljúka verður uppsetningu á einingakvarðanum</p>                           |
| Loka og opna fyrir vinnu                             | Já | Já                          |
| Skipta um notanda                                        | Já | Já                          |
| Breyta vinnuhópi á vinnu                           | Já | Já                          |
| Hætta við vinnu                                        | Já | Já                          |

### <a name="production"></a>Framleiðsla

Eftirfarandi tafla dregur saman hvaða framleiðsluaðstæður vöruhúsakerfi eru studdar eins og er í vinnuálagi einingakvarða.

| Vinna | Stöð | Vinnuálag vöruhúsakeyrslu í einingakvarða |
|---------|-----|------------------------------|
| Tilkynna sem lokið og frágangur tilbúinna afurða | Já | Já |
| Frágangur aukaafurða og hliðarafurða | Já | Já |
| <p>Öll önnur vöruhúsakerfisferli sem tengjast framleiðslu, þ.m.t.:</p><li>Losa í vöruhús</li><li>Bylgjuvinnsla framleiðslu</li><li>Tiltekt hráefnis</li><li>Kanban-frágangur</li><li>Kanban-tiltekt</li><li>Hefja framleiðslupöntun</li><li>Framleiðslurýrnun</li><li>Síðasta bretti framleiðslu</li><li>Skrá efnisnotkun</li><li>Tæma kanban</li></ul> | Já | Nei |
| Áfylling hráefnis | Nei | Nei |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Vinna með einingakvarða fyrir vöruhúsakeyrslu

Nokkrar runuvinnslur keyra á bæði miðstöðinni og einingarkvörðum.

Í uppsetningu miðstöðvar er hægt að vinna með runuvinnslur handvirkt. Hægt er að stjórna eftirfarandi þremur runuvinnslum í **Vöruhúsastjórnun \> Reglubundin verkefni \> Stjórnun vinnuálags í bakvinnslu**:

- Skilaboðaúrvinnsla kvörðunareiningar til miðstöðvar.
- Skrá móttökur á upprunapöntun
- Ljúka vöruhúsapöntunum

Í vinnuálaginu í einingarkvörðum er hægt að stjórna eftirfarandi runuvinnslum í **Vöruhúsastjórnun \> Reglubundin verkefni \> Stjórnun vinnuálags**:

- Töflufærslur bylgjuvinnslu
- Skilaboðaúrvinnsla vöruhúsamiðstöðvar til kvörðunareiningar
- Vinna úr beiðnum um magnuppfærslur fyrir vöruhúsapöntunarlínur

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
