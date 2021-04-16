---
title: Úrræðaleita vandamál sem tengjast meðvitund um lausn
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál sem tengjast meðvitund um lausn.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 86dd8803f7560ea337f2452e9722fe0151466daf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748874"
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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]