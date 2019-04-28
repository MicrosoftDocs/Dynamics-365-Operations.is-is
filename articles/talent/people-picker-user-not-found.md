---
title: Notandi finnst ekki í tengiliðavali í Attract eða Onboard
description: Þetta efnisatriði útskýrir hvað skuli gera þegar notendur í leigjanda fyrirtækis birtast ekki í tengiliðavali í Dynamics 365 for Talent Attract eða Onboard forritum.
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
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "859506"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Azure Active Directory-notendur fundust ekki í tengiliðavali

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Úthreyfing

Vissir gildir notendur í Microsoft Azure Active Directory (Azure AD) fyrir leigjandann birtast ekki þegar leitað er að nafninu í tengiliðavalinu í Dynamics 365 for Talent Attract eða Onboard forritunum.

## <a name="cause"></a>Orsök

Ákveðnar gerðir notenda eru ekki studdar sem stendur í forritum Attract og Onboard. Staðfestu að notandinn sé ekki Azure AD Business to Business (B2B) gestanotandi. Upplýsingar um „gerð notanda“ er hægt að finna í Azure Active Directory blaðinu í Azure-gáttinni.

Nánari upplýsingar um Azure B2B er að finna í [Hvað er gestaaðgangur notanda í Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).

Hugsanlegt er að sumir notendur, sem ekki eru B2B-notendur, séu með ófullkominn eiginleika af „gerð notanda“ í hlutnum **Notandi**. Þetta er hægt að staðfesta og laga með Azure AD PowerShell-einingunni. Frekari upplýsingar er að finna í [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>Upplausn

Til að ljúka eftirfarandi skrefum til að leysa málið þarftu að hafa heimildir „altæks stjórnanda“ í Azure Active Directory leigjandanum eða heimildir fyrir **User.ReadWrite.All**.

Til að staðfesta „gerð notanda“ fyrir notanda sem á hlut að máli.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Skipunin skilar eftirfarandi upplýsingum.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Taktu eftir eiginleikanum **UserType** fyrir notandann. Ef **UserType** er autt, t.d. ekki „meðlimur“ eða „gestur“, skal uppfæra **UserType** með því að nota eftirfarandi skipun.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
