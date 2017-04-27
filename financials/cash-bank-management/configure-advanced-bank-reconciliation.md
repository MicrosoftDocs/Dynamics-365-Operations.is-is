---
title: "Yfirlit ítarlegrar bankaafstemmingar"
description: "Ítarleg afstemming aðgerð gerir það mögulegt að flytja inn rafræn bankayfirlit sem er hægt að stemma sjálfkrafa af úr bankafærslu í Microsoft Dynamics 365 for Operations.  Þessi grein verður útskýra skal setja upp ferli fyrir afstemmingu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Yfirlit ítarlegrar bankaafstemmingar

[!include[banner](../includes/banner.md)]


Ítarleg afstemming aðgerð gerir það mögulegt að flytja inn rafræn bankayfirlit sem er hægt að stemma sjálfkrafa af úr bankafærslu í Microsoft Dynamics 365 for Operations.  Þessi grein verður útskýra skal setja upp ferli fyrir afstemmingu.  

Fjöldi eintaka sem verður að setja upp áður en að nota ítarlega afstemmingu aðgerðir. Nánari upplýsingar um uppsetningu banki innflutning uppgjör í [Uppsetning banka innflutningsferlið uppgjör](set-up-advanced-bank-reconciliation-import-process.md).  Kröfur um uppsetningu á afstemmingu stendur nánar hér að neðan.

## <a name="transaction-codes"></a>Færslukóðar
Færslukóða má nota sem hluta af samsvörunarreglum bankaafstemmingar.  Færslukóði mun hjálpa við samsvörun á aðeins sömu gerð viðskipta á milli Dynamics 365 for Operations og bankayfirlits þíns.  Til Til að gera þessa gerð samsvörunar verður fyrst að skilgreina færslugerðir sem eru notaðar fyrir bankafærslur úr Dynamics 365 for Operations, síðan varpa þeim gerðum í kóða yfirlitsfærslna sem bankinn þinn notar.  Færslugerðir fyrir bankafærslur Dynamics 365 for Operations eru skilgreindar á síðunni **Færslugerð banka**.  Þetta er einnig þar sem skilgreina aðallykil til að nota fyrir bókanir færslugerð sem tengist. 

Þegar bankafærslukóðar Dynamics 365 for Operations hafa verið skilgreindir, varpa á færslukóða sem er notaður við rafræna bankayfirlit.  Þetta vörpunarferli er gert með síðunni **Vörðun færslukóða**.  Vörpun færslukóða er lokið aðskilið fyrir hvern bankareikning.

## <a name="matching-rules-and-matching-rule-sets"></a>Jöfnunarreglur og jöfnunarreglusett
Jöfnunarreglur gera kleift að skilgreina skilyrði fyrir sjálfvirka afstemmingu milli bankafærslur Dynamics 365 for Operations og bankafærslur uppgjör.  Uppsetning á jöfnunarreglum er gerð á síðunni **Jöfnunarreglur afstemmingar**.  Nánari upplýsingar um það eru í [Setja upp jöfnunarreglur bankaafstemmingar](set-up-bank-reconciliation-matching-rules.md). 

Jöfnunarreglusett eru notaðar til að skilgreina flokk jöfnunarreglur sem eru keyrðar í röð afstemmingarferlinu banka.  Jöfnunarreglusett eru skilgreind á síðunni **jöfnunarreglusett Afstemmingar**.

## <a name="cash-and-bank-management-parameters"></a>Færibreytur reiðufjár- og bankastjórnunar
Það er fjöldi færibreyta sem eru sértækar fyrir ítarlegt ferli bankaafstemmingar á síðunni **Færibreytur Færibreytur reiðufjár- og bankastjórnunar**.  **Sýna upphæð uppgjörslínu í debet/kredit** breytir yfirliti yfir upphæðir á síðunni **bankayfirlit**.  Ef þessi valkostur er valinn, verða færsluupphæðir bankayfirlits sýndar í aðskildum dálkum debets og kredits.  Ef þessi valkostur er ekki valinn, verða færsluupphæðir bankayfirlits sýndar í einum upphæðadálki með viðeigandi formerki. 

Stilltir staðfestingarkostirnir á færibreytusíðunni yfirskrifa valið sem er stillt í samsvörunarreglunum.  Til dæmis er ekki hægt að samsvara fylgiskjöl handvirkt eða sjálfvirkt umfram þann mismun dagsetninga sem er stilltur á færibreytusíðunni.  Einnig, ef að valkosturinn **Sannprófa vörpun færslugerða** er valinn verður að varpa færslugerðum milli Dynamics 365 for Operations bankafærsla og uppgjör bankafærslu til þess að vera handvirkt eða sjálfvirkt jafnað. 

Einnig þarf að skilgreina nauðsynlegar númeraraðir á **færibreytur reiðufé- og bankastjórnar** síðu.  Á **Númeraraðir** flipanum stilla kóða númeraraða fyrir Niðurhalið **Kenni Kenni Uppgjörs, Kenni Afstemming og Banka afstemmingu** tilvísanir.

## <a name="bank-account-reconciliation-options"></a>afstemmingu bankareiknings valkostur
Fyrst þarf að virkja Ítarlega afstemmingu bankareiknings.  Fjöldi eftirfarandi valkostir eru tiltækir á **bankareikning** síðuna þegar ítarlega afstemmingu aðgerðir eru virkar. 

**Nota bankayfirlit sem staðfestingu á rafrænu greiðsluna** virkni samþætta virkni afstemmingar banka og stöður rafrænar greiðslur.  Þegar þetta er virkt bankaskjali sjálfkrafa stofnuð fyrir rafræna greiðslu staða er stillt á **Sent**.  Þar að auki stöðu rafræna greiðslu er uppfærður úr **Sent** til **Móttekið** eftir greiðslu er jafnað afstemmd og bókaðar. 

Á **nafn bankareikning í yfirlitum** er heitið sem notað er fyrir bankareikninginn sem á við rafræna bankayfirlit.  Þetta nafn er notað þegar hvaða færslur á að flytja inn bankareikningur uppgjör sem innihalda upplýsingar fyrir marga bankareikninga. 

Valkostinn að **Afstemming eftir innflutning** verður sjálfkrafa villuleita bankayfirlit, stofna nýja afstemmingar banka og vinnublaðinu og keyra samsvörunarreglusett Sjálfgefið.  Þessi aðgerð gerir ferliið sjálfvirkt upp að þeim punkti þar sem færslur þarft að jafna handvirkt.  Stilling bankareiknings fer í vanskil við innflutningur.




