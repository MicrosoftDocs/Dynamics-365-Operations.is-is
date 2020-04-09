---
title: Fylgjast með vörusendingabirgðum með samstarfi lánardrottna
description: Þessi verklýsing sýnir hvernig á að nota Lánardrottnar í samstarfi til að sjá upplýsingar um birgðamagn sem hafa verið settar í vörusendingu hjá viðskiptavini.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 589b478fa59f2fb2a5008d02e39f2808391d0994
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145573"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Fylgjast með vörusendingabirgðum með samstarfi lánardrottna

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að nota Lánardrottnar í samstarfi til að sjá upplýsingar um birgðamagn sem hafa verið settar í vörusendingu hjá viðskiptavini. Einnig er hæt að fylgjast með notkun birgða þegar viðskiptavinurinn tekur eignarhald á birgðum. Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="view-consumed-inventory"></a>Skoða notaðar birgðir
1. Fara í Lánardrottnar í samstarfi > vörusendingabirgðir > Afurðir mótteknar úr vörusendingabirgðum.
    * Listinn sýnir innhreyfingarskjalslínur sem voru mynduð þegar eignarhaldi á vörusendingabirgðum var breytt úr lánardrottni í viðskiptavin. Það gæti þurft að skruna til hægri til að sjá magn og aðrar upplýsingar. Hægt er að nota upplýsingarnar í þessum lista til að mynda reikninga fyrir viðskiptavini þína. Einnig er hægt að flytja út gögn í Microsoft Excel.   
2. Smelltu á Skoða innkaupapöntun.
3. Víkkið út hlutann „Upplýsingar um línu“.
    * Línan er merkt sem Vörusending, og hausinn sýnir að innkaupapöntun er með stöðuna Móttekið.  
4. Lokið síðunni.

## <a name="view-on-hand-inventory"></a>Skoða lagerbirgðir
1. Fara í Lánardrottnar í samstarfi > vörusendingabirgðir > vörusendingabirgðum á lager.
    * Síðan vörusendingabirgðir á lager sýnir birgðir sem þú átt í vöruhúsi viðskiptavinar. Hægt er að birta aðrar víddir, eins og svæði og vöruhús, með því að smella á flipann Birta víddir.   

