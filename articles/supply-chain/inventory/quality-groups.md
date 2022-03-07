---
title: Vörugæðaflokkar
description: Í þessu efnisatriði er lýst hvernig á að nota og stofna gæðaflokka fyrir vörur til að flokka vörur rökrétt svo að hægt sé að úthluta þeim á gæðatengingar fyrir sjálfvirka myndun gæðapantana.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3074a6a8cc054be045bf593b509e76a1043af0b7
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956695"
---
# <a name="item-quality-groups"></a>Vörugæðaflokkar

[!include [banner](../includes/banner.md)]

Gæðaflokkur stendur fyrir sameiginlegar prófunarkröfur fyrir vörur. Í þessu efnisatriði er lýst hvernig á að nota og stofna gæðaflokka fyrir vörur til að flokka vörur rökrétt svo að hægt sé að úthluta þeim á gæðatengingar fyrir sjálfvirka myndun gæðapantana.

Til að setja upp, breyta og skoða vörur sem er úthlutað á gæðaflokk eða gæðaflokkarnir sem eru úthlutað á vöru skal fara í **Birgðastjórnun \> Uppsetning \> Gæðaflokkar**. Þegar búið er að skilgreina kröfur fyrir prófun á síðunni **Prófunarflokkar** er hægt að skilgreina reglur fyrir sjálfvirka myndun gæðapantana. Til að einfalda ferlið eru ekki skilgreindar reglur fyrir stakar vörur. Í staðinn er hægt að skilgreina reglur fyrir gæðaflokk á síðunni **Gæðatengingar**.

## <a name="example-of-an-item-quality-group"></a>Dæmi um gæðaflokk vöru

Framleiðslufyrirtæki kaupir ýmislegt hráefni sem eru með sömu prófunarkröfur fyrir væntanlegt eftirlit. Fyrirtækið skilgreinir því gæðaflokk og úthlutar síðan vörunúmerum sem eru tengd hráefnum á þann flokk. Síðar kaupir fyrirtækið nýja gerð hráefnis sem er með sömu prófunarkröfur. Í stað þess að setja upp ný skilyrði um prófanir fyrir nýtt efni bætir við fyrirtækið vörunúmeri fyrir nýtt efni fyrirliggjandi gæðaflokk.

Sama fyrirtæki framleiðir einnig vörur sem eru með sömu prófunarkröfur í framleiðslu og sendir vörur með sömu kröfur fyrir framkvæmd prófana fyrir sendingu. Fyrirtækið skilgreinir því tvo viðbótargæðaflokka og úthlutar síðan viðeigandi vörunúmerum í hvern gæðaflokk.

## <a name="create-a-quality-group"></a>Stofna gæðaflokk

Til að búa til gæðaflokk skal fylgja þessum skrefum.

1. Fara í **birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðaflokkar**
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Gæðaflokkur** – Færið inn einkvæmt kenni eða heiti fyrir gæðaflokkinn.
    - **Lýsing** – Færið inn ítarlega lýsingu á gæðaflokknum.

1. Lokið síðunni.

## <a name="manually-add-items-to-a-quality-group"></a>Bæta vörum handvirkt við gæðaflokk

Fylgið eftirfarandi skrefum til að bæta hlutum handvirkt við gæðaflokk.

1. Fara í **birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðaflokkar**
1. Veljið gæðaflokkinn sem á að bæta vörum við.
1. Á aðgerðasvæðinu skal velja **Vörur**.
1. Á síðunni **Vörur í gæðaflokkum**, á aðgerðasvæðinu, skal velja **Ný** til að bæta nýrri línu við hnitanetið. Í nýju línunni skal síðan stilla reitinn **Vörunúmer** á vörunúmerið sem bæta á við.
1. Endurtakið fyrra skref fyrir hverja viðbótarvöru sem þarf að bæta við.
1. Lokaðu síðunum.

## <a name="add-multiple-items-to-a-quality-group"></a>Bæta mörgum vörum við gæðaflokk

Fylgið eftirfarandi skrefum til að bæta mörgum atriðum við gæðaflokk.

1. Fara í **birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðaflokkar**
1. Búa til eða velja gæðahópinn sem bæta á atriðum við.
1. Á aðgerðasvæðinu skal velja **Bæta við vörum**.
1. Færið inn síuviðmiðin fyrir vörurnar sem á að bæta við í glugganum **Fyrirspurn**. Til dæmis væri hægt að sía fyrir allar vörur í tilteknum vöruflokki.
1. Veljið **Í lagi**.
1. Í glugganum **Bæta við atriðum** sýnir reitur öll atriðin sem samsvara fyrirspurninni. Skoða niðurstöður.

    Ef einhverjar breytingar eru nauðsynlegar skal velja **Velja** til að fara aftur í svargluggann **Spyrjast fyrir** og breyta fyrirspurninni.

1. Þegar niðurstöðurnar innihalda allar vörur sem á að bæta við er valið **Í lagi**.
1. Lokið síðunni.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Tengja atriði handvirkt við gæðahóp

Fylgja skal eftirfarandi skrefum til að tengja hlut handvirkt við gæðflokk.

1. Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðaflokkar vöru**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Vörunúmer** – Velja vörunúmerið sem á að bæta við.
    - **Gæðaflokkur** – Veljið gæðaflokk sem úthluta á vörunni.

1. Endurtaka skal fyrri skref fyrir hverja viðbótarsamsetningu vöru og gæðaflokks sem verður að bæta við.
1. Lokaðu síðunum.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Bæta við gæðaflokki handvirkt af síðunni Útgefnar afurðir

Fylgja skal eftirfarandi skrefum til að bæta gæðahópi handvirkt við á síðunni **Losaðar afurðir**.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið afurðina sem úthluta á gæðaflokki á.
1. Á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, í flokknum **Gæði**, skal velja **Gæðaflokkar vöru**.
1. Á síðunni **Vörur í gæðaflokkum**, á aðgerðasvæðinu, skal velja **Ný** til að bæta nýrri línu við hnitanetið. Í nýju línunni skal síðan stilla reitinn **Gæðaflokkur** á gæðaflokkinn sem þú vilt úthluta afurðinni.
1. Endurtaka á fyrra skref fyrir hvern gæðaflokk sem bætist við sem á að úthluta afurðinni.
1. Lokaðu síðunum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Prófunartæki gæðastjórnunar](quality-test-instruments.md)
- [Prófanir gæðastjórnunar](quality-tests.md)
- [Prófunarflokkar gæðastjórnunar](quality-test-groups.md)
- [Prófunarbreytur gæðastjórnunar](quality-test-variables.md)
- [Gæðatengingar](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
