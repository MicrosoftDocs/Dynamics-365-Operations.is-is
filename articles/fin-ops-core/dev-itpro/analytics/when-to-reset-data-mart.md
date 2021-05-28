---
title: Hvenær á að endurstilla gagnaskemma
description: Í þessu efnisatriði er farið yfir þær aðstæður sem hugsanlega þarf að bæta með því að endurstilla gagnaskemmu og aðstæður þar sem gagnaskemma er ólíkleg til að hjálpa.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988993"
---
# <a name="when-to-reset-a-data-mart"></a>Hvenær á að endurstilla gagnaskemma

Að endurstilla gagnaskemmu getur tekið sinn tíma. Í einhverjum kringumstæðum gæti þessi aðgerð ekki verið rétta lausnin. Í þessu efnisatriði er farið yfir þær aðstæður sem hugsanlega þarf að bæta með því að endurstilla gagnaskemmu, auk aðstæðna þar sem gagnaskemma er ólíkleg til að hjálpa.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Hvenær þarf að endurstilla gagnaskemmu?
Íhugið eftirfarandi spurningar áður en gagnaskemma er endurstillt. Ef einni eða fleiri spurningum var svarað játandi gæti það bent til þess að fyrirtækið gæti hagnast á því að láta endurstilla gagnaskemmuna.

- Var gagnagrunnur forritsins endurheimtur?
- Ef þú opnaðir þjónustutilvik og tæknimaður hjá notendaþjónustu hefur sagt þér að endurstilla gagnaskemmuna sem hluti af skrefi úrræðaleitar.
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Hvenær borgar sig ekki að endurstilla gagnaskemmu?
Undir sumum kringumstæðum viljum við ekki endurstilla gagnaskemmu. Eftirfarandi eru með: 

- Þú finnur fyrir vandamálum varðandi afköst sem tengjast gagnasamstillingu. 
- Ef upp koma endurtekin endurstillingarmynstur vegna einhverra af eftirfarandi ástæðum: 
  - **Gögn vantar** 
  - **Föst samþættingarstaða** 
  - **Útrunnar skrár** - Útrunnar skrár einar og sér réttlæta ekki endilega endurstillingu gagnaskemmunnar. Ef um er að ræða stórt gagnasafn mun endurstillingarferlið taka sinn tíma, en ólíklegt er að það lagi stöðuna.
 
## <a name="what-is-a-data-mart-reset"></a>Hvað er endurstilling gagnaskemma?
- Endurstilling hefst aðeins þegar fyrirliggjandi verkum er lokið. Þetta tryggir að gömul gögn eru ekki sett inn. Á þessu stigi gætu birst skilaboð á borð við: „Ekki var hægt að setja í gang endurstillingu gagnaskemmunnar vegna verks sem er í gangi. Reyna skal aftur síðar.
- Endurstillingin gerir samþættingarverkin óvirk og eyðir öllum gögnum gagnaskemmunnar. Samþætting er virkjuð aftur.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Ef ég endurstilli gagnaskemmu missi ég þá skýrslur sem ég hef þegar hannað? 
Nei, skýrslurnar þínar eru vistaðar í SQL-töflum sem hafa ekki áhrif á endurstillingu gagnaskemma. Ef þú hefur áhyggjur af að missa skýrslur sem þú hefur hannað geturðu tekið afrit af hönnuninni sem þú vilt ekki missa. Opnið Skýrsluhönnun og farið í **Fyrirtæki > Fyrirtæki > Einingar > Útflutningur** til að afrita þau.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Er nauðsynlegt að allir notendur fari úr kerfinu til að endurstilla gagnaskemma?
Nei, notendur geta haldið áfram að vinna í kerfinu við endurstillingu gagnaskemma. Þeir geta þó ekki fengið aðgang að skýrslum sem búnar voru til með Financial Reporter fyrr en endurstillingunni er lokið. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
