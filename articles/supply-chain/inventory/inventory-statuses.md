---
title: Birgðastöður
description: Þessi grein lýsir því hvernig þú getur notað birgðastöðu til að flokka og fylgjast með birgðum.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd86bf525ae33f78fb472e6c333083592ff8a012
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024385"
---
# <a name="inventory-statuses"></a>Birgðastöður

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig þú getur notað birgðastöðu til að flokka og fylgjast með birgðum.

Hægt er að nota birgðastöðu til að flokka birgðir. Síðan er hægt að hefja viðeigandi aðgerðir, eins og áfyllingu eða frágangsvinnu.

Hér eru nokkur dæmi um sem hægt er að nota birgðastöður:

-   Stofna stöðuna fyrir birgðir á lager, færslur á innleið og færslur á útleið .
-   Tilgreina sjálfgefna birgðastöðu fyrir færslur fyrir vöruhús.
-   Breyta stöðu birgða í vörum fyrir komu vöru, við komu, eða þegar vörur eru frágangur við birgðahreyfingu.
-   Notið birgðastöðu fyrir verðlagningu á vörum þegar þeim er skilað og til að áætla þekju fyrir vöru við aðaláætlanagerð.

Birgðastaða er ein af víddum í geymsluvíddaflokki. Hægt er að flokkað birgðastöðu sem tiltækt eða ekki tiltækt og hægt er að nota **birgðalæsingu** færibreytu til að læsa vörum sem hafa stöðuna ekki tiltækt í birgðum. Vörur með lokaða stöðu eru taldar raunbirgðir og ekki er hægt að nota þær í framleiðslupöntun, sölupöntun, millifærslupöntun eða útleiðarfærslu.

Hægt er að nota vörur í vöruhúsi með birgðastöðu tiltækt eða ekki tiltækt fyrir vinnu á innleið. Til dæmis stofnaður tiltæka stöðu sem heitir **tilbúinn**, ótiltæka stöðu sem heitir **skemmt** og lokaða stöðu sem heitir **lokað**. Þegar innkaupapöntun er stofnuð fyrir móttekið eða skilavörur, ef einhverjar vörur eru skemmt eða brotið, hægt að breyta birgðastöðu þær vörur **"Skemmt"** í innkaupapöntunarlínunni. Eftir að þessar vörur eru mótteknar staðan er sjálfkrafa stillt á **Læst**. Ef að þú skannar þessar skemmdu vörur með fartæki, getur Finance and Operations notað staðsetningarleiðbeiningar og vinnusniðmát til að birta upplýsingar um viðeigandi staðsetning eða svið staðsetningar fyrir frágang þessara vara. Fyrir skilavörur er stofnuð **frátekning** fyrir úthreyfingar í skjámyndinni **Birgðafærslur**.

Notið vörur með stöðu tiltækar birgðir fyrir vinnu á útleið. Ef þú ert með vörur með stöðuna **slitin** og aðaláætlanagerð er keyrð fyrir þessar vörur, er litið á þessar vörur þannig að þær vanti og birgðir eru endurnýjaðar sjálfkrafa.

Eftir að þú hefur sett upp birgðastöðu er hægt að stilla sjálfgefna birgðastöðu fyrir síðu, vöru og vöruhús. Einnig er hægt að stilla sjálfgefna stöðu fyrir sölu, flutning, og innkaupapantanir. Sjálfgefin staða fyrir sölupantanir og flutningspöntun á útleið getur ekki haft **birgðalæsingu** valkostur stilltan á **Já**. Birgðastöðu sem er erft frá sjálfgefnar stillingar á setri, vöruhúsi, vöru, innkaupapöntun, flutningspöntun eða sölupöntun er hægt að breyta með því að nota fartækið eða á innkaupapöntun, sölupöntun eða flutningspöntunarlínu.

Til að áætla þekju fyrir vörur sem hafa stöðuna tiltækar birgðir skal velja **þekjuáætlun eftir vídd** valkostinn fyrir geymsluvídd á í **geymsluvíddaflokka** síðu. Þegar opnar **Vöruþekju** leiðsagnarforritið birtast vörur sem hafa stöðuna tiltækt á **Stöðu** síðu. Til að stofna þekjustillingar fyrir þessar vörur er að velja birgðastöðukenni fyrir tiltæka birgðastöðu. Samkvæmt þekjustillingar hægt að reikna vöruþarfir og spá framboð og eftirspurn tiltækar vörur með við áætlanagerð. Ekki er hægt að stofna uppsetningu vöruþekju með læsta birgðastöðu. Að öðrum kosti notarðu **vöruþekju** síðu til að stofna eða breyta tryggingafæribreytum vöru.
