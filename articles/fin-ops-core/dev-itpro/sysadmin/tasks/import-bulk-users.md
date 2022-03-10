---
title: Flytja inn notendur úr Azure Active Directory
description: Þetta ferli geta kerfisstjórar notað til að flytja handvirkt inn valda notendur eða inn stóra hópa notenda frá Azure Active Directory.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce8c98add0c6d5fb07b3ba5338037d9a12b1d8e50a2d2039b0231d3d305c9ebe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748289"
---
# <a name="import-users-from-azure-active-directory"></a>Flytja inn notendur úr Azure Active Directory

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Flytja inn val á notendum

Þetta ferli geta kerfisstjórar notað til að flytja inn val notenda úr Azure Active Directory (Azure AD).

1. Notandi verður fluttur inn með núgildandi lotufyrirtæki sem sjálfgefnu fyrirtæki. Breytið núverandi fyrirtæki ef við á áður en notendur eru fluttir inn.
2. Farið í **Kerfisstjórnun > Notendur > Notendur**.
3. Smelltu á **Flytja inn notendur**.
4. Veljið notendur sem á að flytja inn og veljið **Flytja inn notendur**.

Eftir að innflutningi er lokið þarf að úthluta hlutverkum á notendur.

## <a name="import-users-in-bulk"></a>Flytja inn marga notendur í einu

Þetta ferli geta kerfisstjórar notað til að flytja inn stóra hópa notenda frá Azure Active Directory.
Athugið að ekki er hægt að velja notendur þegar valkosturinn Runuinnflutningur er notaður.

## <a name="run-the-import-as-a-batch-job"></a>Keyra innflutning sem runuverk
1. Notandi verður fluttur inn með núgildandi lotufyrirtæki sem sjálfgefnu fyrirtæki. Breytið núverandi fyrirtæki ef við á áður en notendur eru fluttir inn.
2. Farið í **Kerfisstjórnun > Notendur > Notendur**.
3. Smellt er á **Runuinnflutningur**.
4. Stækkaðu hlutann **Keyra í bakgrunni**.
4. Veldu **Já** í reitnum **Runuvinnsla**.
6. Sláið inn eða veldu gildi í reitnum **Runuflokkur**. Þetta skref er valfrjálst.  
7. Veljið **Já** í reitnum **Einka**. Þetta skref er valfrjálst.  
8. Veljið **Já** í svæðinu **Mikilvægt starf**. Þetta skref er valfrjálst.  
9. Í reitnum **Fylgjast með flokki** skal velja valkost.
10. Smellt er á **OK**.

Eftir að innflutningi er lokið þarf að úthluta hlutverkum á notendur.

## <a name="run-in-a-sandbox-environment"></a>Keyrsla í sandkassaumhverfi
1. Veljið **Runuinnflutningur**.
2. Veljið **Í lagi**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]