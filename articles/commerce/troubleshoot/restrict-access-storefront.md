---
title: Takmarka aðgang að netverslun við prófun eða þróun
description: Þetta efnisatriði útskýrir hvernig á að takmarka aðgang að Microsoft Dynamics 365 Commerce-netverslun á meðan innri prófun eða þróun er í gangi.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f5cba6b7ff3aa65441c932e72fa458bda0d0fc69
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801532"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Takmarka aðgang að netverslun við prófun eða þróun

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að takmarka aðgang að Microsoft Dynamics 365 Commerce-netverslun á meðan innri prófun eða þróun er í gangi.

## <a name="description"></a>lýsing

Á meðan innri prófun eða virk þróun er í gangi gæti verið sniðugt að takmarka aðgang að svæðinu til að koma í veg fyrir aðgang ytri notenda að virkum netverslunarsíðum.

## <a name="resolution"></a>Upplausn

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Setja upp Azure AD B2C með því að nota hefðbundið notandastreymi

Upplýsingar um hvernig á að skilgreina Azure Active Directory B2C (Azure AD B2C) fyrir svæði rafrænna viðskipta er að finna í [Setja upp B2C-leigjanda í Commerce](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Takmarka aðgang notanda að síðum netverslunar og loka á stofnun nýrra notenda

Til að takmarka aðgang að síðum netverslunar í vefsmið Commerce skal fylgja þessum skrefum.

1. Opnið svæðið ykkar.
1. Veljið **Síður** og veljið því næst síðuna þar sem á að takmarka aðgang notanda.
1. Veljið hólf einingar eða síðubrots og veljið því næst **Breyta**.
1. Í eiginleikaglugganum skal velja **Krefst innskráningar?** og því næst velja **Ljúka við breytingar**.
1. Velja **Birta**.

Til að loka á stofnun nýrra notenda í Azure AD skal fylgja þessum skrefum.

1. Opna [Azure-gáttina](https://portal.azure.com/).
1. Veljið forrit Azure AD B2C sem var búið til fyrir aðgang að svæðinu.
1. Í vinstri flettingunni skal velja **Notandastreymi**.
1. Efst á síðunni **Notandastreymi** skal velja **Nýtt notandastreymi**.
1. Á síðunni **Velja gerð notandastreymis** skal velja **Forskoða**.
1. Fyrir miðju síðunnar skal velja **Skrá inn v2**. Síðan skal fylgja skrefunum í [Setja upp B2C-leigjanda í Commerce](../set-up-b2c-tenant.md) til að skilgreina streymið sem hefðbundið notandastreymi svæðisins fyrir Azure AD B2C á meðan prófun og þróun er í gangi.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2C-leigjanda í Commerce](../set-up-b2c-tenant.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](../custom-pages-user-logins.md)
