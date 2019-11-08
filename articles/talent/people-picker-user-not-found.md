---
title: Notandi finnst ekki í tengiliðavali í Attract eða Onboard
description: Þetta efnisatriði útskýrir hvað skuli gera þegar notendur í leigjanda fyrirtækis birtast ekki í tengiliðavali í Dynamics 365 Talent - Attract eða Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d84dd9c22738a1b4fc5edb5331d4aa213b82facb
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551934"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a><span data-ttu-id="189cc-103">Notandi finnst ekki í tengiliðavali í Attract eða Onboard</span><span class="sxs-lookup"><span data-stu-id="189cc-103">User not found in People Picker in Attract or Onboard</span></span>
[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="189cc-104">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="189cc-104">Issue</span></span>

<span data-ttu-id="189cc-105">Vissir gildir notendur í Microsoft Azure Active Directory (Azure AD) fyrir leigjandann birtast ekki þegar leitað er að nafninu í tengiliðavalinu í Dynamics 365 Talent: Attract eða Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="189cc-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in Dynamics 365 Talent: Attract or Dynamics 365 Talent: Onboard.</span></span>

## <a name="cause"></a><span data-ttu-id="189cc-106">Orsök</span><span class="sxs-lookup"><span data-stu-id="189cc-106">Cause</span></span>

<span data-ttu-id="189cc-107">Ákveðnar gerðir notenda eru ekki studdar sem stendur í Attract og Onboard.</span><span class="sxs-lookup"><span data-stu-id="189cc-107">Certain user types are not currently supported in Attract and Onboard.</span></span> <span data-ttu-id="189cc-108">Staðfestu að notandinn sé ekki Azure AD Business to Business (B2B) gestanotandi.</span><span class="sxs-lookup"><span data-stu-id="189cc-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="189cc-109">Upplýsingar um „gerð notanda“ er hægt að finna í Azure Active Directory blaðinu í Azure-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="189cc-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="189cc-110">Nánari upplýsingar um Azure B2B er að finna í [Hvað er gestaaðgangur notanda í Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="189cc-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="189cc-111">Hugsanlegt er að sumir notendur, sem ekki eru B2B-notendur, séu með ófullkominn eiginleika af „gerð notanda“ í hlutnum **Notandi**.</span><span class="sxs-lookup"><span data-stu-id="189cc-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="189cc-112">Þetta er hægt að staðfesta og laga með Azure AD PowerShell-einingunni.</span><span class="sxs-lookup"><span data-stu-id="189cc-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="189cc-113">Frekari upplýsingar er að finna í [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="189cc-113">For more information, see [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="189cc-114">Upplausn</span><span class="sxs-lookup"><span data-stu-id="189cc-114">Resolution</span></span>

<span data-ttu-id="189cc-115">Til að ljúka eftirfarandi skrefum til að leysa málið þarftu að hafa heimildir „altæks stjórnanda“ í Azure Active Directory leigjandanum eða heimildir fyrir **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="189cc-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="189cc-116">Til að staðfesta „gerð notanda“ fyrir notanda sem á hlut að máli.</span><span class="sxs-lookup"><span data-stu-id="189cc-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="189cc-117">Skipunin skilar eftirfarandi upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="189cc-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="189cc-118">Taktu eftir eiginleikanum **UserType** fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="189cc-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="189cc-119">Ef **UserType** er autt, t.d. ekki „meðlimur“ eða „gestur“, skal uppfæra **UserType** með því að nota eftirfarandi skipun.</span><span class="sxs-lookup"><span data-stu-id="189cc-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
