---
title: Gerðir vandamála fyrir ósamkvæmni
description: Í þessu efnisatriði er lýst hvernig á að stofna og nota gerðir vandamála fyrir ósamkvæmni.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ded53fd273ace8a6ed7f37219ca50ade329d9f08249596b524b1e3673d6ad547
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744823"
---
# <a name="problem-types-for-nonconformances"></a>Gerðir vandamála fyrir ósamkvæmni

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig á að stofna og nota gerðir vandamála fyrir ósamkvæmni.

Nota skal síðuna **Gerðir vandamála** til að skilgreina flokkun á gæðavanda sem getur komið upp fyrir hinar ýmsu gerðir ósamkvæmni. Fyrir hverja gerð vandamáls sem búin er til þarf að tilgreina ósamkvæmnisgerðir sem gerð vandamáls getur verið notuð með. Hægt er að setja upp eftirfarandi gerðir ósamkvæmni:

- **Innra** – Ósamkvæmni af þessari gerð tengjast lagerbirgðum (til dæmis gæðapantanir eða biðgeymslupantanir).
- **Viðskiptavinur** – Ósamkvæmni af þessari gerð tengist sölupöntunum.
- **Lánardrottinn** – Ósamkvæmni af þessari gerð tengist innkaupapöntunum.
- **Þjónustubeiðni** – Ósamkvæmni af þessari gerð tengjast þjónustupöntunum.
- **Framleiðsla** – Ósamkvæmi af þessari gerð eru tengd lotupöntunum eða framleiðslupöntunum.
- **Framleiðsla aukaafurðar** – Ósamkvæmni af þessari gerð tengist runupöntunum fyrir aukaafurðir.

Þegar ný gerð vandamáls er stofnuð skal velja **Gerðir ósamkvæmni** á aðgerðasvæðinu til að búa til lista yfir eina eða fleiri gerðir af ósamkvæmni sem eru heimilaðar fyrir gerð vandamáls. Til dæmis getur vandamálagerð sem tengist gallakóða átt við um allar gerðir ósamkvæmni. Hins vegar getur vandamálagerð um kvartanir viðskiptavina hugsanlega aðeins átt við um ósamkvæmisgerðir **Viðskiptavinar** og **Þjónustubeiðni**.

## <a name="examples-of-problem-types"></a>Dæmi um gerðir vandamála

Hér eru nokkur dæmi um aðstæður fyrir gerðir vandamála sem hægt er að nota með mismunandi gerðum ósamkvæmni:

- **Viðskiptavinur**: Viðskiptavinur lagði fram kvörtun, viðskiptavinur skilaði einhverju eða gæðalýsingar voru ekki uppfyllt.
- **Lánardrottinn:** Afurðin skemmdist, gæðalýsingar voru ekki uppfylltar eða röng afurð barst.
- **Þjónustubeiðni:** Gæðaskilyrði voru ekki uppfyllt, viðskiptavinur lagði fram kvörtun eða vélarviðhald er nauðsynlegt.
- **Framleiðsla:** Gæðaskilyrði voru ekki uppfyllt, viðhald vélar er nauðsynlegt eða varan skemmdist.
- **Framleiðsla aukaafurðar:** Gæðalýsingar voru ekki uppfylltar, viðhald vélar er nauðsynlegt eða afurðin skemmdist.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Stofna gerð vandamáls og úthluta henni á gerðir ósamkvæmni

1. Fara í **Birgðastjórnun \> Uppsetningu \> gæðastjórnun \> gerðir vandamála**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Gerð vandamáls** – Færið inn einkvæmt kenni eða heiti fyrir gerð vandamálsins.
    - **Lýsing** – Færið inn ítarlega lýsingu á gerð vandamáls.

1. Á meðan nýja línan er enn valin, skal velja **Gerðir ósamkvæmnitilvika** á aðgerðasvæðinu.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið. Í nýju röðinni skal síðan stilla reitinn **Gerð ósamkvæmni** á gerðina sem þú vilt leyfa fyrir gerð vandamálsins.
1. Endurtaka skal fyrri skref fyrir hverja viðbótargerð ósamkvæmni sem á að heimila fyrir gerð vandans.
1. Lokaðu síðunum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gæðastjórnunaryfirlit](quality-management-processes.md)
- [Virkja stjórnun gæða og ósamkvæmni](enable-quality-management.md)
- [Starfsmenn ábyrgir fyrir samþykki ósamkvæmni](quality-responsible-workers.md)
- [Biðgeymslusvæði fyrir ósamkvæmi](quality-quarantine-zones.md)
- [Gerðir greininga fyrir ósamkvæmni](quality-diagnostic-types.md)
- [Gæðagjöld fyrir ósamkvæmi](quality-charges.md)
- [Aðgerðir fyrir ósamkvæmni.](quality-operations.md)
- [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
