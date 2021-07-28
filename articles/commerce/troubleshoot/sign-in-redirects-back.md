---
title: Tengill innskráningar framsendir aftur á svæði rafrænna viðskipta
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar innskráningartengill framsendir aftur á svæði rafrænna viðskipta í stað þess að fara á innskráningarsíðuna.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: e83b381e73d28dce0a438a37d5f8ed23b4957adf
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350379"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Tengill innskráningar framsendir aftur á svæði rafrænna viðskipta

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar innskráningartengill framsendir aftur á svæði rafrænna viðskipta í stað þess að fara á innskráningarsíðuna.

## <a name="description"></a>lýsing

Þegar búið er að skilgreina nýjan Microsoft Azure Active Directory B2C-leigjanda (Azure AD B2C) í vefsmið Commerce eru notendur sem velja tengilinn **Innskráning** framsendir á aðallendingarsíðu rafrænna viðskipta án þess að fara á innskráningarsíðuna.

## <a name="resolution"></a>Upplausn

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Staðfesta að svarvefslóð sé rétt skilgreind í forriti Azure AD B2C

Til að staðfesta að svarvefslóð sé rétt skilgreind í forriti Azure AD B2C skal fylgja þessum skrefum.

1. Opna [Azure-gáttina](https://portal.azure.com/).
1. Veljið forrit Azure AD B2C sem var búið til fyrir aðgang að svæðinu.
1. Veljið forritið sem var búið til við uppsetningu Azure AD B2C uppsetningu.
1. Undir **Svarslóð** skal ganga úr skugga um listinn innihaldi færslur fyrir bæði vefslóð svæðisins og vefslóð sem rafræn viðskipti mynda eins og sýnt er í dæminu á eftirfarandi skýringarmynd.

    ![Færslur svarslóðar Azure AD B2C.](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Bæði vefslóð svæðisins og mynduð vefslóð rafrænna viðskipta verða að vera á gildu sniði vefslóðar sem inniheldur ekki línubil fyrir framan og aftan.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skrá vefforrit í Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[Setja upp B2C-leigjanda í Commerce](../set-up-b2c-tenant.md)