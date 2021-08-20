---
title: Stilla TDS færibreytur
description: Þetta efnisatriði útskýrir hvernig á að stilla færibreytur til að virkja virkni skattur sem dreginn er frá í uppruna (TDS) í tilgreindum færslum. Þetta er nauðsynlegt skref til að nota eiginleikann skattur sem dreginn er frá í uppruna, TDS.
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
ms.openlocfilehash: b74a1ab6d0f17367fc16f795e1b28ff5d0c5508e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358243"
---
# <a name="set-the-tds-parameters"></a>Stilla TDS færibreytur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að stilla færibreytur til að virkja virkni skattur sem dreginn er frá í uppruna (TDS) í tilgreindum færslum. Þetta er nauðsynlegt skref til að nota eiginleikann skattur sem dreginn er frá í uppruna, TDS.

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