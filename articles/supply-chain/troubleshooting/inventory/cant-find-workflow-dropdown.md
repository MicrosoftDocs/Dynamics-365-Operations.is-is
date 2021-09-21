---
title: Ekki er hægt að finna felligluggann „Verkflæði“ fyrir birgðabækur
description: Ekki er hægt að Verkflæði felligluggann á færslusíðunni eða tengdar verkflæðisaðgerðir eru ekki í boði
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476642"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Ekki er hægt að finna felligluggann „Verkflæði“ fyrir birgðabækur

## <a name="symptoms"></a>Einkenni

Ekki er hægt að **Verkflæði** felligluggann á færslusíðunni eða tengdar verkflæðisaðgerðir eru ekki í boði.

Þrjár ástæður geta verið fyrir þessu vandamáli eins og lýst er í eftirfarandi undirköflum.

## <a name="resolution-1"></a>Ályktun 1

Ef vandamálið á við alla notendur kann það að koma upp vegna þess að samþykktarverkflæði hefur ekki verið úthlutað á færslubókarheitið. Til að laga úr vandamálið skal fylgja þessum skrefum.

1. Farið í **Birgðastjórnun &gt; Uppsetning &gt; Færslubókarheiti &gt; Birgðir**.
1. Veljið heiti færslubókar úr listadálknum til að opna stillingasíðuna.
1. Á flipanum **Almennt** skal stilla **Samþykktarverkflæði** valkostinn á *Já*. Ef notandi er beðinn um að staðfesta breytinguna skal velja **Já**.
1. Í reitnum **Verkflæði** skal velja verkflæðið sem á að nota fyrir valið heiti færslubókar.

## <a name="resolution-2"></a>Ályktun 2

Ef verkflæðið notar sérsniðinn kóða gætu vandamál komið upp eftir uppfærslu á kerfinu. Í verkflæði færslubókar gæti til dæmis hnappurinn **Senda inn** verið skyggður þannig að ekki er hægt að velja hann til að samþykkja innsendingu.

Ef hnappurinn **Senda inn** er skyggður gæti verkflæðið hafa verið sérstillt, sem þýðir að aðferð verkflæðisins, `canSubmitToWorkflow()` í `FormDataUtil`, hafi verið stækkuð. Til að laga þetta vandamál skal breyta því hvernig aðferð er stækkuð fyrir `canSubmitToWorkflow()` til að nota skipulagið í eftirfarandi dæmi.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>Ályktun 3

Ef vandamálið á aðeins við fáa tiltekna notendur gætu þessir notendur ekki haft þau öryggisréttindi sem krafist er til að keyra verkflæðisaðgerðir á birgðabókum. Gangið úr skugga um að hver og neinn notandi hafi öryggisréttindin *Vinna með verkflæði í birgðabók*. Sjálfgefið er að þessum réttindum sé úthlutað á skyldu sem er með sama heiti og skyldan er notuð í hlutverkunum *Starfsmaður í vöruhúsi* og *Vöruhúsastjórnandi*.
