---
title: "Stofna þjónustupantanir handvirkt"
description: "Þú getur búið til þjónustupantanir handvirkt með því að nota þjónustusamning eða með því að nota **þjónustupantanir** skjámyndina."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a0cc6b2646929776f4efb20474de6b0fc5c4719c
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-orders-manually"></a>Stofna þjónustupantanir handvirkt    

[!include [banner](../includes/banner.md)]


Þú getur búið til þjónustupantanir handvirkt með því að nota þjónustusamning eða með því að nota **þjónustupantanir** skjámyndina. Einnig er hægt að stofna þjónustupöntun úr verki.

> [!TIP]
> <P>Þú getur notað sjálfvirk ferli til að búa til þjónustupantanir. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Búðu til þjónustupöntun handvirkt út frá þjónustusamningi

1.  Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.

2.  Veljið þjónustusamning eða stofnið nýjan þjónustusamning.

3.  Smelltu á flipann **Afhenda** og í **Stofna** hópnum skal smella á **Skipulögð þjónustupantanir** til að opna **Stofna þjónustupantanir** skjámynd.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Stofna þjónustupöntun handvirkt í skjámyndinni Þjónustupantanir

1.  Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.

2.  Styðjið á CTRL+N til að stofna nýja þjónustupöntun.

3.  Stofnið þjónustupöntunarlínur fyrir þjónustupöntunina.

> [!NOTE]
> <P>Ef valinn er gátreitur <STRONG>Leyfa án þjónustusamnings</STRONG> í skjámyndinni <STRONG>Færibreytur þjónustustjórnunar</STRONG> getur þú sent færslurnar frá þjónustupöntunarlínunum án þess að tengja þjónustupöntunina við þjónustusamning. Ef gátreiturinn er hreinsaður verður í það minnsta að tengja þjónustupöntunina, sem var stofnuð handvirkt, við verk áður en þjónustupöntunarlínurnar eru bókaðar.</P>

## <a name="create-a-service-order-from-a-project"></a>Búðu til þjónustupöntun frá verkefni

1.  Smelltu á **Verkefnastjórnun og bókhald** \> **Almenn** \> **Verkefni** \> **Öll verkefni**.

2.  Í **Verkefni** skjámynd, á **Aðgerðarúðu**, smelltu á **Stjórna** flipann \> smella **Þjónusta** \> **Þjónustupantanir**.

3.  Fylgja fyrri aðferð til að búa til þjónustupöntun handvirkt í **þjónustupantanir** skjámynd. **Auðkenni verkefnis** reitinn sýnir verkefni tilvísun.

> [!NOTE]
> <P>Ef valinn er gátreitur <STRONG>Leyfa án þjónustusamnings</STRONG> í skjámyndinni <STRONG>Færibreytur þjónustustjórnunar</STRONG> getur þú sent færslurnar frá þjónustupöntunarlínunum án þess að tengja þjónustupöntunina við þjónustusamning. Ef gátreiturinn er hreinsaður verður í það minnsta að tengja þjónustupöntunina, sem var stofnuð handvirkt, við verk áður en þjónustupöntunarlínurnar eru bókaðar.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Búðu til þjónustupöntun út frá sölupöntunarskjámynd

Þú getur búið til þjónustupöntun út frá **Sölupantanir** skjámynd með því að nota **Stofna nýjan þjónustupöntun sem byggist á sölupöntunar** hjálpinni.

1.  Smellið á **Sala og markaðssetning** \> **Almennt** \> **Sölupantanir** \> **Allar sölupantanir**.

2.  Viðeigandi sölupöntun er opnuð.

3.  Á **Sölupöntun** flipanum smelltu á **Þjónustupöntun** til að hefja **Stofna nýjan þjónustupöntun sem byggist á sölupöntun** hjálpinni.

4.  Smelltu á **Næsta \>**, og svo ljúka eftirfarandi skrefum á **Veldu samkomulag um þjónustupöntun** síðunni:
    
      - Notaðu **þjónustusamningur** reitinn til að velja þjónustusamninginn sem ætti að tengja nýja þjónustupöntunina við.
    
      - Valfrjálst: Notaðu **Auðkenni verkefnis** reitinn til að tengja þessa þjónustupöntun við tiltekið verkefni.

5.  Smelltu á **Næsta \>** , og svo ljúka eftirfarandi skrefum á **Stofna þjónustupöntun** síðunni:
    
      - Sláðu inn dagsetningu og tíma fyrir þjónustusímtalið í reitnum **Valinn þjónustutími** reitinn.
    
      - Valfrjálst: Breyttu textanum í **Lýsing** reitnum. Sjálfgefið inniheldur þetta reitur lýsingu á þjónustusamningnum sem þú valdir á fyrri síðunni.
    
      - Í **Ábyrgur** reitinn, velja Kenni starfsmanns sem ber ábyrgð á samningnum, og ef þú veist hvað það er, slá inn Kenni valinn tæknimaður viðskiptavinarins fyrir þjónustusímtali.
    
      - Í **Kenni tengiliðar** reitinn, velja einstakling í fyrirtæki viðskiptavinarins sem ætti að hafa samband við varðandi þessa þjónustupöntun.

6.  Smella á **Næsta \>** og smella síðan á **Ljúka**.


## <a name="see-also"></a>Sjá einnig

[Þjónustupantanir](service-orders.md)

[Stofna þjónustupantanir sjálfkrafa](create-service-orders-automatically.md)

[Stofna þjónustupantanir (klasaskjámynd)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\)) 


