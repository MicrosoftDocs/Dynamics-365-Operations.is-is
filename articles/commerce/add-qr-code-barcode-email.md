---
title: Bæta QR-kóða eða strikamerki við tölvupósta sem tengjast færslum eða kvittunum
description: Þetta efnisatriði útskýrir hvernig á að setja QR-kóða og strikamerki sem standa fyrir auðkenni pantana inn í tölvupósta sem tengjast færslum og kvittunum í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9a3ab355d6e68221610e48e02e191c1d21f5155db81990d0991a8c353f3f9ecd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729939"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>Bæta QR-kóða eða strikamerki við tölvupósta sem tengjast færslum eða kvittunum

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja QR-kóða og strikamerki sem standa fyrir auðkenni pantana inn í tölvupósta sem tengjast færslum og kvittunum í Microsoft Dynamics 365 Commerce.

Auðvelt er að hafa með QR-kóða og strikamerki í tölvupóstum sem tengjast færslum til að flýta fyrir uppflettingu pöntunar í smásöluumhverfi. Til að setja QR-kóða og strikamerki inn í tölvupósta skal nota HTML-merki **\<img\>** sem biður um mynd af QR-kóða og strikamerki frá myndþýðingarþjónustu. Microsoft býður ekki upp á þessa þjónustu. Hins vegar eru til margar ókeypis eða ódýrar þjónustur sem geta afgreitt QR-kóða eða strikamerki sem eru mynduð sjálfkrafa samkvæmt gildi sem gefið er upp í fyrirspurnarstreng.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>Bæta QR-kóða eða strikamerki við tölvupóst sem tengist færslu

Til að bæta QR-kóða eða strikamerki við færslutengdan tölvupóst sem er sendur sem hluti af rafrænum viðskiptum skal fylgja þessum skrefum.

1. Opnið upprunalegt HTML fyrir sniðmát færslutölvupósts og bætið við HTML-merki **\<img\>** sem vísar á QR-kóða- eða strikamerkjaþjónustuna. Eftirfarandi er dæmi.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Hér er skýring á fyrrgreindu dæmi:

    - **ÞÍN\_QR\_KÓÐA\_STRIKA\_MERKJA\_ÞJÓNUSTA** stendur fyrir lén QR-kóða- eða strikamerkjaþjónustunnar.
    - **gögn** standa fyrir færibreytuna sem QR-kóða- eða strikamerkjaþjónustan notar til að taka við efninu sem á að breyta í QR-kóða eða strikamerki.

        Gildinu **%salesid%** verður að vera úthlutað á þessa færibreytu. Takið eftir að í þessu dæmi er gildið einnig notað sem baktexti fyrir myndina.

    - **param1** og **param2** standa fyrir aukalegar, valfrjálsar færibreytur.

1. Farið í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Sniðmát tölvupósts fyrirtækis** og hlaðið upp uppfærðu HTML í viðeigandi sniðmát færslutölvupósts.

> [!NOTE]
> Færibreytur gæti verið mismunandi á milli þjónustanna sem bjóða upp á QR-kóða og strikamerki. Því skal hafa samband við þjónustuveituna til að staðfesta færibreyturnar sem þarf að úthluta gildum til.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>Bæta QR-kóða eða strikamerki við tölvupóst sem tengist kvittun 

Til að setja QR-kóða eða strikamerki inn í tölvupóst kvittunar sem hægt er að senda að loknum kaupum á sölustað (POS) skal fylgja þessum skrefum.

1. Opnið upprunalegt HTML fyrir sniðmát kvittunartölvupósts og bætið við HTML-merki **\<img\>** sem vísar á QR-kóða- eða strikamerkjaþjónustuna. Hér fyrir neðan er dæmi.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Hér er skýring á fyrrgreindu dæmi:

    - **ÞÍN\_QR\_KÓÐA\_STRIKA\_MERKJA\_ÞJÓNUSTA** stendur fyrir lén QR-kóða- eða strikamerkjaþjónustunnar.
    - **gögn** standa fyrir færibreytuna sem QR-kóða- eða strikamerkjaþjónustan notar til að taka við efninu sem á að breyta í QR-kóða eða strikamerki.

        Gildinu **%receiptid%** verður að vera úthlutað á þessa færibreytu. Takið eftir að í þessu dæmi er gildið einnig notað sem baktexti fyrir myndina.

    - **param1** og **param2** standa fyrir aukalegar, valfrjálsar færibreytur.

1. Farið í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Sniðmát tölvupósts fyrirtækis** og hlaðið upp uppfærðu HTML í tölvupóstssniðmátið sem er með tölvupóstskennið **emailrecpt**.

> [!NOTE]
> Færibreytur gæti verið mismunandi á milli þjónustanna sem bjóða upp á QR-kóða og strikamerki. Því skal hafa samband við þjónustuveituna til að staðfesta færibreyturnar sem þarf að úthluta gildum til.

## <a name="additional-resources"></a>Frekari upplýsingar

[Senda kvittanir í tölvupósti frá Modern POS (MPOS)](email-receipts.md)

[Stofna sniðmát fyrir tölvupóst fyrir færslutilvik](email-templates-transactions.md)
