---
title: Úthluta notendum á öryggishlutverk
description: Til að fá aðgang að forritum Finance and Operations, þarf að úthluta notendum á öryggishlutverk.
author: Peakerbl
ms.date: 05/06/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb4b143400a1f092c8f7a15bbb047eda52a4a4d8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745886"
---
# <a name="assign-users-to-security-roles"></a>Úthluta notendum á öryggishlutverk

[!include [banner](../../includes/banner.md)]

Til að nota eitthvað annað en algengan eiginleika í Finance and Operations forritum þarf að úthluta notendum á öryggishlutverk. Hægt er að úthluta notendum á hlutverk sjálfkrafa, byggt á reglum og viðskiptagögnum, útiloka notendur frá sjálfvirkri hlutverkaúthlutun eða bæta notendum við hlutverk handvirkt.

## <a name="automatically-assign-users-to-roles"></a>Sjálfkrafa skipa notendum í hlutverkin
Þessu ferli útskýrt hvernig kerfisstjórum geta sjálfvirkt úthlutað notendum á hlutverk, byggt á viðskiptagögnum. 
1. Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.
2. Í þessu dæmi skal velja yfirmaður Bókhalds. Veljið hlutverk sem nota á fyrir útvinnsluna á reglunni. Í þessu dæmi skal velja yfirmann bókhalds. 
3. Veljið **Bæta við reglu** til að opna svargluggann.
4. Í listanum **Velja fyrirspurn** skal finna og velja þá skráningu sem óskað er eftir. Velja fyrirspurn fyrir þessa reglu.  
5. Á listanum **Heiti aðildarreglu** skaltu smella á tengilinn í valinni röð.
6. Veldu **Breyta fyrirspurn**. Breyta skal fyrirspurninni eftir því sem þörf krefur.  
7. Veljið **Í lagi**.
8. Veldu **eyra sjálfvirka hlutverkaúthlutun**.
9. Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Notendur > Notendur** (helst á sérstökum vafraflipa).
10. Farðu yfir hlutverkin sem úthlutað var ýmsum notendum til að staðfesta að fyrirspurnin um hlutverkaskiptin hafi verið rétt. Stilla og keyra aftur ef þörf krefur.

## <a name="exclude-users-from-automatic-role-assignment"></a>Útiloka notendum frá sjálfvirka hlutverkaúthlutun
1. Lokið síðunni.
2. Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.
3. Í þessu dæmi skal velja yfirmaður Bókhalds. Veljið hlutverk. Fyrir þessu dæmi skal velja yfirmann bókhalds.  
4. Í valmyndinni **Notendur sem úthlutað er á hlutverk** skaltu velja **Úthluta / útiloka notendur handvirkt**.
5. Í listanum **Úthluta notendum til eða útiloka notendur frá hlutverki** skaltu merkja valda línu. Velja notanda  
6. Í **Aðgerðarsvæði** velurðu **Útiloka frá hlutverki**.
7. Veldu **Útiloka frá hlutverki** til útiloka valda notendur úr hlutverkinu. Til að fjarlægja útilokanir skal velja notendur sem á að fjarlægja útilokanir á og smella síðan á **Endurstilla stöðu**. Þegar fjarlægja útilokun með því að endurstilla stöðu notanda er hlutverki notanda úthlutað sjálfkrafa. Hins vegar notanda er ekki strax þetta hlutverk úthlutað eða útilokað frá hlutverki þegar endurstilla stöðu. Í stað þess, notandinn annað hvort úthlutaður í hlutverkið eða fjarlægð úr hlutverk í næsta sinn sem keyrðar eru reglum fyrir sjálfvirka hlutverkaúthlutun.  

## <a name="manually-assign-users-to-roles"></a>Úthluta notendum sjálfkrafa á hlutverk
Stjórnandi þarf einnig að fjarlægja notendur sem er úthlutað handvirkt á öryggishlutverk. Þessir notendur eru ekki fjarlægðir úr hlutverkum eftir reglum fyrir sjálfvirka hlutverkaúthlutun.

1. Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.
2. Í trénu skal velja hlutverk og í valmyndinni **Notendur sem úthlutað er á hlutverk** skal velja **Úthluta / útiloka notendum handvirkt**.
4. Í **Úthluta eða útiloka notendum frá hlutverki** eru notendur sem hafa ekki fengið hlutverkið birtir þar sem **Úthlutunarstillingu** er stillt á **Ekkert**. Velja einn eða fleiri notendur sem á að úthluta hlutverkinu.
5. Á **Aðgerðarsvæði** skal velja **Úthluta hlutverki**. **Úthlutunarstilling** er uppfærð í **Handvirkt** og notendur hafa nú nýtt hlutverk.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]