---
title: Tvöföld skrif – yfirlit
description: Þessi grein veitir yfirlit yfir tvískrift, sem veitir nánast rauntíma samskipti milli forrita fyrir þátttöku viðskiptavina og fjármála- og rekstrarappa.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2ef4fb1a51bd92db440841eb2a9d9ebcce0e1b1d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872941"
---
# <a name="dual-write-overview"></a>Tvöföld skrif – yfirlit

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Hvað er tvískipt skriftarverk?

Dual-write er út-af-kassa innviði sem veitir næstum rauntíma samskipti milli þátttökuforrita viðskiptavina og fjármála- og rekstrarappa. Þegar gögn um viðskiptavini, afurðir, fólk og rekstur streyma út fyrir forritamörk, verðar allar deildir fyrirtækis öflugri.

Dual-write veitir þétttengda, tvíátta samþættingu milli Finance and Operations forrita og Dataverse. Allar gagnabreytingar í Finance and Operations forritum valda skrifum til Dataverse, og allar breytingar á gögnum Dataverse veldur skrifum í Finance and Operations öpp. Þetta sjálfvirka gagnaflæði veitir samþætta notendaupplifun í forritunum.

![Gagnasamband milli forrita.](media/dual-write-overview.jpg)

Tvíritun hefur tvo þætti: *Innviðaþátt* og *forritsþátt*.

### <a name="infrastructure"></a>Grunnvirki

Innbyggingin með tvískiptum skrifum er teygjanleg og áreiðanleg og inniheldur eftirfarandi lykilatriði:

+ Samstillt og tvíátta gagnaflæði milli forrita
+ Samstilling, ásamt spilunar-, hlé- og tímaflakksstillingum til að styðja við kerfið í net- og ótengdum/ósamstilltum stillingum.
+ Geta til að samstilla upphafsgögn milli forritanna
+ Samsett yfirlit yfir verkþætti og villukladda fyrir gangastjórnendur
+ Geta til að stilla sérsniðnar viðvaranir og viðmiðunarmörk og gerast áskrifandi að tilkynningum
+ Leiðandi notendaviðmót (UI) fyrir síun og umbreytingu
+ Geta til að stilla og skoða töflutengsl og sambönd
+ Stækkunarhæfni fyrir bæði staðlaðar og sérsniðnar töflur og kort
+ Áreiðanleg stjórnun á líftíma forrits
+ Tilbúin uppsetningarupplifun viðskiptavina fyrir nýja viðskiptavini

### <a name="application"></a>Forrit

Dual-write skapar kortlagningu á milli hugtaka í Finance and Operations öppum og hugtaka í öppum fyrir þátttöku viðskiptavina. Þessi samþætting styður eftirfarandi atburðarásir:

+ Samþætt aðalsniðmát viðskiptavinar
+ Aðgangur að vildarkortum viðskiptavina og verðlaunapunkta
+ Samræmd afurðarsniðmátaupplifun
+ Meðvitund um stigveldi fyrirtækis
+ Samþætt lánardrottinssniðmát
+ Aðgangur að fjárhags- og skattatilvísunargögnum
+ Reynsla verðvélar eftir þörfum
+ Samþætt reynsla viðfangs til sjóðstreymis
+ Geta til að þjóna bæði eigin eignum og eignum viðskiptavina í gegnum umboðsmenn svæðisins
+ Samþætt reynsla af öflun til að greiða
+ Innbyggt athæfi og athugasemdir fyrir gögn viðskiptavina og skjöl
+ Geta til að leita að tiltækum birgðum og smáatriðum
+ Verk til reiðfjár-upplifun
+ Geta til að takast á við mörg heimilisföng og hlutverk í gegnum aðilahugtakið


## <a name="top-reasons-to-use-dual-write"></a>Helstu ástæður til að nota tvískipt skrif

Tvöföld skrifa veitir samþættingu gagna í öllu forritum Microsoft Dynamics 365. Þessi öflugi rammi tengir umhverfi og gerir ólíkum viðskiptaforritum kleift að vinna saman. Hér eru helstu ástæður þess að þú ættir að nota tvískipt skrif:

+ Tvöföld skráning veitir vel tengda, næstum í rauntíma og tvíátta samþættingu milli fjármála- og rekstrarforrita og forrita viðskiptavinar. Þessi samþætting gerir Microsoft Dynamics 365 að því eina sem þarf fyrir allar viðskiptalausnir þínar. Viðskiptavinir sem nota Dynamics 365 Finance og Dynamics 365 Supply Chain Management, en þeir sem nota ekki Microsoft lausnir fyrir stjórnun viðskiptavinatengsla (CRM), eru að fara í átt að Dynamics 365 fyrir tvískrifaðan stuðning.
+ Gögn frá viðskiptavinum, vörum, rekstri, verkefnum og net hlutanna (IoT) renna sjálfkrafa til Dataverse í gegnum tvískipt skrif. Þessi tenging er gagnleg fyrir fyrirtæki sem hafa áhuga á Power Platform útvíkkun.
+ Tvöfaldur-skrifa innviði fylgir meginreglunni um enga kóða/lágkóða. Lágmarks verkfræðiátak er krafist til að framlengja venjulegar varpanir frá töflu til töflu og fela í sér sérsniðnar varpanir.
+ Tvöföld skriftarverk styðja bæði netstillingu og ótengda stillingu. Microsoft er eina fyrirtækið sem býður upp á stuðning við net- og ótengdar stillingar.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Hvað þýða tvöföld skrif fyrir þróunaraðila og hönnuði forrita viðskiptavina?

Dual-write gerir sjálfvirkan gagnaflæði á milli Finance and Operations forrita og þátttökuforrita viðskiptavina. Tvöföld skrif samanstendur af tveimur AppSource lausnum sem eru settar upp á Dataverse. Lausnirnar víkka út töfluskema, viðbætur og verkflæði á Dataverse þannig að hægt sé að kvarða þær fyrir ERP-stærð. Til að innleiðingin takist vel verða þróunaraðilar og arkitektar forrita fyrir þátttöku viðskiptavina að skilja þessar breytingar og vinna með hliðstæðum sínum um fjármála- og rekstraröpp.

Til að skapa jafnræði með Finance and Operations forritum gerir tvískrift nokkrar mikilvægar breytingar á Dataverse skema. Ef ætlunin er að skilja áætlunina er hægt að koma í veg fyrir endurvinnslu tiltekinnar hönnunr og þróunar í framtíðinni.

+ Þegar AppSource pakkinn fyrir tvöföld skrif er uppsettur mun Dataverse innihald ný hugtök á borð við fyrirtæki og aðila. Þessi hugtök hjálpa forritum sem eru byggð á Dataverse, þar á meðal Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service, til að eiga óaðfinnanlega samskipti við Finance and Operations öpp.

+ Starfsemi og athugasemdir eru sameinaðar og stækkaðar til að styðja bæði C1 (notendur kerfisins) og C2 (viðskiptavini kerfisins).

+ Til að koma í veg fyrir gagnatap við gjaldeyrisflutning milli Finance and Operations forrita og Dataverse, muntu geta lengt fjölda aukastafa í gjaldmiðilsgagnagerð viðskiptaforrita fyrir þátttöku. Eiginleikinn þýðir sjálfkrafa fyrirliggjandi línur í nýja útvíkkaða stöðu á lýsigagnalagi. Í þessu ferli er gjaldmiðilsgildið þýtt með tugagögnum, frekar en peningagögnum, og gjaldmiðilsgildið styður 10 aukastafi. Velja þarf þennan eiginleiki er innskráður og fyrirtæki sem þurfa ekki meira en 4 aukastafi þurfa ekki að velja hann. Nánari upplýsingar er að finna í [Flutningur gagnagerðar gjaldmiðils fyrir tvöföld skrif](currrency-decimal-places.md).

+ [Dagsetningarvirkni](../../dev-tools/date-effectivity.md) verður bætt við Dataverse. Það styður gögn í fortíð, nútíð og framtíð í sömu töflu.

+ [Umreikningur eininga](../../../../supply-chain/pim/tasks/manage-unit-measure.md) er studdur fyrir vörur, tilboð, pantanir og reikninga.

Frekari upplýsingar um breytingar á næstunni er að finna í [Nýjungar eða breytingar í tvöföldum skrifum](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
