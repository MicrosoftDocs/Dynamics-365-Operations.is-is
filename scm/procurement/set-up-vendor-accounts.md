---
title: "Setja upp lánardrottnalykla"
description: "Þetta efnisatriði lýsir gerðir upplýsinga sem þarf að tilgreina þegar þú stofnar nýjan lykil lánardrottins."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendBankAccounts, VendTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2f0ddf0e4cff0d799a7baf6bdc9d5c2da0622f4d
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-vendor-accounts"></a>Setja upp lánardrottnalykla

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir gerðir upplýsinga sem þarf að tilgreina þegar þú stofnar nýjan lykil lánardrottins.

Þegar lánardrottnalykill er stofnaður eru færðar inn upplýsingar um lánardrottinn. Þessar upplýsingar eru notaðar til að fylla út skjöl sjálfvirkt og rekja aðgerðir með þeim lánardrottni. Til dæmis er hægt að stilla eftirfarandi upplýsingar fyrir lánardrottinn:

-   Úthluta lánardrottnaflokki. Allir lánardrottnar verða að fá úthlutað lánardrottnaflokk. Lánardrottnar í lánardrottnaflokki hafa sameiginlegar færibreytur. Til dæmis geta þeir notað sömu greiðsluskilmála.
-   Stilla lánardrottinn fyrir innflutning vörulista. Lánardrottnar geta veitt skrá sem inniheldur vörulista yfir vörur þeirra og þjónustu. Þessi skrá getur verið hlaðið upp þannig að starfskraftar fyrirtækisins geta pantað frá lánardrottni.
-   Úthluta lánardrottninum til innkaupategunda.
-   Leyfa fyrirliggjandi lánardrottni að stunda viðskipti við annan lögaðila í fyrirtækinu.
-   Setja lánardrottinn í bið fyrir sérstakar gerðir af færslum.
-   Setja upp bankaupplýsingar fyrir lánardrottin, svo að hægt sé að senda greiðslur rafrænt.
-   Setja upp skatta-, afhendingar-, reiknings- og greiðsluupplýsingar fyrir lánardrottinn. Að sjálfgefnu eru þessar stillingar afritaðar yfir í ný skjöl sem stofnuð eru fyrir lánardrottininn.
-   Setja upp sjálfgefnar fjárhagsvíddir sem eru notaðar til að bóka sjálfkrafa færslur með lánardrottni í fjárhagsbókhald.

Hægt er að flýta fyrir stofnun lánardrottnalykla með því að stofna sniðmát. Til að stofna sniðmát, á síðunni **Lánardrottinn** á aðgerðasvæðinu skal smella á **Valkostir** &gt; **Færsluupplýsingar**. Smelltu síðan á **sniðmát reikningsskila** Sniðmát reikningsskila er deilt með öðrum notendum.  

Einnig er hægt að stofna sniðmát notanda til eigin nota. Ekki hægt að eyða lánardrottni sem er tengd við aðrar færslur, eins og tengiliði eða vörur.

## <a name="vendor-account-numbers"></a>Númer lánardrottnalykils
Lykilnúmer er einkvæmt auðkenni fyrir lánardrottinn. Hægt er að stofna lykilnúmer sjálfkrafa þegar lánardrottinn er stofnaður. Einnig er hægt að skilgreina númeraröðina þannig að lykilnúmer eru færð inn handvirkt. Til dæmis mætti nota símanúmer lánardrottins sem auðkenni.

## <a name="vendor-organizations-and-individual-vendors"></a>Fyrirtæki lánardrottins og einstaka lánardrottnar
Þegar þú stofnar nýjan lánardrottnalykil, verður að velja hvort lánardrottinn er fyrirtæki eða einstakling. Valið hefur áhrif á þær upplýsingar sem fylla þarf út fyrir lánardrottinn. Þessar upplýsingar eru í fornafn eftirnafn, og titill fyrir einstakling. Fyrir fyrirtæki innihalda þessar upplýsingar fyrirtækisnúmerið og fjölda starfsmanna fyrir fyrirtæki.

## <a name="addresses"></a>Aðsetur
Fyrir hvern lánardrottinn, hægt er að skilgreina fleiri en eitt aðsetur, sem hvert er notað í mismunandi tilgangi. Til dæmis, hægt er að stofna aðsetur sem hefur tilganginn **Reikningur**. Ef greiða á lánardrottninum með ávísun er hægt setja upp aðsetur með tilganginn **greiðsla til**. Ef þú þarft að tilgreina aðsetur til að nota fyrir peningaflutninga til erlendra banka, verður tilgangurinn **SWIFT**.

## <a name="vendor-contacts"></a>Tengiliður lánardrottins
Hægt er að geyma tengiliði fyrir lánardrottin. Síðan er hægt að nota þessar tengiliðum á skjöl, eins og innkaupapantanir eða beiðnir um tilboð (RFQ).  

Til að bæta við tengiliðum fyrir lánardrottinn, á **Allir lánardrottnar** síðunni á **Lánardrottinn** flipanum í **Setja upp** flokknum, er smellt á **Tengiliðir** &gt; **Bæta við tengiliðum**.  

Hægt er að stofna tengiliði lánardrottins frá grunni. Einnig er hægt að afrita upplýsingar frá annarri manneskju sem er þegar skráð í Microsoft Dynamics 365 for Operations og breyta upplýsingum eins og þarf.  

**Athugasemd:** að Bæta við tengilið fyrir lánardrottin er ekki það sama og að bæta við tengslaupplýsingum fyrir þann lánardrottinn. Þótt þú gætir bætt við almennum upplýsingum um tengslaupplýsingum við fyrir lánardrottinn, gætu einnig verið til staðar fjölmargir tilteknir einstaklingar sem eru tengiliðir í því fyrirtæki, og eru allir með sínar eigin tengslaupplýsingar.  

Ekki er hægt að eyða færslu tengiliðar ef vísað er til tengiliðs í skjali. Í staðinn er hægt að óvirkja tengiliðinn.  

Hægt er að bæta við tengiliðum lánardrottins við persónulega tengiliði í Microsoft Office 365. Hins vegar verður fyrst að setja upp samstillingu milli Dynamics 365 for Operations og Office 365 í bæði samstillingu Microsoft Exchange Server og uppsetningarleiðsögn Microsoft Outlook.

## <a name="vendors-in-different-legal-entities"></a>Lánardrottnar í öðrum lögaðilum
Ef lánardrottinn er skráð aðeins fyrir einn lögaðila í fyrirtækinu, og aðrir lögaðilar þurfa að skrá sama lánardrottin, er hægt að nota **Bæta lánardrottni við annan lögaðila** síðu til að skilgreina lánardrottinn til að geta átt viðskipti við annan lögaðila. Þú verður að velja lánardrottnaflokk, gjaldmiðill, biðstöðu fyrir lánardrottinn í völdum lögaðila.  

Ef margir lögaðilar innan samstæðunnar eiga viðskipti við sama lánardrottin og hver þeirra er með sérstakan lánardrottinslykil fyrir hann er hægt að steypa saman kennum aðila úr lánardrottnalyklum. Á þennan hátt má deila upplýsingar eins og aðsetur og fjölda starfsmanna, þannig að unnt er að uppfæra hana eingöngu á einum stað.  

Fylgið eftirfarandi skrefum til að steypa saman kennum aðila.

1.  Á við **Altækrar aðsetursbókar** síðunni, Veljið aðsetursbókarfærslurnar sem standa fyrir þann lánardrottin í hverjum lögaðila sem á að vera með í vörpuninni.
2.  Í aðgerðasvæðinu er smellt á **sameina færslur**.

## <a name="agreements"></a>Samningar
Þegar sett er upp lánardrottnalykil viltu kannski líka skrá samninga sem hefur verið gerðir við lánardrottininn. Hægt er að setja upp verð- og afsláttarsamninga með því að nota aðgerðirnar í færslu lánardrottins. Einnig er hægt að setja upp innkaupasamning á **Innkaupasamningar** síðunni.

## <a name="putting-a-vendor-on-hold"></a>Setja lánardrottinn í bið
Hægt er að setja lánardrottinn í bið fyrir ýmsar færslugerðir. Eftirtaldir valkostir eru í boði:

-   **Engir** – Engin bið hefur verið sett á lánardrottin.
-   **Reikningur** – Ekki má stofna neina reikninga fyrir þennan lánardrottinn.
-   **Allir** – Lánardrottininn er í bið fyrir allar færslugerðir. Þessar færslugerðir innifela innkaupabeiðnir, reikningar og greiðslur.
-   **Greiðsla** – Ekki er hægt að mynda neinar greiðslur fyrir þennan lánardrottin.
-   **Beiðni** - Aðeins er hægt að stofna innkaupabeiðnir Ekki er hægt að stofna neinar aðrar færslur.
-   **Aldrei** – lánardrottins er aldrei sett í bið vegna óvirkni.

Þegar lánardrottinn er sett í bið er einnig hægt að tilgreina ástæðu og dagsetning þegar biðstöðunni skal ljúka. Ef ekki er fært inn lokadagsetningu, endist biðstaða lánardrottins í óráðinn tíma.

## <a name="vendor-invoice-account"></a>Reikningslykill lánardrottins
Ef fleiri en einn lánardrottinn hefur sama aðsetur eða ef reikningsfært er á lánardrottinn í gegnum þriðja aðila, geturðu tilgreint reikningslykil á lánardrottinsfærslu. Reikningslykill er lykill sem reikningsupphæð er skuldfærð á þegar reikningur lánardrottins er stofnaður úr innkaupapöntun. Ef reikningslykill er ekki færður inn er lánardrottnalykill notaður sem reikningslykill.

## <a name="vendor-bank-accounts"></a>Bankareikningur lánardrottins
Ef þú þarft að framkvæma greiðslur inn á bankareikning lánardrottins er hægt að færa inn upplýsingar um banka og bankareikninga lánardrottins í **bankareikningar Lánardrottins** síðu. Þú getur einnig fær inn upplýsingar um villuleit og greiðslur fyrir valinn bankareikning. Til dæmis er hægt færa inn fyrirframkvittanir á bankareikning lánardrottins. Þessar fyrirframkvittanir má nota til að sannprófa nákvæmni reikningsgagna, svo sem leiðarnúmer og reikningsnúmer. Tilgreina verður sjálfgefinn lykill fyrir greiðslur til lánardrottins. Hins vegar þegar þú framkvæmir raunverulega greiðslu, er hægt að breyta þessum lykli í einhvern af öðrum lyklar lánardrottins.

## <a name="ledger-accounts"></a>Fjárhagslyklar
Hægt er að tilgreina sjálfgefnir lyklar sem birtast sjálfkrafa í færslubækur fyrir reikning lánardrottins fyrir tilgreindan lánardrottin. Þessi virkni getur komið að gagni ef þú greiðir yfirleitt fyrir sömu gerðir vara eða þjónustu frá sama lánardrottni með tímanum. Þegar tilgreindur er sjálfgefinn lykill, er fljótlegt og hagkvæmt að slá inn færslur í reikningsbók. Sjálfgefnir lyklar sem þú tilgreinir eru ekki notuð fyrir innkaupapantanir eða fyrir reikninga lánardrottins sem eru færðar inn í **lánardrottinsreikning** síðu.  

Þú velur sjálfgefna lykla á **uppsetning sjálfgefins lykils** síðu, sem hægt er að opna úr **Reiknings** flipanum í færslu lánardrottins. Lyklar sem valdir eru hér birtist í síaða lista yfir reikninga fyrir lykil lánardrottins þegar þú slærð inn færslu í færslubók. Hægt er að setja einn af lyklunum sem sjálfgefinn lykil.




