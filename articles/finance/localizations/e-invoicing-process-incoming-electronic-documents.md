---
title: Afgreiðsla rafrænna skjala sem berast
description: Þessi grein veitir yfirlit yfir vinnslu rafrænna skjala sem berast.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277302"
---
# <a name="processing-of-incoming-electronic-documents"></a>Afgreiðsla rafrænna skjala sem berast

[!include [banner](../includes/banner.md)]

Hægt er að flytja inn rafræn skjöl, svo sem rafræna reikninga lánardrottna, inn og vinna á tvo vegu:

- Skrár eru sóttar af ytri rásum og sendar beint í tengda forritið þitt. Þar gangast þær fyrir frekari umbreytingum og eru síðan fluttar inn í gagnagrunninn.
- Skrár fara í forvinnslu í rafrænum reikningaþjónustu og eru síðan sendar í tengda umsókn þína.

Rafræn reikningagerð styður tvær rásir fyrir skjöl sem berast: tölvupóst og Microsoft SharePoint möppur.

Það eru twp uppsetningargerðir til að tilgreina hvort skjöl gangast undir forvinnslu eða fara beint í tengda forritið þitt:

- **Gagnarás** – Kerfið mun senda skjalið beint í tengda forritið.
- **Gagnarás með vinnsluleiðslu** – Þú getur sett upp viðbótaraðgerðir sem verða keyrðar áður en skjalið er sent til tengda forritsins.

Fyrir upplýsingar um hvernig á að setja upp aðstæður fyrir vinnslu rafrænna skjala sem berast fyrir mismunandi rásir, sjá [Stilltu tölvupóstrás](e-invoicing-configure-email.md) og [Stilla a SharePoint rás](e-invoicing-configure-sharepoint-channel.md).
