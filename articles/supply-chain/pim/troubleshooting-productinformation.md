---
title: Úrræðaleit fyrir afurðarupplýsingar
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með afurðarupplýsingar.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5b74c1a769b3f0c3b848a034ed3d1bab76fda7eb5d8d62f4b3608d8706c696dc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778651"
---
# <a name="troubleshoot-product-information"></a>Úrræðaleit fyrir afurðarupplýsingar

Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með afurðarupplýsingar.

## <a name="i-cant-delete-a-released-product"></a>Ekki er hægt að eyða losaðri afurð.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Hægt er að eyða útgefinni afurð og öllum afbrigðum hennar aðeins ef útgefna afurðin er ekki með neinar tengdar færslur.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Fylgið eftirfarandi skrefum til að eyða útgefinni afurð eða afurðarsniðmáti.

1. Loka öllum opnum færslum fyrir vörurnar.
1. Minnka birgðir í 0 (núll).
1. Framkvæma birgðalokun.
1. Eyða öllum afurðarafbrigðum fyrir afurðarsniðmát sem á að eyða.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Get ég breytt vörunúmeri útgefinnar afurðar?

Í flestum tilfellum er ekki hægt að breyta vörunúmerum fyrir útgefnar afurðir vegna þess að slík breyting veldur því að gögn skemmist. Aðeins er hægt að breyta vörunúmeri ef nauðsynlegt er að gera við skemmd gögn sem fyrri endurnefning á aðallykli olli þeirri útgefnu afurð eins og minnst er á í listanum yfir [fjarlægðir eða úreltir eiginleikar fyrir Finance and Operations 10.0.0 með verkvangsuppfærslu 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).

Ef ætlunin er að breyta vörunúmerum fyrir útgefnar afurðir er hægt að [kjósa um þessa hugmynd í hugmyndagáttinni](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Sjálfgefna losunarreglan úr afurðinni er ekki færð inn í uppskriftarlínuna.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar vöru er bætt við uppskriftarlínu notar kerfið ekki sjálfgefnar upplýsingar um losunarreglu sem er sett upp fyrir vöruna. Með öðrum orðum birtist losunarregla afurðarinnar ekki á síðunni **Uppskriftarlína**.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Ef losunarregla er tilgreind í uppskriftarlínu, á hún við um þá uppskriftarlínu. Ef losunarreglan er hinsvegar auð, eða hún er ekki sett upp í uppskriftarlínu, mun losunarreglan sem er stillt fyrir vöruna samt eiga við þá uppskriftarlínu, jafnvel þótt hún sjáist ekki í uppskriftarlínunni.

Sjálfgefin reikniregla fyrir aðra eiginleika í Microsoft Dynamics 365 Supply Chain Management virkar yfirleitt ekki á þennan hátt. Hins vegar er ekki hægt að breyta núverandi hegðun. Annars gætu sumar fyrirliggjandi sérstillingar sem reiða sig á hana verið í ólagi.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Kerfið gerir mér kleift að vista tvítekin strikamerki fyrir mismunandi vörur eða sömu vöruna sem er með aðrar víddir.

Sem stendur framfylgir kerfið ekki einkvæmum strikamerkjum og viðbót þessarar takmörkunar myndi leiða til bilunar. Í reynd hefur Microsoft sannanir fyrir því að sumar núverandi uppsetningar viðskiptavinar myndu verða skemmast með þessari breytingu. Við munum hinsvegar íhuga víðtækari hönnunarbreytingu til að virkja þennan eiginleika í framtíðinni.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Ég fæ eftirfarandi villuboð: „Ekki er hægt að stofna staðsetningu vöruhúss vegna þess að varan er ekki á lager“. Velja skal framleiðsluvalkostinn Í birgðum í tengdum líkanaflokki ef ætlunin er að setja vörurnar í birgðir.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál á sér stað ef eftirfarandi skrefum er fylgt til að reyna að búa til sniðmát fyrir vöru sem ekki er í birgðum.

1. Opnið útgefna afurð sem er ekki til á lager.
1. Á aðgerðasvæðinu, í flipanum **Valkostir**, skal velja **Upplýsingar um færslu**.
1. Í svarglugganum **Upplýsingar um færslu** skal velja **Sniðmát fyrirtækjareikninga**.

Eftirfarandi villuboð birtast í þessu tilvikum:

> Ekki er hægt að stofna staðsetningu vöruhúss vegna þess að varan er ekki á lager. Velja skal framleiðsluvalkostinn Í birgðum í tengdum líkanaflokki ef ætlunin er að setja vörurnar í birgðir.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Ferlið við stofnun afurðasniðmáts krefst sérstakrar reiknireglu sem miðast við afurð. Þess vegna er ekki hægt að nota almenna hnappinn **Sniðmát fyrirtækjareikninga** í þessum tilgangi. Fylgdu þess í stað eftirfarandi skrefum.

1. Opna útgefna afurð.
1. Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Nýtt**, skal velja **Sniðmát \> Stofna samnýtt sniðmát**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Sjálfgefnum hjálpartexta sem er bætt við í afurðareigindir er ekki færður í útgefna afurð.

Lýsing og hjálpartexti sem bætt er við afurðareigindir eru ekki sýnilegir eða sjálfgefið færðir inn í útgefnar afurðir. Þessi hegðun er samkvæmt hönnuninni.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Sjálfgefið magn sem fært er inn er frábrugðið þegar það er skráð úr uppskrift og þegar það er skráð úr uppskriftarútgáfu.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Að sjálfgefnu, þegar vöru er bætt við uppskrift er magnið stillt á 1 í stað þess magns sem er skilgreint í reitnum **Lágmarks pöntunarmagn** á síðunni **Sjálfgefnar pöntunarstillingar** fyrir valda afurð. Þegar vöru er hinsvegar bætt við úr uppskriftarútgáfu og varan og afbrigðið er valið, tekur magnið sem er sjálfgefið fært inn með í reikninginn lágmarksmagnið sem er stillt í sjálfgefnum pöntunarstillingum fyrir tilteknar víddir.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Búist er við þessari hegðun. Sú staðreynd að reiknireglan sé ólík uppskriftinni og uppskriftarútgáfunni er hinsvegar þekkt vandamál. Þessari hegðun verður samt sem áður ekki breytt vegna þess að breyting gæti haft áhrif á margar ólíkar aðstæður viðskiptavina.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>Í upplýsingum um útgefna afurð get ég ekki breytt viðhengdum myndum sem hlaðið var upp úr gagnaeiningu fyrir viðhengi afurðarskjala.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál getur komið upp þegar mynd er hengd við vöru með því að nota gagnaeininguna *Viðhengd skjöl afurða*. Í þessu tilviki er vörumyndin sýnd fyrir vöruna. Ef þú velur hinsvegar **Breyta mynd** verður ekkert sýnt í listanum yfir myndir sem hlaðnar eru upp. Auk þess eru engin viðhengi sýnd fyrir vöruna.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Einingin *EcoResProductDocumentAttachmentEntity* (*Viðhengd skjöl afurða*) flytur inn viðhengd skjöl fyrir *afurðir* en ekki fyrir *útgefnar afurðir*. (Útgefnar afurðir eru einnig þekktar sem *vörur*.) Til að skoða viðhengi fyrir vöru á síðunni **Upplýsingar um losaðar afurðir** þarf að nota eininguna *EcoResReleasedProductDocumentAttachmentEntity* (*Viðhengd skjöl fyrir útgefnar afurðir*) í staðinn.

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Tengillinn Microsoft Flow sýnir eftirfarandi villuboð: „Uppfærsla ekki leyfð fyrir reit „ProductNumber“.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál á sér stað ef reynt er að uppfæra reitinn **Afurðarnúmer** með því að nota V2 eininguna *Útgefnar afurðir* og Microsoft Flow.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Búist er við þessari hegðun. Möguleikinn á að breyta afurðarnúmerinu fyrir útgefna afurð var fjarlægður í Dynamics 365 Finance and Operations 10.0.0 með verkvangsuppfærslu 24 til að hjálpa til við að koma í veg fyrir skemmdir á gögnum. Í undantekningartilfellum, þar sem nauðsynlegt er að lagfæra gagnaskemmdir sem voru gerðar af fyrri endurnefningu á aðallykli útgefinnar afurðar, geturðu beðið notendaþjónustu Microsoft um að fjarlægja takmörkunina tímabundið.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Ég get ekki stofnað útgefið afurðarafbrigði í öðrum lögaðila.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef reynt er að gefa út afurðarsniðmát án afbrigða og síðan stofna afbrigðin í hverjum lögaðila (fyrirtæki) fyrir sig eins og þarf að gera, þá geturðu ekki gefið út afbrigðin með því að nota uppástungur um afbrigði. Einnig verður ekki hægt að stofna afbrigðin handvirkt.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þessi hegðun er samkvæmt hönnuninni. Tengsl afurðarsniðmáts og víddanna sem sniðmátið getur tekið eru geymdar á samnýttu stigi. Þess vegna er ekki hægt að stofna tiltækar víddir fyrir samnýtt afurðarsniðmát í tilteknum lögaðila þar sem þessar víddir eru gefnar út og síðan endurtaka ferlið í hverjum lögaðila fyrir sig þar sem víddirnar eru nauðsynlegar. Þess í stað þarftu að breyta útgáfuferlinu til að aðlagast hönnunarferlinu.

Hér er ferlið fyrir losun afurða.

1. Stofnið samnýtt afurðarsniðmát og víddirnar sem hægt er að gefa út í lögaðilum.
1. Losið afurðirnar í lögaðilana annaðhvort með því að nota uppástungur um afbrigði eða bæta samsetningum handvirkt við sem á að losa.

Að öðrum kosti er hægt að stofna útgefna afurð með beinum hætti.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Þegar ég sleppi losa afbrigði í öðru fyrirtæki fæ ég eftirfarandi villuboð: „Afurðarafbrigði hefur þegar verið stofnað með tilgreindri vídd“.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef afurðarafbrigði hefur þegar verið losað í fyrirtæki A, og reynt er að losa það í fyrirtæki B með því að nota hnappinn **Nýtt** á síðunni **Útgefin afurðarafbrigði** koma upp eftirfarandi villuboð:

> Afurðarafbrigði hefur þegar verið stofnað með tilgreindri vídd.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Hnappurinn **Nýtt** á síðunni **Útgefin afurðarafbrigði** stofnar afbrigðið og losar það í samhengi fyrirtækisins. Ef afbrigðið hefur þegar verið stofnað er ekki hægt að nota hnappinn **Nýtt** til að losa það í annað fyrirtæki.

Til að laga vandamálið skal opna síðuna **Afurðarsniðmát** og velja **Losa afurð** til að losa fyrirliggjandi afbrigði í æskilegt fyrirtæki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]