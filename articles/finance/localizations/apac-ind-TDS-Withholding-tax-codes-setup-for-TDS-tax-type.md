---
title: Setja upp staðgreiðsluskattskóða fyrir TDS-skattgerð
description: Í þessari grein er útskýrt hvernig á að setja upp skattkóða fyrir skatt sem dreginn er frá í uppruna (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fabe14b74c445434c37cb6ee79597d37affb162d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904384"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>Setja upp staðgreiðsluskattskóða fyrir TDS-skattgerð

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að setja upp skattkóða fyrir skatt sem dreginn er frá í uppruna (TDS).

1. Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Staðgreiðsluskattskóðar**.

    [![Síða staðgreiðsluskattskóða.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

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
