---
title: Setja upp B2C-leigjanda í Commerce
description: Þessi grein lýsir því hvernig á að setja upp Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C) fyrir auðkenningu notendasíðu í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785138"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Setja upp B2C-leigjanda í Commerce

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C) fyrir auðkenningu notendasíðu í Dynamics 365 Commerce.

Dynamics 365 Commerce notar Azure AD B2C til að styðja persónuskilríki notenda og staðfesting. Notandi getur skráð sig, skráð sig inn og endurstillt lykilorð sitt í gegnum þessa flæði. Azure AD B2C geymir viðkvæmar sannvottunarupplýsingar notanda, svo sem notandanafn og lykilorð. Notendaskráin í leigjanda B2C mun geyma annað hvort skrá yfir B2C staðbundna reikninga eða skrá yfir fyrirtækjasamfélag B2C. Þessar B2C skrár munu tengjast aftur viðskiptamannaskránni í Commerce-umhverfi.

> [!WARNING] 
> Azure AD B2C mun hætta í gamla (eldra) notandaflæði frá 1. ágúst, 2021. Því ætti að áforma að yfirfæra notandaflæðin í nýju ráðlögðu útgáfuna. Nýja útgáfan býður upp á jafngilda eiginleika og nýja eiginleika.. Einingasafnið fyrir Commerce-útgáfu 10.0.15 eða nýrri ætti að nota með ráðlögðum B2C-notandaflæðum. Frekari upplýsingar eru í [Notandaflæði í Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Matsumhverfi Commerce koma með fyrirframhlöðnum Azure AD B2C-leigjanda fyrir sýnikennslu. Ekki er krafist þess að hlaða eigin Azure AD B2C-leigjanda með neðangreindum skrefum fyrir matsumhverfi.

> [!TIP]
> Þú getur verndað notendur síðunnar enn frekar og aukið öryggi Azure AD B2C-leigjenda þinna með Azure AD auðkennisvörn og skilyrtum aðgangi. Til að fara yfir möguleikana sem eru í boði fyrir Azure AD B2C Premium P1 og Premium P2 leigjendur skal skoða [Auðkennisvörn og skilyrtur aðgangur fyrir Azure AD B2C](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Forkröfur Dynamics-umhverfis

Áður en hafist er handa skal ganga úr skugga um að Dynamics 365 Commerce umhverfi þitt og netverslunarrás séu stillt á viðeigandi hátt með því að uppfylla eftirfarandi forsendur.

- Stilla gildið **AllowAnonymousAccess** fyrir aðgerðir sölustaðar á „1“ í Commerce-höfuðstöðvum:
    1. Fara í **POS-aðgerðir**.
    1. Í aðgerðanetinu er hægrismellt og valið **Sérstilla**.
    1. Veljið **Bæta við reit**.
    1. Á listanum yfir tiltæka dálka skal velja **AllowAnonymousAccess** dálkinn til að bæta honum við.
    1. Veldu **Uppfæra**.
    1. Fyrir aðgerðina **612** „Bæta við viðskiptavini“ skal breyta **AllowAnonymousAccess** í „1“.
    1. Keyrðu **1090 (Skrár)** verkið.
- Stillið eigind **Handvirkt** fyrir númeraraðarviðskiptavinalykilinn á **Nei** í Commerce-höfuðstöðvum:
    1. Opnið **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Færibreytur viðskiptakrafna**.
    1. Velja **númeraraðir**.
    1. Tvísmelltu á gildið **Kóði númeraraðar** í **Viðskiptavinalykill**.
    1. Á flýtiflipanum **Almennt** í númeraröðinni skal stilla **Handvirkt** á **Nei**.

Eftir að Dynamics 365 Commerce umhverfið hefur verið tekið í notkun er einnig mælt með því [Frumstilla grunngögn](enable-configure-retail-functionality.md) í umhverfinu.

## <a name="next-steps"></a>Næstu skref

Til að halda áfram ferlinu við að setja upp B2C leigjanda í Commerce, haltu áfram til [Búðu til eða tengdu við núverandi Azure AD B2C leigjandi í Azure gáttinni](create-link-aad-b2c-tenant.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Búðu til eða tengdu við núverandi Azure AD B2C leigjandi í Azure gáttinni](create-link-aad-b2c-tenant.md)

[Stofna B2C forrit](create-b2c-app.md)

[Stofna notandaflæðisstefnu](create-user-flow-policies.md)

[Bæta við kennitöluveitendum (valfrjálst)](add-social-identity-providers.md)

[Uppfærðu höfuðstöðvar viðskipta með nýju Azure AD B2C upplýsingar](update-hq-aad-b2c-info.md)

[Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði](config-b2c-tenant-site-builder.md)

[Frekari B2C upplýsingar](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
