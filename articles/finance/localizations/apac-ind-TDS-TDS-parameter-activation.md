---
title: Stilla TDS færibreytur
description: Þessi grein útskýrir hvernig á að stilla færibreytur til að virkja Tax Deducted at Source (TDS) virkni í tilgreindum færslum. Þetta er nauðsynlegt skref til að nota eiginleikann skattur sem dreginn er frá í uppruna, TDS.
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
ms.openlocfilehash: 3390cad6979858fbff73769d0d25132ba18a2157
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865614"
---
# <a name="set-the-tds-parameters"></a>Stilla TDS færibreytur

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að stilla færibreytur til að virkja Tax Deducted at Source (TDS) virkni í tilgreindum færslum. Þetta er nauðsynlegt skref til að nota eiginleikann skattur sem dreginn er frá í uppruna, TDS.

1. Farðu í **Fjárhag \> Fjárhagsuppsetning \> Fjárhagsfæribreytur**.
2. Á flipanum **Beinir skattar** í hlutanum **Skattur sem dreginn er frá í uppruna** skal stilla valkostinn **Virkja TDS** á **Já** til að virkja TDS virknina og síður og reiti sem eru notaðir fyrir það.
3. Stilltu valkostinn **Reikningur** á **Já** til að virkja reitina sem eru notaðir til að reikna út og draga TDS á reikningsstigi.
4. Veldu valkostinn **Greiðsla** á **Já** til að virkja reitina sem eru notaðir til að reikna út og draga TDS frá greiðslustiginu.

    [![Flipi beinna skatta.](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Á flipanum **Númeraraðir** finnur þú röðina þar sem reiturinn **Tilvísun** er stilltur á **Greiðsla staðgreiðsluskatts**. Í línunni **Kóði númeraraðar** fyrir línuna er kóði númeraraðarinnar valinn. Kóði númeraraðar er notaður til að mynda númer fylgiskjals fyrir reglulegt TDS-uppgjörsferli.

    > [!NOTE]
    > Til að keyra reglubundna TDC-jöfnun farið í **Skattur \> Skattskýrslur \> Staðgreiðsluskattur \> Greiðsla staðgreiðsluskatts**.

    [![Flipi númeraraðar.](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Lokið síðunni.
