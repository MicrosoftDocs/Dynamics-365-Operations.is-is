---
title: Vinnsla á kostnaðarinnhreyfingum
description: Þetta efni veitir upplýsingar um vinnslu á ljósstafalínu (OCR) fyrir innhreyfingar. Þessi eiginleiki er hannaður til að bæta upplifun notenda þegar kostnaðarskýrslur eru búnar til í Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2e819521828b054f70476b1eb061ee08c486d09f
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113687"
---
# <a name="public-preview-expense-receipt-processing"></a>Opin forskoðun: Vinnsla á kostnaðarinnhreyfingum

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Útgjaldafærsla hefur verið aukin með tilkomu vinnslu á ljósstafalínu (OCR) fyrir innhreyfingar. Þessi eiginleiki er hannaður til að bæta upplifun notenda þegar kostnaðarskýrslur eru búnar til.

## <a name="key-features"></a>Lykileiginleikar

- Nafn söluaðila, dagsetning og heildarupphæð er dregin út úr innhreyfingum.
- Aðgerðin reynir að samsvara óbundnum kvittunum við óbundin kostnaðarfærslna.
- Notendur geta búið til handvirkt færð kostnaðarfærslur úr innhreyfingum.

## <a name="usage-examples"></a>Dæmi um notkun

- **Hengdu sjálfkrafa við innhreyfingar sem innihalda kreditkortafærslur þegar kostnaðarskýrsla er búin til.**

    1. Opnaðu vinnusvæðið **Kostnaðarstjórnun**.
    2. Á flipanum **Innhreyfingar** staðfestirðu að óviðhengdar innhreyfingar séu til staðar. Þú getur líka hlaðið inn innhreyfingum á flipann **Innhreyfingar**.
    3. Á flipanum **Kostnaður** staðfestirðu að óviðhengdur kostnaður sé til staðar. Venjulega flytur kostnaðarstjórinn inn þennan kostnað frá kreditkortafyrirtækinu.
    4. Veldu **Nýja kostnaðarskýrslu**. Taktu eftir að þú getur líka haft kostnað og innhreyfingar þegar þú býrð til kostnaðarskýrslu. Ef þú bætir bæði við kostnaði og innhreyfingum er sjálfvirk samsvörun innhreyfinga gagnvart kostnaðinum sett af stað.

- **Búðu til kostnað eða samsvaraðu kostnaði við kvittun.**

    1. Í kostnaðarskýrslu, á flipanum **Innhreyfingar**, festirðu innhreyfingu við með því að velja **Bæta við innhreyfingum**.
    2. Undir upphlaðinni mynd af innhreyfingunni skaltu taka eftir valkostunum **Stofna** og **Jafna**.

        - Veldu **Stofna** til að búa til handvirkt færðar kostnaðarfærslur og fylla út gildin sem eru dregin út úr innhreyfingunni.
        - Ef þú velur **Jafna** reynir kerfið að passa núverandi kostnað við innhreyfinguna.

## <a name="installation"></a>Uppsetning

Þessi aðgerð virkar ásamt eiginleikanum **Kostnaðarskýrslur endurhugsaðar** til að auðvelda kostnaðarupplifunina.

Til að nota þessa ítarlegu kostnaðarmöguleika skaltu setja upp innbótina Þjónusta kostnaðarstýringar fyrir Microsoft Dynamics 365 Finance og kveikja á aðgerðum í þínu tilviki. Þú getur fengið aðgang að viðbótinni frá verkefninu í Microsoft Dynamics Lifecycle Services (LCS).

1. Skráðu þig inn á LCS og opnaðu viðkomandi umhverfi.
2. Farðu í **Fullar upplýsingar**.
3. Veldu **Viðhalda** eða skrunaðu niður að flýtiflipanum **Umhverfisinnbætur**.
4. Veldu **Setja upp nýja innbót**.
5. Veldu **Kostnaðarstjórnunarþjónusta**.
6. Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.
7. Velja **Setja upp**.

Í vinnusvæðinu **Stjórnun eiginleika** kveikirðu á eftirfarandi eiginleikum:

- Kostnaðarskýrslur endurhugsaðar
- Sjálfvirk samsvörun og kostnaður vegna kvittunar búinn til

Þegar kveikt er á þessum eiginleikum gerast eftirfarandi aðgerðir:

- Núverandi vinnusvæði **Kostnaðarstjórnunar** er skipt út fyrir nýja vinnusvæðið.
- Nýtt valmyndaratriði fyrir sýnileika kostnaðarreits er bætt við.
- Þú getur samt opnað fyrri síðuna **Kostnaðarskýrslur** með því að fara í **Kostnaðarstjórnun > Minn kostnaður > Kostnaðarskýrslur**.
- Verkflæði og allar samþykktir leiða þig ennþá að núverandi síðu fyrir kostnaðarskýrslur.
- Innhreyfingar verða unnar í gegnum Microsoft Azure Cognitive Services og lýsigögn verða dregin út og bætt við.
- Bætt er við valkosti sem gerir þér kleift að búa til kostnaðarskýrslu sem inniheldur samsvarandi ótengdar innhreyfingar.
- Valkostur sem er bætt við kostnaðarskýrslur gerir þér kleift að búa til kostnaðarlínu úr innhreyfingu eða reyna að jafna núverandi innhreyfingu við núverandi kostnaðarlínu.

Fyrir frekari upplýsingar um eiginleikan Kostnaðarskýrslur endurhugsaðar er að finna í [Kostnaðarskýrslur endurskoðaðar](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Algengar spurningar

**Notar Microsoft gögnin mín fyrir gerðir sínar?**

Nei, Microsoft hefur smíðað almennt vélanámslíkan fyrir innhreyfingavinnsluþjónustu sína. Þetta líkan er ekki byggð á innhreyfingum sem þú hleður upp.

**Hvar er þessi eiginleiki tiltækur og afgreiddur?**

Sem stendur eru Bandaríkin studd.

**Hvert fara innhreyfingarnar mínar?**

Finance mun hafa samband við Cognitive Services til að vinna úr gögnum svæðisins. Cognitive Services mun geyma afrit af innhreyfingunni í allt að sólarhring meðan vinnsla á sér stað. Eftir að vinnslu er lokið mun Cognitive Services fjarlægja innhreyfinguna. Innhreyfingar eru enn geymdar í Finance.

Fyrir frekari upplýsingar, sjá [Virkja skilning á kvittun með nýrri getu Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
