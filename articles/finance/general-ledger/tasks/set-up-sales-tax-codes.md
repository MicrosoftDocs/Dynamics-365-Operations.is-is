---
title: Setja upp VSK-kóða
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp virðisaukaskatt í Dynamics 365 Finance.
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2539d701dda4ef5e1484d095b2d86d1f68a0dc98
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562103"
---
# <a name="set-up-sales-tax-codes"></a>Setja upp VSK-kóða

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp virðisaukaskatt. Vsk-kóða eru stofnaðar fyrir hvert óbeint skattur eða gjald sem lögaðili er skylt að reikna, innheimta og greiða til skattyfirvalda.

Þetta verkefni notar USMF-sýnifyrirtækið.

1. Farðu í **Skoðunarrúða > Skattur > Óbeinir skattar > Virðisaukaskattur- > Vsk-kóðar**.
2. Veljið **Nýtt**.
3. Í reitnum **VSK-kóði** skal færa inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Veljið **Jöfnunartímabil** með því að opna fellilistann til að tilgreina hvaða skattyfirvöld og í hvaða tímabilum þessi vsk þarf að tilkynntur og greiddur.
6. Veljið **fjárhagsbókunarflokk** til að tilgreina skal aðallykla til að bóka vsk í fjárhag.
7. Stækka **Útreikningur** flýtiflipi. Þetta inniheldur mörg svæði sem stjórna hvernig vsk-upphæðir verður reiknuð. Fylltu út þessa reiti eftir þörfum.  
8. Á **Aðgerðarrúðan** efst í viðmótinu skaltu velja **VSK-kóði**.
9. Veldu **Gildi**.
10. Sláðu inn gildi fyrir þennan skattakóða í **gildi** dálki.

    Á Flýtiflipanum **Útreikningur**, í svæðinu **Uppruni** ef **Upphæð á einingu** er valinn er gildið margfaldað með magninu í færsluna til að reikna út vsk-upphæð.  Ef skattkóði er ekki skattur byggður á einingum er gildið sem er prósenta sem er notað í Uppruna fyrir þetta skattkóði til að reikna út upphæð virðisaukaskatts.     

11. Veldu **Vista**.
12. Lokið síðunni.
13. Veldu **Vista**.

Frá og með útgáfu 10.0.22 af Microsoft Dynamics 365 Finance, ef þú ert að nota [Skattþjónustu](../../localizations/global-tax-calcuation-service-overview.md), og eiginleikinn [**Styðja mörg VSK-skráningarnúmer**](../../localizations/emea-multiple-vat-registration-numbers.md) er virkjaður á vinnusvæði **Eiginleikastjórnunar**, getur þú notað reitinn **Skattagerð** til að tilgreina gerð skattkóðans. Eftirtalin gildi eru tiltæk:

- Hefðbundinn VSK-skattur
- Skertur virðisaukaskattur
- VSK 0%
- Vörugjald
- Annað

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
