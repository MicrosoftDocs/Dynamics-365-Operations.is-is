---
title: Bókun í bakfærslubók
description: Þetta efni lýsir getu sem gerir þér kleift að bakfæra fylgiskjöl af færslulista fylgiskjala eða úr fjárhagsfærslubókum.
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
ms.openlocfilehash: fb1615312e9fd1786a5a0050dda3e9e9b20fe710
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753779"
---
# <a name="reverse-journal-posting"></a>Bókun í bakfærslubók

[!include [banner](../includes/banner.md)]

Þetta efni lýsir getu Microsoft Dynamics 365 Finance sem gerir þér kleift að bakfæra heila færslubók eða bakfæra eitt eða fleiri fylgiskjöl af færslulistum fylgiskjala án tillits til uppruna. 

Áður en hægt er að nota eiginleikann sem lýst er í þessu efnisatriði þarf að vera kveikt á honum í kerfinu. Stjórnendur geta notað vinnusvæði **Eiginleikastjórnun** til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:
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

Aðeins er hægt að bakfæra færslur ef þær uppfylla viðskiptareglur um bakfærslur. Ekki er hægt að bakfæra lánardrottnagreiðslum með því að nota getu sem lýst er í þessu efni. Lánardrottnagreiðslur verður að bakfæra með því að fylgja skrefunum sem talin eru upp í [Bakfæra lánardrottnagreiðslu](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
