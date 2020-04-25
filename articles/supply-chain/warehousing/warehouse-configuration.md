---
title: Yfirlit yfir skilgreiningu vöruhúss
description: Þessi grein útskýrir hvernig eigi að stilla vöruhús. Þar er meðal annars að finna upplýsingar um hvernig á að virkja útlit vöruhús og ferli vöruhúsa.
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8cd436f1b8324335cc39ce54344db834dddebc9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204609"
---
# <a name="warehouse-configuration-overview"></a>Yfirlit yfir skilgreiningu vöruhúss

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig eigi að stilla vöruhús. Þar er meðal annars að finna upplýsingar um hvernig á að virkja útlit vöruhús og ferli vöruhúsa.

> [!NOTE]
> Þessi grein á við um aðgerðir í á einingunni **Vöruhúsakerfi** (ítarlegt vöruhús). Það á ekki við um aðgerðir vöruhúss í **birgðastjórnunarkerfi**.

## <a name="warehouse-layout"></a>Útlit Vöruhúss
Stjórnkerfi Vöruhúss í Supply Chain Management býður upp á sveigjanlega leiðir til að skilgreina útlit vöruhúss til að mæta síbreytilegum þörfum þannig að hægt er að ná bestu skilvirkni vöruhúss.

-   Þú getur að koma á háforgangs og lágforgangs geymslusvæði fyrir bestu vistun vöru.
-   Hægt er að skipta vöruhús í svæði til móts við mismunandi geymsluþarfir , s.s. kröfur um hitastig, eða ýmsa veltuhraði fyrir vörur.
-   Hægt er að tilgreina vöruhúsastaðsetninga á hvaða stigi sem er (t.d., svæði, vöruhús, gangur, rekka, hillu, og staðsetningu hólfa).
-   Hægt er að flokka staðsetningar með því að nota stillingar fyrir efnislegri afkastagetu.
-   Hægt er að stjórna hvernig vörur eru geymdar og teknar til, byggðar á reglum sem byggjast á fyrirspurnum.

Til að nota vöruhúsakerfi í Supply Chain Management, verður að stofna vöruhús og virkja það fyrir ítarlega eða sérhæfða stjórnun verkþátta í vöruhúsum. Á **Vöruhús** síðunni, veljið **Nota vöruhúsakerfisferli** valkost.

### <a name="zone-groups-zones-location-types-and-locations"></a>Staðaflokka, staði, staðsetningargerðum og staðsetningar

Sem hluti af ferlinu til að virkja útlit vöruhúss, verður að skilgreina staðaflokka vöruhúss og staði, forstillingar staðsetningar, gerðir staðsetninga, og staðsetningar.

-   **Svæðisflokkarflokka** – rökrétt eða efnisleg flokkun svæði innan vöruhúss.
-   **Svæði** – rökrétt eða efnisleg flokkun svæði innan vöruhúss.
-   **Forstillingar staðsetningar** – rökrétt eða efnisleg flokkun staðsetninga sem hafa sömu ferlisreglur fyrir staðsetningu vöruhúss (t.d. þar má geyma blöndu af mismunandi vörunúmerum, og sömu takmarkanir á efnislegt afkastagetu).
-   **Gerðir staðsetninga** – rökrétt eða efnisleg flokkun vöruhúsastaðsetninga. Til dæmis er hægt að stofna staðsetningargerð fyrir allar stigastaðsetningar. Áskildar stillingarnar í **Færibreytur vöruhúsakerfis** síðuna knýja ferlið við að skilgreina gerðir sviðsetningarstaðsetninga og er endanleg gerð sendingarstaðsetningar.
-   **Staðsetningar** – lægsta stig upplýsinga um staðsetningu. Staðsetningar er notað til að rekja hvar birgðir á lager er geymd og teknar til í vöruhúsi.

Einingar sem eru stofnaðar til að skilgreina útlit vöruhúss eru notuð í fyrirspurnum sem sett eru upp í vinnusniðmát til að knýja vinnupantanir í vöruhúsi. Því, þegar þú skilgreina staði,staðsetningagerðir og o.s.frv., hafðu í huga hvernig mismunandi svæði í vöruhúsinu eru notaðir fyrir mismunandi ferli. Þar að auki skal hafa þáttum í huga eins og eðliseiginleika tiltekins svæðis. Til dæmis gætu verið svæði þar sem aðeins er hægt að nota tiltekna gerð lyftara. Eða ef fyrirtæki þitt hefur bæði framleiðslu og fullunninna vara í sama aðstöðu gætirðu viljað stofna eitt vöruhús í Supply Chain Management en aðskilja síðan reksturinn með því að stofna tvo svæðishópa. Gefðu einingum þínum lýsandi nöfn, þannig að það er auðvelt að bera kennsl á þær þegar þú notar þá í fyrirspurnum um sniðmát.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Birgðamörk staðsetningar, forstillingar staðsetningar og fastar tiltektarstaðsetningar

Þú verður að íhuga efnislegt útlit vöruhúss, bæði til að ákvarða geymslugetu (Birgðamörk staðsetningar, forstillingar staðsetningar) og sem hluti af tilraunum þínum til að ná sem bestum vöruhúsaferlum. 

Birgðamörk staðsetningar hjálpa við að tryggja að vinna sé ekki stofnuð til að biðja um að birgðir séu settar á staðsetningu sem er ekki með efnislega afkastagetu til að taka við birgðunum. Til dæmis, ef einhver staðsetning innan vöruhúss getur aðeins verið með eitt bretti á staðsetningu, er hægt að virkja birgðamörk staðsetningar. **Magn** gildi má stilla **1**, og **Einingu** gildi má stilla **PL** innan tiltekinnar forstillingarflokks staðsetningar. 

Ef ítarlegri útreikninga þarf til að stýra skorður fyrir afkastagetu staðsetningar , er hægt að nota forstillingar staðsetningar. Í þessu tilfelli , er tekið tillit til þyngd og rúmmál þegar gerðar útreikningar fyrir afköst. 

Til að ná bestu útleiðaferlunum, ætti að meta hvort eigi að nota fastar tiltektarstaðsetningar og/eða pökkunarstaðsetningar. Oft er lágmarks/hámarks áfylling notað fyrir áfyllingarferlin frá magnsvæðum til fastra tiltektarstaðsetninga og margar fasta tiltektarstaðsetningar má virkja innan sama vöruhúss og fyrir afurðarafbrigði. Íhugaðu sveigjanleika sem er hægt að ná með því að sérstaka yfirflæðistaðsetningar eftirspurnaráfyllingar sem eru aðeins notaðar fyrir úrvinnslu áfyllingufyrir bylgju/hleðslu.

### <a name="location-setup-wizard"></a>Uppsetningarforrit staðsetningar

Til að stofna staðsetningar á snöggan hátt í vöruhúsi, er hægt að nota í **uppsetning Staðsetningar** leiðsagnarforritið. Sem Hluti af ferlinu er auðveldlega hægt að viðhalda snið fyrir nöfn staðsetninga.

## <a name="warehouse-processes"></a>Vöruhúsaferli
Sem hluti af skilgreiningu vöruhúss, er mikilvægt að virkja ferli vöruhúsa í samræmi við viðskiptaþarfir. Mikilvægustu þættir sem þarf að skilgreina eru bylgjusniðmát, vinnusniðmát, vinnuhópa og staðsetningarleiðbeiningar.

### <a name="wave-templates"></a>Bylgjusniðmát

Bylgjusniðmát hjálpa til við að virkja útleiðarferlið "Losun í vöruhús". Um leið og pöntunarlínurnar eru losaðar (annað hvort beint úr upprunaskjölum, gegnum runuvinnslur eða gegnum hleðslu sem þegar hafa verið stofnaðar), er virkni bylgjusniðmáts notuð. 

Hægt er að stofna þrjú bylgjusniðmát: 
-   **Sending**
-   **Framleiðslupöntun**
-   **Kanban** 

Færibreytur eru notaðar til að skilgreina hversu langt kerfið ætti að fara sjálfkrafa í vinnslu vinnu á útleið. Bylgjusniðmát er valin samkvæmt röð bylgjusniðmáts og skilyrðum sem eru tilgreindar í sniðmátinu. Ef sniðmát er skráð efst á röð, eru skilyrðin í því sniðmát athugað fyrst. Ef hægt er að uppfylla skilyrði, er bylgjusniðmátið unnið. Annars er skilyrði í næsta sniðmát athugað, o.s.frv. Því er gott að setja sniðmátið sem hefur sérstakasta skilyrði efst í róð bylgjusniðmáts, þannig að hún sé unnin fyrst. Til dæmis, óskað er að vinna alla vinnu fyrir tiltekna flutningsaðila í dag og tímabundið úrvinnslu frestað fyrir vinnu fyrir aðrar flutningsaðila. Í þessu tilfelli ætti að skrá bylgjusniðmát sem velur vinnu fyrir þann flutningsaðila að vera skráð hærri í röðinni en aðrar sniðmát. Annars gæti vinnu fyrir aðrar flutningsaðila verið unnin áður en vinnu fyrir þennan flutningsaðila er lokið. 

Tilgreina verður vinnsluaðferðir bylgju í hverri bylgjusniðmát. Aðferðir sem eru tiltækar eru mismunandi, það veltur á gerð bylgjusniðmáts.

### <a name="work-templates"></a>Vinnusniðmát

Skilgreiningar vinnusniðmáts spila mikilvægt hlutverk í skilgreiningu vinnuferlis fyrir vöruhúsakerfi. Þær tilgreina hvaða vinna er framkvæmd og hvernig vinnu er gerð. Sniðmát geta einnig innihaldið leiðbeiningarkóði sem tengir í staðsetningarleiðbeiningar til að ákvarða hvar finna er framkvæmd. Vinnusniðmát inniheldur fyrirspurnar sem tilgreinir skilyrðin fyrir vinnuna. Hvert sniðmát verður að innihalda minnst eina tiltektaraðgerð og einn Frágangsaðgerð til að knýja grunn vinnuaðgerðina við að flytja birgðir á lager frá einum stað á annan. 

Ef margir starfsmenn verða að geta vinna vinnu fyrir sumar af þínum vöruhúsaaðgerðir, gæti verið gott að nota hugtakið *sviðsetningar* fyrir birgðir og aðskilja framkvæmd vinnu í mismunandi vinnuklasa.

### <a name="work-pools"></a>Vinnuhópar

Vinnuhópar eru notaðir til að skipuleggja vinnu í flokka. Til dæmis er hægt að stofna vinnuhópi til að flokka vinnu sem fer í staðsetningu tiltekið vöruhús. Hægt er að úthluta á vinnuhópi að vinnusniðmát fyrir allar gerðir vinnu nema talningu. Fyrir reglulega talningu er hægt að tengja hóp vinnu á eftirfarandi síðum:

-   Áætlanir um reglulega talningu
-   Þröskuldar fyrir reglulega talningu
-   Vinna reglulegrar talningar eftir staðsetningu
-   Vinna reglulegrar talningar eftir vörum

Þegar vinnusniðmát eru notuð til að stofna vinnu er vinnuhópnum sjálfkrafa úthlutað á vinnu. 

Einnig er hægt að nota Kenni vinnuhópa til að takmarka gerð vinnu sem er stýrt til tiltekins starfsmanns vöruhúss , svo lengi sem aðgerðin er skilgreindur í valmyndaratriði viðeigandi fartækis .

### <a name="location-directives"></a>Staðsetningarleiðbeiningar

Eins og nafn gefur til kynna, eru staðsetningarleiðbeiningar notaðar til að beina vinnufærslur á viðeigandi staðsetningar í vöruhúsi. Með öðrum orðum þær tilgreina hvar á að taka til og ganga frá. 

Til að gera það auðveldara og fljótlegra að skilgreina aðgerðir sem eru tengd hverri línu fyrir staðsetningarleiðbeiningar, nota einn af skilgreindum aðferðum. Til dæmis er hægt að nota í **Auð staðsetning með engu verki á innleið** stjórnunarstefnu til að leita að lausum staðsetningar í vöruhúsi, eða hægt er að nota **FEFO runufrátekt** stjórnunarstefnu fyrir tiltekt fyrir sölu á útleið.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi](tasks/configure-locations-wms-enabled-warehouse.md)



