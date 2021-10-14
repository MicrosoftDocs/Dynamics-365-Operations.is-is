---
title: Prófunartæki gæðastjórnunar
description: Í þessu efnisatriði er lýst hvernig á að stofna prufubreytur sem hægt er að nota í prófunum gæðapantana í Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d80a4f784a43e0d83d1f5b42f6740ef6da3add1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565904"
---
# <a name="quality-management-test-instruments"></a>Prófunartæki gæðastjórnunar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig á að stofna prufubreytur sem hægt er að nota í prófunum gæðapantana í Microsoft Dynamics 365 Supply Chain Management.

Þú notar síðuna **Prófunartæki** til að skilgreina og skoða upplýsingar um tækin sem eru notuð til að framkvæma prófanir á gæðapöntunum. Prófunartæki eru valfrjáls. Hins vegar geta þeir hjálpað gæðastarfsmönnum að vita hvaða tæki eða tól þeir ættu að nota til að framkvæma sérstakt próf.

## <a name="test-instrument-example"></a>Dæmi um prófunartæki

Þú ert að framkvæma ýmis próf á íhlutum raftækja. Sum próf eru fyrir rafspennu íhlutanna, eitt próf er fyrir hitastig þeirra og eitt próf er fyrir þyngd þeirra. Mismunandi verkfæri, tæki eða búnaður er notaður til að framkvæma hvert próf. Til dæmis er spennumælir notaður til að mæla spennu, hitamælir notaður til að mæla hitastig og vog notuð til að mæla þyngd. Þú getur stillt hvert þessara tækja sem prófunarbúnað og tilgreint mælieininguna sem skal skrá niðurstöður prófunarinnar í. Til dæmis eru niðurstöður úr spennumælinum skráðar í voltum, niðurstöður úr hitamælinum eru skráðar í gráðum Fahrenheit eða gráðum selsíus og niðurstöður vigtarinnar eru skráðar í pundum eða kílóum.

## <a name="create-a-test-instrument"></a>Stofna prófunartæki

1. Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Prófunartæki**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Prófunartæki** – Færið inn einkvæmt kenni eða heiti fyrir prófunartækið.
    - **Lýsing** – Færið inn nákvæma lýsingu á prófunartækinu.
    - **Eining** – Veljið eininguna sem tækið mælir niðurstöður í. Reiturinn **Nákvæmni** er sjálfkrafa stilltur út frá einingunni sem þú velur.

1. Lokið síðunni.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Prófun gæðastjórnunar](quality-tests.md)
- [Prófunarflokkar gæðastjórnunar](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
