---
title: Skráningarsnið
description: Þetta efni veitir yfirlit yfir birgðafærslusnið.
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
ms.openlocfilehash: 28e3a3051978f921e01a929496e96909e6c32429
ms.sourcegitcommit: 00b39900d3cbdbc9ca1ab3145265007f5dc98a3f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/25/2022
ms.locfileid: "8806387"
---
# <a name="inventory-posting-profiles"></a>Skráningarsnið

[!include [banner](../includes/banner.md)]

Birgðabókunarsnið stjórna bókun á birgðaundirbókarfærslum í aðalbókina. Hægt er að búa til birgðafærslur úr mörgum einingum, þar á meðal **Sala og markaðssetning**, **og innkaup**, **·**, og fleira. Birgðaundirbókarfærslur gætu verið bókaðar hvenær sem vara er notuð í sölupöntun eða innkaupapöntun. 

Viðbótarfærslur í birgðaundirbók gætu verið bókaðar:
- Í hvert sinn sem skjal er uppfært.
- Þegar fylgiseðill sölupöntunar eða reikningur er bókaður.
- Þegar innkaupapöntun vörukvittun eða reikningur er myndaður.

Fyrir frekari upplýsingar, farðu í Birgðafærslur undirbókar.

## <a name="inventory-transaction-overview"></a>Yfirlit yfir birgðafærslur

Hver birgðaundirbókarfærsla inniheldur:
 - Magn 
 - Verð 
 - Svæði 
 - Vöruhús 
 - Staðsetning 

Birgðaundirbókarfærslur búa til tvær færslur í aðalbókinni í gegnum efnisbókunina og fjárhagsbókunina. Fyrir frekari upplýsingar, farðu á [Líkamlegar og fjárhagslegar uppfærslur](/supply-chain/cost-management/physical-financial-updates.md).
Eftirfarandi dæmi er innkaupapöntun með þremur línum. Í þessu dæmi, gerðu ráð fyrir að öll pöntunin sé fyrir eina síðu og vöruhús. Hver innkaupapöntunarlína hefur eina tengda InventTrans skrá – einnig þekkt sem birgðafærsla – og hver lína er fyrir 10 magn. Eftirfarandi skýringarmynd sýnir tengsl eins innkaupapöntunarhauss við þrjár innkaupapöntunarlínur, hver með einni InventTrans færslu.

![Tengsl skýringarmynd fyrir innkaupapöntun með þremur línum hver með einni InventTrans færslu.](./media/InventTransRelationship.PNG)

Magn upp á 5 er móttekið í fyrstu innkaupapöntunarlínu. Allt magn fyrir aðra línu og ekkert magn móttekið á þriðju línu innkaupapöntunarinnar. Það er nú önnur birgðafærsla sem tengist fyrstu innkaupapöntunarlínunni. Færslan fyrir aðra innkaupapöntunarlínu verður uppfærð í **Tekið á móti**, og þriðja viðskiptin verða óbreytt. Eftirfarandi skýringarmynd sýnir tengslin við viðbótar InventTrans færslu fyrir innkaupapöntunarlínu 1.

![Tengsl skýringarmynd fyrir innkaupapöntun með þremur línum. Ein lína er móttekin að hluta og sýnir tvær InventTrans færslur.](./media/InventTransRelationshipPartialReceipt.PNG)

Í þessu dæmi verður fylgiskjal bókað í aðalbókina; þetta er líkamlega skírteinið. Vörulíkanaflokkurinn er stilltur til að bóka efnislegar birgðir og allar vörur nota sama vörulíkanaflokk. Birgðabókunarsniðið notar eitt sett af aðalreikningum. Einn skírteini verður búinn til og InventTrans skráin mun tengja bæði InventTrans 1 og InventTrans 2 við sama skírteini.

Næst berst reikningur fyrir magnið sem er móttekið á línum 1 og 2. Annað fylgiskjal er búið til í aðalbókinni; þetta er fjárhagsskírteinið. Vörulíkanaflokkurinn er stilltur til að bóka fjárhagsbirgðir. Nýja seinni skírteinið tengist InventTrans 1 og InventTrans 2.

Það fer eftir kostnaðarlíkaninu, þriðja fjárhagsbókun gæti verið til fyrir birgðaundirbókarfærslur þínar sem tengjast lokun og uppgjöri birgða. Fyrir frekari upplýsingar, farðu á [Birgðalokun](/supply-chain/cost-management/inventory-close.md). Þú getur skoðað upplýsingar um allar birgðafærslur með því að fara á **Vörustjórnun** > **Fyrirspurnir og skýrslur** > **Viðskipti**.

>[!Important]
> Birgðafærslunum verður skipt fyrir hverja einstaka samsetningu birgðavídda og fyrir hverja hlutauppfærslu. Þetta var sýnt í dæminu á undan fyrir uppfærslur að hluta.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Skiptu birgðum byggt á birgðavíddardæmi

Innkaupapöntunarlínan 3 í dæminu er raðnúmeruð vara. Tíu raðnúmer eru skráð fyrir innkaupapöntunina meðan á móttökuferlinu stendur. Birgðafærslunni verður skipt í 10 birgðafærslur. Eftirfarandi skýringarmynd sýnir sambandið og viðbótarbirgðafærslur, hver með sínu raðnúmeri sem tengist innkaupapöntunarlínu 3.

![Tengsl skýringarmynd fyrir innkaupapöntun með þremur línum. Ein lína er sett í röð og sýnir fleiri InventTrans færslur](./media/InventTransRelationshipSerialNumber.PNG)

Í dæminu hér að ofan, ef hvert raðnúmer er móttekið á einni vörukvittun, verður ein aukaskírteini búin til. Raunverulegi fylgiskjölareiturinn verður tengdur hverju raðnúmeri. Sama gildir um fjárhagsuppfærsluna þegar þú reikningsfærir innkaupapöntunina.

## <a name="inventory-transactions"></a>Birgðafærslur

Þú getur skoðað birgðafærslur á **Birgðaviðskipti** síðu undir **Birgða- og vörustjórnun** eða **Kostnaðarstjórnun**. Þú getur líka skoðað birgðafærslur sem tengjast tiltekinni upprunaskjalslínu—svo sem innkaupapöntunarlínu eða sölupöntunarlínu—með því að velja **Birgðir** og velja síðan **Viðskipti**. 

The **Birgðaviðskipti** síða inniheldur eftirfarandi reiti.

| Reitur            | Lýsing                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Vörunúmer      | Vörunúmerið sem tengist viðskiptunum.                                                                  |
| Efnisleg dagsetning    | Dagsetningin sem birgðahaldið kemur í vöruhúsið, fer úr vöruhúsinu, er notað í framleiðslu eða framleitt. Til dæmis, birtingardagsetning á
Bókun fylgiseðils fyrir sölupöntun eða vörukvittunarbókun fyrir innkaupapöntun.                             |
| Fjárhagsdagsetning   | Dagsetningin sem birgðafærslunni er lokað og kostnaðurinn er skráður í fjárhag. Til dæmis bókunardagsetningin á reikningnum 
Kynslóð fyrir sölu- eða innkaupapöntun. Uppfærslur á tilvísunarskjalinu eru ekki leyfðar eftir að fjárhagsdagsetning er fyllt út. |
| Tilvísun        | Gefur til kynna uppruna færslunnar og tegund skjals sem birtist í **Númer** sviði. Til dæmis sölupöntun, innkaupapöntun eða kvittun fyrir flutningspöntun.                                                 |
| Númer           | Gefur tilvísunarauðkenni fyrir færslu. Til dæmis, ef **Tilvísun** reiturinn sýnir sölupöntun, sem **Númer** reiturinn sýnir sölupöntunarnúmerið.                                                       |
| Kvittun (staða) | Fyrir birgðafærslur sem eru innhreyfingar sýnir þessi reitur stöðu innhreyfingarinnar. Til dæmis er innkaupapöntun kvittun og staðan gæti verið **Pantaði** eða **Keypt**.                                                            |
| Mál (staða)   | Fyrir birgðafærslur sem eru útgáfur gefur þessi reitur til kynna stöðu útgáfunnar. Til dæmis er sölupöntun vandamál og staðan gæti verið **Á pöntun** eða **Seldur**.                         |
| Magn         | Magn birgðafærslunnar. Jákvæðar tölur eru notaðar fyrir innhreyfingar til birgða á meðan neikvæðar tölur eru notaðar fyrir útgáfur úr birgðum.                                                                                                                          |
| Eining             | Mælieiningin sem magnið er gefið upp í.                                                                                   |
| Þyngd afurðar, magn      | Aflaþyngdarmagn fyrir viðskiptin. Fyrir frekari upplýsingar, farðu á [Um aflaþyngdarhluti](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Þyngd afurðar, eining          | Aflaþyngdarmælieiningin sem aflaþyngdarmagnið er gefið upp í.                                                         |
| Kostnaðarupphæð      | Lokakostnaður við birgðafærsluna. Þessi reitur er fylltur út þegar færsla er fjárhagslega uppfærð. Það fer eftir kostnaðaraðferðinni, birgðalokun og leiðréttingarferlið gæti uppfært þennan reit.                            |

## <a name="inventory-status"></a>Birgðastaða

Hver birgðafærsla hefur stöðu sem birtist í annaðhvort **Kvittun** eða the **Mál** sviði. Reiturinn sem er notaður fer eftir gerð birgðafærslur. Kvittanir eru færslur sem auka birgðahaldið. Til dæmis, innkaupapöntun með jákvætt magn eða sölupöntun skilar með neikvætt magn. Útgáfur eru birgðafærslur sem minnkuðu birgðahaldið. Til dæmis, sölupöntun með jákvætt magn eða innkaupapöntun skilar með neikvætt magn.

### <a name="receipt-status"></a>Staða innhreyfingar

Eftirfarandi tafla lýsir **Kvittun** stöðu.

| **Staða innhreyfingar** | **Lýsing**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Raðað            | Upphafsstaða hvers kyns birgðafærslu sem táknar kvittun. Þetta felur í sér innkaupapantanir með jákvætt magn, framleiðslupantanir eða sölupöntunarskil með neikvætt magn.                                                   |
| Skráð         | Þessi staða er notuð þegar tveggja þrepa móttökuferli er til staðar eða þegar vörukoma er notuð til að gefa til kynna að vara sé komin. Það er notað þegar lotu- eða raðnúmerum er „úthlutað“ eða skráð á pöntunina. Fyrir frekari upplýsingar um komu vöru, farðu á [Yfirlit um komu](/supply-chain/inventory/arrival-overview.md). |
| Móttekið           | Þessi staða er notuð þegar færslan er líkamlega uppfærð. Fyrir innkaupapöntun er þetta þegar vörukvittun er bókuð. Fyrir skil á sölupöntun er þetta þegar fylgiseðillinn er bókaður.                                                                            |
| Keypt          | Þessi staða er notuð þegar færslan er fjárhagslega uppfærð. Fyrir innkaupapöntun eða skilapöntun sölupöntunar er þetta þegar reikningurinn er búinn til.                                                                                             |

### <a name="issue-status"></a>Staða úthreyfingar

Eftirfarandi tafla lýsir **Mál** stöðu.

| **Staða úthreyfingar**  | **Lýsing**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Í pöntun          | Upphafsstaða hvers kyns birgðafærslu sem táknar mál. Þetta felur í sér sölupantanir með jákvætt magn, framleiðslupantanir uppskrift eða formúlulínur, eða innkaupapantanir með neikvætt magn.                                             |
| Frátekið pantað  | Þessi birgðastaða gefur til kynna að birgðir séu fráteknar gegn pöntun sem hefur verið stofnuð, en ekki enn móttekin líkamlega í birgðum. Þegar birgðin er móttekin mun staðan sjálfkrafa uppfæra í **Frátekið líkamlegt**. Fyrir frekari upplýsingar um bókanir, farðu á [Varabirgðamagn](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Frátekið á lager | Þessi staða gefur til kynna að birgðum hafi verið úthlutað eða frátekið gegn tiltekinni pöntun. Þegar birgðir eru fráteknar eru þær ekki líkamlega tiltækar fyrir aðrar pantanir.                                 |
| Tekið til         | Þetta gefur til kynna að birgðin hafi verið tekin úr vöruhúsinu. Birgðin er enn líkamlega í vöruhúsinu, hefur ekki verið fjarlægð, en er ekki tiltæk fyrir aðrar pantanir.  |
| Frádregið          | Þessi staða er notuð þegar færslan er líkamlega uppfærð. Fyrir sölupöntun er þetta þegar fylgiseðillinn er bókaður; fyrir innkaupapöntun, þetta þegar vörukvittun er bókuð.                                                                      |
| Selt              | Þetta er staða sem notuð er þegar viðskiptin eru fjárhagslega uppfærð. Fyrir innkaupapöntun eða sölupöntun er þetta þegar reikningurinn er búinn til.|

Frekari upplýsingar um birgðafærslurnar er að finna á [Upplýsingar um birgðafærslur](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Stilltu birgðafærslusnið

Til að stilla birgðafærslusnið skaltu fylgja þessum skrefum:

1.  Opið **Vörustjórnun** > **Uppsetning** > **Birting** > **Birting**.
2.  Veldu flipann fyrir tegund viðskipta. Til dæmis, veldu **Pöntun**.
3.  Veldu valhnappinn fyrir færslugerðina. Til dæmis, veldu **Kaup útgjöld fyrir kostnað**.
4.  Veljið **Nýtt**.
5.  Í **Vörukóði** reit, veldu valkost fyrir **Tafla**, **·**, **·**, eða **Flokkur**. Til dæmis, til að stilla færslusnið fyrir tiltekinn vöruflokk, veldu **Hópur**.
     - Ef þú valdir **Tafla** í skrefi 5, veldu tiltekið vörunúmer fyrir færslusniðið í **Atriðatengsl** sviði.
     - Ef þú valdir **Hópur** í skrefi 5, veldu **Atriðahópur** fyrir færslusniðið í **Atriðatengsl** sviði.
     - Ef þú valdir **Allt** í skrefi 5, sem **Atriðatengsl** reiturinn verður auður.
     - Ef þú valdir **Flokkur** í skrefi 5, sem **Atriðatengsl** reiturinn verður auður. Nota **Flokkstengsl** reitinn til að velja flokkinn sem færslusniðið á við.

6.  Í **Reikningskóði** reit, veldu valkost fyrir **Tafla**, **·**, eða **Allt**. Til dæmis, til að nota bókunarsniðið á alla lánardrottna skaltu velja **Allt**.
     - Ef þú valdir **Tafla** í skrefi 5, veldu tiltekið númer lánardrottins fyrir bókunarsniðið í **Reikningstengsl** sviði.
     - Ef þú valdir **Hópur** í skrefi 5, veldu lánardrottnahópinn fyrir bókunarsniðið í **Reikningstengsl** sviði.
     - Ef þú valdir **Allt** í skrefi 5, sem **Reikningstengsl** reiturinn verður auður.

7.  Til að tengja tiltekinn skattflokk sem hefur valda bókunargerð skaltu velja a **Vöruskattshópur**. Ef þessi reitur er auður gildir bókunargerðin fyrir alla skattaflokka sem fyrir eru. Bókun sem er tilgreind fyrir skattflokka á aðeins við um sölu- og innkaupafærslur.
8.  Tilgreindu reikningsnúmerið til að bóka reikningsgerðina á **Aðalreikningur** sviði. Ef reikningsnúmer hefur ekki verið búið til til að nota sem bókhaldsgerð geturðu búið til nýjan reikning. Þú býrð til nýjan reikning í **Aðalreikningsupplýsingar** síðu í aðalbók.

## <a name="additional-resources"></a>Frekari upplýsingar

Hver flipi á **Birgðafærslusnið** síða tengist undirbók í Dynamics 365 Supply Chain Management. Fyrir frekari upplýsingar, farðu á:
-   [Bókun sölupöntunar](sales-order-posting.md)
-   [Bókun innkaupapöntunar](purchase-order-posting.md)
-   [Birgðabókun](inventory-posting.md)
-   [Framleiðslueftirlit](production-posting.md)
-   [Bókun staðlaðrar kostnaðarfráviks](standard-cost-variance-posting.md)
