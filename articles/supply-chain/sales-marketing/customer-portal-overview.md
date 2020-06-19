---
title: Viðskiptavinagátt fyrir Dynamics 365 Supply Chain Management-yfirlit
description: Þetta efnisatriði fjallar um viðskiptavinagáttina og útskýrir hver ætti að nota hana og hvernig hún virkar.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6b57365d8042c1d791ee2c50c5458a6595a58270
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413973"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Viðskiptavinagátt fyrir Dynamics 365 Supply Chain Management-yfirlit

## <a name="what-is-the-customer-portal"></a>Hvað er viðskiptavinagátt?

Í dag treysta aðfangakeðjukerfi á samþættingu. Þau þarfnast þess að birgðir, eftirspurn viðskiptavinar og söludeildir verði samþættar í stað þess að vera hver í sínu horni. Viðskiptavinagáttin hjálpar fyrirtækjum sem keyra Microsoft Dynamics 365 Supply Chain Management að auka þessa samþættingu og, það sem meira er, að halda viðskiptavinunum upplýstum.

Viðskiptavinagáttin er sniðmát [Power Apps-gáttar](https://docs.microsoft.com/powerapps/maker/portals/overview) sem gerir fyrirtækjum kleift að búa til vefsvæði sem gengur út á viðskipta milli fyrirtækja (B2B) fyrir aðstæður sem tengjast sölupöntunarferlum. Sniðmátið notar [tvíritun](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), Supply Chain Management og gáttir Power Apps til að gera utanaðkomandi fyrirtækjum kleift að skoða og búa til gögn úr Dynamics 365-umhverfi fyrirtækisins.

Sniðmát viðskiptavinagáttar er með alla sérstillingarmöguleika sem gáttir Power Apps bjóða upp á. Auðveldlega er hægt að breyta sniðmátinu til að halda vörumerki fyrirtækisins á lofti, bæta við aukinni virkni og breyta notandaupplifuninni. Hægt er að breyta allri virkni sem tilbúna sniðmátið býður upp á.

> [!IMPORTANT]
> Ekki er gert ráð fyrir að sniðmátið virki að fullu eitt og sér. Það þjónar bara sem hvati fyrir viðskiptavini sem vilja búa til almennt vefsvæði svo að fyrirtækin í viðskiptum geti nálgast gögnin í Supply Chain Management.

> [!NOTE]
> Fylgiskjölum viðskiptavinagáttar er beint að stjórnendum, hönnuðum og þróunaraðilum kerfis sem setja upp viðskiptavinagáttina fyrir uppsetningu Supply Chain Management. Það notar hugtökin _viðskiptavinur_ og _notandi_ til að lýsa einstaklingum sem eru viðskiptavinir fyrirtækisins sem keyrir Supply Chain Management, og sem nota sjálfa lokagáttina.

## <a name="who-should-use-it"></a>Hver ætti að nota hana?

Viðskiptavinagáttin er hönnuð fyrir fyrirtæki sem keyra Supply Chain Management og eru af þessum toga:

- Þau vilja byggja upp vefsvæði út á við sem miðlar upplýsingum um vinnslu pantana (svo sem pöntunarstöðu eða reikningsupplýsingar) beint úr Supply Chain Management-kerfinu þeirra til fyrirtækja sem þau eru í viðskiptum við.
- Þau eru að færa sig úr Dynamics AX 2012 í Supply Chain Management og notuðu áður [AX 2012 Sjálfsafgreiðslugátt viðskiptavina](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Eftirfarandi gerðir fyrirtækja eru **ekki** góðir kandídatar fyrir innleiðingu viðskiptavinagáttar:

- Fyrirtæki sem vilja setja upp vefsvæði fyrir viðskiptavini sem ekki eru fyrirtæki. Þessi fyrirtæki ættu að íhuga að búa til [Dynamics 365 Commerce vefsvæði rafrænna viðskipta](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site).
- Fyrirtæki sem eru þegar að nota fyrirliggjandi vefsvæði Power Apps-gáttar í svipuðum tilgangi. Þessi fyrirtæki fá ekki frekari fríðindi frá viðskiptavinagáttinni. Viðskiptavinagáttin er afhend sem sniðmát sem virkar eins og leiðarvísir og upphafspunktur fyrir viðskiptavini sem vilja „tengja saman punktana“ milli tvíritunar, Supply Chain Management og Power Apps-gátta. Ef þegar er búið að setja upp vefsvæði sem þjónar þessum tilgangi er ekki víst að neinn ávinningur fylgi því að nota sniðmát viðskiptavinagáttar til að endurúthluta þessu vefsvæði.

## <a name="how-does-it-work"></a>Hvernig virkar það?

Viðskiptavinargátt er gefin upp sem Power Apps gáttasniðmát. Það fer eftir Power Apps-gáttum og tvíritun.

[Power Apps gáttir](https://docs.microsoft.com/powerapps/maker/portals/overview) er eiginleiki sem gerir notendum kleift að búa til vefsvæði fyrir almenning sem fólk utan fyrirtækisins geta skráð sig inn á. Lítil eða engin kóðun er nauðsynleg til að búa til gáttir. Viðskiptavinagáttin er eitt margra [sniðmáta Dynamics 365-gáttar](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) sem eru í boði hjá Microsoft.

[Tvöföld skrif](https://docs.microsoft.com/powerapps/maker/portals/overview) er tilbúin kerfisafurð sem býður upp á næstum rauntíma samskipti milli líkanadrifinni forrita í Dynamics 365 og Finance and Operations-forrita. Tvöföld skrif veitir tvíátta samþættingu milli Finance and Operations-forrita og Common Data Service. Þau bjóða þar af leiðandi upp á samþætta notandaupplifun í öllum forritunum. Viðskiptavinagáttin veltur á einingum sem eru samstilltar með tvöföldum skrifum. Áður en hægt er að fara með gögn úr Supply Chain Management í viðskiptavinagáttina verða tvöföld skrif að vera virk fyrir allar viðeigandi einingar.

![![Tengsl viðskiptavinagáttar](media/customer-portal-elements.png "Tengsl viðskiptavinagáttar")](media/customer-portal-elements.png "Customer portal dependencies")

Viðskiptavinagáttin virkar sem upphafspunktur fyrir fyrirtæki sem vilja nota Power Apps-gáttir til að búa til vefsvæði út á við sem notar gögn úr uppsetningu Supply Chain Management. Hún hjálpar fyrirtækjum að tengja saman tvöföld skrif, Supply Chain Management og Power Apps-gáttir.
