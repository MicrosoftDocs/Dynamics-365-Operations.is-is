---
title: Virkja Azure Active Directory sannvottun fyrir POS innskráningu
description: Þetta efni útskýrir hvernig á að stilla innskráningarupplifunina fyrir Microsoft Dynamics 365 Commerce sölustað (POS) þannig að hún noti Azure Active Directory auðkenningu.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d6073a04814adf8237b4caa952b31b011f4b34bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982741"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>Virkja Azure Active Directory sannvottun fyrir POS innskráningu
[!include [banner](includes/banner.md)]


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
> 
> Sem stendur styður aðgerðin **Hnekking stjórnanda** ekki Azure AD sem sannvottunaraðferð. Krafist er notandakennis og aðgangsorðs jafnvel þótt Azure AD er skilgreint sem sannvottunaraðferðin fyrir innskráningu sölustaðar.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Tengja við Azure AD reikning hjá starfsmanni

Áður en starfsmaður verslunar getur notað Azure AD til að skrá sig inn í POS forritið verður Azure AD-reikningurinn að vera tengdur þeim starfsmanni.

Til að tengja Azure AD-reikning við starfsmann skaltu fylgja þessum skrefum.

1. Farðu í **Retail og Commerce** \> **Starfsmenn** \> **Starfsfólk**.
1. Opnaðu upplýsingasíðuna fyrir starfskraft.
1. Í aðgerðarúðunni á flipanum **Commerce** í flokknum **Ytra kenni** skal velja **Tengja fyrirliggjandi kenni**.
1. Í valmyndinni **Nota fyrirliggjandi ytra kenni** velurðu **Leita með tölvupósti**, slærð inn Azure AD-netfangið og veldu síðan **Leita**.
1. Veldu Azure AD-reikninginn sem er skilað og veldu síðan **Í lagi**.

Reitirnir **Samheiti**, **UPN** og **Ytra undirkennimerki** á flipanum **Commerce** á upplýsingasíðu starfsmannsins verður fylltur út.

> [!NOTE]
> Þegar skrá starfsmanns er uppfærð, til dæmis ef nýr Azure AD-reikningur er tengdur við, aðgangsorði er breytt eða aðsetursbók starfsmanns er uppfærð, er mælt með því að keyra dreifingaráætlun **1060** (**Starfsfólk**) til að samstilla nýjustu upplýsingar um starfsfólk við rásina. Þannig getur forrit sölustaðar sótt réttar upplýsingar fyrir sannvottun notanda og athugun heimildar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp aukna innskráningarvirkni fyrir MPOS og Cloud POS](extended-logon.md)

[Stofna virknireglu fyrir smásölu](retail-functionality-profile.md)

[Skilgreina starfsmann](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)


[!INCLUDE[footer-include](../includes/footer-banner.md)]