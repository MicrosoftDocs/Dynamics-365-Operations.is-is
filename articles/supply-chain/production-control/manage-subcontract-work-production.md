---
title: Stjórnun úthýsingarvinnu í framleiðslu
description: Þetta efnisatriði skýrir hvernig aðgerðum undirverktaka er stjórnað í Dynamics 365 Supply Chain Management. Þar er m.ö.o. skýrt hvernig framleiðsluaðgerðum sem er úthlutað á tilfang er stjórnað af lánardrottni.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup, ProdBOMVendorListPagePreviewPane, ProdBOMVendor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e80efc751ccf9243163d23ed48fd17923326f89
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579380"
---
# <a name="manage-subcontracting-work-in-production"></a>Stjórnun úthýsingarvinnu í framleiðslu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði skýrir hvernig aðgerðum undirverktaka er stjórnað í Dynamics 365 Supply Chain Management. Þar er m.ö.o. skýrt hvernig framleiðsluaðgerðum sem er úthlutað á tilfang er stjórnað af lánardrottni.

Í [framleiðsluferli](production-process-overview.md) er hægt að framkvæma vinnu með tilföngum sem eru í eigu eða er stjórnað af lánardrottni. Yfirleitt eru tilföng lánardrottins notuð til að jafna út tímabundna umfram eftirspurn sem fer yfir tiltækt framboð eigin tilfanga fyrirtækis. Lánardrottinn gæti einnig verið fær um að bjóða tiltekna [tilfangagetu](resource-capabilities.md) eða tilföng á lægra verði.  

Allt eftir því hvaða tilföng lánardrottins eru notuð í framleiðsluferli er [leið](routes-operations.md) oft með viðbótarvörustjórnunarkröfur þar sem efnið og hálfunnu vörurnar verður fyrst að flytja á vinnusvæði lánardrottins. Þá verður að flytja niðurstöðuna úr undirverktakaaðgerðinni annað hvort á staðsetninguna sem er úthlutað á næstu aðgerð eða í vöruhús fyrir fullunnar vörur.  

Þegar undirverktakaaðgerðir eða virkni eru notuð hefur það áhrif á öll aðgerðastigin, frá skilgreininu þeirra aðgerða sem framleiðslan krefst, kostnaði, spám, áætlanagerð og tímaáætlun, til birgðastjórnunar fyrir efni, hálfunnar vörur og fullunnar vörur. Lokst krefjast slík tilföng sinna eigin verkferla fyrir bókhald og kostnaðarstýringu.  

Fyrir innri tilföng er yfirleitt úthlutað föstu verði á tilteknu tímabilil. Kostnaður við tilföng undirverktaka byggist hins vegar á innkaupaverði tengdu þjónustunnar. Þjónustan er skilgreind sem önnur vara og er notuð til að knýja innkaupaferli fyrir tiltekna undirverktakaaðgerð.  

Sem stendur er ekki til nein ítarleg lýsing á hálfunnum vörum í Supply Chain Management. Fyrir framleiðslupöntun sem krefst fleiri en einnar aðgerðar til að geta breytt hráefni í fullunna vöru er fullunna varan ekki bókuð aftur inn í lager fyrr en í síðustu aðgerðinni. Hálfunnar vörur sem fyrri aðgerðir framleiða eru færðar til bókar í verk í vinnslu (WIP) en eru ekki bókaðar eða raktar í birgðum. Þótt hægt sé að skipta leiðum og uppskriftum (BOM) í margar smærri einingar eykur þessi aðferð fjölda vöru, uppskrifta og leiða sem þarf að fylgjast með.  

Til eru tvær aðferðir til þess að gera líkön af undirverktakavinnu fyrir framleiðsluaðgerðir. Þessar aðferðir eru mismunandi hvað varðar hvernig hægt er að gera líkön af undirverktakaferlinu, hvernig hálfunnar vörur eru sýndar í ferlinu og hvernig kostnaðarstýring er framkvæmd.

-   Úthýsing leiðaraðgerða í framleiðslupöntunum eða runupöntunum
    -   Þjónustuvaran verður að vera lagervara og verður að vera hluti af uppskriftinni.
    -   Þessi aðferð styður „fyrsta inn,fyrsta út“ (FIFO (fyrst inn - fyrst út)) eða staðalkostnað.
    -   Hálfunnar vörur eru sýndar með þjónustuvörunni í ferlinu.
    -   Kostnaðarstýring úthlutar kostnaði sem tengist úthýsingarverki á hráefniskostnaðinn..
-   Úthúsing á framleiðsluflæðiaðgerðum í lean production flæði
    -   Þjónustuvaran er ekki lagervara og er ekki hluti af uppskriftinni.
    -   Þessi aðferð notar innkaupasamningur sem þjónustusamningur.
    -   Þessi aðferð notar bakfærslukostnaðaraðferð.
    -   Þessi aðferð heimilar samanlögðog ósamstillt innkaup. (Efnisflæði er óháð innkaupaferli.)
    -   Kostnaðarstýring úthlutar undirverktakavinnu í sinni eigin sundurliðun kostnaðar.

## <a name="subcontracting-of-route-operations"></a>Úthýsing leiðaraðgerða
Til að nota úthýsingu leiðaraðgerða fyrir framleiðlu- eða runupantanir verður að skilgreina þjónustuvöruna sem er notuð við innkaup á þjónustunni sem vöru af gerðinni **Þjónusta**. Auk þess verður hún að vera af vörulíkanaflokki sem er með valkostinn **Lagervara** undir **Lagerstefna** stilltan á **Já**. Þessi valkostur tilgreinir hvort vara er bókfærð sem birgðir á vörureikningi (**Lagervara** = **Já**), eða hvort varan er færð sem kostnður á rekstrarreikningi (**Lagervara** = **Nei**). Þótt þessi hegðun gæti virst þverstæðukennd byggir hún á þeirri staðreynd að aðeins vörur með þessa stefnu stofna birgðafærslur sem hægt er að nota í kostnaðarstýringu til að reikna út áætlaðan kostnað og ákvarða raunkostnað þegar framleiðslupöntun er lokið.  

Til að vera talið með í áætlaun og kostnaðarútreikningi verður að bæta þjónustunni við uppskrifina. Uppskriftarlínan verður að vera af gerðinni **Lánardrottinn** og verður að vera úthlutað á þá leiðaraðgerð sem þjónustunni er úthlutað á. Þessi leiðaraðgerð verður að vera með kostnaðartilföng og tilfangaþörf sem vísar á tilföng af gerðinni **Lánardrottinn** sem tengir aðgerðina og tengda þjónustu við samsvarandi lánardrottnalykill.  

Þegar þessi skilgreining er notuð er stofnuð innkaupapöntun fyrir tengdu þjónustuvöruna á grundvelli áætlunar framleiðslupöntunar. Innkaupapöntun þjónustunnar er notuð sem grundvöllur fyrir úthýstu aðgerðina. Úthýstu vinnunni má stjórna gegnum listasíðuna **Úthýsing vinnu** í Framleiðslustýringu. Úthýsta vinnan er notuð til að senda hráefni og að lokuð hálfunnu vöruna til framleiðanda til að undirbúa aðgerðina. Hún er einnig notuð til að taka við vörunni sem verður til við úthýstu aðgerðina í vörumóttöku, þar sem þjónustuvaran er notuð til að auðkenna móttöku hálfunnar vöru. Þegar innkaupapöntunarlína er móttekin, er framleiðsluaðgerðin uppfærð sem lokið.  

Framleiðslupöntun getur innihaldið margar aðgerðir og hverri aðgerð má úthluta á mismunandi lánardrottinn. Þar af leiðandi er hugsanlegt að framleiðslupöntun sem tekur til alls ferlisins geti orðið til að stofna margar innkaupapantanir.

## <a name="subcontracting-of-production-flow-activities"></a>Úthýsing á framleiðsluflæðiaðgerðum
Í [lean-framleiðsla](lean-manufacturing-overview.md) er úthýsingarvinna byggð upp sem þjónusta sem er tengd við verkþátt [framleiðsluflæðis](tasks/create-production-flow-version.md) (efnisatriði í Verkefnaleiðbeiningum). Þess vegna er þessi gerð úthýsingar einnig kölluð [Verkþáttarbyggð úthýsing.](activity-based-subcontracting.md) Sérstök gerð kostnaðarflokks sem kallast **Bein útvistun** hefur verið kynnt til sögunnar og úthýsingarþjónusta er ekki lengur hluti af uppskrift (BOM) fulllunnu vörunnar. Þegar lean manufacturing er notað er öll virkni skilgrein með kanbönum sem hægt er að tengja við einn eða fleiri virkniþætti framleiðsluflæðis. Fram að þessu hljómar sú útskýring bara eins og skýring á framleiðslupöntunum. Hinsvegar, á meðan framleiðslupöntunum lýkur alltaf með fullunni vöru er hægt að stofna kanbön til að útvega hálfunna vöru. Ekki þarf að koma með nýtt framleiðslustig eða uppskriftarstig.  

Kanbanreglur geta verið mjög gagnvirkar og því er hægt að byggja mismunandi afbrigði birgða fyrir sömu vöruna á framleiðsluflæði. Þegar notuð er lean úthýsing eru efnisflæði og fjárhagslegt flæði aðskilin með skýrum hætti. Allt efnisflæði er táknað með kanban-virkniþáttum. Innkaupapantanir fyrir þjónustuvörurnar og bókanir á móttöku slíkrar þjónustu má gera sjálfvirkar, á grundvelli stöðu kanban-vinnslu í framleiðsluflæðinu. Kanban-vinnslu má hefja og ljúka jafnvel þótt ekki sé búið að stofna innkaupapantanir. Fylgiskjöl úthýsingar (innkaupapöntun og innkaupakvittun þjónustunnar) er hægt að safna upp eftir tímabili og þjónustu. Því er hægt að halda fjölda innkaupaskjala og -lína í lágmarki, jafnvel í margendurteknum aðgerðum þar sem lánardrottnar útvega úthýsta þjónustu í eins þáttar flæði.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Líkan úthýsingar í framleiðsluflæði

Í [lean-framleiðsluflæði](lean-manufacturing-modeling-lean-organization.md), má skilgreina verkþátt ferlis sem úthýstan þegar honum er úthlutað á vinnuflokk (tilfangaflokk) sem er með stakt lánardrottinstilfang. Þegar vinnuflokki er úthýst verður að tengja tengda verkþætti ferlis við virka innkaupasamningslínu sem inniheldur þjónustuatriðið og verð þjónustunnar. Þjónustusamningurinn fyrir verkþáttinn skilgreinir einnig útreikningshlutfallið milli vörumagnsins í kanban-vinnslunni og þjónustumagninu sem af leiðir. Þú getur valið hvort þjónustumagnið er reiknað út á grundvelli fjölda vinnsla, góða vörumagnsins sem tilkynnt er í vinnslunum eða heildarvörumagnsins (þetta heildarmagn innheldur vöru sem á að fleygja).  

Flutningsaðgerðir má einnig skilgreina sem úthýstar. Þessi skilgreining kemur sérstaklega fyrir þegar þú velur ábyrgan aðila fyrir flutningi í flutningsverkþættinum. Þegar þú velur **Farmsendandi** eða **Viðtakandi**, if samsvarandi uppruna- eða markvöruhús er vöruhús sem er stjórnað af lánardrottni, telst verkþættinum hafa verið úthýst. Þegar þú skal velja **Flutningsaðili**, er verkþætti alltaf úthýst. Líkt og úthýstir ferlisverkþættir verður úthýstur flutningsverkþáttur að tengjast þjónustusamningu áður en hægt er að virkja framleiðsluflæðið.

### <a name="backflush-costing"></a>Bakfærslukostnaðaraðferð

Kostnaðarbókhald vinnu undirverktaka er samþætt að fullu inn í kostnaðarútreikningslausn fyrir lean-framleiðslu (bakfærslukostnaðaraðferð). Þegar innkaupapöntunarkvittun þjónustunnar er bókuð eða þegar reikningsfærsla fer fram er kostnaði við þjónustuna úthlutað á framleiðsluflæði. Fyrir bakfærslukostnaðaraðferð, eru afbrigði við úthýstu þjónustuna reiknuð út með því að jafna úthýsta hluta staðalkostnaðar við móttekna vöru á móti raunverulegu magni móttekinnar og reikningsfærðrar þjónustu.

## <a name="material-supply-for-subcontracted-operations"></a>Framboð á hráefni fyrir úthýstar aðgerðir.
Hálfunnar vörur og annað tengt hráefni verður að flytja á þá staðsetningu þar sem á að framkvæma vinnuna efnislega. Þegar þú notar undirverktaka er þessi flutningur oft tengdur viðbótarflutningi til svæðis á vegum lánardrottins. Með því að úthluta efni í uppskrift til undirverktaka lýsir þú því yfir að setja verður efnið í bið á ílagsstaðsetningu forðaflokks fyrir úthlutað tilfang. Aðaláætlanagerð eða lean-áfylling ráðstafar síðan efninu á þennan stað.  

Til að búa til líkan af birgðum hjá lánardrottni eru bestu starfsvenjur í geiranum að skilgreina vöruhús sem er stjórnað af lánardrottni. Þú getur auðveldlega skilgreint vöruhús sem er stjórnað af lánardrottni með því að búa til nýtt vöruhús og og tengja lánardrottnalykil. Til að skjalfesta að flytja verði efnið til lánardrottins áður en hægt er að framkvæma aðgerð ættir þú að úthluta vöruhúsinu sem er stjórnað af lánardrottni til inntaksvöruhúss forðaflokksins sem geymir tilfangið.  

Til að bæta á efni í þessu vöruhúsi er hægt að nota margar aðferðir:

-   Flutningspantanir
-   Flutningabækur
-   Úttektarkanbön
-   Bein kaup á staðsetningu lánardrottins

Hálfunnar vörur eru undantekning á þessari reglu. Til að flytja hálfunnar vörur eru aðeins þessir valkostir í boði:

-   Fyrir framleiðslu- og runupantanir er aðeins hægt að flytja hálfunnar vörur rökrænt með því að nota færslubók tiltektarlista af listasíðunni **Vinna undirverktaka**. Þessi færslubók býr til skjal með fylgiseðli sem hægt er að nota til að flytja hálfunnið og óunnið efni til lánardrottins.
-   Fyrir undirverktakastarfsemi í framleiðsluflæði er flutningur á hálfunnum vörum skjalfestur með móttöku á úttektar- eða framleiðslukanbönum á staðsetningu lánardrottins. Til að búa til líkan af tilteknum flutningsverkþætti er hægt að ljúka framleiðslukanbani með frekari flutningsverkþætti.

**Athugið:** Framleiðsluleið fyrir staka framleiðslupöntun má ekki liggja yfir fleiri en eitt svæði. Þessi regla gildir einnig um vinnu undirverktaka. Af þessum sökum verður að skilgreina vöruhúsin sem standa fyrir staðsetningar efnis sem lánardrottinn stjórnar á sama svæði og innri tilföng sem eru notuð á leiðinni. Jafnvel þótt framleiðsluflæði geti farið yfir fleiri en eitt svæði geta þau ekki flutt hálfunnar afurðir frá einu svæði til annars þar sem sú aðgerð felur í sér breytingu á kostnaðargildi.  

Yfirleitt eru úttaksvöruhús og staðsetning forðaflokks undirverktaka tengd beint við vöruhúsið og staðsetningu næsta skrefs vinnslunnar á leiðinni eða í framleiðsluflæðinu. Þetta skipulag fækkar verkskýrslum eða fjölda frekari flutningsaðgerða sem gera verður líkan fyrir.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]