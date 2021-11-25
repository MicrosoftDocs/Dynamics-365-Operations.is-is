---
title: Villukóðar fyrir ástandsskoðun töfluvörpunar
description: Þetta efnisatriði lýsir villukóðum fyrir ástandsskoðun töfluvörpunar.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: c2d1f1e39a5ddccddf6fbbf524ff7eb0945b3c32
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782237"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Villukóðar fyrir ástandsskoðun töfluvörpunar

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þetta efnisatriði lýsir villukóðum fyrir ástandsskoðun töfluvörpunar.

## <a name="error-100"></a>Villa 100

Villuboðin eru: „Lágmarksútgáfa Finance and Operations verkvangs er PU 43 til að keyra Finance and Operations tillögur.“

Eiginleikinn krefst uppfærslu á verkvangi fyrir útgáfu 10.0.19 eða síðar af Finance and Operations forritum.

## <a name="error-400"></a>Villa 400

Villuboðin eru: „Engin skráningargögn fyrir viðskiptatilvik fundust fyrir eininguna \{Finance and Operations UniqueEntityName\} sem þýðir að annaðhvort er vörpunin ekki keyrð eða allar reitarvarpanir eru einátta.“

## <a name="error-500"></a>Villa 500

Villuboðin eru: „Engar grunnstillingar verks fundust fyrir verk \{ verkheit\}. Þetta gæti verið annaðhvort vegna þess að verkið er ekki virkjað eða að allar reitarvarpanir eru einátta úr þátttöku viðskiptavinar í Finance and Operations.“

Athugaðu varpanir fyrir töfluvörpunina. Ef þær eru einátta úr forritum viðskiptavinar í Finance and Operations forrit myndast engin umferð fyrir samstillingu í rauntíma úr Finance and Operations forritum í Dataverse.

## <a name="error-900"></a>Villa 900

Villuboðin eru: „Ógildur uppruni síu \{ sourceFilter\} snið fyrir einingu \{Finance and Operations UniqueEntityName\}.“

Upprunasían sem er tilgreind í töfluvörpuninni fyrir Finance and Operations forrit er ekki setningafræðilega rétt. Til að staðfesta síuskilyrðið skal skoða [Úrræðaleita vandamál vegna samstillingr í rauntíma](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Villa 1000

Villuboðin eru: „Eining \{Finance and Operations UniqueEntityName\} fyrirspurn notuð fyrir samstillingu í rauntíma tvöfaldrar skráningar er \{Finance and Operations EntityFilterQueryString\}. Færslur sem uppfylla skilyrði fyrirspurnar verða með í samstillingu í rauntíma.“

Fyrirspurn einingar sem var skilað er öryggisafrit SQL-fyrirspurnar fyrir eininguna. Athugaðu innri samtengingar eða síur á fyrirspurninni sem ákvarða viðskiptagögnin sem verað notuð fyrir samstillingu í rauntíma. Innri samtengingar og síur eru áskilin skilyrði sem þarf að uppfylla fyrir hverja færslu sem notuð er fyrir samstillingu tvöfaldrar skráningar í rauntíma.

## <a name="error-1300"></a>Villa 1300

Villuboðin eru: „Sýndarreiti \{ s.EntityFieldName\} fyrir einingu \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} er ekki hægt að rekja fyrir tvöfalda skráningu.“

Sýndarreitir úr Finance and Operations töflum eru ekki virkjaðir fyrir rakningu. Samstilling í rauntíma getur samstillt gögnin en getur ekki tekið með breytingarnar sem eru gerðar á dálkunum.

## <a name="error-1500"></a>Villa 1500

Villuboðin eru: „Það á að vera a.m.k. einum reit varpað á reit sem ekki er uppflettireitur í viðskiptavinaforriti til að virkja rakningu á gagnagjafanum \{ datasource.DataSourceName\}.

Gagnagjafinn úr einingunni er ekki með neina reiti sem eru varpaðir fyrir tvöfalda skráningu. Breytingar á undirliggjandi töflu verða ekki raktar fyrir tvöfalda skráningu.

## <a name="error-1600"></a>Villa 1600

Villuboðin eru: „Gagnagjafi: \{ datasource.DataSourceName\} fyrir einingu \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} er með svið. Aðeins færslur sem uppfylla skilyrði sviðsins eru notaðar fyrir útleiðina.“

Einingar í Finance and Operations forritum geta verið með gagnagjafa þar sem síuskilyrði eru virkjuð. Þessi svið skilgreina færslurnar sem eru notaðar sem hluti af samstillingu í rauntíma. Ef sumum færslum er sleppt úr Finance and Operations forritum í Dataverse skal athuga hvort færslurnar uppfylla skilyrði sviðsins í einingunni. Einföld leið til að gera þessa athugun er að keyra SQL-fyrirspurn sem líkist eftirfarandi dæmi.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Villa 1700

Villuboðin eru: „Tafla: \{ datasourceTable.Key.subscribedTableName\} fyrir einingu \{ datasourceTable.Key.entityName\} er rakin fyrir einingu \{ origTableToEntityMaps.EntityName\}. Sömu töflur raktar fyrir margar einingar geta haft áhrif á kerfisafköst fyrir færslur í samstillingu í rauntíma.“

Ef sama taflan er rakin eftir mörgum einingum geta allar breytingar á töflunni ræst mat á tvöfaldri skráningu fyrir tengdar einingar. Þótt síuákvæðin muni aðeins senda gildar færslur gæti matið valið vandamálum með afköst ef til staðar eru fyrirspurnir seinlegar í keyrslu eða óstilltar áætlanir fyrirspurnar. Ekki er víst að hægt sé að koma í veg fyrir þetta vandamál frá sjónarhóli viðskipta. Ef hinsvegar eru margar töflur sem tengjast yfir margar einingar ætti hugsanlega að einfalda eininguna eða athuga fínstillingar fyrir fyrirspurnir um einingu.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
