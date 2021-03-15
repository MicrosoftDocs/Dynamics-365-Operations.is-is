---
title: Vsk-greiðslur og sléttunarreglur
description: Þessi grein útskýrir hvernig uppsetning sléttunarreglu á Skattyfirvöld gengur fyrir sig og hvernig á að slétta virðisaukaskatt í ferlinu Jafna og bóka virðisaukaskatt.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8d7e402614b35a77a0283d31377a073b0a6b357
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990190"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Vsk-greiðslur og sléttunarreglur

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig uppsetning sléttunarreglu á Skattyfirvöld gengur fyrir sig og hvernig á að slétta virðisaukaskatt í ferlinu Jafna og bóka virðisaukaskatt.

Reglulega þarf að tilkynna vsk og greiða hann til skattayfirvalda. Þetta er gert með því að keyra í jafna og bóka vsk-ferlið á síðunni Virðisaukaskattur. Virðisaukaskattur fyrir tímabilið verða jafnaðar á móti lyklum virðisaukaskatts og staða virðisaukaskatts verður bókuð í lykilinn fyrir jöfnun vsk. Stöðu virðisaukaskatts sem er bókuð í VSK-lykilinn er hægt slétta eins og krafist er á af skattayfirvöldum með því að setja upp sléttunarreglu á síðunni Virðisaukaskattur. 

Sléttunarmismunur er bókaður á VSK-sléttunarlykil sem er valinn í lyklum fyrir sjálfvirkar færslur í reitnum Fjárhagur.

Dæmið hér að neðan sýnir hvernig sléttunarreglan á virðisaukaskattsyfirvöld virkar.

## <a name="examples"></a>Dæmi

Heildarupphæð VSK fyrir tímabil sýnir kreditstöðu-98,765.43. Lögaðili innheimti hærri virðisaukaskattsupphæð en hann greiddi. Þess vegna skuldar lögaðili peninga til skattyfirvalda. 

Fyrirtækið vill nota sléttunaraðferð sem sléttar stöðuna í næstu 1,00 EUR. Starfsmaðurinn sem ber ábyrgð á VSK-bókhaldi framkvæmir eftirfarandi skref.

1. Fara á **Skattur** > **Óbeinir skattar** > **Virðisaukaskattur** > **Virðisaukaskattsyfirvöld**.
2. Í flýtiflipanum **Almennt**, í reitnum **Sléttunarregla** skal velja **Eðlilegt**.
3. Í reitinn **Sléttun** skal slá inn 1,00.
4. Þegar tími er kominn til að greiða skattyfirvöldum VSK-skattinn skal opna **Skattur** > **Skattframtöl** > **Virðisaukaskattur** > **Jafna og bóka virðisaukaskatt**. Í vsk-jöfnunarlykli má sjá að upphæð skattskuldar upp á **98.765,43** er sléttuð í **98.765**.

Eftirfarandi tafla sýnir hvernig upphæðin 98.765,43 er sléttuð með því að nota hverja sléttunaraðferð sem tiltæk er í svæðið **Sléttunarregla** á síðunni **Skattayfirvöld**.

> [!NOTE]                                                                                  
> Ef sléttunargildið er stillt á 0,00 verður:
>
> - Fyrir eðlilega sléttun verður sléttunin sú sama og fyrir **Sléttun = 0,01**.
> - Fyrir **Valkostir sléttunarreglu**, **Niður á við**, **Upp á við** og **Í eigin hag** er hegðunin sú sama og fyrir **Sléttun = 1,00**.

| Skjámyndavalkostur fyrir sléttun                | Námunda markaðsvirði = 0,01 | Námunda markaðsvirði = 0,10 | Námunda markaðsvirði = 1,00 | Námunda markaðsvirði = 100,00 | Námunda markaðsvirði = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Venjulegt                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Slétta niður                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Slétta upp                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Eigin hagur fyrir kreditstöðu | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Eigin hagur fyrir debetstöðu  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

### <a name="normal-round-and-round-precision-is-001"></a>Venjuleg sléttun og sléttunarnákvæmni er 0,01

<table>
  <tr>
    <td>Sléttun
    </td>
    <td>Ferli útreiknings
    </td>
  </tr>
    <tr>
    <td>sléttun(1,015, 0,01) = 1,02
    </td>
    <td>
      <ol>
        <li>sléttun(1,015 / 0,01, 0) = sléttun(101,5, 0) = 102
        </li>
        <li>102 * 0,01 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>sléttun(1,014, 0,01) = 1,01
    </td>
    <td> <ol>
        <li>sléttun(1,014 / 0,01, 0) = sléttun(101,4, 0) = 101
        </li>
        <li>101 * 0,01 = 1,01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>sléttun(1,011, 0,02) = 1,02
    </td>
    <td> <ol>
        <li>sléttun(1,011 / 0,02, 0) = sléttun(50,55, 0) = 51
        </li>
        <li>51 * 0,02 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>sléttun(1,009, 0,02) = 1,00
    </td>
    <td> <ol>
        <li>sléttun(1,009 / 0,02, 0) = sléttun(50,45, 0) = 50
        </li>
        <li>50 * 0,02 = 1,00
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> Ef þú velur Eigin hagur er sléttun alltaf í hag lögaðila. 

Frekari upplýsingar er hægt að finna í eftirfarandi efni:
- [Yfirlit virðisaukaskatts](indirect-taxes-overview.md)
- [Stofna VSK-greiðslu](tasks/create-sales-tax-payment.md)
- [Stofna VSK-færslur í skjölum](tasks/create-sales-tax-transactions-documents.md)
- [Skoða bókaðar VSK-færslur](tasks/view-posted-sales-tax-transactions.md)
- [sléttunarvirkni](https://msdn.microsoft.com/library/aa850656.aspx)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]