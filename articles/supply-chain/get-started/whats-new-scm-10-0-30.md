---
title: Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.30. (nóvember 2022)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.30.
author: kamaybac
ms.date: 11/07/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 20674ebd9d49b077371998f53d2b22c74f888fc6
ms.sourcegitcommit: 613be2f35e600ae1a1fa7ea2ae30e78984ca398a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748465"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10030-november-2022"></a>Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.30. (nóvember 2022)

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.30. Þessi útgáfa er með smíðarnúmer 10.0.1362 og er í boði á eftirfarandi áætlun:

- **Forskoðun útgáfu:** september 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Október 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Nóvember 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þessa grein til að hafa með eiginleika sem var bætt við smíðina eftir að þessi grein var upphaflega birt.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Birgða- og vörustjórnun | [Fylgjast með óbundnu fráteknu magni innan úthlutunar](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/track-soft-reserved-quantities-within-allocations) | [Inventory Visibility birgðaúthlutun](../inventory/inventory-visibility-allocation.md) |  Gert virkt með [þjónustustillingu](../inventory/inventory-visibility-configuration.md) |
| Framleiðsla | [Fylgjast með búnaði með Sensor Data Intelligence](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Sensor Data Intelligence heimasíða](../sensor-data-intelligence/sdi-home-page.md) | Stjórnun eiginleika:<br>*(Forútgáfa) Gagnagreindarskynjari* |
| Vöruhúsakerfi | [Fjölþrepa hjáleiðir fyrir fartækjaforrit Warehouse Management](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/multi-level-detours-warehouse-management-mobile-app) | [Skilgreina hjáleiðir fyrir skref í valmyndaratriðum fartækis](../warehousing/warehouse-app-detours.md) | Stjórnun eiginleika:<br>*Fjölþrepa hjáleiðir fyrir fartækjaforrit Warehouse Management* |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef á að kveikja eða slökkva á einhverjum þessara eiginleika þarf að gera það í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Framleiðslustýring | Síðan „Lagerupplýsingar í framleiðslupöntunum til losunar“ | Þessi eiginleiki bætir við dálki fyrir lagerbirgðir fyrir línuatriðið í línuhlutanum á síðunni **Framleiðslupantanir til losunar**. |
| Flutningsstjórnun | Úthluta sendingum á tengda leiðarhluta | Þessi eiginleiki gerir kerfinu kleift að skipta niður sendingarkostnaði farms á nákvæmari hátt, þ.m.t. fyrir hleðslur með mörgum sendingum sem afhentar eru á ýmsum áfangastöðum leiðarhluta á einni leið. Hann úthlutar hverri sendingu á þann leiðarhluta sem passar best samkvæmt heimilisföngum áfangastaða fyrir sendingu og leiðarhluta. Eiginleikinn reiknar síðan sendingarkostnað farms sem hlutfall af heildarsendingarkostnaði hleðslunnar samkvæmt hlutfallslegri þyngd, rúmmáli, magni og lengd ferðar fyrir sendinguna. Þessi eiginleiki á aðeins við um sendingar sem eru meðhöndlaðar með flutningsstjórnunareiningunni. |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir fjármála- og rekstrarforrit

Microsoft Dynamics 365 Supply Chain Management 10.0.30 inniheldur verkvangsuppfærslur. Frekari upplýsingar má finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.30 á fjármála- og rekstrarforritum (október 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af útgáfu 10.0.30, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2022 útgáfubylgja 2 áætlun](/dynamics365-release-plan/2022wave2/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

Greinin [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í greininni [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
