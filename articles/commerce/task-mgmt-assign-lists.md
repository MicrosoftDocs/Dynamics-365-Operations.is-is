---
title: Úthlutaðu verkefnalistum til verslana eða starfsmanna
description: Þetta efni lýsir því hvernig á að úthluta verklista á verslanir eða starfsmenn í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 82cec9861b759037f40315fb2e6f36002a0ac059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413225"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Úthlutaðu verkefnalistum til verslana eða starfsmanna

[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að úthluta verklista á verslanir eða starfsmenn í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Verkefnisstjórn í Dynamics 365 Commerce gerir þér kleift að úthluta verkefnalista til margra verslana eða starfsmanna, eða til samblanda verslana og starfsmanna. Til dæmis gæti svæðisstjóri í 20 verslunum viljað úthluta verklistanum **Undirbúningur undir frídaga** á allar 20 verslanir.

## <a name="start-the-task-list-assignment-process"></a>Ræstu úthlutunarferli verkefnalista

Fylgdu þessum skrefum til að hefja úthlutun verkefnalista.

1. Farðu í **Retail og Commerce \> Verkefnisstjórn \> Stjórnun verkefnisstjórnunar**.
1. Veldu verkefnalistann sem á að úthluta.
1. Veldu **Hefja ferli**.
1. Í valmyndinni **Hefja ferli**, á flipanum **Almennt**, í reitnum **Heiti vinnslu**, slærðu inn heiti (t.d. **Verslanir á Austurlandi**).
1. Í reitnum **Markdagsetning** tilgreinirðu dagsetningu.
1. Til að úthluta verkefnalistanum á verslanir, á flipanum **Verslanir** skaltu nota síuna **Stigveldi fyrirtækis** til að finna og velja verslanir.

    Til að úthluta verkefnalistanum á starfsmenn, á flipanum **Starfskraftar** skaltu finna og velja starfsmennina.

1. Veldu **Í lagi** til að hefja ferlið. Verkefnalistinn er úthlutað til valinna verslana eða starfsmanna.

Eftirfarandi mynd sýnir dæmi um hvernig á að finna og velja verslanir í valmyndinni **Hefja ferli**.

![Finndu og veldu verslanir í valmyndinni Hefja ferli](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Úthlutaðu verkefnalistum endurtekið

Söluaðili hefur stundum endurtekin verkefni, eins og „Gátlista yfir lokun fimmtudags“ eða „Gátlista yfir fyrsta dag mánaðar“. Þess vegna gætu þeir viljað úthluta verkefnalistanum ítrekað.

1. Farðu í **Retail og Commerce \> Verkefnisstjórn \> Stjórnun verkefnisstjórnunar**.
1. Veldu verkefnalistann sem á að úthluta.
1. Veldu **Hefja ferli**.
1. Í valmyndinni **Hefja ferli**, á flipanum **Almennt**, í reitnum **Heiti vinnslu**, slærðu inn heiti.
1. Stilltu valkostinn **Endurtekning** á **Já**.
1. Í reitinn **Mótfærsla markdagsetningar endurtekningar í dögum** slærðu inn fjölda daga. Til dæmis ef þú slærð inn **4** er markdagurinn endurtekningardagur auk fjögurra daga.
1. Á flipanum **Keyra í bakgrunni** velurðu **Endurtekning**.
1. Í valmyndinni **Skilgreina endurtekningu** slærðu inn tíðniviðmið og veldu síðan **Í lagi**.

Eftirfarandi mynd sýnir dæmi um hvernig á að færa inn tíðniviðmið í valmyndinni **Skilgreina endurtekningu**.

![Tíðniviðmið færð inn í valmyndina Skilgreina endurtekningu](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Rekja stöðu verkefnalista

Ef þú ert svæðisstjóri eða verslunarstjóri gætirðu viljað fylgjast með stöðu verkefnalista sem hefur verið úthlutað til margra verslana eða starfsmanna. Þú getur síðan fylgst með verslunum eða starfsmönnum sem luku ekki verkefnum sínum á réttum tíma. Bakvinnsla Commerce gerir þér kleift að skoða stöðu verkefnalista, endurúthluta verkefnum eða breyta stöðu verkefnis.

Fylgdu þessum skrefum til að fylgjast með stöðu verkefnalistans fyrir öll verkefni.

1. Farðu í **Retail og Commerce \> Verkefnisstjórn \> Ferli verkefnisstjórnunar**.
1. Veldu flipann **Allir verkefnalistar** til að skoða stöðu allra verkefnalista sem eru úthlutaðir til ýmissa verslana.

Til að rekja stöðu verkefnalista fyrir öll verk sem er úthluta á þig skaltu fylgja þessum skrefum.

1. Farðu í **Retail og Commerce \> Verkefnisstjórn \> Ferli verkefnisstjórnunar**.
1. Veldu flipann **Mín verk** eða **Öll verk** til að skoða eða uppfæra stöðu verkefna sem þér er úthlutað.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit verkefnastjórnunar](task-mgmt-overview.md)

[Skilgreina verkstýringu](task-mgmt-configure.md)

[Búa til verkefnalista og bæta við verkum](task-mgmt-create-lists.md)

[Verkstjórnun á sölustað](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]