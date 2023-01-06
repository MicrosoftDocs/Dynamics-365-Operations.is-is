---
title: Skattur er bókaður í rangan fjárhagslykil í fylgiskjalinu
description: Þessi grein veitir upplýsingar um úrræðaleit sem getur hjálpað til þegar skattur er bókaður á rangan fjárhagslykil í fylgiskjalinu.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 5eb0f7d0196ac52a87d61cba6b9cd438708eff73
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846742"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Skattur er bókaður í rangan fjárhagslykil í fylgiskjalinu

[!include [banner](../includes/banner.md)]

Meðan á bókun stendur gæti skattur verið bókaður á rangan fjárhagslykil í fylgiskjalinu. Til að leysa úr vandamálinu skal fylgja skrefunum í eftirfarandi hlutum eftir þörfum. Dæmin í þessari grein nota sölupöntun sem viðskiptaskjal.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Finndu skattkóðann fyrir ranglega bókaða skattfærslu

1. Á síðunni **Fylgiskjalafærslur** skal velja færsluna sem vinna á með og velja síðan **Bókaður virðisaukaskattur**.

    [![Hnappur bókaðs virðisaukaskatts á síðunni fyrir fylgiskjalsfærslu.](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. Farið yfir gildið í reitnum **VSK-kóði**. Í þessu dæmi er það **VSK 19**.

    [![Reiturinn VSK-kóði á síðunni Bókaður virðisaukaskattur.](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Athugaðu fjárhagsbókunarflokk skattkóðans

1. Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkur**.
2. Finndu og veldu skattkóðann og farðu síðan yfir gildið í reitnum **Fjárhagsbókunarflokkur**. Í þessu dæmi er það **VSK**.

    [![Reitur fjárhagsbókunarflokks á síðu VSK-kóða.](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. Gildið í svæðinu **Fjárhagsbókunarflokkur** er tengill. Veldu tengilinn til að skoða upplýsingar um stillingar hópsins. Einnig er hægt að velja og halda niðri (eða hægrismella) í reitnum og velja síðan **Skoða upplýsingar**.

    [![Skoða upplýsingar um skipun.](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. Í reitnum **Útskattur** skal staðfesta að reikningsnúmerið sé rétt samkvæmt færslugerðinni. Ef svo er ekki skal velja rétta lykilinn sem á að bóka á. Í þessu dæmi er virðisaukaskattur sölupöntunarinnar færður á virðisaukaskattslyjkil 222200.

    [![Reitur útskatts á síðu fjárhagsbókunarflokks.](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    Í eftirfarandi töflu má finna upplýsingar um hvert svæði á síðunni **Fjárhagsbókunarflokkar**.

    | Svæði                  | lýsing |
    |------------------------|-------------|
    | Útskattur      | Aðallykil fyrir útskatt sem er til greiðslu til skattyfirvalda. |
    | Innskattur   | Aðallykill fyrir innskatt sem er móttekinn frá skattyfirvöldum. |
    | Kostnaður neysluskatts        | Aðallykillinn sem er notaður til að bóka frádráttarbæran neysluskatt sem lánardrottnar gera ekki kröfu um eða gefa upp til skattayfirvalda sem hluti af bakfærðum gjöldum vöru- og þjónustuskatts (ÞST)/Samræmdum virðisaukaskatti Evrópusambandsins. **Neysluskattur** verður að vera valinn fyrir VSK-kóði í VSK-flokkur sem er notaður í færslunni. Þetta svæði er ekki tiltækt ef **Reglur fyrir beitingu skattlagningu söluskatts** er valinn á síðunni **Færibreytur fjárhags**. |
    | Neysluskattur út        | Aðallykillinn sem er notaður til að bóka neysluskatt á innleið sem greiða á skattayfirvöldum. |
    | Jöfnunarlykill     | Aðallykillinn sem er notaður til að bóka nettóstöðu fjárhagslykla sem eru tilgreindir í reitunum **Útskattur** og **Innskattur**. |
    | Staðgreiðsluafsláttur lánardrottins   | Aðallykillinn sem er notaður til að bóka staðgreiðsluafslátt fyrir VSK-kóða sem tengjast þessum fjárhagsbókunarflokki. |
    | Staðgreiðsluafsláttur viðskiptavinar | Aðallykillinn sem er notaður til að bóka staðgreiðsluafslátt fyrir VSK-kóða sem tengjast þessum fjárhagsbókunarflokki. |

    Nánari upplýsingar er að finna í [Setja upp bókunarflokka virðisaukaskatts](tasks/set-up-ledger-posting-groups-sales-tax.md)

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Kema í kóða til að athuga fjárhagsvíddir

Í kóðanum er bókunarreikningurinn ákvarðaður af fjárhagsvíddinni. Fjárhagsvíddin vistar kenni aðgangs í gagnagrunninum.

1. Fyrir sölupöntun skal bæta rofstað við í aðferðunum **Tax::saveAndPost()** and **Tax::post()**. Takið eftir gildi **\_ledgerDimension**.

    [![Dæmi um kóða sölupöntunar sem er með rofstað.](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    Fyrir innkaupapöntun skal bæta við rofstað við **TaxPost::saveAndPost()** og **TaxPost::postToTaxTrans()** aðferðirnar. Takið eftir gildi **\_ledgerDimension**.

    [![Dæmi um kóða innkaupapöntunar sem er með rofstað.](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Keyrðu eftirfarandi SQL-fyrirspurn til að finna birtingargildi reikningsins í gagnagrunninum, byggt á færslukenninu sem er vistað í fjárhagsvíddinni.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Birta gildi færsluauðkennisins.](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. Skoðaðu kallastakka til að finna hvar **_ledgerDimension** gildinu er úthlutað. Vanalega er gildið frá **TmpTaxWorkTrans**. Í þessu tilviki ætti að bæta rofstað við **TmpTaxWorkTrans::insert()** og **TmpTaxWorkTrans::update()** til að sjá hvar gildinu er úthlutað.

## <a name="determine-whether-customization-exists"></a>Ákvarða hvort sérstilling sé til staðar

Ef þú hefur lokið við skrefin í fyrri hlutum en hefur ekki getað leyst vandamálið skaltu komast að því hvort sérstillingar séu til staðar. Ef engin sérstilling er til skal stofna þjónustubeiðni frá Microsoft til að fá frekari aðstoð.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
