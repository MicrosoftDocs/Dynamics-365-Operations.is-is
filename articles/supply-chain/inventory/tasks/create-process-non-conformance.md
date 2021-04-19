---
title: Stofna og vinna úr samræmi
description: Þetta efni útskýrir hvernig eigi að framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun.
author: perlynne
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4f7e61adf37e74bdb082270b689cf0375ccc7f7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833954"
---
# <a name="create-and-process-a-conformance"></a>Stofna og vinna úr samræmi

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig eigi að framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun. Hægt er að keyra þessa skráningu í sýnifyrirtækinu USMF og nota ráðlögð gildi. Þetta ferli er yfirleitt framkvæmt af starfsmanni á sviði gæða.  Sem frumskilyrði skaltu ljúka leiðbeiningunum í [Kanna vörugæði](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md). Til að keyra samþykki á ósamkvæmi verður notandi sem keyrir verkskráninguna að hafa „Heiti“ úthlutað á síðunni Notendur. Til að nota athugasemdir skjals verður notandinn einnig að hafa skjalaafgreiðslu virkjaða í valkostum notanda.


## <a name="select-a-quality-order"></a>Velja gæðapöntun.
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastjórnun > Reglubundin verkefni > Gæðastjórnun > Gæðapantanir**.
2. Í listaum velurðu gæðapöntunina sem var stofnuð í [Kanna vörugæði](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).  

## <a name="create-a-nonconformance"></a>Stofna ósamkvæmistilvik
1. Á aðgerðasvæðinu skal velja **Fyrirspurnir**.
2. Veldu **Ósamkvæmnitilvik**.
3. Veljið **Nýtt**.
4. Í fellivalmyndinni **Gerð vandamáls** velurðu vandamálið sem fannst við skoðunarferlið.  
5. Veljið **Í lagi**.

## <a name="approvereject-a-nonconformance"></a>Samþykkja/hafna ósamkvæmistilviki
1. Veljið **Aðgerðir**.
2. Veldu **Samþykkja ósamkvæmni**. Í þessu dæmi samþykkirðu ósamkvæmina. Hægt er að tengja samþykkta ósamkvæmi tengdri virkni til að skrá vinnu sem er lokið sem hluti af afgreiðslu ósamkvæmi og, eins og í þessu efni, vinnslu á afgreiðslu leiðréttinga.  
3. Velja skal **Já**.

## <a name="create-a-correction-action"></a>Stofna leiðréttingaraðgerð
1. Veldu **Leiðréttingar**.
2. Veljið **Nýtt**.
3. Í reitnum **Númer starfsmanns** í nýju línunni velurðu skrána sem óskað er eftir af fellivalmyndinni.
4. Smellið á **Velja**.
5. Veldu **Hengja við**. Stofna athugasemd um leiðréttinguna. Fyrir þetta dæmi er aðgerð að hafa samband við lánardrottininn til að ræða ósamkvæmitilvikið.  
6. Veljið **Nýtt**.
7. Veljið **Athugasemd**. Eftir því hvernig uppsetning skýrslunnar er, hægt er að prenta mismunandi skjalategundir á skýrslum sem eru tengdar stjórnun á ósamkvæmi.  
8. Í reitinn **Lýsing** skal slá inn gildi.
9. Lokið síðunni.

## <a name="maintain-a-correction"></a>Viðhalda leiðréttingu
1. Velja **Merka sem lokið**.
2. Veljið **Í lagi**.
3. Lokið síðunni.

## <a name="close-a-nonconformance"></a>Loka ósamkvæmistilviki
1. Veljið **Aðgerðir**.
2. Veldu **Loka ósamkvæmni**.
3. Velja skal **Já**.
4. Lokaðu síðunum.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]