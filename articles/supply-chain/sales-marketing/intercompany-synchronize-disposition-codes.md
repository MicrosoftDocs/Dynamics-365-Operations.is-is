---
title: Samstilla ráðstöfunarkóða
description: Þessi grein útskýrir samstillingu ráðstöfunarkóða fyrir viðskipti milli fyrirtækja
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: d347181dd6ba12de0e114d74d43cd46230ba4fb7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905661"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Samstilla ráðstöfunarkóða innan samstæðu

[!include [banner](../../includes/banner.md)]

Til að styðja skil innan samstæðu gerir Microsoft Dynamics 365 Supply Chain Management þér kleift að varpa ytra skilgreindum ráðstöfunarkóðum í samsvarandi innri ráðstöfunarkóða. Þegar verið er að setja upp samstæðukeðju verða aðgerðir ráðstöfunar í báðum fyrirtækjunum sem varpað er hvort í annað að vera þær sömu. Ef þær eru ekki þær sömu mun samstillingarferlið ekki takast.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Um ráðstöfunarkóða fyrir þrískipt bein skil

Ráðstöfunarkóðar eru samstilltir úr sölupöntunarlínunni innan samstæðunnar við upprunalegu sölupöntunarlínuna. Samstilling hefur þó aðeins ein tafarlaus áhrif á upphaflegu sölupöntunarlínuna. Áhrifin eru að ýmsum línugjöldum er eytt út frá ráðstöfunarkóðanum og gjöldum sem eru sett upp í fyrirtæki A. Fyrirtæki A er fyrirtækið sem stofnar skilapöntunina.

Í þrískiptri keðju beinnar afhendingar eru allir ráðstöfunaraðgerðir studdar í samstæðusölupöntunarlínunni. Ef afurð er hinsvegar skilað til viðskiptavinarins ætti að staðfesta að afhendingaraðsetrið í skilapöntuninni passi við afhendingaraðsetur viðskiptavinarins sem er tilgreint á upprunalegu pöntuninni.

> [!NOTE]
> Ráðstöfunarkóðar fyrir innkaupapantanir eru ekki til. Þess vegna þarf að framkvæma samstillingu á ráðstöfunarkóðum úr samstæðusölupöntuninni við upprunalegu skilapöntunina frá sölupöntun til sölupöntunar.

## <a name="replacing-returned-items"></a>Skipt á skilavörum

Ef verið er að skipta skilavöru út og þegar er búið að stofna skiptipöntun í fyrirtæki B er ekki hægt að velja ráðstöfunarkóða og enginn ráðstöfunarkóði er stofnaður í fyrirtæki A.

## <a name="rules-for-intercompany-direct-deliveries"></a>Reglur fyrir beinar afhendingar innan samstæðu

Eftirfarandi almennar reglur eiga við um upprunalegar skilapantanir í aðstæðum sem hafa með beinar afhendingar innan samstæðu að gera:

- Ef undirliggjandi ráðstöfunaraðgerð í upprunalegu sölupöntunarlínunni er kreditfærsla og rýrnun, kreditfærsla eða skil til viðskiptavinar er ráðstöfunaraðgerð kreditfærslu notuð. Hins vegar mun aðgerðakóðinn Skil til viðskiptavinar stilla nettóupphæðina á 0 (núll) á línunni sem til er og á nýlega samstilltu línunni úr sölupöntuninni innan samstæðunnar. Þar að auki eru rýrnunarlínur aldrei samstilltar. Þegar línu er bætt við sölupöntun innan samstæðu er hún aldrei samstillt fyrir sölupöntun með jákvæðu magni og ráðstöfunaraðgerðina rýrnun (til dæmis Kredit og Rýrnun eða Skipti og Rýrnun).
- Undirliggjandi ráðstöfunaraðgerð kreditfærslu og útskiptingu eða rýrnun og útskiptingu er ekki hnekkt. Hún er meðhöndluð sem ráðstöfunaraðgerð kreditfærslu og útskiptingar eða rýrnunar og útskiptingar. Þessi regla á við þótt engin rýrnunarlína er stofnuð í fyrirtæki A og engin skiptipöntun er stofnuð í fyrirtæki B (fyrirtækið sem tók á móti skilavörunni). Skiptipöntun er einungis stofnuð í fyrirtæki A þegar uppfærsla á fylgiseðli er framkvæmd.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
