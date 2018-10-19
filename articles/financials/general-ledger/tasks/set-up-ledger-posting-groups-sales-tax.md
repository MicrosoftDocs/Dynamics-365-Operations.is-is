--- 
title: "Setja upp fjárhagsbókunarflokkur fyrir virðisaukaskattur"
description: "Vsk er reiknaður og bókaður á aðallykla sem eru tilgreindar í fjárhagsbókunarflokkur."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 15421da6f325dfee22a303e9fe83a0e72895fa08
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Setja upp fjárhagsbókunarflokkur fyrir virðisaukaskattur

[!include [task guide banner](../../includes/task-guide-banner.md)]

Vsk er reiknaður og bókaður á aðallykla sem eru tilgreindar í fjárhagsbókunarflokkur. Fjárhagsbókunarflokkar eru tengdir hverri vsk-kóða. Geturðu uppsett einstaka fjárhagsbókunarflokkur fyrir hvern VSK-kóði, notað einn fjárhagsbókunarflokkur fyrir VSK-kóði eða úthluta mörgum fjárhagsbókunarflokkur í VSK-kóði. Þessi skráning notar sýnigögn DEMF fyrirtækis 

1. Fara í Skattur > Uppsetning > VSK > fjárhagsbókunarflokkur.
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum fjárhagsbókunarflokkur.
4. Sláið inn gildi í reitnum „Lýsing“.
5. í reitnum VKS-kröfur, Velja aðallykil fyrir útskatt sem eru greiðslu til skattyfirvalda.
    * Virðisaukaskattur er safnað fyrir hönd skattyfirvalda þegar skattskyldar vörur eru seldar.  
6. í Vsk-viðskiptakröfur, Velja aðallykil fyrir innskatt sem eru mótteknar frá skattyfirvöldum 
    * Lánardrottnar innheimta skatt fyrir hönd skattyfirvalda þegar fyrirtækið kaupir skattskyldar vörur og þjónustu. Þetta svæði er ekki tiltækt ef valkosturinn um reglur fyrir beitingu skattlagningu söluskatts er valinn á síðunni færibreytur fjárhags. Þess í stað, virðisaukaskattur sem eru Greitt í lánardrottinn eru debetfært í sama lykill og innkaup.   
7. Í svæðið Kostnaður neysluskatts, skal velja aðallykil til að bóka frádráttarbæran neysluskatt sem er ekki innheimtur eða tilkynntur til skattyfirvalda af lánardrottnum sem hluti af EU bakfærðum vöru- og þjónustuskattur/samræmdur söluskattur.
    * Valkosturinn Nota skatt í ungverjalandi þarf að velja fyrir Vsk-kóðann í Vsk-flokk sem er notað í færslunni.  Þetta svæði er ekki tiltækt ef valkosturinn um reglur fyrir beitingu skattlagningu söluskatts er valinn á síðunni færibreytur fjárhags.   
8. í reitnum neysluskatts kröfur, Velja aðallykil til að bóka á innleið neysluskattur sem eru kröfur til skattyfirvalda 
    * Valkosturinn neysluskattur í ungverjalandi þarf að velja í Vsk-kóðann í Vsk-flokk til að bóka neysluskatt. Ef valkosturinn Nota vsk-sköttunarreglur í færibreytum fjárhags, er mótlykil bókaðar á kostnaðarlykil færslunnar.   
9. í svæðinu Jöfnunarreikningur, Velja aðallykilinn sem nettóstöðu fjárhagslykla tilgreind í innskatt og útskatt kröfur neysluskatts og kröfur söluskatts verða bókaðar 
    * Staðan verður stofnuð þegar vsk jafna og bóka vinnslu er keyrði.  Ef skattayfirvöld fyrir jöfnunartímabil tengist lykli lánardrottins, stöðu er bókaður í lánardrottnalykil.   
10. í svæðinu staðgreiðsluafsláttur lánardrottins, Velja aðallykil til að bóka staðgreiðsluafslátt fyrir Vsk-kóða sem tengist þessum fjárhagsbókunarflokki 
    * Þetta er valfrjálst og ef enginn lykill er færður inn aðallykil á kóðum staðgreiðsluafsláttar verður notuð. Það getur verið gagnlegt að nota mismunandi, lykla eftir Fjárhagsbókunarflokkur ef notaður er bakfærðum vsk á valkost staðgreiðsluafsláttar á Vsk-flokka.  
11. Í svæðinu mál viðskiptavinar, Velja aðallykil til að bóka staðgreiðsluafslátt fyrir Vsk-kóða sem tengist þessum fjárhagsbókunarflokki 
    * Þetta er valfrjálst og ef enginn lykill er færður inn aðallykil á kóðum staðgreiðsluafsláttar verður notuð. Það getur verið gagnlegt að nota mismunandi, lykla eftir Fjárhagsbókunarflokkur ef notaður er bakfærðum vsk á valkost staðgreiðsluafsláttar á Vsk-flokka.  
12. Smellið á „Vista“.


