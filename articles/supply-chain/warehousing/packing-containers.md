---
title: Geymar til sendingar
description: Þessi grein lýsir pökkunarferlinu sem gerir þér kleift að staðfesta birgðavörur og pakka þeim í gáma.
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
ms.openlocfilehash: 118b1c79d23cd1b5044ede9aa9c469409cd22166
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708784"
---
# <a name="pack-containers-for-shipment"></a>Geymar til sendingar

[!include [banner](../../includes/banner.md)]

Pökkunarferlið fyrir gáma gerir þér kleift að staðfesta birgðavörur og pakka þeim í gáma. Á meðan á þessu ferli stendur taka vöruhúsastarfskraftar yfirleitt upp birgðavörur af geymslusvæðum og flytja þær á pökkunarsvæði. Þar geta margir vöruhúsastarfskraftar athugað magn og tegundir vöru og úthlutað þeim í viðeigandi stærð gáma. Þegar gámi er pakkað að fullu er það lokað og flutt á úthlið, þar sem það er gert tilbúið til sendingar.

Gámar tákna efnislegar einingar sem vörum er pakkað í og hægt er að fylgjast með upplýsingum um gáma í kerfinu. Þessar upplýsingar geta verið gagnlegar við skipulagningu flutninga, sérstaklega ef þú reiknar sendingargjöld miðað við gáma. Áður en þú sendir, getur þú skoðað fjölda gáma sem eru notuð í sendingu, tegundir gáma sem eru notuð og efnislegar víddir hvers gáms (eins og heildarrúmmál og þyngd).

Hægt er að nota nokkra tengda vöruhúsaaðgerðir á útleið með gámum. Frekari upplýsingar er hægt að finna í eftirfarandi greinum:

- [Bylgja gámun](wave-containerization.md)
- [Flokkun á útleið](outbound-sorting.md)
- [Sending lítilla pakka](small-parcel-shipping.md)
- [Staðfesta og flytja](confirm-and-transfer.md)
- [Stilla mismunandi víddir fyrir pakka og geymslu](packing-vs-storage-dimensions.md)
- [Pökkunarvinna fyrir pökkunargáma og vinnslusendingar á útleið](packing-work.md)
- [Gámum pakkað með farsímaforriti Warehouse Management](warehouse-app-packing-containers.md)
- [Dæmi –gámum pakkað með farsímaforriti Warehouse Management](warehouse-app-pack-containers-scenario.md)
- [Prenta merkimiða gáms](print-container-labels.md)

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Settu upp vöruhúsið þitt til að nota handvirkar pökkunaraðgerðir

Hægt er að skipuleggja aðgerðir á útleið á tvo vegu:

- **Stofnun og meðhöndlun bylgju** – Starfskraftar taka til vörur miðað við vinnu í vöruhúsi á útleið. Síðan setja þeir vörurnar beint á úthlið, þar sem þeir eru tilbúnir til tafarlausrar sendingar. Upplýsingar um hvernig á að setja upp og nota þetta ferli er að finna [Stofnun og meðhöndlun bylgju](wave-processing.md).
- **Handvirk pökkun á pökkunarstöðvum** – Þetta ferli hefur viðbótaraðgerð milli pökkunar og sendingar. Í stað þess að setja birgðirnar á *úthlið* setja starfskraftar þær á *pökkunarstað*. Þeir stjórna síðan pökkunarferlinu á pökkunarstöðinni með því að nota síðuna **Pakka** í vefbiðlaranum. Til að virkja þetta ferli verður þú að stilla kerfið þitt eins og lýst er í þessum hluta.

### <a name="set-up-warehouse-locations-for-packing"></a>Setja upp vöruhúsastaðsetningar fyrir pökkun

Nauðsynlegt er að hafa að minnsta kosti einn pökkunarstað þar sem starfskraftar munu setja birgðavörur svo hægt sé að pakka þeim í gáma. Frekari upplýsingar um hvernig á að stofna staðsetningar í vöruhúsi er að finna í [Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi](tasks\configure-locations-wms-enabled-warehouse.md). Eftirfarandi undirhlutar útskýra hvernig á að stofna og úthluta þessum pökkunarstaðsetningum.

#### <a name="set-up-location-types-for-packing"></a>Setja upp staðsetningagerðir fyrir pökkun

Skilgreina verður *staðsetningartegund* fyrir pökkunarstaðsetningar. Hægt er að nota gerðir staðsetninga sem síunarvalkosti til að stýra mismunandi vöruhúsakerfisferlum. Nafn hverrar staðsetningargerðar lýsir yfirleitt einhverju um hvernig sú staðsetningargerð ætti að vera notuð. Staðsetningargerðin sem þú setur upp hér verður að vera tengd við hverja staðsetningu sem er notuð fyrir pökkunaraðgerðir.

Fylgið þessum skrefum til að setja upp staðsetningargerð.

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Gerðir staðsetninga**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að bæta staðsetningargerð við hnitanetið.
1. Stillið eftirfarandi reiti fyrir nýju staðsetningargerðina:

    - **Staðsetningargerð** – Slá inn heiti fyrir staðsetningargerðina. Hvert nafn verður að vera einkvæmt og ætti að lýsa einhverju um hvernig staðsetningargerðin er ætluð til notkunar.
    - **Lýsing** – Færðu inn stutta lýsingu á staðsetningargerðinni.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Upplýsa kerfið um gerð pökkunarstaðsetningar

Eftir að staðsetningargerð hefur verið búin til verður að stilla kerfið þannig að það þekkist sem sú staðsetningargerð sem á að nota við pökkunaraðgerðir.

Fylgið þessum skrefum til að stilla staðsetningartegundina sem er notuð fyrir pökkunaraðgerðir.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**
2. Í flipanum **Almennt**, í flýtiflipanum **Gerðir staðsetninga**, skal stilla reitinn **Gerð pökkunarstaðsetningar** á staðsetningargerðina sem á að nota til að auðkenna pökkunarstöðvar.

> [!NOTE]
> Ef þú ert að uppfæra úr nýrri útgáfu af Microsoft Dynamics AX, þá hefur staðan *Í pökkun* verið fjarlægð úr sendingum og förmum, því það virkaði ekki af fullri samkvæmni og bjó til umframgögn. Því hafa listasíðurnar **Í afhendingu** og **Farmur í pökkun** verið gerðar úreltar. Gámar sem verður að pakka eru raktir á birgðageymslustigi.
>
> Í fyrri útgáfum hefur þú skilgreint pökkunarstaðsetninguna með því að nota reitinn **Auðkenni notendaupplýsinga fyrir pökkunarstaðsetningar** á flipanum **Pökkun** á síðunni **Færibreytur vöruhúsakerfis** til að tilgreina *staðsetningarsnið*. Í núverandi útgáfu, getur þú notað reitinn fyrir **Gerð pökkunarstaðsetningar** á flipanum **Almennt** á síðunni **Færibreytur vöruhúsakerfis** til að tilgreina *tegund staðsetningar*, eins og lýst er í þessari grein. Nýi reiturinn er í betra samræmi við ferlið við að finna sviðsetningarstaðsetningar og endanlegar sendingarstaðsetningar.
>
> Þrátt fyrir að þú getir haldið áfram að nota gamla **Auðkenni notendaupplýsinga fyrir pökkunarstaðsetningar**, mælum við með því að þú byrjir að nota nýja reitinn **Gerð pökkunarstaðsetningar** í staðinn vegna þess gamli reiturinn verður að lokum úreltur.
>
> Ef þú hreinsar stillingar á gamla reitnum **Auðkenni notendaupplýsinga fyrir pökkunarstaðsetningar** og vistar síðan síðuna verður reiturinn gerður óvirkur til frambúðar. Fyrir uppsetningar þar sem reiturinn **Auðkenni notendaupplýsinga fyrir pökkunarstaðsetningar** hefur aldrei verið notað verður hann alltaf gerður óvirkur. Eftir að þú hefur hreinsað reitinn **Auðkenni notendaupplýsinga fyrir pökkunarstaðsetningar** skaltu nota stillingarnar sem lýst er í þessari grein til að setja upp og auðkenna pökkunarstaðsetninguna þína.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Setja upp staðsetningarforstillingar fyrir pökkunarstaðsetningar

Á hverjum *staðsetningarforstillingu* eru upplýsingar og reglur sem gilda um tengdar staðsetningar. Þar sem þú þarft að hafa að minnsta kosti eina staðsetningu til að nota fyrir pökkunaraðgerðir, verður þú að búa til staðsetningarforstilling fyrir hana til viðbótar við staðsetningargerð. Hægt er að nota hvern prófíl fyrir sig eftir fjölda staðsetninga. Staðsetningar sem eru notaðar til pökkunar verða að vera settar upp til að rekja númeraplötur.

Fylgið þessum skrefum til að setja upp staðsetningarforstillingu fyrir pökkunarstaðsetningu.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.
1. Veldu núverandi forstilling á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjan.
1. Í haus nýja eða valda sniðsins skal stilla eftirfarandi reiti:

    - **Kenni staðsetningarforstillingar** Sláið inn einkvæmt kenni fyrir forstillinguna.
    - **Heiti** - Færið inn lýsandi heiti á forstillingunni.

1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Staðsetningarsnið** – Velja staðsetningarsniðið sem á að nota fyrir núverandi staðsetningu. Staðsetningarsnið eru nafngiftarkerfi sem eru notuð til að stofna einkvæm og samræmd heiti fyrir mismunandi staðsetningar karfa sem eru notað innan vöruhúss. Ef þú ert ekki nú þegar með sniðið sem þú þarft geturðu búið það til með því að opna **Vöruhúsastjórnun \> Uppsetning \> Vöruhús \> Staðsetningarsnið**. Frekari upplýsingar er að finna í [Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Tegund staðsetningar** – Veldu tegund staðsetningar sem er sett upp sem tegund pökkunarstaðsetningar á síðunni **Færibreytur vöruhúsakerfis**, eins og lýst var fyrr í þessari grein.
    - **Nota rakningu númeraplötu** – Fyrir pökkunarstaðsetningar skal stilla þennan valkost á *Já*. Kerfið verður að geta fylgst með númeraplötuauðkennum á pökkunarstöðum svo það geti stjórnað pökkunarferlinu.
    - **Leyfa neikvæðar birgðir** – Fyrir pökkunarstaðsetningar, stillið þennan valkost á *Nei*.
    - **Leyfa blönduð atriði** – Fyrir pökkunarstaðsetningar skal stilla þennan valkost á *Já*. Þessarar stillingar er krafist vegna þess að mörg mismunandi vörunúmer eru yfirleitt færð á pökkunarstaðina á sama tíma.
    - **Leyfa blandaðar birgðastöðu** – Fyrir pökkunarstaðsetningar skal stilla þennan valkost á *Já*. Þessi stilling er nauðsynleg vegna þess að vörur með mismunandi birgðastöðu eru yfirleitt færðir á pökkunarstaðina á sama tíma.
    - **Leyfa blandaðar birgðarunur** – Fyrir pökkunarstaðsetningar skal stilla þennan valkost á *Já*. Þegar þessi valkostur er sjálfkrafa stilltur á *Já* í hvert sinn þegar valkosturinn **Leyfa blandaðar vörur** er stilltur á *Já*.

#### <a name="set-up-packing-locations"></a>Setja upp pökkunarstaðsetningar

Nauðsynlegt er að vera með minnst eina *staðsetningu* þar sem starfskraftar setja birgðir sem þarf að pakka niður í gáma.

Fylgið eftirfarandi skrefum til að bæta við pökkunarstaðsetningu.

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**.
1. Á aðgerðasvæðinu skal velja **Nýr** til að bæta við staðsetningu.
1. Stillið svo eftirfarandi reiti fyrir nýju staðsetninguna:

    - **Vöruhús** – Tilgreinið vöruhúsið þar sem pökkunarstaðsetning þarf að vera.
    - **Staðsetning** – Færðu inn heiti fyrir nýja staðsetningu.
    - **Auðkenni staðsetningarforstillingar** – Gættu þess að tilgreina auðkennið sem var búið til í fyrri hlutanum.

## <a name="set-up-the-packing-process"></a>Setja upp pökkunarferlið

Þessi hluti lýsir því hvernig stilla skuli stillingar sem virkja pökkunarferlið og láta starfskrafta pakka birgðum í gám.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Setja upp pökkunarreglur geymis

Hver *Pökkunarregla gáms* skilgreinir hvernig vinna skal úr gámi. Í hvert sinn sem nýr gámur eru stofnuð er einnig valin pökkunarregla fyrir gáminn til að nota í þau.

Fylgið þessum skrefum til að setja upp pökkunarreglur gáms.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Gámar \> Pökkunarreglur gáms**.
1. Veldu núverandi reglu á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjan.
1. Í haus nýju eða völdu reglunnar skal stilla eftirfarandi gildi:

    - **Pökkunarregla gáms** – Slá inn einkvæmt heiti reglunnar.
    - **Lýsing** - Færið inn lýsandi heiti á reglunni.

1. Í flipanum **Yfirlit** skal stilla eftirfarandi reiti. Þessir reitir gera þér kleift að tilgreina til hvaða aðgerða skal grípa þegar gám er lokað, hvort það eigi að starfa með eða án vinnustofnunar og hvenær losa eigi gám úr pökkunarstöðinni.

    - **Vöruhús** – Veljið vöruhúsið þar sem pökkunarreglan gildir.
    - **Sjálfgefin staðsetning lokasendingar -** Tilgreindu ákjósanlega staðsetningu gáms eftir að því er lokað. Þessi reitur er einungis í boði þegar reiturinn **Losunarregla geymis** er stillt á *Gera tiltækt á endanlegum sendingarstað*.
    - **Sjálfgefin staðsetning fyrir röðun** – Þessi reitur er notaður með eiginleikanumm [raða á útleið](outbound-sorting.md).
    - **Þyngdareining** – Veldu sjálfgefna mælieiningu til að nota þegar gámi er lokað og skráður. Venjulega er þessi mælieining mælieiningin sem er notuð af vog á pökkunarstöðinni. Þessi reitur á við reglur með eða án sköpunar vinnu.
    - **Reglur um lokun gáms** – Veljið einn af eftirfarandi valkostum til að skilgreina hvað á að eiga sér stað þegar gámnum er lokað:

        - *Sjálfvirk losun* – Gámur verður talið laust frá pökkunarstöðinni og aðgerðin sem tilgreind er í reitnum **Losunarregla gáms** verður virkjuð.
        - *Seinkuð losun* – Gámurinn verður ekki tafarlaust losaður úr pökkunarstöðinni. Starfsmaður í vöruhúsi verður að losa það handvirkt síðar.
        - *Valfrjálst* – Þegar starfskraftur lokar gámnum getur hann valið hvort losa skuli gáminn.

        Ef pökkunarstöðin meðhöndlar aðallega staka gáma sem eru sendir beint til viðskiptavina er eðlilegasta aðferðin að losa gámana strax. Ef pökkunarstöðin sér um sendingar sem samanstanda af mörgum gámum eða jafnvel vörubrettum er líklega best að fresta losuninni þar til allri sendingunni eða vörubrettinu hefur verið pakkað og er tilbúinn til afhendingar.

    - **Losunarregla gáms** – Veljið einn af eftirfarandi valkostum til að skilgreina hvað á að eiga sér stað þegar gámur er losað frá pökkunarstað:

        - *Gera tiltækt á endanlegum sendingarstað* – Uppfærðu gáminn á endanlegan sendingarstað. Ef þessi kostur er valinn skaltu nota reitinn **Sjálfgefin staðsetning lokasendingar** til að tilgreina ákjósanlega staðsetningu fyrir gáminn eftir að því hefur verið lokað.
        - *Stofna vinnu til að færa geymi af pökkunarstöð* – Stofna vinnu til að færa geymi af pökkunarstöð yfir á biðsvæði eða beint á útkeyrsluhurð. Notaðu reitinn **Vinnusniðmát** til að tilgreina vinnusniðmátið sem á að nota þegar vinna er búin til fyrir gám.
        - *Úthluta gámi flokkaðri staðsetningu á útleið* – Þessi valkostur er notaður með eiginleikanum [flokkun á útleið](outbound-sorting.md).

        Í flestum tilvikum er mælt með því að þú búir til verk til að færa gáma, vegna þess að þessi aðferð sýnir betur raunverulega handvirka ferla í vöruhúsinu. Hins vegar, við einfaldar aðstæður, eða aðstæður þar sem pökkunarstöðin er staðsett beint á úthliði, gæti verið æskilegt að gámurinn sé tiltækt strax á endanlegum sendingarstað.

    - **Vinnusniðmát** – Veldu vinnusniðmátið sem á að nota þegar vinna er búin til fyrir gáminn. Þetta svæði er aðeins tiltækt þegar reiturinn **Losunarregla gáms** er stillt á *Stofna vinnu til að færa gám frá pökkunarstöð* og tengist verkbeiðnigerð sem er nefnd *Tiltekt pakkaðs gáms*. Frekari upplýsingar eru í [Vinnusnið og staðsetningarleiðbeiningar](control-warehouse-location-directives.md).

    Í næstu skrefum stillir þú stillingar sem varða *skráningu*. Skráning er ferlið við að tilgreina þyngd gáms, gámaflokks eða sendingar, ásamt rakningarkennum sem berast frá flutningsaðila. Dynamics 365 Supply Chain Management er ekki hægt að samþætta ytri kerfum flutningsaðila. Þess í stað verða vöruhúsastarfskraftar að prenta merkimiða sem berast frá flutningafyrirtækinu og skanna síðan rakningarnúmer þegar þeir fylla út farmskrána.

    Vegna þess að skráningarkröfur eru mismunandi frá viðskiptavini til viðskiptavinar, og jafnvel frá sendingu til sendingar, veita pökkunarreglur verulegan sveigjanleika í verkflæðinu. Hægt er að setja upp farmskrár fyrir gáma, gámaflokka og sendingar í hvaða samsetningu sem er.

    Ef þú ert að nota fjölþrepa verklag við skráningu verða starfskraftar að skrá öll gáma áður en þeir skrá tengdan gámaflokk og þeir verða að skrá alla gámaflokka áður en þeir skrá tengda sendingu.

1. Stilltu eftirfarandi reiti á flýtiflipanum **Skrá geymis**:

    - **Sjálfvirk skrá við lokun gáms** – Stillið þennan valkost á *Já* til að skrá upplýsingum um skráningarupplýsingar sem hluta af lokunarferli gámsins. Ef þú ert ekki að nota samþættingu flutninga verður að skrá upplýsingarnar handvirkt.
    - **Skráarkröfur fyrir gám** – Veljið einn af eftirfarandi valkostum:

        - *Ekkert* - Ekkert kynningarferli verður notað.
        - *Handvirkt* – Verkflæði pökkunar krefst skráningar. Kerfið leyfir ekki að gámi sé lokað eða losað fyrr en skráningu er lokið.
        - *Flutningsstjórnun* – Skráning verður gerð í gegnum taxtavélar flutningsstjórnunar (TMS). Þar sem þessi valkostur krefst sérsniðinnar þróunar til að framkvæma tiltekna vél fyrir flutningafyrirtækið mun hún ekki virka eins og hún kemur fyrir í núverandi útgáfu.

    - **Prenta innihald gámsins** – Stillið þennan valkost á *Já* til að prenta sjálfkrafa innihaldsskýrslu gáms þegar gámur er skráð lokað. Einnig er hægt að prenta skýrsluna eftir þörfum.

1. Á flýtiflipanum **Skráning geymaflokks**, í reitnum **Skráarkröfur fyrir geymaflokk** skal velja einn eftirfarandi valkosta:

    - *Ekkert* – Farmskrá geymaflokks verður ekki tekin með sem skilyrði í verkflæði pöntunar.
    - *Handbók* – Farmskrá geymaflokks verður tekin með sem krafa í verkflæði pökkunar. Allir gámar í hópnum verða að vera lokað áður en hægt er að skrá flokkinn. Veljið þennan valkost ef fylla þarf út farmskrá fyrir hvern gámaflokk sem er pakkað á pökkunarstöðinni. Þennan kost velur þú yfirleitt ef gámum er pakkað á vörubretti og allt vörubrettið er skráð.

    > [!NOTE]
    > Núverandi útgáfa styður ekki farmskrár fyrir gámaflokka og engin TMS-vél styður við gámaflokka.

1. Á flýtiflipanum **Farmskrá sendingar** stillirðu eftirfarandi reiti:

    - **Skráarkröfur fyrir sendingu** – Veljið einn af eftirfarandi valkostum:

        - *Ekkert* – Farmskrá sendingar verður ekki tekin með sem skilyrði í verkflæði pöntunar.
        - *Handbók* – Farmskrá sendingar verður tekin með sem krafa í verkflæði pökkunar. Engum gámum fyrir sendingu er hægt að sleppa fyrr en að skráningu lokinni.
        - *Flutningsstjórnun* – Skráning verður gerð í gegnum TMS-taxtavélar. Þar sem þessi valkostur krefst sérsniðinnar þróunar til að framkvæma tiltekna vél fyrir flutningafyrirtækið mun hún ekki virka eins og hún kemur fyrir í núverandi útgáfu.

        Skráning sendingar ætti að vera virk ef þú þarft að fylla út farmskrá fyrir alla sendinguna sem er pökkuð á pökkunarstöðinni. Það er yfirleitt notað þegar þörf er á einni samstæðri farmskrá jafnvel þótt sendingin samanstandi af mörgum gámum eða gámaflokkum.

    - **Prenta fylgiseðil** – Stillið þennan valkost á *Já* til að prenta sjálfkrafa út fylgiseðil sem hluta af farmskrá. Einnig er hægt að prenta út fylgiseðilinn eftir þörfum.

### <a name="set-up-container-types"></a>Setja upp gámagerðir

Á meðan á handvirka pökkunarferlinu stendur verður að búa til gáma áður en hægt er að pakka vörum í þau. Hver gámur verður að vera byggður á *gámagerð*, sem skilgreinir hámarks efnislegt rúmmál gáms og burðargetu.

Fylgdu þessum skrefum til að búa til gámagerð.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Gámar \> Gámagerðir**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að bæta við gámagerð.
1. Stillið svo eftirfarandi reiti fyrir nýju gámagerðina:

    - **Kóði fyrir gámagerð** – Sláið inn einkvæmt auðkenni fyrir gámagerð.
    - **Lýsing** - Færðu inn lýsingu á nýju gámagerð.
    - Í **Umbúðaþyngd** skal færa inn raunverulega eða áætlaða þyngd gámsins.
    - **Hámarks nettóþyngd** - Sláðu inn þá hámarksþyngd sem gámur getur haldið.

1. Í hlutanum **Gámavíddir** í reitunum **Lengd**, **Breidd**, **Hæð** og **Rúmmál**, skal færa inn efnislegar víddir gámsins.
1. Í hlutanum **Hámark** í reitunum **Lengd**, **Breidd**, **Hæð** og **Rúmmál**, skal færa inn hámarks efnislegar víddir gámsins.
1. Þú getur skilgreint viðbótareiginleika fyrir gámagerðir sem tengjast öðrum aðgerðum sem nota gáma. Frekari upplýsingar eru í [Gámun](wave-containerization.md).

> [!NOTE]
> Fyrir handvirka pökkunarferlið notar kerfið aðeins gildið í reitnum **Hámarks nettóþyngd** og gildið í reitnum **Rúmmál** í hlutanum **Hámark**.

### <a name="set-up-packing-profiles"></a>Setja upp pökkunarforstillingar

*Pökkunarsnið* eru nauðsynleg fyrir pökkunarferlið. Hægt er að velja þær eða stilla þær sjálfgefið þegar pökkun er hafin á síðunni **Pökkun**.

Fylgið þessum skrefum til að setja upp forstillingu umbúða.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Forstillingar umbúða**.
1. Veldu núverandi forstilling á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjan.
1. Í haus nýja eða valda sniðsins skal stilla eftirfarandi reiti:

    - **Pökkunarforstillingakenni.** – Sláðu inn stutt kenni fyrir forstillinguna.
    - **Lýsing** – Færið inn lýsingu á pökkunarforstillingu.
    - **Pökkunarstefna gáms** – Veljið pökkunarstefnu sem á við prófílinn. Frekari upplýsingar eru í hlutanum [Setja upp pökkunarreglur geymis](#packing-policy) í þessari grein.
    - **Auðkennisstilling gáms** Veldu hvort auðkenni gáms eigi sjálfkrafa að myndast þegar gámur er búið til eða hvort það verði að vera búið til handvirkt.
    - **Gámagerð** – Veldu gámagerð sem er sjálfgefið notuð þegar nýjum gámi er stofnuð.
    - **Stofna sjálfkrafa gám við lokun gáms** – Veljið þennan gátreit til að búa sjálfkrafa til nýjan gám ef fyrra gámur er lokað, og ein eða fleiri línur eru eftir í núverandi sendingu.

### <a name="set-up-warehouse-workers"></a>Setja upp starfsmenn í vöruhúsi

Allir notendur eða starfskraftar sem pakka gámum með því að nota síðuna **Pökkun** í vefbiðlararanum eða aðgerðarkóðann *Pökkun* í farsímaforriti vöruhúsastjórnunar verða að hafa notendareikning sem tengist *starfskrafti/einstaklingi* og skrá að tilskildum aðgangsréttindum að öryggi sé úthlutað. (Nánari upplýsingar um hvernig setja á upp nýja notendur eru í [Setja upp notendur](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md).)

Fylgið þessum skrefum til að setja upp skrá *starfskraft/einstakling* fyrir pökkunarferlið.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Starfskraftur**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að bæta við vinnunotanda.
1. Stilltu reitinn **Starfskraftur** á núverandi starfskrafts sem skilgreind er í eininguni **Mannauður** fyrir notandann sem mun ljúka pökkunarferlinu.
1. Á flýtiflipanum **Forstilling** skal stilla eftirfarandi reiti:

    - **Regla gámapökkunar** – Veldu gámapökkunarreglu sem skilgreinir hvernig á að afgreiða gáma á pökkunarstöðinni. Regla gámapökkunar sem er valin hér verður valin fyrirfram fyrir starfskraftinn þegar viðkomandi opnar pökkunarstöðina. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Bætt pökkunaraðferð](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Auðkenni pökkunarforstillingar** – Veldu auðkenni pökkunarforstillingar sem skilgreinir pökkunarreglu og gámastillingar sem ætti að nota. Ef valið auðkenni pökkunarforstillingar er tengt við reglu gámapökkunar verður ekki hægt að breyta stillingunni **Regla gámapökkunar** reitsins á þessari síðu.

1. Á flýtiflipanum **Sjálfgefin pökkunarstöð** skal velja sjálfgefið svæði, vöruhús og staðsetningu sem á við starfskraftinn.
1. Ef starfskraftur mun nota farsímaforrit vöruhúsakerfis til að hafa umsjón með og skrá pökkunarvinnu sína í gám, á flýtiflipanum **Notendur**, skaltu setja upp einn eða fleiri reikninga sem starfskraftur getur notað til að skrá sig inn í forritið. Frekari upplýsingar er að finna í [Notendareikningar fartækis](mobile-device-work-users.md).

## <a name="example-scenario"></a><a name="scenario"></a>Dæmi

Þessi hluti sýnir dæmi um aðstæður sem sýna hvernig á að búa til pöntun og pakka vörum.

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

Einnig er hægt að nota þessa atburðarás sem leiðsögn fyrir notkun eiginleikans í framleiðslukerfi. Hins vegar, í því tilfelli, verður að skipta út eigin gildi fyrir hverja stillingu sem er lýst hér.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Skrá inn sem notandi sem getur unnið pökkunarvinnu

Skráðu þig inn í Supply Chain Management með því að nota notandareikning sem hefur þær heimildir sem þarf til að pakka í gáma. Notandinn *Julia Funderburk* fylgir með sem hluti af sýningargögnunum og hefur tilskildar heimildir. Þessi notandi er með notandaauðkennið *Stjórnandi*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Stofna sölupöntun og ljúka verkinu

Fylgið eftirfarandi skrefum til að stofna sölupöntun og ljúka vinnu við að færa pantaðar vörur á pökkunarstöð.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. IÍ svarglugganum **Búa til sölupöntun** í svæðinu **Viðskiptavinalykill** skaltu velja *US-005*.
1. Veldu **Í lagi** til að loka svarglugganum.
1. Nýja sölupöntunin er opnuð og inniheldur eina, auða línu á flýtiflipanum **Sölupöntunarlínur**. Stillið eftirfarandi gildi fyrir nýju pöntunarlína:

    - **Vörunúmer:** *A0001*
    - **Magn:** *2*
    - **Svæði:** *6*
    - **Vöruhús:** *62*

1. Á meðan nýja línan er enn valin skal velja **Birgðir \> Frátekning** on á verkstiku flýtiflipans **Sölupöntunarlínur**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Skilaboð sýna sendinguna og bylgjukenni fyrir pöntunina.

1. Á meðan pöntunarlínan sé enn valin skaltu velja **Vöruhús** \> **Vinnuupplýsingar** á tækjastikunni á flýtiflipanum **Sölupöntunarlínur**. Ef þú notar lotuvinnslu til að keyra bylgjurnar gæti þurft að bíða í stuttan tíma eftir að vinnan sé búin til.
1. Á síðunni **Vinna** á aðgerðasvæðinu, í flipanum **Vinna**, skal velja **Ljúka vinnu**.
1. Á síðunni **Verki lokið** stillir þú reitinn **Notandakenni** á *62*.
1. Veldu **Villuleita verk** á aðgerðasvæðinu.
1. Þegar þú færð skilaboð sem gefa til kynna að vinnan þín sé gild skaltu velja **Ljúka vinnu** til að ljúka við að taka til birgðavörurnar og setja þær í staðsetninguna *Pökkun*.
1. Gera skal athugasemd um **Auðkenni sendingar** sem sýnt er fyrir verkið á efra hnitanetinu.

### <a name="pack-the-ordered-items-into-a-container"></a>Pakkið pöntuðu hlutunum í gám

Birgðavörur hafa nú verið færðar á pökkunarsvæðið og eru tilbúnar til pökkunar í gáma. Fylgdu þessum skrefum til að búa til nýjan gám í kerfinu og pakka því.

1. Fara skal í **Vöruhúsakerfi \> Pökkun og gámun \> Pakka**.
1. Í svarglugganum **Velja pökkunarstöð** skal stilla eftirfarandi gildi:

    - **Svæði:** *6*
    - **Vöruhús:** *62*
    - **Staðsetning:** *Pakka*
    - **Forstillingarkenni pökkunar:** *WH62*

1. Veldu **Í lagi**.
1. Á síðuna **Pakka**, í reitinn **Númeraplata eða sending**, skal slá inn kenni sendingar sem þú skrifaðir niður hjá þér áður. Þú ættir að sjá vörurnar sem á eftir að pakka á flýtiflipanum **Opin lína**.
1. Á aðgerðasvæðinu skal velja **Nýr gámur** til að stofna nýjan gám í kerfinu.
1. Í svarglugganum **Kenni nýja gámsins** skal stilla reitinn fyrir **Gámagerð** á *SmallBox*.
1. Velja skal **Í lagi** til að stofna gáminn.
1. Veldu **Í lagi** til að fara aftur á síðuna **Pakka**. Nú sýni flýtiflipinn **Opnir gámar** gildi **Auðkenni gáms** gámsins sem var búið til.
1. Í þessum aðstæðum pakkið þið bara einu af pöntuðu vörunum í bili. Í flýtiflipanum **Vörupökkun** skal því stilla eftirfarandi gildi:

    - **Magn:** *1.00*
    - **Auðkenni:** *A0001*

    Strax eftir að **Auðkennið** auðkennið hefur verið valið uppfærir síðan flýtiflipana **Opnar línur** og **Allar línur** til að sýna að einni vöru hafi verið pakkað. Nú átt þú að vera búin(n) að pakka öðru af tveimur hlutum vöru *A0001*.

1. Á aðgerðasvæðinu skal velja **Loka gámi**.
1. Í svarglugganum **Loka gámi** skal velja **Sækja kerfisþyngd** til að fá fylla út sjálfgefna gildið **Brúttóþyngd**.
1. Velja skal **Í lagi** til að loka geyminum.

> [!TIP]
> Til eru ýmsar leiðir til að skoða gáma út frá samhengi. Þegar þú pakkar til dæmis sendingu er oft gagnlegt að skoða annað hvort gáma sem eru hluti af sendingunni eða alla gáma sem eru efnislega í pökkunarstöð. Á síðunni **Pökkunarstöð** eru hnappar sem hægt er að nota til að skoða öll opin og lokuð gáma á pökkunarstöð. Þessi yfirlit eru ekki bundnar við tiltekna sendingu. Þeir geta verið mjög gagnlegir við aðstæður þar sem einn starfskraftur er að pakka gámi og annar starfskraftur er að setja upp og losa gáminn.
>
> Einnig er í boði samantekið yfirlit yfir alla gáma. Þetta yfirlit er mest gagnleg fyrir notendur sem vinna ekki með staka pökkunarstöðvar. Fara skal í **Vöruhúsakerfi \> Pökkun og gámun \> Gámar**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
