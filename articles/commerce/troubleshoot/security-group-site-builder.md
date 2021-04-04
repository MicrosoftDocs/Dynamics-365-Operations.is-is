---
title: Ekki hægt að skilgreina öryggisflokk fyrir vefsmið Commerce við fyrstu uppsetningu
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar öryggisflokkur Microsoft Azure Active Directory (Azure AD) fyrir vefsmið Commerce birtist ekki sem valkostur þegar þættir rafrænna viðskipta eru stofnaðir í Microsoft Dynamics Lifecycle Services (LCS) við fyrstu uppsetningu á nýjum leigjanda rafrænna viðskipta.
author: Reza-Assadi
manager: AnnBe
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
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585378"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Ekki hægt að skilgreina öryggisflokk fyrir vefsmið Commerce við fyrstu uppsetningu

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar öryggisflokkur Microsoft Azure Active Directory (Azure AD) fyrir vefsmið Commerce birtist ekki sem valkostur þegar þættir rafrænna viðskipta eru stofnaðir í Microsoft Dynamics Lifecycle Services (LCS) við fyrstu uppsetningu á nýjum leigjanda rafrænna viðskipta.

## <a name="description"></a>lýsing

Þegar þættir rafrænna viðskipta eru stofnaðir sem hluti af ferlinu við að setja upp nýjan leigjanda rafrænna viðskipta sem felur í sér þátt Commerce-vefsmiðs, þá birtist ekki öryggisflokkur Azure AD sem valkostur í svarglugganum.

## <a name="resolution"></a>Upplausn

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Útvega svæði fyrir rafræn viðskipti með notanda í réttum leigjanda

1. Opna [Azure-gáttina](https://portal.azure.com/).
1. Undir leigjandanum sem LCS-verkið fyrir svæði rafrænna viðskipta var útvegað fyrir skal fylgja leiðbeiningunum í [Stofna grunnflokk og bæta við meðlimum með Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Farið í [LCS](https://lcs.dynamics.com/) og skráið ykkur inn með reikningi sem deilir leigjandanum sem Azure AD-öryggisflokknum sem var stofnaður rétt í þessu. Reikningurinn verður að hafa aðgang til að skoða Azure AD-öryggisflokkinn.
1. Ljúkið uppsetningarskrefunum til að skilgreina svæði fyrir rafræn viðskipti. Þegar þáttum rafrænna viðskipta er úthlutað ætti öryggisflokkurinn nú að birtast sem valkostur í svarglugganum.

> [!NOTE]
> Til að tryggja að fyllt sé í reitinn í svarglugganum með listanum yfir öryggisflokka þarf að velja **Færa inn** þegar búið er að færa inn heiti Azure AD-öryggisflokksins sem var stofnaður. Leitarniðurstöðurnar munu birta alla Azure AD-öryggisflokkana sem hefjast á leitartextanum og sem notandinn hefur aðgang að. Hægt er að nota styttri leitarlýsingu þannig að leitarniðurstöðurnar verði víðtækari.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna grunnflokk og bæta meðlimum við með Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Uppsetning á nýjum leigjanda rafrænna viðskipta](../deploy-ecommerce-site.md)