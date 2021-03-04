---
title: Rafræn skýrslugerð skilgreina áfangastað
description: Þetta ferli sýnir hvernig á að setja upp og nota mismunandi áfangastaði fyrir Rafræna skýrslugerð (ER) úttak þætti, eins og möppu eða skrá.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0073033454c7d3054496fe4c38cdb3cff71d8755
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681878"
---
# <a name="er-configure-destinations"></a>Rafræn skýrslugerð skilgreina áfangastað

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig á að setja upp og nota mismunandi áfangastaði fyrir Rafræna skýrslugerð (ER) úttak þætti, eins og möppu eða skrá. Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF. Þýskaland er land/svæði fyrir aðalaðsetur lögaðila, hins vegar er hægt að nota hvaða lögaðila sem er fyrir þetta ferli. 

Snið sem notuð er í þessu dæmi er ISO20022 millifærsla fjármuna en þú getur nota hvaða snið sem hafa þegar verið fluttar. Athugið að þetta ferli er dæmi um eina skrá og eina uppsetningu áfangastaðar. Frekari upplýsingar um stjórnun viðtökustaðar Rafræna skýrslugerð finnast í Dynamics 365 Finance Hjálp.

1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Rafræn skýrslugerð áfangastaður.
2. Smellt er á Nýtt til að búa til nýtt sett áfangastaða fyrir snið.
3. Í tilvísunarsvæði er valið snið sem á að skilgreina áfangastaði fyrir.
    * Ef ekki gildi til að velja þýðir það að þú hafa ekki flytja inn Rafræna skýrslugerð skilgreiningarsnið. Þarf að flytja inn skilgreiningarsnið áður en uppsetning áfangastaði.  
4. Smelltu á Nýtt til að stofna nýjan viðtökustað skráa.
    * Athugið að hægt er að stofna eina viðtökustað skráar fyrir hvert úttaksþátt í sama snið t.d. möppu eða skrá. Getur virkja og óvirkja áfangastaði sér í stillingum.  
5. Í svæðið Heiti færið inn notendavænt heiti úttaksþáttar.
    * Mælt er með því að nota skilmerkileg heiti "Greiðsluskrá" eða „Eftirlitsskýrsla". Þessi nöfn verða sýndar notendum á keyrslutíma með stillingar fyrir áfangastað.  
6. Í Skrárheiti, velja skrána eða möppu sem tilheyra snið.
7. Smellt er á stillingar
8. Veljið Já í reitnum Virkja.
    * Gátreiturinn Virkt á hvern flipa virkjar og óvirkjar hvern ákvörðunarstað sérstaklega. Í þessu dæmi, verður hægt að senda frálagsskrá til viðtakanda tölvupósts þegar skráin er mynduð.  
9. Smella á Breyta til að setja upp viðtakendur tölvupósts.
10. Smelltu á Bæta við.
11. Smelltu á Tölvupóstur vegna prentstýringar
12. Veljið valkost í upprunareit tölvupósts.
    * Hægt er að mismunandi upprunagerðir tölvupósts, eins og viðskiptavin eða gerð lánardrottins. Þetta skilgreinir gerð af frumbreytu sem verður skilað með formúlu upprunareiknings tölvupósts. Formúla upprunareiknings Tölvupóstsm sen lýst er í eftirfarandi skrefi, er staðurinn þar sem þú munt bindast uppruna tölvupósts. Veljið Lánadrottinn ef formúlan skilar lánardrottnalykill. Nota Lánardrottinn ef verið er að nota ISO 20022 millifærsla fjármuna skilgreiningardæmi.  
13. Smella á hnappinn upprunabinding tölvupósts.
14. Í formúla, Færið inn skjalbundna tilvísun í gerð aðila sem þú valdir áður.
    * Í stað þess að því að slá inn, er hægt að finna gagnaveituhnút sem stendur fyrir lykil aðilans, og smella á bæta Við gagnaveitu hnappinn til að uppfæra formúlu. Til dæmis: Ef ISO 20022 skilgreining fyrir millifærsla fjármuna er notuð, er hnúta sem standa fyrir lykil lánardrottins '$PaymentsForCoveringLetter'. Creditor.Identification.SourceID. Annars að færa inn strenggildi, eins og "DE-001", til að vista formúlu.  
15. Smellið á „Vista“.
16. Lokið síðunni.
17. Smella á Breyta til að skilgreina upplýsingar um tengilið fyrir aðila.
18. Veljið Já í reitnum aðaltengiliður.
    * Hægt er að nota mismunandi valkosti til að tilgreina hvaða gerð tengiliðar aðilans ætti að nota sem tölvupóstfang fyrir þessa áfangastaðar. Aðaltengiliður er notuð í þessu dæmi.  
19. Smellið á „Í lagi“.
20. Smellið á „Í lagi“.
21. Í reitinn Efni skal slá inn gildi.
22. Smellið á „Í lagi“.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]