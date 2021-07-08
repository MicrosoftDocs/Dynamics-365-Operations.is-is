---
title: Villa kemur upp við keyrslu á innbyggðri aðaláætlunarvél
description: Þegar úreld innbyggð aðaláætlunarvél er keyrð koma upp villuboð.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294102"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>Villa kemur upp við keyrslu á innbyggðri aðaláætlunarvél

Villukóði: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>Einkenni

Þegar aðaláætlanagerð er keyrð með úreldri innbyggðri aðaláætlunarvél koma upp eftirfarandi villuboð:

> Þú færð þessi villuskilaboð vegna þess að innbyggð aðaláætlunarvél var notuð fyrir aðstæður sem eru studdar fínstillingu skipulagningar. Þú ættir að flytja þig yfir í fínstillingu skipulagningar núna, þar sem núverandi aðaláætlanagerð verður úrelt. Athugaðu að þessi áætlanakeyrsla var keyrð. Ef flutningurinn þinn inniheldur sterk tengsl um eiginleika sem bíða er hægt að biðja um undantekningu á áframhaldandi notkun á vél fyrir innbyggðri aðaláætlunarvél. Ljúktu við eftirfarandi spurningalista til að hefjast handa og, ef svo á við, biddu um undantekningu frá yfirfærslu í fínstillingu skipulagningar. [Fínstilling áætlanagerðar, yfirfærsla og spurningalisti undantekningar](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>Orsök

Ef aðaláætlanagerð er keyrð og eiginleikar framleiðslustýringar eru ekki notaðir ættirðu að huga að því að flytja þig yfir í fínstillingu skipulagningar. Verið er að úrelda innbyggða aðaláætlunarvél. Ef þú vilt halda áfram að nota hana án þess að fá villuboð verður þú að sækja um undanþágu hjá Microsoft.

## <a name="resolution"></a>Lausn

Frekari upplýsingar um hvernig á að flytja yfir í fínstillingu skipulagningar eða hvernig á að sækja um undanþágu svo þú getir í staðinn haldið áfram að nota úrelda innbyggða áætlunarvél er að finna í [Flutningur yfir í fínstillingu skipulagningar fyrir aðaláætlanagerð](/dynamics365/supply-chain/master-planning/new-master-planning-engine).
