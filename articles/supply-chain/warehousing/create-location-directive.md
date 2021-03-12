---
title: Vinna með staðsetningarleiðbeiningar
description: Þetta efnisatriði útskýrir hvernig á að vinna með staðsetningarleiðbeiningar. Staðsetningarleiðbeiningar eru notandaskilgreindar reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar.
author: Mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b1b3bafb24ff6eb0c42d901fac3b6668cedf39ef
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963311"
---
# <a name="work-with-location-directives"></a>Vinna með staðsetningarleiðbeiningar

[!include [banner](../includes/banner.md)]

Staðsetningarleiðbeiningar eru reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar. Til dæmis, í sölupöntunarfærslu, ákvarða staðsetningarleiðbeiningar hvar vörurnar verða teknar til og hvar tilteknar vörur verða að setja. Staðsetningarleiðbeiningar samanstanda af haus og tengdum línum. Þær eru búnar til fyrir tilteknar *verkbeiðnigerðir*.

> [!NOTE]
> Athugasemd: Þetta efni á við aðgerðir í **Vöruhúsakerfi**. Það á ekki við um eiginleika í einingunni [Birgðastjórnun](../inventory/inventory-home-page.md).

Hægt er að nota staðsetningarleiðbeiningar til að framkvæma eftirfarandi verk:

- Frágangur varanna á innleið.
- Taka til og geyma vörur fyrri færslur á útleið.
- Sækja og setja hráefni fyrir framleiðslu.
- Fylla á staðsetningar.

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að stofna staðsetningarleiðbeiningu þarf að fylgja þessum skrefum til að ganga úr skugga um að forkröfur séu til staðar.

1. Gangið úr skugga um að kveikt sé á tilskildum leyfislykli. Farið í **Kerfisstjórnun \> Uppsetning \> Leyfisskilgreining**, stækkið leyfislykilinn **Viðskipti** og veljið síðan skilgreiningarlykilinn **Vöruhúsakerfi og flutningsstjórnun**. Athugið að stjórnendaaðgangur er nauðsynlegur fyrir þetta skref.
1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Vöruhús**.
1. Stofna vöruhús.
1. Í flýtiflipanum **Vöruhús** skal stilla valkostinn **Nota ferli vöruhúsastjórnunar** á *Já*.
1. Stofna staðsetningar, staðsetningargerðir, staðsetningarforstillingar og staðsetningarsnið. Frekari upplýsingar er að finna í [Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Stofna svæði og svæðisflokka. Frekari upplýsingar er að finna í [Uppsetning vöruhúss](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) og [Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="work-order-types-for-location-directives"></a>Verkbeiðnigerðir fyrir staðsetningarleiðbeiningar

Margir reitirnir sem hægt er að stilla fyrir staðsetningarleiðbeiningar eru eins í öllum verkbeiðnigerðunum. Hins vegar eru aðrir reitir sem tilheyra tilteknum verkbeiðnigerðum.

![Verkbeiðnigerðir staðsetningarleiðbeiningar](media/Location_Directives_Work_Order_Types.png "Verkbeiðnigerðir staðsetningarleiðbeininga")

> [!NOTE]
> Tvær verkbeiðnigerðir *Afturkölluð vinna* og *Regluleg talning* eru eingöngu notaðar af kerfinu. Ekki er hægt að búa til staðsetningarleiðbeiningar fyrir þessar verkbeiðnigerðir.

Töflurnar í eftirfarandi undirköflum sýna sameiginlega reiti og sérreit verkbeiðnigerðar sem eru í boði þegar staðsetningarleiðbeining er sett upp.

### <a name="fields-that-are-common-to-all-work-order-types"></a>Reitir sem eru sameiginlegir öllum verkbeiðnigerðum

Í eftirfarandi töflu er listi yfir þá reiti sem eru sameiginlegir öllum verkbeiðnigerðum.

| Flýtiflipi | Svæði |
|---|---|
| Staðsetningarleiðbeiningar | Vinnugerð |
| Staðsetningarleiðbeiningar | Vefsvæði |
| Staðsetningarleiðbeiningar | Vöruhús |
| Staðsetningarleiðbeiningar | Leiðbeiningarkóði |
| Staðsetningarleiðbeiningar | Margar birgðahaldseiningar |
| Línur | Raðnúmer |
| Línur | Frá-magn |
| Línur | Til magn |
| Línur | Eining |
| Línur | Finna magn |
| Línur | Takmarka eftir einingu |
| Línur | Slétta upp í einingu |
| Línur | Staðsetja umbúðamagn |
| Línur | Leyfa að skipta |
| Aðgerðir í staðsetningarleiðbeiningum | Raðnúmer |
| Aðgerðir í staðsetningarleiðbeiningum | Nafn |
| Aðgerðir í staðsetningarleiðbeiningum | Notkun fastrar staðsetningar |
| Aðgerðir í staðsetningarleiðbeiningum | Heimila neikvæðar birgðir |
| Aðgerðir í staðsetningarleiðbeiningum | Runa virk |
| Aðgerðir í staðsetningarleiðbeiningum | Stjórnunarstefna |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>Reitir sem eru sértækir fyrir verkbeiðnigerðir

Í eftirfarandi töflu er listi yfir þá reiti sem tilheyra ákveðnum verkbeiðnigerðum.

| Flýtiflipi | Svæði | Gerð verkbeiðni |
|---|---|---|
| Staðsetningarleiðbeiningar | Staðsetja eftir | Innkaupapantanir |
| Staðsetningarleiðbeiningar | Gildandi ráðstöfunarkóði | Innkaupapantanir |
| Staðsetningarleiðbeiningar | Ráðstöfunarkóði | Innkaupapantanir |
| Staðsetningarleiðbeiningar | Gildandi ráðstöfunarkóði | Frágangur á fullunnum vörum |
| Staðsetningarleiðbeiningar | Ráðstöfunarkóði | Frágangur á fullunnum vörum |
| Staðsetningarleiðbeiningar | Gildandi ráðstöfunarkóði | Skilapantanir |
| Staðsetningarleiðbeiningar | Ráðstöfunarkóði | Skilapantanir |
| Staðsetningarleiðbeiningar | Gildandi ráðstöfunarkóði | Kanban-frágangur |
| Staðsetningarleiðbeiningar | Gildandi ráðstöfunarkóði | Kanban-tiltekt |
| Línur | Sniðmát fyrir tafarlausa áfyllingu | Sölupantanir |
| Línur | Sniðmát fyrir tafarlausa áfyllingu | Tiltekt hráefnis |
| Línur | Sniðmát fyrir tafarlausa áfyllingu | Flutningsútgáfa |
| Línur | Sniðmát fyrir tafarlausa áfyllingu | Kanban-tiltekt |

## <a name="open-the-location-directives-page"></a>Opna síðu staðsetningarleiðbeininga

Til að opna síðuna **Staðsetningarleiðbeiningar** er farið í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.

Þaðan er hægt að skoða, búa til og breyta staðsetningarleiðbeiningum með því að nota skipanirnar á aðgerðasvæði. Í eftirstandandi hlutum í þessu efnisatriði er að finna upplýsingar um hvernig á að nota alla reitina sem eru í boði á síðunni.

## <a name="action-pane"></a>Aðgerðasvæði

Aðgerðasvæðið á síðunni **Staðsetningarleiðbeiningar** inniheldur hnappa sem hægt er að nota til að búa til, breyta og eyða leiðbeiningum (**Breyta**, **Ný** og **Eyða**). Þar er einnig að finna eftirfarandi hnappa sem gera þér kleift að stilla röðina sem staðsetningarleiðbeiningin er unnin í og skilgreina fyrirspurn sem skilgreinir skilyrðin fyrir því að nota staðsetningarleiðbeininguna:

- **Færa upp** – Færið völdu staðsetningarleiðbeininguna upp í röðinni. Til dæmis er hægt að færa hana úr raðnúmeri 4 í raðnúmer 3.
- **Færa niður** – Færið völdu staðsetningarleiðbeininguna niður í röðinni. Til dæmis er hægt að færa hana úr raðnúmeri 4 í raðnúmer 5.
- **Breyta fyrirspurn** – Opnið svarglugga þar sem hægt er að skilgreina skilyrðin sem valin staðsetningarleiðbeining á að vera unnin undir. Til dæmis er hægt að nota hana eingöngu í ákveðnu vöruhúsi.

## <a name="location-directives-header"></a>Haus staðsetningarleiðbeininga

Haus staðsetningarleiðbeiningar inniheldur eftirfarandi reiti fyrir raðnúmer og lýsandi heiti staðsetningarleiðbeiningarinnar:

- **Raðnúmer** – Þessi reitur bendir til þess að kerfið reyni að nota hverja staðsetningarleiðbeiningu í fyrir valda verkbeiðnigerð. Lágar tölur eru fyrst notaðar. Hægt er að breyta röðinni með því að nota hnappinn **Færa upp** og **Færa niður** á aðgerðasvæðinu.
- **Heiti** - Færið inn lýsandi heiti á staðsetningarleiðbeiningunni. Þetta heiti ætti að hjálpa til við að greina almennan tilgang tilskipunarinnar. Sláið til dæmis inn *Tiltekt sölupöntunar í vöruhús 24*.

## <a name="location-directives-fasttab"></a>Flýtiflipi staðsetningarleiðbeininga

Reitirnir í flýtiflipanum **Staðsetningarleiðbeiningar** eru sértækir fyrir verkbeiðnigerðina sem er valin í reitnum **Verkbeiðnigerð** í listasvæðinu.

- **Verkgerð** - Veljið gerð verks sem á að framkvæma. Tiltæk gildi fara eftir gerð birgðafærslu sem valin er í reitnum **Gerð verkbeiðni**. Veljið eitt af eftirfarandi gildum:

    - **Frágangur** – Staðsetningarleiðbeiningin reynir að finna ákjósanlegustu staðsetninguna til að ganga frá eða finna birgðir sem koma inn í kerfið við móttöku, framleiðslu eða leiðréttingu birgða. Hana er einnig hægt að nota til að skilgreina frágang á geymslustað eða útskot fyrir endanlegan afhendingarstað.
    - **Tiltekt** – Staðsetningarleiðbeiningin reynir að finna ákjósanlegustu staðsetningarnar til að taka frá efnislegar birgðir (þ.e. stofna vinnu). Hægt er að ljúka tiltekt (þ.e. hægt er að losa vinnulínu tiltektar), jafnvel þótt vinnunni sé ekki lokið. Notandinn getur lokið efnislegri tiltekt. Í kerfinu er þessi aðgerð tiltektarskref. Notandinn getur síðan hætt við í fartæki og lokið verkinu síðar. Hins vegar er vinnuhausnum fyrst lokað þegar lokafrágangi er lokið.

    > [!IMPORTANT]
    > Önnur gildi í reitnum **Verkgerð** eiga ekki við fyrir staðsetningarleiðbeiningar. Þau birtast aðeins vegna þess að reiturinn er ekki síaður til að passa við valda verkbeiðnigerð.

- **Svæði** – Þessi reitur er áskilinn vegna þess að staðsetningarleiðbeiningin þarf að geta ákvarðað svæðið og vöruhúsið sem það gildir um.
- **Vöruhús** – Þessi reitur er áskilinn vegna þess að staðsetningarleiðbeiningin þarf að geta ákvarðað svæðið og vöruhúsið sem það gildir um.
- **Leiðbeiningarkóði** - Veljið kóða leiðbeiningarkóðann til að tengja við vinnusniðmát eða áfyllingarsniðmát. Á síðunni **Leiðbeiningarkóði** er hægt að stofna nýja kóða sem má nota til að tengja vinnusniðmát eða áfyllingarsniðmát við staðsetningarleiðbeiningar. Leiðbeiningarkóða er einnig hægt að nota til að koma á tengingu milli hvaða vinnusniðmátslínu sem er og staðsetningarleiðbeiningar (t.d. útskot eða geymslustað).

    > [!TIP]
    > Ef leiðbeiningarkóði er stilltur leitar kerfið ekki í staðsetningarleiðbeiningum eftir raðnúmeri þegar búa þarf til vinnu. Þess í stað leitar það eftir leiðbeiningarkóða. Á þennan hátt er hægt að vera nákvæmari í sniðmáti staðsetningar sem er notað fyrir tiltekið skref í vinnusniðmáti, eins og skrefið fyrir geymslu á efni.

- **Margar birgðahaldseiningar** – Stillið þennan valkost á *Já* til að virkja margar birgðaeiningar sem á að nota á staðsetningu. Til dæmis verður að virkja margar birgðahaldseiningar fyrir staðsetningu útskots. Ef margar birgðahaldseiningar eru virkjaðar verður frágangsstaðsetningin tilgreind í vinnu eins og ætlast er til. Hins vegar getur frágangsstaðsetningin aðeins höndlað frágang á mörgum vörum (ef vinna felur í sér mismunandi birgðahaldseiningar sem þarf að taka til og ganga frá). Hún getur ekki höndlað frágang á einni birgðahaldseiningu. Ef þessi valkostur er stilltur á *Nei* verður frágangsstaðsetningin aðeins tilgreind ef frágangurinn er með aðeins eina birgðahaldseiningu.

    > [!IMPORTANT]
    > Til að geta notað bæði frágang á mörgum vörum og einni birgðahaldseiningu þarf að tilgreina tvær línur sem eru með sama skipulag og uppsetningu, en stilla þarf valkostinn **Margar birgðahaldseiningar** á *Já* fyrir eina línu og *Nei* fyrir hinar. Þar af leiðandi þarf fyrir frágangsaðgerðir að hafa tvær eins staðsetningarleiðbeiningar, jafnvel þótt ekki þurfi að greina á milli einnar birgðahaldseiningar og margra birgðahaldseininga á verkkenni. Ef báðar þessar staðsetningarleiðbeiningar eru ekki settar upp birtast oft óvæntar staðsetningar viðskiptaferla frá notaðri staðsetningarleiðbeiningu. Nota þarf sams konar uppsetningu fyrir staðsetningarleiðbeiningar sem eru með **Verkgerðina** *tiltekt* ef þarf að vinna úr pöntunum sem innihalda margar birgðahaldseiningar.

    Nota skal valkostinn **Margar birgðahaldseiningar** fyrir vinnulínur sem fást við fleiri en eitt vörunúmer. (Vörunúmerið verður autt í vinnulýsingunni og það verður sýnt sem **Mörg** á vinnslusíðunum í vöruhúsi forritsins.)

    Í dæmigerðu sýnidæmi er vinnusniðmát sett upp þannig að það er með fleiri en eitt par af tiltekt/frágangi. Í þessu tilviki gæti verið gott að leita að tiltekinni geymslustaðsetningu til að nota fyrir línurnar með **Verkgerðina** *Frágangur*.

    > [!NOTE]
    > Ef valkosturinn **Margar birgðahaldseiningar** er stilltur á *Já* er ekki hægt að velja **Breyta fyrirspurn** í aðgerðasvæðinu vegna þess að ekki er hægt að meta fyrirspurnina á stigi vörunnar þegar margar vörur eru til staðar. Til að tryggja að æskileg staðsetningarleiðbeining sé valin skal nota reitinn **Leiðbeiningarkóði** til að leiðbeina um val á staðsetningarleiðbeiningu sem tengist frágangslínum þar sem þessum leiðbeiningarkóða er úthlutað í vinnusniðmátinu.

    Nema alltaf sé unnið með annaðhvort aðgerð einnar vöru eða blandaðrar vöru, er mikilvægt að skilgreina tvær staðsetningarleiðbeiningar fyrir verkgerðina *Frágangur*: eina þar sem valkosturinn **Margar birgðahaldseiningar** er stilltur á *Já* og eina þar sem hann er stilltur á *Nei*.

- **Viðeigandi ráðstöfunarkóði** - Tilgreinið ef ráðstöfunarkóði staðsetningarleiðbeiningar þarf að samræmast ráðstöfunarkóðanum sem er notaður þegar varan er móttekin eða hvort hægt er að velja staðsetningarleiðbeininguna út frá hvaða ráðstöfunarkóða sem er. Ef valið er *Nákvæmt samræmi* og reitur fyrir **ráðstöfunarkóða** er auður, koma aðeins auðir ráðstöfunarkóðar til greina fyrir þessa staðsetningartilskipun.

    > [!NOTE]
    > Þessi reitur er aðeins í boði fyrir valdar gerðir verkbeiðni þar sem áfylling er leyfð. Ítarlegan lista er að finna í hlutanum [Reitir sem eru sértækir fyrir verkbeiðnigerðir](#fields-specific-types) fyrr í þessu efnisatriði.

- **Staðsetja eftir** - Tilgreinið hvort frágangsmagnið eigi að vera allt magnið í númeraplötunni eða hvort það eigi að vera vöru eftir vöru. Nota skal þennan reit til að tryggja að allt innihaldið á númeraplötu sé sett á eina staðsetningu og að kerfið leggi ekki til að skipt verði upp innihaldinu á nokkrar staðsetningar fyrir **ASN** (móttaka númeraplötu), móttaka **Blandaðrar númeraplötu** og móttökuferli **Klasa**. (Móttökuferli **Klasa** krefst þess að kveikt verði á eiginleikanum *Klasafrágangur*.) Hegðun fyrirspurnar staðsetningarleiðbeiningar, línanna og aðgerðir staðsetningarleiðbeiningar verða mismunandi, eftir því hvaða gildi er valið. Flýtiflipinn **Línur** er aðeins notaður þegar **Staðsetja eftir** er stilltur á *Vara*.

    > [!NOTE]
    > Þessi reitur er aðeins í boði fyrir valdar gerðir verkbeiðni þar sem áfylling er leyfð. Ítarlegan lista er að finna í hlutanum [Reitir sem eru sértækir fyrir verkbeiðnigerðir](#fields-specific-types).

- **Ráðstöfunarkóði** - Þessi reitur er notaður fyrir staðsetningarleiðbeiningar sem eru með verkbeiðnigerðina *Innkaupapantanir*, *Frágangur fullbúinnar vöru* eða *Skilapantanir* og verkgerðina *Frágangur*. Notið hann til að leiðbeina flæðinu til að nota tiltekna staðsetningarleiðbeiningu, allt eftir ráðstöfunarkóðanum sem starfskraftur valdi í vöruhúsaforriti. Til dæmis er hægt að beina skilavörum á eftirlitsstað áður en þeim er skilað í birgðir. Hægt er að tengja ráðstöfunarkóða við birgðastöðu. Á þennan hátt er hægt að nota hann til að breyta birgðastöðu sem hluta af móttökuferli. Þú getur til dæmis verið með ráðstöfunarkóða *QA* sem stillir birgðastöðuna á *QA*. Síðan er hægt að hafa sérstaka staðsetningarleiðbeiningu til að flytja birgðirnar á birgðageymslustaðsetningu.

    > [!NOTE]
    > Þessi reitur er aðeins í boði fyrir valdar gerðir verkbeiðni þar sem áfylling er leyfð. Ítarlegan lista er að finna í hlutanum [Reitir sem eru sértækir fyrir verkbeiðnigerðir](#fields-specific-types).

## <a name="lines-fasttab"></a>Flýtiflipinn Línur

Nota skal flýtiflipann **Línur** til að setja á skilyrði við að nota tengdar aðgerðir sem eru tilgreindar í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum**. Fyrir hverja línu er hægt að tilgreina lágmarksmagn og hámarksmagn sem aðgerðirnar eiga að eiga við um. Einnig er hægt að tilgreina að aðgerðirnar eigi að eiga við um tiltekna birgðaeiningu.

- **Raðnúmer** - Sláið inn röðina sem vinna skal hverja línu staðsetningarleiðbeiningar í fyrir valda verkgerð. Hægt er að breyta röðinni eins og þörf er á með því að nota hnappana **Færa upp** og **Færa niður** á tækjastikunni.
- **Frá magn** – Tilgreinið upphaf magnbilsins sem línan á við um. Tilgreinið magnið í mælieiningunni sem er valin í reitnum **Eining**.
- **Til magn** – Tilgreinið lok magnbilsins sem línan á við um. Tilgreinið magnið í mælieiningunni sem er valin í reitnum **Eining**.
- **Eining** - Velja mælieiningu fyrir vörurnar. Hægt er að tilgreina lágmarksmagn og hámarksmagnið sem á við leiðbeiningarnar eiga að gilda um, og hægt er að tilgreina að leiðbeiningarnar eigi að vera fyrir tiltekna birgðaeiningu. Reiturinn **Eining** er *aðeins* notaður fyrir magnáætlun. Til að ákvarða hvort lína staðsetningarleiðbeiningar eigi við allt notar kerfið magnið í einingunni sem er tilgreind í þeirri línu. Í hvert sinn það nær í línu staðsetningarleiðbeiningar mun kerfið reyna að umbreyta eftirspurnareiningunni í einingu sem er tilgreind í línunni. Ef umreikningur mælieiningar er ekki til staðar, fer kerfið yfir í næstu línu.
- **Staðsetja magn** – Þessi reitur er aðeins notaður þegar reynt er að ganga frá eða staðsetja vörur í vöruhúsinu. (Þess vegna á hann aðeins við þegar reiturinn **Verkgerð** er stilltur á *Frágangur*). Velja skal eitt af eftirfarandi gildum til að tilgreina magnið sem er notað til að meta hvort magn sé innan bilsins **Frá magn** og **Til magn**:

    - **Magn númeraplötu** ─ Notið magnið í númeraplötunni sem verið er að taka á móti.
    - **Einingamælt magn** – Notið magnið sem er notað við færsluna. Til dæmis ef tekið er á móti magni upp á 1.000 í vöruhúsi og því er skipt niður á 10 númeraplötur, hver þeirra er með magn upp á 100. Í þessu tilviki er hægt að nota magn upp á 1.000 vörur í staðinn fyrir númeraplötumagn upp á 100.
    - **Eftirstandandi magn** – Notið magnið sem þarf samt að taka á móti í innkaupapöntunarlínunni sem verið er að vinna úr.
    - **Væntanlegt magn** - Notið heildarmagn innkaupapöntunarlínunnar, burtséð frá því hvað hefur þegar verið móttekið.

- **Takmarka eftir einingu** – Þessi gátreitur gerir kleift að láta línu staðsetningarleiðbeiningar eiga við um mælieiningu eða margar mælieiningar. Veljið hann til að takmarka mælieiningar sem teljast gild valskilyrði fyrir línur staðsetningarleiðbeiningar. Þessi virkni virkar aðeins fyrir staðsetningarleiðbeiningar þar sem reiturinn **Verkgerð** er stilltur á *Tiltekt*.

    Til dæmis þegar magn er tekið frá, viltu aðeins taka frá bretti úr tilteknum staðsetningum. Í þessu tilviki munu línurnar takmarka þá röð við bretti á þann hátt að í hvert skipti sem eitthvert magn er minna eitt brett, verður það ekki valið fyrir staðsetningarleiðbeininguna.

    Athugið að gátreiturinn **Takmarka eftir einingu** stjórnar ekki einingunni eða einingunum sem eru notaðar í vinnulínum. Takmörkun einingar gildir aðeins um einingarnar sem eru gerðar tiltækar í gegnum röðunarflokk einingarinnar. Til dæmis tengist vara röðunarflokki einingar sem inniheldur báðar einingarnar *bretti* og *stk*. Mælieining hefur verið skilgreind þar sem 1 bretti = 100 stk, og staðsetningarleiðbeiningin notar virknina **Takmarka eftir einingu** aðeins fyrir bretti. Ennfremur hefur vinnusniðmát verið skilgreint sem takmarkar stofnun vinnuhauss við 50 stk. Í slíku tilfelli verða vinnulínur með 50 stk. stofnaðar. Til að tilgreina mælieiningu fyrir takmarkanir skal fylgja þessum skrefum:

    1. Í flýtiflipanum **Línur** skal velja **Takmarka eftir einingu** á tækjastiku. (Þessi hnappur verður aðeins tiltækur eftir að gátreiturinn **Takmarka eftir einingu** er valinn í línunni og síðan velja **Vista**.)
    1. Á síðunni **Takmarka eftir einingum**, í reitnum **Eining**, skal velja mælieininguna sem á að takmarka eftir fyrir ferli tiltektar og frágangs.

- **Námunda upp að einingu** - Þessi reitur vinnur með gátreitinn **Takmarka eftir einingu**. Ef til dæmis **Takmarka eftir einingu** og **Námunda upp að einingu** eru valin í línu staðsetningarleiðbeiningar, ætti verkið sem búið er til úr leiðbeiningunni fyrir tiltekt hráefnis að vera námunduð upp í eina af afgreiðslueiningunum sem eru tilgreindar á síðunni **Takmarka eftir einingu**.

    > [!NOTE]
    > Þessi **Námunda upp að einingu** uppsetning virkar aðeins fyrir verkbeiðnigerðina *Tiltekt hráefnis* og aðeins fyrir staðsetningarleiðbeiningar þar sem reiturinn **Verkgerð** er stilltur á *Tiltekt*.

- **Staðsetja umbúðamagn** - Ef gefið er upp umbúðamagn á sölupöntun, flutningspöntun eða framleiðslupöntun gerir þessi gátreitur þér kleift að takmarka kerfið þannig að það geti valið aðeins staðsetningar sem eru með a.m.k. þetta umbúðamagn.

    > [!NOTE]
    > Þessi virkni virkar aðeins með staðsetningarleiðbeiningum af gerðinni *Tiltekt*.

- **Leyfa að skipta** - Tilgreinið hvort staðsetningarleiðbeiningin geti skipt upp magninu sem tekið er á móti eða tekið frá yfir margar vöruhúsastaðsetningar, eða hvort staðsetja verði heildarmagnið í eina staðsetningu eða tekið frá úr einni staðsetningu til að búa til vinnu.
- **Sniðmát tafarlausrar áfyllingar** - Notið þennan reit til að stofna tengingu við áfyllingarsniðmát þannig að áfylling hefjist strax ef vörum er ekki úthlutað. Ef reiturinn er skilinn eftir auður, hefst vöruáfylling ekki fyrr en unnið hefur verið úr öllum línum staðsetningarleiðbeiningarinnar.

    > [!NOTE]
    > Þessi reitur er aðeins í boði fyrir valdar gerðir verkbeiðni þar sem áfylling er leyfð. Ítarlegan lista er að finna í hlutanum [Reitir sem eru sértækir fyrir verkbeiðnigerðir](#fields-specific-types).

## <a name="location-directive-actions-fasttab"></a>Flýtiflipi fyrir aðgerðir staðsetningarleiðbeininga

Hægt er að skilgreina margar aðgerðir í staðsetningarleiðbeiningum fyrir hverja línu. Einu sinni enn, númeraröð er notuð til að ákvarða röðun sem aðgerðir eru metnar í. Á þessu stigi er hægt að setja upp fyrirspurn til að skilgreina hvernig á að finna bestu staðsetningu í vöruhúsinu. Einnig er hægt að nota forskilgreint gildi fyrir **Stjórnunarstefnu** til að finna ákjósanlega staðsetningu.

- **Raðnúmer** - Þessi reitur sýnir röðina sem aðgerðirnar verða unnar í fyrir valda verkgerð. Hægt er að breyta röðinni með því að nota hnappinn **Færa upp** og **Færa niður** á tækjastikunni.
- **Heiti** - Sláið inn heiti á aðgerð staðsetningarleiðbeiningar. Veljið skýrt heiti svo aðgerðin sem á að framkvæma er greinileg út frá heitinu.
- **Notkun fastrar staðsetningar** - Tilgreinið hvaða staðsetningar staðsetningarleiðbeiningin á að taka til greina: Veljið eitt af eftirfarandi gildum:

    - **Fastar og lausar staðsetningar** - staðsetningarleiðbeiningin tekur tillit til allra staðsetninga.
    - **Aðeins fastar staðsetningar fyrir afurðina** - staðsetningarleiðbeiningin tekur aðeins tillit til fastra staðsetninga fyrir afurðir.
    - **Aðeins fastar staðsetningar fyrir afurðarafbrigðið** - staðsetningarleiðbeiningin tekur aðeins tillit til fastra staðsetninga fyrir afurðarafbrigði.

- **Heimila neikvæðar birgðir** - Veljið þennan gátreit til að heimila neikvæðar birgðir á staðsetningu tilgreinds vöruhúss í staðsetningarleiðbeiningum.
- **Runa virk** - Veljið þennan gátreit til að nota runuvinnslustefnu fyrir vörur sem nota runur. Mikilvægt er að velja þennan gátreit fyrir ferli sem nota staðsetningarleiðbeiningar til að finna staðsetningar til að sækja runuraktar vörur úr. Á þennan hátt er leit að staðsetningum sem geyma runuraktar vörur hafðar með. Ef þessi gátreitur er valinn og reiturinn **Stefna** er stilltur á *Engin* fer kerfið yfir í næstu aðgerðarlínuna.
- **Stefna** – Til að skilgreina aðgerðir á auðveldari og fljótlegri hátt sem tengjast hverri línu staðsetningarleiðbeiningar, er hægt að velja eina af eftirfarandi forskilgreindum stefnum:

    - **Engin** – Engin stefna verður notuð.
    - **Jafna umbúðamagn** - Þessi aðferð athugar hvort staðsetning tiltektar hafi tilgreint umbúðamagn. Þessi aðferð gildir aðeins þegar reiturinn **Vinnugerð** er stilltur á *Tiltekt*.
    - **Sameina** - Þessi aðferð sameinar vörur í tiltekinni staðsetningu þegar líkar vörur eru þegar fyrir hendi. Þessi aðferð gildir aðeins þegar reiturinn **Vinnugerð** er stilltur á *Frágangur*. Í dæmigerðri uppsetningu fyrir frágang er reynt að sameina fyrstu aðgerðarlínuna og síðan í annarri línunni er reynt að ganga frá án sameiningar. Sameining á vörum gerir seinni tiltektir skilvirkari.
    - **Frátekt á FEFO-runu** – Þessi stefna notar runufrátekningarnar fyrst útrunnið, fyrstu út (FEFO). Nota skal þetta þegar birgðir eru staðsettar með lokadag runu og er úthlutað fyrir frátekningu á runu. Aðeins er hægt að nota þessa aðferð fyrir vörur sem nota runu. Hún gildir aðeins þegar reiturinn **Vinnugerð** er stilltur á *Tiltekt*.
    - **Námunda upp í heila númeraplötu og FEFO-runu** – Þessi stefna sameinar einingar fyrir stefnurnar *Frátekt á FEFO-runu* og *Námunda upp í heila númeraplötu*. Hún gildir aðeins fyrir runuvörur og staðsetningarleiðbeiningar sem eru með verkgerðina *Tiltekt*. Línan verður að vera runuvirk til að nota stefnuna *Frátekt á FEFO-runu* og stefnan *Námunda upp í heila númeraplötu* er aðeins hægt að nota fyrir áfyllingu. Ef þessi stefna er skilgreind saman með birgðamörkum staðsetningar, getur hún valdið því að valin staðsetning frágangsvinnu verði ofhlaðin og birgðamörk verði hunsuð.
    - **Slétta upp í heila númeraplötu** - Þessi aðferð sléttar upp birgðamagnið þannig að það samsvari númeraplötumagninu sem er úthlutað á vörurnar sem þarf að taka til. Aðeins er hægt að nota þessa stefnu fyrir staðsetningarleiðbeiningar áfyllingar af gerðinni *Tiltekt*. Ef þessi stefna er skilgreind saman með birgðamörkum staðsetningar, getur hún valdið því að valin staðsetning frágangsvinnu verði ofhlaðin og birgðamörk verði hunsuð.
    - **Leitt af númerplötu** - Notið þessa stefnu þegar pöntun er losuð í vöruhúsið til að stofna vinnu tiltektar og frágangs. Hægt er að nota þessa nálgun fyrir margar númeraplötur. Þessi stefna reynir að taka frá og stofna tiltekt fyrir staðsetningarnar sem geyma umbeðnar númeraplötur sem hafa verið tengdar við flutningspöntunarlínurnar. Hins vegar, ef ekki er hægt að ljúka þessum aðgerðum en þú vilt samt stofna tiltekt, ættirðu að fara til baka í aðra stefnu fyrir aðgerðir staðsetningarleiðbeiningar. Það fer eftir kröfum viðskiptaferlisins, en þú gætir einnig vilja leita að birgðum á öðru svæði vöruhússins.
    - **Tóm staðsetning með engin verk á innleið** - Notið þessa stefnu til að finna tómar staðsetningar. Staðsetning er talin tóm ef hún hefur engar efnislegar birgðir og enga væntanlega vinnu á innleið. Aðeins er hægt að nota þessa stefnu fyrir staðsetningarleiðbeiningar sem eru með verkgerðina *Tiltekt*.
    - **FIFO aldursgreining staðsetningar** - Notið stefnuna fyrst inn, fyrst út (FIFO) til að senda bæði runuraktar vörur og ekki runuraktar vörur, byggt á dagsetningunni þegar birgðir voru færðar inn í vöruhúsið. Þessi eiginleiki getur verið mjög gagnlegur fyrir birgðir án runurakningar þar sem enga lokadagsetningu er hægt að nota til að raða eftir. FIFO-aðferðin finnur staðsetningu sem inniheldur elstu aldursdagsetninguna og hún úthlutar tiltekt eftir þessari aldursdagsetningu.
    - **LIFO aldursgreining staðsetningar** - Notið stefnuna síðast inn, síðast út (LIFO) til að senda bæði runuraktar vörur og ekki runuraktar vörur, byggt á dagsetningunni þegar birgðir voru færðar inn í vöruhúsið. Þessi eiginleiki getur verið mjög gagnlegur fyrir birgðir án runurakningar þar sem enga lokadagsetningu er hægt að nota til að raða eftir. FIFO-aðferðin finnur staðsetningu sem inniheldur nýjustu aldursdagsetninguna og hún úthlutar tiltekt eftir þessari aldursdagsetningu.

## <a name="example-using-location-directives"></a>Dæmi: Staðsetningarleiðbeiningar notaðar

Í þessu dæmi skal íhuga innkaupapöntunarferli þar sem staðsetningarleiðbeiningar verða að finna lausa afkastagetu í vöruhúsi fyrir birgðavara sem hafa einungis verið skráð í móttökusvæðinu. Fyrst þarftu að finna laust pláss innan vöruhússins með því að sameina við fyrirliggjandi lagerbirgðir. Ef sameining er ekki möguleg, þarftu að finna tóma staðsetningu.

Fyrir þessa atburðarás verður þú að skilgreina tvær aðgerðir staðsetningarleiðbeiningar. Fyrsta aðgerð í röðinni verður að nota í *Sameina* stjórnunarstefnu og annar ætti að nota í *Autt staðsetning með engu verki á innleið* stjórnunarstefnu. Nema þú skilgreinir þriðju aðgerð til að meðhöndla aðstæður yfirflæðis eru tvær niðurstöður mögulegar þegar engin afkastageta er í vöruhúsinu: hægt er að stofna vinnu jafnvel þótt engin staðsetningar eru skilgreindar eða ferli verkstofnunar getur mistekist. Niðurstaðan er ákvarðaður með uppsetningu á **staðsetningarleiðbeiningum** síðuna, þar sem hægt er að ákveða hvort að velja **Stöðva vinnu á misheppnuðum staðsetningarleiðbeiningum** valkost fyrir hverja gerð vinnupöntunar.

## <a name="next-step"></a>Næsta skref

Eftir að þú stofnar staðsetningarleiðbeiningar getur þú tengir hvert tilskipunarkóða með vinnusniðmátskóða fyrir vinnusköpun. Frekari upplýsingar er að finna í [Stýra vöruhúsavinnu með vinnusniðmátum og staðsetningarleiðbeiningum](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="additional-resources"></a>Frekari upplýsingar

- Myndskeið: [Ítarleg greining á grunnstillingum vöruhúsastjórnunar](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Hjálparefni: [Stýra vöruhúsavinnu með vinnusniðmát og staðsetningarleiðbeiningar](control-warehouse-location-directives.md)
