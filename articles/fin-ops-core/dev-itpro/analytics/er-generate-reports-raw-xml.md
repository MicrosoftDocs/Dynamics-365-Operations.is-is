---
title: Búa til skýrslur með því að bæta við efni sem hráu XML
description: Hægt er að hanna snið rafrænnar skýrslugerðar sem býr til skjöl á útleið í XML-sniði.
author: kfend
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 87b70d5893d71e5022205a2f39f8263edf6d5280
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277543"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>Búa til skýrslur með því að bæta við efni sem hráu XML

[!include[banner](../includes/banner.md)]

Hægt er að nota nýju sniðseininguna **HRÁTT XML** til að hanna snið rafrænnar skýrslugerðar sem búa til skjöl á útleið í XML-sniði. Í sumum tilfellum gætir þú frekar viljað bæta hráum XML-gögnum við þessar skýrslur af einni eða fleiri af eftirfarandi ástæðum:

- Það er þægilegra að nota hrátt XML fyrir upprunalegu hönnunina og áframhaldandi viðhald á skýrslu vegna þess að hægt er að búa til XML-uppbygginguna sjálfkrafa með því að framkvæma keyrslusegð. Þess vegna þarf ekki að ákvarða margar bindingar fyrir margar sniðseiningar á hönnunartíma. Það er mögulegt þegar gagnagjafarnir sem eru notaðir innihalda upplýsingar sem hægt er að nota til að búa til XML-einingar á meðan skýrslan er búin til.
- Ekki er hægt að nota neina aðra aðferð til að fylla skýrsluna með XML-efni sem áður var móttekið og geymt í kerfinu. Til dæmis gæti XML-svarið sem myndað er þurft að innihalda efni XML-beiðni sem var send áður.
- Ekki er hægt að nota neina aðra aðferð til að setja stafi inn í myndaða skjalið á grundvelli númerakóða þeirra. Fyrir sum tungumál og stafi eru kóðar af þessari tegund ekki til. Sem dæmi er gríski stafurinn rho (ρ) og HTML-einingakóðar á borð við \&e-áherslumerki fyrir *e* sem hefur hljóðgildistákn (é).

> [!NOTE]
> Hafa skal í huga að ramminn stjórnar því ekki hvort XML-efnið sem er sett á myndaða skjalið með því að nota sniðið **HRÁTT XML** sé rétt.

Til að læra meira um þennan eiginleika skal spila verkefnaleiðbeiningarnar **Nota hrá XML-gögn rafrænnar skýrslugerðar til að búa til XML-skýrslur (hluti 1: Hanna gagnalíkan)** og **Rafræn skýrslugerð notar hrá XML-gögn til að búa til XML-skýrslur (hluti 2: Hanna og keyra skýrslu)** sem eru hluti af viðskiptaferlinu **7.5.4.3 Acquire/Develop IT þjónustu-/lausnaþáttum (10677)** og sem hægt er að hlaða niður frá [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Þessar verkefnaleiðbeiningar fylgja þér í gegnum ferlið við að grunnstilla snið rafrænnar skýrslugerðar til að setja hrá XML-gögn inn í myndaðar skrár.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
