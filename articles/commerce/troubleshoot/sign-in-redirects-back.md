---
title: Tengill innskráningar framsendir aftur á svæði rafrænna viðskipta
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar innskráningartengill vísar aftur á netverslunarsíðuna í stað þess að fara á innskráningarsíðuna.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 0bc9c0afbd6b349d8565f9eea56e207eae179f65
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291456"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Tengill innskráningar framsendir aftur á svæði rafrænna viðskipta

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar innskráningartengill vísar aftur á netverslunarsíðuna í stað þess að fara á innskráningarsíðuna.

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
