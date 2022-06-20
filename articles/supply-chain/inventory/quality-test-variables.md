---
title: Prófunarbreytur gæðastjórnunar
description: Þessi grein lýsir því hvernig á að búa til prófunarbreytur sem hægt er að nota fyrir eigindlegar prófanir á gæðapöntunum í Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 10fe206b76f2e50e09cb6aaa6055614c2fe9425d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857635"
---
# <a name="quality-management-test-variables"></a>Prófunarbreytur gæðastjórnunar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til prófunarbreytur sem hægt er að nota fyrir eigindlegar prófanir á gæðapöntunum í Microsoft Dynamics 365 Supply Chain Management.

Fyrir hvert gæðapróf sem er skilgreint á síðunni **Prófanir** þarf að skilgreina prófunarbreytu og mögulegar útkomur hennar (niðurstöður). (Fyrir gæðaprófanir er reiturinn **Gerð** á síðunni **Prófanir** stilltur á *Valkostur*.)

Þú notar síðuna **Prófunarbreytur** til að setja upp, breyta, og skoða mögulegar útkomur fyrir prófunarbreytu sem er tengd gæðaprófun. Fyrir hverja útkomu úthlutar þú stöðu útkomu sem annaðhvort *Staðið* eða *Fallið* til að gefa til kynna hvort prófið sé staðið eða fallið þegar sú útkoma er valin sem niðurstaða prófunar. Síðan **Prófunarflokkar** er notuð til að úthluta breytu á prófun og sjálfvirkri niðurstöðu á staka eigindlega prófun.

Fyrir hverja prófunarbreytur er mælt með að skilgreina a.m.k. tvær útkomur: ein sem er með stöðu útkomu sem *Staðið* og hin með stöðu útkomu sem *Fallið*. Engin takmörk eru á heildarfjölda breytna eða niðurstaðna sem hægt er að skilgreina. Auk þess geta mörg próf notað sömu prófbreytur til að skrá niðurstöður.

## <a name="examples-of-test-variables"></a>Dæmi um prófunarbreytur

### <a name="example-1"></a>Dæmi 1

Framleiðslufyrirtæki framkvæmir tvö próf á framleiddum efnum. Í einu prófi er sýrustigið tengt litaræmu. Áættanlegt sýrustig er í ljósari litum og óásættanlegt sýrustig er í dekkri litum. Í öðru prófi eru framkvæmdar margar sjónrænar skoðanir og gæðastarfsmenn nota eigin dómgreind til að ákveða hvort varan stenst eða fellur á slíkri skoðun.

### <a name="example-2"></a>Dæmi 2

Framleiðslufyrirtæki sem framleiðir kexkökur notar skoðunarpróf sem nær til nokkurra gerða af hinni framleiddu vöru. Þessi prófun hefur nokkur breytur. Ein færibreyta er bragð, með hugsanlegri útkomu gott eða vont. Önnur færibreyta er litur, með mögulega niðurstöðu of dökkur, of ljós, og í lagi.

## <a name="create-a-test-variable"></a>Stofna prófunarbreytu

Fylgið þessum skrefum til að stofna prófunarbreytu.

1. Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Prófunarbreytur**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Breyta** – Færið inn einkvæmt kenni eða heiti fyrir breytuna.
    - **Lýsing** – Færið inn ítarlega lýsingu á breytunni.

1. While the new row is still selected, select **Niðurstöður** on the Action Pane.
1. Á síðunni **Útkomur úr prófunarbreytum**, á aðgerðasvæðinu, skal velja **Ný** til að bæta línu við hnitið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Útkoma** – Færið inn einkvæmt kenni eða heiti fyrir útkomuna.
    - **Lýsing** – Færið inn ítarlega lýsingu á útkomunni.
    - **Staða útkomu** – Veljið annaðhvort *Staðið* eða *Fallið* til að gefa til kynna hvort prófið sé staðið eða fallið þegar sú útkoma er valin sem niðurstaða prófunar.

1. Endurtakið fyrra skref fyrir hverja útkomu sem fylgir á eftir. Gangið úr skugga um að a.m.k. ein útkoma sé með stöðu útkomu sem *Staðið* og a.m.k. ein sé með stöðuna *Fallið*.
1. Lokaðu síðunum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Prófunartæki gæðastjórnunar](quality-test-instruments.md)
- [Prófanir gæðastjórnunar](quality-tests.md)
- [Prófunarflokkar gæðastjórnunar](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
