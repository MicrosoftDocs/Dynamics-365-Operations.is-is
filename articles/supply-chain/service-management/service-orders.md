---
title: Þjónustupantanir
description: Þetta efnisatriði veitir yfirsýn yfir hvernig á að vinna með þjónustupantanir.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8dc88d445e1331e1532cb3b7385cda39c4f22e80
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566120"
---
# <a name="service-orders"></a>Þjónustupantanir

[!include [banner](../includes/banner.md)]

Þjónustupöntun táknar heimsókn sem þjónustutæknimaður fer í til viðskiptavinar á tilteknum degi. Hver þjónustupöntun samanstendur af einni eða fleiri þjónustupöntunarlínum. Þjónustupöntunarlínur tákna fjölda vinnustunda sem þjónustutæknar þurfa að inna af hendi, og tengda hluti, gjöld og þóknanir.

Þú getur tengt verkefni og hluti við þjónustupöntunarlínu. Þú getur síðan flokkað þjónustupöntunarlínur eftir verkefni eða hlut. Þú getur einnig tengt hluti sem eru skráðir í birgðum við þjónustupöntunarlínur.

## <a name="create-service-orders"></a>Stofna þjónustupantanir

Þú getur stofnað þjónustupantanir sem byggjast á þjónustusamningi og línunum sem eru í þeim samningi. Þú getur hins vegar búið til þjónustupantanir sem tengjast þjónustusamningi aðeins á því tímabili sem tilgreint er í samningnum. Til dæmis, ef þjónustusamningur gildir fyrir almanaksárið 2011, getur þú stofnað þjónustupantanir fyrir samninginn frá 1. janúar 2011 til 31. desember 2011.

Þú getur einnig stofnað þjónustupantanir hverja fyrir sig, án þess að tengja þær við samning. Þessar þjónustupantanir geta verið notaðar til að meðhöndla óundirbúnar eða stakar þjónustuheimsóknir. Til dæmis, í marsmánuði, vill viðskiptavinurinn að þjónusta sé framkvæmd á tveimur vélum, auk þeirra véla sem eru tilgreindar í þjónustusamningnum. Í þessu verkefni stofnar þú þjónustupantanir en tengir þær ekki við samning.


> [!NOTE]
> Til að búa til þjónustubeiðnir sem ekki tengjast þjónustusamningi þarftu að velja gátreitinn **Leyfa án þjónustusamnings** í síðunni **Færibreytur þjónustustjórnunar**.

### <a name="scenario"></a>Aðstæður

Eftirfarandi atburðarás lýsir öðrum aðstæðum þar sem það er gagnlegt að stofna þjónustupöntun sem ekki er tengd þjónustusamningi.

Fyrirtækissendandinn fær símtal þar sem beðið er um neyðarþjónustu í lyftu. Það er ekki tími til að setja upp þjónustusamning og verkefni fyrir þjónustuna. Þess vegna stofnar afgreiðslustjórinn þjónustupöntun beint á síðunni **Þjónustupantanir**, tengir þjónustupöntunina við verkefni sem er til staðar og stofnar þjónustupöntunarlínur. Sendandinn stofnar einnig verkefni eða hlutatengsl við þjónustupöntun sem er til staðar, til að skrá vinnu sem ekki tengist þjónustusamningnum. Nánari upplýsingar er að finna í: [Stofna þjónustupantanir handvirkt](create-service-orders-manually.md) og [Stofna tengsl þjónustuverks](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>Fylgjast með framvindu þjónustupantana

Til að fylgjast með framvindu þjónustupantana í gegnum mismunandi hópa og vinnuferla, er hægt að setja upp kerfi sem byggist á stigum og ástæðukóðum fyrir þjónustupantanir. Fyrir hvert stig er hægt að tilgreina aðgerðir sem eru leyfðar. Nánari upplýsingar er að finna í [Stofna ástæðukóða](create-reason-codes.md).

### <a name="example"></a>Dæmi

Þjónustupöntun er samþykkt af sendanda. Sendandinn uppfærir stig þjónustupöntunar og tilgreinir ástæðukóða sem gefur til kynna að þjónustupöntunin hafi verið gefin út til þjónustutæknimanns. Tæknimaðurinn fer til viðskiptavinar og sinnir þjónustunni.

## <a name="specify-item-requirements-for-service-orders"></a>Tilgreina vöruþarfir fyrir þjónustupantanir

Þú getur tilgreint birgðavörurnar sem eru nauðsynlegar fyrir þjónustupöntunina. Hins vegar verður þjónustan að tengjast verkefni. Liður kröfur um þjónustu pantanir eru unnin í gegnum verkefni. 

### <a name="example"></a>Dæmi

Þjónustupantanir sem eru stofnaðar af þjónustusamningi eru unnar af sendanda. Fyrir fyrstu þjónustupöntunina áttar sendandinn sig á því að þjónustutæknimaðurinn þarfnast mikilvægs varahlutar sem er ekki til á lager. Af þeim sökum stofnar sendandinn vöruþörf fyrir varahlutinn beint frá þjónustupöntuninni.

## <a name="move-and-post-lines"></a>Hreyfa og bóka línur

Þjónustutæknimaður kemur úr þjónustuheimsókn og breytir þá og uppfærir þjónustupöntunarlínur. Á meðan á þjónustuheimsókn stóð framkvæmdi þjónustutæknimaðurinn þjónustuverk sem var áætlað fyrir næstu þjónustuheimsókn. Þess vegna færir tæknimaðurinn línurnar frá næstu þjónustuheimsókn yfir á núverandi þjónustuheimsókn. Tæknimaðurinn bókar síðan þjónustupöntunina. Nánari upplýsingar er að finna í [Færa þjónustupöntunarlínur](move-service-order-lines.md).

## <a name="cancel-service-orders"></a>Afturkalla þjónustupantanir

Ein af hinum þjónustupöntununum sem voru búnar til fyrir janúarmánuð verður úrelt vegna þess að hætt er við verkið. Þess vegna hættir þjónustusendandi við þjónustupöntunina. Nánari upplýsingar er að finna í [Hætta við þjónustupantanir](cancel-service-orders.md).

## <a name="post-from-projects"></a>Bóka frá verkefnum

Í lok hverrar viku vill sendandinn bóka allar þjónustupantanir sem tengjast ákveðnu verkefni. Afgreiðslustjórinn finnur þess vegna viðeigandi verkefni á síðunni **Verkefni** og bókar þjónustupantanir sem er lokið. Nánari upplýsingar er að finna í [Bóka þjónustupantanir (klasaskjámynd)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Eyða þjónustupöntunum

Á seinni hluta ársins ákveður viðskiptavinurinn að þjónustuheimsóknirnar séu of fáar. Stofna þarf nýja og tíðari röð af þjónustuheimsóknum fyrir þann tíma sem eftir er í þjónustusamningnum. Þess vegna verður þú að eyða núverandi þjónustupöntunum og stofna nýjar í staðinn. Nánari upplýsingar er að finna í [Eyða þjónustupöntunum](delete-service-orders.md).

## <a name="see-also"></a>Sjá einnig

[Þjónustupantanir (skjámynd)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]