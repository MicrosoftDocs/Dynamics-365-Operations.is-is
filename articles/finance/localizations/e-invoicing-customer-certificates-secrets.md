---
title: Vottorð og leynilyklar viðskiptavina
description: Þessi grein útskýrir hvernig á að setja upp viðskiptavottorð og leyndarmál í rafrænum reikningum.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a4d33135bf352a4c4a245e597e0c3c7467317864
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880661"
---
# <a name="customer-certificates-and-secrets"></a>Vottorð og leynilyklar viðskiptavina

[!include [banner](../includes/banner.md)]

Ef þú ert nú þegar með a Microsoft Azure Key Vault tilvísun í Regulatory Configuration Service (RCS), þú getur búið til tilvísanir í Key Vault vottorð og leyndarmál. Ef þú ert ekki enn með Key Vault tilvísun, sjáðu [Þjónustuumhverfi](e-invoicing-service-environments.md) til að fá upplýsingar um hvernig á að búa það til.

## <a name="create-certificates-and-secrets"></a>Búðu til vottorð og leyndarmál

Til að búa til og setja upp vottorð og leyndarmál skaltu fylgja þessum skrefum.

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á **Umhverfisuppsetning** síðu, á aðgerðarrúðunni, veldu **Þjónustuumhverfi**.
4. Á **Þjónustuumhverfi** síðu, á aðgerðarrúðunni, veldu **Helstu færibreytur Vault**.
5. Á **Helstu færibreytur Vault** síðu, veldu Key Vault tilvísun og síðan, í **Skírteini** kafla, veldu **Bæta við**.
6. Í **Nafn** reit, sláðu inn heiti Key Vault vottorðsins eða leyndarmálsins. Fyrir frekari upplýsingar, sjá [Búðu til Azure geymslureikning í Azure gáttinni](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Í reitnum **Lýsing** skal færa inn lýsingu.
8. Í **Tegund** reit, veldu **Vottorð** ef þú ert að vísa til vottorðsins sem er geymt í lyklageymslunni. Veldu **Leyndarmál** ef þú ert að vísa til leyndarmálsins sem er geymt í lyklageymslunni.
9. Veldu **Vista**.

> [!NOTE]
> Í sumum tilfellum verður þú að nota opinber vottorð sem hafa .cer skráarheiti. Hins vegar styður Key Vault ekki innflutning og geymslu vottorða af þessari gerð sem Key Vault vottorð. Í þessum tilfellum ættir þú að vista .cer skrána sem Base-64-kóðaðan X.509 (.CER) streng. Síðan, í Key Vault leyndarmáli, geymdu strenginn sem birtist á milli **BYRJA VIÐSKERT** lína og **LOKASKERT** línu í skránni. Í þjónustuumhverfinu ættir þú samt að búa til tilvísun í Key Vault færsluna og stilla **Tegund** sviði til **Vottorð**.

## <a name="create-a-chain-of-certificates"></a>Búðu til keðju vottorða

Ef lands-/svæðissérstakir reikningar þínir krefjast keðju vottorða til að beita stafrænum undirskriftum eða koma á öruggu (Secure Sockets Layer\[ SSL\]) tengingu við ytri vefþjónustu, búðu til keðju vottorða þar sem vottorðin eru í eftirfarandi röð:

1. Rótarvottorð
2. Millistigsskírteini
3. Vottorð fyrir notendur

Rótarvottorðsyfirvöld (CA) eru traust uppspretta vottorða. Millistig CA vottorð eru brýr sem tengja notendaskírteini við rót CA vottorð.

Til að búa til og setja upp keðju vottorða skaltu fylgja þessum skrefum.

1. Á **Helstu færibreytur Vault** síðu, á aðgerðarrúðunni, veldu **Keðja vottorða**.
2. Veljið **Ný** til að búa til nýja vottorðakeðju.
3. Í **Nafn** reit, sláðu inn heiti vottorðakeðjunnar.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Í hlutanum **Vottorð** skal velja **Bæta við** til að bæta vottorði við keðjuna.
6. Notið hnappinn **Upp** eða **Niður** til að breyta stöðu vottorðs í keðjunni. Hafðu CA rótarvottorðið efst á listanum og notendaskírteini neðst.
7. Veldu **Vista**.

Þú getur búið til eins margar Key Vault tilvísanir í RCS og þú vilt. Mundu að leyndarmálið fyrir SAS-táknið (Shared Access Signature) er notað til að tengja tiltekið þjónustuumhverfi við Key Vault tilvísunina. Þú getur vísað í Key Vault vottorðin og leyndarmálin sem eru geymd í lykilhólfinu sem inniheldur einnig leyndarmálið fyrir SAS geymslutáknið sem þú notar þegar þú setur upp þjónustuumhverfið.
