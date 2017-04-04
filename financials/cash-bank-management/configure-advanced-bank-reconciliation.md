---
title: "Yfirlit ítarlegrar bankaafstemmingar"
description: "Ítarlegri bankaafstemmingu er hægt að flytja inn rafræn bankayfirlit og afstemma sjálfkrafa með bankafærslum í Microsoft Dynamics 365 aðgerða.  Þessi grein verður útskýra skal setja upp ferli fyrir afstemmingu."
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

Ítarlegri bankaafstemmingu er hægt að flytja inn rafræn bankayfirlit og afstemma sjálfkrafa með bankafærslum í Microsoft Dynamics 365 aðgerða.  Þessi grein verður útskýra skal setja upp ferli fyrir afstemmingu.  

Fjöldi eintaka sem verður að setja upp áður en aðgerðin ítarlega afstemmingu eru til staðar. Nánari upplýsingar um uppsetningu banka uppgjör innflutning í [Uppsetning banka innflutningsferlið uppgjör](set-up-advanced-bank-reconciliation-import-process.md).  Kröfur um að setja upp ferli afstemmingar er nánar hér að neðan.

## <a name="transaction-codes"></a>Færslukóðar
Hægt er að nota kóða sem hluti af reglum fyrir samsvörunarreglu afstemmingar banka.  Færslukóðar hjálpar til við að stemma aðeins sama gerðir af færslum á bankayfirliti og Dynamics 365 fyrir Aðgerðir.  Til að gera þessa gerð jöfnun, sem verður fyrst skilgreina færslugerðir sem eru notaðir fyrir færslur úr Dynamics 365 fyrir Aðgerðir, þá varpa þær gerðir færslukóða bankayfirlits notað af bankanum.  Færslugerðir fyrir Dynamics 365 fyrir bankafærslur Aðgerðir eru skilgreindar í í **Bankafærslutegund** síðu.  Þetta er einnig þar sem skilgreina aðallykil til að nota fyrir bókanir færslugerð sem tengist. 

Þegar notanda Dynamics 365 fyrir færslukóða banka Aðgerða eru skilgreind er svo að varpa á færslukóða sem er notaður við rafræna bankayfirlitum í.  Þetta ferli vörpun er gert með því að nota í **færslukóðavörpun** síðu.  Færslukóðavörpun er fyllt út sérstaklega fyrir hvern bankareikning.

## <a name="matching-rules-and-matching-rule-sets"></a>Jöfnunarreglur og jöfnunarreglusett
Jöfnunarreglur notandanum kleift að skilgreina skilyrði fyrir sjálfvirka afstemmingu milli 365 Dynamics fyrir bankafærslur Aðgerðir og bankafærslur uppgjörs.  Setja upp jöfnunarreglur eru gerðar á **jöfnunarreglur Afstemmingar** síðu.  Nánari upplýsingar, sjá [Setja upp reglur fyrir samsvörunarreglu afstemmingar banka](set-up-bank-reconciliation-matching-rules.md). 

Jöfnunarreglusett eru notaðar til að skilgreina flokk jöfnunarreglur sem eru keyrðar í röð afstemmingarferlinu banka.  Jöfnunarreglusett eru skilgreind í á **jöfnunarreglusett Afstemmingar** síðu.

## <a name="cash-and-bank-management-parameters"></a>Færibreytur reiðufjár- og bankastjórnunar
Fjöldi færibreyta eru við ítarlega afstemmingu ferli á við **færibreytur Sjóða- og** síðu.  Í **upphæð uppgjörslínunum Sýna debet/kredit** breytist yfirlit yfir upphæðir á í **Bankayfirlit** síðu.  Ef þessi valkostur er valinn banka færsluupphæðum bankayfirlits sýnd í aðskildum debet og kredit-dálkunum.  Ef þetta er ekki valið banka færsluupphæðum bankayfirlits sýnd í einni upphæð dálk með viðeigandi formerki. 

Villuleit valkostirnir stillt á síðu færibreytur hnekkja sett á jöfnunarreglur vali.  Til dæmis er hægt handvirkt eða sjálfvirkt samsvara skjöl umfram dagsetningarmismunur sem setja á síðu færibreytur.  Einnig, ef að **Sannprófa vörpun færslugerða** er valinn, færslugerðir þarf að varpa milli Dynamics 365 bankafærslunnar Aðgerðir og bankafærslu uppgjör í röð fyrir færslur að vera handvirkt eða sjálfvirkt jafnað. 

Einnig þarf að skilgreina nauðsynlegar númeraraðir á í **færibreytur Sjóða- og** síðu.  Á við **Númeraraðir** flipanum stilla kóða númeraraða fyrir Niðurhalið **Kenni Kenni Uppgjörs, Kenni Afstemming og Banka afstemmingu** tilvísanir.

## <a name="bank-account-reconciliation-options"></a>afstemmingu bankareiknings valkostur
Fyrst þarf að virkja Ítarlega afstemmingu bankareiknings.  Fjöldi eftirfarandi valkostir eru tiltækir á í **bankareikning** síðuna þegar ítarlega afstemmingu aðgerðir eru virkar. 

**Nota bankayfirlit sem staðfestingu á rafrænu greiðsluna** virkni samþætt virkni afstemmingar banka stöður rafrænar greiðslur.  Þegar þetta er virkt bankaskjali sjálfkrafa stofnuð fyrir rafræna greiðslu staða er stillt á **Sent**.  Þar að auki stöðu rafræna greiðslu er uppfærður úr **Sent** til **Móttekið** eftir greiðslu er jafnað afstemmd og bókaðar. 

Í **nafn bankareikning í yfirlitum** er heitið sem notað er fyrir bankareikninginn á bankayfirlitum við rafræna.  Þetta nafn er notað þegar hvaða færslur á að flytja inn bankareikningur uppgjör sem innihalda upplýsingar fyrir mörgum bankareikningum. 

Valkostinn að **Afstemming eftir innflutning** verður sjálfkrafa villuleita bankayfirlit, stofna nýja bankaafstemmingu og vinnublað og keyra Sjálfgefna samsvörunarreglusett.  Þessi aðgerð gerir ferlið fram á fyrir færslur sem þarf að jafna þær handvirkt.  Stilling á bankareikning sjálfgefnar við innflutning.


