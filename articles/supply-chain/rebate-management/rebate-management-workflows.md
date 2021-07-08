---
title: Verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp verkflæði tilboðs fyrir stjórnun eftirágreidds afsláttar til að samþykkja og virkja tilboð.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270958"
---
# <a name="rebate-management-deal-workflows"></a>Verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar

[!include [banner](../includes/banner.md)]

Til að samþykkja eftirágreidda afslætti notar stjórnunar eftirágreidds afsláttar sama verkflæðisvettvang og önnur Finance and Operations forrit. Tvö vinnsluferli eru tengd við öll verkflæði:

- Einn þáttur verkflæðisins samþykkir tilboðið.
- Einn þáttur verkflæðisins virkjar tilboðið þannig að notandinn eða verkflæðisferlið getur samþykkt færslurnar.

Áður en hægt er að nota tilboð eftirágreidds afsláttar þarf það að vera virkt í einingunni **Stjórnun eftirágreidds afsláttar**. Til að virkja tilboð þarf fyrst að stofna og grunnstilla *Verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar*.

Notendur geta ekki samþykkt tilboð handvirkt. Alltaf skal nota verkflæðið.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Stofna og hafa umsjón með verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar

Til að vinna með verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning \> Verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar**. Þar er hægt að skoða, búa til og uppfæra verkflæði eins og þörf krefur. Aðeins eitt verkflæði af þessari gerð getur verið virkt í einu. Frekari upplýsingar um verkflæði, hvernig á að nota síðuna **Verkflæði fyrir stjórnun eftirágreidds afsláttar** og hvernig á að stofna verkflæði er að finna í [Yfirlit yfir verkflæðiskerfi](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) og tengdum efnisatriðum.

## <a name="use-a-workflow-to-activate-a-deal"></a>Nota verkflæði til að virkja tilboð

Til að virkja tilboð í verkflæði skal opna tilboðið (til dæmis á **Öll tilboð fyrir stjórnun eftirágreidds afsláttar** síðunni). Í aðgerðasvæðinu er síðan smellt á **Verkflæði \> Senda**. Þegar búið er að vinna úr og samþykkja nýtt tilboð í gegnum verkflæðið verður það virkt og tilbúið til notkunar.

Þegar tilboð hefur verið virkjað er ekki hægt að breyta meirihluta uppsetningarinnar. Ef breyta þarf virku tilboði skal fyrst gera það óvirkt og svo stofna nýtt. Ef nýja tilboðið á að líkjast gamla tilboðinu er hægt að stofna það með því að afrita það gamla.

Hægt er að breyta eftirfarandi stillingum fyrir tilboð eftir að það hefur verið virkjað:

- Afstemma eftir
- Uppsöfnuð trygging
- Bókunarregla
- Bókunarregla fyrir tryggingu
- Athugasemdir skjals
- Gjaldmiðill
- Frá degi
- Til dags.

Auk þess er hægt að fjarlægja línur eftirágreidds afsláttar.
