---
title: Endurstilla fastar runuvinnslur
description: Þetta efnisatriði útskýrir hvernig á að leysa úr vandamálum með runuvinnslur sem ekki er unnið úr.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: c8b80406991bab6ba87fc8e38b9e49391921d98df5dbf223561848157f8f419d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738344"
---
# <a name="reset-stuck-batch-jobs"></a>Endurstilla fastar runuvinnslur

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
