---
title: Runu- og raðnúmer innan samstæðu
description: Þetta efnisatriði útskýrir hvað mun gerast þegar rununúmer og raðnúmer eru skráð fyrir pantanir innan samstæðu
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
ms.openlocfilehash: 9d5e6ddd0bf9ab9dd032e3ab8d1e11d53fba639e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672935"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Runu- og raðnúmer innan samstæðu

[!include [banner](../../includes/banner.md)]

Fyrirtæki sem nota raðnúmer eða rununúmer til að rekja vörur sínar þurfa einnig að fylgjast með raðnúmerum og rununúmerum vöru sem er tínd. Samstæðuvirknin gerir flutning raðnúmera og rununúmera milli fyrirtækja sjálfvirkan. Hægt er að setja kerfið þannig upp að þegar runu- og raðnúmer eru skráð fyrir vörurnar í samstæðusölupöntun að þá séu þessi númer send sjálfkrafa í samstæðuinnkaupapöntun og upphaflegu sölupöntunina. Þú setur upp viðeigandi færibreytur á síðunni **Innan samstæðu** fyrir sölupöntunina:

- Ef reiturinn **Rununúmer** er valinn á síðunni **Sölupöntunarreglur** er rununúmerið samstillt við birgðafærslur á innkaupapöntunarlínum samstæðu þegar fylgiseðill sölupöntunar innan samstæðu er bókaður.
- Ef svæðið **Raðnúmer** er valið er raðnúmerið samstillt við birgðafærslurnar á innkaupapöntunarlínum samstæðu þegar fylgiseðill sölupöntunar samstæðu er bókaður.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
