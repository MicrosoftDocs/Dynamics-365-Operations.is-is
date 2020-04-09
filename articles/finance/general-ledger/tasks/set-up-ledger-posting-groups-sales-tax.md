---
title: Setja upp fjárhagsbókunarflokkur fyrir virðisaukaskattur
description: Vsk er reiknaður og bókaður á aðallykla sem eru tilgreindar í fjárhagsbókunarflokkur.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30870ea17ea73e48467698166ba14a9184f5a3b1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144813"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Setja upp fjárhagsbókunarflokkur fyrir virðisaukaskattur

[!include [banner](../../includes/banner.md)]

Vsk er reiknaður og bókaður á aðallykla sem eru tilgreindar í fjárhagsbókunarflokkur. Fjárhagsbókunarflokkar eru tengdir hverri vsk-kóða. Geturðu uppsett einstaka fjárhagsbókunarflokkur fyrir hvern VSK-kóði, notað einn fjárhagsbókunarflokkur fyrir VSK-kóði eða úthluta mörgum fjárhagsbókunarflokkur í VSK-kóði. Þessi skráning notar sýnigögn DEMF fyrirtækis 

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Skattur > Uppsetning > VSK > fjárhagsbókunarflokkur.**
2. Smellt er á **Nýtt**.
3. Í reitinn **Fjárhagsbókunarflokkur** skal rita gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. í reitnum **VKS-kröfur** velurðu aðallykil fyrir útskatt sem er til greiðslu til skattyfirvalda. Virðisaukaskattur er safnað fyrir hönd skattyfirvalda þegar skattskyldar vörur eru seldar.  
6. Í reitnum **Vsk-viðskiptakröfur** velurðu aðallykil fyrir innskatt sem er móttekinn frá skattyfirvöldum. Lánardrottnar innheimta skatt fyrir hönd skattyfirvalda þegar fyrirtækið kaupir skattskyldar vörur og þjónustu. Þessi reitur er ekki tiltækur ef valkosturinn Beita skattareglum virðisaukaskatts er valinn á síðunni **Færibreytur fjárhags**. Þess í stað, virðisaukaskattur sem eru Greitt í lánardrottinn eru debetfært í sama lykill og innkaup.   
7. Í reitnum **Kostnaður neysluskatts** skal velja aðallykil til að bóka frádráttarbæran neysluskatt sem er ekki innheimtur eða tilkynntur til skattyfirvalda af lánardrottnum sem hluti af EU bakfærðum vöru- og þjónustuskattur/samræmdur söluskattur. Valkosturinn **Neysluskattur** þarf að vera valinn fyrir **Vsk-kóðann** í **Vsk-flokk** sem er notað í færslunni. Þessi reitur er ekki tiltækur ef valkosturinn **Beita skattareglum virðisaukaskatts** er valinn á síðunni **Færibreytur fjárhags**.   
8. í reitnum **Neysluskattskröfur** velurðu aðallykil til að bóka á neysluskatt á innleið sem er til greiðslu til skattyfirvalda. Valkosturinn **Neysluskattur** þarf að vera valinn í **Vsk-kóðann** í **Vsk-flokk** til að bóka **Neysluskatt**. Ef valkosturinn **Nota vsk-sköttunarreglur** er valinn á síðunni **Færibreytur fjárhags** er mótlykill bókaður á kostnaðarlykil færslunnar.   
9. Í reitnum **Jöfnunarreikningur** skal velja aðallykilinn sem nettóstaða fjárhagslykla sem tilgreindir eru og bókaðir í reitunum **Neysluskattur** og **VSK-viðskiptakröfur**. Staðan verður stofnuð þegar vsk jafna og bókunarvinnsla er keyrð.  Ef skattayfirvöld fyrir jöfnunartímabil tengjast lykli lánardrottins er staðan bókuð í lánardrottnalykil þess í stað.
10. í reitnum **Staðgreiðsluafsláttur lánardrottins** velurðu aðallykil til að bóka staðgreiðsluafslátt fyrir Vsk-kóða sem tengist þessum fjárhagsbókunarflokki. Þetta er valfrjálst og ef enginn lykill er færður inn verður aðallykill á **Kóðum staðgreiðsluafsláttar** notaður. Það getur verið gagnlegt að nota mismunandi lykla eftir **Fjárhagsbókunarflokki** ef notaður er bakfærður vsk á valkost staðgreiðsluafsláttar á Vsk-flokka.  
11. Í reitnum **Afsláttur viðskiptavinar** velurðu aðallykil til að bóka staðgreiðsluafslátt fyrir **Vsk-kóða** sem tengjast þessum **fjárhagsbókunarflokki**. Þetta er valfrjálst og ef enginn lykill er færður inn verður aðallykill á **kóðum staðgreiðsluafsláttar** notaður. Það getur verið gagnlegt að nota mismunandi lykla eftir **Fjárhagsbókunarflokki** ef notaður er bakfærður vsk á valkost staðgreiðsluafsláttar á **Vsk-flokka**.  
12. Smellt er á **Vista**.

