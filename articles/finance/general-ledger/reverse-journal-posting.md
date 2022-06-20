---
title: Bakfæra bókun í færslubók
description: Þessi grein lýsir getu sem gerir þér kleift að bakfæra fylgiskjöl úr fylgiskjalsfærslulistanum eða úr fjárhagsbókum.
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bec7d5d0dd64a2d89b00e2aa630a4fe670feaa2b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868403"
---
# <a name="reverse-journal-posting"></a>Bakfæra bókun í færslubók

[!include [banner](../includes/banner.md)]

Þessi grein lýsir getu Microsoft Dynamics 365 Fjármál sem gerir þér kleift að bakfæra heila færslubók, eða bakfæra eitt eða fleiri fylgiskjöl af fylgiskjalsfærslulistanum, óháð uppruna þeirra. 

Áður en þú getur notað einn af þeim eiginleikum sem lýst er í þessari grein verður að kveikja á honum í kerfinu þínu. Stjórnendur geta notað vinnusvæði **Eiginleikastjórnun** til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:
 - Eining: fjárhagur
 - Heiti eiginleika: **Fjöldabakfærslur fyrir mörg skjöl**

## <a name="reversing-journals"></a>Bakfærsla færslubóka

Hægt er að bakfæra eina færslubókarlínu í einu. Með bakfærslu á færslubók geturðu bakfært heila fjárhagsfærslubók. Til að bakfæra færslubók: 

- Síaðu bókaðar færslur og opnaðu **Línur** í færslubókinni.
- Veldu valmyndina **Bakfæra** efst á síðunni.
- Þú munt sjá heildarfjölda fylgiskjala og fylgiskjalalínur sem og heildarfjárhæð línanna sem verið er að bakfæra.
- Veldu **Já** til að nota núverandi færsludagsetningar eða **Nei** til að slá inn nýja. Í sumum tilvikum kann tímabil upphaflegrar færslu að vera lokað og þú verður að færa inn nýja færsludagsetningu fyrir bakfærsluna.
- Ef þú velur **Nei** slærðu inn færsludagsetningu fyrir bakfærsluna. 
- Sláðu inn athugasemd sem þú vilt bæta við bakfærsluna.
- Veljið hnappinn **Bakfæra**.

Færslunar verða bakfærðar. 

Ef fylgiskjalið inniheldur yfir 100 línur, verður bakfærsluferlið keyrt með runuvinnslunni. Þú getur skoðað niðurstöðurnar með því að skoða athugasemdir í runuvinnslunni. Öll viðskipti sem ekki var hægt að bakfæra verða skráð í sögu runuvinnslunnar.

Ef fylgiskjalið inniheldur 100 línur eða færri mun bakfærsluvinnslan keyra þegar í stað. Niðurstöðurnar verða kynntar í glugga sem sýnir öll fylgiskjöl sem ekki var hægt að bakfæra, ásamt ástæðu þess að ekki var hægt að bakfæra þau. Veldu **Í lagi** til að loka svarglugganum.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Bakfærsla fylgiskjala af færslulista fylgiskjala. 

Þú getur líka bakfært fylgiskjöl úr **Fylgiskjalafærslulisti** yfir allar undirfærslubækur. Að auki geturðu bakfært fleiri en eitt fylgiskjal í einu. 

Til að bakfæra eitt eða fleiri fylgiskjöl: 

- Veldu valmyndina **Snúa öllum færslubókarfellilistanum** efst á síðunni.
- Heildarfjöldi fylgiskjala og fylgiskjalalínur er birtur, sem og heildarfjárhæð línanna sem verið er að bakfæra.
- Veldu **Já** til að nota núverandi færsludagsetningar eða **Nei** til að slá inn nýja. Í sumum tilvikum kann tímabil upphaflegrar færslu að vera lokað og þú verður að færa inn nýja færsludagsetningu til að bakfæra hana.
- Ef þú velur **Nei** slærðu inn færsludagsetningu fyrir bakfærsluna. 
- Sláðu inn athugasemd til að lýsa bakfærslunni.
- Veljið hnappinn **Bakfæra**.

Færslunar verða bakfærðar. 

Ef það eru yfir 100 fylgiskjalalínur verður bakfærsluferlið keyrt með runuvinnslunni. Þú getur skoðað niðurstöðurnar með því að skoða athugasemdir í runuvinnslunni. Öll viðskipti sem ekki var hægt að bakfæra verða skráð í sögu runuvinnslunnar.

Ef fjöldi fylgiskjala er 100 línur eða færri mun bakfærsluvinnslan keyra þegar í stað. Niðurstöðurnar munu birtast í glugga sem sýnir öll fylgiskjöl sem ekki var hægt að bakfæra, ásamt ástæðu þess. Veldu **Í lagi** til að loka svarglugganum.

Aðeins er hægt að bakfæra færslur ef þær uppfylla viðskiptareglur um bakfærslur. Ekki er hægt að bakfæra greiðslur lánardrottins með því að nota möguleikann sem lýst er í þessari grein. Lánardrottnagreiðslur verður að bakfæra með því að fylgja skrefunum sem talin eru upp í [Bakfæra lánardrottnagreiðslu](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
