---
title: Tilkynna framleiðslupöntun sem lokna
description: Þessi verklýsing sýnir hvernig á að skrá framleiðslupöntunina sem tilbúna.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d9dcdbcb89df6430fb286c253ebecfc6d885af8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011148"
---
# <a name="report-a-production-order-as-finished"></a>Tilkynna framleiðslupöntun sem lokna

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að skrá framleiðslupöntunina sem tilbúna. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta er sjötta ferli úr sjö sem útskýrir lífsferil framleiðslupöntunar.


## <a name="report-a-production-order-as-finished"></a>Tilkynna framleiðslupöntun sem lokna
1. Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.
    * Veljið framleiðslupöntun sem hefur stöðuna Hafið.  
2. Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.
3. Smellið á „Bóka sem tilbúið“.
    * Á þessari síðu er hægt að staðfesta magn lokinnar vöru til að skrá sem tilbúna.  
4. Smellið á flipann „Almennt“.
5. Setja Gallalaust magn á '18'.
6. Setja Gallað magn á "2".
7. Í ástæða Villu svæðinu, veljið 'Efni'.
8. Veldu eða hreinsaðu gátreitinn Ljúka vinnslu.
9. Veldu eða hreinsaðu gátreitinn Samþykkja Villu.
10. Smellið á „Í lagi“.

## <a name="verify-the-report-as-finished-journal"></a>Staðfesta færslubók bóka sem tilbúið
1. Smellið á „Skoða“ á aðgerðarúðunni.
2. Smellið á Bókað sem tilbúið.
3. Í listanum skal merkja valda línu.
4. Í listanum skal smella á tengilinn í valinni línu.
    * Bóka sem tilbúið færslubók er bókuð. Ef óskað er að leiðrétta færslubókina handvirkt er hægt að stofna nýja færslubók þar sem hægt er að gera breytingar.  

