---
title: Skattaútreikningur (forskoðun)
description: Þetta efnisatriði skýrir heildarumfang og eiginleika skattaútreikningsgetu.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bab6e0e0ea1b9fb7f598e37843b52e3ba9c7f94e
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336633"
---
# <a name="tax-calculation-preview"></a>Skattaútreikningur (forskoðun)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Skattaútreikningur er þjónusta með stillanlegri þjónustu fyrir marga notendur sem gerir altæku skattkerfi kleift að einfalda skattaákvörðun og útreikning og gera það sjálfvirkt. Skattvélin er fullkomlega stillanleg. Einingarnar sem hægt er að stilla fela í sér, en takmarkast ekki við, skattalega gagnalíkansins, skattkóða, fylkisins fyrir skattskyldu og formúlu skattútreiknings. Skattkerfið keyrir á Microsoft Azure verkvangi og býður upp á nútímatækni og sveigjanleika.

Skattútreikningur er samþættur við Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Að lokum verður hún einnig samþætt við Dynamics 365 Project Operations, Dynamics 365 Commerce og önnur forrit frá fyrstu og þriðju aðilum.

> [!IMPORTANT]
> Þegar skattaútreikningsþjónustan er virkjuð gætu sumar aðgerðir á tengdum gögnum verið framkvæmdar í gagnamiðstöð annarri en gagnamiðstöðinni sem heldur utan um þjónustugögnin. Yfirfarið [Skilmálana](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) áður en skattaútreikningsþjónustan er virkjuð. Persónuvernd þín er okkur mikilvæg. Frekari upplýsingar má finna í [tilkynningu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=521839).

Skattaútreikningur er skattakerfi frá Microsoft sem býður upp á mikinn sveigjanleika. Það getur hjálpað þér að framkvæma eftirfarandi verk:

- Grunnstilla skattaútreikning með Regulatory Configuration Service (RCS). RCS er endurbætt útgáfa af hönnuði rafrænnar útgáfu og er fáanleg sem sjálfstæð þjónusta.
- Grunnstilla skattafylki til að ákvarða sjálfkrafa skattkóða og taxta.
- Grunnstilla skattafylki til að ákvarða sjálfkrafa skattskráningarnúmerið.
- Grunnstilla hönnuð skattaútreiknings til að skilgreina formúlur og skilyrði.
- Deildu skattákvörðun og útreikningslausn á milli lögaðila.

Til að nota skattaútreikningsþjónustu skal setja upp innbótina fyrir skattaútreikningsþjónustu ur verkefninu í Microsoft Dynamics Lifecycle Services (LCS). Ljúkið síðan uppsetningunni í RCS og virkið skattútreikningaþjónustuna í Finance and Supply Chain Management. Frekari upplýsingar eru í [Hafist handa með skattþjónustu](./global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Til ráðstöfunar

Skattaútreikningur er aðeins í boði í sandkassaumhverfi og til valinna viðskiptavina í gegnum almenna forútgáfu. Að lokum mun hún verða aðgengileg öllum viðskiptavinum og í framleiðsluferli.

Nýjir eiginleikar verða áfram kynntir til sögunnar og þess vegna þarf að gæta þess að skoða nýjustu fylgiskjöl til að fá upplýsingar um umfang studdra eiginleika.

Skattaútreikningur er í boði á eftirfarandi staðsetningum Azure. Hún verður einnig í boði á fleiri Azure-landsvæðum í samræmi við þarfir viðskiptavina:

- Bandaríkin
- Evrópa

> [!NOTE]
> Skattaútreikningur styður ekki uppsetningu Dynamics 365 á staðnum. Hún styður einnig ekki fyrri útgáfur, eins og Dynamics AX 2012.

## <a name="feature-highlights"></a>Helstu atriði eiginleika

- Stillanlegt skattafylki til að ákvarða og reikna út skatt sjálfkrafa
- Stuðningur fyrir mörg skattskráningarnúmer
- Stuðningur flutningspöntunar fyrir skattákvörðun og útreikning
- Stuðningur flutningspöntunar fyrir ákvörðun margra skattnúmera

## <a name="supported-transactions"></a>Studdar færslur

Lögaðili og færsluhirðir geta gert skattaútreikning virkan. Eftirfarandi færslur eru studdar:

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

[Hafist handa með skattþjónustu](./global-get-started-with-tax-calculation-service.md)

[Mörg VSK-skráningarnúmer](./emea-multiple-vat-registration-numbers.md)

[Stuðningur skattaeiginleika fyrir flutningspöntun](./tasks/tax-feature-support-for-transfer-order.md)

[Hvernig á að byggja upp viðbót í skattsþjónustu](./tax-service-add-data-fields-tax-integration-by-extension.md)
