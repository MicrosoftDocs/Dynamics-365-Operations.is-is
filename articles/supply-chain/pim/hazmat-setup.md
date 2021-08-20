---
title: Setja upp hættuleg efni
description: Þetta efnisatriði útskýrir hvernig á að setja upp gögn sem þarf til að flokka vörur sem hættuleg efni. Þegar stofnuð er sölupöntun sem inniheldur vöru sem flokkast sem hættulegt efni, býr kerfið til fylgigögn um hættuleg efni fyrir þessa sölupöntun þegar hún er send.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: c360d6a0fd5ffb65d1ea50d50e1ea5de00c84abe72e83c72b9bc4d6826cb41d0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712983"
---
# <a name="set-up-hazardous-materials"></a>Setja upp hættuleg efni

[!include [banner](../includes/banner.md)]

Til að nota virkni hættulegra efna þarf fyrst að setja upp gögnin sem nauðsynleg eru til að flokka vörur sem hættuleg efni. Síðan þegar stofnuð er sölupöntun sem inniheldur vöru sem flokkast sem hættulegt efni, býr kerfið til fylgigögn um hættuleg efni fyrir þessa sölupöntun þegar hún er send.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>Kveikja á eiginleika hættulegra efna fyrir kerfið

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Afurðaupplýsingastjórnun*
- **Heiti eiginleika:** *Afurðarlýsingar og fylgigögn sendingar fyrir hættuleg efni*

## <a name="hazardous-material-regulations"></a>Reglugerðir um hættuleg efni

Til að nota ferli hættulegra efna þarf fyrst að búa til reglugerð. Reglugerðir skilgreina hvernig prentaður texti sendingar er búinn til fyrir vöru. Þær skilgreina einnig viðeigandi afhendingarmáta.

Hér eru nokkrar algengar reglugerðir:

- **ADR** - Reglugerðir sem tengjast alþjóðlegum flutningi á hættulegum farmi á vegum
- **CFR 49** - Reglugerðir í Sameinuðu þjóðunum um flutning hættulegs vara
- **IMDG** - Alþjóðlega sjávarhættulegu vörurnar (IMDG) kóðinn
- **IATA** - Alþjóðlega flugsamgöngusamtökin (IATA) reglugerðir um hættulegan varning

Þessar reglugerðir hjálpa til við að ákvarða hvaða upplýsingar eiga að birtast þegar sendingartexti er prentaður fyrir vöru. Hægt er að skilgreina eins margar reglugerðir og þarf að fylgja.

> [!IMPORTANT]
> Virknin til að setja upp upplýsingakóða sem tengjast hættulegum efnum fellir reglugerðirnar ekki inn í fyrirtækið. Hún er aðeins verkfæri sem hjálpar til við að byggja upp ferla fyrir fyrirtækið.

Yfirleitt er reglugerð í boði fyrir tiltekinn flutningsmáta, svo sem vöruflutning sjóleiðis, á landi eða í flugi. Þess vegna er hægt að tengja hverja reglugerð við flutningsmáta. Flutningsmátinn verður notaður þegar tiltekin skjöl eru prentuð í vöruhúsakerfi. Í vöruhúsakerfi er hver sending tengd við farmflytjanda og flutningsþjónustu sem eru sett upp í einingunni **Flutningur**. Flutningsmátinn tengist farmflytjanda og flutningsþjónustu. Þegar skýrsla er keyrð er flutningsmátinn notaður til að finna prentaðan texta sendingar sem tengist losaðri vöru.

Þessi uppsetningargögn eru ekki sértæk fyrir hvern lögaðila (fyrirtæki). Þess vegna er hægt að hafa sameiginlegt safn yfir upplýsingar um hættuleg efni sem er deilt á meðal allra lögaðila.

Fyrir hverja reglugerð er hægt að skilgreina efnalista og nota hann sem sniðmát sem tengist losuðum vörum. Fyrir hverja reglugerð er einnig hægt að skilgreina prentuppsetningu. Prentuppsetning gerir kleift að skilgreina hvernig sendingartexti fyrir vöru er settur saman. Prentuppsetningin er notuð til að setja saman prentaðan texta sendingar fyrir losaða vöru.

Til að setja upp reglugerðir um hættuleg efni skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Reglugerð hættulegra efna**. Á síðunni **Reglugerð um hættuleg efni** er hægt að búa til eins margar reglugerðir og þarf og skilgreina hverja þeirra með því að nota reitina sem lýst er í eftirfarandi undirhlutum.

### <a name="hazardous-material-regulation-header"></a>Síðuhaus reglugerðar um hættuleg efni

Hver reglugerð er með kóða og lýsingu. Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í hausnum.

| Svæði | lýsing |
|---|---|
| Reglugerðarkóði | Færa skal inn kóða sem auðkennir færslu reglugerðar um hættuleg efni. |
| lýsing | Færið inn lýsingu á reglugerð um hættuleg efni. |

### <a name="print-setup-fasttab"></a>Flýtiflipi prentuppsetningar

Hver reglugerð getur haft eins margar prentuppsetningar og þarf á að halda. Prentuppsetningar eru skilgreindar í flýtiflipanum **Prentuppsetning**. Eftirfarandi tafla lýsir svæðunum sem eru tiltæk fyrir hverja prentuppsetningu.

| Svæði | lýsing |
|---|---|
| Röð | Skilgreinið röðina sem vísað verður í svæðin í sendingartextanum. |
| Prentsvæði | Veljið svæðin sem nota á í sendingartextanum. Ekki verður hægt að prenta öll svæði fyrir hættuleg efni. Aðeins sameiginlegu svæðin sem notuð eru til að skilgreina afhendingartexta í hinum ýmsu reglugerðum verða í boði. Skilgreina ætti fyrsta prentsvæðið sem svæðaskiltákn sem er með gildi **Röðunar** upp á *0* (núll) svo hægt sé að nota það sem skiltákn milli annarra svæða. Aðeins er krafist einnar tilvísunar í svæðaskiltákn.<p>Eftirtalin gildi eru tiltæk:</p><ul></li><li>**Svæðaskiltákn** - Þetta prentsvæði er notað sem svæðaskiltáknið fyrir textann. Aðeins eitt svæðaskiltákn er nauðsynlegt í röðinni. Yfirleitt ætti að stilla gildi **Röðunar** fyrir þetta prentsvæði á *0* (núll). Kerfið mun leita að svæðaskiltákni og nota það fyrsta sem finnst á listanum. Textagildið sem er notað í strengnum kemur úr svæðinu **Prenta eftir**.</li><li>**Auðkenni** – Þetta prentsvæði setur [auðkenniskóða og/eða lýsingu](#identification) inn í prenttextann.</li><li>**Klasi** – Þetta prentsvæði setur [klasakóða og/eða lýsingu](#classes) inn í prenttextann.</li><li>**Svið** – Þetta prentsvæði setur [sviðskóða og/eða lýsingu](#divisions) inn í prenttextann.</li><li>**Pökkunarflokkur** – Þetta prentsvæði setur [pökkunarflokkskóða og/eða lýsingu](#packing-group) inn í prenttextann.</li><li>**Gangakóði og/eða lýsing** – Þetta prentsvæði setur [gangakóða og/eða lýsingu](#tunnel) inn í prenttextann.</li><li>**Rétt sendingarheiti** – Þetta prentsvæði setur [Rétt sendingarheiti](hazmat-items.md#hazmat-description) inn í prenttextann.</li><li>**Tækniheiti** – Þetta prentsvæði setur [tækniheiti og/eða lýsingu](#technical-name) inn í prenttextann.</li><li>**Flutningsflokkur** – Þetta prentsvæði setur [flutningsflokkunarkóða og/eða lýsingu](#transport-category) inn í prenttextann.</li><li>**Hleðsla** – Þetta prentsvæði setur [hleðslukóða og/eða lýsingu](#stowage) inn í prenttextann.</li><li>**Fastur texti** - Þetta prentsvæði færir inn textann sem er skilgreindur í reitnum **Fastur texti** fyrir þessa línu.</li><li>**Merkiskóði og/eða lýsing** – Þetta prentsvæði setur [merkiskóða og/eða lýsingu](#label) inn í prenttextann.</li><li>**Pökkun fyrir loftfar** – Þetta prentsvæði setur [leiðbeiningar um pökkun fyrir loftfar og/eða lýsingu](#packing-instruction) inn í prenttextann.</li><li>**Takmarkað magn** - Þetta prentsvæði athugar hvort varan sé merkt sem [vara með takmarkað magn](hazmat-items.md#material-management) og ef svo er, færir þá inn textann sem skilgreindur er í reitnum **Fastur texti** fyrir þessa línu.</li><li>**Pökkunarlýsing** – Þetta prentsvæði setur [pökkunarlýsingu](#packing-description) inn í prenttextann.</li></ul> |
| Prenta fyrir | Færa skal inn textann sem á að prenta á undan efninu sem er skilgreint í stillingunni fyrir **Prentsvæði**. |
| Prenta eftir | Færa skal inn textann sem á að prenta á eftir efninu sem er skilgreint í stillingunni fyrir **Prentsvæði**. |
| Prenta með fyrri | Veljið þennan gátreit til að koma í veg fyrir að svæði skiltákns sé prentað á milli fyrra svæðis og þessa svæðis. Notið þennan gátreit til að prenta svæði sem eru annaðhvort valfrjáls eða höfð með í öðru prentsvæði. |
| Fastur texti | Ef reiturinn **Prentsvæði** er stilltur á **Fastur texti** eða **Takmarkað magn** skal færa inn textann sem á að prenta. |
| Hafa með í prentun | Veljið hvaða gildi úr völdu prentsvæði á að prenta fyrir þessa línu. Hægt er að prenta kóðann, lýsinguna eða bæði kóðann og lýsinguna. |

### <a name="mode-of-delivery-fasttab"></a>Flýtiflipi afhendingarmáta

Reglugerðin er samnýtt tafla og á ekki sérstaklega við um hvern lögaðila fyrir sig. Afhendingarmátar eiga hinsvegar við um tiltekinn lögaðila. Þegar afhendingarmáti er settur upp þarf þar af leiðandi að velja tengslin milli reglugerðarinnar, lögaðilans og afhendingarmátans.

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í flýtiflipanum **Afhendingarmáti**.

| Svæði | lýsing |
|---|---|
| Fyrirt.   | Veljið lögaðila sem tengja á við þessa reglugerð. |
| Afhendingarmáti | Á grundvelli lögaðilans sem var valin, skal velja afhendingarmátann sem á að tengjast reglugerðinni. |

### <a name="country-fasttab"></a>Flýtiflipi landa

Til viðmiðunar er hægt að skrá lönd eða landsvæði sem reglugerðin á við um. Þegar skýrslur um sendingar eru keyrðar er hinsvegar aðeins afhendingarmátinn notaður til að ákveða reglugerðina. Þegar vöruhúsaafhending er yfirfarin er ekki beinn tengill á afhendingarmátann. Hægt er að tengja sendinguna við farmflytjanda og flutningsþjónustu. Þegar flutningsþjónusta er skilgreind þarf að tengja hana við afhendingarmáta. Tengslin verða notuð í skýrslum um sendingar, t.d. farmbréf, til að finna prentaðan texta sendingar fyrir vöru.

Eftirfarandi tafla lýsir svæðinu sem er tiltækt í flýtiflipanum **Land**.

| Svæði | lýsing |
|---|---|
| Land/svæði | Veljið land/svæði til að tengja við reglugerðina. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Efniskóðar

Efniskóðar setja á stillingar sem tengjast tilteknum hættulegum efnisþætti sem kann að vera hluti af útgefinni afurð. Hver efniskóði tilheyrir ákveðinni reglugerð um hættuleg efni og skilgreining hans verður að samræmast reglugerðinni. Þegar efniskóði er notaður á útgefna afurð með því að nota reitinn **Efniskóði**, eru stillingar á efniskóða hættulegra efna sjálfkrafa notaðar fyrir þessa afurð. Þess vegna er ferlið við að setja upp útgefnar afurðir hraðara og minni hætta á villum.

Til að stjórna skilgreiningum á hættulegum efnum skal fylgja þessum skrefum.

1. Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Reglugerð hættulegra efna**.
2. Velja skal reglugerðina til að setja upp skilgreiningu á hættulegum efnum fyrir.
3. Á flipanum **Setja upp**, á aðgerðasvæðinu, skal velja **Hættuleg efni**.
4. Í reitinn **Efniskóði** skal færa inn efniskóða fyrir skilgreiningu á hættulegum efnum. Þú velur þetta gildi þegar þú notar efniskóðann á útgefna afurð.

    Reiturinn **Reglugerðarkóði** er skrifvarinn og sýnir reglugerðina sem var valin í skrefi 2.

5. Nota skal eftirstandandi reiti á þessari síðu til að búa til og setja upp sérhvert hættulegt efni sem gildir um valda reglugerð. Svæðin sem eru í boði heyra undir svæði hættulegra efna sem eru tiltæk fyrir einstakar útgefnar afurðir. Frekari upplýsingar er að finna í [Hættuleg efni í afurðum, pöntunum, sendingum og förmum](hazmat-items.md).

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Flokkunarhópar hættulegra efna

Sérhver flokkunarhópur hættulegs efnis skilgreinir hóp af reitargildum sem búa til sniðmát. Hægt er að nota þetta sniðmát síðar þegar upplýsingar um hættuleg efni eru sett upp fyrir losaða vöru.

Þegar kóðanum fyrir flokkunarhóp hættulegs efnis er úthlutað á losaða vöru, verða upplýsingarnar sem tengjast flokkunarhópnum afritaðar í viðeigandi reiti vörunnar. Þess vegna er hægt að einfalda uppsetningarferlið með því að setja upp safn tengdra reitargilda sem oft eru notuð saman.

Þessi uppsetningargögn eru ekki sértæk fyrir hvern lögaðila. Þess vegna er hægt að hafa sameiginlegt safn yfir upplýsingar um hættuleg efni sem er deilt á meðal allra lögaðila.

Til að setja upp flokkunarhóp hættulegra efna skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Flokkunarhópur hættulegra efna**. Á síðunni **Flokkunarhópur hættulegra efna** er hægt að búa til eins marga hópa og þörf er á og skilgreina hvern með því að nota reitina sem lýst er í eftirfarandi töflu.

| Svæði | lýsing |
|---|---|
| Kóði hóps | Færið inn kóða til að auðkenna hópinn. |
| lýsing | Færa inn lýsingu á flokknum. |
| Klasakóði | Tengja [klasakóða](#classes) hættulegra efna við hópinn. |
| Sviðskóði | Tengja [sviðskóða](#divisions) hættulegra efna við hópinn. |
| Pökkunarflokkskóði | Tengið [pökkunarflokkskóða](#packing-group) við hópinn. |
| Flutningsflokkakóði | Tengið [flutningsflokkskóða](#transport-category) við hópinn. |
| Margfaldari | Sláið inn þann margfaldara hættulegra efna sem á við um valdan klasa og svið hættulegra efna samkvæmt viðeigandi reglugerð. Þessi margfaldari er notaður sem hluti af formúlunni sem reiknar út samtölu *stiga hættulegra efna* sem er tekin með í farm eða sendingu. Frekari upplýsingar um stig hættulegra efna og margfaldara þeirra er að finna í [Flýtiflipa fyrir stjórnun efna](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Klasar fyrir hættuleg efni

Klasi hættulegra efna er yfirleitt varpað í lista yfir klasa sem gefinn er upp í reglugerðinni sem fylgt er eftir. Til dæmis gefur bandarísk reglugerð CFR 49 „klasa 3“ upp sem eldfima og sprengifima vökva. Hægt er að setja upp klasana sem tengjast þeim efnum sem þarf að flokka.

Hverjum klasa verður úthlutað á uppsetningu efnis í efnalistanum sem tengist reglugerðinni. Úthluta skal klasa á hverja losaða vöru eins og þörf krefur til að lýsa hættunni sem stafar af afurðinni.

Þessi uppsetningargögn eru ekki sértæk fyrir hvern lögaðila. Þess vegna er hægt að hafa sameiginlegt safn yfir upplýsingar um hættuleg efni sem er deilt á meðal allra lögaðila.

Klasar hættulegra efna vinna saman með sviðum, hópum og samhæfisflokkum á eftirfarandi hátt:

- Þegar klasa hættulegra efna er úthlutað á losaða vöru þarf einnig að úthluta [sviði hættulegra efna](#divisions).
- Hægt er að nota klasa hættulegra efna saman með [flokkunarhópum hættulegra efna](#classification-groups) til að búa til sniðmát af kóðum til að setja upp vörur.
- Hægt er að nota [samhæfisflokka hættulegra efna](#compatibility-groups) til að finna út hvaða klasa og sviði hættulegra efna er hægt að senda saman.

Til að setja upp klasa hættulegra efna skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Klasi hættulegra efna**. Á síðunni **Klasi hættulegra efna** er hægt að búa til óendanlega fjölda klasa og skilgreina hvern með því að nota reitina sem lýst er í eftirfarandi töflu.

| Svæði | lýsing |
|---|---|
| Klasakóði | Færa skal inn kóða sem auðkennir þennan klasa. Skilgreina þarf þennan kóða fyrir vöruna. Hann verður síðan notaður í uppflettilistum þegar klasa hættulegra efna er úthlutað á losaða vöru. |
| lýsing | Færið inn lýsingu á klasanum. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Svið hættulegra efna

Svið hættulegra efna heyrir undir klasa hættulegra efna. Úthluta verður bæði deiliflokki og klasa á sérhverja afurð sem inniheldur hættuleg efni.

Fyrir klasa sem eru ekki með nein svið skal stofna svið þar sem kóðinn er *0*. Í IATA-reglugerðinni eru til dæmis ekki til nein undirsvið í flokki 7 fyrir geislavirk efni. Í þessu tilfelli er hægt að stofna svið *0* sem hægt er að tengja við útgefna afurð þegar klasanum er úthlutuð.

Þessi uppsetningargögn eru ekki sértæk fyrir hvern lögaðila. Þess vegna er hægt að hafa sameiginlegt safn yfir upplýsingar um hættuleg efni sem er deilt á meðal allra lögaðila.

Svið hættulegra efna vinna saman með klösum, hópum og samhæfisflokkum á eftirfarandi hátt:

- Þegar sviði hættulegra efna er úthlutað á losaða vöru þarf einnig að úthluta [klasa hættulegra efna](#classes).
- Hægt er að nota svið hættulegra efna saman með [flokkunarhópum hættulegra efna](#classification-groups) til að búa til sniðmát af kóðum til að setja upp vörur.
- Hægt er að nota [samhæfisflokka hættulegra efna](#compatibility-groups) til að finna út hvaða klasa og sviði hættulegra efna er hægt að senda saman.

Til að setja upp svið hættulegra efna skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Svið hættulegra efna**. Á síðunni **Svið hættulegra efna** er hægt að búa til eins mörg svið og þörf er á og skilgreina hvert þeirra með því að nota reitina sem lýst er í eftirfarandi töflu.

| Svæði | lýsing |
|---|---|
| Skipting | Sláið inn kóða sem á að nota sem tilvísunarnúmer fyrir sviðið. |
| lýsing | Færðu inn lýsingu á sviðinu. |
| Klasi | Flettið upp og úthlutið klasanum sem sviðið tilheyrir. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Samhæfisflokkar hættulegra efna

Samhæfisflokkar hættulegra efna gefa upp hvaða klasa og svið hættulegra efna er hægt að senda saman. Þegar notendur búa til farma eða sendingar í vöruhúsi, geta þeir keyrt samhæfisathugun sem gefur út viðvörun ef farmurinn eða sendingin inniheldur vörur sem tilheyra ekki sama samhæfingarflokknum.

Þessi uppsetningargögn eru ekki sértæk fyrir hvern lögaðila. Þess vegna er hægt að hafa sameiginlegt safn yfir upplýsingar um hættuleg efni sem er deilt á meðal allra lögaðila.

Til að setja upp samhæfingarflokka hættulegrar efnismeðferðar skal fara á **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Samhæfisflokkur hættulegra efna**. Á síðunni **Samhæfisflokkur hættulegra efna** er hægt að búa til eins marga samhæfisflokka og þörf er á og skilgreina hvern með því að nota reitina sem lýst er í eftirfarandi undirhlutum.

### <a name="hazardous-material-compatibility-group-header"></a>Síðuhaus samhæfisflokks hættulegra efna

Hver samhæfisflokkur er með kóða og lýsingu. Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í hausnum.

| Svæði | lýsing |
|---|---|
| Samhæfisflokkur | Færið inn kóða til að auðkenna samhæfisflokkinn |
| lýsing | Færið inn lýsingu á samhæfisflokknum. |

### <a name="compatibility-group-details"></a>Upplýsingar samhæfisflokks

Hver samhæfisflokkur er með lista yfir klasa og svið hættulegra efna sem hægt er að senda saman.

| Svæði | lýsing |
|---|---|
| Klasi | Veljið klasa hættulegra efna sem samræmist öllum öðrum klösum í hópnum. |
| Skipting | Veljið svið hættulegra efna sem tilheyrir völdum klasa. |

## <a name="hazardous-material-specification-values"></a>Tækniforskriftir hættulegra efna

Microsoft Dynamics 365 Supply Chain Management býður upp á nokkrar gerðir af tækniforskriftum hættulegra efna. Fyrir hverja gerð þarf að koma á miðstýrðu safni af gildum fyrir hvert viðeigandi svæði. Notendur geta þá valið á milli þessara gilda þegar þeir stilla skilgreiningar hættulegra efna eða útgefnar afurðir. Supply Chain Management býður upp á safn af síðum þar sem hægt er að setja inn gildin. Hver síða er tileinkuð einni gerð tækniforskriftar. Lýsing á hverri tiltækri forskrift og upplýsingar um hvernig á að koma á gildunum sem eru tiltæk fyrir hana er að finna í eftirfarandi undirköflum.

Eitt dæmi um forskrift hættulegra efna er _hleðslukóðinn_ sem tilgreinir hvernig hægt er að geyma uppgefið efni í flutningi. Með því að nota upplýsingarnar í þessum hluta er sett upp miðlægt safn geymslukóða. Þetta safn verður síðan kynnt notendum í fellilista þegar þeir stilla geymslukóða fyrir útgefna afurð.

Þessi forskriftargildi hættulegra efna eiga ekki við um ákveðinn lögaðila og er því hægt að hafa safn af algengum gildum sem eru samnýtt á meðal allra lögaðila.

[Efniskóðar](#hazmat-codes) verða notaðir til að setja á safn af algengum stillingum fyrir hverja forskrift eins og það á við fyrir hverja reglugerð. Síðan er hægt að nota viðeigandi kóða fyrir hverja útgefna afurð eftir þörfum. Upplýsingar um hvernig á að nota efniskóða hættulegra efna fyrir ákveðna útgefna afurð og hvernig á að skilgreina einstakar stillingar fyrir þá afurð fyrir hvaða forskrift sem er sem lýst er hér, skal skoða [Hættuleg efni í afurðum, pöntunum, sendingum og förmum](hazmat-items.md).

### <a name="hazardous-material-emergency-response"></a>Neyðaráætlun fyrir hættuleg efni

Forskriftin *Neyðaráætlun fyrir hættuleg efni* segir til um hvað skuli gera ef eitthvað fer úrskeiðis við flutning á afurð sem inniheldur tiltekið hættulegt efni.

Til að setja upp gildi fyrir þessa forskrift skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Neyðaráætlun fyrir hættuleg efni**. Á síðunni **Neyðaráætlun fyrir hættuleg efni** er hægt að búa til eins mörg gildi og þarf og skilgreina hvert þeirra með auðkennandi kóða og stuttri lýsingu.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Auðkenning hættulegra efna

Forskriftin *Auðkenning hættulegra efna* tilgreinir klasann eða hættuna sem stafar af efninu. Gildið er yfirleitt kóði sem byggir á staðli Sameinuðu þjóðanna (SÞ). Hver klasi er auðkenndur með kóða og lýsingu og hann getur sett takmörk á flutningsmáta. Til að auðkenna eldfima vöru eða efni þarf til dæmis að búa til klasa hættulegra efna sem notar kóðann *FL* og lýsinguna *Eldfimt*. Einnig er tilgreint að ekki megi flytja klasann flugleiðis.

Til að setja upp gildi fyrir þessa forskrift skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Auðkenning hættulegra efna**. Á síðunni **Auðkenning hættulegra efna** er hægt að búa til eins mörg gildi og þörf er á og skilgreina hvert þeirra með því að nota reitina sem lýst er í eftirfarandi töflu.

| Svæði | lýsing |
|---|---|
| Auðkenning | Sláið inn kóða sem á að nota sem tilvísunarnúmer sem tilgreinir þennan klasa yfir hættuleg efni. |
| lýsing | Færið inn lýsingu á þessum klasa. |
| Loka á flutning í lofti | Veljið þennan gátreit til að gefa til kynna að ekki eigi að flytja þennan klasa af hættulegum efnum í lofti. |
| Loka á flutning á sjó | Veljið þennan gátreit til að gefa til kynna að ekki eigi að flytja þennan klasa af hættulegum efnum á sjó. |

### <a name="hazardous-material-label"></a><a name="label"></a>Merki fyrir hættuleg efni

Forskriftin *Merki fyrir hættuleg efni* tilgreinir merki hættulegs varnings sem setja verður á tilheyrandi útgefnar afurðir. Merkimiðarnir sjálfir lýsa því hvernig á að meðhöndla afurðina. Til dæmis er til afurð sem inniheldur eitrað gas. Í þessu tilviki er settur upp merkjakóði sem stendur fyrir merki eitraðs gass. Einnig eru viðskiptaferli byggt upp þannig að það leiti að þessu gildi þegar afurðir eru sendar.

Til að setja upp gildi fyrir þessa forskrift skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Merki fyrir hættuleg efni**. Á síðunni **Merki fyrir hættuleg efni** er hægt að búa til hvers kyns merkimiða og skilgreina hvern með auðkennandi kóða og stuttri lýsingu.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Pökkunarlýsing hættulegra vara

Forskriftin *Pökkunarlýsingar hættulegra vara* tilgreinir hvernig skuli pakka hættulegu efni. Til dæmis gæti þurft að pakka því í sérstaka gerð af stáltunnu eða einhvers konar aðra sérpakkningu.

Til að setja upp gildi fyrir þessa forskrift skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Pökkunarlýsingar fyrir hættuleg efni**. Á síðunni **Pökkunarlýsingar hættulegra vara** er hægt að búa til eins margar pökkunarlýsingar og þarf og skilgreina hverja þeirra með auðkennandi kóða og stuttri lýsingu.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Pökkunarflokkur hættulegra efna

Forskriftin *Pökkunarflokkur hættulegra efna* tilgreinir pökkunarflokkinn fyrir hættulegt efni. Pökkunarflokkurinn gerir kleift að skilgreina kóða og lýsingu til að gefa til kynna hvernig eigi að pakka inn hættulegum efnum við flutning eða sendingu. Pökkunarflokknum er úthlutað á vöruna í gegnum síðuna **Hættuleg efni vöru**.

Til að setja upp gildi fyrir þessa forskrift skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Pökkunarflokkur fyrir hættuleg efni**. Á síðunni **Pökkunarflokkur fyrir hættuleg efni** er hægt að búa til eins marga pökkunarflokka og þarf og skilgreina hvern þeirra með auðkennandi kóða og stuttri lýsingu.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Pökkunarleiðbeiningar hættulegra vara

Forskriftin *Pökkunarleiðbeiningar hættulegra vara* tilgreinir pökkunarleiðbeiningar sem þarf að fylgja eftir þegar tiltekið hættulegt efni er undirbúið undir flutning loftleiðis.

Til að setja upp gildi fyrir þessa forskrift skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Pökkunarleiðbeiningar fyrir hættuleg efni**. Á síðunni **Pökkunarleiðbeiningar fyrir hættuleg efni** er hægt að búa til eins margar pökkunarleiðbeiningar og þarf og skilgreina hverja þeirra með auðkennandi kóða og stuttri lýsingu.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Hleðsla hættulegra efna

Forskriftin *Hleðsla hættulegra efna* tilgreinir hvernig eigi að geyma afurð á skipi þegar hún er flutt sjóleiðis.

Til að setja upp gildi fyrir þessa forskrift skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Hleðsla fyrir hættuleg efni**. Á síðunni **Hleðsla fyrir hættuleg efni** er hægt að búa til eins margar hleðslumerkingar og þarf og skilgreina hverja þeirra með auðkennandi kóða og stuttri lýsingu.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Flutningsflokkur hættulegra efna

Forskriftin *Flutningsflokkur hættulegra efna* er yfirleitt notuð til að flokka saman svipaðar hættulegar afurðir í skýrslum. Til dæmis eru flutningsflokkar notaðir í skýrslunni **Samantekt sendingar** sem hægt er að prenta úr afhendingarfærslu vöruhúss.

Til að setja upp gildi fyrir þessa forskrift skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Flutningsflokkur hættulegra efna**. Á síðunni **Flutningsflokkur hættulegra efna** er hægt að búa til eins marga flutningsflokka og þarf og skilgreina hvern þeirra með birtingarnafni og stuttri lýsingu.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Tækniheiti hættulegra efna

Forskriftin *Tækniheiti hættulegra efna* er hægt að nota til að gefa upp almennt heiti eða heiti innan fyrirtækisins sem lýsir hverju efni fyrir sig.

Til að setja upp gildi fyrir þessa forskrift skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Tækniheiti hættulegra efna**. Á síðunni **Tækniheiti hættulegra efna** er hægt að búa til eins mörg tækniheit og þarf og skilgreina hvert þeirra með birtingarnafni og stuttri lýsingu.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Hættuleg efni í göngum

Forskriftin *Hættuleg efni í göngum* takmarkar gerðir ganga sem má flytja hættulegt efni í gegnum með því að gefa upp gangagerðirnar sem þarf að nota. Gangaflokkar eru settir á samkvæmt viðeigandi reglugerðum fyrir flutning á hættulegum efnum. Þessi skilgreining á yfirleitt aðeins við um flutning á vegum.

Til að setja upp gildi fyrir þessa forskrift skal fara í **Afurðaupplýsingastjórnun \> Uppsetning \> Fylgiskjöl fyrir sendingu hættulegra efna \> Hættuleg efni í göngum**. Á síðunni **Hættuleg efni í göngum** er hægt að búa til eins margar gangamerkingar og þarf og skilgreina hverja þeirra með auðkennandi kóða og stuttri lýsingu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]