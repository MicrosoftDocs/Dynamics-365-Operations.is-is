---
title: Setja upp staðgreiðsluskattskóða fyrir TDS-skattgerð
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp skattkóða fyrir skatt sem dreginn er frá í uppruna (TDS).
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023340"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>Setja upp staðgreiðsluskattskóða fyrir TDS-skattgerð

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp skattkóða fyrir skatt sem dreginn er frá í uppruna (TDS).

1. Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Staðgreiðsluskattskóðar**.

    [![Síða staðgreiðsluskattskóða](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. Á aðgerðasvæðinu skal velja **Nýtt** til að stofna staðgreiðsluskattskóa fyrir TDS og færa inn nauðsynlegar upplýsingar.
3. Á flýtiflipanum **Almennt** í reitnum **Tegund skatts** er **TDS** valið til að flokka skattkóðann sem TDS-skattkóða.
4. Í reitnum **Jöfnunartímabil** skal velja jöfnunartímabilið fyrir TDS-skattkóðann.
5. Í svæðinu **Aðallykill** skal velja fjárhagslykilinn sem bóka á TDS-upphæðina í.
6. Í reitnum **Viðskiptakröfur** skal velja þann kröfureikning sem bóka á TDS-upphæðina sem dregin er frá í sölufærslum á.

    Reiturinn **Uppruni** er sjálfkrafa stilltur á **Prósenta af brúttó upphæð** og ekki er hægt að breyta gildinu.

    > [!NOTE]
    > Ekki er hægt að stilla uppruna á **Prósenta af nettó upphæð** fyrir skattkóða af TDS-skatttegund.

7. Í reitnum **Hluti staðgreiðsluskatts** skal velja TDS-skatthluta fyrir TDS-skattkóðann.
8. Á aðgerðasvæðinu skal velja **Gildi** til að opna síðuna **Gildi staðgreiðsluskatts**.
9. Í reitnum **Frá dagsetningu** skal færa inn upphafsdagsetningu TDS-gildisins. Í reitinn **Til dagsetningar** skal slá inn lokadagsetningu.

    > [!NOTE]
    > Reitirnir **Lægri mörk**, **Efri mörk** og **Útiloka %** eru ekki í boði fyrir skattkóða af TDS-skattategund.

10. Í reitinn **Gildi** skal færa inn prósentu TDS fyrir TDS-skattkóðann.
11. Lokið síðunni **Gildi staðgreiðsluskatts** til að snúa aftur á síðuna **Síða staðgreiðsluskattskóðar**.

    > [!NOTE]
    > Hnappurinn **Takmarkanir** á síðunni **Staðgreiðsluskattkóðar** er ekki í boði fyrir skattkóða af tegund TDS-skatts.

12. Lokið síðunni.
