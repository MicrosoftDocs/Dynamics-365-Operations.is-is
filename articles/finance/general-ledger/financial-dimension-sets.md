---
title: Fjárhagsvíddasamstæður
description: Þessi grein lýsir fjárhagsvíddarsettum og veitir nokkur ráð til að hagræða notkun þeirra.
author: yukonpeegs
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3d4c15504b2ad128493e1bafa36aed271c2ab6dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864282"
---
# <a name="financial-dimension-sets"></a>Fjárhagsvíddasamstæður

[!include [banner](../includes/banner.md)]

Þessi grein lýsir fjárhagsvíddarsettum og veitir nokkur ráð til að hagræða notkun þeirra.

Víddasamstæða er raðaður listi yfir fjárhagsvíddir sem hægt er að nota til að taka saman fjárhagsgögn á hátt sem notandi skilgreinir. Helsta notkun víddasamstæða felst í að skilgreina prófjöfnuð.

Eina staðlaða víddasamstæðan er sú sem inniheldur eingöngu aðallykilinn.

Síðan **Fjárhagsvíddasamstæður** er notuð til að búa til og stjórna fjárhagsvíddasamstæðum.

## <a name="dimension-set-balances"></a>Stöður víddasamstæðu

Víddasamstæða sem verið með stöður sem byggja á fjárhagsvíddum hennar. Stöðurnar eru til í fjárhag og byggja á skilgreningu víddasamstæðunnar. Stöðurnar eru teknar saman úr fjárhagsgögnum til að stuðla að betri afköstum þegar þær eru sóttar (t.d. þegar prófjöfnuður er búinn til).

## <a name="create-balances"></a>Stofna stöður

Notið hnappinn **Stofna stöður** til að frumstilla stöðurnar fyrir víddasamstæðu sem er ekki komin með stöður.

> [!NOTE]
> Mælt er með að takmarka fjölda víddasamstæða sem eru með stöður vegna þess að uppfærslur á stöðum hefur áhrif á allar aðgerðir fjárhagsbókunar.

## <a name="update-balances"></a>Uppfæra stöður

Notið hnappinn **Uppfæra stöður** til að hafa með nýjustu aðgerð fjárhagsbókunar í stöðunum. Uppfærslur á stöðum eru léttar aðgerðir. Þær mega aðeins vinna úr aðgerð fjárhagsbókunar sem hefur átt sér stað frá síðustu uppfærslu.

> [!NOTE]
> Birting prófjöfnuðar þvingar fram uppfærslu til að tryggja að stöðurnar sem eru sýndar séu núgildandi. Íhugið að nota endurtekna runuvinnslu þannig að uppfærslur á mest notuðu víddasamstæðunum gangi hratt fyrir sig. Þannig stuðlar þú að því að lágmarka tímann sem notendur prófjöfnuðar þurfa að bíða.

## <a name="rebuild-balances"></a>Endurbyggja stöður

Notið hnappinn **Endurbyggja stöður** til að stofna stöðurnar aftur frá grunni. Þannig tryggir þú að þær stemmi við gögnin í fjárhagnum. Endurbygging á stöðum krefst mikillar úrvinnslu og ætti oftast ekki að þurfa.

> [!NOTE]
> Ef aðstæður koma upp sem krefjast endurbyggingar á stöðum með reglulegu millibili mælum við með að þú hafir samband við notendaþjónustu. Notendaþjónustan getur hjálpað þér að finna út hvers vegna stöður stemma ekki við gögn í fjárhag.

## <a name="clear-balances"></a>Hreinsa stöður

Notið hnappinn **Hreinsa stöður** til að fjarlægja stöðurnar og stöðva frekari uppfærslur. Víddasamstæðan hefur ekki lengur áhrif á aðgerðir fjárhagsbókunar.

## <a name="delete-a-dimension-set"></a>Víddasamstæðu eytt

Ekki gera það **eyða og endurskapa** víddarsett sem hvers kyns lausn til að leysa hugsanleg vandamál með jafnvægisgögnin fyrir tiltekið víddarsett. Það er kostnaðarsamt að endurskapa víddarsett. Fyrir frekari aðstoð við vandamál, hafðu samband við þjónustuver. 


Frekari upplýsingar eru í [Fjárhagsvíddir](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
