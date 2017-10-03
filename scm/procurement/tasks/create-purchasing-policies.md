--- 
title: "Búa til innkaupastefnu"
description: "Þessi verklýsing sýnir hvernig á að stofna innkaupareglur til samræmis við viðskiptaferli þín fyrir innkaup."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 51486712d732bba064fd6c9b64dbccb730603877
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-purchasing-policies"></a>Búa til innkaupastefnu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna innkaupareglur til samræmis við viðskiptaferli þín fyrir innkaup. Áður en hægt er að stofna innkaupastefnur þarf að setja upp færibreytur fyrir innkaupastefnu. Hægt er að stofna, breyta og hætta við innkaupastefna en ekki er hægt að eyða innkaupastefna. Þetta verk myndi venjulega vera framkvæmt af innkaupaaðila. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.


## <a name="set-up-policy-parameters"></a>Setja upp færibreytur reglna
1. Fara í innkaupastefnur
2. Smellt er á Færibreytum.
    * Reglugerðir um forgang eiga við um mismunandi stig innan fyrirtækisins. Skipulagseiningar sem eru sýndar fara eftir því stigveldi fyrirtækis og á hvaða stigi í stigveldi er búið að úthluta tilgangi fyrir innra eftirlit innkaupa. Til dæmis, gæti fyrirtækið verið með lögaðila, kostnaðarstaði, svæði og deildir, en hugsanlega er aðeins sumar þessara eininga með tilgang stigveldis fyrir innra eftirlit innkaupa. Sjálfgefið er að fyrirtækisins af gerðinni Fyrirtæki tiltæk.  
3. Smella á flipa fyrir Færibreytur stefnureglugerðar
4. Veljið 'innkaupastefna\stjórnunarregla innkaupastefnu', í trénu.
    * Er forgangsröð er skilgreind fyrir lausn reglu á reglustigi. Hins vegar er hægt að hnekkja forgangsröð einstaka stefnureglugerða fyrir sumar gerðir reglna. Til dæmis mætti skilgreina forgangsröð fyrir innkaupastefnur í þessari röð: kostnaðarstaður, deild, fyrirtæki. Fyrir stefnureglu vörulista viltu kannski hafa forgangsröð: deild, kostnaðarstaður, fyrirtæki. Forgangsröð má breyta fyrir stefnureglu vörulista. Þegar starfsmaður stofnar beiðni, er vörulistinn sem birtist ákvarðaður af reglunum sem tengjast deild starfsmannsins, síðan kostnaðarstað hans og svo fyrirtæki þeirra.  
    * Ef meira en eitt stjórnunarstig er skráð er hægt að nota örvarnar Upp/Niður til að stilla forgangsröð fyrir reglu innkaupapantanastýringar.  
5. Lokið síðunni.

## <a name="create-a-new-policy"></a>Stofna nýja reglu
1. Smellið á „Nýtt“.
2. Í reitinn Heiti skal slá inn gildi.
3. Sláið inn gildi í reitnum „Lýsing“.
    * Stök innkaupastefna geta átt aðeins við um eitt stigveldi fyrirtækis. Til dæmis gæti eitt stigveldi kallast "landsvæði" og einn kallast "deild" og verið með mismunandi innkaupastefna fyrir hverja.  
    * Veljið fyrirtæki sem stefnan á við.  
4. Smellt er á örina til að bæta við völdu fyrirtæki
    * Hægt er að endurtaka þetta ferli til að bæta við fleiri fyrirtækjum.  

## <a name="add-a-policy-rule"></a>Bæta við stefnureglu
1. Á listanum stefnureglugerð, veljið reglu fyrir tilgang beiðni.
    * Þú stofnar Regla sem stillir sjálfgefinn tilgang beiðni á gerðina Notkun en heimilar að velja í staðinn áfyllingargerð.  
2. Smellt er á Stofna stefnureglu.
3. Velja skal Já í svæðinu Leyfa handvirka hnekkingu.
4. Smellið á „Loka“.
    * Núna er hægt að setja upp aðrar stefnureglur fyrir innkaupastefnu.   Athugið að stefnureglugerð getur ekki haft reglur um skörun sem eru virkar á sama tíma innan einnar innkaupastefnu.  
5. Lokið síðunni.
6. Lokið síðunni.


