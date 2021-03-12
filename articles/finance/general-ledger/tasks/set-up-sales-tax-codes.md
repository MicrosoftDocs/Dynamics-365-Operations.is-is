---
title: Setja upp VSK-kóða
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp virðisaukaskatt í Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f6df5ed3fc49b537845e7d418d4953c0faee5f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994541"
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
    - Á Flýtiflipanum **Útreikninga**, í svæðinu Uppruna ef Upphæð á einingu er valinn er gildið margfaldað með magninu í færsluna til að reikna út vsk-upphæð.  Ef skattkóði er ekki skattur byggður á einingum er gildið sem er prósenta sem er notað í Uppruna fyrir þetta skattkóði til að reikna út upphæð virðisaukaskatts.     
11. Veljið **Vista**.
12. Lokið síðunni.
13. Veljið **Vista**.

