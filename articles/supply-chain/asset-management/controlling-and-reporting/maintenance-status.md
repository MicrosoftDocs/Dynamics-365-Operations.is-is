---
title: Staða viðhalds
description: Þetta efni útskýrir hvernig á að reikna út stöðu viðhalds í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918350"
---
# <a name="maintenance-status"></a>Staða viðhalds

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Í eignastjórnun er hægt að gera útreikninga til að sjá yfirlit yfir nýjar, virkar og fullunnar viðhaldsbeiðnir, verkbeiðnir og aðgerðir niðurtíma vegna viðhalds á tilteknu tímabili. Þú getur einnig séð fjölda lokinna ástandsmatsprófana á sama tímabili. Notaðu þennan útreikning til að fá yfirlit yfir vinnuálag varðandi komandi og loknar viðhaldsbeiðnir og verkbeiðnir.

## <a name="make-a-maintenance-status-calculation"></a>Gerðu útreikning á viðhaldsstöðu

1. Smelltu á **Eignastýring** > **Fyrirspurnir** > **Staða viðhalds**.

2. Í glugganum **Reikna út stöðu** skaltu velja tímabiliði sem þú vilt gera útreikning fyrir í reitunum **Frá dags.** og **Til dags.**.

3. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að viðhaldslínur séu varðandi virkar staðsetningar. Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman stöðu á línu frá virkum staðsetningum á lægra stigi. Ef þú setur töluna „0“ inn í reitinn **Stig** sérðu ítarlegar niðurstöður sem sýna allar viðhaldslínur á öllum virkum staðsetningarstigum sem þær tengjast.

4. Smellið á **Í lagi** til að byrja að reikna.

5. Í aðgerðarrúðahópunum **Flokka eftir...** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn. Valdir aðgerðarrúðahnappar eru auðkenndir. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

6. Mundu að smella á hnappinn **Uppfæra** til að uppfæra útreikninginn í hvert skipti sem þú gerir breytingar með því að virkja eða afvirkja hnappana **Flokka eftir...** eða með því að gera útreikning fyrir nýtt tímabil.

7. Smelltu á **Stöðu** ef þú vilt búa til nýjan útreikning á viðhaldsstöðu.

>[!NOTE]
>Niðurstöðurnar sem eru sýndar í **Staða viðhalds** innihalda aðeins viðhaldsbeiðnir og verkbeiðnir sem hafa raunverulegan upphafsdag og tíma. Lokadagsetning og tími mega vera auður.

*Dæmi 1:*

Á myndinni hér að neðan hafa hnapparnir **Ár** og **Mánuður** verið virkjaðir. Hér færðu almennt yfirlit mánaðarlega um vinnuálag og afköst sem tengjast viðhaldsbeiðnum og verkbeiðnum. 

![Mynd 1](media/13-controlling-and-reporting.png)

*Dæmi 2:*

Á myndinni hér að neðan hefur upplýsingum um virkar staðsetningar verið bætt við. Nú er mögulegt að bera saman vinnuálag og afköst milli virkra staðsetninga, sem geta táknað landfræðilega staði, verksmiðjur eða vinnusvæði. 

![Mynd 2](media/14-controlling-and-reporting.png)

