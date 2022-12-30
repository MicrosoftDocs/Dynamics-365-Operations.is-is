---
title: Hættuleg efni í afurðum, pöntunum, sendingum og förmum
description: Þessi grein útskýrir hvernig á að stilla eiginleika hættulegra efna fyrir útgefnar afurðir, hvernig á að setja birgðamörk á hættulegar vörur og hvernig á að taka með hættuleg efni í sölupöntun, sendingu eða farmi.
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaae3ce4916465cd57da65eaa217c40f9c3ea88a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860697"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Hættuleg efni í afurðum, pöntunum, sendingum og förmum

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að stilla eiginleika hættulegra efna fyrir útgefnar afurðir, hvernig á að setja birgðamörk á hættulegar vörur og hvernig á að taka með hættuleg efni í sölupöntun, sendingu eða farmi.

## <a name="set-hazardous-material-specifications-for-products"></a>Setja verklýsingar hættulegra efna fyrir afurðir

Þegar búið er að skilgreina regluverk fyrir hættuleg efni og setja upp tengda tilvísunarkóða eins og lýst er í [Setja upp hættuleg efni](hazmat-setup.md), er hægt að tengja þessar upplýsingar við útgefnar vörur. Sendingartexti fyrir sendingarskjöl verður fenginn úr upplýsingum um hættuleg efni fyrir útgefnar vörur.

Sem hluti af ferlinu við að tengja útgefna vöru við hættulegt efni þarf að tilgreina reglugerðarkóðann og efnið. Mismunandi reglugerðarkóðar gætu verið tengdir við vöru, fer allt eftir stillingum flutnings, og hægt er að tengja margar reglugerðar- og efniskóða við hverja vöru.

Til að setja upp útgefna afurð sem hættulegt efni skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið eða stofnið afurð til að opna síðuna **Upplýsingar um losaðar afurðir**.
1. Í flýtiflipanum **Stjórna birgðum** skal stilla valkostinn **Hættulegt efni** á **Já**. Þessi stilling auðkennir vöruna sem hættulega vöru og er notuð þegar fylgiskjöl sendingar eru prentuð.
1. Á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, í flokknum **Reglufylgni**, skal velja **Vara með hættulegt efni**.
1. Fyllið út síðuna **Vara með hættuleg efni** fyrir valda vöru með því að nota reitina sem lýst er í eftirfarandi undirhlutum.

### <a name="item-hazardous-materials-header"></a>Síðuhaus vöru með hættuleg efni

Eftirfarandi tafla lýsir reitunum sem eru tiltækir efst á síðunni **Vara með hættuleg efni**.

| Svæði | lýsing |
|---|---|
| Vörunúmer | Útgefna afurðin sem verið er að vinna með. |
| Reglugerðarkóði | Velja skal reglugerð hættulegs efnis sem gildir um afurðina. Reglugerðin skilgreinir hvernig prentaður sendingartexti er búinn til fyrir vöru og tengda afhendingarmáta. Þegar henni hefur verið úthlutað er ekki hægt að breyta kóðanum á þessari síðu. Hins vegar er hægt að úthluta nýjum reglugerðarkóða með því að velja **Nýr**. |
| Efnakóði | (Valfrjálst) Velja skal þann efnakóða hættulegs efnis sem gildir um afurðina. Efnakóðinn býður upp á sniðmát sem inniheldur sjálfgefin gildi fyrir marga aðra reiti á þessari síðu. Þegar kóði er valinn verða allar lýsingar hættulegra efna afritaðar í núverandi afurð. Hins vegar biður kerfið fyrst um að staðfesta að efnisgögn vöru verði fyllt út fyrir efniskóðann. |
| Kóði hóps | (Valfrjálst) Velja skal flokkunarkóða fyrir hættulega efnið sem á við um afurðina. Rétt eins og fyrir reitinn **Efniskóði**, þegar kóði er valinn, verða allar lýsingar á hættulegum efnum hans afritaðar í núverandi afurð. Hins vegar biður kerfið fyrst um að staðfesta að gögn um vöruflokk verði fyllt út fyrir flokkskóðann. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>Flýtiflipi lýsingar

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í flýtiflipanum **Lýsingar**.

| Svæði | lýsing |
|---|---|
| Opinbert flutningstákn | Færið inn staðlaða lýsingu á efninu, eins og tilgreint er í viðeigandi reglugerð. Hægt er að bjóða upp á þýðingar fyrir þetta gildi í flýtiflipanum **Þýðing afhendingartexta vöru** eins og lýst er í næsta hluta. |
| Tækniheiti | Velja skal algengt eða almennt heiti fyrir efnið. Þetta heiti kann að vera heiti sem fyrirtækið notar innan fyrirtækisins fyrir efnið. |
| N.O.S. | Veljið þennan gátreit til að gefa til kynna að gildið **Rétt sendingarheiti** er sendingarheiti sem er „ekki tilgreint á annan hátt“ (N.O.S) fyrir vöruna. N.O.S. sendingarheiti eru notuð fyrir flokka svipaðra íðefna og annarra efna sem gegna ákveðnu hlutverki, en sem eru hugsanlega ekki gefin upp með nafni í spilliefnatöflunni í tiltekinni reglugerð. |

### <a name="item-ship-text-translation-fasttab"></a>Flýtiflipi þýðingar á afhendingartexta vöru

Flýtiflipinn **Þýðing afhendingartexta vöru** inniheldur hnitanet sem sýnir þýðingar á gildunum **Rétt sendingarheiti** sem eru skilgreind fyrir aðaltungumálið í flýtiflipanum **Lýsingar**. Þessar þýðingar er hægt að nota í prentuðum texta sendingar fyrir eitt eða fleiri tungumál.

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í flýtiflipanum **Þýðing á afhendingartexta vöru**.


| Svæði | lýsing |
|---|---|
| Tungumál | Tungumálakóðinn sem línan notar. Til dæmis merkir **pt-br** brasilíska portúgölsku. |
| Prentaður texti sendingar | Þýdda gildið **Rétt sendingarheiti** á tungumálinu sem línan notar. |

Til að bæta við eða breyta þýðingu skal velja **Þýðingar** fyrir ofan hnitanetið til að opna síðuna **Textaþýðingar**. Fylgið síðan einu af eftirfarandi skrefum:

- Til að bæta við nýrri þýðingu, á aðgerðasvæðinu, skal velja **Bæta við**. Velja skal tungumál sem á að bæta við og síðan, í reitinn **Þýddur texti**, skal færa inn þýdda textann.
- Til að breyta fyrirliggjandi þýðingu skal velja markmálið í reitnum **Tungumál** og breyta þýdda textanum í reitnum **Þýddur texti** eftir þörfum.

### <a name="material-management-fasttab"></a><a name="material-management"></a>Flýtiflipi fyrir stjórnun efna

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í flýtiflipanum **Stjórnun efna**.

| Svæði | lýsing |
|---|---|
| Klasi | Veljið flokk hættulegs efnis sem afurðin tilheyrir, eins og reglugerðin segir til um sem fylgt er eftir. Úthluta verður bæði deiliflokki og klasa á sérhverja afurð sem inniheldur hættuleg efni. |
| lýsing | Lýsingin sem er skilgreind fyrir klasann sem er valinn í svæðinu **Klasi**. Þetta svæði er aðeins til lestrar. |
| Skipting | Veljið deiliflokk hættulegs efnis sem afurðin tilheyrir, eins og reglugerðin segir til um sem fylgt er eftir. Deiliflokkurinn er undirþáttur klasans. Úthluta verður bæði deiliflokki og klasa á sérhverja afurð sem inniheldur hættuleg efni. |
| Auðkenning | Veljið auðkenniskóða hættulega efnisins. Yfirleitt er þessi kóði byggður á staðli Sameinuðu þjóðanna (SÞ). |
| Umbúðaflokkur | Velja skal umbúðaflokkinn sem á við um núverandi vöru. |
| lýsing | Lýsingin sem er skilgreind fyrir flokkinn sem var valinn í reitnum **Umbúðaflokkur**. Þetta svæði er aðeins til lestrar. |
| Pökkunarlýsing | Veljið viðeigandi kóða pökkunarlýsingar. Þessi kóði vísar í lýsingu sem gefur til kynna hvernig þarf að pakka afurðinni. |
| Merki fyrir hættuleg efni | Veljið kóða sem vísar í viðeigandi merkingu um hættulegan varning sem á að setja á afurðina. |
| Takmarkað magn | Stillið þennan valkost á **Já** til að gefa upp heildarframleiðsluþyngd sem fylgir með hverjum farmi og hverri farmlínu. |
| Magn | Sláið inn magn hættulegs efnis í afurðinni, í tilgreindri einingu. Þetta gildi verður notað til að reikna út heildarstig hættulegs efnis fyrir farma og sendingar sem innihalda afurðina. |
| Margfaldari | Sláið inn margfeldið sem er notuð þegar stig hættulegs efnis er reiknað út fyrir hverja farmlínu sem inniheldur afurðina. Þetta gildi er tilgreint í viðeigandi reglugerð, í samræmi við gerð hættulegs efnis sem er að finna í afurðinni. |
| Eining | Veljið mælieininguna sem gildir um magn hættulegs efnis í afurðinni, eins og tilgreint er í reitnum **Magn**. Þetta gildi verður notað til að reikna út heildarstig hættulegs efnis fyrir farma og sendingar sem innihalda afurðina. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>Hvernig stig hættulegs efnis er reiknað

Mörg gildin sem eru tilgreind í flýtiflipanum **Stjórnun efna** fyrir afurð eru notuð til að reikna *stig hættulegs efnis* fyrir hverja farmlínu sem inniheldur þessa afurð. Stigin eru reiknuð út með því að nota eftirfarandi formúlu:

Stig hættulegs efnis = *&lt;LineQty&gt;* × *&lt;HazmatQty&gt;* × *&lt;UnitConversion&gt;* × *&lt;Multiplier&gt;*

Hér eru útskýringar á formúlunni:

- *&lt;LineQty&gt;* er það afurðarmagn sem er tilgreint fyrir farmlínu.
- *&lt;HazmatQty&gt;* er magn hættulegs efnis sem tilgreint er fyrir afurð í reitnum **Magn** í flýtiflipanum **Stjórnun efna**.
- *&lt;UnitConversion&gt;* er umreiknistuðull til að umreikna eininguna sem notuð er fyrir magn farmlínunnar yfir í eininguna sem er tilgreind fyrir afurð í reitnum **Eining** í flýtiflipanum **Stjórnun efna**.
- *&lt;Multiplier&gt;* er margfaldari sem tilgreindur er fyrir afurð í reitnum **Margfaldari** í flýtiflipanum **Stjórnun efna**.

Þetta stigaskor er gefið upp fyrir hverja farmlínu sem inniheldur afurð þar sem þessi gildi eru tilgreind. Frekari upplýsingar er að finna í hlutunum [Sendingar sem innihalda hættuleg efni](#hazmat-shipments) og [Farmar sem innihalda hættuleg efni](#hazmat-loads) síðar í þessari grein.

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>Hvernig þyngd á hættulegum efnum er reiknuð út

Farmar og farmlínur sem innihalda afurðir þar sem valkosturinn **Takmarkað magn** í flýtiflipanum **Stjórnun efna** er stilltur á **Já** munu sýna heildarþyngd hættulegs efnis eins og lýst er í hlutunum [Sendingar sem innihalda hættuleg efni](#hazmat-shipments) og [Farmar sem innihalda hættuleg efni](#hazmat-loads) síðar í þessari grein. Þyngd hættulegs efnis er reiknuð út með því að nota eftirfarandi formúlu:

Þyngd hættulegs efnis = *&lt;LineQty&gt;* × *&lt;ProductWeight&gt;* × *&lt;UnitConversion&gt;*

Hér eru útskýringar á formúlunni:

- *&lt;LineQty&gt;* er það afurðarmagn sem er tilgreint fyrir farmlínu.
- *&lt;ProductWeight&gt;* er nettóþyngdin sem tilgreind er fyrir afurðina, í birgðaeiningunni sem er tilgreind fyrir afurðina.
- *&lt;UnitConversion&gt;* er umreiknistuðull til að umreikna eininguna sem notuð er fyrir magn farmlínunnar yfir í birgðaeininguna sem er notuð fyrir *&lt;ProductWeight&gt;*.

### <a name="transport-information-fasttab"></a>Flýtiflipi fyrir upplýsingar um flutninga

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í flýtiflipanum **Upplýsingar varðandi flutninga**.

| Svæði | lýsing |
|---|---|
| Flutningsflokkur | Veljið viðeigandi flutningsflokk. |
| Gangakóði | Veljið viðeigandi kóða fyrir takmarkanir vegna jarðganga fyrir vöruna. |
| Hleðsla hættulegra efna | Veljið tilvísunarkóðann sem er notaður fyrir hleðslu sjóflutnings þegar varan er flutt sjóleiðis. |
| Flugvélagerð | Velja skal takmörkun flugleiðis sem á við um efnið þegar það er flutt með flugi. |
| Pökkun – eingöngu vöruloftfar | Út frá gildinu sem valið var í reitnum **Gerð flugvélar**, skal velja kóða pökkunarlýsingar sem á við þegar aðeins er hægt að senda afurðina með vöruloftfari. |
| Pökkun – farþega- og vöruloftfar | Út frá gildinu sem valið var í reitnum **Gerð flugvélar**, skal velja kóða pökkunarlýsingar sem á við þegar hægt er að senda afurðina með annaðhvort vöruloftfari eða farþegaloftfari. |
| IATA-stjarna | Stillið þennan valkost á **Já** til að gefa til kynna að upplýsingar um flutninga í lofti sem færðar eru inn í þennan flýtiflipa sem tengist staðli Alþjóðasambands flugfélaga (IATA) um hættulegan varning. Þetta svæði er eingöngu ætlað til upplýsinga. |
| Neyðaráætlun | Veljið kóðann sem vísar í leiðbeiningar um meðhöndlun á efninu í neyðartilviki. |

### <a name="environmental-information-fasttab"></a>Flýtiflipi fyrir upplýsingar um umhverfismál

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í flýtiflipanum **Upplýsingar um umhverfismál**.

| Svæði | lýsing |
|---|---|
| Hættulegt umhverfinu | Stillið þennan valkost á **Já** til að gefa til kynna að afurðin sé hættuleg umhverfinu. Notið þetta svæði fyrir eigin tilkynningar. |
| Sjávarmengunarvaldur | Stillið þennan valkost á **Já** til að gefa til kynna að afurðin sé sjávarmengunarvaldar. Notið þetta svæði fyrir eigin tilkynningar. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Stilla birgðamörk fyrir hættulegar afurðir

Af öryggisástæðum gæti þurft að takmarka heildarmagn tiltekinnar afurðar sem hægt er að geyma á einum stað. Til að stilla birgðamörk fyrir útgefna afurð skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið afurð til að opna síðuna **Upplýsingar um útgefna afurð**.
1. Á aðgerðasvæði, í flipanum **Stjórna birgðum**, í flokknum **Reglufylgni**, skal velja **Uppgefnar upplýsingar**.
1. Í reitunum **Birgðamörk hættulegs efnis** og **Viðvörunarmörk hættulegs efni** skal stilla viðeigandi gildi fyrir valda afurð.

Skýrslan **Birgðamörk hættulegs efnis** gerir kleift að fylgjast með birgðamörkum hættulegra efna í staðsetningum vöruhúss, til að ganga úr skugga um að þau haldist undir birgðamörkum sem gefin eru upp hér. Frekari upplýsingar er að finna í [Skýrsla um birgðamörk hættulegra efna](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Sölupöntunarfærslur sem innihalda hættuleg efni

Til að taka með afurð sem flokkast sem hættulegt efni í sölupöntun, verður að tengja viðkomandi farmflytjanda við sölupöntunina. Opnið sölupöntunina og síðan í flýtiflipanum **Afhending** skal stilla reitina **Farmflytjandi** og **Flutningsþjónusta** eftir þörfum.

Farmflytjandinn er einnig tengdur flutningsmáta. Þess vegna þarf að ganga úr skugga um að þessar upplýsingar séu í takt við reglugerðina um hættuleg efni. Með öðrum orðum verður flutningsmátinn sem tilgreindur er í reglugerðinni um hættuleg efni að vera í samræmi við lýsingarnar í sölupöntunarhausnum. Á þennan hátt eru reglugerðin, farmflytjandinn og þjónustan tengd við flutningslínurnar sem notaðar eru í sölupöntun.

Þegar lokið er við sölupöntun og hún tilbúin til afhendingar, er hægt að losa hana í vöruhúsið til að tilgreina flutninginn úr söluaðgerð yfir í vöruhúsaaðgerð.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Sendingar sem innihalda hættuleg efni

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>Skoða stig hættulegra efna fyrir hverja sendingarlínu

Síðan **Upplýsingar sendingar** fyrir sendingu sýnir heildarþyngd hættulegs efnis og gildi sem hafa verið reiknuð fyrir hverja farmlínu sem tilheyrir þessari sendingu. Til að skoða stigin og þyngdirnar skal fylgja þessum skrefum.

1. Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.
1. Veljið sendingu til að opna síðuna **Upplýsingar sendingar**.
1. Farið yfir línurnar í flýtiflipanum **Farmlínur**. Fyrir hverja línu er hægt að sjá útreikninga á hættulegum efnum í eftirfarandi reitum:

    - **Stig hættulegra efna** – Þessi reitur sýnir stigaskor hættulegs efnis fyrir farmlínuna. Gildið er reiknað út í samræmi við reglur og gildi sem hafa verið búin til fyrir viðeigandi reglugerð og í uppsetningu útgefinnar afurðar. Útreikningurinn tekur magnið í farmlínunni og vísar í margfaldarann í [uppsetningu á stjórnun efnis](#material-management) fyrir útgefnu afurðina.
    - **Nettóþyngd á takmörkuðu magni** - Fyrir afurðir merktar sem afurðir með takmörkuðu magni vegna þess að þær innihalda hættuleg efni, sýnir þessi reitur heildarnettóþyngd á hættulegu efni sem haft er með í farmlínunni. Útreikningurinn byggir á afurðunum sem eru merktar sem hættuleg efni í uppsetningu útgefinnar afurðar. Ef vara er merkt sem vara með takmarkað magn, tekur útreikningurinn magnið í hverri farmlínu og vísar í þyngdina í [uppsetning á stjórnun efnis](#material-management) fyrir útgefnu afurðina.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Leita að samhæfi á milli hættulegra efna sem eru tekin með í sendingu

Kerfið getur metið hvort öll hættuleg efni sem eru tekin með í sendingu séu hentug til senda saman. Til að meta samhæfi athugar kerfið samhæfisflokkinn sem er úthlutaður á hverja afurð sem er tekinn með í sendingunni. Nánari upplýsingar er að finna í [Samhæfisflokkar hættulegra efna](hazmat-setup.md#compatibility-groups).

Til að keyra samhæfisathugun þarf að fylgja þessum skrefum.

1. Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.
1. Veljið sendingu til að opna síðuna **Upplýsingar sendingar**.
1. Á aðgerðasvæðinu, í flipanum **Sendingar**, í flokknum **Aðgerðir**, skal velja **Samhæfisprófun**.

Skilaboð birtast sem sýna niðurstöður athugunarinnar.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Farmar sem innihalda hættuleg efni

### <a name="view-hazardous-material-scores-for-each-load-line"></a>Skoða stig hættulegra efna fyrir hverja farmlínu

Síðan **Upplýsingar um farm** fyrir farm sýnir heildarþyngd hættulegs efnis og stigagildin sem hafa verið reiknuð fyrir þann farm og fyrir hverja farmlínu. Til að skoða stigin og þyngdirnar skal fylgja þessum skrefum.

1. Farið í **Vöruhúsakerfi \> Sendingar \> Allir farmar**.
1. Velja skal farm til að opna síðuna **Upplýsingar um farm**. (Einnig er hægt að opna farmupplýsingar með því að velja tengil úr viðeigandi sendingu.)
1. Í flýtiflipanum **Farmur** er hægt að yfirfara heildastig og -þyngd hættulegra efna fyrir allan farminn með því að skoða eftirfarandi reiti:

    - **Stig hættulegra efna** – Þessi reitur sýnir stigaskor hættulegs efnis fyrir farminn. Gildið er reiknað út í samræmi við reglur og gildi sem hafa verið búin til fyrir viðeigandi reglugerð og í uppsetningu útgefinnar afurðar. Útreikningurinn tekur magnið sem er í farminum og vísar í margfaldarann í [uppsetningu á stjórnun efnis](#material-management) fyrir útgefnu afurðina.
    - **Nettóþyngd á takmörkuðu magni** - Fyrir afurðir merktar sem afurðir með takmörkuðu magni vegna þess að þær innihalda hættuleg efni, sýnir þessi reitur heildarnettóþyngd á hættulegu efni sem haft er með í farminum. Útreikningurinn byggir á afurðunum sem eru merktar sem hættuleg efni í uppsetningu útgefinnar afurðar. Ef vara er merkt sem vara með takmarkað magn, tekur útreikningurinn magnið í hverjum farmi og vísar í þyngdina í [uppsetning á stjórnun efnis](#material-management) fyrir útgefnu afurðina.

1. Til að yfirfara stigin og þyngdirnar fyrir einstakar línur skal velja flýtiflipann **Farmlínur**. Gildin sem eru gefin upp fyrir hverja línu líkjast gildunum sem eru gefin upp fyrir allan farminn eins og lýst var í fyrra skrefi.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Athuga samhæfi á meðal hættulegra efna sem er að finna í farmi

Kerfið getur metið hvort öll hættuleg efni sem er að finna í farmi séu hentug til senda saman. Til að meta samhæfi athugar kerfið samhæfisflokkinn sem er úthlutaður á hverja afurð sem er tekin með í farminum. Nánari upplýsingar er að finna í [Samhæfisflokkar hættulegra efna](hazmat-setup.md#compatibility-groups).

Til að keyra samhæfisathugun þarf að fylgja þessum skrefum.

1. Farið í **Vöruhúsakerfi \> Sendingar \> Allir farmar**.
1. Veljið sendingu til að opna síðuna **Upplýsingar um farm**. (Einnig er hægt að opna farmupplýsingar með því að velja tengil úr viðeigandi sendingu.)
1. Á aðgerðasvæðinu, í flipanum **Farmar**, í flokknum **Aðgerðir**, skal velja **Samhæfisprófun**.

Skilaboð birtast sem sýna niðurstöður athugunarinnar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]