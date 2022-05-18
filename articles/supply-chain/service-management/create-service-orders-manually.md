---
title: Stofna þjónustupantanir handvirkt
description: Þú getur búið til þjónustupantanir handvirkt með því að nota þjónustusamning eða með því að nota **þjónustupantanir** skjámyndina.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f969e3de9586c0c47214201b34a16f8afad5ca90
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678263"
---
# <a name="create-service-orders-manually"></a>Stofna þjónustupantanir handvirkt    

[!include [banner](../includes/banner.md)]


Þú getur búið til þjónustupantanir handvirkt með því að nota þjónustusamning eða með því að nota **þjónustupantanir** skjámyndina. Einnig er hægt að stofna þjónustupöntun úr verki.

> [!TIP]
> <P>Þú getur notað sjálfvirk ferli til að búa til þjónustupantanir. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Búðu til þjónustupöntun handvirkt út frá þjónustusamningi

1.  Veljið **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.

2.  Veljið þjónustusamning eða stofnið nýjan þjónustusamning.

3.  Veljið **Afhenda** flipann og í **Stofna** hópnum skal velja **Skipulögð þjónustupantanir** til að opna skjámyndina **Stofna þjónustupantanir**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Stofna þjónustupöntun handvirkt í skjámyndinni Þjónustupantanir

1.  Veljið **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.

2.  Veljið **Nýtt** til að stofna nýja þjónustupöntun.

3.  Stofnið þjónustupöntunarlínur fyrir þjónustupöntunina.

> [!NOTE]
> <P>Ef valinn er gátreitur <STRONG>Leyfa án þjónustusamnings</STRONG> í skjámyndinni <STRONG>Færibreytur þjónustustjórnunar</STRONG> getur þú sent færslurnar frá þjónustupöntunarlínunum án þess að tengja þjónustupöntunina við þjónustusamning. Ef gátreiturinn er hreinsaður verður í það minnsta að tengja þjónustupöntunina, sem var stofnuð handvirkt, við verk áður en þjónustupöntunarlínurnar eru bókaðar.</P>

## <a name="create-a-service-order-from-a-project"></a>Búðu til þjónustupöntun frá verkefni

1.  Opnið **Verkefnastjórnun og bókhald** \> **Almennt** \> **Verk** \> **Öll verk**.

2.  Í **Verkefni** skjámynd, á **Aðgerðasvæði** skal velja **Stjórna** flipann \> velja **Þjónusta** \> **Þjónustupantanir**.

3.  Fylgja fyrri aðferð til að búa til þjónustupöntun handvirkt í **þjónustupantanir** skjámynd. **Auðkenni verkefnis** reitinn sýnir verkefni tilvísun.

> [!NOTE]
> <P>Ef valinn er gátreitur <STRONG>Leyfa án þjónustusamnings</STRONG> í skjámyndinni <STRONG>Færibreytur þjónustustjórnunar</STRONG> getur þú sent færslurnar frá þjónustupöntunarlínunum án þess að tengja þjónustupöntunina við þjónustusamning. Ef gátreiturinn er hreinsaður verður í það minnsta að tengja þjónustupöntunina, sem var stofnuð handvirkt, við verk áður en þjónustupöntunarlínurnar eru bókaðar.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Búðu til þjónustupöntun út frá sölupöntunarskjámynd

Þú getur búið til þjónustupöntun út frá **Sölupantanir** skjámynd með því að nota **Stofna nýjan þjónustupöntun sem byggist á sölupöntunar** hjálpinni.

1.  Farðu í **Sala og markaðssetning** \> **Almennt** \> **Sölupantanir** \> **Allar sölupantanir**.

2.  Viðeigandi sölupöntun er opnuð.

3.  Á **Sölupöntun** flipanum skal velja **Þjónustupöntun** til að hefja **Stofna nýjan þjónustupöntun sem byggist á sölupöntun** hjálpinni.

4.  Veljið **Næsta \>**, og ljúkið svo eftirfarandi skrefum á **Veldu samkomulag um þjónustupöntun** síðunni:
    
      - Notaðu **þjónustusamningur** reitinn til að velja þjónustusamninginn sem ætti að tengja nýja þjónustupöntunina við.
    
      - Valfrjálst: Notaðu **Auðkenni verkefnis** reitinn til að tengja þessa þjónustupöntun við tiltekið verkefni.

5.  Veljið **Næsta \>**, og ljúkið svo eftirfarandi skrefum á **Stofna þjónustupöntun** síðunni:
    
      - Sláðu inn dagsetningu og tíma fyrir þjónustusímtalið í reitnum **Valinn þjónustutími** reitinn.
    
      - Valfrjálst: Breyttu textanum í **Lýsing** reitnum. Sjálfgefið inniheldur þetta reitur lýsingu á þjónustusamningnum sem þú valdir á fyrri síðunni.
    
      - Í **Ábyrgur** reitinn, velja Kenni starfsmanns sem ber ábyrgð á samningnum, og ef þú veist hvað það er, slá inn Kenni valinn tæknimaður viðskiptavinarins fyrir þjónustusímtali.
    
      - Í **Kenni tengiliðar** reitinn, velja einstakling í fyrirtæki viðskiptavinarins sem ætti að hafa samband við varðandi þessa þjónustupöntun.

6.  Veljið **Næsta \>** og svo **Ljúka**.


## <a name="see-also"></a>Sjá einnig

[Þjónustupantanir](service-orders.md)

[Stofna þjónustupantanir sjálfkrafa](create-service-orders-automatically.md)

[Stofna þjónustupantanir (klasaskjámynd)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]