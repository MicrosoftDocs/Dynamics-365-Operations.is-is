---
title: Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra
description: Þetta efnisatriði veitir upplýsingar um eiginleikann sem gera kvörðunareiningum kleift að keyra valin ferli úr vinnuálagi vöruhúsakerfis.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516806"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ekki er öll virkni fyrirtækisins studd að fullu í opinni forútgáfu þegar einingarkvarðar vinnuálags eru notaðir. Gætið þess að nota aðeins þau ferli sem Þetta efnisatriði lýsir sérstaklega sem studd ferli.

## <a name="warehouse-execution-on-scale-units"></a>Framkvæmd vöruhúss í einingarkvörðum

Þessi eiginleiki gerir einingarkvörðum kleift að keyra valda ferla af möguleikum vöruhúsakerfisins. Einingarkvarðar í skýi keyra vinnuálagið í skýinu með því að nota úthlutaða úrvinnslugetu á völdu Microsoft Azure svæði. Fyrir einingarkvarða edge er hægt að keyra sumt vinnuálag út af fyrir sig á staðnum, jafnvel þótt einingarkvarðar séu tímabundið aftengdir skýinu.

Í þessu efnisatriði eru framkvæmdir vöruhúsakerfisins í vöruhúsi sem er skilgreint sem einingarkvarði þekktar sem *Framkvæmdakerfi vöruhúss* (*WES*).

## <a name="prerequisites"></a>Forkröfur

Þú verður að vera með Dynamics 365 Supply Chain Management miðstöð og einingarkvarða sem hefur verið settur upp með vinnuálagi vöruhúsakerfisins. Frekari upplýsingar um skipulag og uppsetningarferli er að finna í [Einingarkvarðar fyrir ský og edge fyrir vinnuálag framleiðslu og vöruhúsakerfis](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Hvernig WES-vinnuálagið virkar í einingarkvörðum

Fyrir ferlana í vinnuálagi vöruhúsakerfisins eru gögnin samstillt milli miðstöðvar og einingarkvarða.

Mælieining getur aðeins haldið utan um gögnin sem hún á. Hugtakið um eignarétt gagna fyrir einingarkvarða hjálpar til við að koma í veg fyrir árekstra. Þess vegna er mikilvægt að skilja hvaða ferlar eru í eigu annars vegar miðstöðvar og hins vegar einingarkvarða.

Einingarkvarðarnir eiga eftirfarandi gögn:

- **Gögn bylgjuvinnslu** - Valdar aðferðir bylgjuvinnslu eru meðhöndlaðar sem hluti af bylgjuvinnslu einingarkvarða.
- **Gögn verkvinnslu** - Eftirfarandi gerðir af úrvinnslu verkbeiðna eru studdar:

    - Birgðahreyfingar (handvirk hreyfing og hreyfing eftir vinnusniðmáti)
    - Innkaupapantanir (frágangsvinna í gegnum vöruhúsapöntun)
    - Sölupantanir (einföld tiltekt og hleðsla)

- **Móttökugögn vöruhúsapöntunar** - Þessi gögn eru aðeins notuð fyrir innkaupapantanir sem eru losaðar handvirkt til vöruhúss.
- **Gögn númeraplötu** - Númeraplötur er hægt að stofna í miðstöðinni og einingarkvarða. Búið er að úthluta meðhöndlun á árekstrum. Athugið að þessi gögn eru ekki bundin við vöruhús.

## <a name="outbound-process-flow"></a>Vinnsluflæði á útleið

Miðstöðin á eftirfarandi gögn:

- Öll upprunaskjöl, svo sem sölupantanirnar og flutningspantanir
- Úthlutun pöntunar og hleðsluvinnsla á útleið
- Losun í vöruhús, stofnun sendingar og ferlar bylgjustofnunar

Einingarkvarðarnir eiga raunverulegu bylgjuvinnsluna (á borð við verkúthlutun, áfyllingarvinnu og eftirspurnarvinnu) þegar bylgja hefur verið losuð. Starfskraftar í vöruhúsi geta þar af leiðandi unnið úr vinnu á útleið með vöruhúsaforriti sem er tengt við einingarkvarðann.

![Vinnsluflæði bylgju](./media/wes_wave_processing_flow.png "Vinnsluflæði bylgju")

## <a name="inbound-process-flow"></a>Vinnsluflæði á innleið

Miðstöðin á eftirfarandi gögn:

- Öll upprunaskjöl, svo sem innkaupapantanir og skilapantanir
- Hleðsluvinnsla á innleið

> [!NOTE]
> Innkaupapöntunarferli á innleið er í grunninn öðruvísi en ferli á útleið þar sem einingarkvarðinn sem sér um vinnsluna fer eftir því hvort pöntunin hafi verið losuð í vöruhúsið.

Ef verið er að nota ferlið *losa í vöruhús* eru vöruhúsapantanir stofnaðar og eignaréttur tengds móttökuferlis er úthlutaður til einingarkvarðans. Miðstöðin getur ekki skráð móttöku á innleið.

Starfskrafturinn getur keyrt móttökuferlið með vöruhúsaforriti sem er tengt við einingarkvarðann. Gögnin eru svo skráð af einingarkvarðanum og tilkynnt gagnvart vöruhúsapöntun á innleið. Stofnun og vinnsla frágangs sem fylgir í kjölfarið verður einnig meðhöndluð af einingarkvarðanum.

Ef þú ert ekki að nota ferlið *losa í vöruhús* og ert þar af leiðandi ekki að nota *vöruhúsapantanir*, getur miðstöðin unnið úr móttöku vöruhúss og úrvinnslu vinnu á eigin vegum úr einingarkvörðum.

![Vinnsluflæði á innleið](./media/wes_Inbound_flow.png "Vinnsluflæði á innleið")

## <a name="supported-processes-and-roles"></a>Studdar vinnslur og hlutverk

Ekki eru allir vöruhúsakerfisferlar studdir í vinnuálagi WES í einingarkvarða. Þess vegna er mælt með því að úthluta hlutverkum sem samsvara þeirri virkni sem er í boði fyrir hvern notanda.

Til að auðvelda þetta ferli er haft með sýnishlutverk sem kallast *Vöruhúsastjórnandi í vinnuálagi* í sýnigögnum í **Kerfisstjórnun \> Öryggi \> Öryggisstillingar**. Tilgangurinn með þessu hlutverki er sá að gera vöruhúsastjórnendum kleift að fá aðgang að WES í einingarkvarðanum. Hlutverkið veitir aðgang að síðunum sem eiga við í samhengi við vinnuálag sem er hýst í einingarkvarða.

Notandahlutverkum í einingarkvarða er úthlutað sem hluta af upphaflegri gagnasamstillingu úr miðstöðinni við einingarkvarðann.

Til að breyta hlutverkum sem úthlutað er á notanda skal fara í **Kerfisstjórnun \> Öryggi \> Úthluta notendum á hlutverk** í einingarkvarðanum. Notendur sem eru aðeins í hlutverki vöruhúsastjórnanda í einingarkvarðanum eiga aðeins að fá úthlutað hlutverkinu *Vöruhúsastjórnandi í vinnuálagi*. Þessi nálgun tryggir að þessir notendur hafi aðeins aðgang að studdri virkni. Fjarlægið öll önnur hlutverk sem þessum notanda er úthlutað.

Notendur sem eru í hlutverki vöruhúsastjórnanda í bæði miðstöðinni og einingarkvörðunum eiga að fá úthlutað fyrirliggjandi hlutverkinu *Starfskraftur í vöruhúsi*. Hafa skal í huga að þetta hlutverk veitir starfskröftum í vöruhúsi aðgang að eiginleikum (svo sem vinnslu flutningspöntunar) sem birtast í notandaviðmótinu en eru ekki studdir í einingarkvörðum sem stendur.

## <a name="supported-wes-processes"></a>Studd WES-ferli

Hægt er að virkja eftirfarandi vöruhúsaferli fyrir vinnuálag WES í einingarkvarða:

- Valdar bylgjuaðferðar fyrir sölupantanir og eftirspurnaráfyllingu
- Keyra verkbeiðnir úr sölupöntunum og eftirspurnaráfyllingu með vöruhúsaforriti
- Spyrjast fyrir um lagerbirgðir í vöruhúsaforriti
- Búa til og stjórna birgðahreyfingum með vöruhúsaforriti
- Skráning innkaupapantana og sinna frágangsvinnu með vöruhúsaforriti

Eftirfarandi verkbeiðnigerðir eru studdar fyrir vinnuálag WES sem stendur í uppsetningum einingarkvarða:

- Sölupantanir
- Áfylling
- Birgðahreyfing
- Innkaupapantanir sem eru tengdar við vöruhúsapantanir

Engin önnur úrvinnsla á upprunaskjölum er studd sem stendur í einingarkvörðum. Til dæmis, fyrir vinnuálag WES einingarkvarða, er ekki hægt að framkvæma eftirfarandi aðgerðir:

- Losa flutningspöntun.
- Vinna úr tiltektar- og afhendingaraðgerðum vöruhúss.

> [!IMPORTANT]
> Ef vinnuálag er notað í einingarkvarða er ekki hægt að keyra óstudd ferli fyrir tiltekið vöruhúsið í miðstöðinni.

Eftirfarandi virkni vöruhúsastjórnunar er ekki studd eins og er fyrir einingarkvarða:

- Ferli á innleið og útleið fyrir vörur sem eru með virkar rakningarvíddir (t.d. runu- eða raðnúmeravíddir)
- Meðhöndla stöðubreytingar birgða
- Vinnslu á birgðum sem eru með stöðugildi útilokunar
- Samþætting við gæðastjórnun
- Samþætting með framleiðslu
- Úrvinnsla á vörum með framleiðsluþyngd
- Úrvinnsla umframafhendingu og vanafhendingu
- Úrvinnsla á neikvæðum lagerbirgðum

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>Á útleið (eingöngu stutt fyrir sölupantanir og eftirspurnaráfyllingu)

Eftirfarandi tafla sýnir hvaða eiginleikar á útleið eru studdir og hvar þeir eru studdir þegar vinnuálag vöruhúsakerfis er notað í einingarkvörðum í skýi og edge.

> [!WARNING]
> Vegna þess að vinnsla sölupöntunar er studd, er ekki hægt að nota úrvinnslu vöruhúsakerfis á útleið fyrir flutningspantanir.
>
> Einhver vöruhúsavirkni verður ekki tiltæk í vöruhúsum sem keyra vinnuálag vöruhúsakerfis í einingarkvarða.

| Vinna                                                      | Stöð | Vinnuálag WES í einingarkvarða |
|--------------------------------------------------------------|-----|------------------------------|
| Úrvinnsla upprunaskjals                                   | Já | Ekkert |
| Hleðslu- og flutningsstjórnunarvinnsla                | Já | Ekkert |
| Losa í vöruhús                                         | Já | Ekkert |
| Sendingarsamstæða                                       | Ekkert  | Ekkert |
| Dreifing frá dreifingarstöð (tiltekt)                                 | Ekkert  | Ekkert |
| Bylgjuvinnsla sendingar                                     | Nei, en frágangur bylgjustöðunnar er meðhöndlaður í miðstöðinni. |<p>Já, en eftirfarandi eiginleikar eru ekki studdir:</p><ul><li>Samhliða stofnun vinnu</li><li>Hleðsluáætlun og röðun</li><li>Gámun</li><li>Prentun bylgjumerkis</li></li></ul><p><b>Athugið:</b> Aðgangur að miðstöðinni er nauðsynlegur til að ljúka við bylgjustöðuna sem hluti af bylgjuvinnslunni.</p> |
| Vinnsla vöruhúsavinnu (þ.m.t. prentun númeraplötu)     | Ekkert  | <p>Já, en aðeins fyrir eftirfarandi möguleika:</p><ul><li>Sölutiltekt (án notkunar virkra rakningarvídda)</li><li>Söluhleðsla (án notkunar virkra rakningarvídda)</li></ul> |
| Klasatiltekt                                              | Ekkert  | Ekkert |
| Pökkunarferli                                           | Ekkert  | Ekkert |
| Röðunarferli á útleið                                  | Ekkert  | Ekkert |
| Prentun á hleðslutengdum skjölum                           | Já | Ekkert |
| Farmbréf og ASN-myndun                            | Já | Ekkert |
| Staðfesting sendingar og vinnsla fylgiseðils                | Já | Ekkert |
| Stutt tiltekt (sölupantanir)                                 | Ekkert  | Ekkert |
| Afbókun vinnu                                            | Ekkert  | Ekkert |
| Breyta vinnustaðsetningum (sölupantanir)                      | Ekkert  | Ekkert |
| Ljúka vinnu (sölupantanir)                                 | Ekkert  | Ekkert |
| Loka og opna fyrir vinnu                                       | Ekkert  | Ekkert |
| Breyta um notanda                                                  | Ekkert  | Ekkert |
| Prenta vinnuskýrslu                                            | Ekkert  | Ekkert |
| Bylgjumerki                                                   | Ekkert  | Ekkert |
| Bakfæra vinnu                                                 | Ekkert  | Ekkert |

### <a name="inbound"></a>Á innleið

Eftirfarandi tafla sýnir hvaða eiginleikar á útleið eru studdir og hvar þeir eru studdir þegar vinnuálag vöruhúsakerfis er notað í einingarkvörðum í skýi og edge.

| Vinna                                                          | Stöð | Vinnuálag WES í einingarkvarða |
|------------------------------------------------------------------|-----|------------------------------|
| Úrvinnsla&nbsp;upprunaskjals&nbsp;                                       | Já | Ekkert |
| Hleðslu- og flutningsstjórnunarvinnsla                    | Já | Ekkert |
| Staðfesting sendingar                                            | Já | Ekkert |
| Losun innkaupapöntunar til vöruhúss (vinnsla vöruhúsapöntunar) | Já | Ekkert |
| Móttaka og frágangur innkaupapöntunarvöru                        | <p>Já,&nbsp;þegar&nbsp;það&nbsp;er ekki vöruhúsapöntun</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, þegar um er að ræða vöruhúsapöntun og þegar innkaupapöntun er ekki hluti af <i>hleðslu</i>. Hins vegar þarf að nota tvö valmyndaratriði fartækis, eitt fyrir móttöku (<i>Vörumóttaka innkaupapöntunar</i>) og hitt, með valkostinn <b>Nota fyrirliggjandi verk</b> virkan, til að vinna úr fráganginum.</p><p>Nei, þegar engin vöruhúsapöntun er til staðar.</p> |
| Móttaka og frágangur innkaupapöntunarlínu                        | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttaka og frágangur skilapöntunar                               | Já | Ekkert |
| Móttaka og frágangur blandaðrar númeraplötu                        | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttaka farmvöru                                              | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttaka og frágangur númeraplötu                              | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |
| Móttaka og frágangur flutningspöntunarvöru                        | Já | Ekkert |
| Móttaka og frágangur flutningspöntunarlínu                        | Já | Ekkert |
| Afbókun vinnu                                                | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | <p>Já, en valkosturinn <b>Afskrá innhreyfingu þegar verk er afturkallað</b> (á síðunni <b>Færibreytur vöruhúsakerfis</b>) er ekki studdur.</p> |
| Meðhöndlun innhreyfingarskjals afurða fyrir innkaupapöntun                        | Já | Ekkert |
| Stofnun verks fyrir dreifingu frá dreifingarstöð sem hluti af móttöku                 | <p>Já, þegar engin vöruhúsapöntun er til staðar</p><p>Nei, þegar um er að ræða vöruhúsapöntun</p> | Ekkert |

### <a name="warehouse-operations-and-exception-handing"></a>Vöruhúsaaðgerðir og meðhöndlun undantekningar

Eftirfarandi tafla sýnir hvaða eiginleikar vöruhúsaaðgerða og meðhöndlunarundantekningar eru studdir og hvar þeir eru studdir þegar vinnuálag vöruhúsakerfis er notað í einingarkvörðum í skýi og edge.

| Vinna                                            | Stöð | Vinnuálag WES í einingarkvarða |
|----------------------------------------------------|-----|------------------------------|
| Fyrirspurn vegna númeraplötu                              | Já | Já                          |
| Vörufyrirspurn                                       | Já | Já                          |
| Staðsetningarfyrirspurn                                   | Já | Já                          |
| Breyta vöruhúsi                                   | Já | Já                          |
| Hreyfing                                           | Ekkert  | Já                          |
| Hreyfingar eftir sniðmáti                               | Ekkert  | Já                          |
| Leiðrétting (inn/út)                                | Já | Ekkert                           |
| Regluleg talning og vinnsla talningarmisræmis | Já | Ekkert                           |
| Endurprenta merki (prentun númeraplötu)             | Já | Ekkert                           |
| Röðun númeraplötu                                | Já | Ekkert                           |
| Númeraplötuskipti                                | Já | Ekkert                           |
| Innskráning ökumanns                                    | Já | Ekkert                           |
| Útskráning ökumanns                                   | Já | Ekkert                           |
| Breyta ráðstöfunarkóða runu                      | Já | Ekkert                           |
| Sýna opinn verkefnalista                             | Já | Ekkert                           |
| Númeraplötur í samstæðu                         | Ekkert  | Ekkert                           |
| Fjarlægja gám úr hópi                        | Ekkert  | Ekkert                           |
| Hætta við vinnu                                        | Ekkert  | Ekkert                           |
| Lágm./hám. áfyllingarvinnsla                   | Ekkert  | Ekkert                           |
| Áfyllingarvinnsla hólfuð                  | Ekkert  | Ekkert                           |

### <a name="production"></a>Framleiðsla

Samþætting vöruhúsakerfis fyrir framleiðsluaðstæður er ekki studd sem stendur, eins og tilgreint er í eftirfarandi töflu.

| Vinna | Stöð | Vinnuálag WES í einingarkvarða |
|---------|-----|------------------------------|
| <p>Öll vöruhúsakerfisferli sem tengjast framleiðslu. Hér eru nokkur dæmi:</p><li>Losa í vöruhús</li><li>Bylgjuvinnsla framleiðslu</li><li>Tiltekt hráefnis</li><li>Frágangur á fullunnum vörum</li><li>Frágangur aukaafurða og hliðarafurða</li><li>Kanban-frágangur</li><li>Kanban-tiltekt</li><li>Hefja framleiðslupöntun</li><li>Framleiðslurýrnun</li><li>Síðasta bretti framleiðslu</li><li>Skrá efnisnotkun</li><li>Tæma kanban</li></ul> | Ekkert | Ekkert |

## <a name="maintaining-scale-units-for-wes"></a>Vinna með einingarkvörðum fyrir WES

Nokkrar runuvinnslur keyra á bæði miðstöðinni og einingarkvörðum.

Í uppsetningu miðstöðvar er hægt að vinna með runuvinnslur handvirkt. Hægt er að stjórna eftirfarandi þremur verkum í **Vöruhúsastjórnun \> Reglubundin verkefni \> Stjórnun vinnuálags í bakvinnslu**:

- Vinna úr uppfærslutilvikum vinnustöðu
- Vinna úr flutningstilviki fyrir stjórnun á bylgjukeyrslu
- Skrá móttökur á upprunapöntun

Í vinnuálaginu í einingarkvörðum er hægt að stjórna eftirfarandi tveimur runuvinnslum í **Vöruhúsastjórnun \> Reglubundin verkefni \> Stjórnun vinnuálags**:

- Töflufærslur bylgjuvinnslu
- Vinna úr flutningstilviki fyrir stjórnun á bylgjukeyrslu
