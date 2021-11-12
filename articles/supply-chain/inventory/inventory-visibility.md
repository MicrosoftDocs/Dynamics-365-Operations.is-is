---
title: Yfirlit viðbótar fyrir sýnileika birgða
description: Í þessu efnisatriði er útskýrt hvað birgðasýnileiki er og eiginleikum hans er lýst.
author: yufeihuang
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea1d8c1b0e8c996ead8461005960fa756ce6ca7
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678910"
---
# <a name="inventory-visibility-add-in-overview"></a>Yfirlit viðbótar fyrir sýnileika birgða

[!include [banner](../includes/banner.md)]

Innbót birgðasýnileika (einnig vísað í hana sem *Birgðasýnileiki*) er sjálfstæð og einstaklega sveigjanleg örþjónusta sem býður upp á rakningu lagerbirgða í rauntíma. Þar af leiðandi býður hún upp á altækt yfirlit yfir birgðir.

Ytri kerfi nálgast þjónustuna í gegnum RESTful API. Á þann hátt geta þau annaðhvort sent fyrirspurn um lagerupplýsingar vegna tiltekinna víddasafna eða gert breytingar á birgðunum í öðrum sérstilltum gagnagjöfum.

Sem örþjónusta sem er smíðuð í Microsoft Dataverse, býður birgðasýnileiki upp á stækkunarhæfni. Þú getur notað Power Apps til að smíða forrit. Þú getur einnig notað Power BI til að bjóða upp á sérstillta aðgerð sem uppfyllir viðskiptakröfur þínar.

Þú getur samþætt birgðasýnileika við mörg kerfi þriðja aðila með því að setja upp valkosti skilgreiningar fyrir staðlaðar birgðavíddir og setja upp færslugerðir. Birgðasýnileiki styður einnig sérstilla stækkunarhæfni í gegnum stillanlegt reiknað magn.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Samþætting birgðasýnileika við Dynamics 365 Supply Chain Management

Samþætta lausnin sækir birgðagögn úr Dynamics 365 Supply Chain Management og heldur samfellt áfram að rekja birgðabreytingar. Frekari upplýsingar er að finna í [Setja upp birgðasýnileika](inventory-visibility-setup.md) og [Stilla birgðasýnileika](inventory-visibility-configuration.md).

## <a name="get-a-global-view-of-inventory"></a>Fá altækt yfirlit yfir birgðir

Samþætta lausnin gerir þér kleift að skilgreina þína eigin gagnagjafa og gert birgðagögn miðlæg. Frekari upplýsingar er að finna í [Stilla birgðasýnileika](inventory-visibility-configuration.md).

Tvær aðferðir eru til við að skoða birgðirnar þínar:

- Sendu inn fyrirspurn í gegnum API með miklum afköstum. Þetta API getur skilað birgðagögnum í nánast rauntíma beint úr tilviki skyndiminnis. Þú getur fundið samninga og sýnishorn í [Almennt API birgðasýnileika](inventory-visibility-api.md).
- Skoðaðu hráan lagerlistann. Þessi listi er samstilltur reglulega úr tilviki skyndiminnis og er sýnilegur í Dataverse. Frekari upplýsingar er að finna í [Forrit birgðasýnileika](inventory-visibility-power-platform.md).

## <a name="soft-reservations"></a>Mjúkar frátekningar

Mjúk frátekning á við þegar fyrirtæki verður að taka frá tiltekið magn af afurðum til að styðja við t.d. uppfyllingu sölupöntunar sem kemur í veg fyrir of mikla sölu. Þegar sölupöntun er stofnuð og staðfest í Supply Chain Management eða öðrum kerfum pantanastjórnunar er beiðni um að taka frá magnið send til birgðasýnileika. Birgðasýnileiki gerir þér kleift að taka frá afurðir sem hafa upplýsingar um vídd og tilteknar birgðafærslugerðir. (Frekari upplýsingar er að finna í [Forrit birgðasýnileika](inventory-visibility-power-platform.md).) Eftir að magnið hefur verið tekið frá er frátekningarkenni skilað til baka. Þú getur notað þetta frátekningarkenni til að tengja aftur við upprunalegu pöntunina í Supply Chain Management fyrir birgðakeðjur eða öðrum pöntunarstjórnunarkerfum eða önnur kerfi pantanastjórnunar.

Virknin er hönnuð þannig að frátekning í birgðasýnileika breytir ekki heildarmagninu. Þess í stað flaggar hún aðeins fráteknu magni. (Sem er ástæðan fyrir því að hún er kölluð *mjúk frátekning*.) Hægt er að mótbóka magnið þegar afurðirnar eru notaðar í Supply Chain Management eða kerfi þriðja aðila með því að kalla aftur á API til að draga frá magn og uppfæra heildarmagnið í birgðasýnileika. Frekari upplýsingar er að finna í [Frátekningar birgðasýnileika](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
