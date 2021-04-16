---
title: Skattaútreikningsþjónusta (forskoðun)
description: Þetta efnisatriði skýrir heildarumfang og eiginleika skattaútreikningaþjónustunnar.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818225"
---
# <a name="tax-calculation-service-preview"></a>Skattaútreikningsþjónusta (forskoðun)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Skattaútreikningsþjónustan er þjónusta með stillanlegri þjónustu fyrir marga notendur sem gerir altæku skattkerfi kleift að einfalda skattaákvörðun og útreikning og gera það sjálfvirkt. Skattvélin er fullkomlega stillanleg. Einingarnar sem hægt er að stilla fela í sér, en takmarkast ekki við, skattalega gagnalíkansins, skattkóða, fylkisins fyrir skattskyldu og formúlu skattútreiknings. Skattkerfið keyrir á Microsoft Azure verkvangi og býður upp á nútímatækni og sveigjanleika.

Skattútreikningaþjónustan er samþætt við Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Að lokum verður hún einnig samþætt við Dynamics 365 Project Operations, Dynamics 365 Commerce og önnur forrit frá fyrstu og þriðju aðilum.

Skattaútreikningsþjónustan er skattakerfi frá Microsoft sem býður upp á mikinn sveigjanleika. Það getur hjálpað þér að framkvæma eftirfarandi verk:

- Grunnstilla skattaútreikningsþjónustu með Regulatory Configuration Service (RCS). RCS er endurbætt útgáfa af hönnuði rafrænnar útgáfu og er fáanleg sem sjálfstæð þjónusta.
- Grunnstilla skattafylki til að ákvarða sjálfkrafa skattkóða og taxta.
- Grunnstilla skattafylki til að ákvarða sjálfkrafa skattskráningarnúmerið.
- Grunnstilla hönnuð skattaútreiknings til að skilgreina formúlur og skilyrði.
- Deildu skattákvörðun og útreikningslausn á milli lögaðila.

Til að nota skattaútreikningsþjónustu skal setja upp innbótina fyrir skattaútreikningsþjónustu ur verkefninu í Microsoft Dynamics Lifecycle Services (LCS). Ljúkið síðan uppsetningunni í RCS og virkið skattútreikningaþjónustuna í Finance and Supply Chain Management. Frekari upplýsingar eru í [Hafist handa með skattþjónustu](https://go.microsoft.com/fwlink/?linkid=2138482).

## <a name="availability"></a>Til ráðstöfunar

Skattaútreikningaþjónustan er aðeins í boði í sandkassaumhverfi og til valinna viðskiptavina í gegnum almenna forútgáfu. Að lokum mun hún verða aðgengileg öllum viðskiptavinum og í framleiðsluferli.

Áfram verður boðið upp á nýja eiginleika í skattaútreikningsþjónustu. Þess vegna þarf að gæta þess að skoða nýjustu fylgiskjöl til að fá upplýsingar um umfang studdra eiginleika.

Skattaútreikningsþjónustan er í boði á eftirfarandi staðsetningum Azure. Hún verður einnig í boði á fleiri Azure-landsvæðum í samræmi við þarfir viðskiptavina:

- Bandaríkin
- Evrópa
- Frakkland
- Bretland

> [!NOTE]
> Útreikningaþjónustan styður ekki uppsetningu Dynamics 365 á staðnum. Hún styður einnig ekki fyrri útgáfur, eins og Dynamics AX 2012.

## <a name="feature-highlights"></a>Helstu atriði eiginleika

- Stillanlegt skattafylki til að ákvarða og reikna út skatt sjálfkrafa
- Stuðningur fyrir mörg virðisaukaskattsnúmer (VSK)
- Stuðningur flutningspöntunar fyrir skattákvörðun og útreikning
- Stuðningur flutningspöntunar fyrir ákvörðun margra VSK-númera

## <a name="supported-transactions"></a>Studdar færslur

Lögaðili og færsluhirðir getur gert skattalíkanið virkt. Eftirfarandi færslur eru studdar:

- Söluferli

    - Sölutilboð
    - Sölupöntun
    - Staðfesting
    - Tiltektarlisti
    - Fylgiseðill
    - Sölureikningur
    - Kreditnóta
    - Skila pöntun
    - Ýmis hausgjöld
    - Ýmis línugjöld

- Innkaupaferli

    - Innkaupapöntun
    - Staðfesting
    - Komulisti
    - Innhreyfingarskjal afurða
    - Innkaupareikningur
    - Ýmis hausgjöld
    - Ýmis línugjöld
    - Kreditnóta
    - Skila pöntun
    - Innkaupabeiðni
    - Ýmis gjöld innkaupabeiðnilínu
    - Beiðni um tilboð
    - Ýmis hausgjöld fyrir beiðni um tilboð
    - Ýmis línugjöld fyrir beiðni um tilboð

- Birgðavinnsla

    - Flutningspantanir - senda
    - Móttaka flutningspöntunar

## <a name="related-resources"></a>Tengd tilföng

[Hafist handa með skattþjónustu](https://go.microsoft.com/fwlink/?linkid=2138482)

[Mörg VSK-skráningarnúmer](https://go.microsoft.com/fwlink/?linkid=2153387)

[Stuðningur skattaeiginleika fyrir flutningspöntun](https://go.microsoft.com/fwlink/?linkid=2153388)

[Hvernig á að byggja upp viðbót í skattsþjónustu](https://go.microsoft.com/fwlink/?linkid=2138483)
