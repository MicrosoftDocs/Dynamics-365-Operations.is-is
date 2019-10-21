---
title: Bókun í bakfærslubók
description: Þetta efni lýsir getu sem gerir þér kleift að bakfæra fylgiskjöl af færslulista fylgiskjala eða úr fjárhagsfærslubókum.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248586"
---
# <a name="reverse-journal-posting"></a>Bókun í bakfærslubók

[!include [banner](../includes/banner.md)]

Þetta efni lýsir getu Microsoft Dynamics 365 Finance sem gerir þér kleift að bakfæra heila færslubók eða bakfæra eitt eða fleiri fylgiskjöl af færslulistum fylgiskjala án tillits til uppruna. 

## <a name="reversing-journals"></a>Bakfærsla færslubóka

Hægt er að bakfæra eina færslubókarlínu í einu. Með bakfærslu á færslubók geturðu bakfært heila fjárhagsfærslubók. Til að bakfæra færslubók: 
- Opnaðu fjárhagsfærslubókina og síaðu á bókaðar færslubækur
- Smelltu á bakfærsluvalmyndina efst á síðunni
- Þú munt sjá heildarfjölda fylgiskjala og fylgiskjalalínur sem og heildarfjárhæð línanna sem verið er að bakfæra
- Veldu Já til að nota núverandi færsludagsetningar eða Nei til að slá inn nýja. Í sumum tilvikum kann tímabil upphaflegrar færslu að vera lokað og þú vilt færa inn nýja færsludagsetningu fyrir bakfærsluna.
- Ef þú valdir Nei, slærðu inn færsludagsetningu fyrir bakfærsluna. 
- Sláðu inn athugasemd sem þú vilt bæta við bakfærsluna
- Smelltu á hnappinn Bakfæra.

Færslunar verða bakfærðar. 

Ef fjöldi fylgiskjala er yfir 100 línur, verður bakfærsluferlið keyrt með runuvinnslunni. Þú getur skoðað niðurstöður bakfærslu með því að skoða athugasemdir í runuvinnslunni sem var keyrð. Allar bilanir verða tilgreindar í runuvinnslusögunni.

Ef fjöldi fylgiskjala er 100 línur eða minna, mun bakfærsluvinnslan keyra þegar í stað. Niðurstöðurnar verða kynntar í glugga sem sýnir öll fylgiskjöl sem ekki var hægt að bakfæra og ástæðu þess að ekki var hægt að bakfæra þau. Smelltu á OK til að loka svarglugganum.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Bakfærsla fylgiskjala af færslulista fylgiskjala. 

Þú getur líka bakfært fylgiskjöl úr **Fylgiskjalafærslulisti** yfir allar undirfærslubækur. Að auki geturðu bakfært fleiri en eitt fylgiskjal í einu. 

Til að bakfæra eitt eða fleiri fylgiskjöl: 
- Smelltu á bakfærsluvalmyndina efst á síðunni
- Þú munt sjá heildarfjölda fylgiskjala og fylgiskjalalínur sem og heildarfjárhæð línanna sem verið er að bakfæra
- Veldu Já til að nota núverandi færsludagsetningar eða Nei til að slá inn nýja. Í sumum tilvikum kann tímabil upphaflegrar færslu að vera lokað og þú vilt færa inn nýja færsludagsetningu fyrir bakfærsluna.
- Ef þú valdir Nei, slærðu inn færsludagsetningu fyrir bakfærsluna. 
- Sláðu inn athugasemd sem þú vilt bæta við bakfærsluna
- Smelltu á hnappinn Bakfæra.

Færslunar verða bakfærðar. 

Ef fjöldi fylgiskjala er yfir 100 línur, verður bakfærsluferlið keyrt með runuvinnslunni. Þú getur skoðað niðurstöður bakfærslu með því að skoða athugasemdir í runuvinnslunni sem var keyrð. Allar bilanir verða tilgreindar í runuvinnslusögunni.

Ef fjöldi fylgiskjala er 100 línur eða minna, mun bakfærsluvinnslan keyra þegar í stað. Niðurstöðurnar verða kynntar í glugga sem sýnir öll fylgiskjöl sem ekki var hægt að bakfæra og ástæðu þess að ekki var hægt að bakfæra þau. Smelltu á OK til að loka svarglugganum.

