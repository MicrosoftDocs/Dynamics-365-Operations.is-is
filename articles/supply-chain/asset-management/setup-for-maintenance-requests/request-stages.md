---
title: Líftímastöður viðhaldsbeiðni
description: Þessi grein lýsir því hvernig á að setja upp líftímastöðu viðhaldsbeiðna í eignastýringu.
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81b30820adf11f0239ea8ff9d1886b5738e38162
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862715"
---
# <a name="maintenance-request-lifecycle-states"></a>Lífsferilsstöður viðhaldsbeiðni

[!include [banner](../../includes/banner.md)]

 


Líftímastöður viðhaldsbeiðna skilgreinir stigin sem beiðni getur farið í gegnum. Sem dæmi má nefna **Stofnað**, **Virkur**, og **Kláraði**. Þegar viðhaldsbeiðni er breytt í verkbeiðni skal uppfæra ástand líftíma viðhaldsbeiðninnar til **Kláraði** eða **Lokað** til að gefa til kynna að viðhaldsbeiðnin sé ekki lengur virk. Á listasíðunni **Allar viðhaldsbeiðnir** er hægt að skoða allar viðhaldsbeiðnir, óháð líftímastöðu þeirra.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Setja upp líftímastöður viðhaldsbeiðni

1. Veldu **Eignastýring** \> **Uppsetning** \> **Viðhaldsbeiðnir** \> **Líftímastöður**.
2. Veldu **Nýr** til að stofna líftímastöðu viðhaldsbeiðni.
3. Í reitinn **Líftímastöðu** slærðu inn kenni líftímastöðunnar.
4. Færið inn lýsandi nafn í reitinn **Heiti**.

    Á flýtiflipanum **Upplýsingar** sýnir reiturinn **Líftímalíkön** fjölda líftímalíkana viðhaldsbeiðna sem nota þessa líftímastöðu.

5. Á flýtiflipanum **Almennt**, stilltu **Virkur** kostur á **Já** ef viðhaldsbeiðni ætti að vera virk meðan hún er í þessari líftímastöðu.
6. Stilltu valkostinn **Stilla raunveruleg lok** á **Já** ef sjálfkrafa ætti að slá inn raunverulegan lokadag og tíma í viðhaldsbeiðni í þessari líftímastöðu.
7. Stilltu valkostinn **Stofna verkbeiðni** á **Já** ef hægt er að búa til verkbeiðni út frá viðhaldsbeiðni sem er í þessu líftíma ástand.
8. Stilltu **Eyða** kostur á **Já** ef hægt er að eyða viðhaldsbeiðni meðan hún er í þessu líftíma ástand.
9. Á flýtiflipanum **Uppfærsla** eiga valkostirnir **Á innleið** og **Á útleið** í hlutanum **Eign** við ef þú notar viðgerð á útibúi. Stilltu viðeigandi valmöguleika á **Já** ef líftímastaða eigna sem eru valdar í viðhaldsbeiðni ætti sjálfkrafa að vera uppfærður í **Á innleið** eða **Á útleið** þegar líftímastaða viðhaldsbeiðninnar er stillt á **Á innleið** eða **Á útleið**.

Eftirfarandi mynd sýnir dæmi um síðuna **Líftímastöður viðhaldsbeiðna**.

![Síða fyrir líftímastöður viðhaldsbeiðni.](media/02-setup-for-requests.png)

> [!NOTE]
> Líftímastöður viðhaldsbeiðna, líftímastöðuhópar og tegundir eru tengdar og notaðar á sama hátt og líftímastöður verkbeiðni, líftímastöðuhópar og tegundir. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Setja upp líftímalíkön viðhaldsbeiðni

Eftir að þú ert búinn að búa til lífsferilstig sem nauðsynleg eru fyrir viðhaldsbeiðnir þínar er hægt að skipta þeim í líftíma hópa eða líftíma líkana. Lífsferilslíkön viðhaldsbeiðna eru notuð til að búa til flæði sem hægt er að nota fyrir mismunandi gerðir af viðhaldsbeiðnum. Að lágmarki ætti að búa til eitt staðlað líftímalíkan viðhaldsbeiðni.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Viðhaldsbeiðnir** \> **Líftímalíkön**.
2. Veldu **Nýr** til að stofna líftímalíkan viðhaldsbeiðni.
3. Í **Líftímalíkan** reitinn, sláðu inn kenni líftímalíkansins.
4. Færið inn lýsandi nafn í reitinn **Heiti**.

    Á flýtiflipanum **Upplýsingar** sýnir **Líftímastöður** fjölda líftímastaða eigna sem eru valin í þessu líftímalíkani eigna. Reiturinn **Gerðir viðhaldsbeiðna** sýnir fjölda gerða viðhaldsbeiðna sem nota líftímalíkanið.

5. Á flýtiflipanum **Líftímastöður** velurðu þær líftímastöður sem ætti að vera með í líftímalíkani:

    - Til að hafa með líftímastöðu í líkani líftímastöðu skal velja það í hlutanum **Eftirstöðvar líftímastaða** og síðan velja hægri örvarhnappinn ![Hægri ör.](media/03-setup-for-requests.png) til að færa það í hlutann **Valdar líftímastöður**.
    - Til að taka með allar tiltækar líftímastöður í líkani líftímastöðu skal velja hnappinn **Velja allar tiltækar stöður** ![Velja allar tiltækar stöður.](media/04-setup-for-requests.png). Allar líftímastöður eru fluttar í hlutann **Valdar líftímastöður**.
    - Til að fjarlægja líftímastöðu úr líkani líftímastöðu skal velja hana í hlutanum **Líftímastöður valdar** og síðan velja vinstri örvarhnappinn ![Vinstri ör.](media/05-setup-for-requests.png) til að færa það í hlutann **Eftirstandandi líftímastöður**.

6. Á flýtiflipanum **Almennt**, reitirnir í **Uppfærslur** kaflinn skiptir máli ef þú notar viðgerð á geymslu.

    - Í reitnum **Líftímastaða fyrir móttekna eign** skaltu velja ástand líftíma eigna að eignir sem eru valdar í viðhaldsbeiðni ættu sjálfkrafa að vera uppfærðar til þegar þær eru mótteknar til lagfæringar á geymslu.
    - Í reitnum **Líftímastaða fyrir afhenta eign** skaltu velja ástand líftíma eigna að eignir sem eru valdar í viðhaldsbeiðni ættu sjálfkrafa að vera uppfærðar til þegar þeim er skilað eftir lagfæringu.

Eftirfarandi mynd sýnir dæmi um síðuna **Líftímalíkön viðhaldsbeiðna**.

![Síðan fyrir líftímalíkön viðhaldsbeiðni.](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]