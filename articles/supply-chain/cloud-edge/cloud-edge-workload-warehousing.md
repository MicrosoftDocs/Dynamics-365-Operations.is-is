---
title: Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra
description: Þetta efnisatriði veitir upplýsingar um eiginleikann sem gera kvörðunareiningum kleift að keyra valin ferli úr vinnuálagi vöruhúsakerfis.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, InventTransferOrders, SalesTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d8b0f5a4878a924943f6f8876575d5247875811
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068110"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ekki er öll viðskiptavirkni í vöruhúsakerfinu studd fullkomlega fyrir vöruhús sem keyra vinnuálag á einingakvarða. Gætið þess að nota aðeins þau ferli sem Þetta efnisatriði lýsir sérstaklega sem studd ferli.

## <a name="warehouse-execution-on-scale-units"></a>Framkvæmd vöruhúss í einingarkvörðum

Vinnuálag vöruhúsakerfis gera einingakvarða skýja og jaðra kleift að keyra valda ferla úr möguleikum vöruhúsakerfisins.

## <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar að vinna með vinnuálag vöruhúsastjórnunar verður að undirbúa kerfið eins og lýst er í þessum hluta.

### <a name="deploy-a-scale-unit-with-the-warehouse-management-workload"></a>Settu upp mælieiningu með vinnuálagi vöruhúsastjórnunar

Þú verður að vera með Dynamics 365 Supply Chain Management miðstöð og einingarkvarða sem hefur verið settur upp með vinnuálagi vöruhúsakerfisins. Frekari upplýsingar um skipulag og uppsetningarferli er að finna í [Einingarkvarðar í dreifðri blandaðri grannfræði](cloud-edge-landing-page.md).

### <a name="turn-on-required-features-in-feature-management"></a>Kveiktu á nauðsynlegum eiginleikum í eiginleikastjórnun

Nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæði til að kveikja á báðum eftirfarandi eiginleikum. (Báðir eiginleikar eru skráðir undir *Vöruhússtjórnun* mát.)

- Aftengja frágangsvinnu frá ASN (tilkynningum um sendingu)
- (Forútgáfa) Stuðningur kvörðunareiningar fyrir vöruhúsapantanir á inn- og útleið

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Hvernig vinnuálag vöruhúsakeyrslu virkar í einingakvörðum

Fyrir ferlana í vinnuálagi vöruhúsakerfisins eru gögnin samstillt milli miðstöðvar og einingarkvarða.

Mælieining getur aðeins haldið utan um gögnin sem hún á. Hugtakið um eignarétt gagna fyrir einingarkvarða hjálpar til við að koma í veg fyrir árekstra. Þess vegna er mikilvægt að skilja hvaða vinnslugögn eru í eigu annars vegar miðstöðvar og hins vegar einingarkvarða.

Það fer eftir viðskiptaferlunum hvort sama gagnafærslan geti breytt eignarhaldi milli miðstöðvar og einingakvarða. Dæmi um þessa atburðarás er gefið upp í eftirfarandi hluta.

> [!IMPORTANT]
> Sum gögn er hægt að búa til í bæði miðstöðinni og einingakvarðanum. Dæmin fela m.a. í sér **Númeraplötur** og **Rununúmer**. Boðið er upp á sérstaka meðhöndlun ágreinings í aðstæðum þar sem sama einkvæma færslan er stofnuð í bæði miðstöðinni og einingakvarðanum í sama samstillta ferlinu. Þegar þetta gerist mun næsta samstilling mistakast og þú verður fara í **Kerfisstjórnun > Fyrirspurnir > Fyrirspurnir um vinnuálag > Tvíteknar færslur** þar sem hægt er að skoða og sameina gögnin.

## <a name="outbound-process-flow"></a>Vinnsluflæði á útleið

Áður en þú setur upp vöruhúsastjórnunarvinnuálag á skýja- eða brúnkvarðaeiningu skaltu ganga úr skugga um að þú hafir *Stuðningur við mælieiningu til að losa pantanir á útleið í vöruhús* eiginleiki virkjaður á fyrirtækismiðstöðinni þinni. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Eiginleikaheiti:** *Stuðningur við mælieiningu til að losa pantanir á útleið í vöruhús*

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

## <a name="production-control"></a>Framleiðslustýring

Vinnuálag vöruhúsastjórnunar styður eftirfarandi þrjú flæði fyrir framleiðslu í vöruhúsastjórnun appinu:

- Bóka sem tilbúið og ganga frá
- Hefja framleiðslupöntun
- Skrá efnisnotkun

### <a name="report-as-finished-and-put-away"></a>Bóka sem tilbúið og ganga frá

Starfsmenn geta notað **Tilkynntu sem lokið og settu í burtu** flæði í Vöruhússtjórnun appinu til að tilkynna framleiðslu- eða runupöntun sem lokið. Þeir geta einnig tilkynnt um aukaafurðir og aukaafurðir í lotupöntun sem fullunnar. Þegar tilkynnt er um að verki sé lokið myndar kerfið venjulega frágangsvöruhúsavinnu á mælikvarðaeiningunni. Ef þú þarfnast ekki frágangsvinnu geturðu sett upp vinnustefnu þína til að sleppa því.

### <a name="start-production-order"></a>Hefja framleiðslupöntun

Starfsmenn geta notað **Hefja framleiðslupöntun** flæði í Vöruhússtjórnun appinu til að skrá upphaf framleiðslu- eða lotupöntunar.

### <a name="register-material-consumption"></a>Skrá efnisnotkun

Starfsmenn geta notað **Skrá efnisnotkun** flæði í vöruhúsastjórnunarappinu til að tilkynna efnisnotkun fyrir framleiðslu- eða lotupöntun. Tínslulistabók er síðan stofnuð fyrir tilkynnt efni á framleiðslu- eða runupöntun á mælikvarðaeiningunni. Færslubókarlínurnar gera efnislega frátekningu á neyslubirgðum. Þegar gögn eru samstillt á milli mælikvarðaeiningarinnar og miðstöðvarinnar, er tiltektarlista færslubók mynduð og bókuð á hubtilvikið.

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
- **Millifærslukvittun** – Með númeraplötu móttöku vinnslu.
- **Úthreyfing flutnings** – Einföld tiltekt og hleðsla.
- **Áfylling** – Að undanskildum hráefnum fyrir framleiðslu.
- **Frágangur á fullunnum vörum** – Eftir ferlið tilkynna sem tilbúna afurð.
- **Frágangur aukaafurða og hliðarafurða** – Eftir ferlið tilkynna sem tilbúna afurð.
<!-- - **Packed container picking** - After manual packing station processing. -->

Engar aðrar tegundir frumskjalavinnslu eða vöruhúsavinnu eru nú studdar á mælikvarðaeiningum. Til dæmis, þegar þú keyrir á móti vöruhúsaframkvæmdarvinnuálagi á mælieiningu, geturðu ekki notað móttökuferli söluskilapöntunar til að vinna úr skilapantunum. Þess í stað verður þessi vinnsla að fara fram af hubtilvikinu.

> [!NOTE]
> Valmyndaratriði og hnappar fartækis fyrir óstuddar aðgerðir eru ekki sýnd í _Farsímaforriti Warehouse Management_ þegar það er tengt við uppsetningu einingarkvarða.
>
> Nokkur aukaskref eru nauðsynleg til að setja upp vöruhússtjórnunarfarsímaforritið til að vinna gegn skýja- eða brúnkvarðaeiningu. Fyrir frekari upplýsingar, sjá [Stilltu Warehouse Management farsímaforritið fyrir skýja- og brúnkvarðaeiningar](cloud-edge-workload-setup-warehouse-app.md).
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
- Samnýting gagna milli fyrirtækja fyrir afurðir. <!-- Planned -->
- Vinnsla vöruhúsavinnu með athugasemdum sendingar.
- Vinna vinnslu í vöruhúsi með efnismeðhöndlun/sjálfvirkni vöruhúss.
- Myndir af afurðarsniðmátsgögnum (til dæmis í farsímaforriti Warehouse Management).

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
| Handvirkt pökkunarferli, þ.m.t úrvinnsla vinnunnar „Tiltekt pakkaðs gáms“ | Nr. <P>Sum vinnsla er hægt að framkvæma eftir upphaflegt tínsluferli sem er meðhöndlað af mælikvarðaeiningu, en ekki er mælt með því vegna eftirfarandi lokaðra aðgerða.</p>  | Nei |
| Fjarlægja gám úr hópi                                  | Nei  | Nei |
| Röðunarferli á útleið                                  | Nei  | Nei |
| Prentun á hleðslutengdum skjölum                           | Já | Já|
| Farmbréf og ASN-myndun                            | Nei  | Já|
| Staðfesting sendingar                                             | Nr.  | Já|
| Staðfesting sendingar með „Staðfesta og flytja“            | Nr.  | Já|
| Fylgiseðill og reikningsfærsla                        | Já | Nr. |
| Stutt tiltekt (sölu- og flutningspantanir)                    | Nei  | Já, án þess að fjarlægja frátekningar fyrir upprunaskjöl|
| Umframtiltekt (sölu-og flutningspantanir)                     | Nr.  | Já|
| Númeraplötur í samstæðu                                   | Nr.  | Já|
| Breyting vinnustaðsetninga (sölu-og flutningspantanir)         | Nei  | Já|
| Ljúka vinnu (sölu-og flutningspantanir)                    | Nei  | Já|
| Prenta vinnuskýrslu                                            | Já | Já|
| Bylgjumerki                                                   | Nei  | Já|
| Skipta vinnu                                                   | Nei  | Já|
| Úrvinnsla vinnu - Stjórnað af „Flutningshleðslu“            | Nr.  | Nr. |
| Minnka tiltekið magn                                       | Nr.  | Já|
| Bakfæra vinnu                                                 | Nr.  | Já|
| Bakfæra staðfestingu sendingar                                | Nr.  | Já|
| Beiðni um að hætta við vöruhúspöntunarlínur                      | Já | Nei, en beiðnin verður samþykkt eða henni hafnað |
| <p>Losa flutningspantanir fyrir móttöku</p><p>Þetta ferli mun sjálfkrafa eiga sér stað sem hluti af sendingarferli flutningspöntunar. Hins vegar er hægt að nota það handvirkt til að virkja móttöku númeraplötu í mælieiningu ef pöntunarlínum á innleið vöruhúss hefur verið hætt eða sem hluti af nýju vinnuálagsdreifingarferli.</p> | Já | Nr.|

### <a name="inbound"></a>Á innleið

Eftirfarandi tafla sýnir hvaða eiginleikar á útleið eru studdir og hvar þeir eru studdir þegar vinnuálag vöruhúsakerfis er notað í einingarkvörðum í skýi og edge.

| Vinna                                                          | Stöð | Vinnuálag vöruhúsakeyrslu í einingakvarða<BR>*(Vörur merktar „Já“ eiga aðeins við um vöruhúsapantanir)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Úrvinnsla&nbsp;upprunaskjals&nbsp;                             | Já | Nei |
| Hleðslu- og flutningsstjórnunarvinnsla                    | Já | Nei |
| Heildarkostnaður og móttaka á vörum í flutningi                       | Já | Nei |
| Staðfesting sendingar á innleið                                    | Já | Nei |
| Losun innkaupapöntunar til vöruhúss (vinnsla vöruhúsapöntunar) | Já | Nr. |
| Beiðni um að hætta við vöruhúspöntunarlínur                            | Já | Nei, en beiðnin verður samþykkt eða henni hafnað |
| Vinnsla innkaupapöntunar upprunaskjals vörukvittunar                        | Já | Nr. |
| Móttaka og frágangur innkaupapöntunarvöru                       | <p>Já,&nbsp;þegar&nbsp;það&nbsp;er ekki vöruhúsapöntun</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, þegar innkaupapöntun er ekki hluti af <i>hleðslu</i></p> |
| Móttaka og frágangur innkaupapöntunarlínu                       | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, þegar innkaupapöntun er ekki hluti af <i>hleðslu</i></p></p> |
| Móttaka og frágangur skilapöntunar                              | Já | Nei |
| Móttaka og frágangur blandaðrar númeraplötu                       | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Já |
| Móttaka farmvöru                                              | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nr. |
| Innkaupapöntun Númeraplötu móttekin og afhent              | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nr. |
| Flytjapöntun Móttaka á númeraplötu og setja í burtu             | Nr. | Já |
| Móttaka og frágangur flutningspöntunarvöru                       | Já | Nr. |
| Móttaka og frágangur flutningspöntunarlínu                       | Já | Nr. |
| Móttaka innkaupapantana með vanafhendingu                      | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Já, en aðeins með því að gera afturköllunarbeiðni úr miðstöðinni |
| Móttaka innkaupapöntunar með umframafhendingu                       | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Já  |
| Móttekið með stofnun vinnunnar *Dreifing frá dreifingarstöð*                 | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Móttekið með stofnun vinnunnar *Gæðapöntun*                  | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Móttekið með stofnun vinnunnar *Sýnataka gæðavinnu*          | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Móttekið með stofnun vinnunnar *Gæði í gæðaskoðun*       | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Móttekið með stofnun gæðapöntunar                            | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Nei |
| Úrvinnsla vinnu - Stjórnað af *Frágangur klasa*                 | Já | Nr. |
| Úrvinnsla vinnu með *Stutt tiltekt*                               | Já | Nr. |
| Hætta við vinnu (á innleið)                                            | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, en aðeins þegar<b>Afskrá kvittun þegar sagt er upp vinnu</b> valmöguleika á<b>Vöruhússtjórnunarfæribreytur</b> síða er hreinsuð</p> |
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
| Pakka í ívafnar númeraplötur                      | Já | Nei                           |
| Innskráning ökumanns                                    | Já | Nei                           |
| Útskráning ökumanns                                   | Já | Nei                           |
| Breyta ráðstöfunarkóða runu                      | Já | Já                          |
| Sýna opinn verkefnalista                             | Já | Já                          |
| Áfyllingarvinnsla fyrir lágm/hám og þröskuld svæðis| Já <p>Tillaga á ekki að taka með sömu staðsetningar sem hluta af fyrirspurnunum</p>| Já                          |
| Áfyllingarvinnsla hólfuð                  | Já  | Já<p>Athugið að ljúka verður uppsetningu á einingakvarðanum</p>                           |
| Loka og opna fyrir vinnu                             | Já | Já                          |
| Skipta um notanda                                        | Já | Já                          |
| Breyta vinnuhópi á vinnu                           | Já | Já                          |
| Hætta við vinnu                                        | Já | Já                          |

### <a name="production"></a>Framleiðsla

Eftirfarandi tafla dregur saman hvaða framleiðsluaðstæður vöruhúsakerfi eru studdar eins og er í vinnuálagi einingakvarða.

| Vinna | Stöð | Vinnuálag vöruhúsakeyrslu í einingakvarða |
|---------|-----|----------------------------------------------|
| Úrvinnsla frumskjala framleiðslupöntunar    | Já | Nr. |
| Losa í vöruhús                           | Já | Nr. |
| Hefja framleiðslupöntun                         | Já | Já|
| Búðu til vöruhúsapantanir                        | Já | Nr. |
| Beiðni um að hætta við vöruhúspöntunarlínur        | Já | Nei, en beiðnin verður samþykkt eða henni hafnað |
| Tilkynna sem lokið og frágangur tilbúinna afurða | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Já|
| Frágangur aukaafurða og hliðarafurða             | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Já|
| Skrá efnisnotkun                  | Já | Já|
| Bylgjuvinnsla framleiðslu                     | Já | Nr. |
| Tiltekt hráefnis                           | Já | Nr. |
| Kanban-frágangur                                | Já | Nr. |
| Kanban-tiltekt                                 | Já | Nr. |
| Tæma kanban                                   | Já | Nr. |
| Framleiðslurýrnun                               | Já | Nr. |
| Síðasta bretti framleiðslu                         | Já | Nr. |
| Áfylling hráefnis                     | Nr.  | Nr. |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Vinna með einingakvarða fyrir vöruhúsakeyrslu

Nokkrar runuvinnslur keyra á bæði miðstöðinni og einingarkvörðum.

Í miðstöð dreifingarinnar geturðu viðhaldið eftirfarandi runuverkum handvirkt:

- Hafa umsjón með eftirfarandi lotustörfum á **Vöruhússtjórnun \> Reglubundin verkefni \> Stýring á vinnuálagi á bak skrifstofu**:

    - Skilaboðaúrvinnsla kvörðunareiningar til miðstöðvar.
    - Skrá móttökur á upprunapöntun
    - Ljúka vöruhúsapöntunum

- Hafa umsjón með eftirfarandi lotustörfum á **Vöruhússtjórnun \> Reglubundin verkefni \> Vinnuálagsstjórnun**:

    - Skilaboðaúrvinnsla vöruhúsamiðstöðvar til kvörðunareiningar
    - Vinna úr móttökum á línum vöruhúsapöntunar fyrir bókun vöruhúsamóttöku

Í mælieiningadreifingum geturðu stjórnað eftirfarandi runuverkum á **Vöruhússtjórnun \> Reglubundin verkefni \> Vinnuálagsstjórnun**:

- Töflufærslur bylgjuvinnslu
- Skilaboðaúrvinnsla vöruhúsamiðstöðvar til kvörðunareiningar
- Vinna úr móttökum á línum vöruhúsapöntunar fyrir bókun vöruhúsamóttöku

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
