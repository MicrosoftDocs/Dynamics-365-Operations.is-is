---
title: Endurstilla fastar runuvinnslur
description: Þetta efnisatriði útskýrir hvernig á að leysa úr vandamálum með runuvinnslur sem ekki er unnið úr.
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: f1aa9f53e0d314edd920a664d18408019325d435
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534022"
---
# <a name="reset-stuck-batch-jobs"></a>Endurstilla fastar runuvinnslur


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Úthreyfing

Microsoft Dynamics 365 Human Resources getur fundið vandamál við runuvinnslur sem er fastar í **Keyrir** eða **Hættir við** stöðu og lýkur ekki.

## <a name="resolution"></a>Upplausn

Þegar runuvinnsla er föst í stöðunni **Í keyrslu** eða **Hættir við** er hægt að endurstilla stöðuna með því að þvinga á afturköllun vinnslunnar. Eftir að hætt hefur verið við það er hægt að endurstilla runuvinnsluna með því að setja hana í stöðuna **Í bið**. Hún er svo aftur keyrð í næstu runuvinnslu á dagskrá.

1. Á **Kerfisstjórnun** vinnusvæðinu skal velja **Tenglar** síðuna og svo **Runuvinnslur**.

2. Á **Runuvinnsla** listasíðunni skal velja verkið sem þarf að endurstilla.

3. Á aðgerðaborðanum skal velja **Þvinga afturköllun** og staðfesta aðgerðina.

   > [!NOTE]
   > Aðgerðin **Þvinga afturköllun** er aðeins tiltæk þegar valin runuvinnsla er með stöðuna **Keyrir** eða **Hættir við** og engin runuvinnsla eða afturköllunarferli er í keyrslu fyrir verkið.

4. Á aðgerðaborðanum skal velja **Breyta stöðu**.

5. Á síðunni **Velja nýja stöðu** skal velja **Í bið** og svo velja **Í lagi**.

   ![Velja nýja stöðu á runuvinnslu.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Sjá einnig

[Bæta frammistöðu með því að tímasetja runuvinnslur utan vinnutíma](hr-admin-troubleshooting-batch-jobs.md)<br>
[Auka afköst með sjálfvirkum hreinsunarverkum](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
