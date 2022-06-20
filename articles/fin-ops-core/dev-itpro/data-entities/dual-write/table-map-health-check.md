---
title: Villukóðar fyrir ástandsskoðun töfluvörpunar
description: Þessi grein lýsir villukóðum fyrir heilsuathugun töflukortsins.
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 3ae78077fc716311c38620b14665af3983a44c2d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884084"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Villukóðar fyrir ástandsskoðun töfluvörpunar

[!include [banner](../../includes/banner.md)]



Þessi grein lýsir villukóðum fyrir heilsuathugun töflukortsins.

## <a name="error-100"></a>Villa 100

Villuboðin eru: "Lágmarksútgáfa fjármála- og rekstrarvettvangs sem krafist er er PU 43 til að keyra ráðleggingar um fjármál og rekstrar."

Eiginleikinn krefst uppfærslu á vettvangi fyrir útgáfu 10.0.19 eða nýrri af Finance and Operations forritum.

## <a name="error-400"></a>Villa 400

Villuboðin eru: „Engin skráningargögn fyrirtækjaviðburða fundust fyrir eininguna\{ Fjármál og rekstur UniqueEntityName\} sem þýðir að annað hvort er kortið ekki í gangi eða öll sviðskortlagningin er einstefnu.“

## <a name="error-500"></a>Villa 500

Villuboðin eru: „Engar grunnstillingar verks fundust fyrir verk \{verkheit\}. Þetta gæti annaðhvort verið að verkefnið sé ekki virkt eða að öll sviðskortin séu einstefnu frá þátttöku viðskiptavina til fjármála og rekstrar.“

Athugaðu varpanir fyrir töfluvörpunina. Ef þau eru einátta frá þátttökuforritum viðskiptavina yfir í Finance and Operations forrit myndast engin umferð fyrir samstillingu í beinni frá Finance and Operations forritum til Dataverse.

## <a name="error-900"></a>Villa 900

Villuboðin eru „Ógild upprunasía\{ sourceFilter\} snið fyrir einingu\{ Fjármál og rekstur UniqueEntityName\} ."

Upprunasían sem er tilgreind á töflukortinu fyrir Finance and Operations forrit er ekki setningafræðilega rétt. Til að staðfesta síuskilyrðið skal skoða [Úrræðaleita vandamál vegna samstillingr í rauntíma](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Villa 1000

Villuskilaboðin eru „Atli\{ Fjármál og rekstur UniqueEntityName\} fyrirspurn sem notuð er fyrir tvíritun í beinni samstillingu er\{ Finance and Operations EntityFilterQueryString \}. Færslur sem uppfylla skilyrði fyrirspurnar verða með í samstillingu í rauntíma.“

Fyrirspurn einingar sem var skilað er öryggisafrit SQL-fyrirspurnar fyrir eininguna. Athugaðu innri samtengingar eða síur á fyrirspurninni sem ákvarða viðskiptagögnin sem verað notuð fyrir samstillingu í rauntíma. Innri samtengingar og síur eru áskilin skilyrði sem þarf að uppfylla fyrir hverja færslu sem notuð er fyrir samstillingu tvöfaldrar skráningar í rauntíma.

## <a name="error-1300"></a>Villa 1300

Villuskilaboðin eru „Sýndarreitir\{ s.EntityFieldName\} fyrir aðila\{ Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} má ekki rekja fyrir tvískrift."

Sýndarreitir úr Finance and Operations töflum eru ekki virkjaðir fyrir rakningu. Samstilling í rauntíma getur samstillt gögnin en getur ekki tekið með breytingarnar sem eru gerðar á dálkunum.

## <a name="error-1500"></a>Villa 1500

Villuboðin eru: „Það á að vera a.m.k. einum reit varpað á reit sem ekki er uppflettireitur í viðskiptavinaforriti til að virkja rakningu á gagnagjafanum \{datasource.DataSourceName\}.

Gagnagjafinn úr einingunni er ekki með neina reiti sem eru varpaðir fyrir tvöfalda skráningu. Breytingar á undirliggjandi töflu verða ekki raktar fyrir tvöfalda skráningu.

## <a name="error-1600"></a>Villa 1600

Villuboðin eru: "Gagnaheimild:\{ datasource.DataSourceName\} fyrir aðila\{ Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} er með svið. Aðeins færslur sem uppfylla skilyrði sviðsins eru notaðar fyrir útleiðina.“

Aðilar í Finance and Operations forritum geta haft gagnagjafa þar sem síusvið eru virkjuð. Þessi svið skilgreina færslurnar sem eru notaðar sem hluti af samstillingu í rauntíma. Ef einhverjum skrám er sleppt úr Finance and Operations forritum til Dataverse, athugaðu hvort færslurnar uppfylli sviðsviðmiðin fyrir eininguna. Einföld leið til að gera þessa athugun er að keyra SQL-fyrirspurn sem líkist eftirfarandi dæmi.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Villa 1700

Villuboðin eru: „Tafla: \{datasourceTable.Key.subscribedTableName\} fyrir einingu \{datasourceTable.Key.entityName\} er rakin fyrir einingu \{origTableToEntityMaps.EntityName\}. Sömu töflur raktar fyrir margar einingar geta haft áhrif á kerfisafköst fyrir færslur í samstillingu í rauntíma.“

Ef sama taflan er rakin eftir mörgum einingum geta allar breytingar á töflunni ræst mat á tvöfaldri skráningu fyrir tengdar einingar. Þótt síuákvæðin muni aðeins senda gildar færslur gæti matið valið vandamálum með afköst ef til staðar eru fyrirspurnir seinlegar í keyrslu eða óstilltar áætlanir fyrirspurnar. Ekki er víst að hægt sé að koma í veg fyrir þetta vandamál frá sjónarhóli viðskipta. Ef hinsvegar eru margar töflur sem tengjast yfir margar einingar ætti hugsanlega að einfalda eininguna eða athuga fínstillingar fyrir fyrirspurnir um einingu.

## <a name="error-1800"></a>Villa 1800
Villuboðin eru: "Gagnaheimild:{} fyrir einingu CustCustomerV3Entity inniheldur sviðsgildi. Skrá á heimleið upserts frá Dataverse to Finance and Operations geta orðið fyrir áhrifum af sviðsgildum á einingu. Vinsamlega prófaðu skráaruppfærslur frá Dataverse til Finance and Operations með skrár sem passa ekki við síuskilyrðin til að sannreyna stillingarnar þínar."

Ef það er svið tilgreint á einingunni í fjármála- og rekstrarforritum, þá er samstilling á heimleið frá Dataverse til að fjármagna og rekstrarforrit ættu að vera prófuð með tilliti til uppfærsluhegðunar á skrám sem passa ekki við þetta sviðsviðmið. Sérhver skrá sem passar ekki við svið verður meðhöndluð sem innsetningaraðgerð af einingunni. Ef það er fyrirliggjandi skrá í undirliggjandi töflu, þá mun innsetningin mistakast. Við mælum með því að þú prófir þetta notkunartilvik fyrir allar aðstæður áður en þú ferð í framleiðslu.

## <a name="error-1900"></a>Villa 1900
Villuskilaboðin eru: „Entity: has{} gagnagjafar sem ekki er rakið fyrir tvískrifað á útleið. Þetta getur haft áhrif á árangur samstillingarfyrirspurna í beinni. Endurgerðu eininguna í Finance and Operations til að fjarlægja ónotaða gagnagjafa og töflur eða innleiða getEntityRecordIdsImpactedByTableChange til að fínstilla keyrslufyrirspurnirnar."

Ef það eru margir gagnagjafar sem eru ekki notaðir til að rekja í raunverulegri samstillingu í beinni frá fjármála- og rekstrarforritum, þá er möguleiki á að frammistaða einingarinnar geti haft áhrif á samstillingu í beinni. Til að fínstilla raktar töflur, notaðu aðferðina getEntityRecordIdsImpactedByTableChange.

## <a name="error-5000"></a>Villa 5000
Villuboðin eru: „Samstillar viðbætur eru skráðar fyrir gagnastjórnunarviðburði fyrir einingareikninga. Þetta getur haft áhrif á upphaflega samstillingu og árangur samstillingar í beinni Dataverse. Til að ná sem bestum árangri, vinsamlegast breyttu viðbótunum í ósamstillta vinnslu. Listi yfir skráð viðbætur{} ."

Samstilltar viðbætur á a Dataverse eining getur haft áhrif á samstillingu í beinni og fyrstu samstillingarafköstum þar sem það eykur álag á færslur. Mælt er með því að slökkva á viðbæturnar eða gera þessar viðbætur ósamstilltar ef þú stendur frammi fyrir hægum hleðslutíma í fyrstu samstillingu eða samstillingu í beinni fyrir tiltekna aðila.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
