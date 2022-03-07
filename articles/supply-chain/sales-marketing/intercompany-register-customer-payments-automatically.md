---
title: Skrá greiðslur sjálfkrafa fyrir samstæðureikninga viðskiptavinar
description: Þetta efnisatriði útskýrir hvernig á að skrá greiðslur sjálfkrafa fyrir samstæðureikninga viðskiptavinar
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ffc5c7bf44989fbcc18e940b5a7c9df81260d770
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548338"
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
