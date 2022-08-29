---
title: Pakkaðu ílát til sendingar
description: Þessi grein lýsir pökkunarferlinu sem gerir þér kleift að staðfesta birgðavörur og pakka þeim í ílát.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 171b9f1dcb1d4ece63bc0beeb71f45b9f8ae7bba
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220751"
---
# <a name="pack-containers-for-shipment"></a>Pakkaðu ílát til sendingar

[!include [banner](../../includes/banner.md)]

Gámapökkunarferlið gerir þér kleift að staðfesta birgðavörur og pakka þeim í gáma. Meðan á þessu ferli stendur velja vöruhúsastarfsmenn venjulega birgðavörur úr magngeymslusvæðum og flytja þær á pökkunarsvæði. Þar athuga margir vöruhúsastarfsmenn vörumagn og -gerðir og úthluta þeim á viðeigandi gámastærðir. Þegar gámur er fullpakkaður er hann lokaður og færður á bryggjusvæðið á útleið, þar sem hann er tilbúinn til sendingar.

Gámar tákna líkamlega uppbyggingu sem hlutum er pakkað í og þú getur fylgst með gámaupplýsingum í kerfinu. Þessar upplýsingar geta verið gagnlegar við skipulagningu flutninga, sérstaklega ef þú reiknar út sendingargjöld út frá gámum. Áður en þú sendir er hægt að skoða fjölda gáma sem eru notaðir í sendingu, gerðir gáma sem eru notaðar og líkamlegar stærðir hvers gáms (svo sem heildarrúmmál og þyngd).

Hægt er að nota nokkra tengda vöruhúsagetu á útleið með gámum. Frekari upplýsingar er hægt að finna í eftirfarandi greinum:

- [Bylgjugámavæðing](wave-containerization.md)
- [Flokkun á útleið](outbound-sorting.md)
- [Sending lítilla pakka](small-parcel-shipping.md)
- [Staðfesta og flytja](confirm-and-transfer.md)
- [Stilla mismunandi víddir fyrir pakka og geymslu](packing-vs-storage-dimensions.md)
- [Pökkunarvinna við pökkun á útgámum og vinnslu sendinga](packing-work.md)
<!-- KFM: Add link to upcoming topic when available (10.0.31): [Manual packing on the Warehouse management mobile app](manual-packing-on-the-warehouse-management-mobile-app.md) -->

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Settu upp vöruhúsið þitt til að nota handvirkar pökkunaraðgerðir

Það eru tvær helstu leiðir til að skipuleggja aðgerðirnar á útleið:

- **Bylgjusköpun og vinnsla** – Starfsmenn velja vörur á grundvelli vöruhúsavinnu á útleið. Þeir setja síðan hlutina beint á útflutningsstað þar sem þeir eru tilbúnir til sendingar strax. Fyrir upplýsingar um hvernig á að setja upp og nota þetta ferli, sjá [Bylgjusköpun og vinnsla](wave-processing.md).
- **Handvirk pökkun á pökkunarstöðvum** – Þetta ferli hefur aukaaðgerð á milli tínslu og sendingaraðgerða. Í stað þess að setja vöruna í a *flóahurð sendingarstaður*, verkamenn settu það í a *pökkunarstað*. Þeir stjórna síðan pökkunarferlinu á pökkunarstöðinni með því að nota **Pakki** síðu í vefþjóninum. Til að virkja þetta ferli verður þú að stilla kerfið þitt eins og lýst er í þessum hluta.

### <a name="set-up-warehouse-locations-for-packing"></a>Settu upp vöruhús fyrir pökkun

Þú verður að hafa að minnsta kosti einn pökkunarstað þar sem starfsmenn setja birgðavörur svo hægt sé að pakka þeim í gáma. Fyrir frekari upplýsingar um hvernig á að stofna vöruhúsastaðsetningar, sjá [Stilltu staðsetningar í WMS-virku vöruhúsi](tasks\configure-locations-wms-enabled-warehouse.md). Eftirfarandi undirkaflar lýsa því hvernig á að búa til og setja upp pökkunarstaði.

#### <a name="set-up-location-types-for-packing"></a>Settu upp staðsetningargerðir fyrir pökkun

Þú verður að skilgreina a *staðsetningargerð* fyrir pökkunarstaði. Hægt er að nota gerðir staðsetninga sem síunarvalkosti til að stýra mismunandi vöruhúsakerfisferlum. Nafn hverrar staðsetningartegundar lýsir venjulega einhverju um hvernig ætti að nota þá staðsetningargerð. Staðsetningargerðin sem þú setur upp hér verður að vera tengd hverri staðsetningu sem er notuð fyrir pökkunaraðgerðir.

Fylgdu þessum skrefum til að setja upp staðsetningargerð.

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Gerðir staðsetninga**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta staðsetningargerð við hnitanetið.
1. Stilltu eftirfarandi reiti fyrir nýju staðsetningargerðina:

    - **Staðsetningargerð** – Sláðu inn heiti fyrir staðsetningargerðina. Hvert nafn verður að vera einstakt og ætti að lýsa einhverju um hvernig staðsetningargerðinni er ætlað að nota.
    - **Lýsing** – Sláðu inn stutta lýsingu á staðsetningargerðinni.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Láttu kerfið vita um gerð pökkunarstaðsetningar

Eftir að þú hefur búið til staðsetningargerð verður þú að setja upp kerfið þitt til að þekkja það sem staðsetningargerðina til að nota fyrir pökkunaraðgerðir.

Fylgdu þessum skrefum til að stilla staðsetninguna sem er notuð fyrir pökkunaraðgerðir.

1. Fara til **Vöruhússtjórnun \> Uppsetning \> Vöruhússtjórnunarfæribreytur**
2. Á **Almennt** flipa, á **Staðsetningargerðir** flýtiflipann, stilltu **Gerð pökkunarstaðsetningar** reitnum að staðsetningargerðinni sem þú munt nota til að auðkenna pökkunarstöðvar.

> [!NOTE]
> Ef þú ert að uppfæra úr útgáfu af Microsoft Dynamics AX, hinn *Í pökkun* Staðan hefur verið fjarlægð úr sendingum og farmi, vegna þess að það virkaði ekki stöðugt og olli óþarfi gögnum. Þess vegna er **Í sendingum** og **Hleðsla í pökkun** listasíður hafa verið úreltar. Gámar sem þarf að pakka eru raktar á staðsetningarstigi.
>
> Í fyrri útgáfum skilgreindirðu pökkunarstaðinn með því að nota **Prófílauðkenni fyrir pökkunarstað** sviði á **Pökkun** flipi á **Vöruhússtjórnunarfæribreytur** síðu til að tilgreina a *staðsetningarsnið*. Í núverandi útgáfu notarðu **Gerð pökkunarstaðsetningar** sviði á **Almennt** flipi á **Vöruhússtjórnunarfæribreytur** síðu til að tilgreina a *staðsetningargerð*, eins og lýst er í þessari grein. Nýi reiturinn er betur í takt við ferlið við að bera kennsl á stöðvunarstaði og endanlega sendingarstaði.
>
> Þó þú getir haldið áfram að nota gamla **Prófílauðkenni fyrir pökkunarstað** reit, mælum við með að þú byrjar að nota nýja **Gerð pökkunarstaðsetningar** reit í staðinn, vegna þess að gamli reiturinn verður að lokum úreltur.
>
> Ef þú hreinsar stillinguna á gamla **Prófílauðkenni fyrir pökkunarstað** reitinn og vistaðu síðan síðuna, reiturinn verður varanlega óvirkur. Fyrir uppsetningar þar sem **Prófílauðkenni fyrir pökkunarstað** reiturinn hefur aldrei verið notaður, hann verður alltaf óvirkur. Eftir að þú hefur hreinsað stillinguna á **Prófílauðkenni fyrir pökkunarstað** reit, notaðu stillingarnar sem lýst er í þessari grein til að setja upp og bera kennsl á pökkunarstaðinn þinn.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Settu upp staðsetningarsnið fyrir pökkunarstaði

Hver *staðsetningarsnið* setur upplýsingar og reglur sem gilda um tengda staði. Þar sem þú þarft að minnsta kosti eina staðsetningu til að nota fyrir pökkunaraðgerðir, verður þú að búa til staðsetningarsnið fyrir hana til viðbótar við staðsetningargerð. Hvert snið er hægt að nota af hvaða fjölda staða sem er. Staðsetningar sem eru notaðar til pökkunar verða að vera settar upp til að rekja númeraplötur.

Fylgdu þessum skrefum til að setja upp staðsetningarsnið fyrir pökkunarstað.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.
1. Veldu annað hvort fyrirliggjandi prófíl af listaglugganum eða veldu **Nýtt** á aðgerðarrúðunni til að búa til nýjan.
1. Á haus nýja eða valda sniðsins skaltu stilla eftirfarandi reiti:

    - **Auðkenni staðsetningarprófíls** – Sláðu inn einstakt auðkenni fyrir prófílinn.
    - **Nafn** – Sláðu inn lýsandi heiti fyrir prófílinn.

1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Staðsetningarsnið** – Veldu staðsetningarsniðið sem á að nota fyrir núverandi staðsetningu. Staðsetningarsnið eru nafnakerfi sem er notað til að búa til einstök og samræmd nöfn fyrir mismunandi staðsetningarhólfsstöður sem eru notaðar í vöruhúsi. Ef þú ert ekki þegar með sniðið sem þú þarft geturðu búið það til með því að fara á **Vöruhússtjórnun \> Uppsetning \> Vöruhús \> Staðsetningarsnið**. Frekari upplýsingar er að finna í [Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Staðsetningargerð** – Veldu staðsetningargerðina sem er sett upp sem gerð pökkunarstaðsetningar á **Vöruhússtjórnunarfæribreytur** síðu, eins og lýst er fyrr í þessari grein.
    - **Notaðu númeraplötumælingu** – Fyrir pökkunarstaði, stilltu þennan valkost á *Já*. Kerfið verður að geta fylgst með auðkenni númeraplötu á pökkunarstöðum, svo það geti stjórnað pökkunarferlinu.
    - **Leyfa neikvæðar birgðir** – Fyrir pökkunarstaði, stilltu þennan valkost á *Nei*.
    - **Leyfa blandað atriði** – Fyrir pökkunarstaði, stilltu þennan valkost á *Já*. Þessi stilling er nauðsynleg vegna þess að mörg mismunandi vörunúmer eru venjulega færð á pökkunarstaðina á sama tíma.
    - **Leyfa blandaðar birgðastöður** – Fyrir pökkunarstaði, stilltu þennan valkost á *Já*. Þessi stilling er nauðsynleg vegna þess að vörur sem hafa mismunandi birgðastöðu eru venjulega fluttar á pökkunarstaðina á sama tíma.
    - **Leyfa blandaðar birgðalotur** – Fyrir pökkunarstaði, stilltu þennan valkost á *Já*. Þessi valkostur er sjálfkrafa stilltur á *Já* hvenær sem **Leyfa blandað atriði** valkostur er stilltur á *Já*.

#### <a name="set-up-packing-locations"></a>Settu upp pökkunarstaði

Þú verður að hafa að minnsta kosti einn *staðsetningu* þar sem starfsmenn munu setja birgðahluti sem þarf að pakka í gáma.

Fylgdu þessum skrefum til að bæta við pökkunarstað.

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við staðsetningu.
1. Stilltu eftirfarandi reiti fyrir nýju staðsetninguna:

    - **Vöruhús** – Tilgreindu vöruhúsið þar sem pökkunarstaðurinn verður að vera til.
    - **Staðsetning** – Sláðu inn nafn fyrir nýja staðsetninguna.
    - **Auðkenni staðsetningarprófíls** – Vertu viss um að tilgreina auðkennið sem þú bjóst til í fyrri hlutanum.

## <a name="set-up-the-packing-process"></a>Settu upp pökkunarferlið

Þessi hluti lýsir því hvernig á að stilla stillingar sem virkja pökkunarferlið og leyfa starfsmönnum að pakka birgðum í gáma.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Setja upp pökkunarreglur geymis

Hver *gámapökkunarstefnu* skilgreinir hvernig ílát á að vinna. Í hvert skipti sem þú býrð til nýjan gám muntu einnig velja gámapökkunarstefnu til að eiga við hann.

Fylgið þessum skrefum til að setja upp pökkunarreglur gáms.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Gámar \> Pökkunarreglur gáms**.
1. Veldu annaðhvort núverandi stefnu af listaglugganum eða veldu **Nýtt** á aðgerðarrúðunni til að búa til nýjan.
1. Í haus nýju eða völdu reglunnar skal stilla eftirfarandi gildi:

    - **Gámapökkunarstefna** – Sláðu inn einstakt heiti fyrir stefnuna.
    - **Lýsing** – Sláðu inn lýsandi heiti fyrir stefnuna.

1. Á **Yfirlit** flipanum, stilltu eftirfarandi reiti. Þessir reitir gera þér kleift að tilgreina hvaða aðgerðir eigi að grípa til þegar gámurinn er lokaður, hvort á að starfa með eða án vinnusköpunar og hvenær ílátið á að losa frá pökkunarstöðinni.

    - **Vöruhús** – Veldu vöruhúsið þar sem pökkunarstefnan á við.
    - **Sjálfgefin staðsetning fyrir endanlega sendingu** – Tilgreindu ákjósanlega staðsetningu fyrir ílátið eftir að honum hefur verið lokað. Þessi reitur er aðeins tiltækur þegar **Gámaútgáfustefna** reiturinn er stilltur á *Gera tiltækt á endanlegum sendingarstað*.
    - **Sjálfgefin staðsetning fyrir flokkun** – Þessi reitur er notaður með [flokkun á útleið](outbound-sorting.md) getu.
    - **Þyngdareining** – Veldu sjálfgefna mælieiningu sem á að nota þegar ílát er lokað og birtist. Venjulega mun þessi mælieining vera mælieiningin sem er notuð af kvarða á pökkunarstöðinni. Þessi reitur á við um stefnur með eða án vinnusköpunar.
    - **Stefna um lokun gáma** – Veldu einn af eftirfarandi valkostum til að skilgreina hvað ætti að gerast þegar ílátið er lokað:

        - *Sjálfvirk losun* – Gámurinn verður talinn losaður frá pökkunarstöðinni og aðgerðin sem tilgreind er í **Gámaútgáfustefna** reiturinn verður ræstur.
        - *Seinkun á útgáfu* – Gámurinn losnar ekki strax frá pökkunarstöðinni. Vöruhússtarfsmaður verður að losa það handvirkt síðar.
        - *Valfrjálst* – Á meðan starfsmaður er að loka gámnum mun hann geta valið hvort gámnum skuli sleppt.

        Ef pökkunarstöðin meðhöndlar aðallega staka gáma sem eru fluttir beint til viðskiptavina er eðlilegast að losa gámana strax. Ef pökkunarstöðin sér um sendingar sem samanstanda af mörgum gámum eða jafnvel brettum er líklega best að fresta losun þar til allri sendingunni eða brettinu hefur verið pakkað og tilbúið til afhendingar.

    - **Gámaútgáfustefna** – Veldu einn af eftirfarandi valkostum til að skilgreina hvað ætti að gerast þegar ílátið er losað af pökkunarstaðnum:

        - *Gera tiltækt á endanlegum sendingarstað* – Uppfærðu gáminn á endanlegan sendingarstað. Ef þú velur þennan valkost skaltu nota **Sjálfgefin staðsetning fyrir endanlega sendingu** reit til að tilgreina valinn stað fyrir gáminn eftir að honum er lokað.
        - *Búðu til verk til að flytja gám frá pökkunarstöð* – Búðu til vinnu til að flytja gáminn frá pökkunarstöðinni á uppsetningarsvæðið eða beint að flóahurðinni. Nota **Vinnusniðmát** reit til að tilgreina vinnusniðmátið sem ætti að nota þegar verk er búið til fyrir ílátið.
        - *Úthlutaðu íláti á flokkunarstöðu á útleið* – Þessi valkostur er notaður með [flokkun á útleið](outbound-sorting.md) getu.

        Í flestum tilfellum mælum við með því að þú stofnir verk til að færa gáma, því þessi nálgun endurspeglar betur raunveruleg handvirk ferla í vöruhúsinu. Hins vegar, fyrir einfaldar aðstæður, eða aðstæður þar sem pökkunarstöðin er staðsett beint á flóadyrasvæðinu, gæti verið æskilegra að gámurinn sé strax tiltækur á loka sendingarstaðnum.

    - **Vinnusniðmát** – Veldu vinnusniðmátið sem á að nota þegar verk er búið til fyrir ílátið. Þessi reitur er aðeins tiltækur þegar **Gámaútgáfustefna** reiturinn er stilltur á *Búðu til verk til að flytja gám frá pökkunarstöð* og tengist tegund verkbeiðni sem er nefnd *Pökkuð gámatínsla*. Fyrir frekari upplýsingar, sjá [Vinnusniðmát og staðsetningarleiðbeiningar](control-warehouse-location-directives.md).

    Í þeim skrefum sem eftir eru muntu stilla stillingar sem tengjast *birtast*. Birting er ferlið við að tilgreina þyngd gáms, gámahóps eða sendingar, ásamt rakningarauðkenni sem er móttekið frá flutningsaðila. Dynamics 365 Supply Chain Management er ekki samþætt við ytri flutningsþjónustukerfi. Þess í stað verða starfsmenn vöruhúsa að prenta út merkimiða sem berast frá flutningsaðilanum og skanna síðan rakningarnúmer þegar þeir ljúka upplýsingaskránni.

    Vegna þess að kröfur eru mismunandi frá viðskiptavinum til viðskiptavina, og jafnvel frá sendingu til sendingar, leyfa pökkunarstefnur verulegan sveigjanleika í verkflæðinu. Þú getur sett upp upplýsingaskrá fyrir gáma, gámahópa og sendingar í hvaða samsetningu sem er.

    Ef þú ert að nota margþrepa upplýsingaskrá, verða starfsmenn að birta alla gáma áður en þeir birta tengda gámahópinn og þeir verða að birta alla gámahópa áður en þeir birta tengda sendinguna.

1. Á **Gámaskrá** Flýtiflipi, stilltu eftirfarandi reiti:

    - **Sjálfvirk upplýsingaskrá við lokun gáma** – Stilltu þennan valkost á *Já* að beita upplýsingaskrá sem hluta af lokunarferli gáma. Ef þú ert ekki að nota samþættingu flutninga verður að skrá upplýsingarnar handvirkt.
    - **Augljósar kröfur um ílát** – Veldu einn af eftirfarandi valkostum:

        - *Enginn* – Ekkert birtingarferli verður notað.
        - *Handbók* - Krafist er opinberunar í pökkunarvinnuflæðinu. Kerfið mun ekki leyfa að ílát sé lokað eða sleppt fyrr en birtingu er lokið.
        - *Samgöngustjórnun* - Birting verður unnin með flutningsstjórnunarvélum (TMS). Vegna þess að þessi valkostur krefst sérsniðinnar þróunar til að innleiða ákveðna vél fyrir flutningsaðilann mun hann ekki virka beint úr kassanum í núverandi útgáfu.

    - **Prentaðu innihald ílátsins** – Stilltu þennan valkost á *Já* til að prenta sjálfkrafa skýrslu um innihald gáma þegar gámur er skráður sem lokaður. Skýrsluna er einnig hægt að prenta eftir beiðni.

1. Á **Upplýsingaskrá gámahóps** Flýtiflipi, í **Augljósar kröfur til gámahóps** reit, veldu einn af eftirfarandi valkostum:

    - *Enginn* – Upplýsingaskrá gámahópsins verður ekki tekin með sem krafa í pökkunarverkflæðinu.
    - *Handbók* – Upplýsingaskrá gámahópsins verður innifalin sem krafa í pökkunarvinnuflæðinu. Loka þarf öllum ílátum sem eru í hópnum áður en hægt er að birta hópinn. Veldu þennan valkost ef þú þarft að fylla út upplýsingaskrá fyrir hvern gámahóp sem er pakkað á pökkunarstöðinni. Þú velur venjulega þennan valkost ef gámum er pakkað á bretti og allt brettið kemur fram.

    > [!NOTE]
    > Núverandi útgáfa styður ekki upplýsingaskrár fyrir gámahópa og það er enginn TMS vélstuðningur fyrir gámahópa.

1. Á **Sendingarskrá** Flýtiflipi, stilltu eftirfarandi reiti:

    - **Augljósar kröfur um sendingu** – Veldu einn af eftirfarandi valkostum:

        - *Enginn* – Upplýsingaskrá sendingar verður ekki innifalin sem krafa í pökkunarferlinu.
        - *Handbók* – Upplýsingaskrá sendingar verður innifalin sem krafa í pökkunarferlinu. Engum gámum fyrir sendingu er hægt að losa fyrr en birtingu er lokið.
        - *Samgöngustjórnun* - Birting verður gerð í gegnum TMS hraðavélar. Vegna þess að þessi valkostur krefst sérsniðinnar þróunar til að innleiða ákveðna vél fyrir flutningsaðilann mun hann ekki virka beint úr kassanum í núverandi útgáfu.

        Sendingarskrá ætti að vera virkjuð ef þú þarft að fylla út upplýsingaskrá fyrir alla sendinguna sem er pakkað á pökkunarstöðinni. Það er venjulega notað þegar krafist er einnar samstæðu upplýsingaskrár jafnvel þó að sendingin samanstandi af mörgum gámum eða gámahópum.

    - **Prentaðu fylgiseðil** – Stilltu þennan valkost á *Já* til að prenta fylgiseðilinn sjálfkrafa sem hluta af sendingarskránni. Einnig er hægt að prenta fylgiseðilinn ef óskað er.

### <a name="set-up-container-types"></a>Setja upp gámagerðir

Meðan á handvirku pökkunarferlinu stendur verður að búa til ílát áður en hægt er að pakka hlutum inn í þá. Hver ílát verður að byggjast á a *gerð gáma*, sem skilgreinir hámarks líkamlegt rúmmál og þyngdargetu gáms.

Fylgdu þessum skrefum til að búa til gámagerð.

1. Fara til **Vöruhússtjórnun \> Uppsetning \> Gámar \> Gámategundir**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við gerð gáma.
1. Stilltu eftirfarandi reiti fyrir nýju gámagerðina:

    - **Gámategundarkóði** – Sláðu inn einstakt auðkenni fyrir gámagerðina.
    - **Lýsing** – Færið inn lýsingu á nýju gámagerðinni.
    - **Tare þyngd** – Sláðu inn raunverulega eða áætlaða þyngd ílátsins.
    - **Hámarks nettóþyngd** – Sláðu inn hámarksþyngd sem ílátið getur haldið.

1. Í **Stærðir gáma** kafla, í **Lengd**, **·**, **·**, og **Bindi** reiti, sláðu inn líkamlegar stærðir ílátsins sjálfs.
1. Í **Hámark** kafla, í **Lengd**, **·**, **·**, og **Bindi** reiti, sláðu inn hámarks efnisstærðir sem ílátið getur séð um.
1. Hægt er að skilgreina viðbótareiginleika fyrir gámagerðir sem eru tengdar öðrum aðgerðum sem nota gáma. Fyrir frekari upplýsingar, sjá [Gámavæðing](wave-containerization.md).

> [!NOTE]
> Fyrir handvirka pökkunarferlið notar kerfið aðeins verðmæti **Hámarks nettóþyngd** sviði og verðmæti **Bindi** sviði í **Hámark** kafla.

### <a name="set-up-packing-profiles"></a>Setja upp pökkunarforstillingar

*Pökkunarsnið* eru nauðsynlegar fyrir pökkunarferlið. Þeir geta verið valdir eða stilltir sjálfgefið þegar þú byrjar pökkunaraðgerð á **Pakki** síðu.

Fylgið þessum skrefum til að setja upp forstillingu umbúða.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Forstillingar umbúða**.
1. Veldu annað hvort fyrirliggjandi prófíl af listaglugganum eða veldu **Nýtt** á aðgerðarrúðunni til að búa til nýjan.
1. Á haus nýja eða valda sniðsins skaltu stilla eftirfarandi reiti:

    - **Pökkunarprófílauðkenni** – Sláðu inn stutt auðkenni fyrir prófílinn.
    - **Lýsing** – Sláðu inn lýsingu á pökkunarsniðinu.
    - **Gámapökkunarstefna** – Veldu pökkunarstefnuna sem á við sniðið. Fyrir frekari upplýsingar, sjá [Settu upp gámapökkunarreglur](#packing-policy) kafla þessarar greinar.
    - **Gámaauðkennisstilling** – Veldu hvort gámaauðkenni skuli myndast sjálfkrafa þegar gámur er búinn til, eða hvort það þarf að búa til handvirkt.
    - **Gerð gáma** – Veldu gámagerðina sem er sjálfgefið notuð þegar nýr gámur er búinn til.
    - **Búðu til gám sjálfkrafa við lok gámsins** – Veljið þennan gátreit til að búa til nýjan gám sjálfkrafa ef fyrri gámurinn er lokaður og ein eða fleiri línur eru eftir í núverandi sendingu.

### <a name="set-up-warehouse-workers"></a>Settu upp lagerstarfsmenn

Sérhver notandi eða starfsmaður sem pakkar gámum með því að nota **Pakki** síðu vefþjónsins eða *Pökkun* virknikóði í Vöruhússtjórnun farsímaforritinu verður að hafa notandareikning sem er tengdur við a *starfsmaður/manneskja* skrá sem nauðsynlegum öryggisaðgangsréttindum er úthlutað til. (Nánari upplýsingar um hvernig á að setja upp notendur er að finna í [Búðu til nýja notendur](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md) .)

Fylgdu þessum skrefum til að setja upp a *starfsmaður/manneskja* skrá fyrir pökkunarferlið.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Starfskraftur**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við vinnunotanda.
1. Stilltu **Vinnumaður** reit í núverandi starfsmannsskrá sem er skilgreind í **Mannauður** mát fyrir notandann sem mun ljúka pökkunarferlinu.
1. Á flýtiflipanum **Forstilling** skal stilla eftirfarandi reiti:

    - **Regla gámapökkunar** – Veldu gámapökkunarreglu sem skilgreinir hvernig á að afgreiða gáma á pökkunarstöðinni. Gámapökkunarstefnan sem þú velur verður forvalin fyrir starfsmanninn þegar hann opnar pökkunarstöðina. Fyrir frekari upplýsingar, sjá eftirfarandi bloggfærslu: [Bætt pökkunarvirkni](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Pökkunarprófílauðkenni** – Veldu auðkenni pökkunarprófíls sem skilgreinir pökkunarstefnuna og gámastillingarnar sem ætti að nota. Ef valið auðkenni pökkunarsniðs er tengt gámapökkunarstefnu muntu ekki geta breytt stillingum **Gámapökkunarstefna** reit á þessari síðu.

1. Á **Sjálfgefin pökkunarstöð** Flýtiflipi, veldu sjálfgefna síðu, vöruhús og staðsetningu sem eiga við starfsmanninn.
1. Ef starfsmaðurinn mun nota Vöruhússtjórnun farsímaforritið til að stjórna og skrá gámapökkunarvinnu sína, á **Notendur** Flýtiflipi, settu upp einn eða fleiri reikninga sem starfsmaðurinn getur notað til að skrá sig inn í appið. Fyrir frekari upplýsingar, sjá [Notendareikningar farsíma](mobile-device-work-users.md).

## <a name="example-scenario"></a><a name="scenario"></a>Dæmi

Þessi hluti gefur dæmi um atburðarás sem sýnir hvernig á að búa til pöntun og pakka hlutunum.

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

Þú getur líka notað þessa atburðarás sem leiðbeiningar til að nota eiginleikann á framleiðslukerfi. Hins vegar, í því tilfelli, verður að skipta út eigin gildi fyrir hverja stillingu sem er lýst hér.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Skráðu þig inn sem notandi sem getur unnið pökkunarvinnu

Skráðu þig inn á Supply Chain Management með því að nota notandareikning sem hefur þær heimildir sem þarf til að pakka gámum. Notandinn *Julia Funderburk* er innifalinn sem hluti af kynningargögnum og hefur nauðsynlegar heimildir. Þessi notandi hefur notandakennið *Admin*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Búðu til sölupöntun og kláraðu verkið

Fylgdu þessum skrefum til að stofna sölupöntun og ljúka vinnu við að flytja pantaðar vörur á pökkunarstöðina.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. IÍ svarglugganum **Búa til sölupöntun** í svæðinu **Viðskiptavinalykill** skaltu velja *US-005*.
1. Veldu **Í lagi** til að loka svarglugganum.
1. Nýja sölupöntunin er opnuð og inniheldur eina tóma línu á **Sölupöntunarlínur** Hraðflipi. Stilltu eftirfarandi gildi fyrir nýju pöntunarlínuna:

    - **Vörunúmer:** *A0001*
    - **Magn:** *2*
    - **Svæði:** *6*
    - **Vöruhús:** *62*

1. Á meðan pöntunarlínan er enn valin skaltu velja **Birgðir \> Fyrirvari** á tækjastikunni á **Sölupöntunarlínur** Hraðflipi.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Skilaboð sýna sendinguna og veifuauðkenni pöntunarinnar.

1. Á meðan pöntunarlínan er enn valin skaltu velja **Vöruhús** \> **Upplýsingar um vinnu** á tækjastikunni á **Sölupöntunarlínur** Hraðflipi. Ef þú notar lotuvinnslu til að keyra bylgjur þínar gætirðu þurft að bíða í stuttan tíma þar til verkið er búið til.
1. Á **Vinna** síðu, á aðgerðarrúðunni, á **Vinna** flipa, veldu **Fullkomið verk**.
1. Á **Verklok** síðu, stilltu **notandanafn** sviði til *62*.
1. Á aðgerðarrúðunni velurðu **Staðfesta vinnu**.
1. Þegar þú færð skilaboð sem gefa til kynna að vinnan þín sé gild skaltu velja **Fullkomið verk** til að ljúka ferlinu við að tína birgðahlutina og setja þá í *Pakki* staðsetningu.
1. Taktu eftir **Sendingarauðkenni** gildi sem er sýnt fyrir verkið í efri ristinni.

### <a name="pack-the-ordered-items-into-a-container"></a>Pakkaðu pöntuðu hlutunum í ílát

Nú er búið að koma birgðahlutunum á pökkunarsvæðið og tilbúið til að pakka þeim í gáma. Fylgdu þessum skrefum til að búa til nýjan ílát í kerfinu og pakka honum.

1. Fara skal í **Vöruhúsakerfi \> Pökkun og gámun \> Pakka**.
1. Í svarglugganum **Velja pökkunarstöð** skal stilla eftirfarandi gildi:

    - **Svæði:** *6*
    - **Vöruhús:** *62*
    - **Staðsetning:** *Pakka*
    - **Pökkunarprófílauðkenni:** *WH62*

1. Veldu **Í lagi**.
1. Á **Pakki** síðu, í **Skráningarnúmer eða sending** reit skaltu slá inn sendingarauðkenni sem þú skráðir áðan. Þú ættir nú að sjá hlutina sem eftir eru ópakkaðir á **Opnar línur** Hraðflipi.
1. Á aðgerðarrúðunni velurðu **Nýr gámur** að búa til gám í kerfinu.
1. Í **Auðkenni nýja gámsins** valmynd, stilltu **Gerð gáma** sviði til *Small Box*.
1. Veldu **Allt í lagi** til að búa til ílátið.
1. Veldu **Allt í lagi** að fara aftur til **Pakki** síðu. The **Opna ílát** Flýtiflipi sýnir nú **Gámaauðkenni** gildi ílátsins sem þú bjóst til.
1. Fyrir þessa atburðarás muntu pakka aðeins einum af pöntuðu hlutunum í bili. Þess vegna, á **Atriðapökkun** Flýtiflipi, stilltu eftirfarandi gildi:

    - **Magn:** *1.00*
    - **Auðkenni:** *A0001*

    Strax eftir að þú hefur valið **Auðkenni** gildi, síðan uppfærir **Opnar línur** og **Allar línur** Flýtiflipar til að gefa til kynna að einum hlut hafi verið pakkað. Þú ættir nú að hafa pakkað einum af tveimur hlutum *A0001*.

1. Á aðgerðasvæðinu skal velja **Loka gámi**.
1. Í **Lokaðu ílátinu** valmynd, veldu **Fáðu kerfisþyngd** til að fylla út sjálfgefið **Heildarþyngd** gildi.
1. Veldu **Allt í lagi** að loka ílátinu.

> [!TIP]
> Það eru ýmsar leiðir til að skoða gáma út frá samhengi. Til dæmis, þegar þú pakkar sendingu, er oft gagnlegt að skoða annað hvort gáma sem eru hluti af sendingunni eða alla gáma sem eru líkamlega á pökkunarstöð. The **Pökkunarstöð** á síðunni eru hnappar sem þú getur notað til að skoða alla opna og lokaða ílát á pökkunarstöð. Þessar skoðanir eru ekki bundnar við tiltekna sendingu. Þeir geta verið mjög hjálpsamir í aðstæðum þar sem einn starfsmaður er að pakka ílát og annar starfsmaður sýnir og losar gáminn.
>
> Samstæða yfirsýn yfir alla gáma er einnig fáanleg. Þetta útsýni er aðallega gagnlegt fyrir notendur sem vinna utan samhengis eins pökkunarstöðvar. Til að sjá það, farðu til **Vöruhússtjórnun \> Pökkun og gámavæðing \> Gámar**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
