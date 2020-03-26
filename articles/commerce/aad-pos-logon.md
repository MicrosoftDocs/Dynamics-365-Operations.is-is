---
title: Virkja Azure Active Directory sannvottun fyrir POS innskráningu
description: Þetta efni útskýrir hvernig á að stilla innskráningarupplifunina fyrir Microsoft Dynamics 365 Commerce sölustað (POS) þannig að hún noti Azure Active Directory auðkenningu.
author: boycezhu
manager: annbe
ms.date: 03/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: f030e8382627191dd32d855e15432fc85dca4bbd
ms.sourcegitcommit: 1789a78de1cbeac19d96767812df653a191c67e9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/05/2020
ms.locfileid: "3100381"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>Virkja Azure Active Directory sannvottun fyrir POS innskráningu
[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Margir viðskiptavinir sem nota Microsoft Dynamics 365 Commerce nota einnig aðra Microsoft-skýjaþjónustu og þeir gætu notað Azure Active Directory (Azure AD) til að stjórna notendaskilríkjum fyrir þessa þjónustu. Í þeim tilvikum gætu viðskiptavinirnir viljað nota sama Azure AD reikninginn yfir forrit. Þetta efni útskýrir hvernig á að stilla innskráningarupplifun sölustaðar (POS) í Commerce til að nota Azure AD auðkenningu.

## <a name="configure-azure-ad-authentication"></a>Skilgreina Azure AD sannvottun

Til að gera Azure AD tiltækt sem sannvottunaraðferð fyrir POS innskráningu fyrir verslun, verður þú að skilgreina stillingarnar á virkni sniðs verslunarinnar og nota þær stillingar á POS viðskiptavini.

Til að skilgreina virknireglu skal fylgja þessum skrefum.

1. Fara í **Retail og Commerce** \> **Uppsetning rásar** \> **Uppsetning sölustaðar** \> **Forstillingar sölustaðar** \> **Virknireglur**.
1. Veldu virkniregluna sem á að breyta.
1. Á flýtiflipanum **Aðgerðir**, í hlutanum **Innskráning starfsmanna í POS**, breytirðu gildi í reitnum **Sannvottunaraðferð innskráningar** úr **Persónuskilríki og lykilorð** í **Azure Active Directory**.

Sjálfgefið eru allar virknireglur nota **Persónuskilríki og lykilorð** sem POS sannvottunaraðferð. Þess vegna verður þú að breyta gildi í reitnum **Sannvottunaraðferð innskráningar** ef þú vilt nota Azure AD. Þessi breyting hefur áhrif á sérhverja smásöluverslun sem er tengd við valdar virkniforstillingar.

Fylgdu þessum skrefum til að beita stillingunum til POS viðskiptavina.

1. Farðu í **Retail og Commerce** \> **Upplýsingatækni í Retail og Commerce** \> **Dreifingaráætlun**.
1. Keyrðu dreifingaráætlunina **1070** (**Stilling rásar**).

> [!NOTE]
> Azure AD sannvottun krefst internettengingar. Það virkar ekki þegar POS er í stillingu án nettengingar.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Tengja við Azure AD reikning hjá starfsmanni

Áður en starfsmaður verslunar getur notað Azure AD til að skrá sig inn í POS forritið verður Azure AD-reikningurinn að vera tengdur þeim starfsmanni.

Til að tengja Azure AD-reikning við starfsmann skaltu fylgja þessum skrefum.

1. Farðu í **Retail og Commerce** \> **Starfsmenn** \> **Starfsfólk**.
1. Opnaðu upplýsingasíðuna fyrir starfskraft.
1. Í aðgerðarúðunni á flipanum **Commerce** í flokknum **Ytra kenni** skal velja **Tengja fyrirliggjandi kenni**.
1. Í valmyndinni **Nota fyrirliggjandi ytra kenni** velurðu **Leita með tölvupósti**, slærð inn Azure AD-netfangið og veldu síðan **Leita**.
1. Veldu Azure AD-reikninginn sem er skilað og veldu síðan **Í lagi**.

Reitirnir **Samheiti**, **UPN** og **Ytra undirkennimerki** á flipanum **Commerce** á upplýsingasíðu starfsmannsins verður fylltur út.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp aukna innskráningarvirkni fyrir MPOS og sölukerfi í skýinu](extended-logon.md)

[Stofna virknireglu fyrir smásölu](retail-functionality-profile.md)

[Skilgreina starfsmann](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
