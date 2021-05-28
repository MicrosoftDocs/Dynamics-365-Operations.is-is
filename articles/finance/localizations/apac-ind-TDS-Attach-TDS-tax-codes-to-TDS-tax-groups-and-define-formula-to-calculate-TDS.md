---
title: Hengja TDS-skattkóða við TDS-skattflokka og skilgreina formúluna fyrir útreikning TDS
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp TDS-skattflokka og hengja TDS-skattkóða við TDS-skattflokka. Til að reikna út TDS fyrir TDS-skattflokk þarf að skilgreina formúluna fyrir TDS-skattkóða sem eru hengdir við hana.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023337"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>Hengja TDS-skattkóða við TDS-skattflokka og skilgreina formúluna fyrir útreikning TDS

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp TDS-skattflokka og hengja TDS-skattkóða við TDS-skattflokka. Til að reikna út TDS fyrir TDS-skattflokk þarf að skilgreina formúluna fyrir TDS-skattkóða sem eru hengdir við hana.

Fylgið þessum skrefum til að setja upp TDS-skattflokk, hengja TDS-skattkóða við hann, og skilgreina formúluna fyrir útreikning TDS.

1. Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Staðgreiðsluskattsflokkar**.

    [![Síða staðgreiðsluskattsflokka](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. Á aðgerðasvæðinu skal velja **Nýtt** til að stofna staðgreiðsluskattsflokk fyrir TDS og færa inn nauðsynlegar upplýsingar.
3. Í reitnum **Skattgerð** skal velja **TDS**.
4. Í flýtiflipanum **Uppsetning** skal velja **Bæta við** til að stofna línu.
5. Í reitnum **Staðgreiðsluskattskóði** skal velja TDS-skattkóða fyrir TDS-skattflokkinn. Reiturinn **Heiti staðgreiðsluskatts** sýnir heiti TDS-skattkóðans og reiturinn **Gildi** sýnir gildið.
6. Til að hunsa mörkin og undantekningarmörkin sem eru skilgreind fyrir TDS-skattþáttinn sem er hengdur við TDS-skattkóðann í TDS-færslum skal velja gátreitinn **Horfa fram hjá mörkum**.
7. Til að koma í veg fyrir að skattflokkurinn verði reiknaður út í færslum skal velja gátreitinn **Undanþága**.
8. Á aðgerðasvæðinu skal velja **Hönnuður** til að opna formúluhönnuðinn svo þú getir skilgreint formúluna fyrir útreikning á TDS fyrir TDS-skattflokkinn. Á síðunni **Hönnuður** sýnir flipinn **Skattar** TDS-skattkóðana sem hafa verið valdir fyrir TDS-skattflokkinn.

    [![Hönnuðarsíða](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Í flipanum **Útreikningur** skal velja **Alt+N** til að stofna línu. Reiturinn **Kenni** sýnir sjálfkrafa myndað forgangskenni fyrir TDS-útreikning.
10. Í reitnum **Skattkóði** skal velja TDS-skattkóðann til að skilgreina formúluna fyrir hann. Allir TDS-skattkóðarnir sem hafa verið valdir fyrir TDS-skattflokkinn er hægt að velja í þessum reit.
11. Í reitnum **Skattskyldur stofn** skal velja stofninn fyrir útreikning á TDS:

    - **Brúttóupphæð** – Reiknið út TDS út frá brúttóupphæð færslunnar (þ.e. reikningsupphæðinni) með því að nota útreikningssegðina sem er skilgreind fyrir skattkóðann.
    - **Án brúttóupphæðar** – Reiknið út TDS út frá útreikningssegðinni sem skilgreind er fyrir skattkóðann.

    > [!NOTE]
    > Ekki er hægt að stilla reitinn **Skattskyldur stofn** á **Án brúttóupphæðar** fyrir TDS-skattkóðann sem er með forgangskenni upp á **1**.

12. TDS-útreikningurinn byggir á formúlunni sem er skilgreind í reitnum **Segð útreiknings** fyrir hvern skattkóða sem er hengdur við TDS-skattflokkinn. Veljið hnappinn fyrir plúsmerkið (**+**), mínusmerkið (**-**), margföldunarmerkið (**\**_) eða deilingarmerkið (_*/**) til að færa inn útreikningssegðina fyrir valinn TDS-skattkóða í reitnum **Segð útreiknings**.

    > [!NOTE]
    > Ekki er hægt að skilgreina neina útreikningssegð fyrir TDS-skattkóða sem er með forgangskennið **1**.

13. Til að skilgreina segð útreiknings fyrir TDS-skattkóðann í reitnum **Segð útreiknings** skal bæta við TDS-skattkóðum sem eru í boði í flipanum **Skattar**. Til að bæta við TDS-skattkóðum í reitinn **Segð útreiknings** er hægt að nota einhverja af eftirfarandi aðferðum:

    - Dragið nauðsynlegan skattkóða úr flipanum **Skattar** og yfir í reitinn **Segð útreiknings**.
    - Pikkið tvisvar (eða tvísmellið) á nauðsynlegan skattkóða í flipanum **Skattar**.
    - Veljið og haldið (eða hægrismellið á) nauðsynlegum skattkóða í flipanum **Skattar** og veljið síðan **Bæta við skattkóða**.

    > [!NOTE]
    > Setjið inn segð útreiknings á undan hverjum TDS-skattkóða. TDS-skattkóðarnir sem hefur verið bætt við segð útreiknings birtast innan sviga (\[...\]).

14. Til að hreinsa segð útreiknings sem er skilgreind fyrir skattkóða í reitnum **Segð útreiknings** skal velja hnappinn **C**.
15. Til að eyða færslu í flipanum **Útreikningur** skal velja **Eyða**.
16. Lokið síðunni.
