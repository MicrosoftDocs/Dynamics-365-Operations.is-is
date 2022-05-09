---
title: Rafræn reikningur fyrir Egyptaland
description: Þetta efni veitir upplýsingar sem hjálpa þér að byrja með rafræna reikningagerð fyrir Egyptaland í Microsoft Dynamics 365 Fjármál og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e21c4ce4d676c3194665672a078dc1e3d0492799
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661723"
---
# <a name="electronic-invoicing-for-egypt"></a>Rafræn reikningur fyrir Egyptaland

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Egyptaland. Það leiðir þig í gegnum stillingarskrefin sem eru háð landinu í Regulatory Configuration Service (RCS). Þessi skref eru viðbót við þau skref sem lýst er í [Settu upp rafræna reikningagerð](e-invoicing-set-up-overview.md).

## <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar aðgerðir í þessu efni skaltu ljúka eftirfarandi forsendum:

- Kynntu þér rafræna reikningagerð eins og henni er lýst í [Yfirlit rafrænna reikninga](e-invoicing-service-overview.md).
- Skráðu þig í RCS og settu upp rafræna reikninga. Frekari upplýsingar er hægt að finna í eftirfarandi efni:

    - [Skráðu þig í og settu upp rafræna reikningaþjónustu](e-invoicing-sign-up-install.md)
    - [Setja upp Azure-tilföng fyrir rafrænar reikningsfærslur](e-invoicing-set-up-azure-resources.md)
    - [Setja upp viðbót smáþjónustu í Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    
- Virkjaðu samþættingu milli þín Microsoft Dynamics 365 Fjármál eða Dynamics 365 Supply Chain Management umsókn og rafræna reikningsþjónustu eins og lýst er í [Virkjaðu og settu upp samþættingu við rafræna reikningagerð](e-invoicing-activate-setup-integration.md).
- Búðu til stafrænt vottorðsleyndarmál í Azure Key Vault og settu það upp eins og lýst er í [Viðskiptavinavottorð og leyndarmál](e-invoicing-customer-certificates-secrets.md). Í prófunartilgangi veita egypsk skattyfirvöld ákveðnar prufur af stafrænum vottorðum sem þarf aðeins að nota við prófun og staðfestingu lausnar. Fyrir frekari upplýsingar, farðu á vefsíðu egypsku skattyfirvalda með því að nota hlekkinn sem er að finna í [Egyptian e-invoicing SDK](https://sdk.invoicing.eta.gov.eg/faq/).

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Landssértæk uppsetning fyrir egypska rafræna reikninginn (EG) eiginleikann

Sumir af breytum frá **Egypskur rafrænn reikningur (EG)** eiginleikar rafrænna reikninga eru birtir með sjálfgefnum gildum. Áður en þú innleiðir rafræna reikningseiginleikann í þjónustuumhverfið skaltu skoða sjálfgefna gildin og uppfæra þau eftir þörfum svo þau endurspegli betur rekstur fyrirtækisins.

1. Flytja inn nýjustu útgáfuna af **Egypskur rafrænn reikningur (EG)** Hnattvæðingareiginleiki eins og lýst er í [Flytja inn eiginleika frá alþjóðlegu geymslunni](e-invoicing-import-feature-global-repository.md).
2. Búðu til afrit af innfluttum hnattvæðingareiginleikanum og veldu stillingarþjónustuna þína fyrir hann, eins og lýst er í [Búðu til hnattvæðingareiginleika](e-invoicing-create-new-globalization-feature.md).
3. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
4. Á **Uppsetningar** flipann, í hnitanetinu, veldu **Sölureikningur fenginn** uppsetningu eiginleika.
5. Veljið **Breyta**.
6. Á **Vinnsluleiðsla** flipa, í **Vinnsluleiðsla** kafla, veldu **Skrifaðu undir json skjal fyrir egypska skattayfirvöld**.
7. Í **Færibreytur** kafla, veldu **Nafn skírteinis**, og veldu síðan nafn stafræna vottorðsins sem þú bjóst til.
8. Í **Vinnsluleiðsla** kafla, veldu **Samþætta egypska ETA þjónustu**. Endurtakið þetta skref fyrir tvö tilvik þessarar aðgerðar.
9. Í **Færibreytur** kafla, veldu **Vefslóð vefþjónustu** og **Slóð innskráningarþjónustu**. Skoðaðu síðan vefslóðarfæribreyturnar. Til að fá prófunar- og framleiðsluslóðina skaltu fara á vefsíðu egypska skattyfirvalda með því að nota hlekkinn sem er að finna í [Egyptian e-invoicing SDK](https://sdk.invoicing.eta.gov.eg/faq/).
10. Veljið **Vista** og lokið skjámyndinni.
11. Endurtaktu skref 4 til 10 fyrir **Verkefnareikningur fenginn** uppsetningu eiginleika.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Landssértæk uppsetning fyrir egypska rafræna reikninginn (EG) forritsuppsetningu

Það eru færibreytur sem þarf að setja upp í fjármála- eða framboðskeðjuumhverfi þínu. Þú getur lokið þessari uppsetningu á öðrum hvorum tveimur stöðum:

- Beint í fjármála- eða framboðskeðjuumhverfi þínu. Fyrir frekari upplýsingar, sjá [Setja upp færibreytur rafrænna reikninga](e-invoicing-set-up-parameters.md).
- Í RCS. Í umfangi uppsetningareiginleika rafrænna reikninga geturðu skilgreint allar færibreytur og sett þær síðan beint í fjármála- eða framboðskeðjuumhverfið þitt þegar þú notar rafræna reikningseiginleikann.

Fyrir báða valkostina eru færibreyturnar þær sömu. Ef þú ert að setja upp fyrsta eiginleikann þinn í rafræna reikningsþjónustunni, mælum við með því að þú fylgir þessum skrefum til að setja upp færibreytur í RCS og dreifa þeim síðan í tengda forritið þitt.

> [!NOTE]
> Sumar útgáfur rafrænna reikningaeiginleika gætu innihaldið fyrirframskilgreint sett af forritssértækum færibreytum fyrir fjármál eða birgðakeðjustjórnun. Í þessu tilviki ættir þú að ganga úr skugga um að gögnin séu rétt. Annars skaltu stilla færibreyturnar handvirkt.

1. Finndu afritið af **Egypskur rafrænn reikningur (EG)** Hnattvæðingareiginleiki sem þú bjóst til.
2. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
3. Í flipanum **Uppsetningar** skal velja **Uppsetning forrits**.
4. Í **Tengd forrit** reit, veldu forritið þar sem þú vilt dreifa breytunum.
5. Á **Tegundir rafrænna skjala** síðu, veldu **Bæta við** til að búa til skrá.
6. Í **Nafn töflu** sviði, bæta við **CustInvoiceJour**.
7. Í **Samhengi** reit skaltu bæta við tilvísun í **Samhengi reiknings viðskiptavinar** kortlagningarheiti. Stillingin er **Samhengislíkan viðskiptavinareiknings**.
8. Í **Rafræn skjalakortlagning** reit skaltu bæta við tilvísun í **Reikningur viðskiptavinar** kortlagningarheiti. Stillingin er **Kortlagning reikningslíkana**.
9. Veldu **Vista**.
10. Á **Svartegundir** síðu, veldu **Bæta við**.
11. Í reitinn **Gerð svars** skal færa inn **Svar**.
12. Í **Lýsing** reit, slá inn **Ferlið viðbrögð**.
13. Í reitnum **Staða sendingar** skal velja **Í bið**.
14. Í **Líkanskortlagning** reit, veldu **Innflutningur svarskilaboða**. Stillingin er **Innflutningur svarskilaboða í Egyptalandi (EG)**.
15. Veldu **Vista**.
16. Veljið **Bæta við**.
17. Í **Svartegund** reit, slá inn **Svargögn**.
18. Í **Lýsing** reit, slá inn **Vinnsla viðbragðsgagna**.
19. Í reitnum **Staða sendingar** skal velja **Í bið**.
20. Í **Nafn gagnaeiningar** reit, veldu **SalesInvoiceHeaderV2Entity**.
21. Í **Líkanskortlagning** reit, veldu **Innflutningur svargagna**. Stillingin er **Egyptaland svargagnainnflutningssnið (EG)**.
22. Veljið **Vista** og lokið skjámyndinni.
23. Lokið síðunni.

Til að dreifa eiginleikum í þjónustuumhverfið og uppsetningu forrits í tengda forritið Finance eða Supply Chain Management, sjá [Ljúktu við, birtu og settu í notkun hnattvæðingareiginleika](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Að virkja **Egypskur rafrænn reikningur (EG)** eiginleiki gæti krafist þess að takmörkuð gögn séu send. Þessi gögn innihalda skattskráningarauðkenni stofnunarinnar. Gögnin verða send til þriðju aðila sem hafa fengið heimild skattyfirvalda til að senda rafræna reikninga til skattyfirvalda á fyrirfram skilgreindu sniði sem þarf til samþættingar við vefþjónustu ríkisins. Kerfisstjóri getur virkjað og slökkt á eiginleikanum með því að fara á **Stjórn stofnunarinnar** \> **Uppsetning** \> **Færibreytur rafrænna skjala**. Í flipanum **Eiginleikar** skal velja línuna sem inniheldur eiginleikann **Egypskur rafrænn reikningur (EG)** og síðan velja viðeigandi atriði. Gögn sem eru flutt inn úr ytri kerfum inn í þessa Dynamics 365 netþjónustu eru háð okkar [persónuverndaryfirlýsingu](https://go.microsoft.com/fwlink/?LinkId=512132). Fyrir frekari upplýsingar, sjá hlutann „Persónuverndartilkynning“ í landssértækum eiginleikum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu](e-invoicing-get-started-service-administration.md)
- [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md)
- [Rafrænir reikningar viðskiptavinar í Egyptalandi](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
