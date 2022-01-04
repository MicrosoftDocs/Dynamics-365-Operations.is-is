---
title: Viðskiptavinagátt fyrir Dynamics 365 Supply Chain Management yfirlit (inniheldur myndband)
description: Þetta efnisatriði fjallar um viðskiptavinagáttina og útskýrir hver ætti að nota hana og hvernig hún virkar.
author: Henrikan
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c1383ee3c8e72f630d29a557de4150cdd3aa905f
ms.sourcegitcommit: ef0dd4245fc499907ffe00e2a32f59a6cd96e45d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/18/2021
ms.locfileid: "7937505"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Viðskiptavinagátt fyrir Dynamics 365 Supply Chain Management-yfirlit

[!include [banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="what-is-the-customer-portal"></a>Hvað er viðskiptavinagátt?

Í dag treysta aðfangakeðjukerfi á samþættingu. Þau þarfnast þess að birgðir, eftirspurn viðskiptavinar og söludeildir verði samþættar í stað þess að vera hver í sínu horni. Viðskiptavinagáttin hjálpar fyrirtækjum sem keyra Microsoft Dynamics 365 Supply Chain Management að auka þessa samþættingu og, það sem meira er, að halda viðskiptavinunum upplýstum.

Viðskiptavinagáttin er sniðmát [Power Apps-gáttar](/powerapps/maker/portals/overview) sem gerir fyrirtækjum kleift að búa til vefsvæði sem gengur út á viðskipta milli fyrirtækja (B2B) fyrir aðstæður sem tengjast sölupöntunarferlum. Sniðmátið notar [tvíritun](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md), Supply Chain Management og gáttir Power Apps til að gera utanaðkomandi fyrirtækjum kleift að skoða og búa til gögn úr Dynamics 365-umhverfi fyrirtækisins.

Sniðmát viðskiptavinagáttar er með alla sérstillingarmöguleika sem gáttir Power Apps bjóða upp á. Auðveldlega er hægt að breyta sniðmátinu til að halda vörumerki fyrirtækisins á lofti, bæta við aukinni virkni og breyta notandaupplifuninni. Hægt er að breyta allri virkni sem tilbúna sniðmátið býður upp á.

> [!IMPORTANT]
> Ekki er gert ráð fyrir að sniðmátið virki að fullu eitt og sér. Það þjónar bara sem hvati fyrir viðskiptavini sem vilja búa til almennt vefsvæði svo að fyrirtækin í viðskiptum geti nálgast gögnin í Supply Chain Management.

> [!NOTE]
> Fylgiskjölum viðskiptavinagáttar er beint að stjórnendum, hönnuðum og þróunaraðilum kerfis sem setja upp viðskiptavinagáttina fyrir uppsetningu Supply Chain Management. Það notar hugtökin _viðskiptavinur_ og _notandi_ til að lýsa einstaklingum sem eru viðskiptavinir fyrirtækisins sem keyrir Supply Chain Management, og sem nota sjálfa lokagáttina.

## <a name="video"></a>Myndband

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

Myndbandið [Yfirlit yfir sniðmát viðskiptavinagáttar í Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) (sýnt hér að ofan) er innifalið í [Finance and Operations spilunarlistanum](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) á YouTube.

## <a name="who-should-use-it"></a>Hver ætti að nota hana?

Viðskiptavinagáttin er hönnuð fyrir fyrirtæki sem keyra Supply Chain Management og eru af þessum toga:

- Þau vilja byggja upp vefsvæði út á við sem miðlar upplýsingum um vinnslu pantana (svo sem pöntunarstöðu eða reikningsupplýsingar) beint úr Supply Chain Management-kerfinu þeirra til fyrirtækja sem þau eru í viðskiptum við.
- Þau eru að færa sig úr Dynamics AX 2012 í Supply Chain Management og notuðu áður [AX 2012 Sjálfsafgreiðslugátt viðskiptavina](/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Eftirfarandi gerðir fyrirtækja eru **ekki** góðir kandídatar fyrir innleiðingu viðskiptavinagáttar:

- Fyrirtæki sem vilja setja upp vefsvæði fyrir viðskiptavini sem ekki eru fyrirtæki. Þessi fyrirtæki ættu að íhuga að búa til [Dynamics 365 Commerce vefsvæði rafrænna viðskipta](../../commerce/create-ecommerce-site.md).
- Fyrirtæki sem eru þegar að nota fyrirliggjandi vefsvæði Power Apps-gáttar í svipuðum tilgangi. Þessi fyrirtæki fá ekki frekari fríðindi frá viðskiptavinagáttinni. Viðskiptavinagáttin er afhend sem sniðmát sem virkar eins og leiðarvísir og upphafspunktur fyrir viðskiptavini sem vilja „tengja saman punktana“ milli tvíritunar, Supply Chain Management og Power Apps-gátta. Ef þegar er búið að setja upp vefsvæði sem þjónar þessum tilgangi er ekki víst að neinn ávinningur fylgi því að nota sniðmát viðskiptavinagáttar til að endurúthluta þessu vefsvæði.

## <a name="how-does-it-work"></a>Hvernig virkar það?

Viðskiptavinargátt er gefin upp sem Power Apps gáttasniðmát. Það fer eftir Power Apps-gáttum og tvíritun.

[Power Apps gáttir](/powerapps/maker/portals/overview) er eiginleiki sem gerir notendum kleift að búa til vefsvæði fyrir almenning sem fólk utan fyrirtækisins geta skráð sig inn á. Lítil eða engin kóðun er nauðsynleg til að búa til gáttir. Viðskiptavinagáttin er eitt margra [sniðmáta Dynamics 365-gáttar](/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) sem eru í boði hjá Microsoft.

[Tvöföld skrif](/powerapps/maker/portals/overview) er tilbúið tölvuvörukerfi sem býður upp á samskipti í rauntíma á milli forrita viðskiptavina og Finance and Operations-forrita. Tvöföld skrif veitir tvíátta samþættingu milli Finance and Operations-forrita og Microsoft Dataverse. Þau bjóða þar af leiðandi upp á samþætta notandaupplifun í öllum forritunum. Viðskiptavinagáttin veltur á töflum sem eru samstilltar með tvöföldum skrifum. Áður en hægt er að fara með gögn úr Supply Chain Management í viðskiptavinagáttina verða tvöföld skrif að vera virk fyrir allar viðeigandi töflur.

![Tengsl viðskiptavinagáttar.](media/customer-portal-elements.png "Tengsl viðskiptavinagáttar")

Viðskiptavinagáttin virkar sem upphafspunktur fyrir fyrirtæki sem vilja nota Power Apps-gáttir til að búa til vefsvæði út á við sem notar gögn úr uppsetningu Supply Chain Management. Hún hjálpar fyrirtækjum að tengja saman tvöföld skrif, Supply Chain Management og Power Apps-gáttir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]