---
title: Ekki hægt að skilgreina öryggisflokk fyrir vefsmið Commerce við fyrstu uppsetningu
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar Microsoft Azure Active Directory (Azure AD) öryggishópur fyrir verslunarsíðugerð birtist ekki sem valkostur þegar þú býrð til rafræna viðskiptahluta í Microsoft Dynamics Lifecycle Services (LCS) við upphaflega dreifingu nýs rafrænnar viðskiptaleiganda.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 7098c853c262fd7e0d48231634b232eef71c2b8d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292001"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Ekki hægt að skilgreina öryggisflokk fyrir vefsmið Commerce við fyrstu uppsetningu

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar Microsoft Azure Active Directory (Azure AD) öryggishópur fyrir verslunarsíðugerð birtist ekki sem valkostur þegar þú býrð til rafræna viðskiptahluta í Microsoft Dynamics Lifecycle Services (LCS) við upphaflega dreifingu nýs rafrænnar viðskiptaleiganda.

## <a name="description"></a>lýsing

Þegar þættir rafrænna viðskipta eru stofnaðir sem hluti af ferlinu við að setja upp nýjan leigjanda rafrænna viðskipta sem felur í sér þátt Commerce-vefsmiðs, þá birtist ekki öryggisflokkur Azure AD sem valkostur í svarglugganum.

## <a name="resolution"></a>Upplausn

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Útvega svæði fyrir rafræn viðskipti með notanda í réttum leigjanda

1. Opna [Azure-gáttina](https://portal.azure.com/).
1. Undir leigjandanum sem LCS-verkið fyrir svæði rafrænna viðskipta var útvegað fyrir skal fylgja leiðbeiningunum í [Stofna grunnflokk og bæta við meðlimum með Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Farið í [LCS](https://lcs.dynamics.com/) og skráið ykkur inn með reikningi sem deilir leigjandanum sem Azure AD-öryggisflokknum sem var stofnaður rétt í þessu. Reikningurinn verður að hafa aðgang til að skoða Azure AD-öryggisflokkinn.
1. Ljúkið uppsetningarskrefunum til að skilgreina svæði fyrir rafræn viðskipti. Þegar þáttum rafrænna viðskipta er úthlutað ætti öryggisflokkurinn nú að birtast sem valkostur í svarglugganum.

> [!NOTE]
> Til að tryggja að fyllt sé í reitinn í svarglugganum með listanum yfir öryggisflokka þarf að velja **Færa inn** þegar búið er að færa inn heiti Azure AD-öryggisflokksins sem var stofnaður. Leitarniðurstöðurnar munu birta alla Azure AD-öryggisflokkana sem hefjast á leitartextanum og sem notandinn hefur aðgang að. Hægt er að nota styttri leitarlýsingu þannig að leitarniðurstöðurnar verði víðtækari.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna grunnflokk og bæta meðlimum við með Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Uppsetning á nýjum leigjanda rafrænna viðskipta](../deploy-ecommerce-site.md)
