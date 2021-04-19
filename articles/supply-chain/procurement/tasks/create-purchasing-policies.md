---
title: Stofna innkaupastefnu
description: Þetta efni sýnir hvernig á að stofna innkaupareglur til samræmis við viðskiptaferli þín fyrir innkaup.
author: kamaybac
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2cc64d0b9492a7bfcf0076ea74ca36a9a26ee6c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812207"
---
# <a name="create-purchasing-policies"></a>Stofna innkaupastefnu

[!include [banner](../../includes/banner.md)]

Þetta efni sýnir hvernig á að stofna innkaupareglur til samræmis við viðskiptaferli þín fyrir innkaup. Áður en hægt er að stofna innkaupastefnur þarf að setja upp færibreytur fyrir innkaupastefnu. Hægt er að stofna, breyta og hætta við innkaupastefnu en ekki er hægt að eyða innkaupastefnu. Þetta verk myndi venjulega vera framkvæmt af innkaupaaðila. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.


## <a name="set-up-policy-parameters"></a>Setja upp færibreytur reglna
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Uppsetning > Reglur > Innkaupareglur**.
2. Á aðgerðasvæðinu skal velja **Færibreytur**.
- Reglugerðir um forgang eiga við um mismunandi stig innan fyrirtækisins. Skipulagseiningar sem eru sýndar fara eftir því stigveldi fyrirtækis og á hvaða stigi í stigveldi er búið að úthluta tilgangi fyrir innra eftirlit innkaupa. Til dæmis, gæti fyrirtækið verið með lögaðila, kostnaðarstaði, svæði og deildir, en hugsanlega er aðeins sumar þessara eininga með tilgang stigveldis fyrir innra eftirlit innkaupa. Sjálfgefið er að fyrirtækisins af gerðinni Fyrirtæki tiltæk.  
3. Veldu flipann **Færibreytur stefnureglugerðar**.
4. Í trénu ferðu í **Innkaupastefna > Stjórnunarregla innkaupastefnu**.
- Er forgangsröð er skilgreind fyrir lausn reglu á reglustigi. Hins vegar er hægt að hnekkja forgangsröð einstaka stefnureglugerða fyrir sumar gerðir reglna. Til dæmis mætti skilgreina forgangsröð fyrir innkaupastefnur í þessari röð: kostnaðarstaður, deild, fyrirtæki. Fyrir stefnureglu vörulista viltu kannski hafa forgangsröð: deild, kostnaðarstaður, fyrirtæki. Forgangsröð má breyta fyrir stefnureglu vörulista. Þegar starfsmaður stofnar beiðni, er vörulistinn sem birtist ákvarðaður af reglunum sem tengjast deild starfsmannsins, síðan kostnaðarstað hans og svo fyrirtæki hans.  
- Ef meira en eitt stjórnunarstig er skráð er hægt að nota örvarnar Upp/Niður til að stilla forgangsröð fyrir reglu innkaupapantanastýringar.  
5. Lokið síðunni.

## <a name="create-a-new-policy"></a>Stofna nýja reglu
1. Veljið **Nýtt**.
2. Í reitinn **Heiti** skal slá inn gildi.
3. Í reitinn **Lýsing** skal slá inn gildi.
- Stök innkaupastefna geta átt aðeins við um eitt stigveldi fyrirtækis. Til dæmis gæti eitt stigveldi kallast "landsvæði" og annað kallast "deild" og hvort þeirra haft með mismunandi innkaupastefna.  
- Veljið fyrirtæki sem stefnan á við.  
4. Veldu örina til að bæta við völdu fyrirtæki.
- Hægt er að endurtaka þetta ferli til að bæta við fleiri fyrirtækjum.  

## <a name="add-a-policy-rule"></a>Bæta við stefnureglu
1. Á listanum **Stefnureglugerð**, velurðu **Málefnisregla beiðni**.
- Þú stofnar reglu sem stillir sjálfgefinn tilgang beiðni á gerðina Notkun en heimilar að velja í staðinn áfyllingargerð.  
2. Veldu **stefnureglu**.
3. Velja skal **Já** í reitnum **Leyfa handvirka hnekkingu**.
4. Veljið **Loka**.
- Núna er hægt að setja upp aðrar stefnureglur fyrir innkaupastefnu. Athugið að stefnureglugerð getur ekki haft reglur um skörun sem eru virkar á sama tíma innan einnar innkaupastefnu.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]