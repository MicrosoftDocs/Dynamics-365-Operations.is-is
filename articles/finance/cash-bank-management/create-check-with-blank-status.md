---
title: Búa til auðar ávísanir
description: Þetta efnisatriði útskýrir hvernig á að búa til auðar ávísanir fyrir bankareikning á síðunni Ávísanir.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: aa1c4c33b977c0173da98aee409389b9242980fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976454"
---
# <a name="create-checks-that-have-blank-status"></a>Búa til auðar ávísanir

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að búa til auðar ávísanir. Til dæmis væri hægt að stofna auða ávísun til að skrá ávísun sem hefur skemmst og er ekki hægt að nota til greiðslu.

Á síðunni **Ávísanir** er hægt að framkvæma viðhaldsverk fyrir ávísanir. Til dæmis er hægt að búa til ný ávísunarnúmer og eyða ávísunum. Einnig er hægt að búa til ávísanir með stöðuna **Auð**. Eftir að auðar ávísanir eru stofnaðar er ekki hægt að eyða þeim eða endurnýta þær í kerfinu.

> [!NOTE]
> Þessi eiginleiki er aðeins í boði á síðunni **Ávísanir** og aðeins ef kveikt er á eiginleikanum **Búa til auðar ávísanir á ávísanasíðunni** á síðunni **Eiginleikastjórnun**. Ef ekki er kveikt er á eiginleikanum er einungis hægt að stofna **auðar** ávísanir í svarglugganum **Greiðsla með ávísun** meðan á greiðslumyndun stendur í viðskiptaskuldum.

Til að opna síðuna **Ávísanir** skal fara í **Reiðufjár-og bankastjórnun \> Bankareikningar \> Bankareikningar** og síðan, á aðgerðasvæðinu. í flipann **Stjórna greiðslum** í hópnum **Tengdar upplýsingar** og velja **Ávísanir**. Einnig er hægt að fara í **Reiðufjár- og bankastjórnun \> Fyrirspurnir og skýrslur \> Ávísanir**.

Síðan, til að búa til ávísanir með stöðuna **Auð** á aðgerðasvæðinu, skal velja **Stofna auðar ávísanir**. Þegar kerfið er að búa til auðar ávísanir er tengdur bankareikningur gerður óvirkur tímabundið. Þessi virkni dregur úr hættunni á því að greiðslur verði myndaðar á sama tíma og auðar ávísanir eru stofnaðar. Þegar vinnslunni er lokið er tengdur bankareikningur endurvirkjaður.
