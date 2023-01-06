---
title: Rafræn reikningsfærsla fyrir Egyptaland
description: Í þessari grein er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Egyptaland í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: e603bcad4d6dc46bd2594cfdcdf8871eb1f49019
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269502"
---
# <a name="electronic-invoicing-for-egypt"></a>Rafræn reikningsfærsla fyrir Egyptaland

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Egyptaland. Það leiðir notandann í gegnum grunnstillingarskrefin sem fara eftir hverju landi fyrir sig í Regulatory Configuration Services (RCS). Þessi skref eru viðbót við skrefin sem lýst er í [Setja upp rafrænar reikningsfærslur](e-invoicing-set-up-overview.md).

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að hefja ferlið í þessari grein þarf að ljúka eftirfarandi skilyrði:

- Kynnið ykkur rafræna reikningagerð eins og henni er lýst í [Yfirlit rafrænnar reikningsfærslu](e-invoicing-service-overview.md).
- Skráðu þig fyrir RCS og settu upp Rafræna reikninga. Frekari upplýsingar er hægt að finna í eftirfarandi efni:

    - [Skráðu þig fyrir og settu upp þjónustu fyrir rafræna reikninga](e-invoicing-sign-up-install.md)
    - [Setja upp Azure-tilföng fyrir rafrænar reikningsfærslur](e-invoicing-set-up-azure-resources.md)
    - [Setja upp viðbót smáþjónustu í Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    
- Virkja samþættingu milli Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management og rafrænnar reikningsfærsluþjónustu eins og lýst er í [Virkja og setja upp samþættingu við rafræna reikningsfærslu](e-invoicing-activate-setup-integration.md).
- Búa til stafrænan leynilykil í Azure-lyklageymslu og setja hann upp eins og lýst er í [Vottorð og leynilyklar viðskiptavina](e-invoicing-customer-certificates-secrets.md). Í prófunartilgangi veita egypsk skattyfirvöld ákveðnar prufur af stafrænum vottorðum sem þarf aðeins að nota við prófun og staðfestingu lausnar. Til að fá frekari upplýsingar skal skoða vefsvæði egypskra skattyfirvalda með tenglinum sem gefinn er upp í [SDK rafræn reikningsfærsla í Egyptalandi](https://sdk.invoicing.eta.gov.eg/faq/).

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Landssértæk skilgreining fyrir rafrænan reikningseiginleika fyrir Egyptaland (EG)

Sumar færibreyturnar úr **Rafræna reikningseiginleikanum fyrir Egypskan rafrænan reikning (EG)** eru birtar með sjálfgefnum gildum. Farið yfir sjálfgefin gildin og, ef þörf krefur, uppfærið gildin svo þau endurspegli betur fyrirtækjareksturinn áður en rafræni reikningseiginleikinn er notaður í þjónustuumhverfinu.

1. Flytja inn nýjustu útgáfu altæka eiginleikans **Egypskur rafrænn reikningur (EG)** eins og lýst er í [Flytja inn eiginleika úr altækri geymslu](e-invoicing-import-feature-global-repository.md).
2. Útbúðu afrit af innflutta altæka eiginleikanum og veldu skilgreiningarveitu fyrir hann eins og lýst er í [Stofna altækan eiginleika](e-invoicing-create-new-globalization-feature.md).
3. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
4. Í flipanum **Uppsetningar**, í hnitanetinu, skal velja eiginleikauppsetningu **Sölureikningur afleiddur**.
5. Veljið **Breyta**.
6. Á flipanum **Pípuvinnsla** í hlutanum **Pípuvinnsla** er valið **Undirrita JSON-skjal fyrir egypsk skattyfirvöld**.
7. Í hlutanum **Færibreytur** velur þú **Heiti skírteinis** og velur svo heiti stafræna skírteinisins sem þú bjóst til.
8. Í hlutanum **Pípuvinnsla** skal velja **Samþætta við egypska ETA-þjónustu**. Endurtakið þetta skref fyrir tvö tilvik þessarar aðgerðar.
9. Í hlutanum **Færibreytur** skal velja **Vefslóð þjónustu** og **Skrá inn vefslóð þjónustu**. Farðu svo yfir færibreytur vefslóðarinnar. Til að fá prófunar- og framleiðsluvefslóð skal opna vefsvæði egypskra skattyfirvalda til að fá vefslóð prófunar og framleiðslu með því að nota tengilinn sem gefinn er upp í [SDK rafrænnar reikningsfærslu fyrir Egyptaland](https://sdk.invoicing.eta.gov.eg/faq/).
10. Veljið **Vista** og lokið skjámyndinni.
11. Endurtakið skref 4 til 10 fyrir eiginleikauppsetninguna **Verkreikningur afleiddur**.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Landsbundin skilgreining forritsuppsetningar rafrænnar reikningsfærslu fyrir rafrænan reikning í Egyptalandi (EG)

Það eru færibreytur sem verða að vera settar upp í Finance eða Supply Chain Management umhverfi. Þú getur lokið við þessa uppsetningu á tveimur stöðum:

- Beint í útgáfu Finance eða Supply Chain Management-umhverfi. Nánari upplýsingar má finna í [Setja upp færibreytur fyrir rafræna reikningsfærslu](e-invoicing-set-up-parameters.md).
- Í RCS. Í tengslum við uppsetningu rafrænna reikningsfærslu er hægt að skilgreina allar færibreytur og setja þær svo beint inn í umhverfi Finance eða Supply Chain Management-umhverfis þegar þú setur inn rafræna reikningagerð.

Fyrir báða valmöguleikana eru færibreyturnar þær sömu. Ef þú ert að setja upp fyrsta eiginleikann þinn í rafrænni reikningsfærsluþjónustu mælum við með því að þú fylgir eftirfarandi skrefum til að setja upp færibreyturnar í RCS og setja þær svo inn í tengda forritið þitt.

> [!NOTE]
> Sumar eiginleikaútgáfur rafrænnar reikningsfærslu gætu innihaldið fyrirframskilgreindar sértækar færibreytur fyrir Finance eða Supply Chain Management. Ef svo er ættir þú að staðfesta að gögnin séu rétt. Annars skal stilla færibreytur handvirkt.

1. Finndu afritið af altækum eiginleika **Egypskur rafrænn reikningur (EG)** sem þú bjóst til.
2. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
3. Í flipanum **Uppsetningar** skal velja **Uppsetning forrits**.
4. Í reitnum **Tengt forrit** skal velja forritið þar sem á að setja upp færibreyturnar.
5. Á síðunni **Gerðir rafrænna skjala** velur þú **Bæta við** til að stofna færslu.
6. Í svæðið **Heiti töflu** skal bæta við **CustInvoiceJour**.
7. Í reitnum **Samhengi** skaltu bæta við tilvísun í vörpunarheitið **Samhengi viðskiptavinareiknings**. Skilgreiningin er **Samhengislíkan viðskiptavinareiknings**.
8. Í reitnum **Rafræn skjalatenging** skaltu bæta við tilvísun í vörpunarheiti **Reikningur viðskiptavinar**. Skilgreiningin er **Vörpun reikningslíkans**.
9. Veldu **Vista**.
10. Á síðunni **Svargerðir** skaltu velja **Bæta við**.
11. Í reitinn **Gerð svars** skal færa inn **Svar**.
12. Í reitinn **Lýsing** skal slá inn **Vinna úr svörum**.
13. Í reitnum **Staða sendingar** skal velja **Í bið**.
14. Í reitnum **Líkanavörpun** skal velja **Innflutningur svarskilaboða**. Skilgreiningin er **Innflutningur svarskilaboða fyrir Egyptaland (EG)**.
15. Veldu **Vista**.
16. Veljið **Bæta við**.
17. Í reitinn **Gerð svars** skal færa inn **ResponseData**.
18. Í reitinn **Lýsing** skal slá inn **Vinna úr svargögnum**.
19. Í reitnum **Staða sendingar** skal velja **Í bið**.
20. Í reitnum **Heiti gagnaeiningar** skal velja **SalesInvoiceHeaderV2Entity**.
21. Í reitinn **Líkanavörpun** skal velja **Innflutningur svargagna**. Skilgreiningin er **Innflutningssnið svargagna fyrir Egyptaland (EG)**.
22. Veljið **Vista** og lokið skjámyndinni.
23. Lokið síðunni.

Til að setja inn eiginleika í þjónustuumhverfið og uppsetningu forrits í tengda Finance eða Supply Chain Management-forritið, sjá [Ljúka við, birta og setja upp altækan eiginleika](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Ef eiginleikanum **Egypskur rafrænn reikningur (EG)** er virkjaður gæti þurft að senda takmarkað magn af gögnum. Þessi gögn innihalda skattaskráningarauðkenni stofnunar/fyrirtækis. Þessi gögn verða send til stofnana þriðja aðila sem skattyfirvöld heimila að megi senda rafræna reikninga til þessara skattyfirvalda á fyrirframskilgreindu sniði sem þarf fyrir samþættingu við vefþjónustu yfirvalda. Stjórnandi getur kveikt og slökkt á eiginleikanum með því að fara í **Fyrirtækisstjórnun**\>**Uppsetning**\>**Færibreytur rafrænna skjala**. Í flipanum **Eiginleikar** skal velja línuna sem inniheldur eiginleikann **Egypskur rafrænn reikningur (EG)** og síðan velja viðeigandi atriði. Gögn sem eru flutt inn úr ytri kerfum í þessa Dynamics 365-netþjónustu falla undir [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=512132). Frekari upplýsingar er að finna í hlutanum „Persónuverndartilkynning“ í fylgiskjölum um eiginleika fyrir viðkomandi land.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu](e-invoicing-get-started-service-administration.md)
- [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md)
- [Rafrænir reikningar viðskiptavinar í Egyptalandi](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
