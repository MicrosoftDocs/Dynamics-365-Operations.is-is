---
title: Úrræðaleita vandamál sem tengjast meðvitund um lausn
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál sem tengjast meðvitund um lausn.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 79b2920b80ce4a8b419c2a146e15babc061cf64d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683565"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Úrræðaleita vandamál sem tengjast meðvitund um lausn

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem tengjast meðvitund um lausn.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="error-on-the-dual-write-page"></a>Villa á síðunni Tvíritun

Á síðunni **Tvöfalt skrif** gætirðu fengið villuboð sem líkjast eftirfarandi dæmi:

*Einingin sem heitir 'msdyn\_dualwriteentitymap' með namemapping='Logical' fannst ekki í MetadataCache.*

Til að laga málið skaltu ganga úr skugga um að tvískipt kjarnalausnin sé sett upp í Dataverse. Tvískipt kjarnalausnin er forsenda fyrir vitund um lausn.
