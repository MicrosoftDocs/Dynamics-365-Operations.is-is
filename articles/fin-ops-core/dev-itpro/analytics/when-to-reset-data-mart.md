---
title: Hvenær á að endurstilla gagnaskemma
description: Í þessu efnisatriði er farið yfir þær aðstæður sem hugsanlega þarf að bæta með því að endurstilla gagnaskemmu og aðstæður þar sem gagnaskemma er ólíkleg til að hjálpa.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093213"
---
# <a name="when-to-reset-a-data-mart"></a>Hvenær á að endurstilla gagnaskemma

Að endurstilla gagnaskemmu getur tekið sinn tíma. Í einhverjum kringumstæðum gæti þessi aðgerð ekki verið rétta lausnin. Í þessu efnisatriði er farið yfir þær aðstæður sem hugsanlega þarf að bæta með því að endurstilla gagnaskemmu, auk aðstæðna þar sem gagnaskemma er ólíkleg til að hjálpa.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Hvenær þarf að endurstilla gagnaskemmu?
Íhugið eftirfarandi spurningar áður en gagnaskemma er endurstillt. Ef einni eða fleiri spurningum var svarað játandi gæti það bent til þess að fyrirtækið gæti hagnast á því að láta endurstilla gagnaskemmuna.

- Gagnagrunnur hugbúnaðarins var endurheimtur en gagnagrunnur gagnaskemma var ekki endurheimtur.
- Þú sérð röng gögn fyrir reikningstímabil sem koma ekki til vegna vandamála varðandi hönnun skýrslunnar.
- Þú sérð röng gögn fyrir reikningstímabil og færslur eru skráðar undir samþættingartilraunir á síðunni **Staða samþættingar** í skýrsluhönnun (ræsið skýrsluhönnun og veljið **Verkfæri > Staða samþættingar**).
- Þjónustutilvik var opnað og tæknimaður hjá notendaþjónustu hefur sagt þér að endurstilla gagnaskemmuna sem hluti af skrefi úrræðaleitar.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Hvenær borgar sig ekki að endurstilla gagnaskemmu?
Undir sumum kringumstæðum viljum við ekki endurstilla gagnaskemmu. Eftirfarandi eru með: 

- Hvenær sem ástæða er ekki tiltekin í þessu efnisatriði.
- Þú finnur fyrir vandamálum varðandi afköst sem tengjast gagnasamstillingu. Við þessar kringumstæður mun endurstilling gagnaskemmu líklega ekki koma að neinu gagni.
- Ef upp koma endurtekin endurstillingarmynstur vegna einhverra af eftirfarandi ástæðum: 
  - **Vantar gögn** - Fyrst skal útiloka vandamál varðandi skýrsluhönnun og tímasetningu gagnasamstillingar; til að mynda tekurðu eftir því að staðfestingarvörpun hafi ekki verið keyrð frá því að týnd gögn voru bókuð.
  - **Föst samþættingarstaða** - Ef samþættingin er hæg eða virðist föst er ólíklegt að endurstilling gagnaskemmunnar muni leysa vandamálið.
  - **Tilraunir til endurstillingar hafa ekki tekist** - Ef margar tilraunir til að ljúka endurstillingu hafa verið reyndar og hafa ekki tekist vegna þess að gögn vantar er mælt með því að opna þjónustutilvik og vinna með tæknimanni hjá notendaþjónustu til að átta sig á vandanum áður en reynt er að endurstilla gagnaskemmuna aftur.
  - **Útrunnar skrár** - Útrunnar skrár einar og sér réttlæta ekki endilega endurstillingu gagnaskemmunnar. Ef um er að ræða stórt gagnasafn mun endurstillingarferlið taka sinn tíma, en ólíklegt er að það lagi stöðuna.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Það sem endurstilling gagnaskemmu gerir ekki  
- Endurstilling hefst aðeins þegar fyrirliggjandi verkum er lokið. Þetta tryggir að gömul gögn eru ekki sett inn. Á þessu stigi gætu birst skilaboð á borð við: „Ekki var hægt að setja í gang endurstillingu gagnaskemmunnar vegna verks sem er í gangi. Reyna skal aftur síðar.
- Endurstillingin gerir samþættingarverkin óvirk og eyðir öllum gögnum gagnaskemmunnar. Samþætting er virkjuð aftur.

> [!NOTE]
> Eftirfarandi punktar tilgreina tvö atriði sem endurstilling gagnaskemmunnar mun *ekki* gera. <br>
> - Endurstillingar hreinsa ekki hönnun skýrslu. <br>
> - Endurstillingar hreinsa ekki fyrirtækisgögn eða notendagögn nema þau séu valin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]