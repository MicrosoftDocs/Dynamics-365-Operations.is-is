---
title: Líftímastöður eigna
description: Þessi grein útskýrir líftímastöðu eigna og líftímalíkönum í Eignastýringu.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43b1ff9438437e6c1ff33bab9a7ba0361029cb6d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901061"
---
# <a name="asset-lifecycle-states"></a>Líftímastöður eigna

[!include [banner](../../includes/banner.md)]

 

Þessi grein útskýrir líftímastöðu eigna og líftímalíkönum í Eignastýringu. Líftímastöður eigna eru notaðar til að skilgreina hvort eignin sé virk eða óvirk. Þú getur til dæmis sett upp eignalífsferilstig eins og **Stofnað**, **Virkur**, og **Hætt**.

> [!NOTE]
> - Beiðni um líftímastöður er tengd við líftímastöður eigna. Þess vegna, þegar beiðni er breytt í nýja líftímastöðu beiðni þá er eigninni sem fylgir beiðninni breytt í nýja líftímastöðu eignar. Til dæmis, ef líftíma beiðni er breytt í **Á heimleið**, er líftímastöðu meðfylgjandi eignar breytt í líftímastöðuna sem var valin í reitnum **Líftímastaða á innleið** á flýtiflipanum **Líftímastaða eigna** á síðunni **Líkön líftímastöðu eigna**. 


Hægt er að setja upp eignalíftímatöðu í líftímalíkönum eigna, þar sem þú getur skilgreint nauðsynleg líftímastöður fyrir mismunandi tegundir eigna. Fyrst seturðu upp líftímastöður. Síðan stofnaður líftímalíkan og velur líftímastöðu fyrir það.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Líftímastöður**.
2. Veldu **Nýr** til að stofna nýja líftímastöðu eignar.
3. Í **Líftímastöðu** reitinn, sláðu inn auðkenni líftímastöðunnar.
4. Færið inn lýsandi nafn í reitinn **Heiti**.

    Reiturinn **Líftímalíkön** sýnir fjölda líftímalíkana eigna sem nota líftímastöðu eigna.

5. Stilltu valkostinn **Virkt** á **Já** ef þessi líftímastaða á að vera virk líftímastaða (með öðrum orðum, ef hægt er að stofna verkbeiðnir fyrir eignir sem eru í þessari líftímastöðu).
6. Stilltu **Eyða opnum dagatalalínum** kostur á **Já** ef opnar eignadagatalalínur sem hafa eigið líftímastöðu eigna **Stofna** á að vera eytt þegar þær eru í þessari líftímastöðu. Þessi stilling er gagnleg ef þú vilt hreinsa upp opnar viðhaldsáætlanir sem eru ekki lengur viðeigandi fyrir eignina (til dæmis ef eignin er ekki lengur virk).

> [!NOTE]
> Líftímastöður eigna, líftímalíkön eigna og tegundir eigna tengjast. Þau eru notuð á sama hátt og líftímastöður verkbeiðni, líftímalíkön verkbeiðni og tegundir verkbeiðni. 


Eftir að þú hefur búið til tilskildar líftímastöður eigna geturðu sett upp líftímastöður í líftímalíkönum eigna.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Líftímalíkön**.
2. Veldu **Nýr** til að stofna nýja líftímalíkani eignar.
3. Í **Líftímalíkan** reitinn, sláðu inn auðkenni líftímalíkansins.
4. Færið inn lýsandi nafn í reitinn **Heiti**.

    Reiturinn **Líftímastöður** sýnir fjölda líftímastaða eigna sem eru valin í líftímalíkani eigna. Reiturinn **Gerðir eigna** sýnir fjölda eignagerða sem nota líftímalíkanið.

5. Á flýtiflipanum **Líftímastöður** velurðu þær líftímastöður eigna sem ætti að vera með í líftímalíkani eigna:

    - Til að nota líftímastöðu fyrir líkanið skal velja það í hlutanum **Eftirstöðvar líftímastaða** og síðan velja hægri örvarhnappinn ![Hægri ör.](media/15-setup-for-objects.png) til að færa það í hlutann **Valdar líftímastöður**.
    - Til að nota allar tiltækar líftímastöður fyrir líkanið skal velja hnappinn **Allar tiltækar líftímastöður** ![Allar tiltækar líftímastöður](media/20-setup-for-objects.png). Allar líftímastöður eru fluttar í hlutann **Valdar líftímastöður**.
    - Til að fjarlægja líftímastöðu úr líkaninu skal velja hana í hlutanum **Líftímastöður valdar** og síðan velja vinstri örvarhnappinn ![Vinstri ör.](media/16-setup-for-objects.png) til að færa það í hlutann **Eftirstandandi líftímastöður**.

6. Veldu **Uppfærslur á líftímastöðu** til að skilgreina líftímastöður eignar sem geta fylgt valinni líftímastöðu.
7. Þú notar flýtiflipann **Eignarstaða** ef þú annast eignir sem þú færð til viðgerðar. Í hlutanum **Innleið/útleið**, getur þú valið líftímastöður eigna til að gefa til kynna verkflæði eignar sem þú færð til viðgerðar. Ef þú býður upp á eignir til viðskiptavina eða deilda, í **Lán** kafla, getur þú valið líftímastöðu fyrir lánaeignir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]