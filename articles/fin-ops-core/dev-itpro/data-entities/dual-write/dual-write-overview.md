---
title: Yfirlit yfir tvöfalt skriftarverk
description: Þetta efni veitir yfirlit tvöföld skriftarverk. Tvöföld skriftarverk er grunngerð sem veitir nær rauntíma samskipti á milli Microsoft Dynamics 365 líkanaknúinna forrita og Finance and Operations forrita.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 85530cf644c7b7ffe922a6fb3288f4e05c5df91c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685614"
---
# <a name="dual-write-overview"></a>Yfirlit yfir tvöfalt skriftarverk

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a>Hvað er tvískipt skriftarverk?

Tvöföld skrif er tilbúið tölvukerfi sem býður upp á samskipti í rauntíma á milli forrita viðskiptavina og Finance and Operations-forrita. Þegar gögn um viðskiptavini, afurðir, fólk og rekstur streyma út fyrir forritamörk, verðar allar deildir fyrirtækis öflugri.

Tvöföld skriftarverk veitir þétt samtengingu, tvíátta samþættingu milli Finance and Operations forrita og Dataverse. Allar gagnabreytingar í forritum Finance and Operations valda skrifum í Dataverse og allar gagnabreytingar í Dataverse valda skrifum í forrit Finance and Operations. Þetta sjálfvirka gagnaflæði veitir samþætta notendaupplifun í forritunum.

![Gagnasamband milli forrita](media/dual-write-overview.jpg)

Tvíritun hefur tvo þætti: *Innviðaþátt* og *forritsþátt*.

### <a name="infrastructure"></a>Grunnvirki

Innbyggingin með tvískiptum skrifum er teygjanleg og áreiðanleg og inniheldur eftirfarandi lykilatriði:

+ Samstillt og tvíátta gagnaflæði milli forrita
+ Samstilling, ásamt spilunar-, hlé- og tímaflakksstillingum til að styðja við kerfið í net- og ótengdum/ósamstilltum stillingum.
+ Geta til að samstilla upphafsgögn milli forritanna
+ Samsett yfirlit yfir verkþætti og villukladda fyrir gangastjórnendur
+ Geta til að stilla sérsniðnar viðvaranir og viðmiðunarmörk og gerast áskrifandi að tilkynningum
+ Leiðandi notendaviðmót (UI) fyrir síun og umbreytingu
+ Geta til að stilla og skoða ósjálfstæði og sambönd eininga
+ Stækkunarhæfni fyrir bæði staðlaðar og sérsniðnar töflur og kort
+ Áreiðanleg stjórnun á líftíma forrits
+ Tilbúin uppsetningarupplifun viðskiptavina fyrir nýja viðskiptavini

### <a name="application"></a>Forrit

Tvöföld skrif stofnar vörpun milli hugtaka í Finance and Operations-forritum og hugataka í forritum viðskiptavina. Þessi samþætting styður eftirfarandi atburðarásir:

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
+ Stjórnun á einum stað fyrir notendur
+ Innbyggðar rásir fyrir smásölu og markaðssetningu
+ Sýnileiki í kynningum og afslætti
+ Biðja um þjónustu aðgerðir
+ Staumlínulagaðar þjónustuaðgerðir

## <a name="top-reasons-to-use-dual-write"></a>Helstu ástæður til að nota tvískipt skrif

Tvöföld skrifa veitir samþættingu gagna í öllu forritum Microsoft Dynamics 365. Þessi öflugi rammi tengir umhverfi og gerir ólíkum viðskiptaforritum kleift að vinna saman. Hér eru helstu ástæður þess að þú ættir að nota tvískipt skrif:

+ Tvöföld skrifa veitir þétt samtengd, næstum rauntíma og tvíátta samþættingu milli forrita Finance and Operations og líkanadrifinna forrita í Dynamics 365. Þessi samþætting gerir Microsoft Dynamics 365 að því eina sem þarf fyrir allar viðskiptalausnir þínar. Viðskiptavinir sem nota Dynamics 365 Finance og Dynamics 365 Supply Chain Management, en sem nota lausnir utan Microsoft fyrir stjórnun tengsla við viðskiptavini (CRM), fara í átt að Dynamics 365 fyrir tvískiptan stuðning.
+ Gögn frá viðskiptavinum, vörum, rekstri, verkefnum og net hlutanna (IoT) renna sjálfkrafa til Dataverse í gegnum tvískipt skrif. Þessi tenging er gagnleg fyrir fyrirtæki sem hafa áhuga á Power Platform útvíkkun.
+ Tvöfaldur-skrifa innviði fylgir meginreglunni um enga kóða/lágkóða. Lágmarks verkfræðiátak er krafist til að framlengja venjulegar varpanir frá töflu til töflu og fela í sér sérsniðnar varpanir.
+ Tvöföld skriftarverk styðja bæði netstillingu og ótengda stillingu. Microsoft er eina fyrirtækið sem býður upp á stuðning við net- og ótengdar stillingar.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Hvað þýða tvöföld skrif fyrir þróunaraðila og hönnuði forrita viðskiptavina?

Tvöföld skrif gerir gagnaflæði á milli Finance and Operations forrita og forrit fyrir viðskiptavini sjálfvirk. Tvöföld skrif samanstendur af tveimur AppSource lausnum sem eru settar upp á Dataverse. Lausnirnar víkka út einingarskema, viðbætur og verkflæði á Dataverse þannig að hægt sé að kvarða þær fyrir ERP-stærð. Fyrir árangursríka innleiðingu verða þróunaraðilar og hönnuðir forrita viðskiptavina að hafa skilning á þessum breytingum og vinna með viðkomandi í Finance and Operations-forritum.

Ef búa á til samstæðu með Finance and Operations-forritum gera tvöföld skrif nauðsynlegar breytingar í Dataverse-skemanu. Ef ætlunin er að skilja áætlunina er hægt að koma í veg fyrir endurvinnslu tiltekinnar hönnunr og þróunar í framtíðinni.

+ Þegar AppSource pakkinn fyrir tvöföld skrif er uppsettur mun Dataverse innihald ný hugtök á borð við fyrirtæki og aðila. Þessi hugtök aðstoða forrit sem byggja á Dataverse, þar á meðal Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service, að eiga samskipti við Finance and Operations-forrit.

+ Starfsemi og athugasemdir eru sameinaðar og stækkaðar til að styðja bæði C1 (notendur kerfisins) og C2 (viðskiptavini kerfisins).

+ Til að koma í veg fyrir gagnatap við flutning á milli Finance and Operations-forrita og Dataverse, er hægt að útvíkka fjölda aukastafa í gagnagerð gjaldmiðils fyrir forrit viðskiptavina. Eiginleikinn þýðir sjálfkrafa fyrirliggjandi línur í nýja útvíkkaða stöðu á lýsigagnalagi. Í þessu ferli er gjaldmiðilsgildið þýtt með tugagögnum, frekar en peningagögnum, og gjaldmiðilsgildið styður 10 aukastafi. Velja þarf þennan eiginleiki er innskráður og fyrirtæki sem þurfa ekki meira en 4 aukastafi þurfa ekki að velja hann. Nánari upplýsingar er að finna í [Flutningur gagnagerðar gjaldmiðils fyrir tvöföld skrif](currrency-decimal-places.md).

+ [Dagsetningarvirkni](../../dev-tools/date-effectivity.md) verður bætt við Dataverse. Það styður gögn í fortíð, nútíð og framtíð í sömu einingu.

+ [Umreikningur eininga](../../../../supply-chain/pim/tasks/manage-unit-measure.md) er studdur fyrir vörur, tilboð, pantanir og reikninga.

Frekari upplýsingar um breytingar á næstunni er að finna í [Nýjungar eða breytingar í tvöföldum skrifum](whats-new-dual-write.md).

