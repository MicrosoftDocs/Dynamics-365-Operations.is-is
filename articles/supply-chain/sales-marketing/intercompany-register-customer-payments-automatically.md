---
title: Skrá greiðslur sjálfkrafa fyrir samstæðureikninga viðskiptavinar
description: Þetta efnisatriði útskýrir hvernig á að skrá greiðslur sjálfkrafa fyrir samstæðureikninga viðskiptavinar
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: dbd06b21d736d1e247cd087e5bb86fbe641352e6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669433"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Skrá greiðslur sjálfkrafa fyrir samstæðureikninga viðskiptavinar

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management stofnar viðskiptavinafærslu þegar samstæðureikningur viðskiptavinar er bókaður. Þessi viðskiptavinafærsla helst opin þar til hún er jöfnuð, sem þýðir að hún hafi verið greidd. Þegar samsvarandi samstæðuinnkaupapöntun er reikningsuppfærð er lánardrottinsfærsla sem samsvarar viðskiptavinafærslunni stofnuð. Þessi lánardrottnafærsla helst einnig opin þar til hún er jöfnuð. Til að draga úr hættunni á misræmi er hægt að stofna greiðslubók viðskiptavina sjálfkrafa og bóka hana þegar greiðslubók lánardrottna er bókuð.

1. Opnið **Sölu og markaðssetning \> Viðskiptavinir \> Allir viðskiptavinir**.
1. Í aðgerðasvæðinu, á flipanum **Almennt**, skal velja **Innan samstæðu**.
1. Til að setja upp greiðslur vegna viðskiptakrafa innan samstæðu á síðunni **Innan samstæðu** fyrir sölupantanir skal velja tengilinn **Sölupöntunarreglur**.
1. Í reitnum **Greiðslubók** skal velja greiðslubók viðskiptakröfu sem á að skrá greiðslur samstæðulánardrottins í. Þetta er sett upp á síðunni **Færibreytur viðskiptakrafa**.
1. Ef þú vilt bóka í þessa færslubók sjálfkrafa skaltu velja gátreitinn **Bóka færslubók sjálfvirkt**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
