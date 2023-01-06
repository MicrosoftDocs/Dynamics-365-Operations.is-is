---
title: Birgðabókunarreglur
description: Þessi grein veitir yfirlit yfir birgðabókunarreglur.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cae5b39ef8e6e153fe522dee1874deae2a2cb86e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901343"
---
# <a name="inventory-posting-profiles"></a>Birgðabókunarreglur

[!include [banner](../includes/banner.md)]

Birgðabókunarreglur stýra bókun á birgðaundirbókarfærslum í fjárhag. Hægt er að stofna fjárhagsfærslur undirbókar úr mörgum einingum þ.m.t. **Sala og markaðssetning**, **Innkaup og aðföng**, **Framleiðslustýring** og fleira. Birgðafærslur undirbókar gætu verið bókaðar í hvert skipti sem vara er notuð í sölupöntun eða innkaupapöntun. 

Fleiri birgðaundirbókarfærslur gætu verið bókaðar:
- Í hvert skipti sem skjal er uppfært.
- Þegar fylgiseðill eða reikningur sölupöntunar er bókaður.
- Þegar afurðarinnhreyfing innkaupapöntunar eða reiknings er stofnuð.

Frekari upplýsingar er að finna á „Undirbókarfærslur birgða“.

## <a name="inventory-transaction-overview"></a>Birgðafærsluyfirlit

Hver undirbókarfærsla birgða inniheldur:
 - Magn 
 - Verð 
 - Svæði 
 - Vöruhús 
 - Staðsetning 

Birgðafærslur undirbókar stofna tvær færslur í fjárhagnum í gegnum efnislega bókun og fjárhagslega bókun. Frekari upplýsingar er að finna á [Efnislegar og fjárhagslegar uppfærslur](/supply-chain/cost-management/physical-financial-updates.md).
Eftirfarandi dæmi er innkaupapöntun með þremur línum. Í þessu dæmi gerum við ráð fyrir að öll pöntunin sé fyrir eitt vefsvæði og vöruhús. Hver innkaupapöntunarlína er með eina tengda InventTrans færslu – einnig þekkt sem birgðafærsla – og hver lína er fyrir magn upp á 10. Eftirfarandi skýringarmynd sýnir tengsl eins innkaupapöntunarhauss við þrjár innkaupapöntunarlínur, hver með eina InventTrans færslu.

![Tengslaskýringarmynd fyrir innkaupapöntun með þremur línum, hver með eina InventTrans-færslu.](./media/InventTransRelationship.PNG)

Tekið er á móti 5 í fyrstu innkaupapöntunarlínu. Fullt magn fyrir aðra línuna og ekkert magn móttekið í þriðju línu innkaupapöntunarinnar. Nú er önnur birgðafærsla í tengslum við fyrstu innkaupapöntunarlínuna. Færslan fyrir aðra innkaupapöntunarlínuna verður uppfærð í **Móttekið** og þriðja færslan verður óbreytt. Eftirfarandi skýringarmynd sýnir sambandið við viðbótarfærslu InventTrans fyrir innkaupapöntunarlínu 1.

![Tengslaskýringarmynd fyrir innkaupapöntun með þremur línum. Ein lína er að hluta til móttekin og sýnir tvær InventTrans-færslur.](./media/InventTransRelationshipPartialReceipt.PNG)

Í þessu dæmi er fylgiskjal bókað í fjárhag. Þetta er efnislega fylgiskjalið. Vörulíkanaflokkurinn er grunnstilltur til að bóka efnislegar birgðir og allar vörur nota sama vörulíkanaflokkinn. Birgðabókunarreglan er notuð með einu setti af aðallyklum. Eitt fylgiskjal verður búið til og InventTrans færslan mun tengja bæði InventTrans 1 og InventTrans 2 við sama fylgiskjalið.

Því næst er reikningur móttekinn fyrir magnið sem er móttekið á línum 1 og 2. Annað fylgiskjal er stofnað í fjárhagnum; þetta er fjárhagslegt fylgiskjal. Vörulíkanaflokkurinn er grunnstilltur til að birta fjárhagslegar birgðir. Nýr annar afsláttarmiði tengist InventTrans 1 og InventTrans 2.

Það fer eftir líkani kostnaðarútreiknings hvort þriðja fjárhagsbókunin er til staðar fyrir birgðafærslur undirbókar sem tengjast lokun og jöfnun birgðanna. Frekari upplýsingar er að finna á [Birgðalokun](/supply-chain/cost-management/inventory-close.md). Hægt er að skoða upplýsingar um allar birgðafærslur með því að fara í **Birgðastjórnun** > **Fyrirspurnir og skýrslur** > **Færslur**.

>[!Important]
> Birgðafærslum verður skipt fyrir hverja einstaka samsetningu birgðavídda og fyrir hverja hlutauppfærslu. Þetta var sýnt í dæminu á undan fyrir hlutauppfærslur.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Dæmi um skiptingu birgða á grunni birgðavíddar

Innkaupapöntunarlína 3 í dæminu er raðtengd vara. Tíu raðnúmer eru skráð fyrir innkaupapöntuninni í móttökuferlinu. Birgðafærslunni verður skipt upp í 10 birgðafærslur. Eftirfarandi skýringarmynd sýnir tengslin og frekari birgðafærslur, hver með sitt raðnúmer sem tengist innkaupapöntunarlínu 3.

![Tengslaskýringarmynd fyrir innkaupapöntun með þremur línum. Ein lína er raðgreind og sýnir fleiri InventTrans-færslur.](./media/InventTransRelationshipSerialNumber.PNG)

Í dæminu hér að ofan, ef hvert raðnúmer er móttekið í einu innhreyfingarskjali afurðar verður annað fylgiskjal búið til. Reiturinn fyrir efnislegt fylgiskjal verður tengdur við hvert raðnúmer. Það sama á við um fjárhagsuppfærsluna þegar þú reikningsfærir innkaupapöntunina.

## <a name="inventory-transactions"></a>Birgðafærslur

Hægt er að skoða birgðafærslur á síðunni **Birgðafærslur** undir **Birgða- og vöruhúsakerfi** eða **Kostnaðarstjórnun**. Einnig er hægt að skoða birgðafærslur sem tengjast tiltekinni upprunaskjalalínu - svo sem innkaupapöntunarlínu eða sölupöntunarlínu - með því að velja **Birgðir** og velja svo **Færslur**. 

Síðan **Birgðafærslur** inniheldur eftirfarandi reiti.

| Svæði            | Lýsing                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Vörunúmer      | Vörunúmer tengt færslunni.                                                                  |
| Efnisleg dagsetning    | Dagsetningin sem birgðirnar koma í vöruhúsið, fara úr vöruhúsinu, eru notaðar í framleiðslu eða eru framleiddar. Til dæmis bókunardagsetningin á
fylgiseðillinn fyrir sölupöntun eða bókun innhreyfingarskjals afurðar fyrir innkaupapöntun.                             |
| Fjárhagsdagsetning   | Dagsetning birgðafærslunnar er lokuð og kostnaðurinn er skráður í fjárhag. Til dæmis bókunardagsetningin á reikningnum 
myndun fyrir sölu- eða innkaupapöntun. Uppfærslur á tilvísunarskjalinu eru ekki leyfðar eftir að fjárhagsdagur er fylltur út. |
| Tilvísun        | Gefur til kynna uppruna færslunnar og tegund fylgiskjalsins sem birtist í reitnum **Númer**. Til dæmis innhreyfing sölupöntunar, innkaupapöntunar eða flutningspöntunar.                                                 |
| Númer           | Gefur til kynna tilvísanakenni færslu. Ef til dæmis reiturinn **Tilvísun** gefur til kynna sölupöntun gefur reiturinn **Númer** til kynna sölupöntunarnúmerið.                                                       |
| Innhreyfing (staða) | Í birgðafærslum sem eru innhreyfingar sýnir þessi reitur stöðu innhreyfingarinnar. Til dæmis er innkaupapöntun innhreyfing og staða gæti verið **Pantað** eða **Keypt**.                                                            |
| Útgáfa (staða)   | Fyrir birgðafærslur sem eru vandamál sýnir þessi reitur stöðu vandamálsins. Til dæmis er sölupöntun vandamál og staðan gæti verið **Í pöntun** eða **Selt**.                         |
| Magn         | Magn birgðafærslunnar. Jákvæðar tölur eru notaðar fyrir innhreyfingar á birgðum á meðan neikvæðar tölur eru notaðar fyrir úthreyfingar úr birgðum.                                                                                                                          |
| Eining             | Mælieiningin sem magnið er gefið upp í.                                                                                   |
| Þyngd afurðar, magn      | Magn framleiðsluþyngdar fyrir færsluna. Frekari upplýsingar er að finna á [Um framleiðsluþyngd vara](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Þyngd afurðar, eining          | Mælieining framleiðsluþyngdar sem framleiðsluþyngdarmagnið er gefið upp í.                                                         |
| Kostnaðarupphæð      | Endanlegur kostnaður við birgðafærsluna. Þessi reitur er fylltur út þegar færsla er uppfærð fjárhagslega. Birgðalokun og breytingarferli gætu uppfært þennan reit eftir því hvaða aðferð kostnaðarútreiknings er notuð.                            |

## <a name="inventory-status"></a>Birgðastaða

Hver birgðafærsla er með stöðu sem er sýnd í annaðhvort reitnum **Innhreyfing** eða **Úthreyfing**. Reiturinn sem er notaður fer eftir gerð birgðafærslna. Innhreyfingar eru færslur sem auka birgðirnar. Til dæmis innkaupapöntun með jákvæðu magni eða sölupöntun með neikvæðu magni. Vandamál eru birgðafærslur sem minnkuðu birgðir. Til dæmis sölupöntun með jákvæðu magni eða innkaupapöntun með neikvæðu magni.

### <a name="receipt-status"></a>Staða innhreyfingar

Eftirfarandi tafla lýsir stöðu **Innhreyfing**.

| **Staða innhreyfingar** | **Lýsing**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Raðað            | Upphafleg staða birgðafærslna sem tákna innhreyfingu. Þar með talið eru innkaupapantanir með jákvæðu magni, framleiðslupantanir eða sölupöntunarskil með neikvæðu magni.                                                   |
| Skráð         | Þessi staða er notuð þegar tveggja skrefa móttökuferli er til staðar eða þegar vörukoma er notuð til að gefa til kynna að varan sé komin. Það er notað þegar runu- eða raðnúmerum er "úthlutað" eða skráð á pöntunina. Frekari upplýsingar um komu vöru er að finna í [Komuyfirlit](/supply-chain/inventory/arrival-overview.md). |
| Móttekið           | Þessi staða er notuð þegar færslan er uppfærð efnislega. Fyrir innkaupapöntun er þetta þegar innhreyfingarskjal afurða er bókað. Fyrir sölupöntunarskil er þetta tími bókunar fylgiseðilsins.                                                                            |
| Keypt          | Þessi staða er notuð þegar færslan er uppfærð fjárhagslega. Fyrir skil á innkaupapöntun eða sölupöntun er það þegar reikningurinn er myndaður.                                                                                             |

### <a name="issue-status"></a>Útgáfustaða

Eftirfarandi tafla lýsir stöðu **Úthreyfing**.

| **Útgáfustaða**  | **Lýsing**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Í pöntun          | Upphafleg staða birgðafærslna sem táknar vandamál. Þetta á við um sölupantanir með jákvæðu magni, uppskrift framleiðslupöntunar eða formúlulínur eða innkaupapöntunarskil með neikvæðu magni.                                             |
| Frátekið pantað  | Þessi birgðastaða gefur til kynna að birgðir séu fráteknar vegna pöntunar sem var stofnuð, en ekki ennþá efnislega fráteknar í birgðum. Þegar birgðirnar eru mótteknar uppfærist staðan sjálfkrafa í **Frátekið efnislegt magn**. Frekari upplýsingar um frátektir er að finna í [Taka frá birgðamagn](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Frátekið á lager | Þessi staða gefur til kynna að birgðum hafi verið úthlutað eða þær teknar frá vegna tiltekinnar pöntunar. Þegar birgðir eru fráteknar eru þær ekki efnislega í boði fyrir aðrar pantanir.                                 |
| Tekið til         | Þetta gefur til kynna að birgðirnar hafi verið sóttar úr vöruhúsinu. Birgðirnar eru enn í vöruhúsinu, þær hafa ekki verið fjarlægðar en eru ekki tiltækar fyrir aðrar pantanir.  |
| Frádregið          | Þessi staða er notuð þegar færslan er uppfærð efnislega. Fyrir sölupöntun er þetta þegar fylgiseðill er bókaður; fyrir innkaupapöntunarskila er þetta þegar innhreyfingarskjal er bókað.                                                                      |
| Selt              | Þetta er staðan sem er notuð þegar færslan er uppfærð fjárhagslega. Fyrir innkaupapöntun eða sölupöntun er þetta þegar reikningurinn er myndaður.|

Frekari upplýsingar um birgðafærslurnar er að finna í [Birgðafærsluupplýsingar](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Skilgreina birgðabókunarreglu

Til að stilla birgðabókunarreglu skal fylgja þessum skrefum:

1.  Opnið **Birgðastjórnun** > **Uppsetning** > **Bókun** > **Bókun**.
2.  Veljið flipann fyrir gerð færslunnar. Veljið t.d. **Innkaupapöntun**.
3.  Veljið hnapp fyrir bókunargerðina. Veljið t.d. **Innkaupaútgjöld kostnaðar**.
4.  Veljið **Nýtt**.
5.  Veljið valkost á svæðinu **Vörukóði** fyrir **Tafla**, **Flokkur**, **Allt** eða **Flokkur**. Til dæmis, til að skilgreina bókunarreglu fyrir tiltekinn vöruflokk, velur þú **Hópur**.
     - Ef **Tafla** var valin í skrefi 5 skal velja vörunúmer fyrir bókunarregluna í reitnum **Vöruvensl**.
     - Ef **Flokkur** er valið í skrefi 5 skal velja **Vöruflokkur** fyrir bókunarregluna á svæðinu **Vöruvensl**.
     - Ef **Allt** er valið í 5. skrefi er reiturinn **Vöruvensl** auður.
     - Ef **Flokkur** er valið í 5. skrefi er reiturinn **Vöruvensl** auður. Notið reitinn **Tegundavensl** til að velja flokkinn sem bókunarreglan á við um.

6.  Á svæðinu **Kóði lykils** skal velja valkost fyrir **Tafla**, **Flokkur** eða **Allt**. Til dæmis til að úthluta bókunarreglu á alla lánardrottna skal velja **Allt**.
     - Ef **Tafla** var valið í skrefi 5 skal velja tiltekið númer lánardrottins fyrir bókunarregluna í reitnum **Lyklavensl**.
     - Ef **Flokkur** var valið í skrefi 5 skal velja lánardrottnaflokk fyrir bókunarregluna í reitnum **Lyklavensl**.
     - Ef **Allt** er valið í 5. skrefi er reiturinn **Lyklavensl** auður.

7.  Til að tengja tiltekinn skattflokk sem er með valda bókunargerð skal velja **VSK-flokkur**. Ef þetta svæði er autt mun bókunargerðin eiga við um alla fyrirliggjandi skattaflokka. Bókun sem er tilgreind fyrir skattflokka á einungis við um sölu- og innkaupafærslur.
8.  Tilgreinið lykilnúmerið til að bóka við lykilgerðina á svæðinu **Aðallykill**. Ef lykilnúmer hefur ekki verið stofnað til að nota sem bókhaldsgerð er hægt að stofna nýjan lykil. Þú stofnar nýjan lykil á síðunni **Upplýsingar um aðallykil** í fjárhag.

## <a name="additional-resources"></a>Frekari upplýsingar

Hver flipi á síðunni **Birgðabókunarregla** tengist undirbók í Dynamics 365 Supply Chain Management. Nánari upplýsingar má sjá á:
-   [Bókun sölupöntunar](sales-order-posting.md)
-   [Bókun innkaupapöntunar](purchase-order-posting.md)
-   [Birgðabókun](inventory-posting.md)
-   [Bókun á framleiðslustýringu](production-posting.md)
-   [Bókun á stöðluðu kostnaðarfráviki](standard-cost-variance-posting.md)
