---
title: Vottorð og leynilyklar viðskiptavina
description: Þessi grein útskýrir hvernig á að setja upp vottorð og leynilykla viðskiptavina í rafrænni reikningsfærslu.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 3943e7cb43cc6bf93995f0b3957766227cc3ec99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279841"
---
# <a name="customer-certificates-and-secrets"></a>Vottorð og leynilyklar viðskiptavina

[!include [banner](../includes/banner.md)]

Ef þú ert nú þegar með tilvísun í Microsoft Azure lyklageymslu í Regulatory Configuration Service (RCS) er hægt að búa til tilvísanir í vottorð og leynilykla lyklageymslunnar. Ef þú ert ekki með tilvísun í lyklageymslu skaltu skoða [Þjónustuumhverfi](e-invoicing-service-environments.md) til að fá  upplýsingar um hvernig á að búa hana til.

## <a name="create-certificates-and-secrets"></a>Búa til vottorð og leynilykla

Fylgdu eftirfarandi skrefum til að búa til og setja upp vottorð.

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi**.
4. Á síðunni **Þjónustuumhverfi** á aðgerðasvæðinu skal velja **Færibreytur lyklageymslu**.
5. Á síðunni **Færibreytur lyklageymslu** skal velja tilvísun lyklageymslu og síðan í hlutanum **Vottorð** skal velja **Bæta við**.
6. Í reitinn **Heiti** skal slá inn heiti á vottorði eða leynilykli lyklageymslunnar. Frekari upplýsingar eru í [Stofna Azure-geymslureikning í Azure-gáttinni](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Í reitnum **Lýsing** skal færa inn lýsingu.
8. Í reitnum **Tegund** skal velja **Vottorð** ef vísað er í vottorðið sem geymt er í lyklageymslunni. Veldu **Leynilykill** ef vísað er í leynilykilinn sem geymdur er í lyklageymslunni.
9. Veldu **Vista**.

> [!NOTE]
> Í sumum aðstæðum þarftu að nota almenn vottorð sem eru með skráarendinguna .cer. Hins vegar styður lyklageymslan ekki innflutning og geymslu vottorða af þessari gerð sem vottorð lyklageymslu. Í þessum aðstæðum ættir að vista .cer-skrána sem Base-64 kóðaðan X.509 (.CER) streng. Í leynilykli lyklageymslu skal síðan geyma strenginn sem birtist á milli línanna **HEFJA VOTTORÐ** og **LJÚKA VOTTORÐI** í skránni. Í þjónustuumhverfinu ættir þú samt að búa til tilvísun í færslu lyklageymslunnar og stilla reitinn **Gerð** á **Vottorð**.

## <a name="create-a-chain-of-certificates"></a>Búa til vottorðakeðju

Ef lands-/svæðisbundnir reikningar þínir þurfa vottorðakeðju til að nota stafræna undirskrift eða koma á öruggri (Secure Socket Layer \[SSL\]) tengingu við ytri vefþjónustur skal búa til vottorðakeðju þar sem vottorðin eru í eftirfarandi röð:

1. Rótarvottorð
2. Millivottorð
3. Notandavottorð

Yfirvöld rótarvottorðs eru traustur uppruni vottorða. Vottorð millivottunaraðila eru brýr sem tengja vottorð notanda við vottorð rótarvottunaraðila.

Fylgdu eftirfarandi skrefum til að búa til og setja upp vottorðakeðju.

1. Á síðunni **Færibreytur lyklageymslu** á aðgerðasvæðinu skal velja **Vottorðakeðja**.
2. Veljið **Ný** til að búa til nýja vottorðakeðju.
3. Í reitinn **Heiti** skal færa inn heiti vottorðakeðjunnar.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Í hlutanum **Vottorð** skal velja **Bæta við** til að bæta vottorði við keðjuna.
6. Notið hnappinn **Upp** eða **Niður** til að breyta stöðu vottorðs í keðjunni. Haltu rótarvottorði vottorðaútgefanda efst á listanum og vottorði notanda neðst.
7. Veldu **Vista**.

Hægt er að búa til eins margar tilvísanir í lyklageymslu í RCS og þörf er á. Mundu að leynilykillinn fyrir SAS-lykilinn er notaður til að tengja tiltekið þjónustuumhverfi við tilvísun lyklageymslunnar. Hægt er að vísa í vottorð og leynilykla lyklageymslunnar sem geymd eru í lyklageymslu sem inniheldur einnig leynilykilinn fyrir SAS-lykilinn sem er notaður þegar þjónustuumhverfið er sett upp.
