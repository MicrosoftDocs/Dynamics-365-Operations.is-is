---
title: Staða viðhalds
description: Þetta efni útskýrir hvernig á að reikna út stöðu viðhalds í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43389db93032ec29adb805f86ae04a686803176f
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889578"
---
# <a name="maintenance-status"></a>Staða viðhalds

[!include [banner](../../includes/banner.md)]

 

Í eignastjórnun er hægt að gera yfirlitsútreikning fyrir tiltekið tímabil yfir nýjar, virkar og fullunnar viðhaldsbeiðnir, verkbeiðnir og aðgerðir niðurtíma vegna viðhalds. Þú getur einnig séð fjölda lokinna ástandsmatsprófana á sama tímabili. Notaðu þennan útreikning til að fá yfirlit yfir vinnuálag fyrir komandi og loknar viðhaldsbeiðnir og verkbeiðnir.

## <a name="make-a-maintenance-status-calculation"></a>Gerðu útreikning á viðhaldsstöðu

1. Smelltu á **Eignastýring** > **Fyrirspurnir** > **Staða viðhalds**.

2. Í glugganum **Reikna út stöðu** skaltu velja tímabilið sem þú vilt gera útreikning fyrir í reitunum **Frá dags.** og **Til dags.**.

3. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að viðhaldslínur séu varðandi virkar staðsetningar. 

  Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman stöðu á línu frá virkum staðsetningum á lægra stigi. 
  
  Ef þú setur töluna „0“ inn í reitinn **Stig** sérðu ítarlegar niðurstöður sem sýna allar viðhaldslínur á öllum virkum staðsetningarstigum sem þær tengjast.

4. Smellið á **Í lagi** til að byrja að reikna.

5. Smelltu á hnappana **Flokka eftir** til að sýna nauðsynleg smáatriði við útreikninginn. Valdir hnappar **Flokka eftir** eru auðkenndir. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

6. Mundu að smella á hnappinn **Uppfæra** til að uppfæra útreikninginn í hvert skipti sem þú gerir breytingar með því að virkja eða afvirkja hnappana **Flokka eftir** eða með því að gera útreikning fyrir nýtt tímabil.

7. Smelltu á **Stöðu** ef þú vilt búa til nýjan útreikning á viðhaldsstöðu.

>[!NOTE]
>Niðurstöðurnar sem eru sýndar í **Staða viðhalds** innihalda aðeins viðhaldsbeiðnir og verkbeiðnir sem hafa raunverulegan upphafsdag og tíma. Lokadagsetning og tími mega vera auður.

## <a name="example-1"></a>Dæmi 1

Á skjámyndinni hér að neðan hafa hnapparnir **Ár** og **Mánuður** verið virkjaðir. Með hakað í þessa valkosti **Flokka eftir** færðu almennt yfirlit mánaðarlega um vinnuálag og afköst sem tengjast viðhaldsbeiðnum og verkbeiðnum. 

![Dæmi um mánaðarlegt vinnuálag](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>Dæmi 2

Á skjámyndinni hér að neðan hefur upplýsingum um virkar staðsetningar verið bætt við. Nú er mögulegt að bera saman vinnuálag og afköst milli virkra staðsetninga, sem geta táknað landfræðilega staði, verksmiðjur eða vinnusvæði. 

![Dæmi um mánaðarlegt vinnuálag með virkum staðsetningum](media/14-controlling-and-reporting.png)

