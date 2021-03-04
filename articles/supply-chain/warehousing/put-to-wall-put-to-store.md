---
title: Setja á vegg - setja í verslun
description: Þetta efnisatriði veitir upplýsingar um aðgerðina Setja á vegg - setja í verslun. Þessi virkni gerir þér kleift að takast á við atburðarásir þar sem þú verður að sameina vöru á biðsvæði forpökkunar, byggt á stillanlegu skilyrði. Hún hjálpar til við að draga úr tiltektartímanum vegna þess að hún gerir kleift að tína á eina marknúmeraplötu og getur notað fleiri frágangsstaðsetningar en klasatiltektir.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 12501b90e4b31ec11e3c59784ace9fd9a8b7d934
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430668"
---
# <a name="put-to-wall---put-to-store"></a>Setja á vegg - setja í verslun

[!include [banner](../includes/banner.md)]

Virknin *Setja á vegg - setja í verslun* gerir þér kleift að takast á við atburðarásir þar sem þú verður að sameina vöru á biðsvæði forpökkunar, byggt á stillanlegu skilyrði. Fyrst að þessi virkni gerir kleift að tína á eina marknúmeraplötu og getur notað fleiri frágangsstaðsetningar en klasatiltekt, munu fyrirtæki sem senda í verslanir eða meðhöndla litlar vörur hagnast á styttri tiltektartíma.

Verkflæðið fyrir þessa virkni beinir valdri vöru á röðunarstaðsetningu til að dreifa í ýmsar gerðir gáma. Yfirleitt inniheldur hver röðunarstaðsetning margar röðunarstaði. Hverjum röðunarstað er úthlutað samkvæmt skilyrðinu sem sett er af viðskiptaferlinu. Dæmigerð skilyrði eru lokaáfangastaður, sending eða hleðsla. Þegar vara kemur er henni dreift á hvern röðunarstað samkvæmt magninu sem tengist pöntuninni, áfangastaðnum, sendingunni eða hleðslunni. Þegar gámur er fullur eða honum lokið er hann fluttur á biðsvæði eða sendingarstað til frekari meðferðar, fer allt eftir viðskiptaferlinu.

Þessi vöruhúsaaðgerð er einnig kölluð öðrum nöfnum, t.d. „put-to-light“ og „break opens“.

## <a name="turn-on-the-outbound-sorting-feature"></a>Kveikja á eiginleika flokkunar á útleið

Áður en hægt er að nota virknina *Setja á vegg - setja í verslun*, verður að vera kveikt á eiginleikanum *Flokkun á útleið* í kerfinu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Flokkun á útleið*

Hægt er að nota eiginleikann *Flokkun á útleið* saman með eiginleikanum *Bylgjuskrefakóði fyrir allt fyrirtækið* ef kveikt er á honum. Einnig þarf að kveikja á þessum eiginleika ef notaðir eru fyrirframskilgreindir kóðar sem settir eru upp í bylgjuskrefakóðum. Í vinnusvæðinu **Stjórnun eiginleika** er þessi eiginleiki skráður á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Stigskóði bylgju fyrir alla stofnunina/fyrirtækið*

## <a name="setup"></a>Setja upp

Í þessu sýnidæmi er venjuleg Contoso-gögn og vöruhús *62* notað. Sumar viðbætur sem koma fram síðar eru einnig notaðar.

### <a name="location-type"></a>Staðsetningargerð

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Gerðir staðsetninga**.
1. Á aðgerðasvæðinu skal velja **Ný** til að búa til staðsetningargerð fyrir röðun.
1. Stilla eftirfarandi gildi:

    - **Gerð staðsetningar:** *SORT*
    - **Lýsing:** *Raða*

1. Veljið **Vista**.

### <a name="warehouse-management-parameters"></a>Færibreytur vöruhúsakerfis

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Í flipanum **Almennt**, í flýtiflipanum **Gerðir staðsetninga**, í reitinn **Flokkun á gerð staðsetningar**, skal færa inn *SORT*.
1. Veljið **Vista**.

### <a name="location-profile"></a>Forstillingar staðsetningar

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til staðsetningarforstillingu fyrr flokkunarstaðsetninguna.
1. Stilla eftirfarandi gildi í hausnum:

    - **Kenni staðsetningarforstillingar:** *Raða*
    - **Heiti:** *Raða*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Staðsetningarsnið:** *PACK*
    - **Gerð staðsetningar:** *SORT*
    - **Nota rakningu númeraplötu:** *Já*
    - **Heimila blandaðar vörur:** *Já*
    - **Heimila blandaða birgðastöðu:** *Já*

1. Veljið **Vista**.

### <a name="locations"></a>Staðsetningar

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**.
1. Hreinsið gátreitinn **Mynda vartölur fyrir staðsetningu**.
1. Veldu **Nýtt** á aðgerðasvæðinu og stilltu svo eftirfarandi gildi:

    - **Vöruhús:** *62*
    - **Staðsetning:** *Raða*
    - **Kenni staðsetningarforstillingar:** *Raða*

1. Veljið **Vista**.

### <a name="packing-profiles"></a>Forstillingar umbúða

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Forstillingar umbúða**.
1. Veldu **Nýtt** á aðgerðasvæðinu og stilltu svo eftirfarandi gildi:

    - **Forstillingarkenni pökkunar:** *Raða*
    - **Lýsing:** *Raða*
    - **Regla gámapökkunar:** Skiljið þennan reit eftir auðan.
    - **Auðkennisstilling gáms:** *Sjálfvirkt*
    - **Gámagerð:** *PALLET 48x48*
    - **Stofna gám sjálfkrafa þegar gámi er lokað:** Skiljið þennan reit eftir auðan.

1. Veljið **Vista**.

### <a name="wave-step-codes"></a>Kóðar bylgjuskrefs

Ef kveikt var á eiginleikanum *Bylgjuskrefakóði fyrir allt fyrirtækið* skal setja upp eftirfarandi kóða.

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjuskrefakóðar**.
1. Veldu **Nýtt** á aðgerðasvæðinu og stilltu svo eftirfarandi gildi:

    - **Kóði bylgjuskrefs:** *Raða*
    - **Lýsing á bylgjuskrefi:** *Raða*
    - **Gerð bylgjuskrefs:** *Sniðmát flokkunar*

1. Veljið **Vista**.

### <a name="outbound-sorting-template"></a>Sniðmát flokkunar á útleið

Flokkunarsniðmátið stjórnar því hvort röðunarstaðir eru búnir til, hvaða skilyrði eru notuð og aðrar eigindir röðunarferlisins.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Flokkunarsniðmát á útleið**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa flokkunarsniðmát.
1. Stilltu eftirfarandi gildi í haus nýja sniðmátsins:

    - **Kenni fyrir flokkunarsniðmát á útleið:** *Bylgjuröðun*
    - **Lýsing:** *Bylgjuröðun*
    - **Sniðmátsgerð röðunar:** *Bylgjueftirspurn*

        Þessi reitur skilgreinir ferlið sem flokkunarsniðmátið er notað í. Eftirtalin gildi eru tiltæk:

        - **Bylgjueftirspurn** - Flokkunarsniðmátið er notað fyrir ferlið *Setja á vegg*. Þessi sniðmátsgerð er notuð til að komast framhjá pökkunarstöðinni og vinna úr birgðum beint úr bylgjunni. Þú getur aðeins notað þessa gerð ef bylgjuúrvinnsluaðferðin **röðun** er höfð með í bylgjusniðmátinu.
        - **Gámur** - Flokkunarsniðmátið er notað fyrir ferlið *Röðun á bretti eftir pökkun*. Þessi sniðmátsgerð er notuð við úrvinnslu á gámum sem eru lokaðir á pökkunarstöðinni og sem þarf að raða á bretti.

    - **Vöruhús:** *62*
    - **Staðsetning:** *Raða*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Sannprófun röðunar:** *Skönnun stöðu*

        Þessi reitur skilgreinir sannprófunina sem krafist er við röðunina. Eftirtalin gildi eru tiltæk:

        - Engum
        - Skönnun númeraplötu
        - Skönnun stöðu

    - **Stofna vinnu á lokun stöðu:** *Já*

        Ef þessi valkostur er stilltur á *Já*, þegar staðan er lokuð, verður vinna stofnuð til að færa birgðir á lokasendingarstaðinn. Ef hann er stilltur á *Nei* verða birgðir strax tíndar fyrir pöntunina þegar staðan er lokuð.

    - **Stöðuverkefni:** *Handvirkt*

        Þessi reitur skilgreinir gerð af úthlutun staðsetningar. Eftirtalin gildi eru tiltæk:

        - **Handvirkt** - notandi verður alltaf að tilgreina hvaða stöðu birgðir eiga að vera flokkaðar í.
        - **Sjálfvirkt** - kerfið beinir birgðum sjálfkrafa að stöðu þegar það er í boði, á grunni sundurliðana sniðmátsflokkunar.

    - **Úthluta skilyrði röðunarstaðs:** *Aðeins nota tóma staði*

        Þessi reitur stjórnar því hvort tekið er tillit til birgða sem þegar eru til staðar á röðunarstaðnum þegar stað er úthlutað fyrir eftirspurnina. Eftirtalin gildi eru tiltæk:

        - **Aðeins nota tóman stað** - Staðir sem þegar eru með birgðir sem tengjast þeim verða teknir til greina
        - **Gert er ráð fyrir auðri staðsetningu** - Litið verður framhjá öllum birgðum sem eru á staðnum við úthlutun. Allar lausar stöður verða notaðar.

    - **Kóði bylgjuskrefs:** *Raða*

        Ef kveikt er á eiginleikanum *Bylgjuskrefakóði fyrir allt fyrirtækið* verður einnig setja upp bylgjuskrefakóðann *Raða* í bylgjuskrefakóðum.

    - **Loka sjálfkrafa röðun staðsetningar:** *Já*

        Ef þessi valkostur er stilltur á *Já* verður röðunarstaðnum sjálfkrafa lokað þegar allri vinnu sem kemur á staðinn hefur verið lokið.

    - **Fjöldi flokkaðra staðsetninga:** *3*

        Þessi reitur skilgreinir hámarksfjölda röðunarstaða sem kerfið mun búa til.

    - **Forskeyti fyrir röðun staðsetningar:** *SP-*

        Þessi reitur skilgreinir forskeytið sem kerfið úthlutar á undan númeri staðsetningar.

    - **Pakka sjálfkrafa röðun staðsetningar:** *Já*

        Ef þessi valkostur er stilltur á *Já* verða birgðirnar á röðunarstaðnum pakkaðar í gám þegar staðsetningunni er lokað.

    - **Forstillingarkenni pökkunar:** *Raða*

        Þessi reitur skilgreinir pökkunarforstillinguna sem verður notuð þegar röðunarstaðnum er pakkað í gám.

1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að tilgreina skilyrðið sem notað er fyrir þetta flokkunarsniðmát.
1. Í svarglugga fyrirspurnar, í flipanum **Röðun**, skal velja **Ný** til að bæta við línu og síðan stilla eftirfarandi gildi:

    - **Tafla:** *Upplýsingar um hleðslu*
    - **Afleidd tafla:** *Upplýsingar um hleðslu*
    - **Reitur:** *Auðkenni sendingar*
    - **Leitarstefna:** *Hækkandi*

1. Veljið **Í lagi**.
1. Þú gætir fengið eftirfarandi skilaboð: „Flokkun verður endurstillt, á að halda áfram?" Velja skal **Já**.

    Hnappur **Sundurliðanir flokkunarsniðmáts á útleið** á aðgerðasvæðinu verður tiltækur.

1. Á aðgerðasvæðinu skal velja **Sundurliðanir flokkunarsniðmáts á útleið**.
1. Veljið gátreitinn **Flokka eftir reit** til að flokka eftir auðkenni sendingar.

    Þessi stilling býr til eina röðunarstaðsetningu á hverja sendingu sem er gámur í bylgjunni.

1. Veljið **Í lagi**.

### <a name="wave-process-methods"></a>Vinnsluaðferðir bylgju

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.
1. Veldu **Endurgera aðferðir** á aðgerðasvæðinu.

    Aðferð **röðunar** er bætt við listann yfir tiltækar aðferðir og bylgjusniðmátsgerðin *Sending* er valin fyrir hana.

### <a name="wave-templates"></a>Bylgjusniðmát

Breytið bylgjusniðmátinu sem notað er fyrir röðun bylgjueftirspurnar.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Í reitnum **Bylgjusniðmátsgerð** skal velja *Sending*.
1. Veljið fyrirliggjandi sniðmát **62 Sjálfgefin sending**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í flýtiflipanum **Almennt** skal gera eftirfarandi breytingar:

    - Stilla valkostinn fyrir **Vinna úr bylgju við losun í vörugeymslu** á *Nei*.
    - Stilla valkostinn **Úthluta** á opnar bylgjur á *Já*.

1. Í flýtiflipanum **Aðferðir** skal setja upp aðferðina **röðun**:

    1. Í hnitanetinu **Eftirstandandi aðferðir** skal velja **röðun**.
    2. Veljið hægri örvarhnappinn til að færa **röðun** yfir á hnitanetið **Valdar aðferðir**.
    3. Í hnitanetinu **Valdar aðferðir** skal velja **röðun**.
    4. Stillið reitinn **Bylgjuskrefakóði** á *Raða*.

1. Veljið **Vista**.

### <a name="mobile-device-menu-items"></a>Valmyndaratriði fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum:

    - **Heiti valmyndaratriðis:** *Raða*
    - **Titill:** *Raða*
    - **Stilling:** *Óbein*
    - **Nota fyrirliggjandi vinnu:** *Nei*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Verkþáttarkóði:** *Röðun á útleið*
    - **Nota leiðbeiningar fyrir ferli:** *Já* (sjálfgefið gildi)
    - **Kenni fyrir flokkunarsniðmát á útleið:** *Bylgjuröðun*

1. Veljið **Vista**.

### <a name="mobile-device-menu"></a>Valmynd fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Veldu **Á útleið** á valmyndinni.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í hnitanetinu **Tiltækar valmyndir og valmyndaratriði** skal finna og velja valmyndaratriðið **Raða** sem var verið að búa til.
1. Smellið á hægri örvarhnappinn til að færa **Raða** yfir á hnitanetið **Valmyndarskipan**. Á þennan hátt er valmyndaratriðinu bætt við valmyndina **Á útleið**.
1. Veljið **Vista**.

### <a name="location-directives"></a>Staðsetningarleiðbeiningar

Búa þarf til staðsetningarleiðbeiningar til að leiða áfram vinnuna sem búin er til eftir að röðuninni lýkur.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Í reitnum **Gerð verkbeiðni** skal velja *Röðuð birgðatínsla*.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum:

    - **Röð:** *1*
    - **Heiti:** *Koma fyrir í útskoti*

1. Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar**:

    - **Tegund vinnu:** *Frágangur*
    - **Svæði:** *6*
    - **Vöruhús:** *62*
    - **Leiðbeiningarkóði:** Hafðu þetta svæði autt.
    - **Margar birgðahaldseiningar:** *Nei*

1. Veldu **Vista** til að gera flýtiflipann **Línur** tiltækan.
1. Í flýtiflipanum **Línur** skal velja **Ný** og stilla síðan eftirfarandi gildi. Samþykktu sjálfgildin fyrir öll önnur svæði.

    - **Raðnúmer:** *1*
    - **Frá-magn:** *0*
    - **Til magn:** *1000000*

1. Veldu **Vista** til að gera flýtiflipann **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.
1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Ný** og stilla síðan eftirfarandi gildi. Samþykktu sjálfgildin fyrir öll önnur svæði.

    - **Raðnúmer:** *1*
    - **Heiti:** *Útskot*

1. Veldu **Vista** til að gera hnappinn **Breyta fyrirspurn** á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum**.
1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritilsins, í flipanum **Svið**, skal finna línuna þar sem reiturinn **Svæði** er stilltur á *Staðsetning*. Stillið reitinn **Skilyrði** fyrir þessa línu á *Útskot*.
1. Smellið á **Í lagi** til að staðfesta breytinguna.

### <a name="work-classes"></a>Vinnuklasar

1. Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum:

    - **Auðkenni vinnuklasa:** *Röðun*
    - **Lýsing:** *Röðun*
    - **Gerð verkbeiðni:** *Röðuð birgðatínsla*

1. Veljið **Vista**.

### <a name="work-templates"></a>Vinnusniðmát

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Vinnusniðmát**.
1. Í reitnum **Gerð verkbeiðni** velurðu *Sölupantanir*.
1. Í hnitanetinu skal velja vinnusniðmátið **62 Tína til að pakka**.
1. Á aðgerðasvæðinu skal velja **Vinnuhausaskil**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í línunni þar sem reiturinn **Heiti svæðis** er stillt á *Auðkenni sendingar* skal hreinsa gátreitinn **Flokka eftir þessum reit**.
1. Veljið **Vista** og lokið síðan svarglugganum **Vinnuhausaskil**.
1. Í reitnum **Gerð verkbeiðni** skal velja *Röðuð birgðatínsla*.
1. Veljið **Nýtt** til að búa til vinnusniðmát.
1. Í hlutanum **Yfirlit** skal stilla eftirfarandi gildi. Samþykktu sjálfgildin fyrir öll önnur svæði.

    - **Vinnusniðmát:** *Röðuð tiltekt*
    - **Lýsing á vinnusniðmáti:** *Röðuð tiltekt*

1. Veljið **Vista** til að gera hlutann **Upplýsingar um vinnusniðmát** tiltækan.
1. Í hlutanum **Upplýsingar vinnusniðmáts** býrðu til tvær línur. Veldu **Nýtt** og stilltu síðan eftirfarandi gildi fyrir línu 1:

    - **Verkgerð:** *Tiltekt*
    - **Áskilið:** Valið (= *Já*)
    - **Auðkenni vinnuklasa:** *Röðun*

1. Veljið aftur **Ný** og stillið síðan eftirfarandi gildi fyrir línu 2:

    - **Tegund vinnu:** *Frágangur*
    - **Áskilið:** Valið (= *Já*)
    - **Auðkenni vinnuklasa:** *Röðun*

1. Veljið **Vista**.

## <a name="example-scenario"></a>Dæmi

Þessi atburðarás líkir eftir aðstæðum þar sem vöruhúsið geymir litlar vörur í staðsetningum og verður að pakka þeim í kassa áður en þær eru sendar, og þar sem virkni pökkunarstöðva hentar í raun ekki. Starfsmenn tína pantanir fyrir marga viðskiptavini og mismunandi heimilisföng á sama tíma til að auka tínsluhraðann. Eftir að tínslu lýkur fara starfsmenn á röðunarstaðsetninguna þar sem hægt er að flokka tíndar vörur í réttan kassa samkvæmt áskildum skilyrðum. Í þessu dæmi verður auðkenni sendingarinnar notað til að ákvarða réttan kassa vegna þess að hver sending er með sitt eigið heimilisfang. Þegar búið er að pakka og raða öllum vörum hleðslunnar eftir sendingu, verða kassarnir færðir yfir á biðsvæðið og að lokum hlaðnir inn í flutningabíl.

Áður en hafist er handa með atburðarásina skal ganga úr skugga um að allar venjulegar vöruhúsaaðgerðir séu settar upp á réttan hátt fyrir vöruhúsið. Hefðbundið Contoso-vöruhús *62* er notað í þessum tilgangi. Hefðbundnum skilgreiningum hefur ekki verið breytt, fyrir utan því sem lýst er í uppsetningunni.

### <a name="create-demand"></a>Búa til eftirspurn

Áður en hægt er að sýna virknina þarf að búa til eftirspurn. Í þessari atburðarás býrðu til þrjár sölupantanir fyrir þrjá mismunandi viðskiptavini til að líkja eftir mismunandi afhendingaraðsetrum. Þú býrð þar af leiðandi til þrjár aðskildar sendingar.

Áður en þú stofnar sölupantanir og sendingar skaltu ganga úr skugga um að tiltektarstaðsetningar hafi nægar birgðir fyrir allar vörurnar í pöntunum. Farið yfir stillingar staðsetningarleiðbeiningarinnar til að staðfesta tiltektarstaðsetningarnar sem notaðar eru fyrir tiltekt sölupöntunar. Ef þú verður að breyta birgðum geturðu búið til handvirkar birgðahreyfingar, notað áfyllingu eða notað hvaða annað flæði sem er. Því næst taka frá birgðirnar.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Veljið **Ný** til að stofna sölupöntun fyrir pöntun 1.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinur:** *US-001*
    - **Vöruhús:** *62*

1. Veljið **Í lagi**.
1. Nýrri línu er bætt við flýtiflipann **Sölupöntunarlínur**. Stilla eftirfarandi gildi:

    - **Vörunúmer:** *A0001*
    - **Magn:** *5*

1. Veldu **Bæta við línu** til að bæta við annarri línu og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *A0002*
    - **Magn:** *10*

1. Endurtakið eftirfarandi skref fyrir hverja sölulínu í pöntuninni til að taka frá birgðir fyrir hana:

    1. Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Birgðir** velur þú **Frátekning**.
    1. Á síðunni **Frátekning** skal velja **Frátektarlota** og loka svo síðunni.
    1. Veljið **Vista**.

1. Veljið **Ný** til að stofna sölupöntun fyrir pöntun 2.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinur:** *US-004*
    - **Vöruhús:** *62*

1. Veljið **Í lagi**.
1. Nýrri línu er bætt við flýtiflipann **Sölupöntunarlínur**. Stilla eftirfarandi gildi:

    - **Vörunúmer:** *A0001*
    - **Magn:** *7*

1. Veldu **Bæta við línu** til að bæta við annarri línu og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *A0002*
    - **Magn:** *3*

1. Endurtakið eftirfarandi skref fyrir hverja sölulínu í pöntuninni til að taka frá birgðir fyrir hana:

    1. Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Birgðir** velur þú **Frátekning**.
    1. Á síðunni **Frátekning** skal velja **Frátektarlota** og loka svo síðunni.
    1. Veljið **Vista**.

1. Veljið **Ný** til að stofna sölupöntun fyrir pöntun 3.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinur:** *US-007*
    - **Vöruhús:** *62*

1. Veljið **Í lagi**.
1. Nýrri línu er bætt við flýtiflipann **Sölupöntunarlínur**. Stilla eftirfarandi gildi:

    - **Vörunúmer:** *A0001*
    - **Magn:** *8*

1. Fylgið þessum skrefum til að taka frá birgðir fyrir sölulínuna:

    1. Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Birgðir** velur þú **Frátekning**.
    1. Á síðunni **Frátekning** skal velja **Frátektarlota** og loka svo síðunni.
    1. Veljið **Vista**.

Ljúkið við eftirfarandi ferli til að losa hverja sölupöntun fyrir sig í vöruhúsið. Þrjár mismunandi sendingar verða búnar til. Þú bætir síðan öllum þremur sendingunum við nýja bylgju.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í hnitanetinu skal velja fyrstu sölupöntunina sem var stofnuð.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Þú færð skilaboð með upplýsingum um bylgjuauðkenni og sendingarkenni sem voru búin til.

1. Endurtaktu fyrri skrefin til að losa sölupantanir 2 og 3 í vöruhús. Takið eftir að upplýsingarnar í skilaboðunum sem birtust tilgreina að sendingu hafi verið bætt við bylgjuna sem var búin til þegar sölupöntun 1 var losuð.
1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Veljið bylgjukennið sem var búið til úr losuninni á sölupöntuninni til að opna síðuna **Bylgjur**. Þessi síða sýnir upplýsingar um bylgjuna. Flýtiflipinn **Bylgjulínur** sýnir sendingarnar sem búnar voru til.

    Nú þarf að búa til vinnu til að fara með vörur af tiltektarstaðsetningum og yfir á röðunarstaðsetningu.

1. Á aðgerðasvæðinu skal velja **Úrvinnsla**.

    Við bylgjuvinnslu mun flokkunaraðferðin nota flokkunarsniðmátið til að úthluta birgðum á röðunarstaði. Þegar bylgjuvinnslu er lokið færðu skilaboð með upplýsingum um að bylgjan hafi verið bókuð vinna hafi verið búin til.

1. Á Aðgerðasvæðinu, í flipanum **Bylgja**, í flokknum **Tengdar upplýsingar**, skal velja **Vinna** til að skoða vinnuna sem var búin til. Skráið niður vinnukennið.
1. Fara skal í **Vöruhúsakerfi \> Pökkun og gámun \> Úthlutanir á röðunarstað á útleið**.
1. Í vinstri dálknum er hægt að skoða röðunarstaði á útleið sem voru búnir til fyrir hverja sendingu.
1. Í flýtiflipanum **Skilyrði staðsetningarflokkunar** er hægt að skoða auðkenni sendingarinnar fyrir þessa stöðu.

Eitt vinnukenni hefur verið búið til að færa birgðir úr tiltektarstaðsetningu í röðunarstaðsetningu. Til að ljúka vinnunni þarftu vinnukennið sem var búið til í bylgjuvinnslunni.

### <a name="sales-order-picking-to-the-sorting-location"></a>Tínsla sölupöntunar yfir í röðunarstaðsetningu

1. Skráðu þig inn í forrit fartækisins sem starfsmaður í vöruhúsi *62*.
1. Í aðalvalmyndinni skal velja **Á útleið**.
1. Í valmyndinni **Á útleið** skal velja **Sölutiltekt**.
1. Veljið reitinn **Auðkenni** og færið síðan inn vinnukennið úr bylgjuvinnslunni.
1. Staðfestu færsluna.

    Næst er beðið um að færa inn marknúmeraplötu (NP). Takið eftir því að lína 1 í sölupöntun 1 er það sem verður að tína og bæta við marknúmeraplötuna. Vörunúmerið, magnið, vörulýsingin og tiltektarstaðsetningin eru sýnd.

1. Í reitinn **Marknúmeraplata** skal færa inn númer númeraplötu.

    Velja skal allar línur sem búnar voru til í bylgjunni sem unnið var úr og yfir í sömu marknúmeraplötuna.

1. Staðfestu færsluna.

    Fartækjaforritið birtir nú nokkrar síður af **Tiltekt** sem benda á tiltektarstaðsetninguna og vöruna og magnið sem þarf að tína. Þegar búið er að bæta valinni vöru við númeraplötuna skal staðfesta tiltektina. Síðasta síðan verður vinnan við að setja tíndar vörur í röðunarstaðsetninguna.

1. Staðfestið fyrstu tiltektina.
1. Næsta tiltekt er sýnd. Staðfesta tínslu.
1. Haldið áfram að staðfesta eftirstandandi tiltektir.
1. Síðasta skrefið er að ljúka frágangsvinnunni. Staðfestið frágang yfir á röðunarstaðsetningu.

    Skilaboðin „Vinnu er lokið“ birtast.

1. Lokið **Tiltekt sölu** í forriti fartækis.

### <a name="sortingput-to-wall"></a>Röðun/setja á vegg

Nú þegar búið er að koma öllum birgðum fyrir í röðunarstaðsetningunni, þarf að raða þeim á rétta röðunarstaði.

1. Skráið ykkur inn í forrit fartækis.
1. Í aðalvalmyndinni skal velja **Á útleið**.
1. Í valmyndinni **Útleið** skal velja **Raða** til að hefja röðun á vörum.
1. Í reitinn **NP/GÁM** skal færa inn marknúmeraplötu fyrir sölupöntunarvinnuna sem var tínd.
1. Staðfestu færsluna.
1. Sláið inn vörunúmerið sem á fyrst að raða.
1. Kerfið ákvarðar fyrsta röðunarstaðinn sem á að sýna. Staðfestið röðunarstaðinn.
1. Beðið er um að númeraplötu verði úthlutað á röðunarstaðinn. Veljið reitinn **NP**, færið inn númer númeraplötu og staðfestið síðan innsláttinn.

    Röðunarstaðurinn tengist auðkenni sendingar og því þarf að raða tíndum vörum á númeraplötu sem á við þessa tilteknu sendingu á útleið og sölupöntun.

    Næsta síðan sýnir vörukennið, magn, staðsetningarkenni röðunar og auðkenni „frá“ (tiltekt) og „til“ (röðun) númeraplatnanna. Upplýsingarnar á þessari síðu segja þér að raða tiltekinni vöru og magni frá númeraplötu tiltektar í númeraplötu röðunar.

1. Staðfestið röðunarstaðinn.
1. Raðið vörunum í fyrstu röðunarstaðsetninguna. Þegar þessu er lokið beinir kerfið þér að næsta röðunarstað.
1. Endurtakið þetta ferli fyrir allar tíndar línur í vinnubeiðninni. Einnig ætti að nota þetta ferli þegar margar tiltektarlínur eru með sama vörunúmerið.

    Þegar þetta ferli er endurtekið fyrir allar vörurnar, metur kerfið skilyrðið úr næstu skönnuðu vöru (vinnulínu) og ákveður hvaða röðunarstaðsetningu ætti að setja hana í. Þér er sjálfkrafa sagt að setja vöruna á rétta röðunarstaðsetningu. Það fer eftir uppsetningu staðfestingar, en þér er einnig sagt að staðfesta þessa aðgerð með því að slá inn númer staðsetningar eða auðkenni númeraplötu.

    > [!NOTE]
    > Ef kveikt er á sjálfvirkri röðun, er handvirk hnekking ekki í boði.

1. Þegar þessu er lokið, í Microsoft Dynamics 365 Supply Chain Management, skal opna síðuna **Úthlutanir á röðunarstaðsetningum á útleið** til að fara yfir stöðuna á staðsetningunum.

    - Ef staðsetningum er lokað sjálfkrafa skal velja **Sýna lokaðar** til að sýna lokaðar staðsetningar.
    - Takið eftir að færslur röðunarstaðsetningar eru sýndar. Varan og magnið sem unnið var úr í gegnum staðsetninguna er sýnt.

    Þegar flokkunarsniðmát á útleið er sett upp, er valkosturinn **Loka sjálfkrafa röðun staðsetningar** stilltur á *Já*. Þess vegna er staðsetningunni lokað sjálfkrafa þegar síðustu væntanlegu birgðirnar eru settar í hana. Röðunarstaðsetningarnar eru í stöðunni **Lokað** og vinna hefur verið búin til að flytja raðaðar birgðir yfir á staðsetninguna *Útskot*.

1. Ljúkið tiltekt á röðuðum birgðum til að færa birgðirnar yfir á sendingarstaðinn. Þegar birgðir eru tilbúnar skal staðfesta sendingu.

> [!NOTE]
> Til að unnið verði rétt úr tiltekt raðaðra birgða, ætti valmyndaratriði fartækis, sem er með vinnuklasakenni þar sem reiturinn **Gerð vinnubeiðni** er stilltur á *Tiltekt raðaðra birgða*, að vera notað fyrir flutnings- og hleðsluferlið.

### <a name="manually-close-a-position-optional"></a>Loka staðsetningu handvirkt (valfrjálst)

Ef loka á röðunarstaðsetningum handvirkt, verður valkosturinn **Loka sjálfkrafa röðun staðsetningar** fyrir flokkunarsniðmát á útleið að vera stillt á *Nei* og lokun verður að gera áður en hægt er að færa birgðir yfir á útskotssvæðið. Hægt er að loka stöðum á ýmsa vegu:

- Um vöruhúsaforrit:

    - Notandinn getur skannað eina vöruna sem er þegar í staðsetningunni og síðan valið **Loka** til að loka henni.
    - Ef notandi skannar gám sem þegar hefur verið raðað á gám, birtast villuboð. Notandinn getur samt haldið áfram að loka staðnum.

- Af Microsoft Dynamics 365 Supply Chain Management síðunni **Úthlutanir á röðunarstaðsetningu á útleið**:

    - Notandinn getur valið færslu röðunarstaðsetningu á útleið og síðan valið **Loka staðsetningu** á aðgerðasvæðinu.

## <a name="tips"></a>Ábendingar

- Ekki er hægt að færa vörur milli staða þegar búið er að úthluta þeim einni slíkri. Kerfið metur hversu mikið af hverri vöru ætti að fara á tiltekin stað.
- Flokkunarsniðmát er hægt að skilgreina til að búa sjálfkrafa til gáma þegar staðir eru lokaðir. Þessi nálgun býr til hefðbundið skipulag gámakennis sem byggir á tiltekinni pökkunarforstillingu.

> [!IMPORTANT]
> Þegar vinna birgðahreyfingar hefur verið búin til í röðunarstaðsetningu, má ekki hætta við vinnuna. Annars verður staðnum og gámum hans eytt úr kerfinu og ekki tiltækir fyrir frekari úrvinnslu. Birgðir verða einnig fjarlægðar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]