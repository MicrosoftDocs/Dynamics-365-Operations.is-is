---
title: Yfirlit yfir Invoice capture-lausnar
description: Þessi grein veitir upplýsingar um lausn Invoice capture.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690991"
---
# <a name="invoice-capture-solution"></a>Lausn Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þessi grein veitir upplýsingar um lausn Invoice capture sem býr til lánardrottnareikninga sjálfkrafa úr stafrænum myndum af reikningum.

Deild viðskiptaskulda stjórnar og vinnur úr reikningum fyrir vörur og þjónustu sem eru móttekin. Endurskoðandi viðskiptaskulda staðfestir gögnin í reikningum lánardrottins af eftirfarandi ástæðum:

- Til að koma í veg fyrir aukakostnað ef þörf er á leiðréttingum eða lagfæringum við lok tímabilsins
- Til að greiða reikninga lánardrottins tímanlega og koma í veg fyrir fjárhagslegt tap vegna mistaka eða svika

Stafakennsl (OCR) hefur notið vaxandi vinsælda í mismunandi atvinnugreinum síðastliðin ár. Nú er algengt að prentaðir textar séu færðir yfir á stafrænt form þannig að hægt sé að breyta þeim rafrænt, leita að, geyma þá betur og sýna á netinu. Hægt er að nota stafræna textann í vélrænum ferlum eins og vitrænni tölvuvinnslu, vélþýðingu, upplestri, lykilgögnum og textanámi.

Þróun gervigreindartækni hefur gert nútímalegum lausnum stafakennsla að lesa mismunandi reikningssnið frá mismunandi lánardrottnum án þess að þurfa mikið mannlegt inngrip. Fleiri fyrirtæki viðurkenna að þau geti sparað vinnu og bætt nákvæmni með því að vinna úr reikningum með sjálfvirkni í stað þess að sinna handvirkri úrvinnslu.

## <a name="system-landscape"></a>Landslag kerfis

Eftirfarandi mynd sýnir helstu þætti og skref í lausn Invoice capture.

[![Þættir og skref í lausn Invoice capture.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Nauðsynleg hlutverk

Eftirfarandi tafla sýnir hlutverk sem þarf til að setja upp og nota lausn Invoice capture.

| Hlutverk          | Aðgerðir | Kerfi | Heiti hlutverks |
|---------------|---------|---------|-----------|
| Stjórnandi | <ul><li>Setja upp umhverfi í Microsoft Power Platform.</li><li>Nota lausnir í Microsoft Power Platform.</li><li>Settu upp tengingar á milli Dynamics 365 og AI Builder.</li><li>Setja upp Azure Data Lake Storage staðsetningar</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Stjórnandi Dynamics 365</li><li>Power Platform-stjórnandi</li><li>Eigandi Blob-gagna í geymslu</li></ul> |
| Gervigreindarmyndun      | <ul><li>Viðhalda flæðum.</li><li>Búðu til sérsniðin gervigreindarlíkön.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Citizen makers</li></ul> |
| Bókari viðskiptavina      | <ul><li>Farðu yfir og gríptu til aðgerða á biðsvæði lánardrottnareiknings.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Nýtt bókarahlutverk viðskiptaskulda í Power Platform</li></ul> |
| Bókari viðskiptavina      | <ul><li>Framkvæmdu daglegar aðgerðir sem bókari viðskiptaskulda.</li><li>Farðu á biðsvæði lánardrottnareikningsins.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Afgreiðslumaður viðskiptaskulda</li></ul> |
  
Frekari upplýsingar um uppsetningu reikningsupptöku er að finna í [Setja upp Invoice capture](../accounts-payable/install-invoice-capture.md).  
