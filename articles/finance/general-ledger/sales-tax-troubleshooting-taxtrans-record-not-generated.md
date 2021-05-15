---
title: TaxTrans færsla er ekki mynduð
description: Í þessu efni eru upplýsingar um villuleit sem geta hjálpað þegar TaxTrans færsla er ekki búin til.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947655"
---
# <a name="taxtrans-record-isnt-generated"></a>TaxTrans færsla er ekki mynduð

[!include [banner](../includes/banner.md)]

Ef þú velur **Bókaður virðisaukaskattur** fyrir færslu en síðan **Bókaður virðisaukaskattur** sýnir annaðhvort engar skattlínur eða vantar skattlínu gæti verið að færslan **TaxTrans** hafi ekki verið búin til.

[![Síða bókaðs virðisaukaskatts sem er með engin línuatriði](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Til að leysa úr vandamálinu skal fylgja skrefunum í eftirfarandi hlutum eftir þörfum.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Athugaðu söluskattinn áður en færslan er bókuð

1. Áður en færslan er bókuð skal á síðunni **Bókun reiknings** velja **Virðisaukaskattur** til að athuga útreikninginn.

    [![Hnappur virðisaukaskatts á bókunarsíðu reiknings](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. Farðu yfir niðurstöður útreikningsins á síðunni **Tímabundnar VSK-færslur**. Ef enginn skattur er reiknaður skal skoða [Skattur er ekki reiknaður eða skattupphæð er núll](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Finndu TaxTrans færsluna í öllum bókuðum virðisaukaskatti

1. Farið í **Skattur** \> **Fyrirspurnir og skýrslur** \> **Fyrirspurn um virðisaukaskatt** > **Bókaður virðisaukaskattur**.
2. Í dálkahausnum **Fylgiskjal** skal velja síumerkið til að finna færsluna **TaxTrans**.
3. Skoðaðu dagsetninguna ef þú finnur þær söluskattsfærslur sem leitað er að. Ef dagsetningin er frábrugðin dagsetningu færslubókarhauss skal stofna þjónustubeiðni Microsoft til að fá frekari aðstoð.

    [![Síðan Bókaður virðisaukaskattur](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Kemba til að athuga upplýsingar

1. Frekari upplýsingar um hvernig á að kemba og ákveða hvort **TmpTaxWorkTrans** og **TaxUncommitted** séu búin til á réttan hátt er að finna í [Reitargildi í TaxTrans er ekki rétt](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. Ef **TaxTmpWorkTrans** eða **TaxUncommitted** eru búin til á réttan hátt skal bæta við rofstað á **TaxPost::SaveAndPost()** og **Tax::SaveAndPost** til að kemba ástæðuna fyrir því af hverju **TaxTrans** er ekki sett inn.

    [![Rofstöðum bætt við í kóða](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Niðurstöður rofstaða sem bætt var við](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Ákvarða hvort sérstilling sé til staðar

Ef þú hefur lokið við skrefin í fyrri hlutum en hefur ekki getað leyst vandamálið skaltu komast að því hvort sérstillingar séu til staðar. Ef engin sérstilling er til skal stofna þjónustubeiðni frá Microsoft til að fá frekari aðstoð.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
