---
title: Stjórna notendum og hlutverkum rafrænna viðskipta
description: Þessi grein útskýrir hvernig á að veita notendum aðgang að höfundarumhverfinu fyrir þig Microsoft Dynamics 365 Commerce síða.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 180fc5c0a9c9e247d5bd6ec7f469f313463526df
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279503"
---
# <a name="manage-e-commerce-users-and-roles"></a>Stjórna notendum og hlutverkum rafrænna viðskipta


[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að veita notendum aðgang að höfundarumhverfinu fyrir þig Microsoft Dynamics 365 Commerce síða.

Til að aðstoða við að stjórna aðgangi notenda og veita notendum leyfi til að framkvæma tiltekin verk notar höfundarumhverfi svæðisins öryggishópa sem þú býrð til í Microsoft Azure Active Directory (Azure AD). Þú úthlutar fyrst nýjum eða núverandi öryggishópi frá Azure AD á hvert hlutverk í höfundarumhverfinu. Þú veitir eða afturkallar síðan leyfi fyrir einstaka notendur með því að annaðhvort bæta þeim notendum við viðeigandi öryggishóp eða fjarlægja þá úr öryggishópi.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Yfirlit yfir hlutverk í höfundarumhverfinu

The Dynamics 365 for Commerce höfundarumhverfi styður eftirfarandi hlutverk.

| Hlutverk                 | Lýsing |
|----------------------|-------------|
| Kerfisstjóri | Notendur sem hafa þetta hlutverk hafa öll réttindi fyrir öll verkfæri og fyrir allar einkunnir og umsagnir. Þeir geta einnig búið til svæði. |
| Stjórnandi   | Notendur sem hafa þetta hlutverk hafa öll réttindi fyrir öll verkfæri og RnR í tilteknu vefsvæði. |
| Vefframleiðandi         | Notendur sem hafa þetta hlutverk geta búið til síður, brot og sniðmát, hlaðið upp og stjórnað eignum og auðgað vörur og flokka. |
| Lesari               | Notendur sem hafa þetta hlutverk geta skoðað síður, sniðmát, eignir, brot, skipulag og stillingar en mega ekki gera breytingar. |
| RNR stjórnandi        | Notendur sem hafa þetta hlutverk geta stjórnað afurðaumsögnum. |

## <a name="system-administrator-role"></a>Hlutverk kerfisstjóra

Þegar þú veitir Dynamics 365 Commerce í Microsoft Dynamics LCS (Lifecycle Services) umhverfi ertu beðin/n um að bjóða upp á öryggishóp fyrir hlutverkið **Kerfisstjóri**. Þessu hlutverki er síðan sjálfkrafa beitt á allar síður sem þú býrð til í umhverfinu sem þú ert að stilla. Aðeins er hægt að uppfæra öryggishópinn fyrir þetta hlutverk í LCS. Á síðunni **Vefumsjón** fyrir öll svæði birtist hann sem skrifvarinn og er einungis til upplýsinga.

## <a name="administrator-role"></a>Hlutverk stjórnanda

Þegar þú býrð til nýja síðu í Commerce ertu beðinn um að útvega öryggishóp fyrir hlutverkið **Stjórnandi**. Sjá töfluna fyrr í þessari grein fyrir yfirlit yfir þær heimildir sem þetta hlutverk veitir.

## <a name="add-or-update-security-groups"></a>Bættu við eða uppfærðu öryggishópa

Eftir að vefsvæðið þitt er búið til eru aðeins notendur sem eru í öryggishópunum sem tengjast hlutverkunum **Kerfisstjóri** og **Stjórnandi** geta nálgast höfundarumhverfi fyrir þá síðu. Til að tengja notendur við hlutverkin **Vefframleiðandi**, **RnR stjórnandi** og **Lesari** verður þú að úthluta öryggishópum í þessi hlutverk. Fylgdu þessum skrefum til að bæta öryggishópi við hlutverk eða uppfæra öryggishóp sem nú er úthlutað til hlutverks.

1. Farðu á svæðið sem á að uppfæra.
1. Í **Svæðisstjórnun** opnarðu síðuna **Öryggi**.
1. Veldu hlutverkið sem á að breyta.
1. Bættu öryggishópum við hlutverk, eða fjarlægðu öryggishópa úr hlutverkum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar](add-telemetry.md)

[Hugsanleg leitarvélabestun (SEO) fyrir vefsvæðið þitt](search-engine-optimization-considerations.md)

[Stjórna öryggisreglu fyrir efni (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
