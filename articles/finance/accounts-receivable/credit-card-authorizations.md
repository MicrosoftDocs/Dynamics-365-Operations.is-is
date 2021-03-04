---
title: Uppsetningar á kreditkorti, heimild og sækja
description: Þessi grein veitir yfirlit yfir kreditkortaheimildir í Microsoft Dynamics 365 Finance. Þar á meðal eru upplýsingar um hvernig á að setja upp greiðsluþjónustu, bæta kreditkorti við sölupöntun, og ógilda heimild.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0de35934e8bdb160f68f68dab118997d0141bf29
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444246"
---
# <a name="credit-card-setup-authorization-and-capture"></a>Uppsetningar á kreditkorti, heimild og sækja

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir kreditkortaheimildir í Microsoft Dynamics 365 Finance. Þar á meðal eru upplýsingar um hvernig á að setja upp greiðsluþjónustu, bæta kreditkorti við sölupöntun, og ógilda heimild.

<a name="setting-up-the-credit-card-payment-service"></a>Setja upp greiðsluþjónustu kreditkorts
------------------------------------------

Til að nota kreditkort, verður að setja upp og virkja greiðsluþjónustu á síðunni greiðsluþjónusta. Greiðsluþjónustu virkar eins og brú á milli lögaðila lögaðila þíns og bankans sem vinnur kreditkortagjöld viðskiptavinarins. Þú Þarft að vinna með kreditkortaveitu sem er talin upp í svæðinu greiðslutengill og setja upp lykil hjá þessari veitu. Svo er verður að setja upp aðra valkosti á síðunni greiðsluþjónusta, setja upp greiðslukortagerðir fyrir American Express, Discover, MasterCard og Discover á síðunni gerðir kreditkorts og virkja veitu sem sjálfgefna veitu. Einnig verður að fylgja þessum skrefum til að ljúka uppsetningu:
-   Tilgreina færibreytur fyrir notkun kreditkortaheimilda á síðunni færibreytur viðskiptakrafna.
-   Greiðsluskilmálar fyrir kreditkort eru settir upp á síðunni Greiðsluskilmálar. Í svæðinu greiðslugerð er valin kreditkort.
-   Á síðunni kreditkort viðskiptavinar, skal Færa inn kreditkortaupplýsingar viðskiptavinar.

## <a name="adding-a-new-credit-card"></a>Bæta við nýju kreditkorti
Hægt er að stofna nýjar kreditkortafærslur á síðunni Viðskiptavinir með því að nota Viðskiptavinur, Setja upp, kreditkort. Einnig er hægt að stofna kreditkortafærslur þegar sölupantanir eru færðar inn á síðunni Vsk, með því að nota Stjórna, Viðskiptavinur, kreditkort, Afgreiðslukassi.

<a name="adding-a-credit-card-to-a-sales-order"></a>Kreditkorti bætt við sölupöntun
-------------------------------------

Hægt er að bæta kreditkort við sölupöntun með því að velja greiðslukort í uppflettingu kreditkorta í Verð og afslátt flýtiflipa á síðunni Vsk. Til að hefja heimildarferlið, á aðgerðarúðunni, á flipanum Stjórna, veljið kreditkort og heimila.

<a name="authorizing-a-credit-card"></a>Heimila kreditkort
-------------------------

Þegar kreditkort er gefin heimild, er kortanúmerið og nafn handhafa sannvottuð og tiltæk lánsheimild staðfest. Valkvætt er að staðfesta aðsetur og CVV-númer í korthafa. Tiltæk Lánsheimild viðskiptavinar er síðan minnkuð sem nemur reikningnum.. Greiðsluþjónusta sendir upplýsingar um að kreditkortið hefur verið samþykkt eða hafnað. Þegar sölupöntun er reikningsfærð, er kreditkortið rukkað (sótt) um upphæð reikningsins.

### <a name="card-verification-value"></a>Sannprófunargildi korts

Hægt er að krefjast CVV-númers, sem er stundum er kallað öryggisnúmer korts. Þetta er fjögurra stafa gildi fyrir American Express. Fyrir Discover, MasterCard og Visa, er gildið þriggja stafa.

### <a name="address-verification"></a>Staðfesting aðseturs

Sannprófun aðsetursupplýsinga er alltaf sent í greiðsluþjónustuaðila. Hægt er að velja hversu mikils af upplýsingum er krafist til að færsla sé samþykkt. Gætið þess að hafa samband við veitu til að ákvarða hvort hún samþykkir þessar upplýsingar. Hér eru valkostir aðseturssannvottunar:
-   **Alltaf samþykkja færslu** – Samþykkja færsluna, án tillits til niðurstaða aðsetursstaðfestingar.
-   **Handhafi lykils** – bera Saman nafn korthafa í færslunni við upplýsingar um kreditkort hjá fyrirtækisins.
-   **Innheimtuaðsetur** – bera Saman nafn korthafa og innheimtuaðsetur færslunnar við upplýsingum um kreditkort hjá fyrirtæki.
-   **Innheimtupóstnúmer** – bera Saman nafn korthafa og innheimtuaðsetur og póstnúmer færslunnar við upplýsingum um kreditkort hjá fyrirtækinu.

## <a name="data-support"></a>Gagnastuðningur
Fyrir hverja tegund kreditkorts sem er studd, er hægt að tilgreina í gagnastuðningsstig. Stigið stýrir hversu mikið af upplýsingum um færslu er flutt í greiðsluþjónustu. Gætið þess að hafa samband við veitu til að ákvarða hvort hún geti veitt þessar upplýsingar. Hér eru valkostir fyrir gagnastuðningsstig:
-   **Stig 1** - flytja færsludagsetningu, færsluupphæð og lýsingu.
-   **Stig 2** flytja upplýsingar um Stig 1 og einnig aðsetur sendingar- og söluaðila, og skattaupplýsingar.
-   **Stig 3** flytja yfir allar upplýsingar um Stig 2, auk upplýsingar pöntunarlínu.

## <a name="partial-payments"></a>Hlutagreiðslur
Ef þú flytur hluta af pöntun, er magn af hlutapöntun sótt , og heimildin, sem var fyrir upphæð allrar pöntunarinnar, er lokað. Ný heimild er þá send inn fyrir eftirstandandi fjárhæð pöntunar sem ekki hefur verið send.

## <a name="voiding-an-authorization"></a>Ógilda heimild
Til að ógilda heimild fyrir kreditkort, er hægt að breyta greiðsluhætti í annan greiðslumáta sem ekki hefur tegund kreditkorts.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]