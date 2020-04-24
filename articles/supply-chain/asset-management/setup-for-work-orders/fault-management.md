---
title: Villustjórnun
description: Þetta efni skýrir villustjórnun í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6665e80342af1baa7176aee92693b77e83b368f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205921"
---
# <a name="fault-management"></a>Villustjórnun

[!include [banner](../../includes/banner.md)]

 

Í eignastjórnun geturðu notað villuhönnuðinn til að setja upp bilunareinkenni, bilunarsvæði og bilunargerðir á eignategundum. Á þennan hátt geturðu stjórnað göllum sem eru greindar á eignum. Að auki er hægt að skrá bilunarástæður og ábendingar til að laga bilanir í verkbeiðni.

Ferlið til skráningar og stjórnunar á villum samanstendur af þessum skrefum.

1. Búðu til lista yfir bilunareinkenni, bilunarsvæði og bilunargerðir sem gætu komið fram á eignagerðum þínum.
2. Settu upp einkenni, bilunarsvæði og villugerðir hjá bilunarhönnuðinum.

Hér eru nokkur dæmi til að hjálpa þér að skilja muninn á bilunareinkennum, bilunarsvæðum og bilunargerðum.

**Einkenni bilana:**

- Ójafnvægisspenna
- Skammhlaup
- Hávaði
- Leki
- Titringur

**Bilunarsvæði:**

- Rafmagns
- Vélrænn
- Vökvakerfi
- Loftknúið

**Gerðir bilana:**

- Gallað aðalsáturvaf
- Gölluð díóða
- Óhreint vaf
- Gallaður rafall
- Gallaður skynjari

## <a name="create-fault-symptoms"></a>Stofna bilunareinkenni

Fylgdu þessum skrefum til að búa til lista yfir einkenni sem hægt er að nota í villuhönnuðinum.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Bilunareinkenni**.
2. Veljið **Ný** til að stofna nýja skrá.
3. Í reitinn **Bilunareinkenni** reitinn skal slá inn heiti fyrir bilunareinkennið.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Veljið **Vista**.

## <a name="create-fault-areas"></a>Stofna bilunarsvæði

Fylgdu þessum skrefum til að búa til lista yfir svæði eða staðsetningar sem hægt er að nota í villuhönnuðinum.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Bilunarsvæði**.
2. Veljið **Ný** til að stofna nýja skrá.
3. Í reitinn **Bilunarsvæði** skal slá inn heiti fyrir bilunarsvæðið.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Veljið **Vista**.

## <a name="create-fault-types"></a>Stofna biðunargerðir

Fylgdu þessum skrefum til að búa til lista yfir bilunargerðir sem hægt er að nota í villuhönnuðinum.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Bilunargerðir**.
2. Veljið **Ný** til að stofna nýja skrá.
3. Í reitnum **Bilunartegund** skal slá inn heiti á bilunargerð.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Veljið **Vista**.

## <a name="set-up-the-fault-designer"></a>Settu upp bilunarhönnuðinn

Í bilunarhönnuðinum seturðu upp bilunargögn um eignagerðir.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Bilunarhönnuður**.
2. Í vinstri glugganum velurðu þá gerð eigna sem á að setja upp bilanaskrá fyrir.
3. Á flýtiflipanum **Bilunareinkenni** velurðu **Bæta við línu** og síðan bilunareinkenni í reitnum **Bilunareinkenni**.
4. Á flýtiflipanum **Bilunarsvæði** velurðu **Bæta við línu** og síðan bilunarsvæði í reitnum **Bilunarsvæði**.
5. Á flýtiflipanum **Bilunartegund** velurðu **Bæta við línu** og síðan bilunartegund í reitnum **Bilunartegund**.
6. Til að stofna samsetningar af öllum fyrirliggjandi bilanaeinkennum, -svæðum og -gerðum á fljótlegan hátt fyrir valda eignagerð skaltu velja **Stofna bilanasamsetningar**. Þessi aðgerð er gagnleg ef þú hefur bætt við mörgum bilunareinkennum, -svæðum og -gerðum. Það er auðveldara að eyða línunum fyrir samsetningar sem ekki eiga við eignagerðina en að búa til nýjar línur handvirkt.

    > [!NOTE]
    > Veldu til að afrita uppsetningu bilanaeinkenna, -svæða og -gerða frá einni eignategund til valinnar eignartegundar **Afrita úr eignategund**.

7. Veldu **Vista** til að vista breytingarnar.

![Síða bilunarhönnuðar](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Stofna orsakir bilunar

Fylgdu þessum skrefum til að búa til lista yfir þekktar orsakir bilunar sem hægt er að bæta við vinnupöntun eða viðhaldsbeiðni.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Orsakir bilunar**.
2. Veljið **Ný** til að stofna nýja skrá.
3. Í reitnum **Orsakir bilunar** skal slá inn heiti á orsakir bilunar.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Veljið **Vista**.

## <a name="create-fault-remedies"></a>Búðu til bilunarúrræði

Fylgdu þessum skrefum til að búa til lista yfir uppástungur að úrræðum og viðgerðum sem hægt er að bæta við vinnupöntun eða viðhaldsbeiðni.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Bilun** \> **Bilunarúrræði**.
2. Veljið **Ný** til að stofna nýja skrá.
3. Í reitinn **Bilunarúrræði** skal slá inn heiti fyrir bilunarúrræðið.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Veljið **Vista**.

> [!NOTE]
> Þú getur breytt nöfnum á bilanaeinkennum þínum, -svæðum, -gerðum, -orsökum og -úrræðum eins og þú þarft. Nafnabreytingarnar endurspeglast sjálfkrafa í tengdum bilaskráningum.
