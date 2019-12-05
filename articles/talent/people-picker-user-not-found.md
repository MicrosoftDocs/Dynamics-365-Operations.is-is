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
ms.openlocfilehash: a6d916f87ca30aa7405a51841e56ab31bbe31ac8
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832605"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a>Notandi finnst ekki í tengiliðavali í Attract eða Onboard

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Úthreyfing

Vissir gildir notendur í Microsoft Azure Active Directory (Azure AD) fyrir leigjandann birtast ekki þegar leitað er að nafninu í tengiliðavalinu í Dynamics 365 Talent: Attract eða Dynamics 365 Talent: Onboard.

## <a name="cause"></a>Orsök

Ákveðnar gerðir notenda eru ekki studdar sem stendur í Attract og Onboard. Staðfestu að notandinn sé ekki Azure AD Business to Business (B2B) gestanotandi. Upplýsingar um „gerð notanda“ er hægt að finna í Azure Active Directory blaðinu í Azure-gáttinni.

Nánari upplýsingar um Azure B2B er að finna í [Hvað er gestaaðgangur notanda í Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).

Hugsanlegt er að sumir notendur, sem ekki eru B2B-notendur, séu með ófullkominn eiginleika af „gerð notanda“ í hlutnum **Notandi**. Þetta er hægt að staðfesta og laga með Azure AD PowerShell-einingunni. Frekari upplýsingar er að finna í [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).

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
