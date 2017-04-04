---
title: "POS virkni án nettengingar"
description: "Þessi grein veitir upplýsingar um ótengdan ham fyrir Retail Modern POS þar sem POS-tæki skipta sjálfkrafa úr rásar gagnagrunns í ótengda gagnagrunn ef retail-þjónn er ekki tiltækur. Þessi grein einnig inniheldur upplýsingar um almenna uppsetningu fyrir ótengdan ham og útskýrir samstillingu gagna sem fer á milli ótengda gagnagrunns og gagnagrunns rásar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>POS virkni án nettengingar

Þessi grein veitir upplýsingar um ótengdan ham fyrir Retail Modern POS þar sem POS-tæki skipta sjálfkrafa úr rásar gagnagrunns í ótengda gagnagrunn ef retail-þjónn er ekki tiltækur. Þessi grein einnig inniheldur upplýsingar um almenna uppsetningu fyrir ótengdan ham og útskýrir samstillingu gagna sem fer á milli ótengda gagnagrunns og gagnagrunns rásar.

<a name="overview"></a>Yfirlit
--------

Í Retail Modern POS punktur sölustað tækis fer í tengingar í hvert sinn sem retail-þjónn er ekki tiltækur. Þess vegna ef tengingu við retail-þjónn er ekki tekið Retail Modern POS sjálfkrafa skiptir ótengdan gagnagrunn. Við sölufærslu, ef gagnabeiðni gengur ekki í gegn innan tímalokunarbils sem er skilgreint í ótengda sniðinu,skiptir Retail Modern POS sjálfkrafa yfir í ótengdan gagnagrunn og heldur áfram við sölufærslu. Á meðan POS-tæki er í ótengdum ham, reynir Retail Modern POS að endurtengjast við retail-þjón eftir tímabil endurtengingartilraunar sem er skilgreint í ótengda sniðinu. Þessi endurtengingartilraun gerist aðeins við upphaf færslu.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>Ákvarða tengingarmáta Retail Modern POS

Staða hauss í Retail Modern POS tilgreinir gildandi stöðu tengingar, og **staða Tengingar** glugga sýnir stöðu síðustu tilraunar til að samstilla við ótengda gagnagrunninn. [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Stofna hnappinn til að skipta handvirkt milli tengds og ótengds hams

Hægt er að bæta við hnappi í Retail Modern POS til að skipta handvirkt á milli tengds og ótengds hams. Stofna hnappa fyrir POS aðgerð **917 – staða gagnagrunnstengingar**. Heiti þessa hnapps er **Aftengja** þegar Retail Modern POS er tengd við retail-þjónn og **Tengja** þegar hún er aftengd. Hægt er að nota þennan hnapp til að skoða tengingu, og til að aftengjast frá retail-þjón eða tengjast. [![Aftengja hnappinn Retail Modern POS](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Uppsetning
Til að virkja ótengds stuðning fyrir POS tæki (afgreiðslukassa) er stillt á **Notendaþjónusta án tengingar** valkostinn að **Já** á í **Skrá** síðu. Nýja einingu gagnagrunns rásar er stofnað og bætt við verslunarinnar gagnaflokkur rásar. Keyrið síðan öll áskilin dreifingaráætlununum til að mynda gagnapakka fyrir ótengdan gagnagrunn. Næst skal setja upp Retail Modern POS ótengt útgáfu. Uppsetningarferlið býr ótengdan gagnagrunn. Auk þess að setja upp Microsoft SQL Server 2014 Express ef nauðsynlegt er. Ótengd gagnasamstillingu hefst eftir á fyrsta innskráning í Retail Modern POS.

## <a name="data-synchronization"></a>Samstilling gagna
Retail-verkraðari er notuð til að senda aðalgögn í ótengdan gagnagrunn. Að sjálfgefnu þegar dreifingaráætlun er keyrð, eru breytingar á gögnum sendar til gagnagrunns rásar og ótengdum gagnagrunni. Retail Modern POS inniheldur async samstillingarsafnið, sem hleður niður öll tiltæk gagnapakka og setur þær í ótengda gagnagrunninn. Ef einhverjar færslur eru stofnaðar ótengt, hleður Retail Modern POS þeim inn á retail-þjón þannig að þeir geta fært inn í gagnagrunn rásar. Ótengd samstillingu getur átt sér stað eingöngu ef Retail Modern POS er í gangi. [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)


