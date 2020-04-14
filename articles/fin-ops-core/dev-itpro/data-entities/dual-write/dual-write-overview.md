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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172785"
---
# <a name="dual-write-overview"></a>Yfirlit yfir tvöfalt skriftarverk

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a>Hvað er tvískipt skriftarverk?

Tvöföld skriftarverk er tilbúin grunngerð sem veitir nær rauntíma samskipti á milli líkanaknúninna forrita í Microsoft Dynamics 365 og Finance and Operations forrita. Þegar gögn um viðskiptavini, afurðir, fólk og rekstur streyma út fyrir forritamörk, verðar allar deildir fyrirtækis öflugri.

Tvöföld skriftarverk veitir þétt samtengingu, tvíátta samþættingu milli Finance and Operations forrita og Common Data Service. Allar gagnabreytingar í forritum Finance and Operations valda skrifum í Common Data Service og allar gagnabreytingar í Common Data Service valda skrifum í forrit Finance and Operations. Þetta sjálfvirka gagnaflæði veitir samþætta notendaupplifun í forritunum.

![Gagnasamband milli forrita](media/dual-write-overview.jpg)

Tvíritun hefur tvo þætti: *Innviðaþátt* og *forritsþátt*.

### <a name="infrastructure"></a>Grunnvirki

Innbyggingin með tvískiptum skrifum er teygjanleg og áreiðanleg og inniheldur eftirfarandi lykilatriði:

+ Samstillt og tvíátta gagnaflæði milli forrita
+ Samstilling, ásamt spilunar-, hlé- og tímaflakksstillingum til að styðja við kerfið í net- og ótengdum/ósamstilltum stillingum.
+ Geta til að samstilla upphafsgögn milli forritanna
+ Samþjöppuð sýn á verkþátta- og villuskrár fyrir gagnastjórnendur
+ Geta til að stilla sérsniðnar viðvaranir og viðmiðunarmörk og gerast áskrifandi að tilkynningum
+ Leiðandi notendaviðmót (UI) fyrir síun og umbreytingu
+ Geta til að stilla og skoða ósjálfstæði og sambönd eininga
+ Stækkanleiki fyrir bæði staðlaðar og sérsniðnar einingar og kort
+ Áreiðanleg stjórnun á líftíma forrits
+ Tilbúin uppsetningarupplifun viðskiptavina fyrir nýja viðskiptavini

### <a name="application"></a>Forrit

Tvöföld skriftarverk búa til vörpun á milli hugtaka í Finance and Operations forritum og hugtökum í líkanaknúnum forritum í Dynamics 365. Þessi samþætting styður eftirfarandi atburðarásir:

+ Samþættur aðalviðskiptavinur
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
+ Gögn frá viðskiptavinum, vörum, rekstri, verkefnum og net hlutanna (IoT) renna sjálfkrafa til Common Data Service í gegnum tvískipt skrif. Þessi tenging er mjög gagnleg fyrir fyrirtæki sem hafa áhuga á Microsoft Power Platform stækkanir.
+ Tvöfaldur-skrifa innviði fylgir meginreglunni um enga kóða/lágkóða. Lágmarks verkfræðiátak er krafist til að framlengja venjulegar varpanir frá töflu til töflu og fela í sér sérsniðnar varpanir.
+ Tvöföld skriftarverk styðja bæði netstillingu og ótengda stillingu. Microsoft er eina fyrirtækið sem býður upp á stuðning við net- og ótengdar stillingar.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>Hvað þýðir tvískipt skrif fyrir notendur og arkitekta CRM vörur?

Tvöfaldur skrifa sjálfvirkt gagnaflæðið á milli Finance and Operations forrita og Common Data Service. Í framtíðarútgáfum verða hugtök í líkanaknúnum forritum í Dynamics 365 (til dæmis viðskiptavini, tengiliður, tilvitnun og röð) stiguð til viðskiptavina á miðjum markaði og efri miðju markaðarins.

Í fyrstu útgáfunni er mest af sjálfvirkni meðhöndluð með tvískiptum lausnum. Í framtíðarútgáfum verða þessar lausnir hluti af Common Data Service. Með því að skilja væntanlegar breytingar á Common Data Service, þú getur sparað þér áreynslu til langs tíma. Hér eru sumar af mikilvægum breytingunum:

+ Common Data Service mun hafa ný hugtök, svo sem fyrirtæki og aðila. Þessi hugtök hafa áhrif á öll forrit sem eru byggð á Common Data Service, svo sem Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service.
+ Starfsemi og athugasemdir eru sameinaðar og stækkaðar til að styðja bæði C1 (notendur kerfisins) og C2 (viðskiptavini kerfisins).
+ Hér eru sumar af komandi breytingunum í Common Data Service:

    - Tugagagnagerð kemur í stað peningagagnagerðarinnar.
    - Dagvirkni mun styðja fyrri, nútíð og framtíðargögn á sama stað.
    - Það verður meiri stuðningur við gjaldmiðil og gengi og **Gengi** forritunarviðmót forrita (API) verður endurskoðað.
    - Stuðningur við umreiking eininga verður studdur.

Fyrir frekari upplýsingar um væntanlegar breytingar, sjá [Gögn í Common Data Service - áfangi 1 og 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).
