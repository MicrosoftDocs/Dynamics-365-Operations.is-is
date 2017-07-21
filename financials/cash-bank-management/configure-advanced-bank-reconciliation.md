---
title: "Yfirlit ítarlegrar bankaafstemmingar"
description: "Ítarleg bankaafstemming gerir það mögulegt að flytja inn rafræn bankayfirlit og stemma sjálfkrafa við bankafærslur í Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu.  Þessi grein verður útskýra skal setja upp ferli fyrir afstemmingu."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 89f895a9de9fa9863459ae6261b8c429d559d482
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="advanced-bank-reconciliation-overview"></a>Yfirlit ítarlegrar bankaafstemmingar

[!include[banner](../includes/banner.md)]


Ítarleg bankaafstemming gerir það mögulegt að flytja inn rafræn bankayfirlit og stemma sjálfkrafa við bankafærslur í Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu.  Þessi grein verður útskýra skal setja upp ferli fyrir afstemmingu.  

Fjöldi eintaka sem verður að setja upp áður en að nota ítarlega afstemmingu aðgerðir. Nánari upplýsingar um uppsetningu banki innflutning uppgjör í [Uppsetning banka innflutningsferlið uppgjör](set-up-advanced-bank-reconciliation-import-process.md).  Kröfur um uppsetningu á afstemmingu stendur nánar hér að neðan.

## <a name="transaction-codes"></a>Færslukóðar
Færslukóða má nota sem hluta af samsvörunarreglum bankaafstemmingar.  Færslukóðar hjálpa til við að varpa sams konar færslum í Finance and Operations og bankafærslum þínum.  Til að framkvæma þessa tengingu verður fyrst að skilgreina þær færslugerðir sem notaðar eru fyrir bankafærslur úr Finance and Operations og síðan varpa þessum gerðum á færslukóða á yfirlitum sem notaðir eru af þínum banka.  Færslugerðir fyrir bankafærslur Finance and Operations eru skilgreindar á síðunni **Færslugerð banka**.  Þetta er einnig þar sem skilgreina aðallykil til að nota fyrir bókanir færslugerð sem tengist. 

Þegar bankafærslukóðar Finance and Operations hafa verið skilgreindir, varpar þú þeim á færslukóða sem notaðir eru á rafrænum bankayfirlitum þínum.  Þetta vörpunarferli er gert með síðunni **Vörðun færslukóða**.  Vörpun færslukóða er lokið aðskilið fyrir hvern bankareikning.

## <a name="matching-rules-and-matching-rule-sets"></a>Jöfnunarreglur og jöfnunarreglusett
Jöfnunarreglur gera kleift að skilgreina skilyrði fyrir sjálfvirka afstemmingu milli bankafærslna Finance and Operations og bankayfirlitsfærslna.  Uppsetning á jöfnunarreglum er gerð á síðunni **Jöfnunarreglur afstemmingar**.  Nánari upplýsingar um það eru í [Setja upp jöfnunarreglur bankaafstemmingar](set-up-bank-reconciliation-matching-rules.md). 

Jöfnunarreglusett eru notaðar til að skilgreina flokk jöfnunarreglur sem eru keyrðar í röð afstemmingarferlinu banka.  Jöfnunarreglusett eru skilgreind á síðunni **jöfnunarreglusett Afstemmingar**.

## <a name="cash-and-bank-management-parameters"></a>Færibreytur reiðufjár- og bankastjórnunar
Það er fjöldi færibreyta sem eru sértækar fyrir ítarlegt ferli bankaafstemmingar á síðunni **Færibreytur Færibreytur reiðufjár- og bankastjórnunar**.  **Sýna upphæð uppgjörslínu í debet/kredit** breytir yfirliti yfir upphæðir á síðunni **bankayfirlit**.  Ef þessi valkostur er valinn, verða færsluupphæðir bankayfirlits sýndar í aðskildum dálkum debets og kredits.  Ef þessi valkostur er ekki valinn, verða færsluupphæðir bankayfirlits sýndar í einum upphæðadálki með viðeigandi formerki. 

Stilltir staðfestingarkostirnir á færibreytusíðunni yfirskrifa valið sem er stillt í samsvörunarreglunum.  Til dæmis er ekki hægt að samsvara fylgiskjöl handvirkt eða sjálfvirkt umfram þann mismun dagsetninga sem er stilltur á færibreytusíðunni.  Ef valkosturinn **Sannprófa vörpun færslugerða** er valinn verður einnig að varpa færslugerðum milli bankafærslna í Finance and Operations og bankayfirlitsfærslna svo hægt sé að tengja færslurnar handvirkt eða sjálfvirkt. 

Einnig þarf að skilgreina nauðsynlegar númeraraðir á **færibreytur reiðufé- og bankastjórnar** síðu.  Á **Númeraraðir** flipanum stilla kóða númeraraða fyrir Niðurhalið **Kenni Kenni Uppgjörs, Kenni Afstemming og Banka afstemmingu** tilvísanir.

## <a name="bank-account-reconciliation-options"></a>afstemmingu bankareiknings valkostur
Fyrst þarf að virkja Ítarlega afstemmingu bankareiknings.  Fjöldi eftirfarandi valkostir eru tiltækir á **bankareikning** síðuna þegar ítarlega afstemmingu aðgerðir eru virkar. 

**Nota bankayfirlit sem staðfestingu á rafrænu greiðsluna** virkni samþætta virkni afstemmingar banka og stöður rafrænar greiðslur.  Þegar þetta er virkt bankaskjali sjálfkrafa stofnuð fyrir rafræna greiðslu staða er stillt á **Sent**.  Þar að auki stöðu rafræna greiðslu er uppfærður úr **Sent** til **Móttekið** eftir greiðslu er jafnað afstemmd og bókaðar. 

Á **nafn bankareikning í yfirlitum** er heitið sem notað er fyrir bankareikninginn sem á við rafræna bankayfirlit.  Þetta nafn er notað þegar hvaða færslur á að flytja inn bankareikningur uppgjör sem innihalda upplýsingar fyrir marga bankareikninga. 

Valkostinn að **Afstemming eftir innflutning** verður sjálfkrafa villuleita bankayfirlit, stofna nýja afstemmingar banka og vinnublaðinu og keyra samsvörunarreglusett Sjálfgefið.  Þessi aðgerð gerir ferliið sjálfvirkt upp að þeim punkti þar sem færslur þarft að jafna handvirkt.  Stilling bankareiknings fer í vanskil við innflutningur.




