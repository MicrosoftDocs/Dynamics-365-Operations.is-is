---
title: Villukóðar fyrir ástandsskoðun töfluvörpunar
description: Þessi grein lýsir villukóðum fyrir ástandsskoðun töfluvörpunar.
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: d3f413f34296fd01da6741bb49658285394cbd17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288761"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Villukóðar fyrir ástandsskoðun töfluvörpunar

[!include [banner](../../includes/banner.md)]



Þessi grein lýsir villukóðum fyrir ástandsskoðun töfluvörpunar.

## <a name="error-100"></a>Villa 100

Villuboðin eru: „Lágmarksútgáfa fjármála- og reksturs-verkvangs er PU 43 til að keyra fjármála- og reksturs-tillögur.“

Eiginleikinn krefst uppfærslu á verkvangi fyrir útgáfu 10.0.19 eða síðar af forrit fjármála- og rekstursum.

## <a name="error-400"></a>Villa 400

Villuboðin eru: „Engin skráningargögn fyrir viðskiptatilvik fundust fyrir eininguna \{fjármála- og reksturs UniqueEntityName\} sem þýðir að annaðhvort er vörpunin ekki keyrð eða allar reitarvarpanir eru einátta.“

## <a name="error-500"></a>Villa 500

Villuboðin eru: „Engar grunnstillingar verks fundust fyrir verk \{verkheit\}. Þetta gæti verið annaðhvort vegna þess að verkið er ekki virkjað eða að allar reitarvarpanir eru einátta úr þátttöku viðskiptavinar í fjármála- og reksturs.“

Athugaðu varpanir fyrir töfluvörpunina. Ef þær eru einátta úr forritum viðskiptavinar í fjármála- og reksturs-forrit myndast engin umferð fyrir samstillingu í rauntíma úr forritum fjármála- og reksturs í Dataverse.

## <a name="error-900"></a>Villa 900

Villuboðin eru: „Ógildur uppruni síu \{sourceFilter\} snið fyrir einingu \{fjármála- og reksturs UniqueEntityName\}.“

Upprunasían sem er tilgreind í töfluvörpuninni fyrir forrit fjármála- og reksturs er ekki setningafræðilega rétt. Til að staðfesta síuskilyrðið skal skoða [Úrræðaleita vandamál vegna samstillingr í rauntíma](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Villa 1000

Villuboðin eru: „Eining \{fjármála- og reksturs UniqueEntityName\} fyrirspurn notuð fyrir samstillingu í rauntíma tvöfaldrar skráningar er \{fjármála- og reksturs EntityFilterQueryString\}. Færslur sem uppfylla skilyrði fyrirspurnar verða með í samstillingu í rauntíma.“

Fyrirspurn einingar sem var skilað er öryggisafrit SQL-fyrirspurnar fyrir eininguna. Athugaðu innri samtengingar eða síur á fyrirspurninni sem ákvarða viðskiptagögnin sem verað notuð fyrir samstillingu í rauntíma. Innri samtengingar og síur eru áskilin skilyrði sem þarf að uppfylla fyrir hverja færslu sem notuð er fyrir samstillingu tvöfaldrar skráningar í rauntíma.

## <a name="error-1300"></a>Villa 1300

Villuboðin eru: „Sýndarreiti \{s.EntityFieldName\} fyrir einingu \{fjármála- og reksturs EntityMetadata.EntityProperties.LogicalEntityName\} er ekki hægt að rekja fyrir tvöfalda skráningu.“

Sýndarreitir úr fjármála- og reksturs-töflum eru ekki virkjaðir fyrir rakningu. Samstilling í rauntíma getur samstillt gögnin en getur ekki tekið með breytingarnar sem eru gerðar á dálkunum.

## <a name="error-1500"></a>Villa 1500

Villuboðin eru: „Það á að vera a.m.k. einum reit varpað á reit sem ekki er uppflettireitur í viðskiptavinaforriti til að virkja rakningu á gagnagjafanum \{datasource.DataSourceName\}.

Gagnagjafinn úr einingunni er ekki með neina reiti sem eru varpaðir fyrir tvöfalda skráningu. Breytingar á undirliggjandi töflu verða ekki raktar fyrir tvöfalda skráningu.

## <a name="error-1600"></a>Villa 1600

Villuboðin eru: „Gagnagjafi: \{datasource.DataSourceName\} fyrir einingu \{fjármála- og reksturs EntityMetadata.EntityProperties.LogicalEntityName\} er með svið. Aðeins færslur sem uppfylla skilyrði sviðsins eru notaðar fyrir útleiðina.“

Einingar í forriti fjármála- og reksturs geta verið með gagnagjafa þar sem síuskilyrði eru virkjuð. Þessi svið skilgreina færslurnar sem eru notaðar sem hluti af samstillingu í rauntíma. Ef sumum færslum er sleppt úr forrit fjármála- og reksturs í Dataverse skal athuga hvort færslurnar uppfylla skilyrði sviðsins í einingunni. Einföld leið til að gera þessa athugun er að keyra SQL-fyrirspurn sem líkist eftirfarandi dæmi.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Villa 1700

Villuboðin eru: „Tafla: \{datasourceTable.Key.subscribedTableName\} fyrir einingu \{datasourceTable.Key.entityName\} er rakin fyrir einingu \{origTableToEntityMaps.EntityName\}. Sömu töflur raktar fyrir margar einingar geta haft áhrif á kerfisafköst fyrir færslur í samstillingu í rauntíma.“

Ef sama taflan er rakin eftir mörgum einingum geta allar breytingar á töflunni ræst mat á tvöfaldri skráningu fyrir tengdar einingar. Þótt síuákvæðin muni aðeins senda gildar færslur gæti matið valið vandamálum með afköst ef til staðar eru fyrirspurnir seinlegar í keyrslu eða óstilltar áætlanir fyrirspurnar. Ekki er víst að hægt sé að koma í veg fyrir þetta vandamál frá sjónarhóli viðskipta. Ef hinsvegar eru margar töflur sem tengjast yfir margar einingar ætti hugsanlega að einfalda eininguna eða athuga fínstillingar fyrir fyrirspurnir um einingu.

## <a name="error-1800"></a>Villa 1800
Villuboðin eru: „Gagnagjafi: {} fyrir einingu CustCustomerV3Entity inniheldur sviðsgildi. Færsla á innleið sem er uppfærð og sett inn úr Dataverse í fjármála- og reksturs getur orðið fyrir áhrifum frá sviðsgildum í einingu. Prófaðu uppfærslur á færslum úr Dataverse í fjármála- og reksturs með færslum sem samsvara ekki síuskilyrðinu til að staðfesta stillingarnar.“

Ef svið er tiltekið í einingunni í forritum fjármála- og reksturs þá ætti að prófa samstillingu á innleið úr Dataverse í forrit fjármála- og reksturs í leit að uppfærsluhegðun á færslum sem samsvara ekki þessu sviðsskilyrði. Allar færslur sem samsvara ekki sviðinu verða meðhöndlaðar sem innsetningaraðgerð af hálfu einingarinnar. Innsetningin mun ekki takast ef fyrirliggjandi færsla er til í undirliggjandi töflu. Mælt er með að prófa þetta notkunartilfelli fyrir allar aðstæður áður en framleiðslan er sett upp.

## <a name="error-1900"></a>Villa 1900
Villuboðin eru: „Eining: er með {} gagnagjafa þar sem ekki er verið að rekja tvöföld skrif á útleið. Þetta getur haft áhrif á frammistöðu fyrirspurnar í beinni samstillingu. Endurgerðu líkanið í fjármála- og reksturs til að fjarlægja ónotaða gagnagjafa og töflur eða innleiddu getEntityRecordIdsImpactedByTableChange til að fínstilla keyrslufyrirspurnir.“

Ef margir gagnagjafar sem ekki er verið að nota fyrir rakningu í raunverulegri keyrslu samstillingar úr forritum fjármála- og reksturs, þá er möguleiki á að afkastageta einingar geti haft áhrif á keyrslu samstillingar. Til að fínstilla raktar töflur skal nota aðferðina getEntityRecordIdsImpactedByTableChange.

## <a name="error-5000"></a>Villa 5000
Villuboðin eru: „Samstilltar viðbætur eru skráðar fyrir tilvik gagnastjórnunar fyrir einingalykla. Þetta geta haft áhrif á upphafssamstillingu og beina innflutningssamstillingu í Dataverse. Til að ná sem bestu afköstum skal breyta viðbótunum í ósamstillta vinnslu. Listi yfir skráðar viðbætur {}.“

Samstilltar viðbætur á Dataverse einingu geta haft áhrif á keyrslu samstillingar og afköst fyrstu samstillingar því að hún bætist á flutningsálagið. Ráðlögð aðferð er annaðhvort að slökkva á viðbótunum eða gera þessar viðbætur ósamstilltar ef hleðslutíminn er hægur í upphaflegri samstillingu eða keyrslu samstillingar fyrir tiltekna einingu.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

