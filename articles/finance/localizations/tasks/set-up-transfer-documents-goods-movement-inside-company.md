---
title: Setja upp flutningsskjöl fyrir vöruflutninga innan fyrirtækis
description: Þetta ferli sýnir hvernig á að setja upp flutningsskjöl fyrir hreyfingu á vörum innan fyrirtækis.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
ms.openlocfilehash: 333c5b5e5cfa25e705c9864542517f8ec5532dfe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282335"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a>Setja upp flutningsskjöl fyrir vöruflutninga innan fyrirtækis

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig á að stofna flutningsskjöl fyrir hreyfingu á vörum innan fyrirtækis Þetta ferli er aðeins tiltæk fyrir lögaðila með aðalaðsetur í Litháen. Þetta ferli var stofnuð með því að nota sýnigögn fyrirtækisins DEMF með aðalaðsetur í Litháen. Áður en hægt er að ljúka þessu ferli verður að ljúka ferlinu „Setja upp flutningsskjöl fyrir hreyfingu á vörum innan fyrirtækis”. Þetta ferli er ætluð fyrir bókhaldara birgða. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="create-a-transfer-order"></a>Flutningspöntun stofnuð
1. Fara í birgðastjórnun > pantanir á Innleið > Flutningspöntun.
2. Smellið á „Nýtt“.
3. Sláðu inn eða veldu gildi í reitnum Úr vöruhúsi.
4. Sláðu inn eða veldu gildi í reitnum Í vöruhús.
5. Smelltu á Bæta við.
6. Í listanum skal merkja valda línu.
7. Í reitinn Vörunúmer skal slá inn eða veldu gildi.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Fylla út upplýsingar um Flutning fyrir flutningspöntun
1. Smellið á „Vista“.
2. Smellið á senda á aðgerðarúðunni.
3. Smelltu á Upplýsingar um flutning.
4. Velja skal Já í svæðinu Prenta flutningsupplýsingar.
5. Sláið inn eða veldu gildi í reitnum vörur gefnar út eftir.
6. Í reitinn umbúðir skal slá inn gildi.
7. Í reitinn áhættustig skal slá inn gildi.
8. Sláið inn eða veldu gildi í reitnum flutningsaðili.
9. Sláið inn eða veldu gildi í reitnum líkan.
10. Færa inn gildi í reitnum Skráningarnúmer.
11. Færa inn gildi í svæðinu skráningarnúmer eftirvagns.
12. Sláið inn eða veldu gildi í reitnum ökumaður.
13. Sláið inn gildi í reitinn Nafn ökumanns.
14. Smellið á „Vista“.
15. Lokið síðunni.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Skoða fylgiseðil fyrir óbókaðar flutningspöntun
1. Smella skal á fylgiseðilinn.
2. Smellið á „Í lagi“.
3. Lokið síðunni.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Skoða fylgiseðil fyrir bókaðar flutningspöntun
1. Í aðgerðasvæðinu er smellt á flutningspöntun.
2. Smellið á senda á aðgerðarúðunni.
3. Smelltu á Senda flutningspöntun
4. Smellið á flipann „Almennt“.
5. Í reitnum uppfærsla skal velja valkost.
6. Smellið á flipann „Yfirlit“.
7. Í reitinn fylgiseðill skal slá inn gildi.
8. Smellið á „Í lagi“.
9. Smellið á senda á aðgerðarúðunni.
10. Smella skal á fylgiseðilinn.
11. Smellið á „Í lagi“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
