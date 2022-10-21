---
title: Yfirlit yfir lausn reikningsfanga
description: Þessi grein veitir upplýsingar um lausnina fyrir innheimtu reikninga.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690991"
---
# <a name="invoice-capture-solution"></a>Lausn til að fanga reikninga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þessi grein veitir upplýsingar um reikningsfangalausnina sem býr sjálfkrafa til reikninga lánardrottna úr stafrænum reikningsmyndum.

Viðskiptaskuldir (AP) deild heldur utan um og vinnur úr reikningum fyrir vörur og þjónustu sem berast. AP endurskoðandi sannreynir gögn á reikningum söluaðila af eftirfarandi ástæðum:

- Til að koma í veg fyrir auka áreynslu ef þörf er á aðlögun eða leiðréttingum í lok tímabils
- Að greiða reikninga seljanda tímanlega og koma í veg fyrir fjárhagslegt tap vegna mistaka eða svika

Optical character recognition (OCR) hefur orðið mikið notað af mismunandi atvinnugreinum á undanförnum árum. Nú er algengt að prentaður texti sé stafrænn, þannig að hægt sé að breyta þeim rafrænt, leita í þeim, geyma á þéttari hátt og birta á netinu. Hægt er að nota stafræna textann í vélrænum ferlum eins og vitrænni tölvuvinnslu, vélþýðingu, texta í tal, lykilgögn og textanám.

Þróun gervigreindar (AI) tækni hefur gert nútíma OCR lausnum kleift að lesa mismunandi reikningasnið frá mismunandi söluaðilum án þess að krefjast mikillar mannlegrar íhlutunar. Fleiri fyrirtæki eru að viðurkenna að þau geta sparað fyrirhöfn og bætt nákvæmni með því að vinna reikninga með sjálfvirkni í stað þess að vinna handvirkt.

## <a name="system-landscape"></a>Kerfislandslag

Eftirfarandi mynd sýnir helstu íhluti og skref í lausninni fyrir innheimtu reikninga.

[![Íhlutir og skref í lausninni til að fanga reikninga.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Nauðsynleg hlutverk

Eftirfarandi tafla sýnir hlutverkin sem þarf til að setja upp og nota lausnina fyrir innheimtu reikninga.

| Hlutverk          | Aðgerðir | Kerfi | Hlutverkanöfn |
|---------------|---------|---------|-----------|
| Stjórnandi | <ul><li>Settu upp umhverfi í Microsoft Power Platform.</li><li>Settu upp lausnir í Microsoft Power Platform.</li><li>Settu upp tengingar milli Dynamics 365 og AI Builder.</li><li>Settu upp Azure Data Lake Storage staðsetningar.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365 stjórnandi</li><li>Power Platform-stjórnandi</li><li>Geymslu Blob gagnaeigandi</li></ul> |
| Gervigreind framleiðandi      | <ul><li>Viðhalda flæði.</li><li>Búðu til sérsniðin gervigreind módel.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Borgaragerðarmenn</li></ul> |
| AP skrifstofumaður      | <ul><li>Skoðaðu og gríptu til aðgerða á sviðsetningarsvæði reiknings lánardrottins.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Nýtt hlutverk AP afgreiðslumanns í Power Platform</li></ul> |
| AP skrifstofumaður      | <ul><li>Framkvæma daglegan rekstur sem AP skrifstofumaður.</li><li>Farðu í sviðsetningarsvæði reiknings lánardrottins.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Afgreiðslumaður viðskiptaskulda</li></ul> |
  
Fyrir frekari upplýsingar um uppsetningu reikningsfanga, sjá [Settu upp reikningsupptöku](../accounts-payable/install-invoice-capture.md).  
