---
title: TDS-útreikningur á færslum innan samstæðu
description: Þetta efnisatriði lýsir ferlinu sem er notað til að reikna út frádrátt skatt sem dreginn er frá í uppruna (TDS) á færsla milli fyrirtækja í áföngum.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 029a9bcc6fad7bc3348716aadeeda9552a086e5b1a6d08018c1aaced4b241a1d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727250"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>TDS-útreikningur á færslum innan samstæðu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir ferlinu sem er notað til að reikna út frádrátt skatt sem dreginn er frá í uppruna (TDS) á færsla milli fyrirtækja í áföngum.

Þegar innkaupapöntun eða sölupöntun samstæðu er stofnuð er sjálfgefinn TDS-hópur sem er skilgreindur fyrir viðskiptavininn eða lánardrottinn notaður til að reikna út TDS-fjárhæðina. TDS-upphæðin er bókuð á reikninga sem hægt er að endurheimta eða greiða eftir bókun reikningsins.

Samstæðusölupöntun eða innkaupapöntun er sjálfkrafa stofnuð fyrir upprunalega innkaupapöntunina eða sölupöntunina. Sjálfgefni TDS-hópurinn er sýndur á samstæðupöntun, þannig að hægt er að reikna út TDS. Hægt er að breyta TDS-hópnum. Einungis er hægt að bóka reikninginn ef nettóreikningsupphæð samstæðupöntun sem er sjálfkrafa búin til samsvarar nettóreikningsupphæð á upprunalegu pöntuninni. (Nettóupphæðin er reikningsupphæðin eftir að TDS er dregið frá.)

Sölureikningur er til dæmis stofnaður fyrir 50.000 og **10%** TDS-hópurinn er tengdur honum. Upphæð bókaðs reiknings er 45.000 og upphæð bókaðs TDS reiknings fyrir sölureikninginn er 5.000 krónur. Innkaupapöntun stofnast sjálfkrafa fyrir samstæðusölupöntunina og **10%** TDS-hópurinn er tengdur henni. Ef TDS-hópnum er breytt í **15%** er ekki hægt að bóka reikninginn vegna þess að nettógreiðsluupphæðin á samstæðusölupöntunin sem var stofnuð sjálfkrafa samsvarar ekki nettógreiðsluupphæðinni í upprunalegu sölupöntuninni.

Greiðslubók sem er búin til fyrir samstæðureikning er sjálfkrafa bókuð. Aðeins er hægt að bóka greiðslubókina ef nettógreiðsluupphæðin á henni samsvarar nettógreiðsluupphæðinni á upphaflegu greiðslubókinni.
