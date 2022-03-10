---
title: Prófanir gæðastjórnunar
description: Í þessu efnisatriði er lýst hvernig á að búa til prófanir sem hægt er að nota fyrir gæðapantanir í Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c10b67f86fc29b5e8c08081a9b789d4f42c24cf4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573850"
---
# <a name="quality-management-tests"></a>Prófanir gæðastjórnunar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig á að búa til prófanir sem hægt er að nota fyrir gæðapantanir í Microsoft Dynamics 365 Supply Chain Management.

Notið síðuna **Prófanir** til að skilgreina og skoða einstök próf sem ákvarða hvort framleiðsluvara fyrirtækisins uppfylli gæðakröfur. Hægt er að úthluta einu eða fleiri einstökum prófum á prófunarflokk. Í þessu tilviki þarf einnig að tilgreina prófunarsértækar upplýsingar, eins og viðunandi mælingargildi. Mæligildi eru notuð fyrir magnbundnar prófanir. Fyrir gæðapróf eru prófbreytur notaðar.

- Fyrir magnbundnar prófanir er reiturinn **Gerð** stilltur á *Heiltala* eða *Brot*. Mælieining er einnig tilgreind. Gæðaskilyrði og prófunarniðurstöður sem eru sýnd sem tölur.
- Fyrir gæðaprófanir er reiturinn **Gerð** stilltur á *Valkostur*. Eigindlegar prófanir krefjast viðbótarupplýsingar um prófunarbreytuna sem verið er að mæla og tölusetta valkosti hennar. Gæðaforskriftir og prófunarniðurstöður sem eru sýnd eftir útkomu.

Einnig má tengja prófunartækið við próf. Hins vegar þarf ekki að búa til og nota próf með gæðapöntunum. Frekari upplýsingar er að finna í [Prófunartæki gæðastjórnunar](quality-test-instruments.md).

Einnig er hægt að valfrjálst tilgreina einingu fyrir próf, til að gefa upp mælieininguna sem niðurstöður prófunar eru skráðar í. Til dæmis gæti prófun á hitastigi innihaldið einingu sem er annaðhvort gráður Fahrenheit eða gráður Celsíus.

## <a name="example-of-a-test"></a>Dæmi um próf

Framleiðslufyrirtæki framkvæmir tvær prófanir á innkeyptu efni: magnbundið próf fyrir gæði efnis og gæðapróf fyrir skemmdir á umbúðum. Fyrirtækið skilgreinir viðbótarupplýsingar um magnbundna prófið til að skilgreina prófunarbreytuna (til dæmis skemmdir á umbúðum) og útkomu þess. Fyrirtæki notar síðuna **Prófunarflokkar** til að úthluta tveimur prófunum á prófunarflokk og tilgreina prófunarsértækar upplýsingar. Prófunarflokkurinn er tengdur við gæðapöntun, þannig að fyrirtækið getur gert skýrslu um niðurstöður þessara tveggja prófa.

## <a name="create-a-test"></a>Stofna próf

Til að stofna próf skal fylgja eftirfarandi skrefum.

1. Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Prófanir**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Próf** – Færið inn einkvæmt kenni eða heiti fyrir prófið.
    - **Lýsing** – Færið inn nákvæma lýsingu á prófuninni.
    - **Gerð** – Veljið þá gerð niðurstöðu sem á að koma út úr prófinu. Fyrir magnbundnar prófanir skal velja *Brot* eða *Heiltala*. Fyrir gæðaprófanir, veljið *Valkostur*.
    - **Prófunartæki** – Veljið [prófunartæki](quality-test-instruments.md) sem á að nota fyrir prófið.
    - **Eining** – Ef þú valdir *Brot* eða *Heiltölu* í reitnum **Gerð** (þ.e. ef prófið er magnbundið próf), skal velja mælieininguna sem niðurstöður prófunar eiga að vera skráðar í.

1. Lokið síðunni.

> [!NOTE]
> Eftir að próf hefur verið vistað er ekki lengur hægt að breyta reitnum **Tegund** í reitnum hnitanetinu. Ef breyta þarf gerð fyrir niðurstöður prófunar sem verður skráð fyrir próf skal velja **Breyta gerð gæðaprófunar** á aðgerðasvæðinu. Í svarglugganum **Breyta gerð gæðaprófunar** skal stilla reitinn **Ný gerð** á æskilega gerð og síðan velja **Í lagi** til að loka svarglugganum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Prófunartæki gæðastjórnunar](quality-test-instruments.md)
- [Prófunarflokkar gæðastjórnunar](quality-test-groups.md)
- [Prófunarbreytur gæðastjórnunar](quality-test-variables.md)
- [Gæðatengingar](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
